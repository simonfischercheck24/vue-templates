<template>
  <section class="rounded-md bg-white m-2">
    <div class="w-full flex text-left bg-slate-100 p-2 rounded-t-md justify-between">
        <h2 class=" text-lg">{{ friend.name }}</h2>
        <button class="rounded-md bg-emerald-600 p-1 hover:bg-emerald-800" @click="toggleDetails">{{ detailsAreVisible ? 'Hide' : 'Show' }} Details</button>

    </div>
    <div class="p-2">
        <ul v-if="detailsAreVisible">
          <li><strong>Phone:</strong> {{ friend.phone }}</li>
          <li><strong>Email:</strong> {{ friend.email }}</li>
        </ul>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      detailsAreVisible: false,
      friend: {
        id: 'manuel',
        name: 'Manuel Lorenz',
        phone: '0123 45678 90',
        email: 'manuel@localhost.com',
      },
    }
  },
  methods: {
    toggleDetails() {
      this.detailsAreVisible = !this.detailsAreVisible
    },
  },
}
</script>
