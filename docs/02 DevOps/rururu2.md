# Welcome123 to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).
 
``` py title="bubble_sort.py" hl_lines="2-4"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

``` yaml
# Code block content
# Welcome123 to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).
```

=== ":octicons-file-code-16: `docs/stylesheets/extra.css`"

    ``` css
    :root > * {
      --md-code-hl-string-color: #0FF1CE;
    }
    ```

=== ":octicons-file-code-16: `mkdocs.yml`"

    ``` yaml
    extra_css:
      - stylesheets/extra.css
    ```
