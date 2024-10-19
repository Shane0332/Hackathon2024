<template>
  <div class="sticky top-20 mt-5">
    <p class="font-bold">Сургуулиуд</p>

    <ul>
      <template v-for="(r, i) in reminders" :key="i">
        <li>
          <div class="mt-5 flex items-center justify-between">
            <div class="flex items-center gap-3">
              <Icon name="heroicons:check-circle" class="h-4 w-4 text-muted-foreground" />
              <span :class="{'font-bold underline text-blue-500': r.title === '105-р сургууль', 'text-sm': true}">{{ r.title }}</span>
            </div>
            <span class="text-sm text-muted-foreground">{{ r.time }}</span>
          </div>
        </li>
      </template>
    </ul>
  </div>
</template>

<script setup lang="ts">
  const reminders = [
    { title: "105-р сургууль", time: "" },
    { title: "104-р сургууль", time: "" },
    { title: "151-р сургууль", time: "" },
    { title: "4-р сургууль", time: "" },
  ];
</script>
