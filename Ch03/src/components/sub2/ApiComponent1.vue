<template>
    <h4>data</h4>
    <p>
        name:{{ name }}<br/>
        age:{{ age }}<br/>
        addr:{{ addr }}<br/>

    </p>
</template>
<script>
export default {
    name:"ApiComponent1",
    //컴포넌트에 사용할 상태값 선언
    data(){
        return {
            name:"홍길동",
            age:23,
            addr:"부산",
        };
    },
};
</script>
<style scoped>
    
</style>
