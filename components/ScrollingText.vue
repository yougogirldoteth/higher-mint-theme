<template>
    <div class="marquee">
      <div class="marquee__inner">
        <div class="marquee__text" v-for="n in 2" :key="n">{{ text }}</div>
      </div>
    </div>
</template>

<script setup>
const text = 'Higher is a community-run brand. Higher is an experiment. Higher is a token. Higher is yours. Higher is no one’s. Higher is striving for greatness. Higher is definite optimism. Higher is having agency. Higher is authenticity. Higher is a lifestyle.';
</script>

<style scoped>
    .marquee {
        overflow: hidden;
        white-space: nowrap;
        position: relative;
        text-transform: uppercase;
    }

    .marquee__inner {
        display: inline-block;
        animation: marquee 30s linear infinite;
    }

    .marquee__text {
        display: inline-block;
    }

    @keyframes marquee {
        0% {
        transform: translateX(0%);
        }
        100% {
        transform: translateX(-50%);
        }
    }
</style>
