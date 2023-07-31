<template>
    <div>
      <ul>
        <li v-for="item in items" :key="item.id" >{{ item.nama }}</li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        items: [
          { id: 1, nama: 'Apel' },
          { id: 2, nama: 'Jeruk' },
          { id: 3, nama: 'Pisang' }
        ]
      };
    }
  }
  </script>