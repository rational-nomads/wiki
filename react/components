# 1. Creating Components

*(using the component DomainTable as an example)*

## a. File structure

* One folder per component in `src/components` - `src/components/DomainTable`
* Presentational component file should be title case - `DomainTable.tsx` *(some projects use index.tsx for simpler imports, but that can get messy when you have 10 index.tsx files open in your IDE)*
* [CSS Modules](https://create-react-app.dev/docs/adding-a-css-modules-stylesheet/) for styling - `[component name].module.css`, i.e. `DomainTable.module.css`
* Stateful container file (if needed) should be called `Container.tsx`
* If an asset is only present in the component you're making, create an `assets` folder in the component folder. If the asset is present in more than one component, put it in `public/assets`.
* All sub components (if needed) should be in `src/components/DomainTable/components`

## c. Exporting

We are using a design pattern called the [Barrel Pattern](https://basarat.gitbook.io/typescript/main-1/barrel) for our component exports. This pattern simplifies imports and exports of components - instead of having to call `import DomainTable from 'src/components/DomainTable/DomainTable`, we can just call `import { DomainTable } from 'src/components'`.

### Adding a component to the components barrel

1. Export your component as usual `export default DomainTable`
2. Add `export { default as DomainTable } from './DomainTable/DomainTable'`
*I have tried to group exports based on functionality, but just chuck them in Other for now as we will probably just alphabetise them at some point*

## d. Component styling

We are using [CSS Modules](https://create-react-app.dev/docs/adding-a-css-modules-stylesheet/), as they provide the greatest level of encapsulation.

There will be a main stylesheet at `src/styles/main.css` which contains colour values and some generic reusable classes, such as `border-primary`. Documentation here is missing - use other components as a reference for now (`FutureButton.module.css`, `ArrowLink.module.css`). `main.css` may be outdated, as the design has changed drastically since it was first made. Ping @colbr for questions regarding this.

### Guidelines
* Classes should be title case
* Refer to `styling` page in wiki (@todo add link)

---

# 2. Using Components

## a. Importing

We have absolute referencing enabled in our TSConfig, which means all inputs, unless starting with a `./`, will reference the `src/` folder. Alongside the barrel pattern (above), this makes component importing super simple.

`import { DomainTable } from 'components'`
`import { DomainTable, FutureButton, ArrowLink } from 'components'`
