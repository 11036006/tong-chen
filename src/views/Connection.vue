<template>
   

    <iframe :src="src"  :style="frameStyle"></iframe>
</template>

<script>
export default {
    data(){
        return{
            frameStyle:{
                width:"100%",
                height:"300px"
            },
              src:"http://localhost:8080/public/GoogleMap/index.html",
        }
    }
}
</script>