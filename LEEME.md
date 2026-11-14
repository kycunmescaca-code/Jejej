# Voz Flotante

Micrófono flotante que graba, sube el tono de la voz, reproduce y comparte el audio a WhatsApp.

## Opción A: compilar con Android Studio (PC)
1. Abre Android Studio → Open → elige la carpeta `VozFlotante`.
2. Espera a que termine la sincronización de Gradle.
3. Conecta tu teléfono con depuración USB y pulsa Run, o usa Build → Build APK(s).
   El APK queda en `app/build/outputs/apk/debug/app-debug.apk`.

## Opción B: compilar en la nube con GitHub (sin PC)
1. Crea un repositorio en GitHub y sube todo el contenido de esta carpeta (incluida `.github`).
2. Ve a la pestaña Actions → "Compilar APK" → Run workflow.
3. Cuando termine (3 a 5 minutos), entra a la ejecución y descarga `VozFlotante-apk`
   (un ZIP que contiene `app-debug.apk`).

## Instalar en el teléfono
1. Copia `app-debug.apk` al teléfono y ábrelo.
2. Android pedirá permitir "instalar apps desconocidas" para el navegador o gestor de archivos que uses.
3. Abre Voz Flotante, concede el permiso de micrófono y "mostrar sobre otras apps", y toca Iniciar.

## Ajustes
- Tono: variable `factor` en `VoiceOverlayService.kt` (1.2 a 1.5; más alto = más agudo).
- WhatsApp Business: cambia `com.whatsapp` por `com.whatsapp.w4b` en `shareToWhatsApp()`.
