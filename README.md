# ISR401-PFC-ERS-EquipoJ — CarniCore

**Asignatura:** Ingeniería de Requisitos [ISR-401] · UTEQ  
**Período:** 2026-2027 PPA · Unidad IV, Semana 14  
**Sistema PFC:** CarniCore — Sistema de Trazabilidad, Pesaje Inteligente e Inventario para Distribuidora de Cárnicos Pucayacu  

---

## Equipo

| Integrante | Rol en la inspección |
|-------------|----------------------|
| AMAGUA SACON ROBYN WILLIAN | Moderador / Inspector 3 |
| CRESPO ESPINOZA KLEBER OBED | Lector |
| GAMARRA ARAUJO EDHU XAVIER | Inspector 1 |
| PONCE RIVERA MERY HELENMEY | Inspector 2 |
---

## Estructura del repositorio

```
ISR401-PFC-ERS-EquipoJ/
├── README.md                          ← este archivo
├── CHANGELOG.md                       ← historial de versiones del ERS
├── 01_ERS/
│   ├── ERS_v1.0.pdf                   ← versión baseline pre-inspección
│   ├── ERS_v1.1.pdf                   ← versión corregida post-CCB
│   └── fuentes/                       ← archivos .tex fuente del ERS
├── 02_Inspeccion/
│   ├── AnexoA_checklists/
│   │   ├── checklist_inspector1_GAMARRA.pdf
│   │   ├── checklist_inspector2_PONCE.pdf
│   │   └── checklist_inspector3_AMAGUA.pdf
│   ├── AnexoB_registro_defectos.xlsx  ← 17 defectos D-01 a D-17
│   └── metricas.xlsx                  ← métricas + datos de gráficos
├── 03_CCB/
│   ├── RFC-01.pdf
│   ├── RFC-02.pdf
│   ├── RFC-03.pdf
│   └── Acta_CCB.pdf
├── 04_Trazabilidad/
│   ├── matriz_trazabilidad.xlsx       ← 24 issues CARN-01..CARN-24
│   ├── backlog_export.csv             ← exportación real desde Jira
│   └── capturas/  
├── 05_Informe/
│   ├── PE4_U4_AMAGUA_CRESPO_GAMARRA_PONCE.tex
│   ├── references.bib
│   └── PE4_U4_AMAGUA_CRESPO_GAMARRA_PONCE.pdf
└── 06_Evidencias/
    ├── capturas_git/
    │   ├── git_log_graph.png          
    │   └── git_tag.png                
    ├── fotos_sesion/                  
    └── declaracion_IA.pdf
```

---

## Compilar el informe (Overleaf o local)

### Overleaf (recomendado)
1. Crear nuevo proyecto → **Subir proyecto** → seleccionar `PE4_U4_AMAGUA_CRESPO_GAMARRA_PONCE.zip`
2. Compilador: **pdfLaTeX**
3. Archivo principal: `PE4_U4_AMAGUA_CRESPO_GAMARRA_PONCE.tex`
4. Ejecutar compilación **3 veces** (pdfLaTeX → BibTeX → pdfLaTeX → pdfLaTeX) para resolver referencias cruzadas y bibliografía.

### Local (TeX Live / MiKTeX)
```bash
# Requisitos: TeX Live 2023+ con paquetes completos
cd 05_Informe/
pdflatex PE4_U4_AMAGUA_CRESPO_GAMARRA_PONCE.tex
bibtex   PE4_U4_AMAGUA_CRESPO_GAMARRA_PONCE
pdflatex PE4_U4_AMAGUA_CRESPO_GAMARRA_PONCE.tex
pdflatex PE4_U4_AMAGUA_CRESPO_GAMARRA_PONCE.tex
```

**Paquetes LaTeX requeridos:** `geometry`, `graphicx`, `booktabs`, `longtable`, `array`, `multirow`, `colortbl`, `xcolor`, `hyperref`, `float`, `pgf-pie`, `tikz`, `pgfplots`, `listings`, `fancyhdr`, `natbib` (o `ieeetr`), `inputenc` (utf8), `babel` (spanish).

---

## Tag de línea base

```bash
git tag -a baseline-v1.1 -m "Baseline aprobada por CCB - Semana 14 ISR-401 - CarniCore"
git push origin baseline-v1.1
```

La etiqueta `baseline-v1.1` marca la versión del ERS aprobada por el CCB el [04/8/2026], que incorpora los cambios derivados de RFC-01 (RF-27), RFC-02 (MFA en RNF-03) y RFC-03 (firma veterinaria en RF-23).

---

## Tablero Jira

URL: https://equipo-j.atlassian.net/jira/software/projects/CARNICORE/boards/2/backlog?atlOrigin=eyJpIjoiMDdkZjNhODI0ZmQwNGQ5Mjg5NTc4OTQzMDIwNmEwZGIiLCJwIjoiaiJ9

Épicas: EPIC-01 a EPIC-05 · Issues: CARN-01 a CARN-24  
Campos personalizados: Prioridad MoSCoW · Fuente del requisito · Estado de verificación

---

## Convención de commits

```
tipo(alcance): descripción breve

Tipos: docs | fix | feat | chore | refactor
Ejemplos:
  docs(ers): baseline v3.0 — estructura y secciones 1-2
  fix(ers): v1.1 correcciones defectos críticos D-01 D-02 D-03 D-04
  feat(jira): matriz de trazabilidad extendida y epics CARN-01..24
```

---

## Licencia académica

Documento elaborado con fines académicos en el marco de la asignatura ISR-401, UTEQ. Queda prohibida su reproducción o uso comercial sin autorización expresa del equipo.
