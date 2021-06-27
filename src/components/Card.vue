<template>
    <div class="card" style="width: 18rem;">
        <img
            class="card-img-top"
            src="https://i4.hurimg.com/i/hurriyet/75/0x0/60c862244e3fe119909a689a.jpg"
            alt="Card image cap"
            />
            <div class="card-body">
            <h5 class="card-title">Galatasaray</h5>
            <p class="card-text">
                "To play in a collective way like the English, to signify a certain color and name and defeat non-Turkish teams."
                Ali Sami Yen
            </p>
            <a href="https://www.galatasaray.org/anasayfa" class="btn btn-primary">Go to GS Website</a>
            <p>Kullanıcı Adı : {{ name }}</p>
            <button @click="sendToParent">Veriyi Parent'a gönder</button>
        </div>
    </div>
</template>
<script>
    export default{
        // props: ["name",],
        // props: {
        //     name : [String, Array]
        // },
        props: {
            name : {
                type : String,
                required: true,
                default: "omurbozdag",
            }
        },
        data(){
            return{
                childData: "",
            }
        },
        methods: {
            sendToParent(){
                this.$emit("data", "kablosuzkedi");
            }
        }
    }
</script>
