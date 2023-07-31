<!-- 1 bks = 5000
ageng 5 bks

ageng + 100000 -->

<template>
    <div>
        <p>
            Pada tanggal 23 Juli 2023 ada seorang anak laki-laki bernama <b>{{ nama }}</b> membeli makaroni basah
            dengan harga Rp. {{ harga }} perbungkus. <br>
            Kemudian beliau membelinya sebanyak {{ jumlah }} bungkus
            dengan total harga Rp. {{ totalHarga }}. <br>
            Lalu beliau membayar dengan uang dengan berjumlah Rp. {{ bayar }}. <br>
            Berarti Beliau menerima kembalian dengan uang berjumlah Rp. {{ kembalian }}.
        </p>
    </div>
</template>

<script>
export default {
    props: ['nama', 'jumlah', 'bayar'],
    data() {
        return {
            harga: 5000,
            totalHarga: 0,
            kembalian: 0
        }
    },
    created() {
        this.totalHarga = this.harga * parseInt(this.jumlah);
        this.kembalian = parseInt(this.bayar) - this.totalHarga;
    }
}
</script>