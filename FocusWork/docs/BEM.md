
Bloque	Elementos	Modificadores
button	ninguno	--small, --large, --outline
logo	__mark, __text	--light



button es un bloque independiente porque aparece en el header, hero, planes y formulario. No existe header__button porque su apariencia no depende de dónde esté; cada contexto solo lo posiciona. Los modificadores --small, --large y --outline solo declaran lo que cambia respecto al bloque base.

Bloque	Elementos	Modificadores
section	__title, __lead, __grid	--alt, __grid--3
feature-card	__icon, __title, __text	--featured
avatar	ninguno	--large, --alt
testimonial	__text, __author, __meta, __name, __role	--highlight, --compact

section controla el espaciado y la rejilla, y las tarjetas no definen su margen externo; por eso feature-card y testimonial caben en el mismo section__grid. avatar es un bloque propio porque podría usarse fuera de los testimonios. Los modificadores --featured y --highlight describen el rol (destacado), no la apariencia, así que siguen siendo válidos si cambia la paleta. Los elementos nunca se encadenan: testimonial__name, no testimonial__author__name.

pricing-card	__badge, __name, __price, __period, __list, __item	--recommended, __item--off
form	__field, __label, __input, __error, __submit	__field--error, __input--textarea

pricing-card--recommended es un modificador de rol (recomendado), no de apariencia, y solo cambia lo que difiere de la tarjeta base. pricing-card__item--off marca las características no incluidas sin crear un elemento nuevo. En el formulario, form__field--error es un modificador de estado que JavaScript agrega o quita, y el CSS reacciona a él. El botón de envío usa el bloque button más el mix form__submit para posicionarlo, como pasa con el header.

social	__item, __link	ninguno
footer	__inner, __col, __contact, __links, __link, __copy	ninguno

social es un bloque independiente (no footer__social) porque podría ir en el header o en una página de contacto. footer reutiliza logo con su modificador --light en lugar de definir su propio logo, y container para el ancho.