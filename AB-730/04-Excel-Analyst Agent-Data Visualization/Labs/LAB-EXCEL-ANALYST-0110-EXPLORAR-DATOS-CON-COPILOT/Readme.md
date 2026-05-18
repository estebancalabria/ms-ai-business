# LAB-EXCEL-ANALYST-0110-EXPLORAR-DATOS-CON-COPILOT

## Objetivo
Aprender a explorar y analizar un conjunto de datos sencillo en Excel usando **Microsoft 365 Copilot**, sin necesidad de fórmulas avanzadas ni conocimientos técnicos previos. Al finalizar, el alumno podrá:
- Resumir datos por categoría.  
- Filtrar información específica.  
- Detectar valores atípicos.  
- Crear gráficos básicos con Copilot.  

---

## Requisitos previos
- Cuenta de Microsoft 365 con Copilot habilitado.  
- Acceso a Excel en la web o aplicación de escritorio.  

---

## Paso 1: Ingresar a Microsoft 365
1. Abrir el navegador web.  
2. Ir a [www.microsoft365.com](https://www.microsoft365.com).  
3. Iniciar sesión con tu cuenta de Microsoft 365 (empresa, educación o personal con Copilot habilitado).  
4. Seleccionar **Excel** desde el iniciador de aplicaciones.  

---

## Paso 2: Crear un nuevo archivo de Excel
1. Hacer clic en **Nuevo libro en blanco**.  
2. Guardar el archivo en **OneDrive** (Copilot requiere que el archivo esté en la nube).  
   - Ej: nombre sugerido `Lab_Explorar_Datos_Copilot.xlsx`.  

---

## Paso 3: Ingresar los datos de ejemplo
1. Copiar la siguiente tabla y pegarla en la hoja de Excel:

```text
Producto, Región, Ventas, Clientes, Fecha
A, Norte, 120, 10, 2026-01-01
B, Sur, 85, 8, 2026-01-02
C, Este, 150, 15, 2026-01-03
D, Oeste, 95, 12, 2026-01-04
E, Norte, 130, 11, 2026-01-05
F, Sur, 75, 7, 2026-01-06
G, Este, 160, 16, 2026-01-07
H, Oeste, 90, 9, 2026-01-08
````

2. Seleccionar todo el rango de datos copiado.
3. Ir a **Insertar → Tabla** y confirmar que la opción “Mi tabla tiene encabezados” está marcada.

---

## Paso 4: Abrir Copilot Chat

1. En la barra superior de Excel, buscar y hacer clic en el **botón Copilot**.
2. Se abrirá el **panel Copilot Chat** a la derecha.
3. Familiarizarse con la interfaz:

   * Área para escribir prompts.
   * Panel de resultados con resúmenes y gráficos sugeridos.

---

## Paso 5: Explorar datos con prompts

### 5.1 Resumen básico

* Escribir en Copilot Chat:

  ```
  Resume las ventas totales por región
  ```
* Revisar el resumen generado y verificar que coincida con los datos.

### 5.2 Filtrar información

* Escribir:

  ```
  Muestra los productos con ventas mayores a 100
  ```
* Copilot marcará los productos que cumplen el criterio.

### 5.3 Detectar valores atípicos

* Escribir:

  ```
  ¿Qué productos tuvieron ventas muy bajas o muy altas?
  ```
* Revisar los resultados y tomar nota de los valores atípicos.

---

## Paso 6: Generar un gráfico con Copilot

1. Seleccionar la tabla completa (o los datos que quieras graficar).
2. Escribir en Copilot Chat:

   ```
   Crea un gráfico de barras que muestre las ventas por región
   ```
3. Opcional: refinar el gráfico con prompts adicionales:

   * “Agrega etiquetas a los ejes”
   * “Resalta las tres regiones con más ventas”
   * “Cambia el tipo de gráfico a columnas”

---

## Paso 7: Reflexionar sobre la exploración

* Revisar los insights generados:

  * ¿Qué región tiene más ventas?
  * ¿Qué productos destacan?
  * ¿Hay valores atípicos?
* Anotar observaciones en la hoja de Excel o en un documento separado.

---

## Sugerencias y buenas prácticas

* Escribir prompts claros y específicos para mejores resultados.
* Explorar varias formas de preguntar a Copilot sobre los mismos datos.
* Guardar cambios continuamente en OneDrive para que Copilot pueda trabajar correctamente.
* **Opcional/demo:** mostrar que Copilot puede importar tablas desde la web, pero **no es obligatorio** en este lab.

---

## Conclusión

Al finalizar este laboratorio, el alumno habrá aprendido a:

* Explorar y resumir datos en Excel con Copilot.
* Filtrar información relevante.
* Identificar valores atípicos.
* Crear un gráfico básico para visualizar tendencias.

Este lab sienta la base para labs posteriores de **visualización avanzada, fórmulas y uso del agente Analyst**.

