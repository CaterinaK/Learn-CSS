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
