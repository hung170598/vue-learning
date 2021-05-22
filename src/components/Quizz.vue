<template>
  <div id="Quizz">
    <div class="question-box">
      <h1>Bài Tập</h1>
      <div v-show="sumQuestion < questions.length" class="question">{{ questions[curentQuestion].question }}</div>
      <button
        v-bind:class="{
          answer_true: isAnswer & i.isTrue,
          answer: (!isAnswer || !i.isTrue) & !i.isChoose,
          answer_false: i.isChoose & !i.isTrue,
        }"
        v-show="sumQuestion < questions.length"
        v-for="i in questions[curentQuestion].answers"
        :key="i"
        @click="
          if (!isAnswer) {
            isAnswer = true;
            i.isChoose = true;
            if (i.isTrue) score++;
            sumQuestion++;
          }
        "
      >
        {{ i.answer }}
      </button>
      <p v-show="sumQuestion >= questions.length">
        Ban tra loi dung {{ score }}/{{sumQuestion}} cau
      </p>
      <button
        class="btn"
        @click="
          curentQuestion++;
          isAnswer = false;
        "
      >
        Next
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Quizz",
  data() {
    return {
      curentQuestion: 0,
      isAnswer: false,
      score: 0,
      sumQuestion: 0,
      questions: [
        {
          question: "Cau hoi 1: Cau hoi 1",
          answers: [
            {
              answer: "Cau tra loi 1 1",
              isTrue: true,
            },
            {
              answer: "Cau tra loi 1 2",
            },
            {
              answer: "Cau tra loi 1 3",
            },
          ],
        },
        {
          question: "Cau hoi 2: Cau hoi 1",
          answers: [
            {
              answer: "Cau tra loi 2 1",
              isTrue: true,
            },
            {
              answer: "Cau tra loi 2 2",
            },
            {
              answer: "Cau tra loi 2 3",
            },
            {
              answer: "Cau tra loi 2 4",
            },
          ],
        },
        {
          question: "Cau hoi 3: Cau hoi 1",
          answers: [
            {
              answer: "Cau tra loi 1 1",
              isTrue: true,
            },
            {
              answer: "Cau tra loi 1 2",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style>
#Quizz {
  margin-top: 160px;
  width: 100%;
  display: flex;
  justify-content: center;
  position: fixed;
}
.question-box {
  text-align: center;
  width: 500px;
  border: 2px solid black;
  background-color: gainsboro;
  border-radius: 10px;
  padding-bottom: 100px;
}
.question-box h1 {
  color: green;
  font: 20pt;
}
.question {
  background-color: green;
  color: white;
  width: 98%;
  margin: 20px 1%;
  font: 20pt black;
  font-weight: bold;
  border-radius: 10px;
}
.answer {
  background-color: white;
  width: 98%;
  margin: 20px 1%;
  font: 20pt black;
  font-weight: bold;
  border-radius: 10px;
}
.btn {
  background-color: aqua;
  height: 50px;
  width: 80px;
}
.answer_true {
  background-color: blue;
  color: aliceblue;
  width: 98%;
  margin: 20px 1%;
  font: 20pt black;
  font-weight: bold;
  border-radius: 10px;
}
.answer_false {
  background-color: red;
  color: aliceblue;
  width: 98%;
  margin: 20px 1%;
  font: 20pt black;
  font-weight: bold;
  border-radius: 10px;
}
</style>