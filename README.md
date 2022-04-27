# cs103a-cpa02
.DS_Store
node_modules
*~


Things to do
- fix the interface
- one form
- fetch image
- separate pages

 <form method="post" action="/books/byTitle">
            Title: 
              <input type="text" name="title" 
                     placeholder="e.g. Batman">
            <input type="submit">
        </form>
        <form method="post" action="/books/byTitle">
            Author: 
              <input type="text" name="author" 
                     placeholder="e.g. Rowing">
            <input type="submit">
        </form>
        <form method="post" action="/books/byRating">
            Min Rating: 
            <select id="rating" name="rating">
                <% var rating=[1,2,3,4];
                for ( var i = 0; i < rating.length; i++ ){ %>
                <option><%= rating[i]%></option>
                <%}%>
                </select>
                <input type="submit">
        </form>
        <form method="post" action="/books/byPrice">
            Max Price: 
            <input type="number" name="price" 
                     placeholder="e.g. 5">
                <input type="submit">
        </form>


        <% for (book of books) {
    const title = book.title;
    const author = book.author;
    const rating = book.rating;
    const isbn = book.isbn;

%>
<div class="card text-white bg-primary mb-3" style="max-width: 18rem;">
  <div class="card-header"><%= author %></div>
  <div class="card-body">
    <h5 class="card-title"><%= title %><br><p><% rating %></p></h5>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  </div>
</div>