<!--
  This example requires some changes to your config:

  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/forms'),
      require('@tailwindcss/aspect-ratio'),
    ],
  }
  ```
-->
<template>
  <pre>{{tg.initDataUnsafe?.user.first_name}} {{tg.initDataUnsafe?.user.last_name}}</pre>
<!--  <div class="bg-white">-->
<!--    &lt;!&ndash; Mobile menu &ndash;&gt;-->
<!--    <TransitionRoot as="template" :show="mobileMenuOpen">-->
<!--      <Dialog class="relative z-40 lg:hidden" @close="mobileMenuOpen = false">-->
<!--        <TransitionChild as="template" enter="transition-opacity ease-linear duration-300" enter-from="opacity-0" enter-to="opacity-100" leave="transition-opacity ease-linear duration-300" leave-from="opacity-100" leave-to="opacity-0">-->
<!--          <div class="fixed inset-0 bg-black bg-opacity-25" />-->
<!--        </TransitionChild>-->

<!--        <div class="fixed inset-0 z-40 flex">-->
<!--          <TransitionChild as="template" enter="transition ease-in-out duration-300 transform" enter-from="-translate-x-full" enter-to="translate-x-0" leave="transition ease-in-out duration-300 transform" leave-from="translate-x-0" leave-to="-translate-x-full">-->
<!--            <DialogPanel class="relative flex w-full max-w-xs flex-col overflow-y-auto bg-white pb-12 shadow-xl">-->
<!--              <div class="flex px-4 pb-2 pt-5">-->
<!--                <button type="button" class="-m-2 inline-flex items-center justify-center rounded-md p-2 text-gray-400" @click="mobileMenuOpen = false">-->
<!--                  <span class="sr-only">Close menu</span>-->
<!--&lt;!&ndash;                  <XMarkIcon class="h-6 w-6" aria-hidden="true" />&ndash;&gt;-->
<!--                </button>-->
<!--              </div>-->

<!--              &lt;!&ndash; Links &ndash;&gt;-->
<!--              <TabGroup as="div" class="mt-2">-->
<!--                <div class="border-b border-gray-200">-->
<!--                  <TabList class="-mb-px flex space-x-8 px-4">-->
<!--                    <Tab as="template" v-for="category in navigation.categories" :key="category.name" v-slot="{ selected }">-->
<!--                      <button :class="[selected ? 'border-indigo-600 text-indigo-600' : 'border-transparent text-gray-900', 'flex-1 whitespace-nowrap border-b-2 px-1 py-4 text-base font-medium']">{{ category.name }}</button>-->
<!--                    </Tab>-->
<!--                  </TabList>-->
<!--                </div>-->
<!--                <TabPanels as="template">-->
<!--                  <TabPanel v-for="category in navigation.categories" :key="category.name" class="space-y-12 px-4 py-6">-->
<!--                    <div class="grid grid-cols-2 gap-x-4 gap-y-10">-->
<!--                      <div v-for="item in category.featured" :key="item.name" class="group relative">-->
<!--                        <div class="aspect-h-1 aspect-w-1 overflow-hidden rounded-md bg-gray-100 group-hover:opacity-75">-->
<!--                          <img :src="item.imageSrc" :alt="item.imageAlt" class="object-cover object-center" />-->
<!--                        </div>-->
<!--                        <a :href="item.href" class="mt-6 block text-sm font-medium text-gray-900">-->
<!--                          <span class="absolute inset-0 z-10" aria-hidden="true" />-->
<!--                          {{ item.name }}-->
<!--                        </a>-->
<!--                        <p aria-hidden="true" class="mt-1 text-sm text-gray-500">Shop now</p>-->
<!--                      </div>-->
<!--                    </div>-->
<!--                  </TabPanel>-->
<!--                </TabPanels>-->
<!--              </TabGroup>-->

<!--              <div class="space-y-6 border-t border-gray-200 px-4 py-6">-->
<!--                <div v-for="page in navigation.pages" :key="page.name" class="flow-root">-->
<!--                  <a :href="page.href" class="-m-2 block p-2 font-medium text-gray-900">{{ page.name }}</a>-->
<!--                </div>-->
<!--              </div>-->

<!--              <div class="space-y-6 border-t border-gray-200 px-4 py-6">-->
<!--                <div class="flow-root">-->
<!--                  <a href="#" class="-m-2 block p-2 font-medium text-gray-900">Create an account</a>-->
<!--                </div>-->
<!--                <div class="flow-root">-->
<!--                  <a href="#" class="-m-2 block p-2 font-medium text-gray-900">Sign in</a>-->
<!--                </div>-->
<!--              </div>-->

<!--              <div class="space-y-6 border-t border-gray-200 px-4 py-6">-->
<!--                &lt;!&ndash; Currency selector &ndash;&gt;-->
<!--                <form>-->
<!--                  <div class="inline-block">-->
<!--                    <label for="mobile-currency" class="sr-only">Currency</label>-->
<!--                    <div class="group relative -ml-2 rounded-md border-transparent focus-within:ring-2 focus-within:ring-white">-->
<!--                      <select id="mobile-currency" name="currency" class="flex items-center rounded-md border-transparent bg-none py-0.5 pl-2 pr-5 text-sm font-medium text-gray-700 focus:border-transparent focus:outline-none focus:ring-0 group-hover:text-gray-800">-->
<!--                        <option v-for="currency in currencies" :key="currency">{{ currency }}</option>-->
<!--                      </select>-->
<!--                      <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center">-->
<!--&lt;!&ndash;                        <ChevronDownIcon class="h-5 w-5 text-gray-500" aria-hidden="true" />&ndash;&gt;-->
<!--                      </div>-->
<!--                    </div>-->
<!--                  </div>-->
<!--                </form>-->
<!--              </div>-->
<!--            </DialogPanel>-->
<!--          </TransitionChild>-->
<!--        </div>-->
<!--      </Dialog>-->
<!--    </TransitionRoot>-->

<!--    &lt;!&ndash; Hero section &ndash;&gt;-->
<!--    <div class="relative bg-gray-900">-->
<!--      &lt;!&ndash; Decorative image and overlay &ndash;&gt;-->
<!--      <div aria-hidden="true" class="absolute inset-0 overflow-hidden">-->
<!--        <img src="https://tailwindui.com/img/ecommerce-images/home-page-01-hero-full-width.jpg" alt="" class="h-full w-full object-cover object-center" />-->
<!--      </div>-->
<!--      <div aria-hidden="true" class="absolute inset-0 bg-gray-900 opacity-50" />-->

<!--      &lt;!&ndash; Navigation &ndash;&gt;-->
<!--      <header class="relative z-10">-->
<!--        <nav aria-label="Top">-->
<!--          &lt;!&ndash; Top navigation &ndash;&gt;-->
<!--          <div class="bg-gray-900">-->
<!--            <div class="mx-auto flex h-10 max-w-7xl items-center justify-between px-4 sm:px-6 lg:px-8">-->
<!--              &lt;!&ndash; Currency selector &ndash;&gt;-->
<!--              <form>-->
<!--                <div>-->
<!--                  <label for="desktop-currency" class="sr-only">Currency</label>-->
<!--                  <div class="group relative -ml-2 rounded-md border-transparent bg-gray-900 focus-within:ring-2 focus-within:ring-white">-->
<!--                    <select id="desktop-currency" name="currency" class="flex items-center rounded-md border-transparent bg-gray-900 bg-none py-0.5 pl-2 pr-5 text-sm font-medium text-white focus:border-transparent focus:outline-none focus:ring-0 group-hover:text-gray-100">-->
<!--                      <option v-for="currency in currencies" :key="currency">{{ currency }}</option>-->
<!--                    </select>-->
<!--                    <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center">-->
<!--&lt;!&ndash;                      <ChevronDownIcon class="h-5 w-5 text-gray-300" aria-hidden="true" />&ndash;&gt;-->
<!--                    </div>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </form>-->

<!--              <div class="flex items-center space-x-6">-->
<!--&lt;!&ndash;                <a href="#" class="text-sm font-medium text-white hover:text-gray-100">Sign in</a>&ndash;&gt;-->
<!--                <a href="#" class="text-sm font-medium text-white hover:text-gray-100">{{ tg.initDataUnsafe }}</a>-->
<!--              </div>-->
<!--            </div>-->
<!--          </div>-->

<!--          &lt;!&ndash; Secondary navigation &ndash;&gt;-->
<!--          <div class="bg-white bg-opacity-10 backdrop-blur-md backdrop-filter">-->
<!--            <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">-->
<!--              <div>-->
<!--                <div class="flex h-16 items-center justify-between">-->
<!--                  &lt;!&ndash; Logo (lg+) &ndash;&gt;-->
<!--                  <div class="hidden lg:flex lg:flex-1 lg:items-center">-->
<!--                    <a href="#">-->
<!--                      <span class="sr-only">Your Company</span>-->
<!--                      <img class="h-8 w-auto" src="https://tailwindui.com/img/logos/mark.svg?color=white" alt="" />-->
<!--                    </a>-->
<!--                  </div>-->

<!--                  <div class="hidden h-full lg:flex">-->
<!--                    &lt;!&ndash; Flyout menus &ndash;&gt;-->
<!--                    <PopoverGroup class="inset-x-0 bottom-0 px-4">-->
<!--                      <div class="flex h-full justify-center space-x-8">-->
<!--                        <Popover v-for="category in navigation.categories" :key="category.name" class="flex" v-slot="{ open }">-->
<!--                          <div class="relative flex">-->
<!--                            <PopoverButton class="relative z-10 flex items-center justify-center text-sm font-medium text-white transition-colors duration-200 ease-out">-->
<!--                              {{ category.name }}-->
<!--                              <span :class="[open ? 'bg-white' : '', 'absolute inset-x-0 -bottom-px h-0.5 transition duration-200 ease-out']" aria-hidden="true" />-->
<!--                            </PopoverButton>-->
<!--                          </div>-->

<!--                          <transition enter-active-class="transition ease-out duration-200" enter-from-class="opacity-0" enter-to-class="opacity-100" leave-active-class="transition ease-in duration-150" leave-from-class="opacity-100" leave-to-class="opacity-0">-->
<!--                            <PopoverPanel class="absolute inset-x-0 top-full text-sm text-gray-500">-->
<!--                              &lt;!&ndash; Presentational element used to render the bottom shadow, if we put the shadow on the actual panel it pokes out the top, so we use this shorter element to hide the top of the shadow &ndash;&gt;-->
<!--                              <div class="absolute inset-0 top-1/2 bg-white shadow" aria-hidden="true" />-->

<!--                              <div class="relative bg-white">-->
<!--                                <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">-->
<!--                                  <div class="grid grid-cols-4 gap-x-8 gap-y-10 py-16">-->
<!--                                    <div v-for="item in category.featured" :key="item.name" class="group relative">-->
<!--                                      <div class="aspect-h-1 aspect-w-1 overflow-hidden rounded-md bg-gray-100 group-hover:opacity-75">-->
<!--                                        <img :src="item.imageSrc" :alt="item.imageAlt" class="object-cover object-center" />-->
<!--                                      </div>-->
<!--                                      <a :href="item.href" class="mt-4 block font-medium text-gray-900">-->
<!--                                        <span class="absolute inset-0 z-10" aria-hidden="true" />-->
<!--                                        {{ item.name }}-->
<!--                                      </a>-->
<!--                                      <p aria-hidden="true" class="mt-1">Shop now</p>-->
<!--                                    </div>-->
<!--                                  </div>-->
<!--                                </div>-->
<!--                              </div>-->
<!--                            </PopoverPanel>-->
<!--                          </transition>-->
<!--                        </Popover>-->

<!--                        <a v-for="page in navigation.pages" :key="page.name" :href="page.href" class="flex items-center text-sm font-medium text-white">{{ page.name }}</a>-->
<!--                      </div>-->
<!--                    </PopoverGroup>-->
<!--                  </div>-->

<!--                  &lt;!&ndash; Mobile menu and search (lg-) &ndash;&gt;-->
<!--                  <div class="flex flex-1 items-center lg:hidden">-->
<!--                    <button type="button" class="-ml-2 p-2 text-white" @click="mobileMenuOpen = true">-->
<!--                      <span class="sr-only">Open menu</span>-->
<!--&lt;!&ndash;                      <Bars3Icon class="h-6 w-6" aria-hidden="true" />&ndash;&gt;-->
<!--                    </button>-->

<!--                    &lt;!&ndash; Search &ndash;&gt;-->
<!--&lt;!&ndash;                    <a href="#" class="ml-2 p-2 text-white">&ndash;&gt;-->
<!--&lt;!&ndash;                      <span class="sr-only">Search</span>&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                      <MagnifyingGlassIcon class="h-6 w-6" aria-hidden="true" />&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;                    </a>&ndash;&gt;-->
<!--                  </div>-->

<!--                  &lt;!&ndash; Logo (lg-) &ndash;&gt;-->
<!--                  <a href="#" class="lg:hidden">-->
<!--                    <span class="sr-only">Your Company</span>-->
<!--                    <img src="https://tailwindui.com/img/logos/mark.svg?color=white" alt="" class="h-8 w-auto" />-->
<!--                  </a>-->

<!--                  <div class="flex flex-1 items-center justify-end">-->
<!--&lt;!&ndash;                    <a href="#" class="hidden text-sm font-medium text-white lg:block">Search</a>&ndash;&gt;-->

<!--                    <div class="flex items-center lg:ml-8">-->
<!--                      &lt;!&ndash; Help &ndash;&gt;-->
<!--                      <a href="#" class="p-2 text-white lg:hidden">-->
<!--                        <span class="sr-only">Help</span>-->
<!--&lt;!&ndash;                        <QuestionMarkCircleIcon class="h-6 w-6" aria-hidden="true" />&ndash;&gt;-->
<!--                      </a>-->
<!--                      <a href="#" class="hidden text-sm font-medium text-white lg:block">Help</a>-->

<!--                      &lt;!&ndash; Cart &ndash;&gt;-->
<!--&lt;!&ndash;                      <div class="ml-4 flow-root lg:ml-8">&ndash;&gt;-->
<!--&lt;!&ndash;                        <a href="#" class="group -m-2 flex items-center p-2">&ndash;&gt;-->
<!--&lt;!&ndash;&lt;!&ndash;                          <ShoppingBagIcon class="h-6 w-6 flex-shrink-0 text-white" aria-hidden="true" />&ndash;&gt;&ndash;&gt;-->
<!--&lt;!&ndash;                          <span class="ml-2 text-sm font-medium text-white">0</span>&ndash;&gt;-->
<!--&lt;!&ndash;                          <span class="sr-only">items in cart, view bag</span>&ndash;&gt;-->
<!--&lt;!&ndash;                        </a>&ndash;&gt;-->
<!--&lt;!&ndash;                      </div>&ndash;&gt;-->
<!--                    </div>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>-->
<!--            </div>-->
<!--          </div>-->
<!--        </nav>-->
<!--      </header>-->

<!--      <div class="relative mx-auto flex max-w-3xl flex-col items-center px-6 py-32 text-center sm:py-64 lg:px-0">-->
<!--        <h1 class="text-4xl font-bold tracking-tight text-white lg:text-6xl">Katerina N</h1>-->
<!--        <p class="mt-4 text-xl text-white">The new arrivals have, well, newly arrived. Check out the latest options from our summer small-batch release while they're still in stock.</p>-->
<!--        <a href="#" class="mt-8 inline-block rounded-md border border-transparent bg-white px-8 py-3 text-base font-medium text-gray-900 hover:bg-gray-100">Shop New Arrivals</a>-->
<!--      </div>-->
<!--    </div>-->

<!--    <main>-->

<!--    </main>-->

<!--    <footer aria-labelledby="footer-heading" class="bg-gray-900">-->
<!--      <h2 id="footer-heading" class="sr-only">Footer</h2>-->
<!--      <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">-->
<!--        <div class="py-20 xl:grid xl:grid-cols-3 xl:gap-8">-->
<!--          <div class="grid grid-cols-2 gap-8 xl:col-span-2">-->
<!--            <div class="space-y-12 md:grid md:grid-cols-2 md:gap-8 md:space-y-0">-->
<!--              <div>-->
<!--                <h3 class="text-sm font-medium text-white">Shop</h3>-->
<!--                <ul role="list" class="mt-6 space-y-6">-->
<!--                  <li v-for="item in footerNavigation.shop" :key="item.name" class="text-sm">-->
<!--                    <a :href="item.href" class="text-gray-300 hover:text-white">{{ item.name }}</a>-->
<!--                  </li>-->
<!--                </ul>-->
<!--              </div>-->
<!--              <div>-->
<!--                <h3 class="text-sm font-medium text-white">Company</h3>-->
<!--                <ul role="list" class="mt-6 space-y-6">-->
<!--                  <li v-for="item in footerNavigation.company" :key="item.name" class="text-sm">-->
<!--                    <a :href="item.href" class="text-gray-300 hover:text-white">{{ item.name }}</a>-->
<!--                  </li>-->
<!--                </ul>-->
<!--              </div>-->
<!--            </div>-->
<!--            <div class="space-y-12 md:grid md:grid-cols-2 md:gap-8 md:space-y-0">-->
<!--              <div>-->
<!--                <h3 class="text-sm font-medium text-white">Account</h3>-->
<!--                <ul role="list" class="mt-6 space-y-6">-->
<!--                  <li v-for="item in footerNavigation.account" :key="item.name" class="text-sm">-->
<!--                    <a :href="item.href" class="text-gray-300 hover:text-white">{{ item.name }}</a>-->
<!--                  </li>-->
<!--                </ul>-->
<!--              </div>-->
<!--              <div>-->
<!--                <h3 class="text-sm font-medium text-white">Connect</h3>-->
<!--                <ul role="list" class="mt-6 space-y-6">-->
<!--                  <li v-for="item in footerNavigation.connect" :key="item.name" class="text-sm">-->
<!--                    <a :href="item.href" class="text-gray-300 hover:text-white">{{ item.name }}</a>-->
<!--                  </li>-->
<!--                </ul>-->
<!--              </div>-->
<!--            </div>-->
<!--          </div>-->
<!--          <div class="mt-12 md:mt-16 xl:mt-0">-->
<!--            <h3 class="text-sm font-medium text-white">Sign up for our newsletter</h3>-->
<!--            <p class="mt-6 text-sm text-gray-300">The latest deals and savings, sent to your inbox weekly.</p>-->
<!--            <form class="mt-2 flex sm:max-w-md">-->
<!--              <label for="email-address" class="sr-only">Email address</label>-->
<!--              <input id="email-address" type="text" autocomplete="email" required="" class="w-full min-w-0 appearance-none rounded-md border border-white bg-white px-4 py-2 text-base text-gray-900 placeholder-gray-500 shadow-sm focus:border-white focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-900" />-->
<!--              <div class="ml-4 flex-shrink-0">-->
<!--                <button type="submit" class="flex w-full items-center justify-center rounded-md border border-transparent bg-indigo-600 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 focus:ring-offset-gray-900">Sign up</button>-->
<!--              </div>-->
<!--            </form>-->
<!--          </div>-->
<!--        </div>-->

<!--        <div class="border-t border-gray-800 py-10">-->
<!--          <p class="text-sm text-gray-400">Copyright &copy; 2021 Your Company, Inc.</p>-->
<!--        </div>-->
<!--      </div>-->
<!--    </footer>-->
<!--  </div>-->
</template>

<script setup>
import { ref } from 'vue'
import {
  Dialog,
  DialogPanel,
  Popover,
  PopoverButton,
  PopoverGroup,
  PopoverPanel,
  Tab,
  TabGroup,
  TabList,
  TabPanel,
  TabPanels,
  TransitionChild,
  TransitionRoot,
} from '@headlessui/vue'
// import {
  // Bars3Icon,
  // MagnifyingGlassIcon,
  // QuestionMarkCircleIcon,
  // ShoppingBagIcon,
  // XMarkIcon,
// } from '@heroicons/vue/24/outline'
// import { ChevronDownIcon } from '@heroicons/vue/20/solid'

const currencies = ['CAD', 'USD', 'AUD', 'EUR', 'GBP']
const navigation = {
  categories: [
    {
      name: 'Women',
      featured: [
        {
          name: 'New Arrivals',
          href: '#',
          imageSrc: 'https://tailwindui.com/img/ecommerce-images/mega-menu-category-01.jpg',
          imageAlt: 'Models sitting back to back, wearing Basic Tee in black and bone.',
        },
        {
          name: 'Basic Tees',
          href: '#',
          imageSrc: 'https://tailwindui.com/img/ecommerce-images/mega-menu-category-02.jpg',
          imageAlt: 'Close up of Basic Tee fall bundle with off-white, ochre, olive, and black tees.',
        },
        {
          name: 'Accessories',
          href: '#',
          imageSrc: 'https://tailwindui.com/img/ecommerce-images/mega-menu-category-03.jpg',
          imageAlt: 'Model wearing minimalist watch with black wristband and white watch face.',
        },
        {
          name: 'Carry',
          href: '#',
          imageSrc: 'https://tailwindui.com/img/ecommerce-images/mega-menu-category-04.jpg',
          imageAlt: 'Model opening tan leather long wallet with credit card pockets and cash pouch.',
        },
      ],
    },
    {
      name: 'Men',
      featured: [
        {
          name: 'New Arrivals',
          href: '#',
          imageSrc: 'https://tailwindui.com/img/ecommerce-images/mega-menu-01-men-category-01.jpg',
          imageAlt: 'Hats and sweaters on wood shelves next to various colors of t-shirts on hangers.',
        },
        {
          name: 'Basic Tees',
          href: '#',
          imageSrc: 'https://tailwindui.com/img/ecommerce-images/mega-menu-01-men-category-02.jpg',
          imageAlt: 'Model wearing light heather gray t-shirt.',
        },
        {
          name: 'Accessories',
          href: '#',
          imageSrc: 'https://tailwindui.com/img/ecommerce-images/mega-menu-01-men-category-03.jpg',
          imageAlt:
              'Grey 6-panel baseball hat with black brim, black mountain graphic on front, and light heather gray body.',
        },
        {
          name: 'Carry',
          href: '#',
          imageSrc: 'https://tailwindui.com/img/ecommerce-images/mega-menu-01-men-category-04.jpg',
          imageAlt: 'Model putting folded cash into slim card holder olive leather wallet with hand stitching.',
        },
      ],
    },
  ],
  pages: [
    { name: 'Company', href: '#' },
    { name: 'Stores', href: '#' },
  ],
}
const categories = [
  {
    name: 'New Arrivals',
    href: '#',
    imageSrc: 'https://tailwindui.com/img/ecommerce-images/home-page-01-category-01.jpg',
  },
  {
    name: 'Productivity',
    href: '#',
    imageSrc: 'https://tailwindui.com/img/ecommerce-images/home-page-01-category-02.jpg',
  },
  {
    name: 'Workspace',
    href: '#',
    imageSrc: 'https://tailwindui.com/img/ecommerce-images/home-page-01-category-04.jpg',
  },
  {
    name: 'Accessories',
    href: '#',
    imageSrc: 'https://tailwindui.com/img/ecommerce-images/home-page-01-category-05.jpg',
  },
  { name: 'Sale', href: '#', imageSrc: 'https://tailwindui.com/img/ecommerce-images/home-page-01-category-03.jpg' },
]
const collections = [
  {
    name: 'Handcrafted Collection',
    href: '#',
    imageSrc: 'https://tailwindui.com/img/ecommerce-images/home-page-01-collection-01.jpg',
    imageAlt: 'Brown leather key ring with brass metal loops and rivets on wood table.',
    description: 'Keep your phone, keys, and wallet together, so you can lose everything at once.',
  },
  {
    name: 'Organized Desk Collection',
    href: '#',
    imageSrc: 'https://tailwindui.com/img/ecommerce-images/home-page-01-collection-02.jpg',
    imageAlt: 'Natural leather mouse pad on white desk next to porcelain mug and keyboard.',
    description: 'The rest of the house will still be a mess, but your desk will look great.',
  },
  {
    name: 'Focus Collection',
    href: '#',
    imageSrc: 'https://tailwindui.com/img/ecommerce-images/home-page-01-collection-03.jpg',
    imageAlt: 'Person placing task list card into walnut card holder next to felt carrying case on leather desk pad.',
    description: 'Be more productive than enterprise project managers with a single piece of paper.',
  },
]
const footerNavigation = {
  shop: [
    { name: 'Bags', href: '#' },
    { name: 'Tees', href: '#' },
    { name: 'Objects', href: '#' },
    { name: 'Home Goods', href: '#' },
    { name: 'Accessories', href: '#' },
  ],
  company: [
    { name: 'Who we are', href: '#' },
    { name: 'Sustainability', href: '#' },
    { name: 'Press', href: '#' },
    { name: 'Careers', href: '#' },
    { name: 'Terms & Conditions', href: '#' },
    { name: 'Privacy', href: '#' },
  ],
  account: [
    { name: 'Manage Account', href: '#' },
    { name: 'Returns & Exchanges', href: '#' },
    { name: 'Redeem a Gift Card', href: '#' },
  ],
  connect: [
    { name: 'Contact Us', href: '#' },
    { name: 'Facebook', href: '#' },
    { name: 'Instagram', href: '#' },
    { name: 'Pinterest', href: '#' },
  ],
}

const mobileMenuOpen = ref(false)
const tg = inject('tg')
</script>