# Optimización de búsqueda de números primos

## Introducción
El código original calcula números primos entre 1 y 100,000 evaluando divisores desde 2 hasta n-1 para cada número.  
Problema principal: complejidad alta y tiempos de ejecución elevados.

## Optimización
Se aplicaron las siguientes técnicas:

1. **Reducir rango del bucle hasta √n**  
   En la lógica de primalidad, basta verificar divisores hasta la raíz cuadrada.

2. **List comprehensions**  
   Se utilizaron para construir de forma eficiente la colección final de primos desde la criba.

3. **NumPy**  
   Se implementó una criba de Eratóstenes usando arrays booleanos y operaciones vectorizadas, reduciendo drásticamente el tiempo.

## Resultados
- Se comparó tiempo del código original vs optimizado.
- Se ejecutó `cProfile` sobre la versión optimizada y se guardó en `profiling_optimizado.txt`.
- Se identificaron funciones críticas por tiempo acumulado.
- Se generaron gráficos:
  - `distribucion_tiempos.png`
  - `comparativa_tiempos.png`

## Conclusiones
La versión optimizada mejora significativamente el rendimiento gracias a:
- menor número de iteraciones,
- operaciones vectorizadas con NumPy,
- mejor estructura algorítmica (criba).

### Recomendaciones futuras
- Evitar algoritmos O(n²) en rangos grandes.
- Usar profiling desde etapas tempranas.
- Documentar métricas de rendimiento en cada cambio relevante.