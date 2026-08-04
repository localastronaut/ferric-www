# ferric-www — preview build

Static preview of **ferric.works**, served at
<https://localastronaut.github.io/ferric-www/>.

This repo holds **built output only**. Do not edit it by hand — the source
lives in the private `Music-Apps` repo under `HQ/site`, and every file here is
overwritten on the next deploy.

To redeploy:

```bash
cd "HQ/site"
npm run build:pages      # BASE_PATH=/ferric-www astro build
# then copy dist/ into this repo, keep .nojekyll, commit, push
```

`.nojekyll` is required: Astro emits `_astro/`, and GitHub Pages' default
Jekyll pipeline ignores underscore-prefixed directories.
