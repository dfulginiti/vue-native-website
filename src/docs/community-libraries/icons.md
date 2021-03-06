---
title: Icons
type: community-libraries
order: 1
vue_version: 2.5.13
# gz_size: "30.67"
---

Usage of icons in Vue Native.

• Import and use the already available icons from the `@expo/vector-icons` for CRNA projects or `react-native-vector-icons` for non-crna projects (remember to link).
• Use PNGs as icons to get your own customized icons running.

We will be showing both these methods here.

### @expo/vector-icons

First install the React Native Elements package using the following command:

```shell
npm install @expo/vector-icons
```

Then you simply import it inside your `script` section like this:

```js
import { Ionicons } from "react-native-elements";
```

Also add the `Ionicons` imported in the `components` block.

```js
<script>
import { Ionicons } from "@expo/vector-icons";
export default {
  components: {Ionicons},
}
</script>
```

If you want to use the imported `Ionicons` globally, you will have to import the `Vue` component from the `vue-native-core` library which is already there if you created your project using the `vue-native-cli`.

Use the `Vue.component` function in your root file `App.vue` to specify the component that will be used globally.

```js
import Vue from "vue-native-core";
Vue.component("ionicons", Ionicons);
```

Now you are ready to use the kebab-case equivalent of the import in your `template` with the desired icon.

```html
<template>
  <view class="container">
    <ionicons name="md-checkmark-circle" size=92 color="green" />
  </view>
</template>
```

### Icon images

If you know how to use the React Native `<Image>` component this will be a breeze.

```html
<template>
  <view class="container">
    <image
        :source="require('./logo.png')"
        class="imagestyle"
      />
  </view>
</template>
```

```css
<script>
.imagestyle{
  width: 100;
  height: 100;
}
</script>
```
