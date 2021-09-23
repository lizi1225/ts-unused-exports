# fork-ts-unused-exports

`fork-ts-unused-exports` The output file information is added on the basis of `ts-unused-exports`，the usage as the same as [ts-unused-exports](https://www.npmjs.com/package/ts-unused-exports)
## Installation

```
npm install --save-dev fork-ts-unused-exports
```

or, to install globally:

```
npm install -g fork-ts-unused-exports
```


```ts
import analyzeTsConfig from 'ts-unused-exports';
const result = analyzeTsConfig('path/to/tsconfig.json');
// or const result = analyzeTsConfig('path/to/tsconfig.json', ['file1.ts']);
// or const result = analyzeTsConfig('path/to/tsconfig.json', ['file1.ts', '--excludePathsFromReport=math']);

// result : {  allFiles: string[]; files: { [index:string] : ExportNameAndLocation[] }, importFiles: File[] } 
// interface ExportNameAndLocation {
//   exportName: string;
//   location: LocationInFile;
// }
// interface ExportNameAndLocation {
//   path: string;
//   fullPath: string;
//   imports: Imports;
//   exports: string[];
//   exportLocations: LocationInFile;
// }
```