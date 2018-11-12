Learn CSS: Selectors and Visual Rules 

CSS, or Cascading Style Sheets, is a language that web developers use to style the HTML content on a web page. The “cascading” in CSS refers to the fact that styling rules “cascade” down from several sources. This means that CSS has an inherent hierarchy and styles of a higher precedence will overwrite rules of a lower precedence. 

Можно обойтись и без CSS. Для этого используем встроенные стили (inline styles). Для этого используем атрибут style, например, внутри абзаца. 
Им можно задать color:, font-size:, font-family: etc. Обязательно на конце должно быть ;

Но если нужно задать стиль нескольким параграфам\заголовкам и.т.д., то нужно будет для каждого прописывать. Такое себе.
Тут на помощь приходит тег style, внутри которого можно писать CSS код. Тег style обязательно располагается внутри тега head, иначе чуда не произойдёт. 

Лучше не смешивать html и css код в одном документе, для этого создаём отдельный style.css и туда весь CSS код пишем.  “separate our concerns”

Чтобы css отображался в документе, нужно использовать self-closing тег link (внутри тега head), который содержит атрибуты:
href — like the anchor element, the value of this attribute must be the address, or path, to the CSS file.
type — this attribute describes the type of document that you are linking to (in this case, a CSS file). The value of this attribute should be set to text/css.
rel — this attribute describes the relationship between the HTML file and the CSS file. Because you are linking to a stylesheet, the value should be set to stylesheet.

Например, link href="https://www.codecademy.com/stylesheets/style.css" type="text/css" rel="stylesheet"

Чтобы выбрать часть html, нужно использовать идентификатор (selector) - это тег без квадратных скобок. Но так можно только с видимыми частями, а с метадатой (head) такого не получится, например. 
Идентификатором может быть не только тег, но и атрибут class. Т.е. например class="brand", тогда мы используем .brand для обозначения в css (точку ставить обязательно). 
Можно задать несколько class, для этого в css нужно добавить элемент, а потом в Html файле дополнить атрибут (без запятой). 

Можно тегать элементы из html по id, для этого нужно в css добавить #имя_Id лучше добавлять по одному. 

Класс используются, когда нужно много элементов стилизировать, а id - когда один. Id>class id>tag. 

Specificity is the order by which the browser decides which CSS styles will be displayed. A best practice in CSS is to style elements while using the lowest degree of specificity, so that if an element needs a new style, it is easy to override. IDs are the most specific selector in CSS, followed by classes, and finally, tags. The only way to override an ID is to add another ID with additional styling. 

Лучше всего в документе использовать спецификацию по тегам по возможности, зачем классы и в самом крайнем случае по id.
Важная инфа: https://discuss.codecademy.com/t/is-it-possible-for-two-selectors-targeting-the-same-element-to-have-the-same-specificity-if-so-which-styles-win-out/340952

Chaining Selectors (сцепление?): можно выбрать, какие именно элементы html будут относиться к этому селектору. Для этого пишем, например, h1.special, тогда для остальных элементов с классом special это правило не будет выполняться. A chained or qualified selector has a higher specificity than a class selector but a lower specificity than the id selector. 
В общем, specificity, как я поняла: id>chained>class>tags
Можно ещё выбрать конкретные элементы внутри других элементов, например для элемента с классом main-list, который наследуется элементом li: .main-list li{}. 

Adding more than one tag, class, or ID to a CSS selector increases the specificity of the CSS selector.

CSS VISUAL RULES 

Типографика (font family). По умолчаю везде Times New Roman. Чтобы шрифт отображался, нужно, чтобы он был установлен на компе пользователя. Хорошо использовать не более 2-3 шрифтов на странице. Если название шрифта состоит из нескольких слов, то берём его в кавычки (привет булевым запросам). 
Вот тут список шрифтов, которые чаще всего уже установлены в ОС: https://www.cssfontstack.com/ 

font-size - размер шрифта (в пикселях px). Если не определяем, то чаще всего браузеры используют 16 пикселей. 
font-weight - толщина. Есть bold и normal. Normal чтобы в отдельном параграфе менять толщину, если во всём остальном тексте выбран другой параметр. Bold есть не у всех шрифтов. 

text-align - расположение текста. По умолчанию он всегда слева в браузере. 
left — aligns text to the left hand side of its parent element, which in this case is the browser.
center — centers text inside of its parent element.
right — aligns text to the right hand side of its parent element.

цвет: color и background-color. По сочетаемости цветов советуют вот эту книгу:
https://issuu.com/serlutin/docs/______________-________________________ 

Opacity (непрозрачность). От 1 (видим) до 0 (невидим). 

 background-image: url("images/mountains.jpg")



