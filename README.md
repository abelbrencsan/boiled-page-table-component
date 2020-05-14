# Boiled Page table component

Table SCSS component for Boiled Page frontend framework. It is intended to create tables.

## Install

Place `_table.scss` file to `/assets/css/components` directory, and add its path to components block in `assets/css/app.scss` file.

## Usage

### Table component

Table component is intended to create tables.

#### Classes

Class name | Description | Example
---------- | ----------- | -------
`table` | Applies a table. | `<table class="table"></table>`

#### Examples

##### Example 1

The following example shows a table.

```html
<table class="table">
  <thead>
    <tr>
      <th>Name</th>
      <th>Author</th>
      <th>ISBN</th>
      <th>Condition</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Animal Farm</td>
      <td>George Orwell</td>
      <td>0452277507</td>
      <td>Very Good</td>
      <td>$5.69</td>
    </tr>
    <tr>
      <td>Of Mice and Men</td>
      <td>John Steinbeck</td>
      <td>0141038424</td>
      <td>Like New</td>
      <td>$8.59</td>
    </tr>
    <tr>
      <td>Goodnight Moon</td>
      <td>Margaret Wise Brown</td>
      <td>0064430170</td>
      <td>Very Good</td>
      <td>$4.69</td>
    </tr>
    <tr>
      <td>Green Eggs and Ham</td>
      <td>Dr. Seuss</td>
      <td>0394892208</td>
      <td>Good</td>
      <td>$6.79</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="4">Price total</td>
      <td>$25.76</td>
    </tr>
  </tfoot>
</table>
```

#### Extension ideas

##### Special table

```scss
/* Table component extensions */
table.table {

  // Special table
  &.table--special {

    td, th {
      border-left: 0;
      border-right: 0;
    }

    thead th {
      border-top: 0;
    }

    tfoot td {
      border-bottom: 0;
    }
  }
}
```

##### Striped table

```scss
/* Table component extensions */
table.table {

  // Striped table
  &.table--striped {

    tbody tr:nth-of-type(odd) {
      background: $border-bg-color;
    }
  }
}
```

### Table wrapper component

Table wrapper component is intended to make tables responsive.

#### Classes

Class name | Description | Example
---------- | ----------- | -------
`table-wrapper` | Applies a table wrapper. | `<div class="table-wrapper"></div>`

#### Examples

##### Example 1

The following example shows a table.

```html
<div class="table-wrapper">
  <table class="table">
    <thead>
      <tr>
        <th>Name</th>
        <th>Author</th>
        <th>ISBN</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Animal Farm</td>
        <td>George Orwell</td>
        <td>0452277507</td>
      </tr>
      <tr>
        <td>Of Mice and Men</td>
        <td>John Steinbeck</td>
        <td>0141038424</td>
      </tr>
    </tbody>
  </table>
</div>
```