<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <div class="relative bg-white overflow-hidden">
    <div class="max-w-7xl mx-auto">
        <div class="relative z-10 pb-8 bg-white sm:pb-16 md:pb-20 lg:max-w-2xl lg:w-full lg:pb-28 xl:pb-32">


        <Popover>
          <div class="relative pt-6 px-4 sm:px-6 lg:px-8">
            <nav class="relative flex items-center justify-between sm:h-10 lg:justify-start" aria-label="Global">
              <div class="flex items-center flex-grow flex-shrink-0 lg:flex-grow-0">
                <div class="flex items-center justify-between w-full md:w-auto">
                  <a href="#">
                    <span class="sr-only">Workflow</span>
                    <img alt="Workflow" class="h-8 w-auto sm:h-10" src="@/assets/logo.png" />
                  </a>
                  <div class="-mr-2 flex items-center md:hidden">
                    <PopoverButton class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500">
                      <span class="sr-only">Open main menu</span>
                      <MenuIcon class="h-6 w-6" aria-hidden="true" />
                    </PopoverButton>
                  </div>
                </div>
              </div>
              <div class="hidden md:block md:ml-10 md:pr-4 md:space-x-8">
                <a v-for="item in navigation" :key="item.name" :href="item.href" class="font-medium text-gray-500 hover:text-gray-900">{{ item.name }}</a>
                <a href="/camp/tools" class="font-medium text-indigo-600 hover:text-indigo-500">软件资源</a>
              </div>
            </nav>
          </div>

          <transition enter-active-class="duration-150 ease-out" enter-from-class="opacity-0 scale-95" enter-to-class="opacity-100 scale-100" leave-active-class="duration-100 ease-in" leave-from-class="opacity-100 scale-100" leave-to-class="opacity-0 scale-95">
            <PopoverPanel focus class="absolute z-10 top-0 inset-x-0 p-2 transition transform origin-top-right md:hidden">
              <div class="rounded-lg shadow-md bg-white ring-1 ring-black ring-opacity-5 overflow-hidden">
                <div class="px-5 pt-4 flex items-center justify-between">
                  <div>
                    <img class="h-8 w-auto" src="@/assets/logo.png" alt="" />
                  </div>
                  <div class="-mr-2">
                    <PopoverButton class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500">
                      <span class="sr-only">Close main menu</span>
                      <XIcon class="h-6 w-6" aria-hidden="true" />
                    </PopoverButton>
                  </div>
                </div>
                <div class="px-2 pt-2 pb-3 space-y-1">
                  <a v-for="item in navigation" :key="item.name" :href="item.href" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50">{{ item.name }}</a>
                </div>
                <a href="/camp/tools" class="block w-full px-5 py-3 text-center font-medium text-indigo-600 bg-gray-50 hover:bg-gray-100"> 软件资源 </a>
              </div>
            </PopoverPanel>
          </transition>
        </Popover>
        
        <main class="mt-10 mx-auto max-w-6xl px-4 sm:mt-12 sm:px-6 md:mt-16 lg:mt-20 lg:px-8 xl:mt-28">
          <div class="sm:text-center lg:text-left">
            <h1 class="text-4xl tracking-tight font-extrabold text-gray-900 sm:text-5xl md:text-6xl">
              <span class="block mb-4 xl:inline text-4xl">江西师范大学计算机信息工程学院<br/></span>
              <span class="block mt-2 text-indigo-600 xl:inline text-6xl">新生程序设计训练营</span>
            </h1>
            <p class="mt-3 text-base text-gray-500 sm:mt-5 sm:text-lg sm:max-w-xl sm:mx-auto md:mt-5 md:text-xl lg:mx-0">江西师范大学计算机信息工程学院-暑期新生程序设计训练营是由学生社团和指导老师共同组织的非盈利性培训活动，主要面向22级新生开展编程基础普及课程，旨在帮助同学们预先学习编程知识，打下坚实的基础，更好的与新学期课程相衔接。</p>
            <div class="mt-5 sm:mt-8 sm:flex sm:justify-center lg:justify-start">
              <div class="rounded-md shadow">
                <a href="/camp/register" class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 md:py-4 md:text-lg md:px-10">立即报名</a>
              </div>
              <div class="mt-3 sm:mt-0 sm:ml-3">
                <a href="/camp/course" class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-indigo-700 bg-indigo-100 hover:bg-indigo-200 md:py-4 md:text-lg md:px-10">课程安排</a>
              </div>
            </div>
          </div>
        </main>
        </div>
        <div class="lg:absolute lg:inset-y-0 lg:right-0 lg:w-1/2">
            <img class="h-56 w-full object-cover overflow-visible sm:h-72 md:h-96 lg:w-full lg:h-full" src="@/assets/MAIN.png" alt="" />
        </div>
    </div>
    </div>

    <section class="text-center">
    <div class="max-w-screen-xl px-4 py-16 mx-auto sm:px-6 lg:px-8">
        <ul class="grid grid-cols-2 gap-4 border-2 border-indigo-600 rounded-xl lg:grid-cols-4">
        <li class="p-8">
            <p class="text-2xl font-extrabold text-indigo-500">{{ RegNum }}</p>
            <p class="mt-1 text-lg font-medium">已报名人数</p>
        </li>

        <li class="p-8">
            <p class="text-2xl font-extrabold text-indigo-500">2022.8.21</p>
            <p class="mt-1 text-lg font-medium">开始时间</p>
        </li>

        <li class="p-8">
            <p class="text-2xl font-extrabold text-indigo-500">6</p>
            <p class="mt-1 text-lg font-medium">总课时</p>
        </li>

        <li class="p-8">
            <p class="text-2xl font-extrabold text-indigo-500">Online</p>
            <p class="mt-1 text-lg font-medium">开展形式</p>
        </li>
        </ul>
    </div>
    </section>

    <div class="pb-16" id="Introduction"> <IntroductionCard/> </div>
    
    <CompetitionCard/>
    


    <FooterComponent/>
</template>

<script setup>
    import IntroductionCard from '@/components/IntroductionCard.vue'
    import CompetitionCard from '@/components/CompetitionCard.vue'
    import FooterComponent from '@/components/footer.vue'
    import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
    import { MenuIcon, XIcon } from '@heroicons/vue/outline'
    import axios from 'axios'

    const navigation = [
    { name: '了解详情', href: '/camp/main' },
    { name: '课程安排', href: '/camp/course' },
    { name: '报名咨询', href: '/camp/register' },
    { name: 'About ACS', href: '#' },
    ]
</script>

<script>
    axios.interceptors.request.use(config => {
        if (/get/i.test(config.method)) { //判断get请求
            config.params  =  config.params || {};
            config.params.t = Date.parse(new Date())/1000; //添加时间戳
        }
        return config;
    }, error => {
        return Promise.reject(error);
    })
    
    export default {
    name: 'MainPage',
    components: {
        IntroductionCard
    },
    data() {
        return{
            RegNum: '',
        }
        
    },
    created() {
        axios
        .get("api/getRegNum")
        .then((res) => {
            this.RegNum = res.data[0]["count(case when hasActivated=1 then 1 end)"]
        })
        .catch((err) => {
            console.log(err);
        });
    }
}

</script>


