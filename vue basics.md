### vue basics 



- **install vue npm**
- **create project vue** 
- **delete code template default**
- **install bootstrap in project** 
- **and add cdn in main.js file** 
- **conenct App.vue file to your-app-file.vue**
- **add code bootstrap  for ui**



## how to make loop in vue 

​      `<tr v-for="(task,index) in tasks" :key="index">`

## how to calling function in vue 

​	`@click="deleteTask(index)`



## this simple code Vue for todo app




<script>
export default {
  name: 'todoApp',
  props: {
    msg: String
  },
  data(){
    return{
      task:'',
      tasks : [
        {
          name : 'Study English',
          status : 'todo',
​    

```
    },
​        {
​          name : 'Study Django',
​          status : 'inprogress',
​        },
​        {
​          name : 'Study Vue.js',
​          status : 'todo',
​          
​        },
​        {
​          name : 'Study Python',
​          status : 'finshed',
​          
​        }
​      ]
​    }

  },
  methods:{
    submitTask(){
      if (this.task==0) return;
      this.tasks.push({
        name: this.task ,
        status: 'todo'
      })
      this.task = ''
    },

  deleteTask(index){
    this.tasks.splice(index,1)

  },

  editTask(index){
    this.task=this.tasks[index].name;

  },

  },
}
</script>
```









## connect Django Rest APIs With Vue.js 

```
import axios from "axios";

export default {

 name: 'todoApp',

 props: {

  msg: String,

 },

 data() {

  return {

   task: '',

   editedtask: null,

   tasks: []

  }

 },
 
 
 
 دا كود الربط ي حمودي 

 mounted(){              //  vue تستحدم اول م اغتح ازل صفحه ف  mouunted الداله دي عشان الداله اللي جوا ال 

  this.getTasks();

 },

 methods: {

  getTasks() {           // vue  عندي في ال  api الداله دي بقا هي اللي بتعرض البيانات اللي في 

  // Using Axios to make a GET request to the specified URL

  axios({

   method: "get",

   url: "http://127.0.0.1:8000/todo/api/",

   }).then(response =>  this.tasks = response.data['results']);

   
  },
```

   
