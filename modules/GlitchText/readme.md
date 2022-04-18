```js
const from = "Hello, World";
const to   = "Hello, Snowy";

const params = {
  step: 2,
  minimum: 10,
  maximum: 200
}
const glitch = new GlitchText(from, to, params);

for (content of glitch){
  body.textContent = content;
  await delay(15);
}
```
