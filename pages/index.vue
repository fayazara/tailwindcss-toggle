<template>
  <main class="min-h-screen bg-gray-100 max-w-sm mx-auto">
    <div class="border">
      <Header />
      <ul class="border-b border-t bg-white divide-y">
        <li v-for="(item, i) in menuItems" :key="i">
          <menu-item :options="item" />
        </li>
      </ul>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      menuItems: [
        {
          label: "Airplane Mode",
          icon: "fa-plane",
          color: "yellow",
          value: false,
        },
        {
          label: "Security",
          icon: "fa-fingerprint",
          color: "red",
          value: true,
        },
        {
          label: "Backups",
          icon: "fa-wifi",
          color: "indigo",
          value: true,
        },
        {
          label: "Developer Mode",
          icon: "fa-terminal",
          color: "gray",
          value: false,
        },
        {
          label: "Backups",
          icon: "fa-cloud-download-alt",
          color: "green",
          value: true,
        },
      ],
    };
  },
};
</script>