# README
First Test repo on the Complete Ruby on Rails Developer course by Tom Solis 
 
<div class ="container" id="home-container">
  <div class="jumbotron text-center text-white">
    <h1 class="display-4">Alpha Blog</h1>
    <p class="lead">This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured content or information.</p>
    <hr class="my-4">
    <p>It uses utility classes for typography and spacing to space content out within the larger container.</p>
    <a class="btn btn-success btn-lg" href="#" role="button">Sign up!</a>
  </div>
</div>

<table>
  <thead>
    <tr>
      <th>Title</th>
      <th>Description</th>
      <th colspan="3">Actions</th>
    </tr>
  </thead>

  <tbody>
  <% @articles.each do |article| %>
    <tr>
        <td><%= article.title %></td>
        <td><%= article.description %></td>
        <td><%= link_to 'Show', article_path(article) %></td>
        <td><%= link_to 'Edit', edit_article_path(article) %></td>
        <td><%= link_to 'Delete', article_path(article), method: :delete, data: { confirm: "Are you sure?" } %></td>    
    </tr>
    <% end %>
  </tbody>
</table>

<p>
  <%= link_to 'Create new article', new_article_path %>
</p>