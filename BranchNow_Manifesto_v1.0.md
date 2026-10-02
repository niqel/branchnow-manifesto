# 📘 BranchNow Manifesto v1.0

### Autor: Gustavo Meléndez Villarreal

### Fecha de publicación: 2025-04-16

---

## 🔥 Introducción

BranchNow es una arquitectura moderna y declarativa para la sincronización distribuida de datos, interfaces y lógica de aplicación, basada en principios de versionamiento, modularidad y control. Inspirada en Git, scripting y la filosofía de texto plano versionable, BranchNow redefine cómo deben estructurarse y evolucionar las aplicaciones modernas.

BranchNow no es una herramienta única, ni un lenguaje, ni un protocolo. Es un modelo arquitectónico completo, adaptable a cualquier tecnología que soporte:

- Texto plano
- Control de versiones (como Git)
- Estructura modular de carpetas y archivos

Su objetivo es permitir una evolución controlada, trazable y distribuida del software, sin necesidad de bases de datos pesadas, APIs REST complejas ni despliegues monolíticos.

---

## 🧠 Principios fundacionales

- Todo es texto plano versionable
- Las vistas, datos y lógica son módulos independientes
- No hay estado centralizado obligatorio
- El sistema es offline-first por diseño
- Las ramas representan contextos, ambientes o clientes
- Git (u otro sistema de versiones) es el medio de transporte
- El usuario tiene control total del ciclo `pull` / `commit` / `revert`

---

## 📐 Clasificación y alcance de BranchNow

BranchNow no solo es una arquitectura de software. Es una base completa para prácticas DevOps, modelos de entrega ágil, y plataformas educativas.Con su estructura modular, trazabilidad natural y compatibilidad total con tecnologías modernas, BranchNow representa una nueva era en la evolución del software distribuido.

---

## 🧩 Estructura de una aplicación BranchNow

```plaintext
/app/
  /vista/          <- HTML, CSS, JS o cualquier interfaz embebida
  /datos/          <- Archivos JSON, YAML, TOML, XML, etc.
  /logica/         <- Scripts declarativos, JS, BSL, o WASM
  /scripts/        <- Shell scripts (bash, ps1), tareas del sistema
  /bin/            <- Módulos binarios precompilados (.wasm)
  meta.yml         <- Descripción del paquete
```

---

## 🛠 Flujo de trabajo

