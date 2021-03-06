# DOMCreateElement

## Intro

運用於前端建立DOM物件使用，啟發自學長並加入一些個人的改變

在遇到如table等巢狀DOM物件時十分實用

## example

```javascript
// single object

// <div></div>
let dom = createElement("div");

// <div class="row"></div>
let dom = createElement("div",{
    "className":"row"
});
```

```javascript

//nested object

//<table>
//      <tr></tr>
//      <tr></tr>
//</table>
let table = createElement("table",{},{
    "objChildren":[
        {
            "childNodeTag":"tr",
            "anchor":{}
        },
        {
            "childNodeTag":"tr",
            "anchor":{}
        }
    ]
});

//<tr>
//      <th> hello </th>
//      <th> world </th>
//</tr>

let row = createElement("tr",{},{
    "objChildren":[
        {
            "childNodeTag":"th",
            "anchor":{
                "innerText":"hello"
            }
        },
        {
            "childNodeTag":"th",
            "anchor":{
                "innerText":"world"
            }
        }
    ]
});
```
