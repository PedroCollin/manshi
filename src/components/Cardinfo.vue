<template>
    <div id="cardinfo" :style="cssCustom">
        <section class="sectionInfo">
            <div class="card-body">
                <h5>{{text_title}}</h5>
                <p>{{text_content}}</p>
            </div>
            <div id="card_images">
                <div class="card_image" v-for="(image,index) in imgs" :key="index">
                    <img :src="image" :alt="index">
                </div>
            </div>
        </section>
    </div>
</template>

<script>
    export default{
        name: "Cardinfo",
        props: ["text_title", "text_content", "back_color", "text_color", "imgs"],
        computed: {
            cssCustom() {
                return {
                    "--mycolor": this.text_color,
                    "--myback": this.back_color,
                };
            }
        }
    }
</script>

<style scoped src="./Cardinfo.css">

</style>

