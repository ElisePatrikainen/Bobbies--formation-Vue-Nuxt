# Order template

Order component :

<div class="max-h-[80%] overflow-auto">

```html
<template>
  <section
    aria-labelledby="summary-heading"
    class="w-full mt-16 rounded-lg bg-gray-50 px-4 py-6 sm:p-6 lg:mt-0 lg:p-8"
  >
    <h2 id="summary-heading" class="text-lg font-medium text-gray-900">
      Order summary
    </h2>

    <dl class="mt-6 space-y-4">
      <ProductOrder />
      <div
        class="flex items-center justify-between border-t border-gray-200 pt-4"
      >
        <dt class="text-base font-medium text-gray-900">Order total</dt>
        <!-- Nb :  for the number and currency formatting, we could use the number localization from Vue I18n : https://kazupon.github.io/vue-i18n/guide/number.html-->
        <dd class="text-base font-medium text-gray-900">90 €</dd>
      </div>
    </dl>

    <div class="mt-6">
      <button
        type="submit"
        class="w-full rounded-md border border-transparent bg-indigo-600 px-4 py-3 text-base font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 focus:ring-offset-gray-50"
      >
        Checkout
      </button>
    </div>
  </section>
</template>
```

</div>