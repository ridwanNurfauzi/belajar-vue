<template>
    <div>
        <p>Angka 1 : {{ angka1 }}</p>
        <p>Angka 2 : {{ angka2 }}</p>
        <p>Hasilnya : {{ hasil }}</p>
    </div>
</template>

<script>
export default {
    props: [
        'angka1',
        'angka2'
    ],
    data(){
        return {
            hasil: parseInt(this.angka1) + parseInt(this.angka2)
        }
    },
    // penjumlahan() {
    //     return {
    //         a: this.angka1,
    //         b: this.angka2,
    //         hasil: this.angka1 + this.angka2
    //     }
    // }
}
</script>