1. `branchnow init`
2. `branchnow pull`
3. Editar datos, vistas o reglas
4. `branchnow commit -m "Actualización de items"`
5. `branchnow push (opcional, si se usa Git remoto)

Las aplicaciones se actualizan por `pull`, y cada cliente puede mantener su propia rama sincronizada.

---

## 📦 Casos de uso ideales

- Apps distribuidas offline (ventas, inventarios, kioskos)
- Sistemas multi-sucursal sin servidor central
- Aplicaciones con lógica local en PowerShell / Bash / JS
- UIs en WebView (Tauri, Electron, Capacitor)
- Plataformas educativas / documentación offline
- Juegos modulares, simuladores, configuradores
- Nodos web regionales (sitios que cambian por país, evento o promoción)
- Aplicaciones online con sincronización distribuida por contexto
- Operaciones sensibles respaldadas con commits (ej. depósitos bancarios, validaciones)

---

## 🔐 Control, licencia y marca

- ✅ **Uso comercial indirecto**:  El uso de BranchNow en aplicaciones internas que gestionen, habiliten o automaticen operaciones con fines comerciales —como ventas internas, reservas, dispensación de productos, servicios pagos o transacciones indirectas— requiere un acuerdo formal de uso.  Esto incluye a empresas que, aunque no vendan el software directamente, lo utilicen como base para procesos que generen ingresos o formen parte de su modelo de negocio.  Casos como parques recreativos, hospitales corporativos o plataformas internas con servicios rentables deberán establecer licencia con el autor.

- ✅ **Uso institucional a gran escala**:  El uso de BranchNow por entidades gubernamentales, educativas, sin fines de lucro o corporativas a gran escala también deberá evaluarse caso por caso para determinar si corresponde una licencia.  Incluso si no existe un lucro directo, pero la arquitectura potencia servicios, recauda fondos o reduce costos de forma significativa, puede requerirse un acuerdo con el autor.

BranchNow es un modelo de arquitectura publicado libremente por su autor, pero protegido legalmente.

- La arquitectura es abierta, pero su uso en plataformas comerciales, institucionales o integraciones cloud requiere licencia o convenio.
- El nombre BranchNow y sus herramientas oficiales son marca registrada.
- El manifiesto técnico y su estructura están cubiertos por derechos de autor.

BranchNow está disponible para la comunidad. Su integración comercial deberá hacerse bajo términos justos, con reconocimiento al autor y sin alteraciones de la marca.

---

## 🟢 Uso libre y casos que no requieren licencia

BranchNow está disponible para la comunidad bajo principios de acceso libre responsable. El siguiente uso se considera justo y no requiere licencia:

### ✅ Uso libre permitido para:

- Personas desarrolladoras individuales
- Estudiantes y universidades públicas
- Proyectos comunitarios o sin fines de lucro de alcance limitado
- Pequeñas empresas (menos de 10 empleados o ingresos reducidos)
- Uso personal, local o experimental sin fines de lucro
- Publicaciones educativas, investigación y prototipos

### ⚠️ Uso sujeto a licencia:

- Empresas medianas o grandes
- Instituciones privadas que ofrecen servicios pagos
- ONG que operan con donativos masivos o estructuras empresariales
- Gobiernos que integran BranchNow en plataformas públicas
- Escuelas privadas que usan BranchNow como parte de su operación interna
- Proveedores SaaS o consultoras que lo integran en soluciones a clientes

> Si no estás seguro de si tu caso requiere licencia, puedes contactar al autor para evaluación y, si aplica, establecer un acuerdo justo.

---

## 🛡️ Seguridad y distribución protegida

BranchNow fue diseñado para ser compatible con entornos distribuidos, locales y controlados. Para proteger la lógica, integridad y estructura del sistema, se recomiendan las siguientes prácticas:

### 🔐 Minificación y ofuscación

Las vistas y scripts dentro de `/vista`, `/logica` o `/scripts` pueden ser minificados u ofuscados en producción para:

- Reducir el tamaño de distribución
- Dificultar la ingeniería inversa
- Ocultar lógica crítica de negocio

Esto aplica especialmente en contextos de WebView, navegadores, o dispositivos compartidos.

### 🧱 Protección de carpetas y rutas

Las carpetas sensibles pueden y deben estar protegidas mediante:

- Permisos de sistema de archivos (Windows, Linux, Android)
- Reglas de acceso en contenedores o sandbox
- Protección por dominio o subdominio en servidores web
- Configuración de rutas seguras en apps embebidas
- Autenticación y control de sesiones si se publica remotamente

La arquitectura BranchNow es compatible con todas estas estrategias. Se recomienda configurar entornos de publicación y clientes con reglas de seguridad adaptadas al caso de uso.

---

## 🧠 Cierre

BranchNow representa una nueva forma de pensar el desarrollo distribuido. No reemplaza a Git, ni a las bases de datos, ni a los servidores REST. **Los libera.**

> Si el software moderno es modular, declarativo y descentralizado, entonces su arquitectura también debe serlo.

---

## ✉️ Autoría

Este manifiesto y la arquitectura BranchNow fueron creados y redactados por:

**Gustavo Meléndez Villarreal**

Publicación original: 16 de abril de 2025

Todos los derechos reservados. El autor podrá habilitar canales oficiales de contacto o licenciamiento en futuras versiones públicas.

---

## ⚖️ Nota legal final

BranchNow es una obra intelectual registrada como modelo arquitectónico, publicada por Gustavo Meléndez Villarreal.Este manifiesto, su estructura propuesta, nomenclatura, organización modular, flujo de trabajo y representación escrita están protegidos por derechos de autor.

El autor no limita el pensamiento libre, la inspiración ni el uso general de ideas como modularidad, scripting o control de versiones.Sin embargo, **el uso estructurado, documentado o comercial de la arquitectura BranchNow tal como está publicada en este manifiesto, requiere seguir las condiciones expresadas en este documento y, si aplica, establecer un acuerdo de licencia.**

BranchNow es libre para el aprendizaje, la evolución del pensamiento arquitectónico y la práctica comunitaria, pero no puede utilizarse con fines de lucro sin reconocimiento y autorización expresa.

---

**Bienvenido a BranchNow.**

> *"From source to state. From branch to now."*
> *(Del código al estado. De la rama... al ahora.)*

> Gracias.