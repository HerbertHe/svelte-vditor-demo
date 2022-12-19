# svelte-vditor-demo

[English](./README.en.md) | [简体中文](./README.md)

Demo for using Vditor with Svelte, See the source code [here](./src/App.svelte)

## Usage

- initialize the project

```bash
# initialize the project
npx degit sveltejs/template my-svelte-project

# install dependencies
npm install
```

- modify the `head` element of `public/index.html` file, link the Vditor stylesheet

```diff
+ <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/vditor/dist/index.css"/>
```

- import the Vditor at the needed component

example: `src/App.svelte`

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

1. add the mounting element for Vditor
2. initialize the Vditor instance at the lifecycle `onMount` of the svelte component
