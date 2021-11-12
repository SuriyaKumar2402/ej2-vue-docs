# Theming

The Syncfusion Vue library has provided the below list of in-built themes,

1. Google’s Material
2. Microsoft Office’s Fabric
3. Bootstrap
4. Bootstrap v4
5. Bootstrap v5
6. High Contrast
7. Tailwind CSS

> The Syncfusion Bootstrap theme is designed based on `Bootstrap v3`, however, it can be compatible with `Bootstrap v4` applications. In addition to these four built-in themes, [ThemeStudio](https://ej2.syncfusion.com/vue/documentation/appearance/theme-studio/) provides support for the Fusion Theme that can only be downloaded from [ThemeStudio](https://ej2.syncfusion.com/themestudio/?theme=fusion).

Themes are shipped as individual and combined CSS files. Combined CSS file can be referred from the npm package `@syncfusion/ej2` and individual CSS files are available within same component repository’s `style` folder. In ej2 npm packages, we have shipped both CSS and SCSS files for all components.

Referring All components CSS

```css
@import "./node_modules/@syncfusion/ej2/<theme_name>.css";
```

Referring All components SCSS

```scss
@import "ej2/<theme_name>.scss";
```

## Referring individual control theme

We can get the individual theme from the individual npm package or from an overall ej2 npm package.

Referring individual control from individual package

```scss
@import "<dependent-package>/<dependent-control>/<theme_name>.scss";
@import "ej2-buttons/styles/button/<theme_name>.scss";
```

**Example:**

```scss
@import "ej2-base/styles/material.scss";
@import "ej2-buttons/styles/button/material.scss";
```

> `ej2-base` is common dependent package for all Syncfusion JavaScript control styles. So, it needs first to be added in the import statement.

Referring individual control from ej2 package

```scss
@import "ej2/<dependent-control>/<theme_name>.scss";
@import "ej2/button/<theme_name>.scss";
```

**Example:**

```scss
@import "ej2/base/material.scss";
@import "ej2/button/material.scss";
```

> The individual control theme will not include its dependent control styles. I.e. The dependent controls theme should be added before adding the individual control themes.

## Common Variables

The below list of common variables used in the Syncfusion Vue library themes for all components. You can change these variables to customize the corresponding theme.

### Google's Material

| Name | Value |
| ------------- | ------------- |
| `$accent` | ![#e3165b](https://ej2.syncfusion.com/download/documentation/svg/e3165b.svg) `#e3165b` |
| `$accent-font` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$primary` | ![#3f51b5](https://ej2.syncfusion.com/download/documentation/svg/3f51b5.svg) `#3f51b5` |
| `$primary-50` | ![#e8eaf6](https://ej2.syncfusion.com/download/documentation/svg/e8eaf6.svg) `#e8eaf6` |
| `$primary-100` | ![#c5cae9](https://ej2.syncfusion.com/download/documentation/svg/c5cae9.svg) `#c5cae9` |
| `$primary-200` | ![#9fa8da](https://ej2.syncfusion.com/download/documentation/svg/9fa8da.svg) `#9fa8da` |
| `$primary-300` | ![#7986cb](https://ej2.syncfusion.com/download/documentation/svg/7986cb.svg) `#7986cb` |
| `$primary-font` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$primary-50-font` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$primary-100-font` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$primary-200-font` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$primary-300-font` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$grey-white` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$grey-black` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$grey-50` | ![#fafafa](https://ej2.syncfusion.com/download/documentation/svg/fafafa.svg) `#fafafa` |
| `$grey-100` | ![#f5f5f5](https://ej2.syncfusion.com/download/documentation/svg/f5f5f5.svg) `#f5f5f5` |
| `$grey-200` | ![#eeeeee](https://ej2.syncfusion.com/download/documentation/svg/eeeeee.svg) `#eeeeee` |
| `$grey-300` | ![#e0e0e0](https://ej2.syncfusion.com/download/documentation/svg/e0e0e0.svg) `#e0e0e0` |
| `$grey-400` | ![#bdbdbd](https://ej2.syncfusion.com/download/documentation/svg/bdbdbd.svg) `#bdbdbd` |
| `$grey-500` | ![#9e9e9e](https://ej2.syncfusion.com/download/documentation/svg/9e9e9e.svg) `#9e9e9e` |
| `$grey-600` | ![#757575](https://ej2.syncfusion.com/download/documentation/svg/757575.svg) `#757575` |
| `$grey-700` | ![#616161](https://ej2.syncfusion.com/download/documentation/svg/616161.svg) `#616161` |
| `$grey-800` | ![#424242](https://ej2.syncfusion.com/download/documentation/svg/424242.svg) `#424242` |
| `$grey-900` | ![#212121](https://ej2.syncfusion.com/download/documentation/svg/212121.svg) `#212121` |
| `$grey-dark` | ![#303030](https://ej2.syncfusion.com/download/documentation/svg/303030.svg) `#303030` |
| `$grey-light-font` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$grey-dark-font` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$base-font` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$error-font` | ![#f44336](https://ej2.syncfusion.com/download/documentation/svg/f44336.svg) `#f44336` |

### Microsoft Office’s Fabric

| Name | Value |
| ------------- | ------------- |
| `$theme-primary` | ![#0078d7](https://ej2.syncfusion.com/download/documentation/svg/f44336.svg) `#0078d7` |
| `$theme-dark-alt` | ![#006fc7](https://ej2.syncfusion.com/download/documentation/svg/006fc7.svg) `darken($theme-primary, 3%)` |
| `$theme-dark` | ![#005ba3](https://ej2.syncfusion.com/download/documentation/svg/005ba3.svg) `darken($theme-primary, 10%)` |
| `$theme-darker` | ![#00457a](https://ej2.syncfusion.com/download/documentation/svg/00457a.svg) `darken($theme-primary, 18%)` |
| `$theme-secondary` | ![#0081e5](https://ej2.syncfusion.com/download/documentation/svg/0081e5.svg) `lighten($theme-primary, 3%)` |
| `$theme-tertiary` | ![#42acff](https://ej2.syncfusion.com/download/documentation/svg/42acff.svg) `lighten($theme-primary, 21%)` |
| `$theme-light` | ![#b7e0ff](https://ej2.syncfusion.com/download/documentation/svg/b7e0ff.svg) `lighten($theme-primary, 44%)` |
| `$theme-lighter` | ![#d1ebff](https://ej2.syncfusion.com/download/documentation/svg/d1ebff.svg) `lighten($theme-primary, 49%)` |
| `$theme-lighter-alt` | ![#aliceblue](https://ej2.syncfusion.com/download/documentation/svg/aliceblue.svg) `lighten($theme-primary, 55%)` |
| `$neutral-white` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$neutral-lighter-alt` | ![#f8f8f8](https://ej2.syncfusion.com/download/documentation/svg/f8f8f8.svg) `#f8f8f8` |
| `$neutral-lighter` | ![#f4f4f4](https://ej2.syncfusion.com/download/documentation/svg/f4f4f4.svg) `#f4f4f4` |
| `$neutral-light` | ![#eaeaea](https://ej2.syncfusion.com/download/documentation/svg/eaeaea.svg) `#eaeaea` |
| `$neutral-quintenaryalt` | ![#dadada](https://ej2.syncfusion.com/download/documentation/svg/dadada.svg) `#dadada` |
| `$neutral-quintenary` | ![#d0d0d0](https://ej2.syncfusion.com/download/documentation/svg/d0d0d0.svg) `#d0d0d0` |
| `$neutral-tertiary-alt` | ![#c8c8c8](https://ej2.syncfusion.com/download/documentation/svg/c8c8c8.svg) `#c8c8c8` |
| `$neutral-tertiary` | ![#a6a6a6](https://ej2.syncfusion.com/download/documentation/svg/a6a6a6.svg) `#a6a6a6` |
| `$neutral-secondary-alt` | ![#767676](https://ej2.syncfusion.com/download/documentation/svg/767676.svg) `#767676` |
| `$neutral-secondary` | ![#666666](https://ej2.syncfusion.com/download/documentation/svg/666666.svg) `#666666` |
| `$neutral-primary` | ![#333333](https://ej2.syncfusion.com/download/documentation/svg/333333.svg) `#333333` |
| `$neutral-dark` | ![#212121](https://ej2.syncfusion.com/download/documentation/svg/212121.svg) `#212121` |
| `$neutral-black` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$alert-bg` | ![#deecf9](https://ej2.syncfusion.com/download/documentation/svg/deecf9.svg) `#deecf9` |
| `$error-bg` | ![#fde7e9](https://ej2.syncfusion.com/download/documentation/svg/fde7e9.svg) `#fde7e9` |
| `$success-bg` | ![#dff6dd](https://ej2.syncfusion.com/download/documentation/svg/dff6dd.svg) `#dff6dd` |
| `$theme-dark-font` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$theme-primary-font` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$theme-light-font` | ![#333333](https://ej2.syncfusion.com/download/documentation/svg/333333.svg) `#333333` |
| `$neutral-light-font` | ![#333333](https://ej2.syncfusion.com/download/documentation/svg/333333.svg) `#333333` |
| `$neutral-light-fontalt` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$grey-dark-font` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$base-font` | ![#333333](https://ej2.syncfusion.com/download/documentation/svg/333333.svg) `#333333` |
| `$message-font` | ![#333333](https://ej2.syncfusion.com/download/documentation/svg/333333.svg) `#333333` |
| `$alert-font` | ![#d83b01](https://ej2.syncfusion.com/download/documentation/svg/d83b01.svg) `#d83b01` |
| `$error-font` | ![#a80000](https://ej2.syncfusion.com/download/documentation/svg/a80000.svg) `#a80000` |
| `$success-font` | ![#107c10](https://ej2.syncfusion.com/download/documentation/svg/107c10.svg) `#107c10` |

### Bootstrap

| Name | Value |
| ------------- | ------------- |
| `$brand-primary` | ![#317ab9](https://ej2.syncfusion.com/download/documentation/svg/317ab9.svg) `#317ab9` |
| `$brand-primary-darken-10` | ![#3071a9](https://ej2.syncfusion.com/download/documentation/svg/3071a9.svg) `#3071a9` |
| `$brand-primary-darken-15` | ![#2a6496](https://ej2.syncfusion.com/download/documentation/svg/2a6496.svg) `#2a6496` |
| `$brand-primary-darken-25` | ![#1f496e](https://ej2.syncfusion.com/download/documentation/svg/1f496e.svg) `#1f496e` |
| `$brand-primary-darken-35` | ![#142f46](https://ej2.syncfusion.com/download/documentation/svg/142f46.svg) `#142f46` |
| `$brand-primary-font` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$grey-base` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$grey-darker` | ![#222222](https://ej2.syncfusion.com/download/documentation/svg/222222.svg) `#222222` |
| `$grey-dark` | ![#333333](https://ej2.syncfusion.com/download/documentation/svg/333333.svg) `#333333` |
| `$grey` | ![#555555](https://ej2.syncfusion.com/download/documentation/svg/555555.svg) `#555555` |
| `$grey-light` | ![#777777](https://ej2.syncfusion.com/download/documentation/svg/777777.svg) `#777777` |
| `$grey-44` | ![#444444](https://ej2.syncfusion.com/download/documentation/svg/444444.svg) `#444444` |
| `$grey-88` | ![#888888](https://ej2.syncfusion.com/download/documentation/svg/888888.svg) `#888888` |
| `$grey-99` | ![#999999](https://ej2.syncfusion.com/download/documentation/svg/999999.svg) `#999999` |
| `$grey-8c` | ![#8c8c8c](https://ej2.syncfusion.com/download/documentation/svg/8c8c8c.svg) `#8c8c8c` |
| `$grey-ad` | ![#adadad](https://ej2.syncfusion.com/download/documentation/svg/adadad.svg) `#adadad` |
| `$grey-dark-font` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$grey-white` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$grey-lighter` | ![#eeeeee](https://ej2.syncfusion.com/download/documentation/svg/eeeeee.svg) `#eeeeee` |
| `$grey-f9` | ![#f9f9f9](https://ej2.syncfusion.com/download/documentation/svg/f9f9f9.svg) `#f9f9f9` |
| `$grey-f8` | ![#f8f8f8](https://ej2.syncfusion.com/download/documentation/svg/f8f8f8.svg) `#f8f8f8` |
| `$grey-f5` | ![#f5f5f5](https://ej2.syncfusion.com/download/documentation/svg/f5f5f5.svg) `#f5f5f5` |
| `$grey-e6` | ![#e6e6e6](https://ej2.syncfusion.com/download/documentation/svg/e6e6e6.svg) `#e6e6e6` |
| `$grey-dd` | ![#dddddd](https://ej2.syncfusion.com/download/documentation/svg/dddddd.svg) `#dddddd` |
| `$grey-d4` | ![#d4d4d4](https://ej2.syncfusion.com/download/documentation/svg/d4d4d4.svg) `#d4d4d4` |
| `$grey-cc` | ![#cccccc](https://ej2.syncfusion.com/download/documentation/svg/cccccc.svg) `#cccccc` |
| `$grey-light-font` | ![#333333](https://ej2.syncfusion.com/download/documentation/svg/333333.svg) `#333333` |
| `$brand-success` | ![#5cb85c](https://ej2.syncfusion.com/download/documentation/svg/5cb85c.svg) `#5cb85c` |
| `$brand-success-dark` | ![#3c763d](https://ej2.syncfusion.com/download/documentation/svg/3c763d.svg) `#3c763d` |
| `$brand-info` | ![#5bc0de](https://ej2.syncfusion.com/download/documentation/svg/5bc0de.svg) `#5bc0de` |
| `$brand-info-dark` | ![#31708f](https://ej2.syncfusion.com/download/documentation/svg/31708f.svg) `#31708f` |
| `$brand-warning` | ![#f0ad4e](https://ej2.syncfusion.com/download/documentation/svg/f0ad4e.svg) `#f0ad4e` |
| `$brand-warning-dark` | ![#8a6d3b](https://ej2.syncfusion.com/download/documentation/svg/8a6d3b.svg) `#8a6d3b` |
| `$brand-danger` | ![#d9534f](https://ej2.syncfusion.com/download/documentation/svg/d9534f.svg) `#d9534f` |
| `$brand-danger-dark` | ![#a94442](https://ej2.syncfusion.com/download/documentation/svg/a94442.svg) `#a94442` |
| `$brand-success-light` | ![#dff0d8](https://ej2.syncfusion.com/download/documentation/svg/dff0d8.svg) `#dff0d8` |
| `$brand-info-light` | ![#d9edf7](https://ej2.syncfusion.com/download/documentation/svg/d9edf7.svg) `#d9edf7` |
| `$brand-warning-light` | ![#fcf8e3](https://ej2.syncfusion.com/download/documentation/svg/fcf8e3.svg) `#fcf8e3` |
| `$brand-danger-light` | ![#f2dede](https://ej2.syncfusion.com/download/documentation/svg/f2dede.svg) `#f2dede` |
| `$input-border-focus` | ![#66afe9](https://ej2.syncfusion.com/download/documentation/svg/66afe9.svg) `#66afe9` |
| `$brand-success-font` | ![#3c763d](https://ej2.syncfusion.com/download/documentation/svg/3c763d.svg) `#3c763d` |
| `$brand-info-font` | ![#31708f](https://ej2.syncfusion.com/download/documentation/svg/31708f.svg) `#31708f` |
| `$brand-warning-font` | ![#8a6d3b](https://ej2.syncfusion.com/download/documentation/svg/8a6d3b.svg) `#8a6d3b` |
| `$brand-danger-font` |![#a94442](https://ej2.syncfusion.com/download/documentation/svg/a94442.svg) `#a94442` |
| `$base-font` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |

### Bootstrap 4

| Name | Value |
| ------------- | ------------- |
| `$white` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$gray-100` | ![#f8f9fa](https://ej2.syncfusion.com/download/documentation/svg/f8f9fa.svg) `#f8f9fa` |
| `$gray-200` | ![#e9ecef](https://ej2.syncfusion.com/download/documentation/svg/e9ecef.svg) `#e9ecef` |
| `$gray-300` | ![#dee2e6](https://ej2.syncfusion.com/download/documentation/svg/dee2e6.svg) `#dee2e6` |
| `$gray-400` | ![#ced4da](https://ej2.syncfusion.com/download/documentation/svg/ced4da.svg) `#ced4da` |
| `$gray-500` | ![#adb5bd](https://ej2.syncfusion.com/download/documentation/svg/adb5bd.svg) `#adb5bd` |
| `$gray-600` | ![#6c757d](https://ej2.syncfusion.com/download/documentation/svg/6c757d.svg) `#6c757d` |
| `$gray-700` | ![#495057](https://ej2.syncfusion.com/download/documentation/svg/495057.svg) `#495057` |
| `$gray-800` | ![#343a40](https://ej2.syncfusion.com/download/documentation/svg/343a40.svg) `#343a40` |
| `$gray-900` | ![#212529](https://ej2.syncfusion.com/download/documentation/svg/212529.svg) `#212529` |
| `$black` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$blue` | ![#007bff](https://ej2.syncfusion.com/download/documentation/svg/007bff.svg) `#007bff` |
| `$indigo` | ![#6610f2](https://ej2.syncfusion.com/download/documentation/svg/6610f2.svg) `#6610f2` |
| `$purple` | ![#6f42c1](https://ej2.syncfusion.com/download/documentation/svg/6f42c1.svg) `#6f42c1` |
| `$pink` | ![#e83e8c](https://ej2.syncfusion.com/download/documentation/svg/e83e8c.svg) `#e83e8c` |
| `$red` | ![#dc3545](https://ej2.syncfusion.com/download/documentation/svg/dc3545.svg) `#dc3545` |
| `$orange` | ![#fd7e14](https://ej2.syncfusion.com/download/documentation/svg/fd7e14.svg) `#fd7e14` |
| `$yellow` | ![#ffc107](https://ej2.syncfusion.com/download/documentation/svg/ffc107.svg) `#ffc107` |
| `$green` | ![#28a745](https://ej2.syncfusion.com/download/documentation/svg/28a745.svg) `#28a745` |
| `$teal` | ![#20c997](https://ej2.syncfusion.com/download/documentation/svg/20c997.svg) `#20c997` |
| `$cyan` | ![#17a2b8](https://ej2.syncfusion.com/download/documentation/svg/17a2b8.svg) `#17a2b8` |

### Bootstrap 5

| Name | Value |
| ------------- | ------------- |
| `$black` | ![#000](https://ej2.syncfusion.com/download/documentation/svg/000.svg) `#000` |
| `$white` | ![#fff](https://ej2.syncfusion.com/download/documentation/svg/fff.svg) `#fff` |
| `$gray-100` | ![#f8f9fa](https://ej2.syncfusion.com/download/documentation/svg/f8f9fa.svg) `#f8f9fa` |
| `$gray-200` | ![#e9ecef](https://ej2.syncfusion.com/download/documentation/svg/e9ecef.svg) `#e9ecef` |
| `$gray-300` | ![#dee2e6](https://ej2.syncfusion.com/download/documentation/svg/dee2e6.svg) `#dee2e6` |
| `$gray-400` | ![#ced4da](https://ej2.syncfusion.com/download/documentation/svg/ced4da.svg) `#ced4da` |
| `$gray-500` | ![#adb5bd](https://ej2.syncfusion.com/download/documentation/svg/adb5bd.svg) `#adb5bd` |
| `$gray-600` | ![#6c757d](https://ej2.syncfusion.com/download/documentation/svg/6c757d.svg) `#6c757d` |
| `$gray-700` | ![#495057](https://ej2.syncfusion.com/download/documentation/svg/495057.svg) `#495057` |
| `$gray-800` | ![#343a40](https://ej2.syncfusion.com/download/documentation/svg/343a40.svg) `#343a40` |
| `$gray-900` | ![#212529](https://ej2.syncfusion.com/download/documentation/svg/212529.svg) `#212529` |
| `$blue` | ![#0d6efd](https://ej2.syncfusion.com/download/documentation/svg/007bff.svg) `#0d6efd` |
| `$indigo` | ![#6610f2](https://ej2.syncfusion.com/download/documentation/svg/6610f2.svg) `#6610f2` |
| `$purple` | ![#6f42c1](https://ej2.syncfusion.com/download/documentation/svg/6f42c1.svg) `#6f42c1` |
| `$pink` | ![#d63384](https://ej2.syncfusion.com/download/documentation/svg/e83e8c.svg) `#d63384` |
| `red` | ![#dc3545](https://ej2.syncfusion.com/download/documentation/svg/dc3545.svg) `#dc3545` |
| `$orange` | ![#fd7e14](https://ej2.syncfusion.com/download/documentation/svg/fd7e14.svg) `#fd7e14` |
| `$yellow` | ![#ffc107](https://ej2.syncfusion.com/download/documentation/svg/ffc107.svg) `#ffc107` |
| `$green` | ![#198754](https://ej2.syncfusion.com/download/documentation/svg/28a745.svg) `#198754` |
| `$teal` | ![#20c997](https://ej2.syncfusion.com/download/documentation/svg/20c997.svg) `#20c997` |
| `$cyan` | ![#0dcaf0](https://ej2.syncfusion.com/download/documentation/svg/17a2b8.svg) `#0dcaf0` |

### High Contrast

| Name | Value |
| ------------- | ------------- |
| `$selection-bg` | ![#ffd939](https://ej2.syncfusion.com/download/documentation/svg/ffd939.svg) `#ffd939` |
| `$selection-font` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$selection-border` | ![#ffd939](https://ej2.syncfusion.com/download/documentation/svg/ffd939.svg) `#ffd939` |
| `$hover-bg` | ![#685708](https://ej2.syncfusion.com/download/documentation/svg/685708.svg) `#685708` |
| `$hover-font` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$hover-border` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$border-default` | ![#969696](https://ej2.syncfusion.com/download/documentation/svg/969696.svg) `#969696` |
| `$border-alt` | ![#757575](https://ej2.syncfusion.com/download/documentation/svg/757575.svg) `#757575` |
| `$border-fg` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$border-fg-alt` | ![#ffd939](https://ej2.syncfusion.com/download/documentation/svg/ffd939.svg) `#ffd939` |
| `$bg-base-0` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$bg-base-5` | ![#0d0d0d](https://ej2.syncfusion.com/download/documentation/svg/0d0d0d.svg) `#0d0d0d` |
| `$bg-base-10` | ![#1a1a1a](https://ej2.syncfusion.com/download/documentation/svg/1a1a1a.svg) `#1a1a1a` |
| `$bg-base-15` | ![#262626](https://ej2.syncfusion.com/download/documentation/svg/262626.svg) `#262626` |
| `$bg-base-20` | ![#333333](https://ej2.syncfusion.com/download/documentation/svg/333333.svg) `#333333` |
| `$bg-base-75` | ![#bfbfbf](https://ej2.syncfusion.com/download/documentation/svg/bfbfbf.svg) `#bfbfbf` |
| `$bg-base-100` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$header-font` | ![#ffd939](https://ej2.syncfusion.com/download/documentation/svg/ffd939.svg) `#ffd939` |
| `$header-font-alt` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$content-font` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$content-font-alt` | ![#969696](https://ej2.syncfusion.com/download/documentation/svg/969696.svg) `#969696` |
| `$link` | ![#8a8aff](https://ej2.syncfusion.com/download/documentation/svg/8a8aff.svg) `#8a8aff` |
| `$invert-font` | ![#000000](https://ej2.syncfusion.com/download/documentation/svg/000000.svg) `#000000` |
| `$success-bg` | ![#166600](https://ej2.syncfusion.com/download/documentation/svg/166600.svg) `#166600` |
| `$error-bg` | ![#b30900](https://ej2.syncfusion.com/download/documentation/svg/b30900.svg) `#b30900` |
| `$message-font` | ![#ffffff](https://ej2.syncfusion.com/download/documentation/svg/ffffff.svg) `#ffffff` |
| `$alert-bg` | ![#944000](https://ej2.syncfusion.com/download/documentation/svg/944000.svg) `#944000` |
| `$info-bg` | ![#0056b3](https://ej2.syncfusion.com/download/documentation/svg/0056b3.svg) `#0056b3` |
| `$success-alt` | ![#2bc700](https://ej2.syncfusion.com/download/documentation/svg/2bc700.svg) `#2bc700` |
| `$error-alt` | ![#ff6161](https://ej2.syncfusion.com/download/documentation/svg/ff6161.svg) `#ff6161` |
| `$alert-alt` | ![#ff7d1a](https://ej2.syncfusion.com/download/documentation/svg/ff7d1a.svg) `#ff7d1a` |
| `$info-alt` | ![#66b0ff](https://ej2.syncfusion.com/download/documentation/svg/66b0ff.svg) `#66b0ff` |
| `$disable` | ![#757575](https://ej2.syncfusion.com/download/documentation/svg/757575.svg) `#757575` |

### Tailwind CSS

| Name | Value (Default Theme) | Value (Dark Theme) |
| ------------- | ------------- | ------------- |
| `$black` | ![#000](https://ej2.syncfusion.com/download/documentation/svg/000.svg) `#000` | ![#000](https://ej2.syncfusion.com/download/documentation/svg/000.svg) `#000` |
| `$white` | ![#fff](https://ej2.syncfusion.com/download/documentation/svg/fff.svg) `#fff` | ![#fff](https://ej2.syncfusion.com/download/documentation/svg/fff.svg) `#fff` |
| `$cool-gray-50` | ![#f9fafb](https://ej2.syncfusion.com/download/documentation/svg/f9fafb.svg) `#f9fafb` | ![#f9fafb](https://ej2.syncfusion.com/download/documentation/svg/f9fafb.svg) `#f9fafb` |
| `$cool-gray-100` | ![#f3f4f6](https://ej2.syncfusion.com/download/documentation/svg/f3f4f6.svg) `#f3f4f6` | ![#f3f4f6](https://ej2.syncfusion.com/download/documentation/svg/f3f4f6.svg) `#f3f4f6` |
| `$cool-gray-200` | ![#e5e7eb](https://ej2.syncfusion.com/download/documentation/svg/e5e7eb.svg) `#e5e7eb` | ![#e5e7eb](https://ej2.syncfusion.com/download/documentation/svg/e5e7eb.svg) `#e5e7eb` |
| `$cool-gray-300` | ![#d1d5db](https://ej2.syncfusion.com/download/documentation/svg/d1d5db.svg) `#d1d5db` | ![#d1d5db](https://ej2.syncfusion.com/download/documentation/svg/d1d5db.svg) `#d1d5db` |
| `$cool-gray-400` | ![#9ca3af](https://ej2.syncfusion.com/download/documentation/svg/9ca3af.svg) `#9ca3af` | ![#9ca3af](https://ej2.syncfusion.com/download/documentation/svg/9ca3af.svg) `#9ca3af` |
| `$cool-gray-500` | ![#6b7280](https://ej2.syncfusion.com/download/documentation/svg/6b7280.svg) `#6b7280` | ![#6b7280](https://ej2.syncfusion.com/download/documentation/svg/6b7280.svg) `#6b7280` |
| `$cool-gray-600` | ![#4b5563](https://ej2.syncfusion.com/download/documentation/svg/4b5563.svg) `#4b5563` | ![#4b5563](https://ej2.syncfusion.com/download/documentation/svg/4b5563.svg) `#4b5563` |
| `$cool-gray-700` | ![#374151](https://ej2.syncfusion.com/download/documentation/svg/374151.svg) `#374151` | ![#374151](https://ej2.syncfusion.com/download/documentation/svg/374151.svg) `#374151` |
| `$cool-gray-800` | ![#1f2937](https://ej2.syncfusion.com/download/documentation/svg/1f2937.svg) `#1f2937` | ![#1f2937](https://ej2.syncfusion.com/download/documentation/svg/1f2937.svg) `#1f2937` |
| `$cool-gray-900` | ![#111827](https://ej2.syncfusion.com/download/documentation/svg/000.svg) `#111827` | ![#111827](https://ej2.syncfusion.com/download/documentation/svg/000.svg) `#111827` |
| `$red-50` | ![#fef2f2](https://ej2.syncfusion.com/download/documentation/svg/fef2f2.svg) `#fef2f2` | ![#fef2f2](https://ej2.syncfusion.com/download/documentation/svg/fef2f2.svg) `#fef2f2` |
| `$red-100` | ![#fee2e2](https://ej2.syncfusion.com/download/documentation/svg/fee2e2.svg) `#fee2e2` | ![#fee2e2](https://ej2.syncfusion.com/download/documentation/svg/fee2e2.svg) `#fee2e2` |
| `$red-200` | ![#fecaca](https://ej2.syncfusion.com/download/documentation/svg/fecaca.svg) `#fecaca` | ![#fecaca](https://ej2.syncfusion.com/download/documentation/svg/fecaca.svg) `#fecaca` |
| `$red-300` | ![#fca5a5](https://ej2.syncfusion.com/download/documentation/svg/fca5a5.svg) `#fca5a5` | ![#fca5a5](https://ej2.syncfusion.com/download/documentation/svg/fca5a5.svg) `#fca5a5` |
| `$red-400` | ![#f87171](https://ej2.syncfusion.com/download/documentation/svg/f87171.svg) `#f87171` | ![#f87171](https://ej2.syncfusion.com/download/documentation/svg/f87171.svg) `#f87171` |
| `$red-500` | ![#ef4444](https://ej2.syncfusion.com/download/documentation/svg/ef4444.svg) `#ef4444` | ![#ef4444](https://ej2.syncfusion.com/download/documentation/svg/ef4444.svg) `#ef4444` |
| `$red-600` | ![#dc2626](https://ej2.syncfusion.com/download/documentation/svg/dc2626.svg) `#dc2626` | ![#dc2626](https://ej2.syncfusion.com/download/documentation/svg/dc2626.svg) `#dc2626` |
| `$red-700` | ![#b91c1c](https://ej2.syncfusion.com/download/documentation/svg/b91c1c.svg) `#b91c1c` | ![#b91c1c](https://ej2.syncfusion.com/download/documentation/svg/b91c1c.svg) `#b91c1c` |
| `$red-800` | ![#991b1b](https://ej2.syncfusion.com/download/documentation/svg/991b1b.svg) `#991b1b` | ![#991b1b](https://ej2.syncfusion.com/download/documentation/svg/991b1b.svg) `#991b1b` |
| `$red-900` | ![#7f1d1d](https://ej2.syncfusion.com/download/documentation/svg/7f1d1d.svg) `#7f1d1d` | ![#7f1d1d](https://ej2.syncfusion.com/download/documentation/svg/7f1d1d.svg) `#7f1d1d` |
| `$green-50` | ![#f0fdf4](https://ej2.syncfusion.com/download/documentation/svg/f0fdf4.svg) `#f0fdf4` | ![#f0fdf4](https://ej2.syncfusion.com/download/documentation/svg/f0fdf4.svg) `#f0fdf4` |
| `$green-100` | ![#dcfce7](https://ej2.syncfusion.com/download/documentation/svg/dcfce7.svg) `#dcfce7` | ![#dcfce7](https://ej2.syncfusion.com/download/documentation/svg/dcfce7.svg) `#dcfce7` |
| `$green-200` | ![#bbf7d0](https://ej2.syncfusion.com/download/documentation/svg/bbf7d0.svg) `#bbf7d0` | ![#bbf7d0](https://ej2.syncfusion.com/download/documentation/svg/bbf7d0.svg) `#bbf7d0` |
| `$green-300` | ![#86efac](https://ej2.syncfusion.com/download/documentation/svg/86efac.svg) `#86efac` | ![#86efac](https://ej2.syncfusion.com/download/documentation/svg/86efac.svg) `#86efac` |
| `$green-500` | ![#22c55e](https://ej2.syncfusion.com/download/documentation/svg/22c55e.svg) `#22c55e` | ![#22c55e](https://ej2.syncfusion.com/download/documentation/svg/22c55e.svg) `#22c55e` |
| `$green-600` | ![#16a34a](https://ej2.syncfusion.com/download/documentation/svg/16a34a.svg) `#16a34a` | ![#16a34a](https://ej2.syncfusion.com/download/documentation/svg/16a34a.svg) `#16a34a` |
| `$green-700` | ![#15803d](https://ej2.syncfusion.com/download/documentation/svg/15803d.svg) `#15803d` | ![#15803d](https://ej2.syncfusion.com/download/documentation/svg/15803d.svg) `#15803d` |
| `$green-800` | ![#166534](https://ej2.syncfusion.com/download/documentation/svg/166534.svg) `#166534` | ![#166534](https://ej2.syncfusion.com/download/documentation/svg/166534.svg) `#166534` |
| `$green-900` | ![#14532d](https://ej2.syncfusion.com/download/documentation/svg/14532d.svg) `#14532d` | ![#14532d](https://ej2.syncfusion.com/download/documentation/svg/14532d.svg) `#14532d` |
| `$orange-50` | ![#fff7ed](https://ej2.syncfusion.com/download/documentation/svg/fff7ed.svg) `#fff7ed` | ![#fff7ed](https://ej2.syncfusion.com/download/documentation/svg/fff7ed.svg) `#fff7ed` |
| `$orange-100` | ![#ffedd5](https://ej2.syncfusion.com/download/documentation/svg/ffedd5.svg) `#ffedd5` | ![#ffedd5](https://ej2.syncfusion.com/download/documentation/svg/ffedd5.svg) `#ffedd5` |
| `$orange-200` | ![#fed7aa](https://ej2.syncfusion.com/download/documentation/svg/fed7aa.svg) `#fed7aa` | ![#fed7aa](https://ej2.syncfusion.com/download/documentation/svg/fed7aa.svg) `#fed7aa` |
| `$orange-300` | ![#fdba74](https://ej2.syncfusion.com/download/documentation/svg/fdba74.svg) `#fdba74` | ![#fdba74](https://ej2.syncfusion.com/download/documentation/svg/fdba74.svg) `#fdba74` |
| `$orange-400` | ![#fb923c](https://ej2.syncfusion.com/download/documentation/svg/fb923c.svg) `#fb923c` | ![#fb923c](https://ej2.syncfusion.com/download/documentation/svg/fb923c.svg) `#fb923c` |
| `$orange-500` | ![#f97316](https://ej2.syncfusion.com/download/documentation/svg/f97316.svg) `#f97316` | ![#f97316](https://ej2.syncfusion.com/download/documentation/svg/f97316.svg) `#f97316` |
| `$orange-600` | ![#ea580c](https://ej2.syncfusion.com/download/documentation/svg/ea580c.svg) `#ea580c` | ![#ea580c](https://ej2.syncfusion.com/download/documentation/svg/ea580c.svg) `#ea580c` |
| `$orange-700` | ![#c2410c](https://ej2.syncfusion.com/download/documentation/svg/c2410c.svg) `#c2410c` | ![#c2410c](https://ej2.syncfusion.com/download/documentation/svg/c2410c.svg) `#c2410c` |
| `$orange-800` | ![#9a3412](https://ej2.syncfusion.com/download/documentation/svg/9a3412.svg) `#9a3412` | ![#9a3412](https://ej2.syncfusion.com/download/documentation/svg/9a3412.svg) `#9a3412` |
| `$orange-900` | ![#7c2d12](https://ej2.syncfusion.com/download/documentation/svg/7c2d12.svg) `#7c2d12` | ![#7c2d12](https://ej2.syncfusion.com/download/documentation/svg/7c2d12.svg) `#7c2d12` |
| `$cyan-50` | ![#ecfeff](https://ej2.syncfusion.com/download/documentation/svg/ecfeff.svg) `#ecfeff` | ![#ecfeff](https://ej2.syncfusion.com/download/documentation/svg/ecfeff.svg) `#ecfeff` |
| `$cyan-100` | ![#cffafe](https://ej2.syncfusion.com/download/documentation/svg/cffafe.svg) `#cffafe` | ![#cffafe](https://ej2.syncfusion.com/download/documentation/svg/cffafe.svg) `#cffafe` |
| `$cyan-200` | ![#a5f3fc](https://ej2.syncfusion.com/download/documentation/svg/a5f3fc.svg) `#a5f3fc` | ![#a5f3fc](https://ej2.syncfusion.com/download/documentation/svg/a5f3fc.svg) `#a5f3fc` |
| `$cyan-300` | ![#67e8f9](https://ej2.syncfusion.com/download/documentation/svg/67e8f9.svg) `#67e8f9` | ![#67e8f9](https://ej2.syncfusion.com/download/documentation/svg/67e8f9.svg) `#67e8f9` |
| `$cyan-400` | ![#22d3ee](https://ej2.syncfusion.com/download/documentation/svg/22d3ee.svg) `#22d3ee` | ![#22d3ee](https://ej2.syncfusion.com/download/documentation/svg/22d3ee.svg) `#22d3ee` |
| `$cyan-500` | ![#06b6d4](https://ej2.syncfusion.com/download/documentation/svg/06b6d4.svg) `#06b6d4` | ![#06b6d4](https://ej2.syncfusion.com/download/documentation/svg/06b6d4.svg) `#06b6d4` |
| `$cyan-600` | ![#0891b2](https://ej2.syncfusion.com/download/documentation/svg/0891b2.svg) `#0891b2` | ![#0891b2](https://ej2.syncfusion.com/download/documentation/svg/0891b2.svg) `#0891b2` |
| `$cyan-700` | ![#0e7490](https://ej2.syncfusion.com/download/documentation/svg/0e7490.svg) `#0e7490` | ![#0e7490](https://ej2.syncfusion.com/download/documentation/svg/0e7490.svg) `#0e7490` |
| `$cyan-800` | ![#155e75](https://ej2.syncfusion.com/download/documentation/svg/155e75.svg) `#155e75` | ![#155e75](https://ej2.syncfusion.com/download/documentation/svg/155e75.svg) `#155e75` |
| `$cyan-900` | ![#164e63](https://ej2.syncfusion.com/download/documentation/svg/164e63.svg) `#164e63` | ![#164e63](https://ej2.syncfusion.com/download/documentation/svg/164e63.svg) `#164e63` |
| `$indigo-50` | ![#eef2ff](https://ej2.syncfusion.com/download/documentation/svg/eef2ff.svg) `#eef2ff` | ![#eef2ff](https://ej2.syncfusion.com/download/documentation/svg/eef2ff.svg) `#eef2ff` |
| `$indigo-100` | ![#e0e7ff](https://ej2.syncfusion.com/download/documentation/svg/000.svg) `#e0e7ff` | ![#e0e7ff](https://ej2.syncfusion.com/download/documentation/svg/000.svg) `#e0e7ff` |
| `$indigo-200` | ![#c7d2fe](https://ej2.syncfusion.com/download/documentation/svg/c7d2fe.svg) `#c7d2fe` | ![#c7d2fe](https://ej2.syncfusion.com/download/documentation/svg/c7d2fe.svg) `#c7d2fe` |
| `$indigo-300` | ![#a5b4fc](https://ej2.syncfusion.com/download/documentation/svg/a5b4fc.svg) `#a5b4fc` | ![#a5b4fc](https://ej2.syncfusion.com/download/documentation/svg/a5b4fc.svg) `#a5b4fc` |
| `$indigo-400` | ![#818cf8](https://ej2.syncfusion.com/download/documentation/svg/818cf8.svg) `#818cf8` | ![#818cf8](https://ej2.syncfusion.com/download/documentation/svg/818cf8.svg) `#818cf8` |
| `$indigo-500` | ![#6366f1](https://ej2.syncfusion.com/download/documentation/svg/6366f1.svg) `#6366f1` | ![#6366f1](https://ej2.syncfusion.com/download/documentation/svg/6366f1.svg) `#6366f1` |
| `$indigo-600` | ![#4f46e5](https://ej2.syncfusion.com/download/documentation/svg/4f46e5.svg) `#4f46e5` | ![#4f46e5](https://ej2.syncfusion.com/download/documentation/svg/4f46e5.svg) `#4f46e5` |
| `$indigo-700` | ![#4338ca](https://ej2.syncfusion.com/download/documentation/svg/4338ca.svg) `#4338ca` | ![#4338ca](https://ej2.syncfusion.com/download/documentation/svg/4338ca.svg) `#4338ca` |
| `$indigo-800` | ![#3730a3](https://ej2.syncfusion.com/download/documentation/svg/3730a3.svg) `#3730a3` | ![#3730a3](https://ej2.syncfusion.com/download/documentation/svg/3730a3.svg) `#3730a3` |
| `$indigo-900` | ![#312e81](https://ej2.syncfusion.com/download/documentation/svg/312e81.svg) `#312e81` | ![#312e81](https://ej2.syncfusion.com/download/documentation/svg/312e81.svg) `#312e81` |
