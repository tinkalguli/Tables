# Organizing Data With Tables

HTML tables were introduced to structure the data in a more digestible way.Many times there are some data that must be displayed in a form that is easy for users to read and digest. For example food ingredients, shopping items with price marks obtained in different subjects, etc. For such kind of data, the HTML table provides a straightforward way to structure the data in tabular form.

## Creating Tables

To introduce a table on a page <table> element is defined. The <table> element represents the data in tabular form that is contained within rows and columns.

```
<table>
  ...
</table>
```

## Table Row

After adding ```<table>``` element we can put table row ```<tr>``` element inside ```<table>``` element. Now we can add table data ```<td>``` element inside the ```<tr>``` element . The ```<td>``` element or the table data will come in a row and create several columns.

```
<table>
  <tr>
    <td>Laptop</td>
    <td>Apple</td>
    <td>₹ 68,999</td>
  </tr>
  <tr>
    <td>Mouse</td>
    <td>Apple</td>
    <td>₹ 5,973</td>
  </tr>
  <tr>
    <td>Keyboard</td>
    <td>Apple</td>
    <td>₹ 8,900</td>
  </tr>
</table>
```

## Table Header

Table header ```<th>``` is similar with ```<td>``` element . Only difference is ```<td>``` elements creates data and ```<th>``` element creates heading.

```
<table>
  <tr>
    <th>Accesories</th>
    <th>Brand</th>
    <th>Price in ₹</th>
  </tr>
  <tr>
    <td>Laptop</td>
    <td>Apple</td>
    <td>₹ 68,999</td>
  </tr>
  <tr>
    <td>Mouse</td>
    <td>HP</td>
    <td>₹ 1,399</td>
  </tr>
  <tr>
    <td>Keyboard</td>
    <td>Apple</td>
    <td>₹ 8,900</td>
  </tr>
</table>
```

The ```<th>``` element comes with an attribute which is ```scope```. The ```scope``` attribute accepts four values i.e. ```col```, ```row```, ```colgroup``` and ```rowgroup```. The most commonly used values are col and row. The col value indicates that every cell within the column relates directly to that table header, and the row value indicates that every cell within the row relates directly to that table header. This attribute wouldn't change anything but it is recommended to use the scope attribute that helps screen readers and other technologies. Additionally, in most of the browsers, the table header is center aligned that can be reset using CSS.

### The col value

```
<table>
  <tr>
    <th scope="col">Accesories</th>
    <th scope="col">Brand</th>
    <th scope="col">Price in ₹</th>
  </tr>
  <tr>
    <td>Laptop</td>
    <td>Apple</td>
    <td>₹ 68,999</td>
  </tr>
  <tr>
    <td>Mouse</td>
    <td>HP</td>
    <td>₹ 1,399</td>
  </tr>
  <tr>
    <td>Keyboard</td>
    <td>Apple</td>
    <td>₹ 8,900</td>
  </tr>
</table>
```

### Col and Row Value

```
<table>
  <tr>
    <th scope="col">Name</th>
    <th scope="col">Phone</th>
    <th scope="col">City</th>
  </tr>
  <tr>
    <th scope="row">Joel Garner</th>
    <td>412-212-5421</td>
    <td>Pittsburgh</td>
  </tr>
  <tr>
    <th scope="row">Clive Lloyd</th>
    <td>410-306-1420</td>
    <td>Baltimore</td>
  </tr>
  <tr>
    <th scope="row">Gordon Greenidge</th>
    <td>281-564-6720</td>
    <td>Houston</td>
  </tr>
</table>
```

## Organizing Data and Table Structure

To organize a table in a better way we use some other elements ```<caption>```, ```<thead>```, ```<tbody>``` and ```<tfoot>```.

### Table Caption

The table caption ```<caption>``` element provides caption or title to a table . The caption of the table helps the user to identify what kind of data the table is containing.

```
<table>
  <caption>
    Pricing list of computer accessories
  </caption>
  ...
</table>
```

### Table Head

The table head, ```<thead>``` element wraps heading row of the table which consists of ```<th>``` elements. The thead element comes after the ```<caption>``` element.

```
<table>
  <caption>
    List of computer accessories bought
  </caption>
  <thead>
    <tr>
      <th scope="col">Items</th>
      <th scope="col">Brand</th>
      <th scope="col">Price in ₹</th>
    </tr>
  </thead>
```

### Table Body

After the ```<thead>``` element ```<tbody>``` comes which contains all the generic data of the table.

```
<table>
  <caption>
    List of computer accessories bought
  </caption>
  <thead>
    <tr>
      <th scope="col">Items</th>
      <th scope="col">Brand</th>
      <th scope="col">Price in ₹</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Laptop</td>
      <td>Apple</td>
      <td>₹ 68,999</td>
    </tr>
    <tr>
      <td>Mouse</td>
      <td>HP</td>
      <td>₹ 1,399</td>
    </tr>
    <tr>
      <td>Keyboard</td>
      <td>Apple</td>
      <td>₹ 8,900</td>
    </tr>
  </tbody>
```

