

<!-- local-development:start -->
# Desarrollo local

Puedes abrir este repositorio en VS Code, Antigravity o Sublime Text. El compilador y los servicios necesarios dependen del componente indicado abajo.

## Python

Crea un entorno por aplicación desde PyCharm o la CLI. Python 3.12 es el punto inicial de compatibilidad; no se presume que todo el código o sus paquetes antiguos ya lo soporten.

```powershell
py -3.12 -m venv .venv
```

No se detectó un archivo requirements. Hay que identificar los imports y declarar las dependencias antes de instalarlas.

## Android / Gradle

Importa en Android Studio la carpeta que contiene `settings.gradle`. Hay que revisar juntos el wrapper, Android Gradle Plugin, JDK y SDK antes de sincronizar. Guarda la ruta del SDK en `local.properties`, ignorado por Git, y configura localmente las claves Maps/Firebase. Esta revisión no acredita todavía un APK válido.

## PHP

Usa un runtime PHP aislado compatible con la aplicación. Ejecuta Composer únicamente en la carpeta con `composer.json`; las aplicaciones Laravel antiguas requieren revisar también PHP y dependencias. Configura las credenciales de base de datos localmente.

## Componentes y validación

Inventario y compilaciones locales del 2026-11-15. Una compilación correcta no acredita todavía interacción, compatibilidad de base de datos, instalador ni despliegue.

| Componente | Tipo / destino | Validación |
| --- | --- | --- |
| [ATree/build.gradle](<ATree/build.gradle>) | gradle | Sin ejecutar |
| [Afw/build.gradle](<Afw/build.gradle>) | gradle | Sin ejecutar |
| [Alkitab/build.gradle](<Alkitab/build.gradle>) | gradle | Sin ejecutar |
| [AlkitabFeedback/build.gradle](<AlkitabFeedback/build.gradle>) | gradle | Sin ejecutar |
| [AlkitabIntegration/build.gradle](<AlkitabIntegration/build.gradle>) | gradle | Sin ejecutar |
| [AlkitabIo/build.gradle](<AlkitabIo/build.gradle>) | gradle | Sin ejecutar |
| [AlkitabModel/build.gradle](<AlkitabModel/build.gradle>) | gradle | Sin ejecutar |
| [AlkitabYes2/build.gradle](<AlkitabYes2/build.gradle>) | gradle | Sin ejecutar |
| [AmbilWarna/build.gradle](<AmbilWarna/build.gradle>) | gradle | Sin ejecutar |
| [BiblePlus/build.gradle](<BiblePlus/build.gradle>) | gradle | Sin ejecutar |
| [BintexReader/build.gradle](<BintexReader/build.gradle>) | gradle | Sin ejecutar |
| [BintexWriter/build.gradle](<BintexWriter/build.gradle>) | gradle | Sin ejecutar |
| [DragSortListView/build.gradle](<DragSortListView/build.gradle>) | gradle | Sin ejecutar |
| [FlowLayout/build.gradle](<FlowLayout/build.gradle>) | gradle | Sin ejecutar |
| [ImportedDesktopVerseUtil/build.gradle](<ImportedDesktopVerseUtil/build.gradle>) | gradle | Sin ejecutar |
| [KpriModel/build.gradle](<KpriModel/build.gradle>) | gradle | Sin ejecutar |
| [Snappy/build.gradle](<Snappy/build.gradle>) | gradle | Sin ejecutar |
| [build.gradle](<build.gradle>) | gradle | Sin ejecutar |
| [extensions/example-imagesharer/app/build.gradle](<extensions/example-imagesharer/app/build.gradle>) | gradle | Sin ejecutar |
| [extensions/example-imagesharer/build.gradle](<extensions/example-imagesharer/build.gradle>) | gradle | Sin ejecutar |
| [extensions/example-imagesharer/settings.gradle](<extensions/example-imagesharer/settings.gradle>) | gradle | Sin ejecutar |
| [settings.gradle](<settings.gradle>) | gradle | Sin ejecutar |

## Archivos ignorados

`.gitignore` excluye credenciales locales, estado del editor y salidas de las herramientas detectadas. No deja de versionar archivos que ya estaban en Git. Los manifiestos, archivos de bloqueo, recursos fuente y scripts de esquema forman parte del código.
<!-- local-development:end -->

<!-- source-findings:start -->
## Hallazgos en los archivos fuente

Hallazgos de inspección estática; deben revisarse aunque otro componente compile.

| Hallazgo | Archivo |
| --- | --- |
| Error de sintaxis Python 3, línea 22 | `publication/prog/en-leb-processor/leb.py` |
| Error de sintaxis Python 3, línea 17 | `publication/prog/zefania-xml/kj2000.py` |
<!-- source-findings:end -->
