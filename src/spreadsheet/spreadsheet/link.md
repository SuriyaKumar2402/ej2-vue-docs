---
title: "Hyperlink"
component: "Spreadsheet"
description: "This section helps to learn how to insert, edit and remove a hyperlink in Spreadsheet control."
---

# Hyperlink

Hyperlink is used to navigate to web links or cell reference within the sheet or to other sheets in Spreadsheet. You can use the [`allowHyperlink`](../api/spreadsheet/#allowHyperlink) property to enable or disable hyperlink functionality.

> * The default value for `allowHyperlink` property is `true`.

## Insert Link

You can insert a hyperlink in a worksheet cell for quick access to related information.

### User Interface

In the active spreadsheet, click the cell where you want to create a hyperlink. Insert hyperlink can be done by any of the following ways:

* Select the INSERT tab in the Ribbon toolbar and choose the `Link` item.
* Right-click the cell and then click Hyperlink item in the context menu.
* Use `Ctrl + K` keyboard shortcut to apply the hyperlink.
* Use the [`addHyperlink`](../api/spreadsheet/#hyperlink) method programmatically.

## Edit Hyperlink

You can change an existing hyperlink in your workbook by changing its destination or the text that is used to represent it.

### User Interface

In the active spreadsheet, Select the cell that contains the hyperlink that you want to change. Editing the hyperlink while opening the dialog can be done by any one of the following ways:

* Select the INSERT tab in the Ribbon toolbar and choose the `Link` item.
* Right-click the cell and then click Edit Hyperlink item in the context menu, or you can press Ctrl+K.

In the Edit Link dialog box, make the changes that you want, and click UPDATE.

## Remove Hyperlink

Performing this operation remove a single hyperlink without losing the display text.

### User Interface

In the active spreadsheet, click the cell where you want to remove a hyperlink. remove hyperlink can be done by any of the following ways:
* Right-click the cell and then click Remove Hyperlink item in the context menu.
* Use the [`removeHyperlink()`](../api/spreadsheet/#hyperlink) method programmatically.

## How to change target attribute

There is an event named `beforeHyperlinkClick` which triggers only on clicking hyperlink. You can customize where to open the hyperlink by using the `target` property in the arguments of that event.

{% tab template="spreadsheet/link", iframeHeight="450px" , isDefaultActive=true %}

```html
<template>
   <ejs-spreadsheet ref="spreadsheet" :beforeHyperlinkClick="beforeHyperlinkClick">
   <e-sheets>
          <e-sheet name="PriceDetails">
             <e-rows>
                    <e-row>
                            <e-cells>
                                <e-cell value="Item Name"></e-cell>
                                <e-cell value="Stock Detail"></e-cell>
                                <e-cell value="Website"></e-cell>
                            </e-cells>
                        </e-row>
                        <e-row>
                            <e-cells>
                                <e-cell value="Casual Shoes"></e-cell>
                                <e-cell value="OUT OF STOCK"></e-cell>
                                <e-cell value="Amazon" hyperlink="https://www.amazon.com/"></e-cell>
                            </e-cells>
                        </e-row>
                        <e-row>
                            <e-cells>
                                <e-cell value="Sports Shoes"></e-cell>
                                <e-cell value="IN STOCK" hyperlink="Stock!A2:B2"></e-cell>
                                <e-cell value="Overstack" hyperlink="https://www.overstock.com/"></e-cell>
                            </e-cells>
                        </e-row>
                        <e-row>
                            <e-cells>
                                <e-cell value="Formal Shoes"></e-cell>
                                <e-cell value="IN STOCK" hyperlink="Stock!A3:B3"></e-cell>
                                <e-cell value="AliExpress" hyperlink="https://www.aliexpress.com/"></e-cell>
                            </e-cells>
                        </e-row>
                        <e-row>
                            <e-cells>
                                <e-cell value="Sandals & Floaters"></e-cell>
                                <e-cell value="OUT OF STOCK"></e-cell>
                                <e-cell value="AliBaba" hyperlink="https://www.aliBaba.com/"></e-cell>
                            </e-cells>
                        </e-row>
                        <e-row>
                            <e-cells>
                                <e-cell value="Flip-Flops & Slippers"></e-cell>
                                <e-cell value="IN STOCK" hyperlink="Stock!A4:B4"></e-cell>
                                <e-cell value="Taobao" hyperlink="https://www.taobao.com/"></e-cell>
                            </e-cells>
                        </e-row>
                    </e-rows>
            <e-columns>
              <e-column :width="width1"></e-column>
              <e-column :width="width1"></e-column>
              <e-column :width="width2"></e-column>
            </e-columns>
          </e-sheet>
          <e-sheet name="Stock">
             <e-rows>
                    <e-row>
                            <e-cells>
                                <e-cell value="Item Name"></e-cell>
                                <e-cell value="Available Count"></e-cell>
                            </e-cells>
                        </e-row>
                        <e-row>
                            <e-cells>
                                <e-cell value="Sports Shoes"></e-cell>
                                <e-cell value="30"></e-cell>
                            </e-cells>
                        </e-row>
                        <e-row>
                            <e-cells>
                                <e-cell value="Formal Shoes"></e-cell>
                                <e-cell value="25"></e-cell>
                            </e-cells>
                        </e-row>
                        <e-row>
                            <e-cells>
                                <e-cell value="Flip-Flops & Slippers"></e-cell>
                                <e-cell value="40"></e-cell>
                            </e-cells>
                        </e-row>
                        <e-row>
                            <e-cells>
                                <e-cell value="Running Shoes"></e-cell>
                                <e-cell value="25"></e-cell>
                            </e-cells>
                        </e-row>
                    </e-rows>
            <e-columns>
              <e-column :width="width1"></e-column>
              <e-column :width="width2"></e-column>
            </e-columns>
          </e-sheet>
        </e-sheets></ejs-spreadsheet>
</template>

<script>
import Vue from "vue";
import { SpreadsheetPlugin } from "@syncfusion/ej2-vue-spreadsheet";
Vue.use(SpreadsheetPlugin);
export default {
   data: () => {
    return {
      width1: 160,
      width2: 120,
    }
  },
  methods: {
  beforeHyperlinkClick: function (args) {
      args.target = '_self'; //change target attribute
      }
    }
}
</script>
<style>
 @import "../node_modules/@syncfusion/ej2-vue-spreadsheet/styles/material.css";
 @import '../node_modules/@syncfusion/ej2-base/styles/material.css';  
 @import '../node_modules/@syncfusion/ej2-buttons/styles/material.css';  
 @import '../node_modules/@syncfusion/ej2-dropdowns/styles/material.css';  
 @import '../node_modules/@syncfusion/ej2-inputs/styles/material.css';  
 @import '../node_modules/@syncfusion/ej2-navigations/styles/material.css';
 @import '../node_modules/@syncfusion/ej2-popups/styles/material.css';
 @import '../node_modules/@syncfusion/ej2-splitbuttons/styles/material.css';
 @import '../node_modules/@syncfusion/ej2-grids/styles/material.css';
 @import "../node_modules/@syncfusion/ej2-spreadsheet/styles/material.css";
</style>
```

{% endtab %}

## Limitation

* Inserting multiple hyperlinks after selecting multiple ranges is not supported in Hyperlink.

## See Also

* [Sorting](./sort)
* [Filtering](./filter)
* [Undo Redo](./undo-redo)