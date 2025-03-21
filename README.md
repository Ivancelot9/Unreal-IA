# 🤖 Unreal-IA: Inteligencia Artificial en Unreal Engine 5  

🚀 **Unreal-IA** es un proyecto educativo diseñado para enseñarte a implementar **IA en Unreal Engine** utilizando distintas herramientas como **Controladores, Behavior Trees, Blackboards, Tasks, EQS y Animaciones**.  

📍 En este proyecto, se han desarrollado dos sistemas diferentes de IA:  

### ✅ Sistema 1: **Peatones inteligentes con semáforo**  
- 🚦 **Rojo**: El peatón **espera** antes de cruzar.  
- 🚦 **Verde**: El peatón **avanza** y cruza la calle.  

### ✅ Sistema 2: **IA Buscadora de Piedra**  
- 🔍 La IA **localiza una piedra en el entorno** (solo una disponible en la escena).  
- 🌄 Se **mueve hasta ella** usando `AI MoveTo`.  
- 🪨 (Opcional) La IA **recoge la piedra** y se marca una condición en Blackboard (`HasRock = true`).  

✨ Además, se integró el sistema **EQS (Environment Query System)** para permitir que la IA seleccione ubicaciones óptimas en el entorno al tomar decisiones dinámicas basadas en el escenario.  

Todo el sistema está construido con **Blueprints**, sin necesidad de usar C++.  

---

## 🎯 **Objetivos**  
✅ Aprender sobre **AI Controllers** y cómo manejan NPCs.  
✅ Usar **Behavior Trees** para definir comportamientos avanzados.  
✅ Integrar **Blackboards** para almacenar información dinámica.  
✅ Implementar **Tasks personalizadas** (BTTasks) como:  
   - `BTTask_FindRock`: Encuentra la piedra y la guarda en Blackboard.  
   - `BTTask_MoveToRock`: Se mueve a la piedra.  
   - `BTTask_PickUpRock` (opcional): La oculta y marca que fue recogida.  
✅ Utilizar **EQS (Environment Query System)** para que la IA evalúe el entorno al tomar decisiones.  
✅ Utilizar **Animaciones** para mejorar la inmersión.  

---

## 🛠️ Tecnologías y Herramientas Utilizadas

| 🛠️ Herramienta | 🚀 Descripción |
|---------------|-------------|
| 🎮 **Unreal Engine 5** | Motor de juego utilizado para desarrollar el proyecto. |
| 🧠 **AI Controller** | Controla el comportamiento de los NPCs. |
| 🌳 **Behavior Trees** | Sistema de árbol de decisiones para la IA. |
| 📌 **Blackboard** | Permite almacenar y gestionar datos para la IA. |
| 🔄 **BTTasks** | Tareas personalizadas en Blueprint que definen acciones de IA. |
| 🧭 **EQS (Environment Query System)** | Sistema para que la IA consulte el entorno y tome decisiones según ubicaciones óptimas. |
| 🏃 **Animaciones** | Integración de animaciones para mejorar el realismo. |

---

## 📋 Requisitos del Sistema

### 🎮 Software Necesario
✅ **Unreal Engine 5** (recomendado: última versión estable).  
✅ **Git** para clonar el repositorio.  

💻 **Opcional (si decides agregar código en C++ en el futuro):**  
✅ **Visual Studio 2022** con los módulos de desarrollo para Unreal.  

### 💻 Especificaciones Mínimas
- Procesador: Intel i5-8400 / AMD Ryzen 5 2600  
- RAM: 16GB  
- Gráfica: NVIDIA GTX 1060 / AMD RX 580 (o superior)  
- Espacio en disco: 20GB disponibles  
- Sistema Operativo: Windows 10 / 11 (64 bits)  

---

## 🎮 ¿Cómo funciona cada sistema de IA?

### ⚡ Sistema de Peatones
1. El NPC selecciona un destino.
2. Si se encuentra cerca de un cruce, consulta el estado del semáforo.
3. ✈ Si está en rojo, espera. Si está en verde, cruza.
4. Se repite el proceso.

### 🧠 Sistema de Buscadora de Piedra
1. La IA ejecuta `BTTask_FindRock` para guardar la referencia de la piedra en Blackboard.
2. Ejecuta `BTTask_MoveToRock` y se mueve hacia la piedra con `AI MoveTo`.
3. Al llegar, puede ejecutar `BTTask_PickUpRock`, que la oculta y marca `HasRock = true`.

Además, mediante **EQS**, la IA puede seleccionar ubicaciones óptimas para posicionarse o planear rutas en función del entorno.

Todo gestionado con un Behavior Tree y Blackboard completamente hechos en Blueprint.

---

## 🎮 Cómo probar el proyecto

1. Clona el repositorio:
```bash
git clone https://github.com/TIvancelot9/Unreal-IA.git
```

2. Abre el proyecto .uproject en Unreal Engine 5
3. Ejecuta desde el mapa principal
4. Interactúa con los sistemas de IA en acción

---

## 📷 Recursos Entregables
- 📅 Ejecutable (.exe empaquetado)
- 📄 Capturas del sistema en funcionamiento
- 🎥 Video de gameplay
- 📁 Repositorio con el proyecto completo

---

📈 Proyecto creado con fines educativos para demostrar el uso de IA en Unreal Engine 5 utilizando Blueprints ✨
