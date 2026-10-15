# n8n_brechacambiaria
# 💵 Monitoreo de Brecha Cambiaria (Oficial vs. MEP) con n8n

Automatiza el seguimiento de las cotizaciones del dólar oficial y el dólar MEP en Argentina, calcula la brecha porcentual entre ambos y envía alertas inteligentes a Telegram cuando el spread cumple con la condición establecida.

---

## 🛠️ Stack Tecnológico
* **n8n:** Motor de automatización y orquestación de flujos[cite: 1].
* **DolarAPI:** API pública para la obtención de cotizaciones financieras en tiempo real[cite: 1].
* **Telegram:** Canal de mensajería para alertas instantáneas[cite: 1].

---


## 🚀 Cómo Usarlo

1. **Importar el Workflow:**
   * Descarga el archivo `My workflow 2.json` de este repositorio.
   * Entra a tu instancia de n8n, haz clic en el menú superior derecho (tres puntos) y selecciona **Import from File**.
2. **Configurar Credenciales de Telegram:**
   * En n8n, crea una nueva credencial de tipo **Telegram API** vinculada a tu bot[cite: 1].
   * Entra al nodo final llamado **Send a text message**, asígnale tu credencial recién creada y completa el campo **Chat ID** con tu identificador personal de Telegram[cite: 1].
3. **Poner en Marcha:**
   * Guarda los cambios, verifica que el temporizador (*Schedule Trigger*) esté configurado a tu preferencia[cite: 1] y cambia el estado del workflow a **Active**.

---

## 💡 Posibles Mejoras Futuras
* **Más referencias:** Añadir llamadas a la API para incluir el Dólar Contado con Liquidación (CCL) o Dólar Cripto.
* **Persistencia histórica:** Conectar una base de datos (como PostgreSQL) o Google Sheets para registrar el comportamiento diario de la brecha.
* **Alertas dinámicas:** Permitir modificar el umbral del nodo condicional (`If`) mediante variables de entorno en lugar de un valor estático[cite: 1].
