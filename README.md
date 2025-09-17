## npm-ls-bug

`npm ls --all --omit=dev` includes devDependencies of dependent relative file: packages

```
❯ npm ls --all --omit=dev
npm-ls-bug@1.0.0
└─┬ utils@1.0.0 -> ./packages/utils
  └─┬ @swc/core@1.13.5
    ├── @swc/core-darwin-arm64@1.13.5
    ├── UNMET OPTIONAL DEPENDENCY @swc/core-darwin-x64@1.13.5
    ├── UNMET OPTIONAL DEPENDENCY @swc/core-linux-arm-gnueabihf@1.13.5
    ├── UNMET OPTIONAL DEPENDENCY @swc/core-linux-arm64-gnu@1.13.5
    ├── UNMET OPTIONAL DEPENDENCY @swc/core-linux-arm64-musl@1.13.5
    ├── UNMET OPTIONAL DEPENDENCY @swc/core-linux-x64-gnu@1.13.5
    ├── UNMET OPTIONAL DEPENDENCY @swc/core-linux-x64-musl@1.13.5
    ├── UNMET OPTIONAL DEPENDENCY @swc/core-win32-arm64-msvc@1.13.5
    ├── UNMET OPTIONAL DEPENDENCY @swc/core-win32-ia32-msvc@1.13.5
    ├── UNMET OPTIONAL DEPENDENCY @swc/core-win32-x64-msvc@1.13.5
    ├── @swc/counter@0.1.3
    ├── UNMET OPTIONAL DEPENDENCY @swc/helpers@>=0.5.17
    └─┬ @swc/types@0.1.25
      └── @swc/counter@0.1.3 deduped
```
