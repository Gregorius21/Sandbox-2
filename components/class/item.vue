<<<<<<< HEAD
<template>
  <div class="card">
    <img :src="img" class="card-img-top" :alt="'foto ' +name">
    <div class="card-body">
      <h5 class="card-title">{{name}}</h5>
      <p class="card-text">{{desc}}</p>
      <button v-if="!unfollow" type="button" class="btn btn-primary" @click="followClass">Follow</button>
      <button v-else type="button" class="btn btn-outline-danger" @click="followClass">Unfollow</button>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    name: {
      type: String,
      default: "Nama Kelas",
    },
    desc: {
      type: String,
      default: "Ini deskripsi kelasnya ya",
    },
    img: {
      type: String,
      default: "https://shiftacademy.id/wp-content/uploads/2021/09/1.png",
    },
    unfollow: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    followClass() {
      const data = {
        name: this.name,
        desc: this.desc,
        img: this.img,
      };
      if (this.unfollow) this.$emit("unfollow-class", data);
      else this.$emit("follow-class", data);
    },
  },
};
=======
<template>
  <div class="card">
    <!-- <img src="..." class="card-img-top" alt="..."> -->
    <div class="card-body">
      <h5 class="card-title">{{name}}</h5>
      <p class="card-text">{{desc}}</p>
      <a href="#" class="btn btn-primary">Go somewhere</a>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    name: {
      type: String,
      default: "Nama Kelas",
    },
    desc: {
      type: String,
      default: "Ini deskripsi kelasnya ya",
    },
  },
};
>>>>>>> 6d515e9e349a3f341e821dd44fe8affba6fa3280
</script>