## Google Sheet extract to JSON example

```js
var app = SpreadsheetApp
function doGet(e) {
  var ss = app.openByUrl("url");
  var sheet = ss.getSheetByName("시트");

  return getStudents(sheet);
}

function getStudents(sheet){
  var obj = {};
  var dataArr = [];

  var rows = sheet.getRange(2,1, sheet.getLastRow()-1, sheet.getLastColumn()).getValues();

  for(var i = 0; i<rows.length; i++) {
    var dataRow = rows[i];
    var table = {};

    table['key1'] = dataRow[0].toLowerCase();
    table['key2'] = dataRow[1];
    table['key3'] = String(dataRow[2]);

    dataArr.push(table);
  }

  obj = dataArr;

  return console.log(obj);
}
```

- 데이터 양이 많으면 못뽑아오니 나눠야함
