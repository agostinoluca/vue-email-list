<script>
export default {
    name: 'LoadMail',
};
</script>
  
<template>
    <div class="loader">
        <div class="loader-icon"></div>
        <div class="loader-text">Loading...</div>
    </div>
</template>
  
  
<style scoped>
.loader {
    margin-top: 10rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.loader-text {
    margin-top: 1rem;
    font-size: 1.5rem;
}

.loader-icon {
    width: 3rem;
    aspect-ratio: 1;
    background-color: rgb(255, 0, 0);
    border-radius: 50%;
    animation: charge 1s linear infinite;
}

@keyframes charge {
    0% {
        border-left: 3px solid black;
    }

    25% {
        border-top: 3px solid black;
    }

    50% {
        border-bottom: 3px solid black;
        background-color: rgb(251, 255, 0);
    }

    75% {
        border-right: 3px solid black;
    }

    100% {
        background-color: rgb(0, 255, 0);

    }
}
</style>
  