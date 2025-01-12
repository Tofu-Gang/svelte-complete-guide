<script>
    export let size = "small";
    export let shadow = false;
    export let bgColor = "inherit";
    export let textColor = "inherit";
</script>

<button style:--buttonBgColor={bgColor}
        style:--buttonTextColor={textColor}
        class:size-lg={size === "large"}
        class:size-sm={size === "small"}
        class:shadow>
    <slot>Default Text</slot>
</button>

<style lang="scss">
    button {
        background-color: var(--buttonBgColor);
        color: var(--buttonTextColor);
        border: none;
        padding: 15px 20px;
        font-weight: bold;
        border-radius: 5px;
        cursor: pointer;
        &:hover {
          background-image: linear-gradient(rgb(0 0 0/40%) 0 0);
        }
        &:active {
            background-image: linear-gradient(rgb(255 255 255/40%) 0 0);
        }
        &.size-sm {
            padding: 15px 20px;
        }
        &.size-lg {
            padding: 20px 25px;
            font-size: 20px;
        }
        &.shadow {
          box-shadow: 0 0 10px rgba(1, 1, 1, 0.3);
        }
    }
</style>
