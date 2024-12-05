<template>
    <section class="pb-16">
      <div class="max-w-screen-lg mx-auto px-4 md:px-8">
        <div class="max-w-md">
          <h1 class="text-white text-2xl font-bold sm:text-3xl">Premios a entregar</h1>
        </div>
        <ul class="mt-5 space-y-3">
          <li v-for="(item, idx) in members" :key="idx" class="px-4 py-5 duration-150 hover:border-white hover:rounded-xl  hover:text-black hover:bg-violet-950 max-md:hover:bg-transparent">
            <a :href="item.path" class="space-y-3">
              <div class="flex items-center gap-x-3">
                <div class="bg-white w-14 h-14 border rounded-full flex items-center justify-center"><img :src="item.company_icon" width="30" :alt="item.company_name" class="project-image"></div>
                <div>
                  <span class="block text-xl text-indigo-600 font-bold">{{ item.company_name }}</span>
                  <h3 class="text-base text-yellow-300 font-thin mt-1">{{ item.job_title }}</h3>
                </div>
              </div>
              <p class="text-white sm:text-sm font-semibold">
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
  import hater from '../assets/images/hater.png'

  export default {
    name: 'OpenPositions',
    data() {
      return {
        members: [
          {
            company_icon: mod,
            company_name: 'MOD DEL AÑO',
            job_title: 'Premio a definir',
            job_description: 'Se le entregará el premio al moderador más activo. Además, se tendrán en cuenta todos los aportes realizados a la comunidad durante el 2024.',
          },
          {
            company_icon: vip,
            company_name: 'VIP DEL AÑO',
            job_title: 'Premio a definir',
            job_description: 'El premio lo obtendrá el vip más activo del canal. También, se considerará su rol y su importancia dentro de la comunidad durante el año.',
          },
          {
            company_icon: viewer,
            company_name: 'VIEWER DEL AÑO',
            job_title: 'Premio a definir',
            job_description: 'Será ganador/a la persona que más tiempo consumió el contenido del canal y más activo estuvo en el chat en 2024.',
          },
          {
            company_icon: hater,
            company_name: 'HATER DEL AÑO',
            job_title: 'Premio a definir',
            job_description: 'Se le entregará el premio al espectador que más hate haya tirado a Tukita durante 2024.',
          }
        ]
      }
    }
  }
  </script>