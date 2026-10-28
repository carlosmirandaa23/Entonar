# Entonar

Entrenador de afinación y lectura para la voz, en una sola página (`index.html`). El micrófono se procesa en el dispositivo.

## Rutina de hoy (30 min, 35 con tu canción)

Está organizada alrededor de las **4 funciones de la voz**:

1. **Cierre de cuerdas:** con el borde, grueso o aireado.
2. **Afinación.**
3. **Altura de la laringe**, incluido el twang.
4. **Resonadores:** nariz o boca.

Se enfoca en el cierre y el aire, que es lo que más falta trabajar. Cada ejercicio indica qué función entrena, y en la tarjeta hay una explicación breve de las cuatro. Antes de cada ejercicio la app explica cómo hacerlo; después cuenta el tiempo y pasa sola al siguiente.

| # | Ejercicio | Función | Min | Qué mide la app |
|---|-----------|---------|-----|-----------------|
| 1 | **Un solo calentamiento** que cambia cada día: trinos, popote, «mmm» o «ng» | Cierre | 3 | Afinación del vocalise |
| 2 | **Toma de aire elegante**: sacar el aire, inhalar en silencio, sostener y soltar en «sss» | Aire | 5 | Si se oyó la toma de aire y cuánto dura el «sss» |
| 3 | **Prueba del aire**: «e» en secreto (susurrada) contra «e» con voz | Cierre | 2 | El cociente entre las dos duraciones. Cerca de 1 es buen cierre; arriba de 1.4 indica escape de aire |
| 4 | **Función del día**: la misma nota cantada de 2 o 3 formas | Rota | 5 | Qué cambió entre las formas (claridad, brillo, afinación y volumen) |
| 5 | **Ambulancia con «i»** | Afinación | 3 | Alcance y posible quiebre de registro |
| 6 | **Nota larga en un solo aliento**, en «i», «a», «o» y «mmm» → vocal | Cierre · aire | 6 | Duración, cuánto se mueve la nota, si se cae al final, si el volumen va parejo y la claridad aproximada |
| 7 | **Terceras en una quinta** | Afinación | 3 | Nivel de memoria |
| 8 | **Terceras completas: subida y bajada** | Afinación | 3 | Nivel de memoria |

**La función del día** rota así: cierre, laringe, cierre, twang, cierre, resonadores. El cierre sale la mitad de los días.

| Función | Formas que se cantan | Qué revisa la app |
|---|---|---|
| Cierre | aireado («a»), limpio con el borde («i»), grueso («e») | Que el limpio tenga más claridad que el aireado, y el grueso más cuerpo |
| Laringe | normal, oscuro (bostezo), brillante (sonrisa) | Que el brillo cambie sin que se mueva la nota |
| Twang | normal, twang de bruja («ñe»), twang abierto («a») | Que el twang sume brillo y se conserve al abrir la vocal |
| Resonadores | nariz («ng»), boca («a»), mitad y mitad («ña») | Que al abrir a la boca suba el brillo |

La claridad y el brillo son aproximados y dependen del micrófono. Lo que cuenta es la diferencia entre una forma y otra.

**Las terceras van por niveles**, por separado en cada patrón:

1. Escuchas el patrón y ves las sílabas en do móvil.
2. Escuchas el patrón, pero las sílabas están ocultas.
3. De memoria: solo suena la primera nota. Las demás aparecen tenues en el pentagrama hasta que las cantas.

Tres rondas limpias seguidas te suben de nivel; tres rondas con fallos seguidas te bajan uno.

- La meta de la nota larga y la del «sss» suben solas con tus récords.
- En Ajustes → **Clase** puedes escribir las indicaciones de tu maestra. Aparecen en la tarjeta de la rutina.
- Si dejas la rutina a medias, «Continuar rutina» la retoma donde te quedaste.
- **Práctica libre** conserva todos los modos (lectura, arcade, ancla, vocalises).
- Los vocalises arrancan en la zona baja-media de tu rango. Si un patrón es casi tan amplio como tu zona cómoda, usan tu rango completo medido para que quede espacio de transponer.

## Mi canción

Para practicar una canción propia, frase por frase. La app **no trae letras ni melodías**: la canción se carga desde un archivo (Ajustes → **Canción**) y se guarda solo en el dispositivo.

Cada frase pasa por tres etapas. Dos intentos buenos seguidos te pasan a la siguiente:

1. **Notas:** escuchas la frase con su ritmo y acordes, y la cantas nota por nota con la letra bajo cada nota.
2. **Con guía:** después de una cuenta de entrada, la cantas a tiempo junto con la melodía. Cada sílaba se califica (verde, amarillo o rojo) y al final se indican las que quedaron altas, bajas o no se oyeron.
3. **Solo acordes:** igual que la anterior, pero sin melodía.

Opciones:

- **Tono:** la app transpone sola para que la canción quepa en tu rango (por ejemplo, una octava abajo de lo escrito para voz grave). También se puede ajustar a mano.
- **Velocidad:** 70–100 %.
- **Etapa y frase:** se pueden elegir a mano.

Con una canción cargada, la rutina agrega el bloque **Tu canción** (5 min). En Práctica libre está el modo **Mi canción**. Usa audífonos si puedes, para que el micrófono solo te oiga a ti.

**Formato del archivo (`entonar-cancion-1`):**

```json
{ "formato": "entonar-cancion-1", "titulo": "…", "tempo": 72, "compas": 4,
  "frases": [ { "texto": "…", "seccion": "…", "pulso": 3, "duracion": 7,
                "acordes": [[0, "C"], [5, "Em"]],
                "notas": [[67, 0.5, "sí", 0], [76, 2, "la", 0.5]] } ] }
```

- Cada nota es `[midi escrito, duración en tiempos, sílaba, inicio en tiempos desde el comienzo de la frase]`.
- `pulso` es el tiempo del compás en que empieza la frase, contado desde 0.
- Los acordes van como `[tiempo, nombre]`, con nombres como C, Em, G7 o Dm7.

## Resumen al terminar

Al terminar la rutina (o si la detienes a la mitad), aparece un **Resumen de hoy** con lo que escuchó el micrófono:

- **Para mejorar:** los 3 puntos más importantes, cada uno con un consejo concreto. Puede detectar escape de aire (cociente entre la «e» en secreto y la «e» con voz), tomas de aire que se oyen, notas largas cortas o inestables, afinación que se cae al final, volumen a tirones, sonido con aire, un «sss» corto, una ambulancia que no cubre tu rango y un posible quiebre. La afinación solo aparece si anda mal.
- **Lo que salió bien.**
- **Tu tendencia:** compara las métricas de hoy con el promedio de tus últimos 7 días.

El último resumen se puede volver a abrir desde la tarjeta de la rutina. El micrófono no evalúa postura, tensión, timbre ni dicción; para eso conviene grabarse en video de vez en cuando.
