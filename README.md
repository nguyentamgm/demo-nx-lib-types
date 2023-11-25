This library was generated with [Nx](https://nx.dev).

---

### Let's start by generating a publishable library

`nx generate library sample-types --publishable --importPath=@nguyentamgm/sample-types`

Now we have `sample-types/` library generated

### Next, let's build some types from `sample-types/src/schemas/sample-schema.json`

```
# Move to our sample library directory
cd `sample-types/src`
# Generate type declaration file from schema
npx json2ts schemas/sample.schema.json types/sample.d.ts
```

### Publish to npm package

`nx publish sample-types --ver=1.0.0`

### Example of usage
`
import {ExampleDTO} from @nguyentamgm/sample-types;

const exampleDto: ExampleDTO = {
  firstName: "Foo",
  lastName: "Bar",
};
`

### To create a new npm package, just repeat the above process, basically this repo can contain multiple libraries