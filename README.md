# svelte-vditor-demo

在Svelte框架使用Vditor的demo, 源码详见 [App.svelte](./src/App.svelte)

## 使用过程

- 使用Svelte官方的举例, 初始化工程

```bash
# 初始化工程
npx degit sveltejs/template my-svelte-project

# 下载依赖
npm install
```

- 修改`public`目录下的`index.html`的`head`标签, 引入Vditor的通用样式

```diff
+ <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/vditor/dist/index.css"/>
```

- 在组件需要的地方引入Vditor

示例: `src/App.svelte`

```diff
<script>
+    import { onMount } from "svelte"
+    import Vditor from "vditor"

+    onMount(() => {
+        const vditor = new Vditor("vditor-container", {
+            theme: "classic",
+            minHeight: 600,
+        })
+    })
</script>

+<div id="vditor-container" />

<style>
</style>
```

1. 为Vditor添加挂载DOM
2. 在`onMount`生命周期引入Vditor初始化
