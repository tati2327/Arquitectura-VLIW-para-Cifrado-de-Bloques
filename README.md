# Arquitectura-VLIW-para-Cifrado-de-Bloques
Se desarrollará una Arquitectura VLIW Propia para Aplicaciones de Cifrado por Bloques aplicando los conceptos de arquitectura de computadores en el diseño e implementación en SystemVerilog de un procesador VLIW con una arquitectura del set de instrucciones (ISA) propia, orientada a la aceleración de un algoritmo de cifrado por bloques tipo Feistel.

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

| Registers  | Descripcion: | Codificación en decimal | 
| rz | Constante cero cableada. Cualquier lectura retorna 0; escrituras se descartan.  | 0  |
| rl | Enlace de retorno (Return Address). JAL guarda aquí el PC de retorno; E lo usa para volver.   | 1 |
| rx |  General  | 2  |
| rg | Puntero global. Base para variables de módulo y tablas de saltos en Calser.| 3 |
| ra | Argumento 0 | 4  |
| rb |  Argumento 1 | 5 |
| rc |  Argumento 2 | 6 |
| rd |  Argumento 3 | 7 |
| ri | Iterador de ciclo I. Optimizado para la variable de control en ciclos S y L | 8 |
| rj | Iterador de ciclo J. Cálculo de índices de columnas en arreglos bidimensionales | 9 |
| rk | Buffer de llaves / Crypto. Registro de staging para cargar palabras hacia la Bóveda con KV_LOAD | 10  |
| re | Temporal de evaluación de expresiones. Cálculo intermedio de operaciones aritméticas. | 11 |
| rf | Registro dedicado de condición/flags para ifmov y resultado de slt | 12 |
| rh | Temporal general y cálculo de direcciones intermedias. | 13  |
| rs | Registro preservado (callee-saved). | 14 |
| rt | Registro preservado (callee-saved). | 15 |



