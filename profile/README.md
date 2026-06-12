# Solguard Security

Auditorías Blockchain, DeFi, DTL & Web3 Security.

Solguard es una herramienta experimental para apoyar auditorías Web3.
Su objetivo es mapear repositorios, detectar superficies críticas, generar hipótesis y ayudar a priorizar revisiones manuales.

No confirma vulnerabilidades por sí sola. Cada finding debe validarse con PoC, impacto real y revisión de scope.

![banner](../assets/banner.png)

## Test Audits — Solguard Labs

**Documentación:** ![docs](../docs/labs.md)

Solguard Labs son laboratorios controlados con vulnerabilidades introducidas manualmente para medir el comportamiento de la herramienta.

La tabla muestra el resultado de Solguard frente a cada laboratorio y versión.

| **Lab**    | **Version**  | **Vulns** | **Detection** | **Invariant** | **Economic** | **Diff** | **Quality** | **FP Control** | **Efficiency** |  **Score**  |
| ------ | -------: | ----: | --------: | --------: | -------: | ---: | ------: | ---------: | ---------: | ------: |
| ![DTL-v1](https://github.com/SolguardSecurity/solguard-lab-dtl-v1) | `v0.0.4` |   1/2 |       50% |       85% |      70% |  55% |     75% |       100% |        78% | **7.2** |
| DTL-v1 |          |       |           |           |          |      |         |            |            |         |
| DTL-v2 |          |       |           |           |          |      |         |            |            |         |
| DTL-v3 |          |       |           |           |          |      |         |            |            |         |

> Las versiones inferiores a: `v0.1.0` se consideran versiones experimentales y tests del funcionamiento de la herramienta.

### Criterios de Evaluación

- **Detection:** vulnerabilidades detectadas frente al total sembrado.
- **Invariant:** calidad del razonamiento sobre invariantes rotas.
- **Economic:** capacidad de conectar el bug con impacto económico o de seguridad.
- **Diff:** capacidad para detectar cambios peligrosos en commits.
- **Quality:** calidad de la evidencia generada.
- **FP Control:** control de falsos positivos.
- **Efficiency:** utilidad práctica del resultado para acelerar la auditoría.
- **Score:** puntuación global del laboratorio, de 1 a 10.
