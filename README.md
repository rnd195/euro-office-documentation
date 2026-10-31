# Euro-Office Documentation

Our documentation is automatically deployed at https://euro-office.github.io/documentation/

Source for the Euro-Office documentation site, built with
[MkDocs](https://www.mkdocs.org/) and the
[Material](https://squidfunk.github.io/mkdocs-material/) theme.

## Build locally

```bash
uv sync

uv run zensical serve
uv run zensical build --strict
```

`--strict` is what CI runs — it fails on broken links, missing pages, and
unused config keys.

## Authoring guidelines

- Never hard-code "Euro-Office", use `{{ brand.name }}` so rebranders inherit the change automatically.
- Internal component names (`DocService`, `FileConverter`, `sdkjs`) are
  product-internal and stay literal.
- Prefer Material's [admonitions](https://squidfunk.github.io/mkdocs-material/reference/admonitions/),
  [content tabs](https://squidfunk.github.io/mkdocs-material/reference/content-tabs/),
  and [code annotations](https://squidfunk.github.io/mkdocs-material/reference/code-blocks/#adding-annotations)
  over plain prose where they aid scanning.
