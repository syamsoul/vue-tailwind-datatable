<script setup>
import { ref } from 'vue';
import DataTable from '@/data-table.vue';

const defaultItemsPerPage = ref(5);
const allowedItemsPerPage = ref([5, 10, 20, 50, 100]);

const is_search_enable = ref(true);

const columns = ['ID', 'Name'];

const data = ref([
    [1, 'Zul'], [2, 'Nana'], [3, 'Siti'], [4, 'Soul'], [5, 'Ayu'], [6, 'Yen'], [7, 'Suzana'], [8, 'Jam'],
    [9, 'Ros'], [10, 'Jan'], [11, 'Wan'], [12, 'Mohd'], [13, 'Azri'], [14, 'Teh'], [15, 'Mizi'], [16, 'Mamat'],
    [17, 'Ali'], [18, 'Jannah'], [19, 'Ameer'], [20, 'Sudesh'], [21, 'Aliudin'], [22, 'Halimah'], [23, 'Nora'], [24, 'Muda'],
    [25, 'Sarifah'], [26, 'Maznah'], [27, 'Ain'], [28, 'Cho'], [29, 'Ema'], [30, 'Sha'], [31, 'Ji'], [32, 'Aimi'],
    [33, 'Bisor'], [34, 'Cek'], [35, 'Sarah'], [36, 'Mudzir'], [37, 'Mahathir'], [38, 'Halim'], [39, 'Hilmi'], [40, 'Fin'],
]);
</script>

<template>
    <div id="app">
        <data-table 
            :columns="columns"
            :data="data"
            :allowedItemsPerPage="allowedItemsPerPage"
            :defaultItemsPerPage="defaultItemsPerPage"
            :is_search_enable="is_search_enable"
        />
    </div>
</template>

<style>
  @import '../dist/main.css';
</style>