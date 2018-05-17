<template>
    <div class="card col-4" style="width: 18rem;">
        <div id="image">
            <img class="rocket-image" :src="rocket.image" :alt="rocket.name">
        </div>
        <div class="card-body">
            <h5 class="card-title">{{rocket.name}}</h5>
            <p class="card-text">{{rocket.country}}</p>
            <p class="card-text">{{rocket.description}}</p>
        </div>
    </div>
</template>

<script>
export default {
    props: ['rocket']

}
</script>

<style>
#image {
    display: flex;
    justify-content: center;
}
.rocket-image {
    max-height: 400px;
    width: auto;
}

</style>
