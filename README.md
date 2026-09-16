<p align="center">
  <img src="images/logo.png" width="180">
</p>

<h1 align="center"> Arquitectura VLIW para Cifrado de Bloques </h1>

<p align="center">
  Diseño e implementación de una arquitectura VLIW orientada al cifrado de bloques.
</p>

<p align="center">

![VLIW](https://img.shields.io/badge/Architecture-VLIW-blue)
![Language](https://img.shields.io/badge/Language-Verilog-orange)
![Platform](https://img.shields.io/badge/Platform-FPGA-green)

</p>

---

## 📖 Descripción

En este proyecto se desarrollará una Arquitectura VLIW Propia para Aplicaciones de Cifrado por Bloques 
aplicando los conceptos de arquitectura de computadores en el diseño e implementación en SystemVerilog 
de un procesador VLIW con una arquitectura del set de instrucciones (ISA) propia, orientada a la 
aceleración de un algoritmo de cifrado por bloques tipo Feistel.

### Resumen de la arquitectura

| Parámetro     | Valor         |
| ------------- | ------------- |
| Tamaño de intrucción  | 	32 bits  | 
| Tamaño Bundle  | 	160 bits | 
| Cantidad registros generales	 | 16  | 
| Tamaño inmediatos	 |   | 
| Endian  | 	Little  | 

### Registros

| Registers  | Descripcion   | Codificación en decimal | 
| -----------| ------------- | ----------------------- |
| rz | Constante cero cableada. Cualquier lectura retorna 0; escrituras se descartan.                | 0  |
| rl | Enlace de retorno (Return Address). JAL guarda aquí el PC de retorno; E lo usa para volver.   | 1  |
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

---

## 🎯 Objetivos

- Diseñar una arquitectura VLIW.
- Implementar unidades funcionales para operaciones criptográficas.
- Analizar el paralelismo a nivel de instrucción.
- Evaluar el funcionamiento de la arquitectura.
- Validar los resultados obtenidos.

---

## 🎛️ Arquitectura

La arquitectura está compuesta por:

- Unidad de control
- Banco de registros
- Unidades funcionales
- Memoria
- Unidad de cifrado
- Interconexiones entre componentes

### Diagrama

<p align="center">
  <img src="images/arquitectura.png" width="700">
</p>

---

## ⚙️ Tecnologías utilizadas

| Tecnología | Uso |
| --- | --- |
| `Verilog/SystemVerilog` | Diseño hardware |
| `Git/GitHub` | Control de versiones |

---

## 📂 Estructura del proyecto

```text


vliw-block-cipher/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── docs/
│   ├── arquitectura.md
│   ├── diseño.md
│   ├── resultados.md
│   └── images/
│       ├── logo.png
│       ├── arquitectura-vliw.png
│       ├── diagrama-bloques.png
│       ├── simulacion.png
│       └── resultados.png
│
├── src/
│   └── systemverilog/
│       ├── top/
│       │   └── vliw_top.sv
│       │
│       ├── processor/
│       │   ├── control_unit.sv
│       │   ├── decoder.sv
│       │   ├── register_file.sv
│       │   └── alu.sv
│       │
│       ├── crypto/
│       │   ├── cipher_core.sv
│       │   ├── sbox.sv
│       │   └── ...
│       │
│       ├── memory/
│       │   ├── instruction_memory.sv
│       │   └── data_memory.sv
│       │
│       └── common/
│           ├── mux.sv
│           └── ...
│
├── simulations/
│   ├── icarus/
│   │   ├── testbench/
│   │   │   ├── tb_vliw_top.sv
│   │   │   ├── tb_alu.sv
│   │   │   └── tb_crypto.sv
│   │   │
│   │   ├── scripts/
│   │   │   ├── run.sh
│   │   │   └── Makefile
│   │   │
│   │   └── results/
│   │       ├── waveforms/
│   │       └── screenshots/
│   │
```

---

## 🚀 Instalación

Clona el repositorio:

```bash
git clone https://github.com/tati2327/vliw-block-cipher.git
```

---

## ▶️ Ejecución

Describe aquí los pasos necesarios para compilar,
simular o ejecutar el proyecto.

```bash
# Ejemplo
comando-de-ejecucion
```

---

## 🧪 Pruebas

Las pruebas permiten verificar el funcionamiento de la arquitectura
y comparar los resultados obtenidos con los valores esperados.

### Ejemplo

| Entrada | Resultado esperado | Resultado obtenido |
|---|---|---|
| `0x1234` | `0xABCD` | `0xABCD` |
| `0x5678` | `0xEF01` | `0xEF01` |

---

## 📊 Resultados

<p align="center">
  <img src="images/resultados.png" width="700">
</p>

Los resultados obtenidos muestran el comportamiento de la arquitectura
durante la ejecución del algoritmo de cifrado.

---

## 📚 Referencias

- 

---

<p align="center">
  ⭐ Proyecto académico de Arquitectura de Computadores ⭐
</p>

---










