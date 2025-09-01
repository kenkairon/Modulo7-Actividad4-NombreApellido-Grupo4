# 📊 Informe de Pruebas de Carga con JMeter

## 1. Configuración de la Prueba
- **Usuarios concurrentes (Threads):** 40  
- **Ramp-up Period:** 40 segundos  
- **Loop Count:** 3 ciclos  
- **Total de peticiones realizadas:** 360  
- **Peticiones HTTP probadas:**
  - GET `/posts`
  - GET `/comments`
  - GET `/users`

---

## 2. Resultados Obtenidos

### 📌 Métricas por petición
| Petición         | Muestras | Tiempo Promedio (ms) | Tiempo Máx (ms) | Throughput (req/s) | Error % |
|------------------|----------|----------------------|-----------------|--------------------|---------|
| GET `/posts`     | 120      | 69                   | 317             | ~72.3              | 0.0 %   |
| GET `/comments`  | 120      | 274                  | 1650            | ~403.9             | 0.0 %   |
| GET `/users`     | 120      | 48                   | 334             | ~17.9              | 0.0 %   |
| **TOTAL**        | 360      | 173                  | 1650            | ~467.2             | 0.0 %   |

---

## 3. Análisis de Resultados
- **Tiempo de respuesta promedio:**  
  La API respondió rápido, con un promedio general de ~173 ms. La petición más “pesada” fue `/comments` (~274 ms).  

- **Errores:**  
  No se registraron errores en ninguna de las solicitudes (**Error % = 0.0%**).  

- **Throughput:**  
  Se alcanzó un rendimiento de **~467 peticiones por segundo**, mostrando que la API soporta la carga concurrente de manera eficiente.  

- **Estabilidad:**  
  La API se comportó de manera **estable** bajo esta carga:  
  - Latencias bajas y consistentes.  
  - Ninguna pérdida de solicitudes.  
  - Rendimiento sostenido a lo largo de la prueba.  

---

## 4. Conclusión
La API de **jsonplaceholder.typicode.com** demostró un **buen rendimiento y estabilidad** bajo un escenario de 40 usuarios concurrentes y 360 peticiones totales.  
Esto indica que puede manejar concurrencia moderada sin degradación notable en el tiempo de respuesta ni pérdida de solicitudes.

✅ **La API es estable y confiable en este escenario de carga.**

---
