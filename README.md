# Temporary redirection repo for docs.oasis.dev -> docs.oasis.io

This is a temporary redirects repository from docs.oasis.dev -> docs.oasis.io.
Remove the repository after Sep 2023 or sooner, if other redirection mechanism
is implemented.

Commands used to generate redirection page:

```sh
for f in `find . -name index.html`; do cp template.phtml $f; done
for f in `find . -name index.html`; do p=${f:1:-11}; echo $p; sed -i "s|PLACEHOLDER|https\://docs.oasis.io$p|i" $f; done
```
