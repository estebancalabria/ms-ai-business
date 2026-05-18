# 🧪 Laboratorio — Crear una Tabla Dinámica con Microsoft 365 Copilot

## 🎯 Objetivo

En este laboratorio aprenderás a usar **Microsoft 365 Copilot** en Excel para generar automáticamente una **tabla dinámica** a partir de un conjunto de datos de ventas, incluyendo cómo usar **Edit with Copilot** para modificar directamente el archivo abierto.

---

## 🔧 Requisitos

* Cuenta activa de **Microsoft 365**
* Acceso a **Excel con Copilot habilitado**
* Navegador web actualizado (Edge o Chrome recomendado)

---

## 📝 Datos de ejemplo

Copia este conjunto de datos en un archivo de Excel nuevo (o crea uno en línea):

| Fecha      | Vendedor | Producto | Cantidad | Total Venta |
| ---------- | -------- | -------- | -------- | ----------- |
| 2026-01-01 | Ana      | Laptop   | 3        | 3000        |
| 2026-01-02 | Juan     | Mouse    | 10       | 500         |
| 2026-01-02 | Ana      | Laptop   | 2        | 2000        |
| 2026-01-03 | Juan     | Teclado  | 5        | 750         |
| 2026-01-03 | Ana      | Mouse    | 7        | 350         |

---

## 🚀 Paso a Paso

### 1️⃣ Acceder al portal de Microsoft 365

1. Abre tu navegador y ve a: [www.microsoft365.com](https://www.microsoft365.com)
2. Inicia sesión con tu cuenta de Microsoft 365.
3. Haz clic en **Apps** → selecciona **Excel**.

---

### 2️⃣ Crear o abrir un archivo de Excel

1. Crea un **Libro en blanco**.
2. Copia los datos de ejemplo en la hoja de cálculo.
3. Guarda el archivo con un nombre descriptivo, por ejemplo:

```

Ventas_Copilot.xlsx

```

---

### 3️⃣ Activar Microsoft 365 Copilot

1. En Excel, busca el botón de **Copilot** en la barra superior (o en la barra lateral).
2. Haz clic en él para abrir el panel de Copilot.
3. Para editar directamente el archivo abierto, haz clic en **Herramientas → Edit with Copilot**.  
Esto permitirá que Copilot genere la tabla dinámica directamente en tu archivo actual, sin crear un archivo nuevo.

---

### 4️⃣ Escribir el prompt para la tabla dinámica

1. En el panel de Copilot, escribe el siguiente prompt:

```

Crea una tabla dinámica que muestre la suma de Total Venta por Vendedor y Producto en una nueva hoja.

```

2. Presiona **Enter** o haz clic en **Generar**.

---

### 5️⃣ Revisar y ajustar la tabla dinámica

1. Copilot generará la tabla dinámica directamente en **Sheet2** del archivo abierto.
2. La tabla debería verse así:

| Vendedor | Producto | Suma de Total Venta |
| -------- | -------- | ----------------- |
| Ana      | Laptop   | 5000              |
| Ana      | Mouse    | 350               |
| Juan     | Mouse    | 500               |
| Juan     | Teclado  | 750               |

3. Opcionalmente, puedes pedir a Copilot que **agregue un gráfico automáticamente** basado en esta tabla:

```

Crea un gráfico de columnas basado en la tabla dinámica en Sheet2.

```

4. Si es necesario, también podés ajustar directamente desde Excel:
- Formato de moneda
- Diseño jerárquico (Producto debajo de Vendedor)
- Segmentadores para filtrar Vendedor o Producto

---

### 6️⃣ Guardar y compartir

* Guarda los cambios en el mismo archivo.
* Puedes compartir el archivo con tus colegas directamente desde **OneDrive** para que también vean la tabla dinámica generada por Copilot.

---

## ✅ Resultado esperado

* Una **tabla dinámica** en **Sheet2** que resuma las ventas por **Vendedor y Producto**.
* Opcional: un **gráfico visual** que represente la información de la tabla.
* Comprensión de cómo **Copilot con Edit with Copilot puede automatizar tareas de análisis de datos directamente en el archivo abierto**.

