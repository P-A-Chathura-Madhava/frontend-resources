# Path Alias [compiler options]

> Define `baseUrl` & `paths` values in your jsconfig.json or tsconfig.json file to replace relative import paths inside your project with its path alias!

```
{
  "compilerOptions": {
    "baseUrl": "./",
    "paths": {
      "@components/*": ["components/*"],
      "@contexts/*": ["contexts/*"],
      "@configs/*": ["configs/*"],
      "@styles/*": ["styles/*"],
      "@libs/*": ["libs/*"]
    }
  }
}
```

## Sample usage:

```
import Homepage from "@components/templates/homepage.template";
import routeConfig from "@configs/route.config.json";
```

## Caveats:

- NextJS does not require external packages—you only need to update your jsconfig.json/tsconfig.json
- CRA setups could throw compiler errors when "baseUrl" is changed—you could choose a [workaround](https://gustavograeff1998.medium.com/absolute-imports-with-create-react-app-typescript-e87878cab65b)
- Using [module-alias](https://dev.to/larswaechter/path-aliases-with-typescript-in-nodejs-4353) package with NodeJS
