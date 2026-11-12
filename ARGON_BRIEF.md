# Los Rojas Coffee — Brief de desarrollo para Argon

## 1. Objetivo del proyecto

Construir el sitio web oficial de **Los Rojas Coffee**, una experiencia comercial e informativa para que los clientes conozcan y exploren los productos desde un enlace o un único código QR impreso en las etiquetas.

La prioridad es **presentar los productos**. La historia de la marca, el origen y el proceso productivo complementan el catálogo, pero no deben desplazarlo.

El sitio debe ser:
- Premium, elegante y visualmente cuidado.
- Bilingüe: español e inglés.
- Mobile-first: la mayoría de visitas puede llegar desde un teléfono al escanear un QR.
- Rápido, accesible y fácil de mantener.
- Preparado para incorporar un panel administrativo y un asistente con IA.

## 2. Dirección visual

Estilo: premium editorial, cálido y minimalista; evitar la apariencia de plantilla genérica o de diseño generado automáticamente.

Paleta inicial orientativa:
- Espresso: #241B16
- Café: #79543A
- Arena: #D5B995
- Marfil: #F5F0E7

Tipografía:
- Títulos con serif editorial elegante.
- Texto y controles con sans serif legible.

Usar fotografías y videos originales aportados por la marca como recurso visual prioritario. No reemplazar las fotografías reales con imágenes de stock o imágenes generadas. Mantener proporciones, calidad y carga optimizada. Aplicar recortes con cuidado y permitir abrir fotografías en una galería cuando tenga sentido.

## 3. Arquitectura de información

Construir inicialmente un sitio comercial tipo catálogo, con navegación clara:

1. **Inicio**: presentación de marca y productos destacados; llamada clara a explorar el catálogo.
2. **Productos / Catálogo**: listado de productos en tarjetas visuales.
3. **Ficha de producto**: fotografías, nombre, presentación, variedad o blend, proceso, tueste, perfil sensorial, origen, datos de evaluación disponibles, precio y disponibilidad cuando se confirmen.
4. **Calidad y proceso**: explicación del proceso Honey y datos de calidad respaldados por documentos.
5. **Origen**: Finca Bella Vista, Manaure, Cesar; la historia detallada queda pendiente de información de la marca.
6. **Preparación**: guía opcional de preparación, solo con recomendaciones que la marca confirme.
7. **Contacto**: canales comerciales y redes sociales cuando se entreguen.

El catálogo debe tener prioridad visual y de navegación. No implementar carrito, pagos ni gestión de pedidos en la primera versión salvo que el responsable del proyecto lo confirme expresamente. Dejar previsto un enlace de consulta comercial (por ejemplo WhatsApp) cuando se suministre el número oficial.

## 4. Información de producto confirmada

### Datos generales comunicados por la marca
- Marca: Los Rojas Coffee.
- Finca: Bella Vista.
- Productora y líder de producción: Gladys Rojas, propietaria de la finca.
- Representación de marketing y plataforma: Juan Felipe.
- Origen indicado para el análisis adjunto: Manaure, Cesar, Colombia.
- Variedades mencionadas por la marca: Tabi, Caturro y Castillo. No asumir si se venden por separado o mezcladas; falta confirmación.
- Niveles de tueste comunicados: medio y medio-alto. No asignar uno a un producto específico sin confirmación.
- Presentaciones: 250 g y 500 g.
- Empaque: todavía en diseño.
- Perfil sensorial general de los lotes actuales: pendiente de confirmación.

### Análisis físico y sensorial documentado
Existe un informe de una muestra analizada el 24/11/2024:
- Productora: Gladys Rojas.
- Municipio: Manaure, Cesar.
- Variedad: Castillo.
- Proceso: Honey.
- Humedad C.P.S.: 11,9.
- Puntaje de la muestra: 86,50.
- Puntaje del catador: 8,50.
- Fragancia/aroma: 8,25.
- Sabor: 8,00.
- Sabor residual: 7,75.
- Acidez: 7,75.
- Cuerpo: 8,25.
- Balance: 8,00.
- Uniformidad: 10,00.
- Taza limpia: 10,00.
- Dulzor: 10,00.
- Notas registradas: cítrico, naranja, mandarina, especias y caramelo; sabor cítrico intenso y miel; acidez media fina y cítrica; cuerpo consistente; residual limpio y especiado.
- El informe indica cero tazas defectuosas y cero broca.

**Regla de exactitud:** estos resultados corresponden a esa muestra Castillo Honey analizada en 2024. No atribuir el puntaje ni el perfil a todos los cafés, a Tabi, Caturro, a mezclas o a cosechas actuales. Identificarlo como análisis de muestra/lote cuando se publique y conservar la fecha.

## 5. Proceso Honey y sostenibilidad: redacción responsable

La marca desea comunicar que el método Honey conserva parte del mucílago natural durante el secado y busca reducir el consumo de agua frente a determinados procesos lavados.

Redactar con precisión y sin garantías no demostradas. No afirmar que:
- el producto es libre de agroquímicos, orgánico o certificado sin pruebas;
- se eliminan totalmente las aguas mieles o toda contaminación;
- el café tiene mayor digestibilidad o beneficios médicos;
- contiene una cantidad o aumento específico de antioxidantes;
- todos los cultivos son agroforestales o protegen biodiversidad sin documentación.

