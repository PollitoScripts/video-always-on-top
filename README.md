# video-always-on-top # 📺 Universal Picture-in-Picture Bookmarklet

Una herramienta ultra ligera (Bookmarklet) que permite activar el modo **Picture-in-Picture (PiP)** en prácticamente cualquier vídeo de internet, permitiéndote moverlo, redimensionarlo y mantenerlo siempre visible en primer plano mientras trabajas en otras pestañas o aplicaciones.

Incluso funciona en plataformas que intentan deshabilitar esta opción de forma nativa.

---

## 🚀 Cómo instalar (Método Rápido)

La forma más fácil de instalarlo es visitando la página web del proyecto:
👉 **[Instalar con un clic aquí](https://PollitoScripts.github.io/video-always-on-top/)** *(Arrastra el botón verde a tu barra de marcadores)*.

### Método Manual:
Si prefieres añadirlo manualmente a tu navegador:
1. Asegúrate de tener visible la **Barra de marcadores** (`Ctrl + Mayús + B` o `Cmd + Shift + B` en Mac).
2. Haz clic derecho en tu barra de marcadores y selecciona **Añadir página** o **Nuevo marcador**.
3. Configúralo con los siguientes datos:
   * **Nombre:** `📺 PiP Flotante`
   * **URL / Dirección:** Copia y pega el siguiente código exacto:

```javascript
javascript:(function(){const v=document.querySelector('video');if(v){v.removeAttribute('disablePictureInPicture');v.disablePictureInPicture=false;v.requestPictureInPicture().catch(()=>{v.play();setTimeout(()=>v.requestPictureInPicture(),100);});}else{alert('Pon el video primero');}})();
```

## 🛠️ Cómo se usa
Entra a cualquier web y reproduce un vídeo (YouTube, Twitch, Netflix, plataformas de cursos, etc.).

Haz clic en el marcador 📺 PiP Flotante que guardaste en tu barra.

El vídeo se desprenderá en una ventana flotante que se quedará siempre on-top (al frente) de tu pantalla.

## 🧠 ¿Cómo funciona por dentro?
El script realiza los siguientes pasos de forma segura:

Busca el elemento <video> activo en la página actual.

Elimina cualquier restricción (disablePictureInPicture) que la web haya impuesto.

Solicita al navegador activar el modo nativo Picture-in-Picture.

Si el vídeo estaba pausado y falla la petición, lo reproduce automáticamente y reintenta la acción en 100 milisegundos para asegurar el cambio.


---

Instalarlo toma literalmente 3 segundos:
1. Entra a la web que armé aquí abajo.
2. Arrastra el botón verde a tu barra de marcadores del navegador.
3. ¡Listo! Vas a cualquier video, tocas el marcador y tendrás tu pantalla flotante.

👉 Instálalo directamente desde aquí: https://PollitoScripts.github.io/video-always-on-top/

