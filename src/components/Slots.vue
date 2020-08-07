<template>
<div class="my-child-component">
<slot> //defaultslot
<h1>
When no slot is specified in the parent, this fallback text will appear.
</h1>
</slot>
<header>
<slot name="header" />
</header>
<main>
<img src="" />
<slot />
<AuthorComponent />
</main>
<footer>
<slot name="footer" />
</footer>
</div>
</template>

<script>
export default {
  name: 'Slots'
}
</script>
