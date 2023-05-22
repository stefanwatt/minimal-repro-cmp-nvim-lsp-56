# Minimal repro for [`#56`](https://github.com/hrsh7th/cmp-nvim-lsp/issues/56)

- open `foo.svelte` and `foo.ts`
- trigger cmp inside the string literal in `foo.svelte` with `ctrl+space` -> should suggest `"foo"` and `"bar"`
- comment the current code in `foo.ts` and uncomment the code marked as such
- trigger cmp again like before

Expected result: suggest "foo", "bar", "baz"
Actual result: suggest "foo", "bar"

