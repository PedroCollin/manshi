<template>
    <div id="cardinfo" :style="cssCustom">
        <section class="sectionInfo">
            <div class="card-body">
                <h5>{{text_title}}</h5>
                <p>{{text_content}}</p>
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

