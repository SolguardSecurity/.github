# Solguard Security

Auditorias Blockchain, DeFi, DTL & Web3 Security.

Solguard es una herramienta experimental para apoyar auditorias Web3.
Su objetivo es mapear repositorios, detectar superficies criticas, generar hipotesis y ayudar a priorizar revisiones manuales.

No confirma vulnerabilidades por si sola. Cada finding debe validarse con PoC, impacto real y revision de scope.

![banner](../assets/banner.png)

## Releases

- v0.5.0: [release](https://github.com/SolguardSecurity/solguard-docs/blob/main/releases/v0.5.0.md)
- v0.6.0: [release](https://github.com/SolguardSecurity/solguard-docs/blob/main/releases/v0.6.0.md)
- **v0.7.0:** [new](https://github.com/SolguardSecurity/solguard-docs/blob/main/releases/v0.7.0.md)

## Test Audits - Solguard Labs

**Documentacion:** [labs](https://github.com/SolguardSecurity/solguard-docs/blob/main/docs/solguard-labs/README.md)

Solguard Labs son laboratorios controlados con vulnerabilidades introducidas manualmente para medir el comportamiento de la herramienta.

La tabla muestra el resultado de Solguard frente a cada laboratorio y version.

| **Lab** | **Version** | **Vulns** | **Detection** | **Invariant** | **Economic** | **Diff** | **Quality** | **FP Control** | **Efficiency** | **Score** |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| [DTL-v1](https://github.com/SolguardSecurity/solguard-lab-dtl-v1) | `v0.4.0` | 1/2 | 50% | 85% | 70% | 55% | 75% | 100% | 78% | **5.2** |
| [DTL-v2](https://github.com/SolguardSecurity/solguard-lab-dtl-v2) | `v0.4.0` | 0/3 | 0% | 0% | 0% | 0% | 0% | 0% | 0% | **0** |
| [DTL-v3](https://github.com/SolguardSecurity/solguard-lab-dtl-v3) | `v0.4.0` | 0/4 | 0% | 0% | 0% | 0% | 0% | 0% | 0% | **0** |
| [DeFi-v1](https://github.com/SolguardSecurity/solguard-lab-defi-v1) | `v0.5.0` | 3/3 | 100% | 2 | 13 | 2 | 3 | 100% | 0.60 | **10** |
| [DeFi-v2](https://github.com/SolguardSecurity/solguard-lab-defi-v2) | `v0.5.0` | 3/3 | 100% | 5 | 3 | 3 | 4 | 75% | 0.80 | **8.5** |
| [DeFi-v3](https://github.com/SolguardSecurity/solguard-lab-defi-v3) | `v0.5.0` | 3/3 | 100% | 2 | 0 | 10 | 4 | 75% | 0.25 | **8.5** |
| [DeFi-v4](https://github.com/SolguardSecurity/solguard-lab-defi-v4) | `v0.5.0` | 2/2 | 100% | 3 | 0 | 12 | 2 | 100% | 0.13 | **10** |
| [DTL-v1](https://github.com/SolguardSecurity/solguard-lab-dtl-v1) | `v0.5.0` | 2/2 | 100% | 5 | 0 | 9 | 3 | 66.7% | 0.10 | **7.7** |
| [DTL-v2](https://github.com/SolguardSecurity/solguard-lab-dtl-v2) | `v0.5.0` | 3/3 | 100% | 6 | 0 | 12 | 3 | 100% | 0.10 | **10** |
| [DTL-v3](https://github.com/SolguardSecurity/solguard-lab-dtl-v3) | `v0.5.0` | 4/4 | 100% | 5 | 0 | 12 | 4 | 100% | 0.13 | **10** |
| [DTL-v4](https://github.com/SolguardSecurity/solguard-lab-dtl-v4) | `v0.5.0` | 4/4 | 100% | 6 | 0 | 13 | 4 | 100% | 0.14 | **10** |

> En `v0.5.0`, las columnas se leen como metricas operativas reales: `Invariant` refleja hipotesis sembradas, `Economic` refleja flujos semanticos detectados, `Diff` refleja mismatches de trazado y `Quality` refleja findings generados. `Score` no se recalcula en esta release porque la version ya se valida con metricas de cobertura y precision medidas directamente.

> Las versiones inferiores a: `v0.1.0` se consideran versiones experimentales y tests del funcionamiento de la herramienta.

### Criterios de Evaluacion

- **Lab:** Laboratorio donde se prueba la herramienta
- **Version:** Version de la herramienta de auditoria
- **Vulns:** Vulnerabilidades detectadas correctamentes

- **Detection:** vulnerabilidades detectadas frente al total sembrado.
- **Invariant:** calidad del razonamiento sobre invariantes rotas.
- **Economic:** capacidad de conectar el bug con impacto economico o de seguridad.
- **Diff:** capacidad para detectar cambios peligrosos en commits.

- **Quality:** calidad de la evidencia generada.
- **FP Control:** control de falsos positivos.
- **Efficiency:** utilidad practica del resultado para acelerar la auditoria.
- **Score:** puntuacion global del laboratorio, de 1 a 10.
