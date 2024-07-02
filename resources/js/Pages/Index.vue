<template>
    <Layout>
        <div>
            <div v-if="$page.props.user.role.name ==='user'" class="card bg-base-100 w-96 shadow-xl">
                <figure>
                    <img alt="Shoes"
                         src="https://img.daisyui.com/images/stock/photo-1494232410401-ad00d5433cfa.jpg"/>
                </figure>
                <div class="card-body">
                    <h2 class="card-title">งานศิลปวัฒนธรรมอุดมศึกษา</h2>
                    <p>{{ $page.props.user.institution }}</p>
                    <div class="card-actions justify-end">
                        <Link v-if="!performance || (performance && !performance.is_published)" :href="route('form')"
                              class="btn btn-primary">
                            แก้ไข
                        </Link>
                        <div v-if="performance && performance.is_published"
                             class="px-4 py-2 bg-green-700 rounded-md text-white opacity-50">
                            ส่งเรียบร้อย
                        </div>
                        <Link v-if="performance && performance.is_published"
                              :href="route('performance_view',performance.id)"
                              class="px-4 py-2 bg-primary rounded-md text-white cursor-pointer">
                            ดูสรุป
                        </Link>
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
    props: {
        performance: {
            type: Object || null,
            default: null
        }
    },
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