Texto editorial provisional:
“En el proceso Honey se conserva parte del mucílago natural del café durante el secado. Este método puede reducir el uso de agua frente a determinados procesos de beneficio lavado. En Los Rojas Coffee trabajamos para comunicar con transparencia el origen, el procesamiento y la calidad de cada lote.”

## 6. Idiomas

Implementar selector ES / EN visible y persistente durante la navegación. Toda la interfaz, navegación, fichas y contenidos editables deben tener campos para ambos idiomas. La versión inglesa debe ser traducción fiel y no añadir afirmaciones que no existan en español.

Si falta una traducción, mostrar un estado claro o el contenido español como fallback; no dejar controles rotos.

## 7. Catálogo administrable

Modelar productos como datos, no como contenido rígido incrustado en componentes.

Campos sugeridos:
- id / slug
- nombre_es / nombre_en
- descripción_es / descripción_en
- estado: borrador / publicado / archivado
- variedad o composición (sin asumir mezcla)
- proceso
- tueste
- perfil sensorial_es / perfil sensorial_en
- origen
- altitud (opcional, pendiente)
- presentaciones (250 g, 500 g y futuras)
- precio (opcional, pendiente de confirmar)
- disponibilidad
- imágenes y texto alternativo
- videos opcionales
- documentos o análisis vinculados al lote
- fecha y referencia del análisis
- lote/cosecha cuando se disponga
- orden de presentación y destacado

No inventar precios, altitud, perfil sensorial actual, certificaciones, disponibilidad ni datos de lote. Mostrar solo datos confirmados y ocultar campos vacíos.

## 8. Panel administrativo e IA — fase posterior

Preparar una arquitectura que permita implementar un área privada de administración:
- crear, editar, duplicar, publicar, despublicar y archivar productos;
- editar secciones y contenido adicional;
- gestionar imágenes y videos;
- actualizar contenido en español e inglés;
- vista previa antes de publicar;
- control de roles y registro de cambios.

Asistente de IA deseado:
- entender instrucciones naturales para preparar cambios en productos y textos;
- proponer descripciones y traducciones;
- pedir los datos faltantes en vez de inventarlos;
- mostrar una vista previa y solicitar aprobación humana antes de publicar;
- ejecutar solo operaciones autorizadas mediante backend.

**Seguridad:** nunca exponer claves API, secretos o credenciales en el frontend o en el repositorio. Las llamadas a modelos de IA y las operaciones de administración deben pasar por backend seguro. No implementar el asistente como simulación que afirme guardar cambios cuando no lo hace.

## 9. QR y dirección web

Se desea un solo QR para todas las presentaciones. Su destino final será una URL estable de la marca.

- Dominio deseado a futuro: https://losrojascoffee.com/ (elegido, aún no registrado).
- Alojamiento provisional considerado: Cloudflare Pages.
- Subdominio propuesto: https://losrojascoffee.pages.dev/ (no creado ni confirmado).
- No generar el QR definitivo ni afirmar que la página está publicada hasta verificar despliegue, HTTPS y URL final.
- Mantener las rutas internas estables y redirigir correctamente si cambia la estructura.

## 10. Stack y despliegue

Propuesta inicial, sujeta a evaluación técnica:
- React + TypeScript con Vite.
- CSS modular o Tailwind, sin mezclar sistemas innecesariamente.
- Componentes reutilizables y diseño responsive.
- Datos de catálogo inicialmente en archivos JSON tipados o una capa de datos separada; preparar migración a backend.
- Cloudflare Pages para despliegue frontend si la configuración y el uso cumplen sus condiciones.
- Backend y base de datos (por ejemplo Supabase) solo cuando el panel autenticado y las funciones dinámicas lo requieran.

No añadir dependencias innecesarias. Incluir instrucciones reproducibles de instalación, desarrollo, build y despliegue.

## 11. Criterios de aceptación de la primera versión

1. Navegación clara y catálogo visible desde la portada.
2. Excelente experiencia móvil y carga rápida.
3. Selector de idioma funcional.
4. Fichas de producto con campos faltantes ocultos, nunca inventados.
5. Sección de análisis sensorial correctamente atribuida a la muestra Castillo Honey de noviembre de 2024.
6. Imágenes originales optimizadas y con textos alternativos.
7. Botones y enlaces funcionales; no incluir controles decorativos sin acción.
8. Sin secretos ni claves API dentro del cliente o Git.
9. Sin carrito ni pagos hasta recibir confirmación del alcance comercial.
10. README actualizado con pasos para ejecutar y publicar.

## 12. Forma de trabajo

Desarrollar por etapas y validar cada una:
- Fase 1: estructura, diseño responsive, navegación y catálogo de demostración con contenido confirmado.
- Fase 2: fichas de producto, galerías y bilingüismo completo.
- Fase 3: integración de fotografías y videos originales.
- Fase 4: panel administrativo con autenticación.
- Fase 5: asistente IA seguro, vista previa y aprobación.
- Fase 6: pruebas, optimización y despliegue.

Antes de asumir datos o funciones no especificados, formular una pregunta concreta o dejar el campo pendiente. Priorizar la veracidad del contenido y la calidad visual.
