# ElectroCenso Pro — Proyecto Listo para Compilar APK en GitHub

Este paquete contiene toda la estructura de **Capacitor + GitHub Actions** configurada para compilar automáticamente el instalador `.apk` de Android en la nube sin necesidad de instalar Android Studio en tu computadora o teléfono.

## Estructura del Proyecto
- `www/index.html`: Aplicación completa autocontenida con base de datos local, validación de contratos (`10000` + 7 dígitos y `K000` + 9 dígitos), cálculo técnico de `kWh`, `kVA`, acometida/protecciones y puente nativo de exportación/compartición de PDF.
- `package.json` y `capacitor.config.json`: Configuración nativa de Capacitor 6 con plugins `@capacitor/filesystem` y `@capacitor/share` para adjuntar el reporte PDF directamente en WhatsApp o Correo dentro de Android.
- `.github/workflows/build-apk.yml`: Flujo de integración continua (CI) que descarga Node 20, Java 17 y Android SDK, genera el proyecto nativo y compila el archivo `app-debug.apk`.

## Pasos para Obtener tu APK en GitHub
1. Crea un repositorio nuevo en tu cuenta de **GitHub** (público o privado).
2. Sube todos los archivos de este ZIP respetando las carpetas (especialmente `.github/workflows/build-apk.yml` y `www/index.html`).
3. Ve a la pestaña **Actions** en tu repositorio de GitHub.
4. Verás ejecutándose el flujo **Compilar APK Android (ElectroCenso Pro)** (o puedes iniciarlo manualmente con **Run workflow**).
5. Al finalizar (tarda ~2-3 minutos), entra en la ejecución completada y descarga el artefacto **ElectroCenso-Pro-APK**, que contiene el archivo `app-debug.apk` listo para instalar en tu teléfono Android.
