<template>
  <div>
    <test 
    :question="question1" 
    :name='name' 
    @saveAnswer="saveAnswer" 
    @setData='setData'/>
  </div>
</template>

<script>
import test from "@/components/Test";

export default {
  name: null,
  components: {
    test
  },
  data() {
    return {
      name: null,
      question1: null
    };
  },
  methods: {
    saveAnswer(answer) {
      console.log(answer);
      this.question1 = answer;
    },
    setData(key,value){
        this[key]=value
    }
  }
};
</script>
