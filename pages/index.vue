<template>
  <div class="p-10 sm:p-10 md:p-20 w-full h-full">
    <div class="grid grid-cols-9 gap-8">
      <div class="col-span-3">
        <div class="flex flex-col gap-8 justify-between h-full">
          <div>
            <h1 class="pb-6">Who Are We</h1>
            <p>{{ intro }}</p>
          </div>
          <div>
            <s-button>About Us</s-button>
          </div>
        </div>
      </div>
      <div class="col-span-3">
        <img class="w-full h-full" src="~/assets/imgs/hero-img.png" />
      </div>
      <div class="col-span-3">
        <div class="grid-rows-4 grid gap-8">
          <div class="row-span-2">
            <img class="w-full h-full" src="~/assets/imgs/hero-img.png" />
          </div>
          <div class="row-span-2">
            <img class="w-full h-full" src="~/assets/imgs/hero-img.png" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SButton from '~/components/SButton.vue'
export default {
  name: 'IndexPage',
  components: { SButton },
  data: () => {
    return {
      intro:
        'Sustainable Ocean Alliance Thailand (SOA Thailand)  คือกลุ่มคนรักทะเลในประเทศไทยที่รวมตัวกันเพื่อแชร์และแลกเปลี่ยนข้อมูล และลงมือทำเพื่อแก้ไขปัญหาทางทะเลที่เกิดขึ้น',
    }
  },
}
</script>
