<template>
    <h4>Basic Usage</h4>
    <p>
        message : {{ message }}
        <button @click="changeMessage">수정</button>    
    </p>
    <p>
        count : {{ count }}
        <button @click="btnCountUp">증가</button>    
    </p>
    <p>
        name : {{ user.name }} / age : {{ user.age }}<br/>

        <button @click="changeUser">수정</button>    
    </p>
</template>
<script>
export default {
    name:"Component1",
    // 기존 Option 
    setup(){
        // 변수 생성(반응성 없음)
        let message = "Hello";
        let count = 0;
        let user = {
            name: "홍길동",
            age: 23,
        };

        // 함수 정의
        function changeMessage(){
            console.log("changeMessage");
            // 변수가 반응성이 없기 때문에 상태값 갱신 안됨
            message = "Welcome";
        }

        const btnCountUp = function(){
            console.log("btnCountUp....." + count);
            count++;
        };

        const changeUser = () => {
            user.name = "김유신",
            user.age = 25;
        };

        return {
            message,
            count,
            user,
            changeMessage,
            btnCountUp,
            changeUser,
        };
    },
};
</script>
<style scoped>
    
</style>