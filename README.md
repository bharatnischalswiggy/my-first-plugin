## @superset-ui/plugin-chart-my-first-plugin

[![Version](https://img.shields.io/npm/v/@superset-ui/plugin-chart-my-first-plugin.svg?style=flat-square)](https://www.npmjs.com/package/@superset-ui/plugin-chart-my-first-plugin)

This plugin provides My First Plugin for Superset.

### Usage

Configure `key`, which can be any `string`, and register the plugin. This `key` will be used to lookup this chart throughout the app.

```js
import MyFirstPluginChartPlugin from '@superset-ui/plugin-chart-my-first-plugin';

new MyFirstPluginChartPlugin()
  .configure({ key: 'my-first-plugin' })
  .register();
```

Then use it via `SuperChart`. See [storybook](https://apache-superset.github.io/superset-ui/?selectedKind=plugin-chart-my-first-plugin) for more details.

```js
<SuperChart
  chartType="my-first-plugin"
  width={600}
  height={600}
  formData={...}
  queriesData={[{
    data: {...},
  }]}
/>
```

### File structure generated

```
├── package.json
├── README.md
├── tsconfig.json
├── src
│   ├── MyFirstPlugin.tsx
│   ├── images
│   │   └── thumbnail.png
│   ├── index.ts
│   ├── plugin
│   │   ├── buildQuery.ts
│   │   ├── controlPanel.ts
│   │   ├── index.ts
│   │   └── transformProps.ts
│   └── types.ts
├── test
│   └── index.test.ts
└── types
    └── external.d.ts
```
# my-first-plugin
