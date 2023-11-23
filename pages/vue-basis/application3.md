# Application

Exemple de template (nécessite Tailwind) :

<div class="max-h-[80%] overflow-auto">
```html
<template>
    <div class="w-56 py-6 px-2">
        <img class="w-full rounded-md object-cover object-center" />
        <div class="py-2">
            <div class="flex justify-between">
                <div>
                    <h3>
                        <a class="font-medium text-gray-700 hover:text-gray-800">T-shirt homme</a>
                    </h3>
                    <div class=" text-sm text-gray-500">Rouge</div>
                </div>
                <div class="text-sm font-medium text-gray-900">30 €</div>
            </div>
            <div class="flex justify-between">
                <div>
                    <label for="quantity" class="sr-only">Quatité</label>
                    <select id="quantity" name="quantity"
                        class="bg-transparent max-w-full rounded-md border border-transparent p-1.5 text-left text-base font-medium leading-5 text-gray-700 shadow-sm focus:border-indigo-500 focus:outline-none focus:ring-1 focus:ring-indigo-500 sm:text-sm">
                        <option value="0">0</option>
                        <option value="1">1</option>
                        <option value="2">2</option>
                        <option value="3">3</option>
                        <option value="4">4</option>
                        <option value="5">5</option>
                        <option value="6">6</option>
                        <option value="7">7</option>
                        <option value="8">8</option>
                    </select>
                </div>
                <p class="text-gray-500">150 €</p>
            </div>
        </div>
    </div>
</template>
```
</div>