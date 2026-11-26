# Laudo Técnico de Armazenamento – Hiren's BootCD PE v1.0.8

* **Técnico Responsável:** [Seu Nome Completo]
* **Data da Execução:** DD/MM/2026
* **VM Utilizada:** `HBCD-v1.0.8`

---

## 1. Particionamento e Formatação (AOMEI / DiskGenius)

| Parâmetro Configurado | Valor Aplicado |
| :--- | :--- |
| **Disco Alvo** | Disk 1 (20 GB VDI) |
| **Tabela de Partição** | GPT |
| **Sistema de Arquivos** | NTFS |
| **Letra Atribuída** | `D:\` |

**Evidência 1 – Gerenciador de Partições:**
![Particionamento GPT NTFS](img/seu-nome-particao.png)

---

## 2. Análise de Saúde S.M.A.R.T. (CrystalDiskInfo)

* **O CrystalDiskInfo exibiu os atributos S.M.A.R.T. do disco de 20 GB?** (Sim / Não)
* **Justificativa Técnica:** [Explique por que o hipervisor/disco virtual VDI oculta ou emula os sensores físicos S.M.A.R.T. em comparação a um HD/SSD real na bancada]

---

## 3. Teste de Desempenho de Leitura (HD Tune Benchmark)

| Métrica Aferida | Resultado Obtido |
| :--- | :--- |
| **Taxa Mínima (Minimum)** | ___ MB/s |
| **Taxa Máxima (Maximum)** | ___ MB/s |
| **Taxa Média (Average)** | ___ MB/s |
| **Tempo de Acesso (Access Time)** | ___ ms |

**Evidência 2 – Gráfico do Benchmark:**
![Benchmark HD Tune](img/seu-nome-benchmark.png)
