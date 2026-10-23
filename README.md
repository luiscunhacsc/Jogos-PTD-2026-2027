# Jogos de Psicologia na Transição Digital · 2026–2027

Dois recursos interativos em português europeu para a unidade curricular de **Psicologia na Transição Digital**, do 3.º ano da Licenciatura em Psicologia. Combinam questões de escolha múltipla e experiências simuladas para apoiar o estudo autónomo e a discussão em aula.

Cada atividade está contida num único ficheiro HTML e funciona diretamente no navegador, sem instalação, conta ou ligação à Internet. Apenas as ligações para referências externas precisam de Internet.

## Começar

1. Descarrega o repositório através de **Code → Download ZIP** e extrai os ficheiros, ou clona-o:

   ```sh
   git clone https://github.com/luiscunhacsc/Jogos-PTD-2026-2027.git
   ```

2. Abre um dos ficheiros HTML num navegador moderno, com JavaScript ativo.
3. Escolhe uma missão ou uma sala para começar. O progresso é guardado automaticamente no navegador, quando o armazenamento local está disponível.

Não é necessário instalar dependências, compilar o projeto ou iniciar um servidor.

## Atividades

### PsicoDigital · Missões de aprendizagem

Ficheiro: [Psicologia_Transicao_Digital_Arcade.html](Psicologia_Transicao_Digital_Arcade.html)

**64 questões distribuídas por oito módulos**, todos disponíveis desde o início:

| Módulo | Tema | Questões |
| --- | --- | ---: |
| 01 · Pensar a tecnologia | Fatores humanos, inteligência artificial e decisões automatizadas | 8 |
| 02 · Explorar outros mundos | Realidade virtual e aumentada | 6 |
| 03 · Proteger pessoas e dados | Cibersegurança, ética e enquadramento legal | 8 |
| 04 · Abrir portas digitais | Literacia, divisão digital e inclusão | 8 |
| 05 · Viver e participar online | Cidadania digital e variáveis psicológicas | 12 |
| 06 · Ler os rastos digitais | Big Data | 6 |
| 07 · Sair da bolha | Desinformação e câmaras de eco | 6 |
| 08 · Aproximar à distância | Consulta psicológica à distância | 10 |

Em cada questão, escolhe a melhor das quatro respostas e seleciona **Confirmar**. O percurso inclui explicações, pistas e um caderno de apoio. Podes interromper e retomar a sessão no mesmo navegador.

- **Rever dificuldades:** recupera questões já praticadas que ainda não estejam consolidadas.
- **Desafio final:** apresenta 16 questões, duas de cada módulo, sem pistas e com correção no fim. Não há limite de tempo.
- **XP e distintivos:** uma resposta correta vale 10 XP sem ajuda ou 5 XP com pista ou caderno; consultar a solução não dá pontos. Cada questão acumula, no máximo, 10 XP. Uma questão fica consolidada quando a última resposta é correta sem ajuda; consolidar todas as questões de um módulo atribui um distintivo.
- **Impressão:** durante uma missão, usa **Imprimir módulo**. Para incluir a correção, ativa previamente **Incluir soluções na impressão**, na secção **Guardar, transportar e imprimir**.

### Por Dentro do Digital · Museu de Experiências Psicológicas

Ficheiro: [Por_Dentro_do_Digital_Museu.html](Por_Dentro_do_Digital_Museu.html)

**Seis salas interativas**, com uma duração indicativa de 5–10 minutos por sala:

| Sala | Experiência |
| --- | --- |
| A atenção em disputa | Comparar uma tarefa com e sem mensagens intermédias. |
| O espelho social | Comparar um perfil selecionado com uma cronologia mais completa. |
| A máquina de recompensas | Explorar sequências de recompensas regulares e variáveis. |
| A bolha que construímos | Alterar a personalização e a diversidade de um feed simulado. |
| O preço da conveniência | Configurar permissões e analisar as suas contrapartidas. |
| Uma máquina convincente | Confrontar respostas simuladas de IA com documentos de apoio. |

