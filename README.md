📡 Radar ADSB - Localizador de Aviones con ESP32-S3

Este proyecto utiliza un ESP32-S3 y una pantalla TFT ILI9341 de 2.4" para rastrear y visualizar en tiempo real los aviones más cercanos a tu ubicación utilizando la API de OpenSky Network.

🚀 Características Principales
Modo Dual de Visualización: alterna entre una lista detallada del avión más cercano y una vista de radar gráfica.
Zoom Dinámico: El radar ajusta su escala automáticamente (entre 10km y 250km) para mostrar los aviones con el mejor detalle posible.
Información Detallada: Muestra Callsign (vuelo), país, distancia, altitud, velocidad, rumbo y estado (en vuelo/pista).
Indicador de Tendencia: Flechas dinámicas que indican si el avión está ascendiendo o descendiendo.

🛠️ Hardware Necesario
Microcontrolador: ESP32-S3 DevKit (N16R8).
Pantalla: TFT 2.4" SPI ILI9341 (320x240).
Caja Impresa en 3D: Diseño disponible en MakerWorld

🔌 Conexión (Pines ESP32-S3)
<img width="492" height="464" alt="Captura de pantalla 2026-04-04 150750" src="https://github.com/user-attachments/assets/dfd985e3-7a16-4579-9320-cab3ac2bd5ff" />

⚙️ Configuración del Software
Antes de subir el código a tu ESP32, asegúrate de modificar las siguientes líneas en el archivo .ino:
WiFi: Introduce el nombre y clave de tu red.
const char* ssid = "Tu_Nombre_WiFi";
const char* password = "Tu_Clave_Wifi";


API OpenSky: Regístrate en OpenSky Network para obtener tus credenciales.
const char* apiUser = "Tu_Usuario_API";
const char* apiPass = "Tu_Contraseña_API";


Ubicación: Coloca las coordenadas de donde te encuentras.
float myLat = 13.726434; // Tu Latitud
float myLon = -98.23483; // Tu Longitud
float maxDist = 250;      // Rango máximo en KM


📚 Librerías Requeridas
Para compilar este proyecto necesitarás instalar las siguientes librerías desde el Gestor de Librerías de Arduino:
Adafruit GFX Library
Adafruit ILI9341
ArduinoJson (v6 o superior)
Nota: Este proyecto es para fines educativos y de hobby. La precisión de los datos depende enteramente de la API de OpenSky.

![1775165252482](https://github.com/user-attachments/assets/1207ecf6-a79d-4297-89da-beba4f4cc232)
![WhatsApp Image 2026-04-04 at 3 01 33 PM](https://github.com/user-attachments/assets/9239f7b3-ac9a-4865-b40f-597752120dc4)
![1775165252517](https://github.com/user-attachments/assets/ae604067-aba0-4d07-b601-85584b8950b3)
![1775165252638](https://github.com/user-attachments/assets/fd993239-2f18-4576-bfa9-af636feb23a3)
[README del Proyecto (1).pdf](https://github.com/user-attachments/files/26484684/README.del.Proyecto.1.pdf)
