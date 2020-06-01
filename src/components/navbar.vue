<template>
    <nav class="navbar navbar-expand-sm bg-dark navbar-dark">
        <a class="navbar-brand mr-auto" v-on:click="$emit('click-home')">Kruemel's Page</a>
        <ul class="navbar-nav ml-auto">
            <li class="nav-item active">
                <a class="nav-link" v-on:click="$emit('click-tutorial')" >Anleitungen</a>
            </li>
            <li class="nav-item active">
                <a class="nav-link" v-on:click="$emit('click-blog')">Blog</a>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
  name: 'navbar',


  
}
</script>


<style>

</style>
