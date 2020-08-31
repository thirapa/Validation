# Validation Package

This package has been created for validate information that users enter in text field. If user entered information in text field not match with the regular expression that defined, will alert validate text under text field.
***

### Usage

This package can use with [Vuetify](https://vuetifyjs.com/en/getting-started/quick-start/) only. You must have vue project with vuetify installed.

**First** --> install package

``` bash
# validation_useable is name of package to created.

npm i validation_useable
```

**Second** --> config your file.vue

``` bash
# import your package

<script>
import Validation from "validation_useable/validation.js";

export default {

data: () => ({
  ...Validation
});
</script>
```

**Third** --> use function in **rules** property

``` bash

<v-text-field
  v-model="editedItem.number"
  label="Number"
  outlined
  dense
  required
  :rules="[required('Number'), numberOnly()]"
></v-text-field>
```

** ***required*** and ***numberOnly*** is function to called from your package. You will see function *required* has 'Number',

this is the incoming parameter we defined in the function. But function *numberOnly* has no incoming parameters

because we don't define them in the function.