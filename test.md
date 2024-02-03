<!-- STARTING POINT: A simple table that will have borders -->
<table>
  <tbody>
    <tr>
      <td>Column One</td>
      <td>Column One</td>
    </tr>
    <tr>
      <td>Content of column one</td>
      <td>Content of columnt two</td>
    </tr>
  </tbody>
</table>

<!-- EXAMPLE 1: To remove the borders, you can add a style tag to the above example -->
<!-- Note the "!important" which ensures this style overrides other styles on the page! -->
<style>
  table td {
    border: none !important;
  }
</style>
<table>
  <tbody>
    <tr>
      <td>Column One</td>
      <td>Column One</td>
    </tr>
    <tr>
      <td>Content of column one</td>
      <td>Content of column two</td>
    </tr>
  </tbody>
</table>

<!-- EXAMPLE 2: Using a table id (BEST OPTION) -->
<!-- The above will have the disadvantage of affecting every single table on the page, to avoid that
     we can add an id to the table, this will also allow as to not use "!important" by increasing what's
     called the specificity of our style -->
<style>
  table#example-table td {
    border: none;
  }
</style>
<table id="example-table">
  <tbody>
    <tr>
      <td>Column One</td>
      <td>Column One</td>
    </tr>
    <tr>
      <td>Content of column one</td>
      <td>Content of column two</td>
    </tr>
  </tbody>
</table>

<!-- EXAMPLE 3 Adjusting the style of each cell separately -->
<!-- This is perhaps the simplest of the approaches - it doesn't require a separate style tag, but it does require
    adjusting the style of every cell separately -->
<table>
  <tbody>
    <tr>
      <td style="border: none">Column One</td>
      <td style="border: none">Column One</td>
    </tr>
    <tr>
      <td style="border: none">Content of column one</td>
      <td style="border: none">Content of column two</td>
    </tr>
  </tbody>
</table>
