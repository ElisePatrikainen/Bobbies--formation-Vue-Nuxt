<template>
    <div class="w-56 py-6 px-2">
        <img :src="product.imageSrc" :alt="product.imageAlt" class="w-full rounded-md object-cover object-center" />
        <div class="py-2">
            <div class="flex justify-between">
                <div>
                    <h3>
                        <a :href="product.href" class="font-medium text-gray-700 hover:text-gray-800">{{ product.name }}</a>
                    </h3>
                    <div class=" text-sm text-gray-500">{{ product.color }}</div>
                        <!-- <p v-if="product.size" class="ml-4 border-l border-gray-200 pl-4 text-gray-500">{{ product.size }}
                        </p> -->
                </div>
                <div class="text-sm font-medium text-gray-900">{{ product.price }} €</div>

                <!-- <div class="mt-4 sm:mt-0 sm:pr-9">
                    <div class="absolute right-0 top-0">
                        <button type="button" class="-m-2 inline-flex p-2 text-gray-400 hover:text-gray-500">
                            <span class="sr-only">Remove</span>
                            <XMarkIconMini class="h-5 w-5" aria-hidden="true" />
                        </button>
                    </div>
                </div> -->
            </div>
            <div class="flex justify-between">
                <div>
                    <label for="quantity" class="sr-only">Quantity, {{ product.name }}</label>
                    <select id="quantity" name="quantity" :value="quantity"
                        @input="setQuantity(($event.target as HTMLInputElement).value)"
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
                <p class="text-gray-500">{{ totalPrice }} €</p>
            </div>

            <!-- <p class="mt-4 flex space-x-2 text-sm text-gray-700">
                <CheckIcon v-if="product.inStock" class="h-5 w-5 flex-shrink-0 text-green-500" aria-hidden="true" />
                <ClockIcon v-else class="h-5 w-5 flex-shrink-0 text-gray-300" aria-hidden="true" />
                <span>{{ product.inStock ? 'In stock' : `Ships in ${product.leadTime}` }}</span>
            </p> -->
        </div>
    </div>
</template>

<script setup lang="ts">
import { computed, onMounted, ref } from 'vue'

const quantity = ref(0)

const product = ref({
    id: 1,
    name: 'Basic Tee',
    href: '#',
    price: '32.00',
    color: 'Sienna',
    inStock: true,
    size: 'Large',
    imageSrc: 'https://tailwindui.com/img/ecommerce-images/shopping-cart-page-01-product-01.jpg',
    imageAlt: "Front of men's Basic Tee in sienna.",
})

const totalPrice = computed(() => {
    return parseInt(product.value.price) * quantity.value
})


// TODO : le mettre a la racine de l'app
// onMounted(() => setTimeout(() => window.alert("Hey, 10% avec le code VUE "), 10000))

function setQuantity(value: string) {
    quantity.value = parseInt(value)
}
</script>