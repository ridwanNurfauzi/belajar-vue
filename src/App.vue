<script setup>
import { ref } from "vue";

let msg = "Assalaamualaikum";
let txt = "Ini adalah contoh teks.";
let red = "#f00";
let blue = "#00f";
let rawHtml = `<span style="color: red">Ini seharusnya merah.</span>`;
let rawText = `<span style="color: red">Ini seharusnya tidak merah.</span>`;

let datas =
  [
    {
      "kode_barang": "1001",
      "nama_barang": "Keyboard",
      "harga": "32000",
      "stock": "3"
    },
    {
      "kode_barang": "1002",
      "nama_barang": "Wajan",
      "harga": "28000",
      "stock": "4"
    },
    {
      "kode_barang": "1003",
      "nama_barang": "Kaus Kaki",
      "harga": "5500",
      "stock": "4"
    },
    {
      "kode_barang": "1004",
      "nama_barang": "Spatula",
      "harga": "32000",
      "stock": "3"
    },
    {
      "kode_barang": "1005",
      "nama_barang": "Baju",
      "harga": "120000",
      "stock": "4"
    },
    {
      "kode_barang": "1006",
      "nama_barang": "Piring",
      "harga": "12000",
      "stock": "4"
    },
    {
      "kode_barang": "1007",
      "nama_barang": "Sendok",
      "harga": "1000",
      "stock": "10"
    },
    {
      "kode_barang": "1008",
      "nama_barang": "Garpu",
      "harga": "1000",
      "stock": "10"
    },
    {
      "kode_barang": "1009",
      "nama_barang": "Meteran",
      "harga": "30000",
      "stock": "4"
    },
    {
      "kode_barang": "1010",
      "nama_barang": "Penggaris 30cm",
      "harga": "6000",
      "stock": "6"
    },
    {
      "kode_barang": "1011",
      "nama_barang": "Timbangan",
      "harga": "82000",
      "stock": "3"
    },
    {
      "kode_barang": "1012",
      "nama_barang": "Celana panjang",
      "harga": "95000",
      "stock": "9"
    },
    {
      "kode_barang": "1013",
      "nama_barang": "Setrika Listrik",
      "harga": "65000",
      "stock": "2"
    },
    {
      "kode_barang": "1014",
      "nama_barang": "Topi",
      "harga": "45000",
      "stock": "9"
    },
    {
      "kode_barang": "1015",
      "nama_barang": "Penyedot debu",
      "harga": "50000",
      "stock": "2"
    }
  ]

let s = true;
</script>

<template>
  <div>
    <span v-bind:style="{ color: blue }">{{ msg }}</span> <br>
    <span v-html="rawHtml"></span> <br>
    <span v-text="rawText"></span>

    <table border="1">
      <thead>
        <tr>
          <th>No</th>
          <th>Kode Barang</th>
          <th>Nama Barang</th>
          <th>Harga</th>
          <th>Stock</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(data, i) in datas">
          <td>{{ i + 1 }}</td>
          <td>{{ data.kode_barang }}</td>
          <td>{{ data.nama_barang }}</td>
          <td>{{ data.harga }}</td>
          <td>{{ data.stock }}</td>
        </tr>
      </tbody>
    </table>
    <br>
    {{ txt.split('').reverse().join('') }}
    <br>
    <p v-if="s">
      {{ text }}
    </p>

    <button v-on:click="reversetxt()">Reverse</button>

  </div>
</template>

<script>
export default {
  data() {
    return {
      text: 'Hallo Dunia',
    }
  },
  methods: {
    reversetxt (){
      this.text = this.text.split('').reverse().join('')
    }
  }
}
</script>