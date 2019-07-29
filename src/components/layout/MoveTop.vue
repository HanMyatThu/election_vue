<template>
    <div>
        <button class="move_to_top"  @click="scrollToTop">
            <i class="fas fa-arrow-alt-circle-up"></i>
        </button>
    </div>
</template>

<script>
export default {
    name: "MoveTop",
    methods: {
        scrollToTop() {
                window.scroll({
                    top: 0,
                    left: 0,
                    behavior: "smooth"
                });
           }
    }
}
</script>
