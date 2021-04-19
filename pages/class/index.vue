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
            <class-item-2 :img="item.img" :title="item.title" :title2="item.title2" :nameClass="item.nameClass" :id="item.id" :homeworks="item.homeworks" :icon1="item.icon1" :icon2="item.icon2" >
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
          img: "https://www.gstatic.com/classroom/themes/SocialStudies.jpg", 
          title: "Fullstack",
          title2: "Batch III",
          nameClass: "Shift Academy",
          homeworks: [
            { id: 1, title: "Homework Frontend" },
            { id: 2, title: "Sandbox Frontend" },
          ],
          icon1: "fas fa-id-card-alt",
          icon2: "far fa-folder",
        },
        {
          id: "1512",
          img: "https://gstatic.com/classroom/themes/English.jpg",
          title: "Fullstack",
          title2: "Batch IV",
          nameClass: "Shift Academy",
          homeworks: [
            { id: 3, title: "Tugas A" },
            { id: 4, title: "Tugas B" },
          ],
          icon1: "fas fa-id-card-alt",
          icon2: "far fa-folder",
        },
      ],
    };
  },
};
</script>