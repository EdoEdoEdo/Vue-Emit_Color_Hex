<template>
<button @click="pickColor" v-bind:style={color:hex}>
    {{label}}
</button>
</template>

<script>
export default {

    props:["hex","label"],

    data: function() {
        return {
            // text: this.hex
            //text: "Click"
        }
    },

    methods:{
        pickColor: function(){
            var colorHex = this.hex;
            this.$emit("BUTTON_CLICK", colorHex);
        }
    }
}

</script>