# DeCA Trujillo — Sistema de Control Administrativo para el Transporte de Mercancías

DeCA Trujillo es una solución tecnológica avanzada orientada a operadores logísticos, empresas de transporte y cargadores para la emisión, gestión y custodia de **Documentos de Control Administrativo (DeCA)** en el sector del transporte público de mercancías por carretera en España. La plataforma se alinea con los estándares jurídicos establecidos por la Ley 9/2025 de Movilidad Sostenible, la Orden FOM/2861/2012, la Orden TRM/282/2026 y la Resolución de 5 de junio de 2026 de la Dirección General de Transporte por Carretera y Ferrocarril.

---

## Marco Normativo y Fundamentos Jurídicos

El diseño del sistema responde de forma estricta a las exigencias regulatorias vigentes para garantizar la seguridad jurídica en la cadena de transporte:

* **Trazabilidad y Asignación de Responsabilidades:** Integración de los datos estructurales obligatorios que delimitan las obligaciones entre el cargador contractual y el transportista efectivo, conforme a las modificaciones introducidas por la normativa sectorial reciente.
* **Soporte Electrónico Homologado:** Adaptación a las disposiciones relativas a la digitalización del documento de control administrativo, garantizando la equivalencia funcional con los soportes tradicionales y su disponibilidad ante los Cuerpos de Inspección de Transporte.
* **Verificación Dinámica mediante Código QR:** Generación de enlaces seguros bajo protocolo HTTPS que permiten a las autoridades competentes la comprobación inmediata de la autenticidad del documento sin comprometer la confidencialidad de la información corporativa.

---

## Características Técnicas del Sistema

* **Estructura de Datos Normalizada:** Modelado riguroso de los campos obligatorios exigidos por la legislación, incluyendo la identificación fiscal de los intervinientes, detalles geográficos de origen y destino, naturaleza de la mercancía, control de pesos con unidades tipificadas y registro de matrículas de vehículos tractores y remolques.
* **Integridad Documental:** Mecanismos de sellado y control criptográfico mediante hashes SHA-256 para la detección inmediata de cualquier intento de alteración o modificación no autorizada de los registros emitidos.
* **Aislamiento Multi-Tenant y Seguridad (RGPD):** Arquitectura diseñada bajo el principio de privacidad desde el diseño, asegurando el cumplimiento estricto del Reglamento General de Protección de Datos mediante el aislamiento lógico de datos entre empresas y la minimización de la información expuesta en los accesos públicos de inspección.
