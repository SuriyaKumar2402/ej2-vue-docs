---
title: "Custom Tooltip for columns"
component: "Grid"
description: "Learn how to Custom Tooltip for columns."
---

# Custom Tooltip for columns

To display a custom ToolTip ([`EJ2 Tooltip`](../../../tooltip/getting-started)), you can render the Grid control inside the Tooltip component and set the target as `.e-rowcell`. The tooltip is displayed when hovering the grid cells.

Change the tooltip content for the grid cells by using the following code in the [`beforeRender`](../../../api/tooltip/#beforerender) event.

```typescript
beforeRender(args) {
  if (args.target.closest("td")) {
  // event triggered before render the tooltip on target element.
    this.$refs.tooltip.content = args.target.innerText;
  }
}
```

{% tab template="grid/how-to/default" %}

```html
<template>
    <div id="app">
    <ejs-tooltip ref="tooltip" target=".e-rowcell" :beforeRender="beforeRender">
      <ejs-grid ref="grid" :dataSource="data" height="315px">
        <e-columns>
          <e-column field="OrderID" headerText="Order ID" textAlign="Right" width="90"></e-column>
          <e-column field="CustomerID" headerText="Customer ID" width="120"></e-column>
          <e-column field="Freight" headerText="Freight" textAlign="Right" format="C2" width="90"></e-column>
          <e-column field="ShipName" headerText="Ship Name" width="120"></e-column>
        </e-columns>
      </ejs-grid>
    </ejs-tooltip>
    </div>
</template>
<script>
import Vue from "vue";
import { GridPlugin } from "@syncfusion/ej2-vue-grids";
import { data } from './datasource.js';
import { TooltipPlugin } from "@syncfusion/ej2-vue-popups";

Vue.use(TooltipPlugin);
Vue.use(GridPlugin);

  export default {
    data() {
      return {
        data: data
      };
    },
    methods: {
      beforeRender: function (args) {
        if (args.target.closest("td")) {
           this.$refs.tooltip.content = args.target.innerText;
        }
      }
    }
  }
</script>
<style>
@import "../node_modules/@syncfusion/ej2-vue-grids/styles/material.css";
</style>
```

{% endtab %}
