<template>
  <div>
    <h1>Aplikasi Vue.js</h1>
    <!-- <MyComponent nama="Kaka Ridwan" namaLengkap="M. Ridwan Nurfauzi H.P" tanggalLahir="3 Mei 2006"
      jenisKelamin="Laki-laki" agama="Islam" alamat="Ds. Rancamanyar" />
    <Hobi hobi="Bersepeda" /> -->
    <!-- <Aritmatika angka1="2" angka2="8" /> -->

    <!-- <Latihan nama="Ridwan" jumlah="5" bayar="100000" /> -->

    <button @click="setnama()">set nama</button>
    <p>
      Nama saya adalah {{ nama }}.
    </p>
    <hr>
    <CekUmur nama="Ridwan" umur="14" />
    <hr>
    <Pengulangan/>
  </div>
</template>

<script>
import MyComponent from "./MyComponent.vue";
import Hobi from "./Hobi.vue";
import Aritmatika from "./Aritmatika.vue";
import Latihan from "./Latihan.vue";
import CekUmur from "./CekUmur.vue";
import Pengulangan from "./Pengulangan.vue";

export default {
  components: {
    MyComponent,
    Hobi,
    Aritmatika,
    Latihan,
    CekUmur,
    Pengulangan
  },
  data() {
    return {
      nama: ''
    }
  },
  methods: {
    setnama() {
      this.nama = this.nama ? '' : "Ridwan";
    }
  }
}

</script>
