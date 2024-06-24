<template>
    <Layout>
        <div class="flex w-full justify-center mb-2">
            <div class="w-40 h-40 rounded-full overflow-hidden">
                <img class="object-cover w-40 h-40" src="/images/logo.jpg">
            </div>
        </div>
        <h1 class="text-3xl font-bold text-center">การลงทะเบียนเข้าร่วมงานศิลปวัฒนธรรมอุดมศึกษาครั้งที่ 23</h1>
        <p class="text-lx text-center">ระหว่างวันที่ 23-25 กุมภาพันธ์ 2567 ณ มหาวิทยาลัยxxx</p>
        <div class="bg-white w-full shadow-lg rounded-xl px-8 py-8 mt-4">
            <form>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">Email</span>
                            </div>
                            <input v-model="form.email" class="input input-bordered w-full" disabled
                                   placeholder="Type here"
                                   type="text"/>
                        </label>
                        <div v-if="$page.props.errors.email" class="text-red-500 text-sm">
                            {{ $page.props.errors.email }}
                        </div>
                    </div>
                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">ชื่อสถาบันการศึกษา</span>
                            </div>
                            <input v-model="form.institution" class="input input-bordered w-full" disabled
                                   placeholder="Type here"
                                   type="text"/>
                        </label>
                        <div v-if="$page.props.errors.institution" class="text-red-500 text-sm">
                            {{ $page.props.errors.institution }}
                        </div>
                    </div>
                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">ชื่อ-สกุลผู้บริหารสถาบันการศึกษา</span>
                            </div>
                            <input v-model="form.institution_head_name" class="input input-bordered w-full"
                                   placeholder="Type here" type="text"/>
                        </label>
                        <div v-if="$page.props.errors.institution_head_name" class="text-red-500 text-sm">
                            {{ $page.props.errors.institution_head_name }}
                        </div>
                    </div>
                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">ตำแหน่ง ผู้บริหารสถาบันการศึกษา</span>
                            </div>
                            <input v-model="form.institution_head_position" class="input input-bordered w-full"
                                   placeholder="Type here" type="text"/>
                        </label>
                        <div v-if="$page.props.errors.institution_head_position" class="text-red-500 text-sm">
                            {{ $page.props.errors.institution_head_position }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">ชื่อ-สกุลผู้ประสานงานประจำสถาบัน</span>
                            </div>
                            <input v-model="form.coordinator_name" class="input input-bordered w-full" disabled
                                   placeholder="Type here" type="text"/>
                        </label>
                        <div v-if="$page.props.errors.coordinator_name" class="text-red-500 text-sm">
                            {{ $page.props.errors.coordinator_name }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">ตำแหน่งผู้ประสานงานประจำสถาบัน</span>
                            </div>
                            <input v-model="form.coordinator_position" class="input input-bordered w-full"
                                   placeholder="Type here" type="text"/>
                        </label>
                        <div v-if="$page.props.errors.coordinator_position" class="text-red-500 text-sm">
                            {{ $page.props.errors.coordinator_position }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">หมายเลขโทรศัพท์ ผู้ประสานงานประจำสถาบัน</span>
                            </div>
                            <input v-model="form.coordinator_phone" class="input input-bordered w-full" disabled
                                   placeholder="Type here" type="text"/>
                        </label>
                        <div v-if="$page.props.errors.coordinator_phone" class="text-red-500 text-sm">
                            {{ $page.props.errors.coordinator_phone }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">ชื่อชุดการการแสดง</span>
                            </div>
                            <input v-model="form.performance_name" class="input input-bordered w-full"
                                   placeholder="Type here" type="text"/>
                        </label>
                        <div v-if="$page.props.errors.performance_name" class="text-red-500 text-sm">
                            {{ $page.props.errors.performance_name }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">ประเภทชุดการแสดง</span>
                            </div>
                            <div class="flex flex-col gap-2">
                                <label class="inline-flex items-center">
                                    <input v-model="form.performance_type" class="checkbox"
                                           type="checkbox" value="การแสดงนาฏศิลป์ไทย">
                                    <span class="ml-2">การแสดงนาฏศิลป์ไทย</span>
                                </label>
                                <label class="inline-flex items-center">
                                    <input v-model="form.performance_type" class="checkbox" type="checkbox"
                                           value="การแสดงนาฏศิลป์พื้นบ้าน">
                                    <span class="ml-2">การแสดงนาฏศิลป์พื้นบ้าน</span>
                                </label>
                                <label class="inline-flex items-center">
                                    <input v-model="form.performance_type" class="checkbox" type="checkbox"
                                           value="การแสดงนาฏศิลป์ร่วมสมัย">
                                    <span class="ml-2">การแสดงนาฏศิลป์ร่วมสมัย</span>
                                </label>
                            </div>
                        </label>
                        <div v-if="$page.props.errors.performance_type" class="text-red-500 text-sm">
                            {{ $page.props.errors.performance_type }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">คำอธิบายประกอบชุดการแสดง</span>
                            </div>
                            <textarea v-model="form.performance_description"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.performance_description" class="text-red-500 text-sm">
                            {{ $page.props.errors.performance_description }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">ระยะเวลาในการแสดง</span>
                            </div>
                            <input v-model="form.performance_duration" class="input input-bordered w-full"
                                   placeholder="เช่น 1.5 ชั่วโมง" type="text"/>
                        </label>
                        <div v-if="$page.props.errors.performance_duration" class="text-red-500 text-sm">
                            {{ $page.props.errors.performance_duration }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">จำนวนนักแสดง(คน)</span>
                            </div>
                            <input v-model="form.number_of_performers" class="input input-bordered w-full"
                                   placeholder="เช่น 10" type="number"/>
                        </label>
                        <div v-if="$page.props.errors.number_of_performers" class="text-red-500 text-sm">
                            {{ $page.props.errors.number_of_performers }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">รายชื่อผู้ควบคุมการแสดง</span>
                            </div>
                            <textarea v-model="form.performance_directors"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="1.นายคิดดี มีชัย" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.performance_directors" class="text-red-500 text-sm">
                            {{ $page.props.errors.performance_directors }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">รายชื่อนักแสดง</span>
                            </div>
                            <textarea v-model="form.performers"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="1.นายคิดดี มีชัย" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.performers" class="text-red-500 text-sm">
                            {{ $page.props.errors.performers }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">รายชื่อนักดนตรี/ผู้พากย์หรือผู้บรรยาย</span>
                            </div>
                            <textarea v-model="form.musicians_or_narrators"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="1.นายคิดดี มีชัย" rows="4"></textarea>

                        </label>
                        <div v-if="$page.props.errors.musicians_or_narrators" class="text-red-500 text-sm">
                            {{ $page.props.errors.musicians_or_narrators }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">จำนวนนักดนตรี(คน)</span>
                            </div>
                            <input v-model="form.number_of_musicians" class="input input-bordered w-full"
                                   placeholder="เช่น 10" type="number"/>
                        </label>
                        <div v-if="$page.props.errors.number_of_musicians" class="text-red-500 text-sm">
                            {{ $page.props.errors.number_of_musicians }}
                        </div>
                    </div>
                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">การเปิดเรื่องหรือภาพแสดงเริ่มแรกบนเวที</span>
                            </div>
                            <textarea v-model="form.opening_scene"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="Type here" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.opening_scene" class="text-red-500 text-sm">
                            {{ $page.props.errors.opening_scene }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">การดำเนินเรื่องบนเวที</span>
                            </div>
                            <textarea v-model="form.stage_performance"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="Type here" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.stage_performance" class="text-red-500 text-sm">
                            {{ $page.props.errors.stage_performance }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">การจบเรื่อง</span>
                            </div>
                            <textarea v-model="form.ending_scene"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="Type here" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.ending_scene" class="text-red-500 text-sm">
                            {{ $page.props.errors.ending_scene }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">ลักษณะการแต่งกายและอุปกรณ์ประกอบการแสดง</span>
                            </div>
                            <textarea v-model="form.costume_and_props"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="Type here" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.costume_and_props" class="text-red-500 text-sm">
                            {{ $page.props.errors.costume_and_props }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">การควบคุมแสงบนเวที</span>
                            </div>
                            <textarea v-model="form.stage_lighting"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="Type here" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.stage_lighting" class="text-red-500 text-sm">
                            {{ $page.props.errors.stage_lighting }}
                        </div>
                    </div>
                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">ประเภทของเสียงประกอบการแสดง</span>
                            </div>
                            <textarea v-model="form.sound_type"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="Type here" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.sound_type" class="text-red-500 text-sm">
                            {{ $page.props.errors.sound_type }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">จำนวนไมค์โครโฟน(ตัว)</span>
                            </div>
                            <input v-model="form.number_of_microphones" class="input input-bordered w-full"
                                   placeholder="เช่น 10" type="number"/>
                        </label>
                        <div v-if="$page.props.errors.number_of_microphones" class="text-red-500 text-sm">
                            {{ $page.props.errors.number_of_microphones }}
                        </div>
                    </div>
                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">จำนวนตู้แอมป์(ตู้)</span>
                            </div>
                            <input v-model="form.number_of_amplifiers" class="input input-bordered w-full"
                                   placeholder="เช่น 10" type="number"/>
                        </label>
                        <div v-if="$page.props.errors.number_of_amplifiers" class="text-red-500 text-sm">
                            {{ $page.props.errors.number_of_amplifiers }}
                        </div>
                    </div>
                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">อื่นๆ โปรดระบุ</span>
                            </div>
                            <textarea v-model="form.other_specifications"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="Type here" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.other_specifications" class="text-red-500 text-sm">
                            {{ $page.props.errors.other_specifications }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">การควบคุมเสียง</span>
                            </div>
                            <textarea v-model="form.sound_control"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="Type here" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.sound_control" class="text-red-500 text-sm">
                            {{ $page.props.errors.sound_control }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">รายชื่อผู้บริหาร/ผู้แทนสถาบัน</span>
                            </div>
                            <textarea v-model="form.institution_representatives"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="1.นายทำดี มานะ" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.institution_representatives" class="text-red-500 text-sm">
                            {{ $page.props.errors.institution_representatives }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">รายชื่ออาจารย์ / เจ้าหน้าที่</span>
                            </div>
                            <textarea v-model="form.faculty_and_staff"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="1.นายทำดี มานะ" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.faculty_and_staff" class="text-red-500 text-sm">
                            {{ $page.props.errors.faculty_and_staff }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">รายชื่อนักศึกษา</span>
                            </div>
                            <textarea v-model="form.students"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="1.นายทำดี มานะ" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.students" class="text-red-500 text-sm">
                            {{ $page.props.errors.students }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">รายการยานพาหนะ</span>
                            </div>
                            <textarea v-model="form.vehicles"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="1.รถบัส 40 ที่นั่ง" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.vehicles" class="text-red-500 text-sm">
                            {{ $page.props.errors.vehicles }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">วันที่เดินทางมาถึง</span>
                            </div>
                            <input v-model="form.arrival_date" class="input input-bordered w-full"
                                   placeholder="Type here" type="date"/>
                        </label>
                        <div v-if="$page.props.errors.arrival_date" class="text-red-500 text-sm">
                            {{ $page.props.errors.arrival_date }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">เวลาที่เดินทางมาถึง</span>
                            </div>
                            <input v-model="form.arrival_time" class="input input-bordered w-full"
                                   placeholder="Type here" type="time"/>
                        </label>
                        <div v-if="$page.props.errors.arrival_time" class="text-red-500 text-sm">
                            {{ $page.props.errors.arrival_time }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">วันที่เดินทางกลับ</span>
                            </div>
                            <input v-model="form.departure_date" class="input input-bordered w-full"
                                   placeholder="Type here" type="date"/>
                        </label>
                        <div v-if="$page.props.errors.departure_date" class="text-red-500 text-sm">
                            {{ $page.props.errors.departure_date }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">เวลาที่เดินทางกลับ</span>
                            </div>
                            <input v-model="form.departure_time" class="input input-bordered w-full"
                                   placeholder="Type here" type="time"/>
                        </label>
                        <div v-if="$page.props.errors.departure_time" class="text-red-500 text-sm">
                            {{ $page.props.errors.departure_time }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">รายชื่อสถานที่พัก</span>
                            </div>
                            <textarea v-model="form.accommodation"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="1.โรงแรมสวนหลวง" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.accommodation" class="text-red-500 text-sm">
                            {{ $page.props.errors.accommodation }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">ข้อมูลการเข้าร่วมพิธีเปิดและการเลี้ยงรับรอง</span>
                            </div>
                            <textarea v-model="form.ceremony_and_reception_details"
                                      class="w-full border border-gray-300 rounded-md px-4 py-4"
                                      placeholder="Type here" rows="4"></textarea>
                        </label>
                        <div v-if="$page.props.errors.ceremony_and_reception_details" class="text-red-500 text-sm">
                            {{ $page.props.errors.ceremony_and_reception_details }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span
                                    class="label-text capitalize">จำนวนผู้บริหาร / ผู้แทนสถาบันการศึกษา ที่เข้าร่วม(ท่าน)</span>
                            </div>
                            <input v-model="form.number_of_institution_heads" class="input input-bordered w-full"
                                   placeholder="เช่น 10" type="number"/>
                        </label>
                        <div v-if="$page.props.errors.number_of_institution_heads" class="text-red-500 text-sm">
                            {{ $page.props.errors.number_of_institution_heads }}
                        </div>
                    </div>

                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span
                                    class="label-text capitalize">จำนวนผู้ควบคุม / อาจารย์ / เจ้าหน้าที่ ที่เข้าร่วม (ท่าน)</span>
                            </div>
                            <input v-model="form.number_of_faculty_and_staff" class="input input-bordered w-full"
                                   placeholder="เช่น 10" type="number"/>
                        </label>
                        <div v-if="$page.props.errors.number_of_faculty_and_staff" class="text-red-500 text-sm">
                            {{ $page.props.errors.number_of_faculty_and_staff }}
                        </div>
                    </div>
                    <div>
                        <label class="form-control w-full">
                            <div class="label">
                                <span class="label-text capitalize">จำนวนนักศึกษา ที่เข้าร่วม (คน)</span>
                            </div>
                            <input v-model="form.number_of_students" class="input input-bordered w-full"
                                   placeholder="เช่น 10" type="number"/>
                        </label>
                        <div v-if="$page.props.errors.number_of_students" class="text-red-500 text-sm">
                            {{ $page.props.errors.number_of_students }}
                        </div>
                    </div>
                    <div class="col-span-2 w-full mt-2 flex gap-4 justify-end">
                        <button :disabled="isSubmitting" class="btn btn-warning text-white" type="button"
                                @click.prevent="saveDraft">บันทึกร่าง
                        </button>
                        <button :disabled="isSubmitting" class="btn btn-primary text-white" type="button">ส่งข้อมูล
                        </button>
                    </div>
                </div>
            </form>
        </div>
    </Layout>
</template>

<script>
import Layout from "@/Pages/Layout/Layout.vue";
import TeachingMaterialCard from "@/Pages/Components/TeachingMaterialCard.vue";
import axios from 'axios';
import {Link} from "@inertiajs/vue3";
import {router} from "@inertiajs/vue3";
import {useForm} from "@inertiajs/inertia-vue3";

export default {
    name: "Index",
    components: {Layout, Link},
    props: {},
    data() {
        return {
            isSubmitting: false,
            form: useForm({
                institution: this.$page.props.user.institution,
                email: this.$page.props.user.email,
                institution_head_name: null,
                institution_head_position: null,
                coordinator_name: this.$page.props.user.name,
                coordinator_position: null,
                coordinator_phone: this.$page.props.user.tel,
                performance_name: null,
                performance_type: [],
                performance_description: null,
                performance_duration: null,
                number_of_performers: null,
                performance_directors: null,
                performers: null,
                musicians_or_narrators: null,
                number_of_musicians: null,
                opening_scene: null,
                stage_performance: null,
                ending_scene: null,
                costume_and_props: null,
                stage_lighting: null,
                sound_type: null,
                number_of_microphones: null,
                number_of_amplifiers: null,
                other_specifications: null,
                sound_control: null,
                institution_representatives: null,
                faculty_and_staff: null,
                students: null,
                vehicles: null,
                arrival_date: '2024-09-01',
                arrival_time: '10:00',
                departure_date: '2024-09-01',
                departure_time: '10:00',
                accommodation: null,
                ceremony_and_reception_details: null,
                number_of_institution_heads: null,
                number_of_faculty_and_staff: null,
                number_of_students: null
            }),
        };
    },
    mounted() {

    },
    methods: {
        async saveDraft() {
            this.isSubmitting = true;
            const url = this.route('save_draft');
            const res = await axios.post(url, this.form);

        }
    },
    watch: {},
    computed: {}
};
</script>

<style scoped>
</style>
