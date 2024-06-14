html
<!DOCTYPE html>
<html>
  <head>
    <title>Listing App</title>
  </head>
  <body>
    <h1>Listing App</h1>
    <ul>
      {% for listing in listings %}
        <li>
          {{ listing.title }} - {{ listing.price }}
          <a href="{{ url_for('update', id=listing.id) }}">Edit</a>
          <a href="{{ url_for('delete', id=listing.id) }}">Delete</a>
        </li>
      {% endfor %}
    </ul>
    <a href="{{ url_for('create') }}">Create a new listing</a>
  </body>
</html>
