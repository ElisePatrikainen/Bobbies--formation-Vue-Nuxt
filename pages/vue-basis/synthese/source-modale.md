# Application

Template de la modale :

```html
<div v-if="open" class="fixed top-[50%] left-[50%] translate-x-[-50%] translate-y-[-50%] bg-white border-solid border border-gray-300 rounded-md py-3">
        <div class="flex justify-end px-3">
            <button @click="open = false" class="left-0">X</button>
        </div>
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
            <div class="max-w-2xl text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">
                <h2 class="inline sm:block">Intéressé ?</h2>
                <p class="inline sm:block">Abonnez-vous à notre newsletter.</p>
            </div>
            <form class="mt-10 max-w-md">
                <div class="flex gap-x-4">
                    <label for="email-address" class="sr-only">Email address</label>
                    <EmailInput />
                    <button type="submit"
                        @click="submit"
                        class="flex-none rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Subscribe</button>
                </div>
                <p class="mt-4 text-sm leading-6 text-gray-900">We care about your data. Read our <a href="#"
                        class="font-semibold text-indigo-600 hover:text-indigo-500">privacy&nbsp;policy</a>.</p>
            </form>
        </div>
    </div>
```