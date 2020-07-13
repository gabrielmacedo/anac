---
title: Projeto Rab Digital
description: Apresentação versão 01, dia 13/07/2020 do projeto Rab Digital. Agência Nacional de Aviação Civil (ANAC)
tags: projeto, anac, rab, 00058.018699/2019-17
lang: pt
slideOptions:
  theme: white
  transition: 'fade'
  slideNumber: 'true'
  # Black (default) - White - League - Sky - Beige - Simple
  # parallaxBackgroundImage: 'https://s3.amazonaws.com/hakim-static/reveal-js/reveal-parallax-1.jpg'
---

# Projeto Rab Digital
## Visão geral do projeto

1. Propósito
1. Evolução do Conceito
1. Telas do Sistema – Exemplo
1. Serviços – Nomenclatura e Compatibilização
1. Complexidade de enquadramento de condições para cada serviço agregado

----

6. Gestão de conhecimento
7. Documentação do processo: https://bit.ly/RabDigital-doc

---

## Objetivo

- Melhorar a instrução dos Processos no RAB
- Orientar o Regulado no preenchimento de solicitação
- Organizar a documentação a ser juntada
- Iniciar processo só depois de validação de requisitos como:
- Documentação necessária a cada pedido

----

- Recolhimento correto das TFAC dos serviços demandados (Geração e conferência de pagamento)
- Elaboração de uma pré minuta do Despacho de deferimento dos serviços
- Distribuição semiautomática de processos aos analistas

---

## Benfícios esperados

- Redução do tempo de análise de processo pois:
    -    Documentos já organizados para conferência
    -    Parte do trabalho de organização e entendimento da solicitação que fica a cargo do analista passa a ser do Regulado e anterior a abertura do processo.
    -    Pré minuta já elaborada

----

- Regulado ficar mais ciente das necessidades e requisitos que tem que cumprir
- Redução nos sobrestamentos e Indeferimentos de processos
- Isonomia na distribuição de carga de serviços entre os analistas
- Criar uma sistemática de gestão compartilhada de projeto de TI na SAR

---

## Estruturação da equipe

Grupo de trabalho multidisciplinar constituído por:

- PO da GTRAB
- PO da Gestão de conhecimento SAR
- GESI Facilitação
- Gestor de sistemas SAR
- Desenvolvedor

---

### Ferramentas

- SEI - instauração do processo e registro oficial
- Teams - conversas e dúvidas pontuais sobre o projeto
- JIT. SI - reuniões online entre a equipe: meet.jit.si/Rab
- E-mail - acordos estabelecidos em reunião e próximos passos
- TFS - backlog do projeto, validações do sistema, código-fonte
- WikiANAC - documentação
- Whatsapp - **grupo com analistas** do RAB

---

### Propostas sugeridas

 - Publicação na Wiki do andamento e fundamentos das principais decisões
 - Uniformização de Nomenclatura de Serviços 
 - Integração de Metadados do RAB Digital e Livro 
 - Navegação guiada do Regulado / Manual 

----

 - Uso de formulário Wizard – experiência anterior 
 - Testar navegação do sistema com escopo enxuto 
 - Buscar fonte de provimento de informações de Seguros – SUSEP – gestão

---

## Alterações do backlog após considerações da equipe

Concepção inicial
```
* Cadastrar Regulado
* Cadastrar Serviços - Perfil Regulado
* Autenticar usuários administradores – Perfil Gestor
* Cadastrar tipos de Seviços – Perfil Gestor
* Cadastrar documentos necessários a um tipo de Serviço 
* Cadastrar campos necessários a um tipo de Serviço – Perfil Gestor
* Listar tipos de serviços e documentos necessários - Perfil Regulado
* Visualizar Serviços cadastrados - Perfil Regulado
* Validar Serviço requerido - Perfil Regulado
* Acompanhar validação de documento físico - Regulado
* Gerar TFAC - Regulado
* Validar TFAC - Regulado
* Criar processo no SEI - Regulado
* Cadastrar analistas - Distribuição automática
* Alterar analistas - Distribuição automática
* Excluir analistas - Distribuição automática
* Cadastrar tipo de prioridade - Distribuição automática
* Cadastro de processo específico - Distribuição automática
* Gerar relatório - Distribuição automática
* Processar a distribuição - Distribuição automática
* Cadastrar modelo de minutas - Gestor - Distribuição automática
* Gerar despacho - Analista - Distribuição automática
```

----

Concepção alterada
```
* Autenticar regulado já cadastrado no SCA.
* Identificar aeronave dos Serviços a demandar.
* Relacionar e ordenar Serviços demandados
* Serviço: Transferência de Aeronaves - escopo reduzido
* Manter analista
* Metadados de Serviços
* Documentos de requisitos de Serviços
* Termo de Responsabilidade com valores das TFAC
* Rotina de Controle e acompanhamento de pagamento TFAC
* Navegação guiada em caráter tutorial
* Camada adicional de verificação de requisitos - como:
  - Existência de gravames de Indisponibilidade
  - Outros
* Diversas backlogs com todos os serviços
* Distribuição de processos para os analistas
* Geração das minutas - para os analistas
* Finalizar análise - Atualizar base do SACI/ALTE.
```

---

## Consequências da mudança da concepção inicial 

Em função da grande quantidade de serviços e da complexidade de composição entre eles, decidimos fazer a próxima sprint englobando todas as abas do sistema – para isso vamos cadastrar de imediato apenas os serviços de **Transferência e Emissão de Certificados**.
- Mesmo essa transferência será apenas para **PF** e de **aeronaves PET**.

