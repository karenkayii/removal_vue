<template>
    <h1></h1>
    <h2>{{ capitalize ("hello from greeting component")}}</h2>
    <h2>Hello {{ name }}</h2>
</template>

<script>
import { capitalize } from '../util';
  export default{
    props:{
        name: {
            type:String,
            required : true
        }
    },
    methods:{
        capitalize
    }
}
</script>


