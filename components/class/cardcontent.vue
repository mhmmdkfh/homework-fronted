<template>
    <div>
        <div class="card rounded-lg cardContent">
            <div class="row">
                <img :src="icon1" class="rounded-circle foto ml-5">
                <span class="pesan ml-3">{{pesan}}</span>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    props: {
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