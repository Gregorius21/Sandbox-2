<template>
  <div class="main-sidebar">
    <aside id="sidebar-wrapper">
      <div class="sidebar-brand">
        <a href="index.html">Stisla</a>
      </div>
      <div class="sidebar-brand sidebar-brand-sm">
        <a href="index.html">St</a>
      </div>
      <ul class="sidebar-menu">
        <li v-for="(menu,i) in listMenu" :key="i">
          <nuxt-link class="nav-link" :to="menu.to">
            <i :class="menu.icon"></i> <span>{{menu.name}}</span>
          </nuxt-link>
        </li>
      </ul>
    </aside>
  </div>
</template> 

<script>
export default {
  data() {
    return {
      listMenu: [
        {
          name: "Dashboard baru",
          icon: "fas fa-home",
          to: "/",
          role: ["admin", "tutor"],
        },
        {
          name: "Semua Kelas",
          icon: "fas fa-igloo",
          to: "/semua-kelas",
        },
        {
          name: "Data Binding",
          icon: "fas fa-book",
          to: "/example/data-binding",
        },
        {
          name: "Methods",
          icon: "fas fa-book",
          to: "/example/methods",
        },
        {
          name: "Computed",
          icon: "fas fa-book",
          to: "/example/computed",
        },
        {
          name: "Watcher",
          icon: "fas fa-book",
          to: "/example/watcher",
        },
         {
          name: "SANDBOX1",
          icon: "fas fa-book",
          to: "/example/sand-box-1",
        },
      ],
    };
  },
};
</script>