Доступна одна функция — GlitchText, представляет собой итерируемый объект
При каждой итерации возвращает чуть изменённое текстовое содержимое, которое стремится к конечной точке
Начальный текст — from
Конечный — to

Третим аргументом принимает параметры:
step — определяет насколько сильно за одну итерацию преобразится текст (по умолчанию 15)
minimum — вводит минимальный разрыв между начальной и конечной (по умолчанию отсуствует)
maximum — соответсвенно, максимальный разрыв
random — следует ли каждый раз применять (step * Math.random() * 2) для шага (по умолчанию false)
```js
const from = "Hello, World";
const to   = "Hello, Snowy";

const params = {
  step: 2,
  random: true,
  minimum: 10,
  maximum: 200
}
const glitch = new GlitchText(from, to, params);

for (content of glitch){
  body.textContent = content;
  await delay(15);
}
```
