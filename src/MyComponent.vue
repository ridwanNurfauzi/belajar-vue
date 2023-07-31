<template>
  <div>
    <hr>
    <h2>Halo, {{ nama }}!</h2>
    <p>Nama Lengkap : {{ namaLengkap }}</p>
    <p>Tanggal Lahir : {{ tanggalLahir }}</p>
    <p>Jenis Kelamin : {{ jenisKelamin }}</p>
    <p>Agama : {{ agama }}</p>
    <p>Alamat : {{ alamat }}</p>

    <p>{{ pesan }}</p>
  </div>
</template>
  
<script>
export default {
  props: [
    'nama',
    'namaLengkap',
    'tanggalLahir',
    'jenisKelamin',
    'agama',
    'alamat'
  ], // Definisi props "nama" dan "umur"
  data(){
    return {
      pesan: 'Halo nama saya '+ this.nama
    }
  }
}
</script>
