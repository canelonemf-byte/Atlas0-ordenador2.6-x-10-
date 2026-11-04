# ORDENADOR HÍBRIDO no binario — alineación documental con Atlas0

Autor: Lázaro López Paz, El Prat de Llobregat, Barcelona, España + asistencia IA.
Licencias: documentos CC BY 4.0; código (`sim/*.py`) MIT (ver `LICENSE` del repo).

## Estado de evidencia (escala E0–E6)
- Nada en esta carpeta es experimento ni medida de hardware. No existe hardware propio.
- `sim/` y `sim/salidas/`: **E2 simulación** con parámetros **supuestos** (`parametros.yaml`).
  - MVM: mejor configuración CIM 10,5 % de error frente a 0,4 % CMOS; ninguna cumple el objetivo ≤1 %.
  - Planificador consciente de error: 8,90e6 pJ frente a 1,87e6 pJ de HEFT (peor que HEFT en esta corrida).
- Propuestas de diseño (planificador, arquitectura): **E0**.
- `registro_evidencia.json`: 29 entradas (E0 12, E1 5, E2 3, E3 2, E4 7; E5–E6 vacías).
- Referencias marcadas en los documentos como PENDIENTE DE VERIFICACIÓN siguen sin verificar.

## Relación con Atlas0
Atlas0 (TQC con aniones de Fibonacci, lógica reversible, Landauer) y este proyecto comparten
únicamente el marco termodinámico de Landauer (ev_01). Esta carpeta no modifica los hitos ni
las afirmaciones de Atlas0.
