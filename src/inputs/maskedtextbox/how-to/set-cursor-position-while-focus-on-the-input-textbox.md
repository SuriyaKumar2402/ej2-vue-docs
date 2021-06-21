# Set cursor position while focus on the input textbox

By default, on focusing the MaskedTextBox the entire mask gets selected. You can customize by using any one of the following methods:

* Setting cursor position at the start of the MaskedTextBox.
* Setting cursor position at the end of the MaskedTextBox.
* Setting cursor at the specified position in the MaskedTextBox.

> The **selectionStart** and **selectionEnd** set to **0** instead of the input element value's length, when we focus on a MaskedTextBox control filled with all mask characters. This is the default behavior of the HTML 5 input element.

Following is an example that demonstrates the above cases to set cursor position in the MaskedTextBox using focus event.

{% tab template="masked-textbox/how-to/cursor", isDefaultActive = "true" %}

```html
<template>
  <div id="app">
        <div class='wrap'>
           <ejs-maskedtextbox mask='00000-00000' value='93828-32132' placeholder='Default cursor position' floatLabelType='Always'></ejs-maskedtextbox>
        </div>
        <div class='wrap'>
            <ejs-maskedtextbox mask='00000-00000' value='83929-4342' placeholder='Cursor positioned at start' floatLabelType='Always' :focus='focus'></ejs-maskedtextbox>
        </div>
        <div class='wrap'>
            <ejs-maskedtextbox mask='00000-00000' value='83929-3213' placeholder='Cursor positioned at end' floatLabelType='Always' :focus='endfocus'></ejs-maskedtextbox>
        </div>
        <div class='wrap'>
            <ejs-maskedtextbox mask='+1 000-000-0000' value='234-432-432' placeholder='Cursor at specified position' floatLabelType='Always' :focus='specifiedfocus'></ejs-maskedtextbox>
        </div>
  </div>
</template>
<script>
import Vue from "vue";
import { MaskedTextBoxPlugin } from "@syncfusion/ej2-vue-inputs";

Vue.use(MaskedTextBoxPlugin);
export default {
  data () {
    return {}
  },
  methods: {
      focus: function(args) {
           args.selectionEnd= args.selectionStart = 0;
      } ,
      endfocus: function(args){
          args.selectionStart=args.selectionEnd = args.maskedValue.length;
      },
      specifiedfocus: function(args){
          args.selectionStart = 3;
          args.selectionEnd = 3;
      }
    }
}
</script>
<style>
  @import "../../node_modules/@syncfusion/ej2-base/styles/material.css";
  @import "../../node_modules/@syncfusion/ej2-vue-inputs/styles/material.css";
 .wrap {
  margin: 20px auto;
  width: 240px;
}

.e-widget {
  padding-bottom: 12px;
}
</style>
```

{% endtab %}