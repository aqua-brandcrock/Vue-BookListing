<template>
<div>
    <h1>{{ title }}</h1>
    <ul>
    <book-item v-for="book in books" :book='book'>{{book.title}}:{{book.author}}</book-item>
    </ul>
    <hr><br />
    <book-form @addBook='appendBook'></book-form>
</div>
</template>

<script>
 import BookItem from './BookItem';
 import BookForm from './BookForm';
export default {
name:'BookList',
    components: {
    BookItem,
    BookForm
    },
    data(){
    return{
        title:'All Books',
        books: [
            {title:'Self reliance',author:'Radalp'},
            
        ]
    }
  },
    methods:{
    appendBook(bookTitle,bookAuthor){
	this.books.push({title: bookTitle,author: bookAuthor})
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