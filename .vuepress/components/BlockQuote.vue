<template>
<blockquote :cite="citeUrl">
    <slot></slot>
    <cite>{{ citeLabel }}</cite>
</blockquote>
</template>

<script>
export default {
    props: {
        citeUrl: String,
        citeLabel: String,
    }
}
</script>
