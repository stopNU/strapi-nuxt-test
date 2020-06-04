<template>
    <div class="btn">
        <a :href="`${url}`" :target="openInTab ? '_blank' : ''"><slot></slot></a>
    </div>
</template>

<script>
export default {
    props:{
        url: String,
        openInTab: Boolean
    },
}
</script>

<style scoped lang="scss">

</style>
