<template>
    <section>
        <nav-bar />
        <new-rocket-form
            :addRocket="addRocket"
            class="container"/>
        <rocket-list :rockets="rockets"/>
    </section>
</template>

<script>
import NewRocketForm from '@/components/NewRocketForm'
import NavBar from '@/components/NavBar'
import API from '@/lib/API'
import RocketList from '@/components/RocketList'

export default {
    name: 'rockets',
    components: {
        NewRocketForm,
        NavBar,
        RocketList
    },
    data () {
        return {
            rockets: [],
        }
    },
    async mounted() {
        this.rockets = await API.getRockets()
    },
    mathods: {
        addRocket(rocket) {
            this.rockets.push(rocket)
        }
    }

}
</script>

<style>

</style>
