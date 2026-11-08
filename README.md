# Entonar

Entrenador de afinación y lectura para la voz, en una sola página (`index.html`). El micrófono se procesa en el dispositivo.

## Rutina de hoy (33 min, 38 con tu canción)

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
- **Acompañamiento:** sale de los cifrados de la partitura. Hay tres estilos:
  - **Improvisa** (el predeterminado): en cada acorde elige al azar un patrón (arpegio, síncopa, bajo caminante o acordes en los tiempos). Conduce las voces a la posición más cercana, a veces adorna con 9.ª o 4.ª suspendida, y prepara el siguiente acorde con una nota de paso en el bajo.
  - **Balada:** arpegios fijos.
  - **Acordes largos.**

  Siempre suena a volumen bajo y por debajo de la melodía.
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

## Análisis de canto

Mide en el navegador las métricas del análisis externo de «El Triste» (pYIN), para seguir el progreso sin depender de él. Está en **Práctica libre → Análisis libre** (cantar lo que quieras, con o sin tu pista) y en dos ejercicios de la rutina.

| Métrica | Cómo se mide |
|---|---|
| **% dentro de ±20 ¢** | Desviación respecto a la nota temperada más cercana, ponderada por tiempo, con histograma de −50 a +50 ¢ |
| **Referencia de afinación** | La4 ajustable ±50 ¢. Con tu pista cargada, la app estima su afinación (picos del espectro, como `estimate_tuning`) |
| **Notas** | Rachas con voz sin saltos de más de 0.5 st, mediana de 9 cuadros, mesetas de al menos 0.12 s. Por nota: núcleo (25–80 %), ataque desde abajo (< −30 ¢), caída al final (< −30 ¢) y estabilidad. También por registro y por bloques de 30 s |
| **Vibrato** | Notas de al menos 0.6 s: quita el 15 % inicial, remuestrea a 100 Hz, resta tendencia cuadrática, aplica Hann y espectro. Hay vibrato si el pico entre 3.5 y 8.5 Hz supera 3× la media y la amplitud es de al menos 15 ¢ |
| **Frase / legato** | Huecos de menos de 0.35 s no cortan la frase. Solo cuentan frases de más de 1 s |
| **Ring** | Energía de 2 a 4 kHz contra la de 80 Hz a 2 kHz, en dB (mediana de los cuadros con voz) |

**Durante el análisis:**

- Medidores en vivo de frase, ring y vibrato.
- El detector corre en cada cuadro, con una ventana de unos 43 ms, para poder seguir el vibrato.

**Al terminar:**

- Reporte con histograma, comparado contra la línea base del 8 de noviembre de 2026 y contra las metas.
- Tendencia por sesión.
- **Reporte para la maestra**: imprimir o guardar como PDF, con los tramos a revisar.

**Ejercicios en la rutina:**

- **«Ng» que se abre a vocal**, con el medidor de ring.
- **Frases ligadas en «u» con vibrato al final**: al terminar cada frase dice cuánto duró y si hubo vibrato.

**Tu pista de karaoke** se carga en Ajustes → **Análisis** y se queda solo en el dispositivo.

## Resumen al terminar

Al terminar la rutina (o si la detienes a la mitad), aparece un **Resumen de hoy** con lo que escuchó el micrófono:

- **Para mejorar:** los 3 puntos más importantes, cada uno con un consejo concreto. Puede detectar escape de aire (cociente entre la «e» en secreto y la «e» con voz), tomas de aire que se oyen, notas largas cortas o inestables, afinación que se cae al final, volumen a tirones, sonido con aire, un «sss» corto, una ambulancia que no cubre tu rango y un posible quiebre. La afinación solo aparece si anda mal.
- **Lo que salió bien.**
- **Tu tendencia:** compara las métricas de hoy con el promedio de tus últimos 7 días.

El último resumen se puede volver a abrir desde la tarjeta de la rutina. El micrófono no evalúa postura, tensión, timbre ni dicción; para eso conviene grabarse en video de vez en cuando.
