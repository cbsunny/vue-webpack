TypeScript 不认识 .vue 结尾的文件，为了让其支持 import App from './App.vue' 导入语句，还需要以下文件 vue-shims.d.ts 去定义 .vue 的类型：

```
// 告诉 TypeScript 编译器 .vue 文件其实是一个 Vue  
declare module "*.vue" {
  import Vue from "vue";
  export default Vue;
}
```