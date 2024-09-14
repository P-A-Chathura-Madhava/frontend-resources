# Component Structure

> We will breakdown our UI as Components: Atoms, Molecules, Organisms and the rest as Layouts & Templates

```
ui-core
 |__ components
        |__ atoms [ie: Button, FormField etc.]
        |__ molecules [ie: SearchBar(FormField + Button)]
        |__ organisms [ie: Popups, Drawer]
 |__ layouts [ie: section/page layouts]
 |__ templates [ie: section/page templates]
        |__ pages [ie: page templates]
```

---

## ui-core/components/atoms/Button

### Button

```
Button.component.tsx
Button.types.ts
index.ts
```

### Button - `index.ts`

```
export { default as Button } from './Button.component';
export type { ButtonProps } from './Button.types';
```

---

### atoms - `index.ts`

```
export * from './Button';
export * from './InputField';
```

### components - `index.ts`

```
export * from './atoms';
export * from './molecules';
export * from './organisms';
```

### ui-core - `index.ts`

```
export * from './components';
export * from './layouts';
export * from './templates';
```
