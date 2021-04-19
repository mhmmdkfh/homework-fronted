<template>
    <div>
        <div>
            <div>
                <center>
                    <img :src="img" class="card-img-top mt-3 rounded-lg " style="height: 230px; width: 90%;" alt="...">
                </center>
            </div>
            <div class="card-img-overlay ">
                <h2 class="card-title titleKelas mt-4">{{title1}}</h2>
                <h5 class="card-title titleKelas">{{title2}}</h5>
            </div>
        </div>
    </div>
</template>

<script>
import Cardcontent from './cardcontent.vue';
export default {
    props: {
        img: {
            type: String,
            default: "",
        },
        title1: {
            type: String,
            default: "",
        },
        title2: {
            type: String,
            default: "",
        },
        icon1: {
            type: String,
            default: "",
        },
        pesan: {
            type: String,
            default: "",
        }
    },
};
</script>