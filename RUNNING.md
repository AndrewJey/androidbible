# Compilar y probar este fork

Este repositorio personal integra `develop` de [yukuku/androidbible](https://github.com/yukuku/androidbible). Se conservan la licencia original y las correcciones Python previas de los procesadores de publicaciones.

## Android Studio y Windows

Abre la raíz como proyecto Gradle. Usa JDK 21 para Gradle y configura `ANDROID_HOME` o un `local.properties` local con `sdk.dir`. Consulta los SDK y NDK requeridos en [gradle/libs.versions.toml](gradle/libs.versions.toml), y el wrapper para Gradle. Snappy requiere el NDK incluso en la variante abierta.

```powershell
.\gradlew.bat assemblePlainDebug
.\gradlew.bat testPlainDebugUnitTest
.\gradlew.bat lintPlainDebug
```

Selecciona `plainDebug` en Android Studio. Las APK se generan en `Alkitab/build/outputs/apk/plain/debug/`. Se pueden instalar desde Android Studio o mediante `adb install -r <apk>` en un dispositivo de prueba compatible.

La variante `plain` utiliza contenido bíblico y configuración Firebase de ejemplo. Permite desarrollar la aplicación sin acceso al repositorio propietario; las funciones que necesitan servicios externos requieren su configuración real. No equivale a una edición de producción con todos sus datos y servicios. No agregues archivos de credenciales, claves ni el overlay propietario al fork.

Las instrucciones completas del original están en [docs/build-environment.md](docs/build-environment.md), [docs/build-system.md](docs/build-system.md) y [AGENTS.md](AGENTS.md). La compilación local usa el wrapper, sin sustituir las versiones fijadas por una instalación global.

## Actualizaciones futuras

`origin` corresponde al fork personal y `upstream` al original. El push a `upstream` está deshabilitado localmente. Integra `upstream/develop` en una rama de trabajo y valida `plainDebug` antes de actualizar la rama personal. Los procesadores de `publication/` son herramientas independientes; compilación Android no significa que todos sus formatos o proveedores se hayan probado.

## Datos internos y pruebas en Windows

Los archivos de `Alkitab/src/plain/assets/internal/` contienen índices de bytes. `.gitattributes` conserva sus bytes originales, incluidos los archivos con extensión `.txt`; convertirlos a CRLF rompe la lectura de capítulos. No los reformatees con un editor. Las pruebas usan SQLite nativo para evitar conexiones simuladas inválidas del modo antiguo en Windows.
