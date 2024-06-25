<template>
    <Layout>
        <div class="w-full flex justify-center py-8">
            <div class="bg-white rounded-xl shadow-lg w-[1240px] min-h-[1754px] py-10 px-20 space-y-4">
                <div class="flex w-full justify-center mb-2">
                    <div class="w-40 h-40 rounded-full overflow-hidden">
                        <img class="object-cover w-40 h-40" src="/images/logo.jpg">
                    </div>
                </div>
                <h1 class="text-3xl font-bold text-center">การลงทะเบียนเข้าร่วมงานศิลปวัฒนธรรมอุดมศึกษาครั้งที่ 23</h1>
                <p class="text-lx text-center">ระหว่างวันที่ 23-25 กุมภาพันธ์ 2567 ณ มหาวิทยาลัยxxx</p>

                <!-- User ID -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        ชื่อสถาบัน
                    </div>
                    <div class="col-span-9">
                        {{ performance.owner.institution }}
                    </div>
                </div>

                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        ชื่อผู้ประสานงาน
                    </div>
                    <div class="col-span-9">
                        {{ performance.owner.name }}
                    </div>
                </div>
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        อีเมลล์
                    </div>
                    <div class="col-span-9">
                        {{ performance.owner.email }}
                    </div>
                </div>
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        เบอร์โทรศัพท์
                    </div>
                    <div class="col-span-9">
                        {{ performance.owner.tel }}
                    </div>
                </div>
                <!-- Institution Head Name -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Institution Head Name
                    </div>
                    <div class="col-span-9">
                        {{ performance.institution_head_name }}
                    </div>
                </div>

                <!-- Institution Head Position -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Institution Head Position
                    </div>
                    <div class="col-span-9">
                        {{ performance.institution_head_position }}
                    </div>
                </div>

                <!-- Coordinator Position -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Coordinator Position
                    </div>
                    <div class="col-span-9">
                        {{ performance.coordinator_position }}
                    </div>
                </div>

                <!-- Name -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Name
                    </div>
                    <div class="col-span-9">
                        {{ performance.name }}
                    </div>
                </div>

                <!-- Type -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Type
                    </div>
                    <div class="col-span-9">
                        <ul>
                            <li v-for="(type,index) in performance.type" :key="index">{{ type }}</li>
                        </ul>
                    </div>
                </div>
                <!-- Description -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Description
                    </div>
                    <div class="col-span-9">
                        {{ performance.description }}
                    </div>
                </div>

                <!-- Duration -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Duration
                    </div>
                    <div class="col-span-9">
                        {{ performance.duration }}
                    </div>
                </div>

                <!-- Number of Performers -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Number of Performers
                    </div>
                    <div class="col-span-9">
                        {{ performance.number_of_performers }}
                    </div>
                </div>

                <!-- Directors -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Directors
                    </div>
                    <div class="col-span-9">
                        {{ performance.directors }}
                    </div>
                </div>

                <!-- Performers -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Performers
                    </div>
                    <div class="col-span-9">
                        {{ performance.performers }}
                    </div>
                </div>

                <!-- Musicians or Narrators -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Musicians or Narrators
                    </div>
                    <div class="col-span-9">
                        {{ performance.musicians_or_narrators }}
                    </div>
                </div>

                <!-- Number of Musicians -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Number of Musicians
                    </div>
                    <div class="col-span-9">
                        {{ performance.number_of_musicians }}
                    </div>
                </div>

                <!-- Opening Scene -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Opening Scene
                    </div>
                    <div class="col-span-9">
                        {{ performance.opening_scene }}
                    </div>
                </div>

                <!-- Stage Performance -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Stage Performance
                    </div>
                    <div class="col-span-9">
                        {{ performance.stage_performance }}
                    </div>
                </div>

                <!-- Ending Scene -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Ending Scene
                    </div>
                    <div class="col-span-9">
                        {{ performance.ending_scene }}
                    </div>
                </div>

                <!-- Costume and Props -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Costume and Props
                    </div>
                    <div class="col-span-9">
                        {{ performance.costume_and_props }}
                    </div>
                </div>

                <!-- Stage Lighting -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Stage Lighting
                    </div>
                    <div class="col-span-9">
                        {{ performance.stage_lighting }}
                    </div>
                </div>

                <!-- Sound Type -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Sound Type
                    </div>
                    <div class="col-span-9">
                        {{ performance.sound_type }}
                    </div>
                </div>

                <!-- Number of Microphones -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Number of Microphones
                    </div>
                    <div class="col-span-9">
                        {{ performance.number_of_microphones }}
                    </div>
                </div>

                <!-- Number of Amplifiers -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Number of Amplifiers
                    </div>
                    <div class="col-span-9">
                        {{ performance.number_of_amplifiers }}
                    </div>
                </div>

                <!-- Other Specifications -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Other Specifications
                    </div>
                    <div class="col-span-9">
                        {{ performance.other_specifications }}
                    </div>
                </div>

                <!-- Sound Control -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Sound Control
                    </div>
                    <div class="col-span-9">
                        {{ performance.sound_control }}
                    </div>
                </div>

                <!-- Institution Representatives -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Institution Representatives
                    </div>
                    <div class="col-span-9">
                        {{ performance.institution_representatives }}
                    </div>
                </div>

                <!-- Faculty and Staff -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Faculty and Staff
                    </div>
                    <div class="col-span-9">
                        {{ performance.faculty_and_staff }}
                    </div>
                </div>

                <!-- Students -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Students
                    </div>
                    <div class="col-span-9">
                        {{ performance.students }}
                    </div>
                </div>

                <!-- Vehicles -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Vehicles
                    </div>
                    <div class="col-span-9">
                        {{ performance.vehicles }}
                    </div>
                </div>

                <!-- Arrival Date -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Arrival Date
                    </div>
                    <div class="col-span-9">
                        {{ performance.arrival_date }}
                    </div>
                </div>

                <!-- Arrival Time -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Arrival Time
                    </div>
                    <div class="col-span-9">
                        {{ performance.arrival_time }}
                    </div>
                </div>

                <!-- Departure Date -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Departure Date
                    </div>
                    <div class="col-span-9">
                        {{ performance.departure_date }}
                    </div>
                </div>

                <!-- Departure Time -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Departure Time
                    </div>
                    <div class="col-span-9">
                        {{ performance.departure_time }}
                    </div>
                </div>

                <!-- Accommodation -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Accommodation
                    </div>
                    <div class="col-span-9">
                        {{ performance.accommodation }}
                    </div>
                </div>

                <!-- Ceremony and Reception Details -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Ceremony and Reception Details
                    </div>
                    <div class="col-span-9">
                        {{ performance.ceremony_and_reception_details }}
                    </div>
                </div>

                <!-- Number of Institution Heads -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Number of Institution Heads
                    </div>
                    <div class="col-span-9">
                        {{ performance.number_of_institution_heads }}
                    </div>
                </div>

                <!-- Number of Faculty and Staff -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Number of Faculty and Staff
                    </div>
                    <div class="col-span-9">
                        {{ performance.number_of_faculty_and_staff }}
                    </div>
                </div>

                <!-- Number of Students -->
                <div class="grid grid-cols-12 gap-2">
                    <div class="col-span-3">
                        Number of Students
                    </div>
                    <div class="col-span-9">
                        {{ performance.number_of_students }}
                    </div>
                </div>
                <p>รูป</p>
                <div class="w-full grid grid-cols-5 gap-4 mt-4">
                    <div v-for="(image,index) in displayImages" :key="index" class="w-full h-60 overflow-hidden">
                        <div class="h-60 relative">
                            <img :src="image.url" class="object-cover w-full h-60">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </Layout>
</template>

<script>
import Layout from "@/Pages/Layout/Layout.vue";
import {Link} from "@inertiajs/vue3";


export default {
    name: "ShowPerformance",
    components: {Layout, Link},
    props: {
        performance: {
            type: Object,
            required: true
        }
    },
    data() {
        return {
            displayImages: []
        };
    },
    mounted() {
        if (this.performance.images.data.length > 0) {
            this.displayImages = this.performance.images.data
        }
    },
    methods: {},
    watch: {},
    computed: {}
};
</script>

<style scoped>
</style>
