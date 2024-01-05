
<script>
    let hereKitty = true;
    const handleMouseenter = () => (hereKitty = true);
    const handleMouseleave = () => (hereKitty = false)
    let text = `here.kitty = true  here.kitty = false`;
 

</script>

<svelte:body on:mouseenter={handleMouseenter} on:mouseleave={handleMouseleave} />

<img
    class:curious={hereKitty}
    alt="Kitten wants to know what's going on?"
    src="https://pub-c1de1cb456e74d6bbbee111ba9e6c757.r2.dev/cat.png"
/>

<style>
    img {
        position: absolute;
        left: 0;
        bottom: -60px;
        transform: translate(-80%, 0) rotate(-30deg);
        transform-origin: 100% 100%;
        transition: transform 0.4s;
    }

    .curious {
        transform: translate(-15%, 0) rotate(0deg);
    }

    :global(body) {
        overflow: hidden;
    }
</style>


    <textarea bind:value={text} />
