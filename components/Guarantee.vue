<template>
    <section class="max-w-7xl m-auto mt-24 md:mt-32">
        <div class="w-[90%] flex flex-col md:flex-row items-center justify-around mx-auto bg-[#E9F2FF] rounded-[20px]">
            <div class="w-full md:w-3/5 flex flex-col items-center md:items-start gap-4 text-center md:text-left p-4">
                <h1 class="text-[#111827] text-[1rem] md:text-[1/75rem] tracking-[-0.56px] font-semibold leading-[1rem] md:leading-[2.25rem]">We guarantee the high quality of your product.</h1>
                <p class="text-[#374151] text-[1rem] leading-4">Our integrated solutions ensure your product meets the highest standards of quality, and we stand behind our work with a guarantee of satisfaction.</p>
                <button class="bg-[#267DFF] text-white px-4 py-2 rounded-lg">Talk to sales</button>
            </div>
            <div class="md:w-[35%] bg-white rounded-[15px] h-full">
                <!-- <img src="~/assets/images/form.png" alt="guarantee" /> -->
                <form @submit.prevent="submitForm" class="flex flex-col p-4 space-y-6">
                    <div class="flex flex-col gap-2">
                        <label for="headline">Headline:</label>
                        <input type="text" id="headline" v-model="form.headline" placeholder="Your Company" class="border rounded-xl px-2 focus:outline-none" />
                        <p class="-mt-2 text-[0.7rem]">e.g Senior QA Engineer proficient in Selenium</p>
                    </div>
                    <div class="flex flex-col gap-2">
                        <label for="proficiency">Proficiency:</label>
                        <select id="proficiency" v-model="form.proficiency" class="border rounded-xl px-2 focus:outline-none">
                            <option value="">Select...</option>
                            <option value="beginner">Beginner</option>
                            <option value="intermediate">Intermediate</option>
                            <option value="advanced">Advanced</option>
                        </select>
                    </div>
                    <div class="flex flex-col gap-2">
                        <label for="skills">Skills:</label>
                        <input type="text" id="skills" v-model="form.skills" placeholder="Search skills" class="border rounded-xl px-2 focus:outline-none"/>
                        <p class="-mt-2 text-[0.7rem]">Popular skills for QA Engineers</p>
                    </div>
                </form>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            form: {
                headline: '',
                proficiency: '',
                skills: '',
            },
        };
    },
    methods: {
        submitForm() {
            console.log(this.form);
        },
    },
};
</script>