<template>
  <form class="custom-options mt-5">
    <div v-for="option in product.bundle_options" :key="('bundleOption_' + option.option_id)">
      <product-bundle-option :option="option" @optionChanged="optionChanged" :error-messages="errorMessages"/>
    </div>
  </form>
</template>

<script>
import { ProductBundleOptions } from '@vue-storefront/core/modules/catalog/components/ProductBundleOptions.ts'
import ProductBundleOption from './ProductBundleOption'

export default {
  mixins: [ProductBundleOptions],
  components: {
    ProductBundleOption
  }
}
</script>
