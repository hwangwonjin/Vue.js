<template>
    <h4>UComponent1</h4>
    <p>
        name: {{ name }}<br/>
        age: {{ age }}<br/>
    </p>
</template>

<script>
export default {
    name:"UComponent1",
    // 상위 컴포넌트에서 속성으로 전갈하는값을 수신하기 위한 api
    props:["name", "age"],
};
</script>

<style scoped>
    
</style>