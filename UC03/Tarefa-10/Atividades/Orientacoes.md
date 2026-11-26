# UC 3 – Gerenciamento, Particionamento e Saúde de Armazenamento (HBCD PE v1.0.8)

Atividade prática da **Unidade Curricular 3 (Planejar e executar a manutenção de computadores)** focada na execução da **Etapa 3** utilizando o **Hiren's BootCD PE (v1.0.8)** e entrega técnica via **Pull Request (PR)** no GitHub.

> [!IMPORTANT]
> **Regras de Entrega no Repositório:**
>
> * **Não edite nem exclua** o arquivo original `entregas/TEMPLATE.md`.
> * Crie uma cópia dele dentro da pasta `entregas/` renomeada com o seu nome (ex.: `entregas/ana-silva.md`).
> * Trabalhe sempre em uma **branch dedicada** (`entrega/seu-nome`) antes de abrir o Pull Request para `main`.

---

## Estrutura do Repositório

```text
0012_uc3_tarefa10/
├── README.md
└── entregas/
    ├── img/
    │   └── .gitkeep
    └── TEMPLATE.md
```

---

## Parte 1: Execução Prática na VM (`HBCD-Diagnostico-v1.0.8`)

Inicialize sua máquina virtual com a ISO oficial do **Hiren's BootCD PE v1.0.8** e execute os três procedimentos abaixo no disco virtual de testes de **20 GB**:

1. **Particionamento e Formatação (AOMEI Partition Assistant ou DiskGenius):**
   * Localize o disco secundário de 20 GB não inicializado (`Disk 1`).
   * Inicialize o disco utilizando a tabela de partições **GPT**.
   * Crie uma partição primária ocupando todo o espaço, formate em **NTFS** e atribua a letra **`D:\`**.
   * Aplique as alterações e capture o **Print 1** (salve como `seu-nome-particao.png`).

2. **Diagnóstico de Saúde S.M.A.R.T. (CrystalDiskInfo):**
   * Abra o **CrystalDiskInfo** e verifique como o utilitário identifica o disco virtualizado de 20 GB em comparação a um HD/SSD físico na bancada.

3. **Teste de Desempenho de Leitura (HD Tune):**
   * Abra o **HD Tune**, selecione o disco de 20 GB na lista superior e clique em **Start** na aba **Benchmark**.
   * Aguarde a conclusão completa do gráfico, anote os valores de taxa de transferência e tempo de acesso, e capture o **Print 2** (salve como `seu-nome-benchmark.png`).

---

## Parte 2: Passo a Passo para Entrega via Pull Request

### 1. Fork e Criação da Branch

1. No canto superior direito desta página, clique em **Fork** para copiar o repositório para o seu perfil do GitHub.
2. No **seu** repositório (fork), crie uma branch chamada `entrega/seu-nome` (ex.: `entrega/joao-souza`) a partir da `main`.

### 2. Adição das Evidências e Preenchimento do Laudo

> [!TIP]
> **Atalho Rápido no Navegador:** Dentro do seu fork no GitHub (com a branch `entrega/seu-nome` selecionada), pressione a tecla `.` (ponto) para abrir o editor web do VS Code diretamente no navegador.

* **Via Navegador (`github.dev`):**
  1. Arraste as duas imagens (`seu-nome-particao.png` e `seu-nome-benchmark.png`) para dentro da pasta `entregas/img/`.
  2. Duplique o arquivo `entregas/TEMPLATE.md`, renomeie para `entregas/seu-nome.md` e preencha todos os campos.
  3. Acesse a aba **Source Control** na barra lateral esquerda, escreva a mensagem de commit e clique em **Commit & Push**.

* **Via Terminal / Git Local:**

  ```bash
  git clone [https://github.com/](https://github.com/)<seu-usuario>/0012_uc3_tarefa10.git
  cd 0012_uc3_tarefa10
  git checkout -b entrega/seu-nome

  # Copie suas imagens para entregas/img/ e crie entregas/seu-nome.md a partir do TEMPLATE.md
  git add .
  git commit -m "docs(uc3): adiciona laudo de particionamento e benchmark - Seu Nome"
  git push origin entrega/seu-nome
  ```

### 3. Abertura do Pull Request

1. Acesse a aba **Pull Requests** no repositório original do professor e clique em **New pull request**.
2. Clique em *compare across forks* e confirme os apontamentos:
   * **Base repository:** `InfoSenac/0012_uc3_tarefa10` | **base:** `main`
   * **Head repository:** `<seu-usuario>/0012_uc3_tarefa10` | **compare:** `entrega/seu-nome`
3. Defina o título como `TAREFA 10 - [Seu Nome Completo]` e clique em **Create pull request**.

---

## Critérios de Avaliação Formativa (Modelo Pedagógico Senac - MPS)

O Pull Request será avaliado conforme os indicadores da **UC 3** nas menções **Atendido (A)**, **Parcialmente Atendido (PA)** ou **Não Atendido (NA)**:

| Critério Avaliado | Indicador / Competência | Menção |
| :--- | :--- | :---: |
| **Fluxo de Versionamento (Git/GitHub):** Realizou Fork, utilizou branch dedicada (`entrega/nome`), preservou o `TEMPLATE.md` intacto e abriu o PR corretamente para `main`. | Marcas Formativas | |
| **Gerenciamento e Particionamento Lógico:** Comprovou via evidência o disco de 20 GB inicializado em GPT, formatado em NTFS e montado na unidade `D:\`. | UC 3 – Indicador 5 | |
| **Diagnóstico de Armazenamento e S.M.A.R.T.:** Executou o benchmark completo no HD Tune e justificou tecnicamente o comportamento do S.M.A.R.T. em ambiente virtualizado. | UC 3 – Indicador 7 | |
