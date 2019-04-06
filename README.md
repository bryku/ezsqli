# ezsqli

### Example Database: items

| id | name | color |
|---|---|---|
|1|ball|red|
|2|box|blue|

### Select All

`$data = $ezsqli -> query("SELECT * FROM items") -> all;`

```
/* Output Examples

  $data = [
      0 => ["id" => 1, "name" => ball, "color" => "red"],
      1 => ["id" => 2, "name" => box, "color" => "blue"],
  ];
  
*/
```

### Select Row

`$data = $ezsqli -> query("SELECT * FROM items WHERE id='1' LIMIT 1") -> row;`

```
/* Output Examples

  $data = ["id" => 1, "name" => ball, "color" => "red"];
  
*/
```

### Select Str

`$data = $ezsqli -> query("SELECT name FROM items WHERE id='1' LIMIT 1") -> str;`

```
/* Output Examples

  $data = "ball";
  
*/
```
