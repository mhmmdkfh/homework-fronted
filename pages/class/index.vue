<template>
    <div>
        <span>
            <span class="fas fa-tasks itemContentImg"></span>
            <a href="" class="itemContent">To-Do List</a>
        </span>
        <span>
            <span class="far fa-calendar itemContentImg"></span>
            <a href="" class="itemContent">Calendar</a>
        </span>
        <div class="row">
          <div class="col-md-4" v-for="(item,i) in listClass" :key="i">
            <class-item-2 :title="item.title" :id="item.id" :homeworks="item.homeworks">
            </class-item-2>
          </div>
        </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      listClass: [
        {
          id: "X122",
          title: "Fullstack 1",
          homeworks: [
            { id: 1, title: "Tugas A" },
            { id: 2, title: "Tugas B" },
          ],
        },
        {
          id: "1512",
          title: "Fullstack 2",
          homeworks: [],
        },
        {
          id: "61712",
          title: "Fullstack 3",
          homeworks: [],
        },
        {
          id: "y6127",
          title: "Fullstack 4",
          homeworks: [
            { id: 3, title: "Tugas A" },
            { id: 4, title: "Tugas B" },
          ],
        },
      ],
    };
  },
};
</script>