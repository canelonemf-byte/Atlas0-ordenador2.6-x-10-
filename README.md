# Atlas0 (ordenador 2.6 × 10)

**Autor:** Lázaro López Paz, El Prat de Llobregat, Barcelona, España, con asistencia de inteligencia artificial.
**ORCID:** [0000-0001-8601-1963](https://orcid.org/0000-0001-8601-1963)
**Licencia:** software MIT (ver `LICENSE`); documentos CC BY 4.0.
**Nivel de evidencia:** E1 (diseño/propuesta con demos mínimas de software). Sin hardware, sin experimento, sin resultados físicos.

## Qué contiene realmente este repositorio

| Ruta | Contenido | Estado verificado (2026-10-30) |
|---|---|---|
| `src/tqc_demo.py` | Demo numérica de "braiding" de anyones de Fibonacci; imprime fidelidad y coherencia de juguete | Se ejecuta; valores de un modelo simplificado, no de un sistema cuántico |
| `src/rewind_demo.rs`, `tests/rewind/` | Puerta Toffoli y límite de Landauer kT·ln2 a 300 K | `cargo test` en `tests/rewind` |
| `lean/Atlas0.lean` | Andamiaje Lean 4 (constante de Boltzmann y lema de no negatividad de Landauer) | Requiere toolchain Lean/elan; no se valida en CI sin Lean |
| `docs/atlas0.{md,tex,bib}`, `docs/atlas0_phase2.md` | Borrador de dossier y notas de Fase 2 | Borrador E1; sin DOI de Zenodo |
| `scripts/sprint_01_manifest.json` | Plan del sprint 01 | Plan, no resultado |
| `Makefile` | Objetivos `check-deps`, `install-*`, `phase2-check`, `test-all`, `lean-check` | Requiere Python 3 y Rust |
| `LICENSE` | MIT | — |

## Qué NO hay todavía

- Compilación topológica cuántica real ni hardware: la demo TQC es una simulación de juguete.
- Prueba formal en Lean comprobada en este entorno.
- Resultados físicos, benchmarks experimentales o publicación con DOI.
- El presupuesto y el calendario del manifiesto son del plan; su ejecución está pendiente de verificación.

## Uso

```bash
python3 src/tqc_demo.py --time 0.8 --tau 2.5 --snr 3.0 --angle 1.25663706
cargo test --manifest-path tests/rewind/Cargo.toml
make phase2-check   # requiere Rust y Python
make lean-check     # opcional; omite si no hay elan/Lean
```

## Autoría

Lázaro López Paz, El Prat de Llobregat, Barcelona, España.
ORCID: 0000-0001-8601-1963.
Trabajo con asistencia de inteligencia artificial. Sin afiliaciones institucionales.

## Referencias de terceros

- Landauer, R. (1961). Irreversibility and Heat Generation in the Computing Process. IBM J. Res. Dev. 5(3).
- Kitaev, A. Yu. (2003). Fault-tolerant quantum computation by anyons. Annals of Physics 303(1).
- Toffoli, T. (1980). Reversible computing.
