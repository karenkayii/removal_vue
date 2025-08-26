<!--NODE AND VITE
to check node type : node -v
to check node type : npm -v
-->
<template>
    <div id="app">
        <Greeting name="Elyn"/>
        <Student />
    </div>
</template>

<script>
import Greeting from "./components/Greeting.vue"
import Students from "./components/Students.vue"
export default {
    components: {Greeting, Students}
}
</script>