### Table Foot

The `<tfoot>` may contain the data that show the overall result of the table.

```
<table>
  <caption>
    List of computer accessories bought
  </caption>
  <thead>
    <tr>
      <th scope="col">Items</th>
      <th scope="col">Brand</th>
      <th scope="col">Price in ₹</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Laptop</td>
      <td>Apple</td>
      <td>₹ 68,999</td>
    </tr>
    <tr>
      <td>Mouse</td>
      <td>HP</td>
      <td>₹ 1,399</td>
    </tr>
    <tr>
      <td>Keyboard</td>
      <td>Apple</td>
      <td>₹ 8,900</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Subtotal</td>
      <td></td>
      <td>₹ 79,298</td>
    </tr>
    <tr>
      <td>Tax</td>
      <td></td>
      <td>₹ 899</td>
    </tr>
    <tr>
      <td>Total</td>
      <td></td>
      <td>₹ 80, 197</td>
    </tr>
  </tfoot>
</table>
```

## Combining Multiple Cells

Sometimes we may need to combine two or more cell in a table in such a case two attribute comes handy i.e. `colspan` and `rowspan`. This two attribute accepts any natural number i.e. how many columns or rows we want to combine. The colspan will span the single cell across multiple columns and rowspan will span the single-cell across the multiple rows.

```
<table>
  <caption>
    List of computer accessories bought
  </caption>
  <thead>
    <tr>
      <th scope="col">Items</th>
      <th scope="col">Brand</th>
      <th scope="col">Price in ₹</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Laptop</td>
      <td>Apple</td>
      <td>₹ 68,999</td>
    </tr>
    <tr>
      <td>Mouse</td>
      <td>HP</td>
      <td>₹ 1,399</td>
    </tr>
    <tr>
      <td>Keyboard</td>
      <td>Apple</td>
      <td>₹ 8,900</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="2">Subtotal</td>
      <td>₹ 79,298</td>
    </tr>
    <tr>
      <td colspan="2">Tax</td>
      <td>₹ 899</td>
    </tr>
    <tr>
      <td colspan="2">Total</td>
      <td>₹ 80, 197</td>
    </tr>
  </tfoot>
</table>
```

## Table Borders

We can give border to each cell in the table or in the table itself. Borders around cells or tables have a large impact that helps the user to interpret the data more clearly. When working with table borders two properties come in handy: border-collapse, and border-spacing.

### Border Collapse Property

When we give border to the cells borders sits next to each other . If we give 1px border then we will get 2px border around each cell except the edges. To solve this problem we have `border-collapse` property which is applied to the `<table>` element . This property accepts three values i.e. `collapse`, `separate` and `inherit`. By default `separate` is the value means the border will stack up. However, the model can be changed using the `collapse` value. The `collapse` value will condense the border into one.

```
table {
  border-collapse: collapse;
}
th,
td {
  border: 2px solid #272727;
  padding: 8px 16px;
}
```

### Border Spacing

We have another property which separate the border by some space , the space is define by length units . This property accepts one value and two value also . If we assign one value than it will give same space horizontally and vertically but if we assign two value then first  value will be for horizontal spacing and second value will be for vertical space .

> With one value

```
table {
  border-collapse: separate;
  border-spacing: 4px;
}
table,
th,
td {
  border: 2px solid #272727;
  padding: 8px 16px;
}
```

> With two values

```
table {
  border-collapse: separate;
  border-spacing: 4px 8px;
}
table,
th,
td {
  border: 2px solid #272727;
  padding: 8px 16px;
}
```

### Adding Borders to Rows

We can't assign border to table rows `<tr>` because `<tr>` element does not take border property. There is one technique we can do i.e. we can add `border-bottom` to the `<td>` elements with `border-collapse` property to `collapse` value.

```
table {
  border-collapse: collapse;
}
th,
td {
  border-bottom: 1px solid #cecfd5;
  padding: 10px 15px;
}
```

### Table Striping

One of the most popular styles when designing a table is to stripe its rows with alternate background colors. This makes the data inside the table more legible and helps users to interpret the data more clearly. To do this style we can use class to the alternate rows or we can use `:nth-child()` pseudo-class with `odd` or `even` argument .

```
table {
  border-collapse: collapse;
}
th,
td {
  padding: 8px 16px;
}
thead {
  background: #bada55;
  color: #fff;
}
tbody tr:nth-child(even) {
  background: #f0f0f2;
}
td {
  border-bottom: 1px solid #272727;
  border-right: 1px solid #272727;
}
td:first-child {
  border-left: 1px solid #272727;
}
```
