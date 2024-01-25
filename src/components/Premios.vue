<template>
    <section class="py-16">
      <div class="max-w-screen-lg mx-auto px-4 md:px-8">
        <div class="max-w-md">
          <h1 class="text-white text-2xl font-extrabold sm:text-3xl">PREMIOS LRS</h1>
        </div>
        <ul class="mt-12 divide-y space-y-3">
          <li v-for="(item, idx) in members" :key="idx" class="px-4 py-5 duration-150 hover:border-white hover:rounded-xl  hover:text-black hover:bg-violet-400">
            <a :href="item.path" class="space-y-3">
              <div class="flex items-center gap-x-3">
                <div class="bg-white w-14 h-14 border rounded-full flex items-center justify-center"><img :src="item.company_icon" width="30" :alt="item.company_name" class="project-image"></div>
                <div>
                  <span class="block text-xl text-indigo-600 font-bold">{{ item.company_name }}</span>
                  <h3 class="text-base text-yellow-300 font-thin mt-1">{{ item.job_title }}</h3>
                </div>
              </div>
              <p class="text-white sm:text-sm">
                {{ item.job_description }}
              </p>
            </a>
          </li>
        </ul>
      </div>
    </section>
  </template>
  
  <script>
  import mod from '../assets/images/mod.png';
  import vip from '../assets/images/vip.png';
  import dupla from '../assets/images/dupla.png'
  import viewer from '../assets/images/viewer.png'
  import meme from '../assets/images/meme.png'

  export default {
    name: 'OpenPositions',
    data() {
      return {
        members: [
          {
            company_icon: mod,
            company_name: 'MOD DEL AÑO',
            job_title: 'Premio a entregar',
            job_description: 'Explicación de como ganar el premio',
          },
          {
            company_icon: vip,
            company_name: 'VIP DEL AÑO',
            job_title: 'Premio a entregar',
            job_description: 'Explicación de como ganar el premio',
          },
          {
            company_icon: viewer,
            company_name: 'VIEWER DEL AÑO',
            job_title: 'Premio a entregar',
            job_description: 'Explicación de como ganar el premio',
          },
          {
            company_icon: dupla,
            company_name: 'DUPLA DEL AÑO',
            job_title: 'Premio a entregar',
            job_description: 'Explicación de como ganar el premio',
          },
          {
            company_icon: meme,
            company_name: 'MEME DEL AÑO',
            job_title: 'Premio a entregar',
            job_description: 'Explicación de como ganar el premio',
          }
        ]
      }
    }
  }
  </script>