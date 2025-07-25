# @plone/registry Release Notes

<!-- Do *NOT* add new change log entries to this file.
     You should create a file in the news directory instead.
     For helpful instructions, please see:
     https://6.docs.plone.org/contributing/index.html#contributing-change-log-label
-->

<!-- towncrier release notes start -->

## 3.0.0-alpha.4 (2025-06-25)

### Bugfix

- `getUtility` returns an empty object if called with a utility type that has not been registered. @davisagli [#7108](https://github.com/plone/volto/issues/7108)

## 3.0.0-alpha.3 (2025-05-13)

### Bugfix

- Return properly in `getUtility` and `getUtilities` in case `type` or `name` is not set. @sneridagh [#7007](https://github.com/plone/volto/issues/7007)
- Fixed `unRegisterSlotComponent` method. @sneridagh [#7016](https://github.com/plone/volto/issues/7016)
- Remove the slot registration from the array if it is the last in `unRegisterSlotComponent`. @sneridagh [#7031](https://github.com/plone/volto/issues/7031)

## 3.0.0-alpha.2 (2025-04-12)

### Feature

- New binary `init-loaders` initializes the `@plone/registry` loaders via the command line.
  This fixes the upgrade to 7.2.0 problem introduced in https://github.com/remix-run/react-router/issues/13078. @sneridagh [#6780](https://github.com/plone/volto/issues/6780)
- Support for Tailwind add-ons detection in Vite plugin. @sneridagh [#6797](https://github.com/plone/volto/issues/6797)
- Added i18n support for projects and add-ons (i18next) for Seven. @pnicolli [#6866](https://github.com/plone/volto/issues/6866)

## 3.0.0-alpha.1 (2025-03-31)

### Feature

- Allow to override slots with no predicate with the same name. @sneridagh [#6887](https://github.com/plone/volto/issues/6887)

## 3.0.0-alpha.0 (2025-03-27)

### Breaking

- Removed support for loading config from project. @sneridagh

  Please see the [upgrade guide](https://6.docs.plone.org/volto/upgrade-guide/index.html)
  for more information. [#6842](https://github.com/plone/volto/issues/6842)

### Internal

- Fix typings for Vite Plugin. @sneridagh [#6733](https://github.com/plone/volto/issues/6733)

## 2.4.1 (2025-02-08)

### Internal

- Update Vite version. @sneridagh [#6640](https://github.com/plone/volto/issues/6640)
- Update internal `peerDependencies` to include React 19.
  Update TS version. @sneridagh [#6641](https://github.com/plone/volto/issues/6641)
- Remove `react` as a hard dependency, use `peerDependencies` instead.  @sneridagh [#6728](https://github.com/plone/volto/issues/6728)

## 2.4.0 (2025-01-31)

### Feature

- Added add-ons styles loader. @sneridagh [#6630](https://github.com/plone/volto/issues/6630)

## 2.3.0 (2025-01-24)

### Feature

- Added route registry. @sneridagh [#6600](https://github.com/plone/volto/issues/6600)

### Documentation

- Document the route API. @sneridagh [#6604](https://github.com/plone/volto/issues/6604)

## 2.2.0 (2024-12-12)

### Feature

- Added an experimental Vite plugin for the registry. @sneridagh [#6409](https://github.com/plone/volto/issues/6409)

### Documentation

- `html_use_opensearch` value must not have a trailing slash. Clean up comments. @stevepiercy [#6502](https://github.com/plone/volto/issues/6502)

## 2.1.2 (2024-11-05)

### Bugfix

- Fix weird typings issue happening in docker build but not locally. @sneridagh [#6471](https://github.com/plone/volto/issues/6471)

### Internal

- Improve packaging. @sneridagh 

## 2.1.1 (2024-11-05)

### Internal

- Repackage registry, the previous build was including the docs. @sneridagh 

## 2.1.0 (2024-11-05)

### Feature

- Allow any type `js`, `cjs`, `mjs`, `ts` as configuration for the add-on registry. @sneridagh [#6458](https://github.com/plone/volto/issues/6458)

### Bugfix

- Fix ERR_REQUIRE from ESM module requiring CJS module. @sneridagh [#6458](https://github.com/plone/volto/issues/6458)
- Fix types for add-on's TypeScript. Fix `.tsconfig` for Node.js side. @sneridagh [#6461](https://github.com/plone/volto/issues/6461)

### Internal

- Replace `parcel` with `tsup` for build. @sneridagh [#6461](https://github.com/plone/volto/issues/6461)

## 2.0.0 (2024-10-31)

### Internal

- Release 2.0.0 @sneridagh 

## 2.0.0-alpha.0 (2024-10-27)

### Breaking

- Moved the package to ESM and refactored the add-on registry scripts to TypeScript. @sneridagh
  Breaking:
  - For maximum compatibility with CommonJS builds, the default exports have been moved to named exports.
  - The modules affected are now built, and the import paths have changed, too.
  - These changes force the modification in imports in a couple of files.
  Please see the [Upgrade Guide](https://6.docs.plone.org/volto/upgrade-guide/index.html). [#6399](https://github.com/plone/volto/issues/6399)

### Feature

- Added an experimental Vite plugin. @sneridagh [#6399](https://github.com/plone/volto/issues/6399)

### Bugfix

- Return empty array when `getUtilities` does not match anything. @sneridagh [#6422](https://github.com/plone/volto/issues/6422)

### Internal

- Update typescript @sneridagh [#6371](https://github.com/plone/volto/issues/6371)
- Update Vite and vitest versions @sneridagh [#6373](https://github.com/plone/volto/issues/6373)
- Update typescript and vitest everywhere @sneridagh [#6407](https://github.com/plone/volto/issues/6407)

## 1.8.0 (2024-07-30)

### Feature

- Added `Utilities` registry for `registerUtility`, `getUtility`, and `getUtilities`. @sneridagh [#6161](https://github.com/plone/volto/issues/6161)

### Documentation

- Changed a few typos within documentation, README's and comments. @FritzHoing [#6109](https://github.com/plone/volto/issues/6109)

## 1.7.0 (2024-06-26)

### Feature

- Improve shadowing by including the support for js->jsx extensions in old shadows. This allow support for upcoming renaming of files that should be jsx and are js. @sneridagh [#6113](https://github.com/plone/volto/issues/6113)

## 1.6.0 (2024-06-13)

### Feature

- Add support for reading the add-ons `tsconfig.json` paths and add them to the build resolve aliases @sneridagh [#6096](https://github.com/plone/volto/issues/6096)

## 1.5.7 (2024-05-15)

### Bugfix

- Fix type for component registry components @sneridagh [#6002](https://github.com/plone/volto/issues/6002)

### Internal

- Saner defaults for building deps, switch default to cached, add `build:force` command @sneridagh [#5980](https://github.com/plone/volto/issues/5980)

## 1.5.6 (2024-04-23)

### Bugfix

- Remove `parcel-optimizer-react-client` plugin @sneridagh [#5887](https://github.com/plone/volto/issues/5887)

### Internal

- Improvements to the monorepo setup with utilities, especially ESLint. Build cached option to speedup operations. @sneridagh [#5969](https://github.com/plone/volto/issues/5969)

## 1.5.5 (2024-04-03)

### Bugfix

- Fix registry wrong default primitive type @sneridagh [#5925](https://github.com/plone/volto/issues/5925)

### Internal

- Sync TypeScript version @sneridagh [#5912](https://github.com/plone/volto/issues/5912)

## 1.5.4 (2024-03-21)

### Bugfix

- - Fix slots reordering function for "before" and "after" keyword @steffenri [#5840](https://github.com/plone/volto/issues/5840)

## 1.5.3 (2024-03-19)

### Bugfix

- Cross-package manager Volto path resolver in `webpack-relative-resolver` @sneridagh [#5893](https://github.com/plone/volto/issues/5893)

## 1.5.2 (2024-03-05)

### Bugfix

- Fix issue with HMR and register the same predicate-less component again @sneridagh [#5832](https://github.com/plone/volto/issues/5832)

## 1.5.1 (2024-03-02)

### Bugfix

- Upgrade parcel @sneridagh [#5822](https://github.com/plone/volto/issues/5822)

## 1.5.0 (2024-03-01)

### Feature

- Upgrade Volto core to use React 18.2.0 @sneridagh [#3221](https://github.com/plone/volto/issues/3221)

## 1.4.0 (2024-03-01)

### Feature

- Support for slots @tiberiuichim @sneridagh [#5775](https://github.com/plone/volto/issues/5775)

## 1.3.1 (2024-02-20)

### Bugfix

- Export ConfigType @sneridagh [#5774](https://github.com/plone/volto/issues/5774)

## 1.3.0 (2024-02-18)

### Feature

- Add `VOLTOCONFIG` environment variable. @sneridagh [#5752](https://github.com/plone/volto/issues/5752)

## 1.2.2 (2024-02-02)

### Bugfix

- Remove `lodash` as a dependency @sneridagh [#5726](https://github.com/plone/volto/issues/5726)

## 1.2.1 (2024-01-17)

### Bugfix

- Fix order of preference in addons-registry for the theme definition (THEME, volto.config.js, package.json) @sneridagh [#5649](https://github.com/plone/volto/issues/5649)

## 1.2.0 (2024-01-02)

### Feature

- Support for cross-JS/TS aliases in the add-on registry aliases generator @sneridagh [#5532](https://github.com/plone/volto/issues/5532)

### Internal

- ESlint general improvements @sneridagh [#5548](https://github.com/plone/volto/issues/5548)

## 1.1.0 (2023-12-13)

### Internal

- Move and unify Types under @plone/types @sneridagh [#5493](https://github.com/plone/volto/issues/5493)

## 1.0.1 (2023-12-02)

### Bugfix

- Initialize only the development addons present in `compilerOptions.paths` filtered by the add-ons registered @sneridagh [#5463](https://github.com/plone/volto/issues/5463)

### Internal

- Cleaned up Registry and renamed `packagesFolderAddons` to `coreAddons`. @sneridagh [#5456](https://github.com/plone/volto/issues/5456)
- Moved @plone/types to `devDependencies` @sneridagh [#5485](https://github.com/plone/volto/issues/5485)

## 1.0.0 (2023-11-05)

### Feature

- Moved add-on registry to its own package. @sneridagh
  Initial Release @sneridagh [#4949](https://github.com/plone/volto/issues/4949)
