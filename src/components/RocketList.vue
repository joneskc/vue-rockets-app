<template>
    <section class="row">
        <rocket
            v-for="rocket in rockets"
            :rocket="rocket"></rocket>
    </section>
</template>

<script>
import Rocket from '@/components/Rocket'

export default {
    props: ['rockets'],
    components: {
        Rocket
    }

}
</script>

<style>

</style>
