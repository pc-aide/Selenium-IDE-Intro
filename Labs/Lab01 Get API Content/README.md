# Lab01 Get API Content

---

## v0.01
|n|Command|Target|Value|Description|Log|
|-|-------|------|-----|-----------|---|
|1|`execute script`|`window.jsonResult = "";`||Clear jsonResult|
|2|`execute async script`|`(async () => {   const callback = arguments[0];   try {     const response = await fetch('https://jsonplaceholder.typicode.com/posts/1');     const data = await response.json();     window.jsonResult = JSON.stringify(data);   } catch (e) {     window.jsonResult = 'Erreur: ' + e;   }   callback(); })();`|
|3|`execute script`|`return window.jsonResult;`|`jsonResult`|
|4|`echo`|`${jsonResult}`|||`echo: {"userId":1,"id":1,"title":"sunt aut facere repellat provident occaecati excepturi optio reprehenderit","body":"quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"}`|
