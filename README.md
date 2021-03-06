# Recommended Repository Layout

```
$/
  artifacts/
  docs/
  eng/
  lib/
  samples/
  src/
  tests/
  .editorconfig
  .gitignore
  .gitattributes
  Build.cmd
  build.sh
  nuget.Config
  README.md
  {solution}.sln
```

- `src` - Main projects (the product code)
- `tests` - Test projects
- `docs` - Documentation stuff, markdown files, help files etc.
- `samples` (optional) - Sample projects
- `lib` - Things that can **NEVER** exist in a nuget package
- `artifacts` - Build outputs go here. Doing a Build.cmd/build.sh generates artifacts here (nupkgs, dlls, pdbs, etc.)
- `eng` - Build customizations (custom msbuild files/psake/fake/albacore/etc) scripts
- `Build.cmd` - Bootstrap the build for windows
- `build.sh` - Bootstrap the build for *n