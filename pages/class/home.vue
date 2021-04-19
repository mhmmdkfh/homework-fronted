<template>
    <div>
        <div v-for="(item,i) in kelas" :key="i">
            <class-homepage :img="item.img" :title1="item.title1"  :title2="item.title2"></class-homepage>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            kelas: [
                {
                    img: "https://www.gstatic.com/classroom/themes/SocialStudies.jpg",
                    title1: "Fullstack",
                    title2: "Batch III",
                },
            ],
        };
    },
}
</script>
