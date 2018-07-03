<template>
<div>
    <h1>{{ title }}</h1>
    <ul>
    <book-item v-for="book in books" :book='book'>{{book.title}}:{{book.author}}</book-item>

    </ul>
</div>
</template>

<script>
 import BookItem from './BookItem';
export default {
name:'BookList',
    components: {
    BookItem
    },
    data(){
    return{
        title:'All Books',
        books: [
            {title:'Self reliance',author:'Radalp'},
            {title:'American Gods',author:'Simson'},
            {title:'Titanic',author:'Jack Smith'},
        ]
    }
  }
}
</script>
<style>
h1,h2{
 font-weight:normal;
}
ul{
    list-style-type: none;
    padding: 0;
}
li{
  display: block;
  margin: 0 10px;
}
</style>