#  Agente Autónomo de Email con n8n y OpenAI

Solución de automatización de extremo a extremo diseñada para la gestión inteligente de consultas por correo electrónico en tiempo real. 

El sistema intercepta mensajes vía Gmail API, analiza la intención de la consulta utilizando **GPT-4o-mini**, mantiene contexto conversacional y responde de forma autónoma con información personalizada.

---

##  Tech Stack & Herramientas

* **Orquestador:** n8n
* **Modelo LLM:** OpenAI GPT-4o-mini (vía AI Agent Node)
* **Memoria:** Simple Memory Node (Persistencia de contexto)
* **Integraciones:** Gmail API (Trigger y Send Message)

---

##  Características Técnicas

* **Payload Mapping Dinámico:** Mapeo de variables (`={{ $json.message.from }}`) para garantizar la entrega directa al remitente.
* **Memoria Conversacional:** Mantiene el hilo de mensajes anteriores para responder dudas de seguimiento.
* **Procesamiento de PLN:** Generación de respuestas adaptadas a consultas sobre inventario, precios y stock.

---

##  Cómo importar este proyecto

1. Descarga el archivo `n8n-ai-email-agent.json` de este repositorio.
2. En tu instancia de n8n, crea un nuevo workflow y selecciona **Import from File**.
3. Configura tus credenciales de **Gmail OAuth2** y la API Key de **OpenAI**.
4. Presiona **Execute Workflow** para activar la escucha del flujo.
