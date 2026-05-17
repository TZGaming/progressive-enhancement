# Progressive Enhancement
Deze README is een work-in-progress op dit moment.

## UI Component - Veelgestelde vragen
<img width="465" height="488" alt="Image" src="https://github.com/user-attachments/assets/abfc161c-2bdf-4999-8272-5c75ac066b46" />

Voor deze UI component heb ik `<details>` en `summary` gebruikt. Dit kan elementen laten uitklappen als je er op klikt. Ik moest alleen wel een `<p>` tag in de summary zetten, anders schaalde de titel van het menu mee met de breedte van wat er in staat ([zie issue](https://github.com/TZGaming/progressive-enhancement/issues/1#issuecomment-4109899175)):

https://github.com/TZGaming/progressive-enhancement/blob/c6df45d5a77c81e802055068435f48dcc2ab563f/faq.html#L101-L107

Verder staat er ook een open state op wat de styling veranderd van het details/summary element, hier word ook de kleur voor elk element aangepast gebaseerd op het aantal:

https://github.com/TZGaming/progressive-enhancement/blob/c6df45d5a77c81e802055068435f48dcc2ab563f/faq.html#L55-L80

## UI Component - Switch Control
<img width="883" height="446" alt="Image" src="https://github.com/user-attachments/assets/77b66c4f-6e13-497d-bb93-190357d8d3c3" />

Voor dit component heb ik `::before` gebruikt om de text in de knop zelf aan te passen. Er zitten ook user preferences in voor de transition van de slider, hierdoor "slide" hij zegmaar niet, maar is hij meteen rechts/links:
https://github.com/TZGaming/progressive-enhancement/blob/c6df45d5a77c81e802055068435f48dcc2ab563f/switch.html#L37-L39

Ook is er een checked state gebruikt om vervolgens de kleur achter de knob groen te maken in plaats van wit:
https://github.com/TZGaming/progressive-enhancement/blob/c6df45d5a77c81e802055068435f48dcc2ab563f/switch.html#L58-L70

## UI Component - Mobiel Menu
<img width="765" height="488" alt="Image" src="https://github.com/user-attachments/assets/7effb991-4afa-46fd-90a4-6b930b3b4d2a" />

Ik heb `:target` gebruikt om de side-bar te vertellen dat hij open kan gaan als er #menu in de URL staat, hij staat normaal off-screen met position fixed -100% op left zodat hij niet te zien is. Zodra #menu dan in de URL staat, dan gaat left op 0% waardoor hij zichtbaar word. Dit is dus een manier om een side-bar te maken zonder enig gebruik van JavaScript.

https://github.com/TZGaming/progressive-enhancement/blob/c6df45d5a77c81e802055068435f48dcc2ab563f/menu.html#L31-L34
https://github.com/TZGaming/progressive-enhancement/blob/c6df45d5a77c81e802055068435f48dcc2ab563f/menu.html#L62-L64

De toggle van de side-bar zelf zit in de `<a>` tag die hem opent, die heeft een href naar #menu waardoor de side-bar dan weet dat hij word gehighlight. Pas dan triggert de CSS code.
https://github.com/TZGaming/progressive-enhancement/blob/c6df45d5a77c81e802055068435f48dcc2ab563f/menu.html#L110