Cada sala segue cinco etapas: **Prevê → Experimenta → Observa → Explica → Transfere**. O passaporte reúne os carimbos das salas exploradas, os resultados das experiências e as reflexões opcionais. Os carimbos assinalam a conclusão do percurso, sem classificação.

No menu **Passaporte**, podes exportar ou importar o progresso e selecionar **Imprimir passaporte**. A experiência de atenção permite fazer pausas e desligar a medição do tempo.

## Guardar e transportar o progresso

As duas atividades usam o `localStorage` do navegador e mantêm registos independentes. Não existe sincronização entre dispositivos nem envio de respostas para um servidor.

Para continuar noutro navegador ou dispositivo:

1. Seleciona **Exportar progresso** na atividade de origem.
2. Guarda o ficheiro JSON exportado e transfere-o juntamente com o HTML correspondente.
3. Abre esse HTML no destino e seleciona **Importar progresso**.
4. Escolhe o JSON e confirma a substituição do progresso existente.

| Atividade | Ficheiro exportado | Conteúdo |
| --- | --- | --- |
| PsicoDigital | `psicodigital-progresso.json` | Registos das questões, incluindo tentativas, XP e consolidação. Não inclui a sessão em curso. |
| Museu | `museu-digital-passaporte.json` | Previsões, registos das experiências, reflexões e progresso das salas. Não inclui uma ronda de atenção ainda em curso. |

Os formatos são específicos de cada atividade. **Importar substitui o progresso atual, após confirmação.** Usa a exportação antes de limpar os dados do navegador, mudar de dispositivo ou se a aplicação indicar que não conseguiu guardar.

O ficheiro [psicodigital-progresso.json](psicodigital-progresso.json) incluído no repositório contém uma exportação com progresso já registado. É opcional, não é carregado automaticamente e só pode ser importado no PsicoDigital. Não é necessário para começar um percurso novo.

## Interface e acessibilidade

Ambas as atividades incluem disposição adaptável ao tamanho do ecrã, temas claro e escuro, ligação para saltar para o conteúdo, foco visível e indicações para tecnologias de apoio. O museu disponibiliza também o controlo **Reduzir movimento**.

## Organização e manutenção

```text
.
├── README.md
├── Psicologia_Transicao_Digital_Arcade.html
├── Por_Dentro_do_Digital_Museu.html
└── psicodigital-progresso.json
```

O projeto usa **HTML, CSS e JavaScript**, com estilos, dados e lógica incorporados em cada HTML. Não utiliza bibliotecas externas nem serviços de backend.

- No PsicoDigital, `DATA.mods` define os módulos e `DATA.qs` contém as questões, alternativas, explicações, pistas e referências.
- No museu, `ROOMS` define as salas e os respetivos percursos; as funções de cada experiência implementam as interações.
- As chaves de armazenamento são `psicodigital-v1` e `museu-psicodigital-v1`. Ao alterar identificadores ou formatos de dados, tem em conta a compatibilidade com o progresso guardado e as exportações existentes.

Depois de uma alteração, abre o HTML no navegador e verifica o percurso afetado, a gravação e retoma do progresso, a exportação/importação e a impressão. O repositório não inclui uma suíte de testes automatizados.

## Enquadramento pedagógico

O PsicoDigital identifica como base o *Banco Completo de Questões com Respostas — Psicologia na Transição Digital* e a *FUC Psicologia na Transição Digital 2026–2027, revista*. A correspondência com os conteúdos programáticos, as notas para o docente e as referências estão disponíveis dentro da atividade. Esses documentos de origem não estão incluídos neste repositório.

Os recursos destinam-se à aprendizagem e à discussão. As pontuações e os carimbos não constituem avaliação formal; o banco de questões adaptado não tem validação psicométrica. O museu utiliza casos e dados simulados, e os seus resultados não constituem avaliação psicológica.
