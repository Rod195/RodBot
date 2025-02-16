Bot de Trading Automatizado para Criptomonedas
Este repositorio contiene un bot de trading automatizado diseñado para operar en el mercado de criptomonedas utilizando la API de Bybit. El bot está programado en Python y utiliza estrategias basadas en indicadores técnicos como las Bandas de Bollinger y el Índice de Fuerza Relativa (RSI) para tomar decisiones de compra y venta.

Características principales
Estrategia de trading: El bot utiliza una combinación de Bandas de Bollinger y RSI para identificar oportunidades de compra y venta.

Bandas de Bollinger: Detecta condiciones de sobrecompra y sobreventa.

RSI: Confirma las señales de trading generadas por las Bandas de Bollinger.

Gestión de riesgos:

Ajusta el tamaño de la posición en función de un porcentaje de riesgo por operación.

Define niveles de Take Profit y Stop Loss para cada operación.

Incluye un Trailing Stop para asegurar ganancias cuando el mercado se mueve a favor.

Precisión en órdenes:

Calcula automáticamente el tamaño de la posición y los niveles de precios teniendo en cuenta los requisitos de precisión del exchange (tick size, lot size, etc.).

Conexión con Bybit:

Utiliza la API de Bybit para ejecutar órdenes en tiempo real y obtener datos de mercado.

Requisitos
Python 3.7 o superior.

Librerías necesarias:

pybit: Para interactuar con la API de Bybit.

pandas: Para el manejo y análisis de datos.

numpy: Para cálculos numéricos.

decimal: Para manejo preciso de decimales en operaciones financieras.

Instalación
Clona el repositorio:

bash
Copy
git clone https://github.com/tu-usuario/tu-repositorio.git
cd tu-repositorio
Instala las dependencias:

bash
Copy
pip install -r requirements.txt
Configura tus claves de API de Bybit en el archivo bot.py:

python
Copy
api_key = "TU_API_KEY"
api_secret = "TU_API_SECRET"
Ejecuta el bot:

bash
Copy
python bot.py
Estrategia de Trading
El bot opera de la siguiente manera:

Condición de venta:

Si el precio cruza la Banda Superior de Bollinger y el RSI está en sobrecompra (RSI > 70), el bot abre una posición de venta (short).

Condición de compra:

Si el precio cruza la Banda Inferior de Bollinger y el RSI está en sobreventa (RSI < 30), el bot abre una posición de compra (long).

Gestión de la posición:

Define un Take Profit y un Stop Loss para cada operación.

Activa un Trailing Stop para proteger las ganancias.

Parámetros configurables
Símbolo: Par de trading (por defecto: XRPUSDT).

Timeframe: Intervalo de tiempo para los datos históricos (por defecto: 5 minutos).

Cantidad de USDT: Cantidad de dólares a invertir por operación (por defecto: 10 USDT).

Riesgo por operación: Porcentaje de riesgo por operación (por defecto: 1%).

Take Profit y Stop Loss: Porcentajes de Take Profit y Stop Loss (por defecto: 0.2% y 0.4%, respectivamente).

Ejemplo de uso
El bot se ejecuta en un bucle infinito, monitoreando el mercado y realizando operaciones automáticamente. Los mensajes de las operaciones y errores se imprimen en la consola.

Advertencia
Este bot es una herramienta educativa y experimental. Úsalo bajo tu propio riesgo.

El trading de criptomonedas es altamente volátil y puede resultar en pérdidas significativas.

Asegúrate de probar el bot en un entorno de pruebas (testnet) antes de usarlo con fondos reales.

Contribuciones
¡Las contribuciones son bienvenidas! Si tienes ideas para mejorar el bot, abre un issue o envía un pull request.

Licencia
Este proyecto está bajo la licencia MIT. Consulta el archivo LICENSE para más detalles.

Enlace al repositorio
GitHub
