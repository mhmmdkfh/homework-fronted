<template>
    <div>
        <div v-for="(item,i) in kelas" :key="i">
            <class-homepage :img="item.img" :title1="item.title1" :title2="item.title2"></class-homepage>
        </div>
        <div v-for="(item,i) in pengumuman" :key="i">
            <class-cardcontent :icon1="item.icon1" :pesan="item.pesan"></class-cardcontent>
        </div>
        <div v-for="(item,i) in materi" :key="i">
            <class-cardcontent1 :icon1="item.icon1" :pesan="item.pesan"></class-cardcontent1>
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
                    icon1: "/_nuxt/assets/img/avatar/profile.png",
                    pesan: "Announce something to your class",
                },
            ],
            pengumuman: [
                {
                    icon1: "/_nuxt/assets/img/avatar/profile.png",
                    pesan: "Announce something to your class",
                },
            ],
            materi: [
                {
                    icon1: "fas fa-clipboard-list",
                    pesan: "Sandbox Frontend",
                },
                {
                    icon1: "fas fa-clipboard-list",
                    pesan: "Homework Frontend",
                },
            ],
        };
    },
}
</script>
