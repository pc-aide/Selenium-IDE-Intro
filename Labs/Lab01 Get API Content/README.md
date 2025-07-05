# Lab01 Get API Content

---

## https://gist.github.com/
1. Git description : ``
2. content :
````json
{
  "code": "123456"
}
````
3. click : `Create secret gist`
4. Test : `https://gist.githubusercontent.com/pc-aide/2632373556e1af5e374ac468f91edcab/raw/943020c548b53cb3f27bd819840ee72e135b521b/gistfile1.txt`

<img src="https://i.imgur.com/vlRtYwk.png">

---

## https://jsonplaceholder.typicode.com/posts/1
````json
{
  "userId": 1,
  "id": 1,
  "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
  "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
}
````

---

## v0.01
|n|Command|Target|Value|Description|Log|
|-|-------|------|-----|-----------|---|
|1|`execute script`|`window.jsonResult = "";`||Clear jsonResult|
|2|`execute async script`|`(async () => {   const callback = arguments[0];   try {     const response = await fetch('https://jsonplaceholder.typicode.com/posts/1');     const data = await response.json();     window.jsonResult = JSON.stringify(data);   } catch (e) {     window.jsonResult = 'Erreur: ' + e;   }   callback(); })();`|
|3|`execute script`|`return window.jsonResult;`|`jsonResult`|
|4|`echo`|`${jsonResult}`|||`echo: {"userId":1,"id":1,"title":"sunt aut facere repellat provident occaecati excepturi optio reprehenderit","body":"quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"}`|

<details><summary>Log</summary><img src="https://i.imgur.com/LgpewqG.png"></details>	
