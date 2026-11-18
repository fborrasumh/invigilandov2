# Invigilando

Vigilancia competitiva y tecnológica con cada hallazgo anclado a sus fuentes. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/invigilandov2/

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

- Vigila una empresa (competidores, precios, productos, contratación, financiación) o una tecnología (quién la desarrolla o la vende, regulación, oportunidades de transferencia).
- Búsqueda en internet con claves propias de **Tavily** y de **Serper**, que se ponen en el botón «IA» junto a la clave del proveedor de IA. Hay tres modos: Tavily con Serper de reserva si no hay resultados, solo Serper, o los dos a la vez para tener más fuentes independientes. Las claves de Invigilando 2 se migran solas.
- Búsquedas por defecto generadas por el código a partir del encargo, que la IA puede mejorar y la persona edita. Tres profundidades.
- Lista de fuentes sin URL duplicadas: se pueden desmarcar o añadir a mano.
- Informe con resumen, tres claves, mercado, competidores o actores, señales por área, DAFO, riesgos con puntuación de amenaza, plan de acción a 90 días y lagunas de información.
- Alertas por umbral, filtro «solo lo confirmado por dos fuentes», historial y comparación con el informe anterior del mismo objeto.
- Word, CSV de fuentes y JSON. Ejemplo sin clave en español, inglés y portugués, con fuentes ficticias (dominios .example).

## Qué comprueba el código

- La cita de cada hallazgo en el extracto de su fuente. Una fuente desmarcada no cuenta.
- Cuántos dominios distintos respaldan cada hallazgo: confirmado (dos o más), una fuente o sin respaldo.
- Las cifras del informe que no aparecen en ninguna fuente.
- La puntuación de amenaza, calculada a partir de la probabilidad, el impacto y el horizonte (impacto alto 40, medio 25, bajo 10; probabilidad alta 30, media 20, baja 10; horizonte 0-6 meses 30, 6-12 meses 20, más de 12 meses 10). Solo hay alerta si se supera el umbral y hay al menos una cita verificada.
- Que los valores que propone la IA (amenaza, probabilidad, horizonte, plazos) son de los permitidos; si no, se normalizan.

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude. La clave se guarda solo en el navegador. No hace falta servidor.

## Privacidad

El encargo, las fuentes, los informes, el historial y las claves (de IA, Tavily y Serper) se guardan solo en el navegador. Las búsquedas salen hacia Tavily o Serper; la clave va siempre en la cabecera, nunca en el cuerpo. Los extractos de las fuentes elegidas y el encargo salen hacia el proveedor de IA, con correos, DNI/NIE y teléfonos enmascarados. Antes del primer envío de cada tipo se muestra lo que sale y se pide confirmación.

## Límites

- Los buscadores devuelven extractos, no páginas completas: la cita se comprueba contra el extracto.
- Que una cita exista no garantiza que la interpretación de la IA sea correcta ni que la fuente sea fiable. El DAFO es interpretación de la IA, sin citas.
- Cada búsqueda consume créditos de la cuenta de Tavily o de Serper.
- Probada con buscadores e IA simulados en los tres proveedores; no con claves reales.
- Respecto a Invigilando 2 se han dejado fuera el análisis de patentes, los modelos distintos por agente y la autoevaluación de calidad.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche).


ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)

## Cómo citar

Borrás Rocher, F. (2026). *Invigilando* (v1.0.0) [Software]. https://doi.org/10.5281/zenodo.21423389

## Licencia

MIT. Véase [LICENSE](LICENSE).
