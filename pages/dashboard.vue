<template>
  <div class="grid scroll">
    <!-- create a card using tailwind for each lesson -->
    <div v-for="lesson in lessons" v-bind:key="lesson.id" class="card">
      <div class="card-header">
        <h4>{{lesson.name}}</h4>
      </div>
      <div class="card-body">
        <p>{{lesson.description}}</p>
        <p>{{lesson.price}}</p>

      </div>
      <div class="card-image">
        <img :src="lesson.image" alt="lesson image" />
      </div>
      <div class="card-footer grid grid-flow-col max-w-[50%] max-h-[50%]">
        <div class="rounded-3xl border-y-green-900 w-16 h-16 bg-green-500 text-center justify-center flex">{{Array.from(lesson.teacher)[0]}}</div>
        <NuxtLink :to="'/lessons/' + lesson.id" class="btn btn-primary text-center justify-center align-center">View</NuxtLink>
      </div>
    </div>


  </div>


</template>

<script>



export default {
  name: "dashboard",
  components: {

  },
  data() {
    return {
      lessons: [
          /* lessons with the name of lesson, image, lesson data, price, description and whos the teacher */
          { id: 1, name: 'Lesson 1', image: 'https://i.pinimg.com/originals/5c/9f/71/5c9f71b2e196ccf71e72eb88b9f75be8.png', lessonData: '2021-05-01', price: '100', description: 'This is a lesson about the basics of the guitar', teacher: 'John Doe' },
          { id: 2, name: 'Lesson 2', image: 'https://i.pinimg.com/originals/5c/9f/71/5c9f71b2e196ccf71e72eb88b9f75be8.png', lessonData: '2021-05-01', price: '100', description: 'This is a lesson about the basics of the guitar', teacher: 'John Doe' },
          { id: 3, name: 'Lesson 3', image: 'https://i.pinimg.com/originals/5c/9f/71/5c9f71b2e196ccf71e72eb88b9f75be8.png', lessonData: '2021-05-01', price: '100', description: 'This is a lesson about the basics of the guitar', teacher: 'John Doe' },
          { id: 4, name: 'Lesson 4', image: 'https://i.pinimg.com/originals/5c/9f/71/5c9f71b2e196ccf71e72eb88b9f75be8.png', lessonData: '2021-05-01', price: '100', description: 'This is a lesson about the basics of the guitar', teacher: 'John Doe' },
      ],
    }
  },
}
</script>

<style scoped>

.card * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

img {
  width: 100%;
  height: 100%;
  max-width: 20rem;
  object-fit: cover;
}

.card {
  display: grid;
  grid-auto-columns: 1fr;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr;
  grid-template-areas:
    "card-header card-header card-image"
    "card-body card-body card-image"
    "card-footer card-footer card-image";
}
.card-header { grid-area: card-header; }
.card-body { grid-area: card-body; }
.card-footer { grid-area: card-footer; }
.card-image { grid-area: card-image; }

.scroll{
  overflow-y: scroll;
  max-height: 85vh;
  min-width: 100%;
}

/* hide scroll bar on scroll class */
.scroll::-webkit-scrollbar {
  display: none;
}

</style>
