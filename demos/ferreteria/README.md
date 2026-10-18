# Demo: Santiago Ferretería

En vivo: **https://santiago3336.github.io/demos/ferreteria/**

> [!WARNING]
> «Santiago Ferretería» es una **marca inventada** para mostrar el diseño. Los precios, referencias y horarios son de ejemplo, y no se usa ninguna dirección real.

## Qué demuestra

Es un **catálogo B2B con cotizador**, pensado para una ferretería que le vende a maestros de obra y constructoras:

- La página no es una sola columna larga: está dividida en planos (Inicio, Catálogo, Para obra, Líneas y Contacto). Se ve uno a la vez y se pasa de uno a otro con un deslizamiento. Un menú flotante acompaña el recorrido, al lado contrario de la lista «Pruebe esta demo»: muestra el plano actual, tiene una flecha al siguiente y despliega todos con una frase de qué hay en cada uno. Al final de cada plano, una tarjeta invita al siguiente. La dirección cambia con cada plano, así que el botón «atrás» funciona. Sin JavaScript, la página se ve completa en una sola columna.
- Hero con una lámina de plano técnico que se traza al cargar.
- Catálogo por línea de producto (eléctrico, plomería, herramienta, tornillería, construcción, pintura), con buscador sin tildes, filtros que reacomodan las tarjetas y precios a la vista. Se ve completo aunque el navegador no ejecute JavaScript.
- Cotizador: el cliente agrega referencias y cantidades, el producto "vuela" a la barra del cotizador y la página arma el mensaje del pedido listo para enviar por WhatsApp.
- Sección de cuenta para maestros y constructoras (crédito, despacho a obra).
- Espacio para la dirección (en la demo no se usa ninguna dirección real) y el horario.
- Espacio para las reseñas reales de Google del negocio. En la demo queda vacío a propósito, porque no se inventan reseñas.

Todo está en un solo `index.html`, sin frameworks ni dependencias.
