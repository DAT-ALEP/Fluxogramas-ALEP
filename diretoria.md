```mermaid

graph LR
    %% Nível Superior
    A[Diretoria de Apoio Técnico<br>Dirige serviços técnicos] --> B[Diretor de Apoio Técnico]

    %% Funções do Diretor
    subgraph DiretorFuncoes
        B --> B1[Acompanhar licitações/compras]
        B --> B2[Acompanhar dispensa/inexigibilidade]
        B --> B3[Gerir saldos e aditivos]
    end

    %% Conexões do Diretor com Coordenadorias
    B --> C[Coord.-Geral]
    B --> D[Coord. Suprimentos]
    B --> E[Coord. Contratos]
    B --> F[Coord. Publicidade]
    B --> G[Coord. Contabilidade]

    %% Coordenadoria-Geral
    subgraph CoordGeral
        C --> C1[Assessorar Diretor]
        C --> C2[Coordenar servidores]
        C --> C3[Elaborar atos normativos]
        C --> C4[Gerir processos]
    end

    %% Coordenadoria de Suprimentos
    subgraph CoordSuprimentos
        D --> D1[Organizar compras]
        D --> D2[Acompanhar licitações]
        D --> D3[Acompanhar dispensa/inexigibilidade]
        D --> D4[Elaborar aditivos]
        D --> D5[Gerir fornecedores]
        D --> D6[Atender licitações]
    end

    %% Coordenadoria de Contratos
    subgraph CoordContratos
        E --> E1[Controlar saldos/vigências]
        E --> E2[Emitir ordens/empenhos]
        E --> E3[Enviar notificações]
        E --> E4[Verificar regularidade fiscal]
        E --> E5[Analisar repactuação]
        E --> E6[Controlar vencimentos]
    end

    %% Coordenadoria de Publicidade
    subgraph CoordPublicidade
        F --> F1[Mapear gestão publicidade]
        F --> F2[Providenciar ordens]
        F --> F3[Controlar pagamentos]
        F --> F4[Encaminhar aditivos]
        F --> F5[Relatórios transparência]
    end

    %% Coordenadoria de Contabilidade
    subgraph CoordContabilidade
        G --> G1[Registrar operações]
        G --> G2[Prestar contas]
        G --> G3[Gerir remanejamento]
        G --> G4[Registrar empenhos]
        G --> G5[Controlar orçamento]
    end

    %% Conexões entre Coordenadorias
    D -->|Aditivos| E
    E -->|Empenhos| G
    F -->|Pagamentos| G
    F -->|Aditivos/Relatórios| H[Diretoria de Comunicação]

   

    class A,B diretor
    class C,D,E,F,G coord
