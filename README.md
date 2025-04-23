# 🌿 Monitor de Calidad del Aire IoT 📡

Bienvenido al repositorio oficial del **Sistema de Monitorización de Calidad del Aire**. Este proyecto combina tecnologías **IoT**, **sensores ambientales** y **modelos de machine learning** para monitorear, analizar y predecir la contaminación del aire en tiempo real. Diseñado para ser **modular, de bajo costo y energéticamente eficiente**, este sistema busca aportar a la salud pública y la sostenibilidad ambiental. 🌎💚

---

## 🧠 ¿Qué hace este sistema?

🔬 **Mide** contaminantes como:
- Material particulado (PM1.0, PM2.5, PM10) 🌫️
- Gases como CO, NO₂ y NH₃ 🧪
- Temperatura, humedad, presión y compuestos orgánicos volátiles (VOC) 🌡️💧

📶 **Procesa y envía** los datos desde un módulo IoT (ESP32 + SIM800L) a un servidor central vía red **2G/GPRS**.

📊 **Analiza** los datos con modelos ML como:
- **ARIMA/SARIMAX** & **XGBoost Regressor** para predicción de contaminantes ⏱️📈
- **Isolation Forest** para detectar anomalías ❗
- **K-Means/DBSCAN** para clustering geoespacial de zonas 🌍

🖥️ **Visualiza** la información en una plataforma web interactiva y una app móvil con mapas, gráficos y alertas en tiempo real 🔔📱

---

## 🧩 Arquitectura General

```
Sensores → ESP32 → SIM800L → Servidor central → ML + API → Web/App
```

### Componentes Clave:
- 📟 **ESP32-WROOM-32** – Controlador principal del sistema
- 📡 **SIM800L** – Transmisión de datos vía GSM/GPRS
- 🌬️ **PMS5003** – Sensor de partículas
- 🧪 **MiCS-6814** – Sensor de gases
- 🌡️ **BME680** – Sensor de temperatura, humedad, presión y VOC
- 🔋 Alimentado por panel solar + batería 🔆🔋

---

## ⚙️ Ciclo de Operación

1. 🌞 **Despierta cada 5 min**
2. 📈 **Recolecta datos**
3. 🧠 **Procesa y estandariza**
4. 🌐 **Transmite al servidor**
5. 😴 **Vuelve a dormir para ahorrar energía**

---

## 🚀 Tecnologías Usadas

- **Hardware:** ESP32, PMS5003, MiCS-6814, BME680, SIM800L
- **Protocolos:** UART, I2C, ADC, HTTP, MQTT
- **ML:** XGBoost, ARIMA/SARIMAX, Isolation Forest, DBSCAN, K-Means
- **Backend:** InfluxDB / PostgreSQL, Python, API REST
- **Frontend:** Web App y Aplicación Móvil (React/Vue/Flutter compatible)

---

## ❤️ Impacto

> En Colombia, más de **15.600 muertes al año** están relacionadas con la mala calidad del aire. Este sistema busca **democratizar el monitoreo ambiental**, permitiendo despliegues en zonas rurales y urbanas, y brindando datos valiosos a ciudadanos, autoridades e investigadores. 📡🌳

---

## 👨‍💻 ¿Quieres contribuir?

¡Toda ayuda es bienvenida! Ya sea en hardware, firmware, visualización o ciencia de datos. Puedes abrir un issue o hacer un pull request 🤝✨

---

## 📬 Contacto

Para dudas o colaboración, no dudes en escribirnos. Estamos construyendo un futuro más limpio y saludable, ¡un sensor a la vez! 🌎📈