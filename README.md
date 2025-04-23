# 🤖 Unreal-IA: Inteligencia Artificial en Unreal Engine 5

🚀 **Unreal-IA** es un proyecto educativo diseñado para enseñarte a implementar **IA en Unreal Engine** utilizando herramientas como **Controladores, Behavior Trees, Blackboards, Tasks, EQS, Smart Objects y Animaciones**.

## 📌 Sistemas implementados

### ✅ Sistema 1: Peatones inteligentes con semáforo
- 🚦 **Rojo**: El peatón espera antes de cruzar.
- 🚦 **Verde**: El peatón avanza y cruza la calle.

### ✅ Sistema 2: IA Buscadora de Piedra
- 🔍 La IA localiza una piedra en el entorno (una sola en escena).
- 🌄 Se mueve hasta ella usando `AI MoveTo`.
- 🧠 Usa un **Smart Object** para ejecutar una animación (ej. recoger piedra):
  - Filtra Smart Objects por **Gameplay Tag** (`SOC.standInteraction`).
  - Si encuentra uno válido, guarda el `ClaimHandle` y `TargetLocation` en el Blackboard.
  - Luego ejecuta `BTTask_UseSmartObject`, que reproduce la animación definida.
- 🪨 Al terminar, se marca `HasRock = true` en el Blackboard.

✨ Además, se implementó **EQS (Environment Query System)** para seleccionar ubicaciones óptimas en el entorno.

🧊 Lógica adicional tipo **Weeping Angel**:
- La IA solo se mueve cuando el jugador **no la mira**.
- Si el jugador la mira, se activa `BTTask_DetenerNPC` que detiene su movimiento.
- Controlado mediante un **Selector** y un **Blackboard Decorator** (`PuedeMoverse`).

> 🔧 Todo el sistema fue construido **exclusivamente con Blueprints**.

---

## 🎯 Objetivos

- ✅ Aprender sobre `AIController` y cómo manejar NPCs.
- ✅ Definir comportamientos con `Behavior Trees`.
- ✅ Usar `Blackboards` para almacenar datos del entorno.
- ✅ Implementar `BTTasks` personalizadas:
  - `BTTask_FindRock`: Encuentra la piedra.
  - `BTTask_MoveToRock`: Se mueve hacia ella.
  - `BTTask_PickUpRock`: Usa un Smart Object para recogerla.
  - `BTTask_UseSmartObject`: Ejecuta la animación definida.
  - `BTTask_DetenerNPC`: Detiene al NPC si el jugador lo observa.
- ✅ Utilizar `EQS` para tomar decisiones según el entorno.
- ✅ Ejecutar animaciones contextuales usando Smart Objects.

---

## 🛠️ Tecnologías y Herramientas Utilizadas

| Herramienta              | Descripción                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| 🎮 Unreal Engine 5       | Motor de desarrollo principal.                                              |
| 🧠 AI Controller          | Controlador de comportamiento para NPCs.                                   |
| 🌳 Behavior Trees        | Árbol de decisiones.                                                        |
| 📌 Blackboard             | Memoria compartida para tareas de IA.                                      |
| 🔄 BTTasks                | Acciones personalizadas definidas en Blueprint.                            |
| 🧭 EQS                    | Sistema de consultas del entorno.                                           |
| 🧊 Smart Objects          | Objetos interactivos con lógica modular (animaciones, interacciones, etc). |
| 🕵️ Weeping Angel Logic   | Detención de IA cuando es observada.                                        |
| 🏃 Animaciones            | Mejoran el realismo durante las interacciones.                             |

---

## 💻 Requisitos del Sistema

### Software necesario
- ✅ Unreal Engine 5 (última versión estable recomendada)
- ✅ Git (para clonar el repositorio)
- 🔧 Visual Studio 2022 (opcional, si se quiere usar C++)

### Especificaciones mínimas
- CPU: Intel i5-8400 / AMD Ryzen 5 2600
- RAM: 16 GB
- GPU: NVIDIA GTX 1060 / AMD RX 580
- Disco: 20 GB libres
- OS: Windows 10/11 (64-bit)

---

## 🧪 ¿Cómo funciona cada sistema?

### ⚡ Sistema de Peatones
1. El NPC selecciona un destino.
2. Consulta el estado del semáforo.
3. Si está en rojo, espera. Si está en verde, cruza.
4. Repite el ciclo.

### 🧠 Sistema de Buscadora de Piedra + Lógica de Weeping Angel
1. `BTTask_FindRock` guarda la referencia de la piedra.
2. Si `PuedeMoverse == true`, ejecuta `BTTask_MoveToRock`; si no, se detiene con `BTTask_DetenerNPC`.
3. Al llegar, ejecuta `BTTask_PickUpRock`, que:
   - Usa un `Smart Object` para animar la recolección.
   - Marca `HasRock = true`.

Todo el flujo se gestiona en Blueprint con soporte de EQS y decoradores condicionales.

---

## 🚀 Cómo ejecutar el proyecto

1. Clona el repositorio:
```bash
git clone https://github.com/TIvancelot9/Unreal-IA.git
