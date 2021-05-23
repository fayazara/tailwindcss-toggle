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
          icon: "fas fa-plane",
          color: "bg-yellow-500",
          value: false,
        },
        {
          label: "Security",
          icon: "fas fa-fingerprint",
          color: "bg-red-500",
          value: true,
        },
        {
          label: "Backups",
          icon: "fas fa-wifi",
          color: "bg-indigo-500",
          value: true,
        },
        {
          label: "Developer Mode",
          icon: "fas fa-terminal",
          color: "bg-gray-500",
          value: false,
        },
        {
          label: "Connect to Google Drive",
          icon: "fab fa-google-drive",
          color: "bg-blue-500",
          value: true,
        },
      ],
    };
  },
};
</script>