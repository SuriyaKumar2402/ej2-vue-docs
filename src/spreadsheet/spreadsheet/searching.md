---
title: "Find and Replace"
component: "Spreadsheet"
description: "This section helps you to learn about how to find, replace and goto(navigate to cell) in Spreadsheet."
---

# Find and Replace

Find and Replace helps you to search for the target text and replace the found text with alternative text within the sheet or workbook. You can use the [`allowFindAndReplace`](../api/spreadsheet/#allowFindAndReplace) property to enable or disable the Find and Replace functionality.

> * The default value for `allowFindAndReplace` property is `true`.

## Find

Find feature is used to select the matched contents of a cell within the sheet or workbook. It is extremely useful when working with large set of data source.

### User Interface

Find can be done by any of the following ways:

* Select the Search icon in the Ribbon toolbar or use `Ctrl + F` key to open the Find dialog.
* Use find Next and find Previous buttons to search the given value in the workbook.
* Select the option button in Find dialog to open the Find and Replace dialog. Then, select the below properties for enhanced searching.

> * `Search within`: To search the target in a sheet (default) or in an entire workbook.
> * `Search by`: It enhance the search, either By Rows (default), or By Columns.
> * `Match case`: To find the matched value with case sensitive.
> * `Match exact cell contents`: To find the exact matched cell value with entire match cases.

* Using [`find()`](../api/spreadsheet/#find) method to perform find operation.

## Replace

Replace feature is used to change the find contents of a cell within sheet or workbook. Replace All is used to change all the matched contents of a cell within sheet or workbook.

### User Interface

Replace can be done by any of the following ways:

* Use `Ctrl + H` key to open the Find and Replace dialog.
* Use Replace button to change the found value in sheet or workbook.
* Using Replace All button, all the matched criteria can be replaced with find value based on sheet or workbook.
* Using [`replace()`](../api/spreadsheet/#replace) method to perform replace operation by passing the argument `args.replaceby` as `replace`.
* Using [`replace()`](../api/spreadsheet/#replace) method to perform replace all operation by passing the argument `args.replaceby` as `replaceall`.

## Go to

Go to feature is used to navigate to a specific cell address in the sheet or workbook.

### User Interface

* Use `Ctrl + G` key to open the Go To dialog.
* Use [`goTo()`](../api/spreadsheet/#goto) method to perform Go To operation.

{% tab template="spreadsheet/searching", iframeHeight="450px" , isDefaultActive=true %}

```html
<template>
  <ejs-spreadsheet ref="spreadsheet" :created="created" :showFormulaBar="false">
                <e-sheets>
                  <e-sheet name="Price Details">
                    <e-ranges>
                      <e-range :dataSource="dataSource1"></e-range>
                    </e-ranges>
                    <e-columns>
                      <e-column :width=100></e-column>
                      <e-column :width=100></e-column>
                      <e-column :width=100></e-column>
                      <e-column :width=100></e-column>
                    </e-columns>
                  </e-sheet>
                  <e-sheet name="Budget Details">
                    <e-ranges>
                      <e-range :dataSource="dataSource2"></e-range>
                    </e-ranges>
                    <e-columns>
                      <e-column :width=100></e-column>
                      <e-column :width=100></e-column>
                      <e-column :width=100></e-column>
                      <e-column :width=100></e-column>
                      </e-columns>
                  </e-sheet>
                </e-sheets>
              </ejs-spreadsheet>
</template>

<script>
import Vue from "vue";
import { SpreadsheetPlugin } from "@syncfusion/ej2-vue-spreadsheet";
import { priceData, budgetData  } from './data.js';
Vue.use(SpreadsheetPlugin);
export default {
   data: () => {
    return {
      dataSource1: priceData,
      dataSource2: budgetData,
    }
  },
  methods: {
   created: function () {
       var spreadsheet = this.$refs.spreadsheet;
    spreadsheet.cellFormat({ fontWeight: 'bold', textAlign: 'center' }, 'A1:H1');
        spreadsheet.cellFormat({ fontWeight: 'bold', textAlign: 'center' }, 'Budget Details!A1:D1');
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

## Limitations

* Undo/redo for Replace All is not supported in this feature.