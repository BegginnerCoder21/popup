<template>
    <Transition name="pop" appear :duration="900">
        <div class="Bouton">
            <div class="BoutonPop">
                <h3>Bouton popups</h3>
                <span>
                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Reprehenderit iure sapiente necessitatibus consectetur aliquam laudantium pariatur nihil culpa dolor autem aperiam repudiandae, porro quae dolores similique unde adipisci magni molestias.
                </span>
                <slot />
            </div>
        </div>
    </Transition>
</template>

<script setup lang="ts">

</script>

<style scoped>
.Bouton{
    position: fixed;
    z-index: 99;
    top: 0%;
    bottom: 0%;
    left: 0%;
    right: 0%;
    background-color: rgba(0, 0, 0, 0.1);
    display: flex;
    justify-content: center;
    align-items: center;
}

.BoutonPop{
    background-color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    max-width: 550px;
    text-align: center;
    margin: auto;
    padding: 50px 10px;
    border-radius: 10px;
}
.pop-leave-active,
.pop-enter-active{
    transition: .4s ease all;
}

.pop-enter-from,
.pop-leave-to{
    opacity: 0;
    transform: scale(0.3);
}


</style>