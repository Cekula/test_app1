Changed
<table>
  <thead>
    <tr>
      <th>Title</th>
      <th>Desctiption</th>
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
        <td><%= link_to 'Delete', article_path(article), data: {
          turbo_method: :delete,
          turbo_confirm: "Are you sure"

        } %></td>
      </tr>
    <% end %>
  </tbody>
</table>
<br>
