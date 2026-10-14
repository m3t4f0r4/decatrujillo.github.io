# DeCA Cloud España — Plataforma Profesional de Generación de Documentos de Control Administrativo

DeCA Cloud es una plataforma web enterprise diseñada para la emisión, gestión y verificación inmutable de **Documentos de Control Administrativo (DeCA)** para el transporte público de mercancías por carretera en España. El sistema implementa los estándares jurídicos establecidos por la Ley 9/2025 de Movilidad Sostenible, la Orden FOM/2861/2012, la Orden TRM/282/2026 y la Resolución de 5 de junio de 2026 de la Dirección General de Transporte por Carretera y Ferrocarril.

---

## Especificaciones Técnicas y Cumplimiento Normativo

* **Estructura de Datos Obligatoria:** Modelado relacional completo de acuerdo con el artículo 6 de la Orden FOM/2861/2012, contemplando los datos del cargador contractual, transportista efectivo, origen, destino, naturaleza de la mercancía, pesos con unidades normalizadas y matrículas de vehículos tractores y remolques.
* **Trazabilidad Criptográfica:** Integridad documental mediante hashes SHA-256 para asegurar la detección de alteraciones y garantizar la trazabilidad entre versiones sustitutivas o modificadas.
* **Códigos QR e Inspección Directa:** Generación de códigos QR de alta densidad de error que codifican URLs HTTPS únicas y persistentes. Diseñado para permitir el acceso directo de los Cuerpos de Inspección de Transporte al documento oficial sin requerir pantallas de autenticación o credenciales intermedias.
* **Emisión Previa al Servicio:** El flujo transaccional bloquea cualquier emisión que no certifique la generación del documento con carácter previo al inicio efectivo de la operación de transporte.

---

## Arquitectura del Sistema

La solución se compone de una arquitectura desacoplada orientada a microservicios y alta disponibilidad:

1. **Frontend (Interfaz de Gestión y Escrititorio):** Desarrollado con HTML5, CSS moderno (Tailwind CSS) y JavaScript optimizado, incorporando validaciones síncronas de datos fiscales (NIF/CIF), formatos de matrículas y control estructurado por pasos.
2. **Backend de Procesamiento (Node.js / NestJS):** Módulos robustos para la compilación de ficheros PDF nativos (garantizando peso inferior a 5 MB, texto seleccionable y metadatos de emisión temporales) y motor de cifrado.
3. **Capa de Persistencia (PostgreSQL):** Esquema relacional optimizado con restricciones estrictas de integridad referencial, aislamiento de datos multi-tenant por empresa y bitácora de auditoría inmutable.

---

## Despliegue en GitHub Pages (Frontend Estático)

La aplicación está preparada para su despliegue inmediato en entornos estáticos como **GitHub Pages**:

1. Asegúrate de que el archivo principal esté renombrado como **`index.html`**.
2. Sube el fichero a la rama principal (`main`) de tu repositorio público en GitHub.
3. Configura la sección **Pages** dentro de las opciones de configuración (*Settings*) de tu repositorio, seleccionando la rama `main` y la carpeta raíz (`/root`).
4. La plataforma quedará accesible mediante un certificado SSL (HTTPS) de forma permanente.

---

## Seguridad y Privacidad (RGPD)

* **Principio de Minimización:** Los códigos QR públicos contienen exclusivamente la URL de verificación de la expedición concreta, evitando la exposición innecesaria de datos personales o empresariales ajenos a la inspección.
* **Aislamiento de Accesos:** Control riguroso de roles (RBAC) para Superadministradores, Administradores de Empresa y Verificadores Documentales, previniendo accesos horizontales no autorizados entre diferentes entidades jurídicas.