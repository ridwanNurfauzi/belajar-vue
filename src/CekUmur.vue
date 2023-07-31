<template>
    <div>
        <p v-if="dataUmur > 17">Selamat menjelang dewasa {{ nama }}, Umur anda {{ dataUmur }}</p>
        <div v-else>
            <button @click="tambahUmur()">Tambah umur</button>
            <p>
                Mohon maaf {{ nama }} umur anda belum cukup. saat ini umur
                anda {{ dataUmur }}
            </p>
        </div>
    </div>
</template>

<script>
export default {
    props: ["nama", "umur"],
    methods: {
        tambahUmur(){
            this.dataUmur = parseInt(this.dataUmur) + 10;
        }
    },
    data(){
        return {
            dataUmur: this.umur
        }
    }
}
</script>