# jsconfig 配置说明

```json
{
  "compilerOptions": {
    "target": "es5", //目标打包成es5的代码
    "module": "esnext", //使用es的模块化
    "baseUrl": ".", // 基本目录，用于解析非相对模块名称
    "moduleResolution": "node", //模块的查找顺序按照node的顺序进行查找
    "experimentalDecorators": true, // 解决prettier对于装饰器语法的警告
    "paths": {
      // 指定要相对于 baseUrl 选项计算的路径映射 (路径别名), 支持vscode文件跳转
      "@/*": [
        "src/*"
      ]
    },
    // 可能会用的库
    "lib": [
      "esnext",
      "dom",
      "dom.iterable", // 使用可迭代对象有更有好的方法提示
      "scripthost" // 提供更友好的数组环境
    ]
  },
  //提高 IDE 性能
  "exclude": [
    "node_modules", "dist"
  ]
}
```


## compilerOptions配置

| 属性                         | 描述                                                         |
| :--------------------------- | :----------------------------------------------------------- |
| nolib                        | 不要包含默认的库文件(lib.d.ts)                               |
| target                       | 指定要使用的默认库(lib.d.ts)。值为 “es3”，"es5""es6""es2015”"es2016”，"es2017”，"es2018”，"es2019"，"es2020”，"esnext" |
| module                       | 在生成模块代码时指定模块系统。值为 ”amd”、”commonJS"，”es2015"，"es6"，”esnext"，”none"，"system"，"umd" |
| moduleResolution             | 指定如何解析导入模块。值为“node”和“classic'                  |
| checkJs                      | 启用 JavaScript 文件的类型检查                               |
| experimentalDecorators       | 为提议的 ES 装饰器提供实验支持                               |
| allowSyntheticDefaultlmports | 允许从没有默认导出的模块进行默认导入。这不影响代码，只是进行类型检查 |
| baseUr                       | 指定模块基础目录                                             |
| paths                        | 指定相对于模块路径别名映射                                   |


