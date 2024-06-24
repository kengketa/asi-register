<template>
    <Layout>
        <div>
            <div v-if="$page.props.user" class="card bg-base-100 w-96 shadow-xl">
                <figure>
                    <img
                        alt="Shoes"
                        src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg"/>
                </figure>
                <div class="card-body">
                    <h2 class="card-title">งานศิลปวัฒนธรรมอุดมศึกษา</h2>
                    <p>{{ $page.props.user.institution }}</p>
                    <div class="card-actions justify-end">
                        <Link :href="route('form')" class="btn btn-primary">แก้ไข</Link>
                    </div>
                </div>
            </div>
        </div>
    </Layout>
</template>

<script>
import Layout from "@/Pages/Layout/Layout.vue";
import TeachingMaterialCard from "@/Pages/Components/TeachingMaterialCard.vue";
import axios from 'axios';
import {Link} from "@inertiajs/vue3";
import {router} from "@inertiajs/vue3";

export default {
    name: "Index",
    components: {Layout, Link},
    props: {},
    data() {
        return {};
    },
    mounted() {

    },
    methods: {},
    watch: {},
    computed: {}
};
</script>

<style scoped>
</style>
