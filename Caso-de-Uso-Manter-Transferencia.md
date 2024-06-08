### Caso de Uso: Manter Transferência

**Ator:** Médico Regulador, Médico Requisitante

**Descrição:** Gerenciar todo o processo de transferência de pacientes, incluindo especificação de transporte, seleção de unidade hospitalar de destino, horários, medicação, anexos e procedimentos.

#### Requisitos Funcionais:
- **RF02:** Especificar o meio de transporte da transferência do paciente.
- **RF03:** Selecionar uma unidade hospitalar de destino.
- **RF04:** Visualizar uma lista de unidades hospitalares disponíveis para receber transferências.
- **RF05:** Cadastrar o horário de saída do paciente e receber do sistema o horário previsto de chegada.
- **RF06:** Realizar solicitações de transferência de pacientes.
- **RF07:** Especificar a classificação da transferência (primária, secundária ou terciária).
- **RF08:** Listar todas as drogas administradas no paciente e escrever detalhes de sua utilização no documento de transferência.
- **RF09:** Anexar ao documento de transferência do paciente uma lista de verificação dos procedimentos de acondicionamento previamente preparada.
- **RF10:** Estabelecer procedimentos a serem seguidos pelos profissionais da unidade de destino e anexá-los ao documento de transferência do paciente.

### Fluxo Principal:

1. **Iniciar Solicitação de Transferência:**
   - **Ator:** Médico Requisitante
   - **Descrição:** O médico requisitante inicia uma nova solicitação de transferência de paciente.
   - **Requisito:** RF06

2. **Especificar Meio de Transporte:**
   - **Ator:** Médico Regulador
   - **Descrição:** O médico regulador especifica o meio de transporte (ambulância terrestre, helicóptero ou avião).
   - **Requisito:** RF02

3. **Selecionar Unidade Hospitalar de Destino:**
   - **Ator:** Médico Regulador
   - **Descrição:** O médico regulador seleciona a unidade hospitalar de destino, utilizando uma lista de unidades disponíveis.
   - **Requisitos:** RF03, RF04

4. **Cadastrar Horário de Saída e Prever Horário de Chegada:**
   - **Ator:** Médico Regulador
   - **Descrição:** O médico regulador cadastra o horário de saída do paciente e recebe o horário previsto de chegada na unidade de destino.
   - **Requisito:** RF05

5. **Especificar Classificação da Transferência:**
   - **Ator:** Médico Requisitante
   - **Descrição:** O médico requisitante especifica a classificação da transferência (primária, secundária ou terciária).
   - **Requisito:** RF07

6. **Listar e Registrar Medicação Administrada:**
   - **Ator:** Médico Requisitante
   - **Descrição:** O médico requisitante lista todas as drogas administradas ao paciente e registra detalhes de sua utilização no documento de transferência.
   - **Requisito:** RF08

7. **Anexar Lista de Verificação de Procedimentos:**
   - **Ator:** Médico Requisitante
   - **Descrição:** O médico requisitante anexa uma lista de verificação dos procedimentos de acondicionamento ao documento de transferência.
   - **Requisito:** RF09

8. **Estabelecer Procedimentos para a Unidade de Destino:**
   - **Ator:** Médico da Unidade de Origem
   - **Descrição:** O médico da unidade de origem estabelece e anexa procedimentos a serem seguidos pelos profissionais da unidade de destino ao documento de transferência.
   - **Requisito:** RF10

### Fluxos Alternativos:

- **Falha na Validação de Unidade Hospitalar:**
  - Se a unidade hospitalar selecionada não estiver disponível:
    - O sistema exibe uma mensagem de erro.
    - O médico regulador seleciona outra unidade hospitalar disponível.

- **Mudança no Meio de Transporte:**
  - Se o meio de transporte especificado não estiver disponível:
    - O sistema notifica o médico regulador.
    - O médico regulador escolhe um meio de transporte alternativo.

### Fluxo de Exceção:

- **Erro na Comunicação:**
  - Se houver falha na comunicação entre unidades hospitalares durante a transferência:
    - O sistema tenta restabelecer a conexão.
    - Se não for possível, uma mensagem de erro é exibida e as partes envolvidas são notificadas.

### Pŕe-condições:
- O médico está logado no sistema de gerenciamento de transferências hospitalares.

### Pós-condições:

- A transferência do paciente é registrada com todas as informações relevantes.
- Todos os documentos e procedimentos são anexados e disponíveis para a unidade de destino.
- A comunicação entre as unidades de origem e destino é estabelecida e mantida.

