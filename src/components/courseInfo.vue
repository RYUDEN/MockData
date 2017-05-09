<template>
    <div>
        <p>{{lessons.name}}</p>
        <p>{{lessons.teacher}}</p>        
    </div> 
</template>

<script>

export default {
    computed:{
        lessons(){
            return this.$store.state.data.lessons
        }
    }
}
</script>

<style>

</style>
