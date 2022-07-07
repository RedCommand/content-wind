<script setup lang="ts">
const props = defineProps({
  title: {
    type: String,
    default: ''
  },
  description: {
    type: String,
    default: ''
  },
  image: {
    type: String,
    default: ''
  }
})
</script>

<!-- <template>
  <section class="py-20">
    <Container class="-my-14 lg:grid lg:grid-flow-col-dense lg:space-x-10">
      <div class="my-5 lg:my-0">
        <div class="text-3xl font-bold text-gray-900 shrink dark:text-gray-100">
          <p v-if="title">
            {{ title }}
          </p>
          <Markdown v-else :use="$slots.title" unwrap="p" />
        </div>
        <div v-if="description || $slots.description" class="pt-5">
          <p v-if="description">
            {{ description }}
          </p>
          <Markdown v-else :use="$slots.description" unwrap="p" />
        </div>
      </div>
      <div class="scale-90">
        <img
          v-if="image"
          class="rounded-3xl"
          :src="props.image"
          alt=" heroicons-outline:exclamation "
        >
      </div>
    </Container>
  </section>
</template> -->

<template>
  <section class="">
    <Container class="lg:grid lg:grid-flow-col-dense">
      <div class="">
        <div class="text-3xl font-bold text-gray-900 shrink dark:text-gray-100">
          <p v-if="title">
            {{ title }}
          </p>
          <Markdown v-else :use="$slots.title" unwrap="p" />
        </div>
        <div v-if="description || $slots.description" class="pt-5 mt-3">
          <p v-if="description">
            {{ description }}
          </p>
          <Markdown v-else :use="$slots.description" unwrap="p" />
        </div>
      </div>
      <div class="lg:h-[192px] lg:w-[388px] mt-8 lg:mt-0 lg:ml-[56px] md:max-h-[274px] bg-slate-500">
        <img
          v-if="image"
          class="object-fill w-full h-full rounded-3xl opacity-20"
          :src="props.image"
          alt=" heroicons-outline:exclamation "
        >
      </div>
    </Container>
  </section>
</template>
