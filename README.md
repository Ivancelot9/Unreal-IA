# 🤖 Unreal-IA: Inteligencia Artificial en Unreal Engine 5  

🚀 **Unreal-IA** es un proyecto educativo diseñado para enseñarte a implementar **IA en Unreal Engine** utilizando distintas herramientas como **Controladores, Behavior Trees, Blackboards, Tasks y Animaciones**.  

📍 En este proyecto, se ha desarrollado un **sistema de peatones inteligente** que responde al estado de un semáforo:  
- 🚦 **Rojo**: El peatón **espera** antes de cruzar.  
- 🚦 **Verde**: El peatón **avanza** y cruza la calle.  

⚡ **Actualmente, este proyecto está desarrollado completamente con Blueprints**, por lo que **no requiere código en C++**.  
🔹 **Si deseas agregar código más adelante, puedes usar Visual Studio u otro IDE de tu preferencia.**  

---

## 🎯 **Objetivos**  
✅ Aprender sobre **AI Controllers** y cómo manejan NPCs.  
✅ Usar **Behavior Trees** para definir comportamientos avanzados.  
✅ Integrar **Blackboards** para almacenar información dinámica de los NPCs.  
✅ Implementar **Tasks** personalizadas para modularizar la IA.  
✅ Utilizar **Animaciones** para mejorar la inmersión de los NPCs.  

---

## 🛠️ **Tecnologías y Herramientas Utilizadas**  

| 🛠️ Herramienta | 🚀 Descripción |
|---------------|-------------|
| 🎮 **Unreal Engine 5** | Motor de juego utilizado para desarrollar el proyecto. |
| 🧠 **AI Controller** | Controla el comportamiento de los NPCs. |
| 🌳 **Behavior Trees** | Sistema de árbol de decisiones para la IA. |
| 📌 **Blackboard** | Permite almacenar y gestionar datos para la IA. |
| 🔄 **Tasks** | Implementación de tareas personalizadas para la IA. |
| 🏃 **Animaciones** | Integración de animaciones para mejorar el realismo de los NPCs. |

---

## 📋 **Requisitos del Sistema**  

Antes de ejecutar el proyecto, asegúrate de cumplir con los siguientes requisitos:  

### 🎮 **Software Necesario**  
✅ **Unreal Engine 5** (recomendado: última versión estable).  
✅ **Git** para clonar el repositorio.  

💻 **Opcional (si decides agregar código en C++ en el futuro):**  
✅ **Visual Studio 2022** (o cualquier IDE de tu preferencia) con los módulos de desarrollo para Unreal.  

### 💻 **Especificaciones Mínimas**  
🔹 **Procesador:** Intel i5-8400 / AMD Ryzen 5 2600  
🔹 **RAM:** 16GB  
🔹 **Tarjeta gráfica:** NVIDIA GTX 1060 / AMD RX 580 (o superior)  
🔹 **Espacio en disco:** 20GB disponibles  
🔹 **Sistema Operativo:** Windows 10 / 11 (64 bits)  

---

## 🎬 **¿Cómo funciona el sistema de peatones?** 🚶‍♂️🚦  

1️⃣ **El NPC selecciona un punto aleatorio para caminar.**  
2️⃣ **Si está cerca de un cruce, verifica el semáforo:**  
   - 🚦 Si el semáforo está en **rojo**, **espera**.  
   - 🚦 Si el semáforo está en **verde**, **avanza** y cruza la calle.  
3️⃣ **Una vez cruzado, busca un nuevo destino y repite el ciclo.**  

📌 **Todo esto se maneja con un AI Controller, Behavior Trees y un Blackboard que almacena el estado del semáforo.**  

---

## 📂 **Estructura del Proyecto**  

