GitHub Dorks

Una colección de "dorks" (consultas avanzadas de búsqueda) para el buscador de código de GitHub, pensada para ayudar a investigadores de seguridad, equipos de Red Team y profesionales de OSINT a identificar información sensible expuesta accidentalmente en repositorios públicos: claves de API, credenciales, tokens, archivos de configuración, variables de entorno y otros secretos.

¿Qué es un "GitHub Dork"?

Un dork es una consulta de búsqueda que combina palabras clave y operadores específicos del motor de búsqueda de GitHub (filename:, extension:, path:, org:, repo:, etc.) para localizar archivos o fragmentos de código que probablemente contengan datos sensibles, en lugar de buscar código de forma genérica.

Ejemplo:

filename:.env DB_PASSWORD

Esto busca archivos .env que contengan la cadena DB_PASSWORD, un patrón común en configuraciones mal gestionadas.

Contenido del repositorio
Archivo	Descripción
dorks.txt	Lista principal de dorks, organizados por categoría (credenciales en la nube, claves de API, bases de datos, tokens de CI/CD, etc.)
README.md	Este documento
Uso
Elegí un dork de la lista según lo que estés buscando (por ejemplo, claves de AWS, tokens de Slack, credenciales de bases de datos).
Pegalo en la búsqueda de código de GitHub o adaptalo para usarlo con la API de búsqueda de GitHub.
Podés acotar la búsqueda a una organización o repositorio específico agregando org:nombre-org o repo:usuario/repo.

Nota: GitHub aplica límites de tasa (rate limits) a las búsquedas, tanto vía web como vía API. Si vas a automatizar consultas, autenticate con un token personal para tener un límite más alto y espaciá las solicitudes.

Categorías cubiertas
Credenciales de proveedores cloud (AWS, GCP, Azure)
Claves de API de servicios de terceros (Stripe, Twilio, SendGrid, etc.)
Archivos de configuración y variables de entorno (.env, config.json, settings.py)
Tokens de CI/CD y webhooks
Cadenas de conexión a bases de datos
Claves privadas y certificados (.pem, id_rsa)
Uso responsable

Este material está pensado exclusivamente para:

Investigación de seguridad autorizada (pentesting con alcance definido, programas de bug bounty).
Auditorías internas de tu propia organización, para detectar filtraciones antes de que las encuentre un tercero.
Fines educativos y de concientización sobre higiene de secretos en el desarrollo de software.

No está permitido usar estos dorks para acceder, explotar o exfiltrar información de sistemas o repositorios para los que no tengas autorización explícita. Si encontrás un secreto expuesto que no te pertenece, lo correcto es reportarlo de forma responsable (responsible disclosure) al propietario del repositorio o a la organización correspondiente, y no acceder a los sistemas asociados.

Los autores y colaboradores de este repositorio no se hacen responsables del mal uso de esta información.

Contribuir

Las contribuciones son bienvenidas. Para agregar un nuevo dork:

Hacé un fork del repositorio.
Agregá tu dork a dorks.txt en la categoría correspondiente (o creá una nueva si no existe).
Abrí un Pull Request describiendo qué tipo de información ayuda a encontrar.
Licencia

Especificá aquí la licencia del repositorio (por ejemplo, MIT