----

Isso será fundamental para entendermos:
- Qual o tamanho do Projeto – **pontos de função**
- Dificuldade de aceitação pelo Regulado
- Usabilidade da interface do sistema

Com o sistema desenvolvido até a fase de abertura do processo SEI, no ambiente de Validação poderemos conceber um sistema tutorial de navegação adequado para ajudar o Regulado.

---

# Protótipo
## Exemplo de tela de pedido de transferência

![](https://i.imgur.com/yDoA3Ek.png)

Decidimos por um modelo _Wizard_ de abas que se abrem conforme a etapa anterior esteja finalizada

----

## Seleção das marcas da aeronave

![](https://i.imgur.com/al4qNb6.png)

Começamos pela **Aba Aeronave** tendo em vista que ela é foco dos processos administrativos. Ficarão registradas **solicitações anteriores** ainda não concluídas para **facilitar a retomada do preenchimento** pelo Regulado.

----

## Dados da aeronave selecionada

Os **dados** da Aeronave são apresentados para que o Regulado verifique se os dados de que dispõe **são os mesmos** do Registro. Deve ser gerado um **alerta para a análise** – e facultado ao Regulado inserir seus dados.

----

![](https://i.imgur.com/xJ48SVk.png)

----

## Seleção dos serviços

![](https://i.imgur.com/wHEWsg5.png)

**Lista de serviços** já relacionada mas ainda sujeita a alterações – compatibilizar com Portais.

----

### Exemplo de serviços selecionados

![](https://i.imgur.com/6SMeJiL.png)

----

### Serviços que podem ser não unitários

Por exemplo: **Transferências**

![](https://i.imgur.com/Q9mqUZm.png)

----

### Cronologia dos serviços

![](https://i.imgur.com/V5XEk5S.png)

Atentar que em Transferência já se faz distinção se será só para PF ou se terá pelo menos uma PJ.

----

#### Uma vez organizado, o passo seguinte leva a execução ordenada dos serviços: transferência e emissão de certificados

![](https://i.imgur.com/fepGWN2.png)

----

### Complexidade de enquadramento da solicitação

Exemplo de enquadramento da solicitação com o termo a ser registrado:

 - Há gravame de Bloqueio de transferência? 
 - Tratar como se fosse uma transferência simples – desconsiderando outros gravames que não o Bloqueio – Então os Proprietários serão os Operadores e se deixa a definição de Inscrição de Direitos de uso para serviço seguinte, se houver.

----

 - 2 casos podem ocorrer:
      - Primeira transferência solicitada – no caso trazer dados da base RAB.
      - Já ter havido uma transferência anterior no próprio pedido – Trazer dados da base do RAB Digital (provisório).
 - Regulado pode não concordar com os dados trazidos pelo RAB – pode existir delay de atualização ou mesmo erro de lançamento – Permitir inserção dos dados trazido pelo Regulado – criar flag avisando analista.

----

 - 4 casos de transferência a considerar pois documentação e TFAC distintas:
     - Aeronave PET com transferência apenas para PF 
     - Aeronave PET com transferência para pelo menos uma PJ 
     - Aeronave Certificada com transferência apenas para PF 
     - Aeronave Certificada com transferência para pelo menos uma PJ

----

### Dados atuais do registro

Será apresentada uma tela com os dados atuais do registro - se não for a primeira transferência na solicitação, então o sistema RAB digital deverá trazer os dados de sua base provisória (base esta que será usada para a geração das minutas).

----

![](https://i.imgur.com/T3aj1Sm.png)

----

### Inclusão de dados do serviço

Seguida de uma tela para preenchimento dos dados necessários à efetivação da transferência:

![]

----

#### Conforme existam mais proprietários

![]

----

As entradas de dados da tela de serviços comporão a **Lista de metadados** necessários para a elaboração da minuta

----

#

----

![](https://i.imgur.com/4o6asdy.png)

----

![]

----

![](https://i.imgur.com/NGNhKGw.png)

----

### Biblioteca de minutas de um analista

![](https://i.imgur.com/sxnI94a.png)

----

Como há uma grande biblioteca de minutas – a **lista de metadados tende a ser grande** – em paralelo esta lista servirá de suporte ao Livro RAB - PDI.

![](https://i.imgur.com/ao5doaI.png)

----

### Cálculos de TFAC e documentos anexos

Dado que CME e CAVE – não são propriamente serviços, mas documentos que são gerados após a execução de serviços - e que apenas em pedidos de segunda vias eles são demandados exclusivamente, passamos à documentação e TFACS.

Rol de documentos será apresentado em função do tipo de transferência.

----

**4 casos** de transferência a considerar:
1. Aeronave PET com transferência apenas para PF
2. Aeronave PET com transferência para pelo menos uma PJ
3. Aeronave Certificada com transferência apenas para PF
4. Aeronave Certificada com transferência para pelo menos uma PJ.

----

### PET --> PF (critério 1 )

PET transferida só para PF - mostrar os seguintes slots:

![](https://i.imgur.com/022VuE2.png)

----

![](https://i.imgur.com/tILCuZE.png)

----

### Termo de consentimento/responsabilidade nas informações

![](https://i.imgur.com/6RHI5SY.png)

----

### TFAC – Controle automático de EMISSÃO E PAGAMENTO

![](https://i.imgur.com/6vT6nK4.png)

----

![](https://i.imgur.com/jwnmAVL.png)
