# How `rendered.html` was produced

The kb export (`src/` only — no `package.json`, no build config) can't be run as a
real SvelteKit site. `rendered.html` is a static server-render of `+page.svx` through
the kb's own `runbook` layout, built with a throwaway Vite + mdsvex + Svelte 5
scaffold that:

- preprocesses `+page.svx` with `mdsvex`,
- aliases `#lib` to the export's `src/lib` unchanged,
- server-renders `<Layout {...metadata}><Page /></Layout>` with Svelte 5's
  `svelte/server` `render()`,
- inlines the layout's and components' own `<style>` blocks (CSS isn't emitted by a
  plain SSR string render).

Nothing in `causes.ts`, `desk-notes.json`, or `reports-4471.json` was modified. The
`<CauseTable ticket={4471} />` numbers in the rendered page are computed live by the
kb's own logic, the same way the original `/kb/incidents/4471` page computes its own
numbers.
