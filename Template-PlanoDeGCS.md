Certidão Concurso Público
=================
Plano de Gerenciamento de Configuração
======================================
Versão 1.03
------------------


Histórico de Versões
--------------------

|Data                |Versão       |Descrição               |Autor          |
|--------------------|-------------|------------------------|---------------|
|_02/12/2013_|_1.00_|_Criação do documento_|_João Paulo_|
|_03/12/2013_|_1.01_|_Atualizar documento_|_João Paulo_|
|_03/12/2013_|_1.02_|_Atualizar documento_|_João Paulo_|
|_05/12/2013_|_1.03_|_Atualizar documento_|_Bruno Queiroz_|



1. Introdução
==============

O Plano de Gerenciamento de Configuração explica todas as atividades do Gerenciamento de Controle de Configuração e Mudança que serão realizadas durante o ciclo de vida do produto. Suas atividades envolvem reconhecer a configuração do software, manter sua integridade durante o projeto e controlar sistematicamente as mudanças.

1.1 Finalidade
---------------
A finalidade deste documento é criar um padrão a ser seguido por todos os membros da equipe com o propósito de garantir o maior controle do produto no decorrer do projeto. Para realizar serão detalhados os recursos necessários (equipes, ferramentas e computadores), as responsabilidades e o cronograma de atividades.


1.2 Escopo
----------
Este Plano de Gerenciamento de Configuração é destinado para todos os integrantes da equipe responsável pelo desenvolvimento do sistema para promover maior eficiência nas atividades de emissão de certidão da 5ª Região da Justiça Federal, através do cadastro das informações, automatização e controle das certidões, além de considerável economia financeira decorrente de redução do gasto com impressões em papel, gasto com materiais de expediente para manter e controlar as certidões e o gasto de mão-de-obra dos funcionários do cadastro da Justiça Federal.

1.3 Definições, Acrônimos e Abreviações
---------------------------------------
SCRUM - É um processo ágil que permite manter o foco na entrega do maior valor de negócio, no menor tempo possível.
GC - Gerência de Configuração.
CCM - Comitê para o Controle de Mudanças.
Baseline - Conjunto de artefatos que recebe uma aprovação de estabilidade. Um baseline é usado como uma base no desenvolvimento das próximas fases dos artefatos e tem suas modificações controladas por um processo.
CM - Controle de Mudanças.

1.4 Referências
---------------
Template de Gerenciamento de Configuração.

1.5 Visão Geral
---------------
Na seção de 2 (Gerenciamento de configuração de software): São relacionados os papéis, as responsabilidades das atividades e as ferramentas dentro da GC da Fábrica.
Na seção 3 (O Programa de Gerenciamento de Configuração): É apresentado como serão criadas e controladas as Baselines.
Na seção 4  (Padrões e Procedimentos): Descreve os padrões e procedimentos que devem ser seguidos no projeto.
Na seção 5 (Treinamento e Recursos): Descreve as ferramentas de software, o pessoal e o treinamento necessários para implementar as atividades de CM especificadas.
Na seção 6 ( Auditorias de Configuração): Descreve o cronograma das auditorias de configuração e o que será verificado. Informe também como serão reportados os problemas encontrados e onde sera feito o acompanhamento dos itens corretivos.


2. Gerenciamento de Configuração de Software
============================================

2.1 Organização, Responsabilidades e Interfaces
------------------------------------------------
Papéis                                                             
Gerente de configuração
Equipe
João Paulo
Responsabilidade
Estabelecer Políticas de GC
Escrever Plano de GC
Configurar Ambiente de GC
Criar Baselines

Papéis                                                             
CCM
Equipe
João Paulo
Sergio Rodrigues
Bruno Duarte
Responsabilidade
Estabelecer Processo de Controle de Mudanças
Revisar Solicitação de Mudança

Papéis                                                             
Desenvolvedor
Equipe
João Paulo
Bruno Duarte
Sergio Rodrigues
Responsabilidade
Seguir os padrões e procedimentos definidos no Plano de Gerência de Configuração

2.2 Ferramentas, Ambiente e Infra-estrutura
-------------------------------------------

Ferramenta:
Subversion - Sistema de controle de versão
TortoiseSVN - Acesso ao repositório, é o Client para o Subversion integrado ao Windows.
 
Ambiente: 
Sistema operacional - Windows 7
Pacote Office 2010
Antvírus: Avast
Controle de versão: Subversion 1.8.5
Plataforma de desenvolvimento JAVA: Eclipse
Banco de dados: PostgreSQL
Comunicação: Gmail

A estrutura do ambiente será da seguinte forma:

Desenvolvimento: É o ambiente que servirá para o desenvolvimento do Sistema.	O componente atingirá a maturidade quando os requisitos forem supridos e testados pelos desenvolvedores através dos testes unitários.
Configuração: Processador 2.8 GHz, Memória RAM 4GB, HD de 500 GB
Integração: É o ambiente que servirá para os testes de integração.
Quando a comunicação entre os módulos atinge o um estagio satisfatório de funcionamento.
Configuração: Processador 2.8 GHz, Memória RAM 4GB, HD de 500 GB
Banco de Dados: É o ambiente onde conterá o Banco de dados.
Configuração: Processador 2.8 GHz, Memória RAM 4GB, HD de 500 GB

3. O Programa de Gerenciamento de Configuração
==============================================

3.1 Identificação da Configuração
---------------------------------
### 3.1.1 Métodos de Identificação
----------------------------------
#### 3.1.1.1 Nomenclatura dos artefatos
---------------------------------------
Todos os documentos disponibilizados no repositório (exceto o código do sistema, pois este segue um padrão de desenvolvimento) devem ser identificados baseados na seguinte nomenclatura:
 
&lt;ID_ARTEFATO&gt; - &lt;NOME_ARTEFATO&gt;

Onde:

* &lt;ID_ARTEFATO&gt; é a sigla de identificação do artefato conforme Tabela 2.
* &lt;NOME_ARTEFATO&gt; é nome de identificação do artefato conforme Tabela 2.

| Id do artefato | Nome do artefato	 |
|----------------|-------------------|
|APD   |   Ativação de Projeto de Desenvolvimento
|EOR   |   Especificação de Objetivos e Requisitos
|LPS   |   Levantamento Preliminar do Software
|PCP   |   Plano de Comunicação do Projeto
|PDS   |    Plano de Desenvolvimento de Software
|PGC   |   Plano de Gerência de Configuração
|PGQ   |  Plano de Gerência da Qualidade
|PGR   |   Plano de Gerência de Riscos
|RAC   |  Relatório de Avaliação do Cliente
|RAP   |   Relatório de Acompanhamento do Projeto
|PFM   |  Pedido Formal de Modificação
|SAI   |  Solicitação de Análise de Impacto
|RTF   |  Relatório de RTF (Revisão Técnica Formal)
|DAS   |   Documento de Análise de Software
|DPS   |   Documento de Projeto de Software
Tabela 2 - Ids e nomes de documentos

#### 3.1.1.2 Versão dos artefatos
---------------------------------
Todos os artefatos (exceto os arquivos de código fonte do programa) deverão ter uma nomenclatura de versionamento segundo o seguinte padrão:

X.YY

Onde:
* X é um número que representa uma versão final do Artefato;
* YY é um número que representa uma versão intermediária posterior a uma versão X do artefato.

O versionamento dos artefatos dar-se-á da seguinte forma:
* a cada versão interdiária o valor de YY aumenta em uma unidade;
* a cada versão estável do artefato o valor de YY é zerado e o valor de X é incrementado em uma unidade.

#### 3.1.1.3 Outras nomenclaturas
---------------------------------
Os artefatos não citados nesta seção terão sua identificação padronizada e diferenciada apenas pelo diretório em que se encontram e não pelo nome do arquivo.

### 3.1.2 Itens de Configuração
| Item (ou Tipo de Item)                 | Responsável na equipe	     | Inclusão em Baseline |
|----------------------------------------|-----------------------------|----------------------|
|_Plano de projeto, planos auxiliares, EAP e Cronograma (documentação do projeto)_|_João Paulo_|_O mais cedo possível_|
|_Requisitos, Especificações, Modelos (documentação de Software)_|_Sérgio_|_Na fase de análise de requisitos_|
|_Massa de dados de teste_|_Bruno_|_Após a fase de construção_|
|_Código fonte_|_Bruno_|_durante a fase de construçao_|

### 3.1.3 Baselines do Projeto
| Fases                 | Itens de configuração da baseline	     |
|----------------------------------------|-----------------------|
|_Iniciação_|_Plano de projeto e planos auxiliares, incluindo Plano de Gerenciamento de Configuração_|
|_Elaboração_|_Requisitos, Especificações_|
|_Projeto de Software_|_Modelos, Código fonte (provas de conceito das partes mais complicadas, arquitetura inicial)_|
|_Construção - 1ª Entrega_|_Código fonte_|
|_Construção - 2ª Entrega_|_Código fonte_|
|_Construção - 3ª Entrega_|_Código fonte_|
|_Transição_|_Executável, documentação do sistema_|

### 3.1.4 Estrutura do Repositório de Versões
| Fases                 | Itens de configuração da baseline	     |
|----------------------------------------|-----------------------|

<table
 <tr>
  <th>Diretório</th>
  <th>Subdiretório</th>
  <th>Artefatos</th>
 </tr>
 <tr>
  <td rowspan="3">Documentos</td>
  <td>Gerência de Configuração</td>
  <td>Modelo do Plano de Gerenciamento de configuração
      Notas de Releases
      Arquivos de aprovação dos documentos
  </td>
 </tr>
 <tr>
  <td>Gerência de Projetos </td>
  <td>Documento de Visão
      Termo de Abertura
      Plano de Projeto
      Cronograma
      Relatório de Status
      Atas de Reuniões
      Arquivos de aprovação dos documentos
  </td>
 </tr>
 <tr>
  <td>Analise e Projeto</td>
  <td>  Manual de Implantação
        Documento de Arquitetura
        Modelo de Banco de Dados
        Modelo de Análise e Projetos
        Arquivos de aprovação dos documentos
  </td>
 </tr>
 <tr>
  <td>Site</td>
  <td>Fontes</td>
 </tr>
</table>

3.2 Controle de Configuração e Mudança
--------------------------------------

### 3.2.1 Processamento e Aprovação de Solicitações de Mudança
_[Descreva o processo pelo qual os problemas e as mudanças são submetidos, revisados e dispostos. Inclua como funciona a transição de estados de uma solicitação de mudança]_

### 3.2.2 Comitê de Controle de Mudança (CCB)
_[Descreva a participação e os procedimentos para processar solicitações e aprovações de mudança a serem seguidos pelo CCB. Informe quem são os membros do CCB e suas responsabilidades.]_



4. Padrões e Procedimentos
==========================
_[Descreva os padrões e procedimentos que devem ser seguidos no projeto. Crie subseções se achar necessário, para organizá-los melhor.]_



5. Treinamento e Recursos
=========================
_[Descreva as ferramentas de software, o pessoal e o treinamento necessários para implementar as atividades de CM especificadas.]_



6. Auditorias de Configuração
=============================
_[Descreva o cronograma das auditorias de configuração e o que será verificado. Informe também como serão reportados os problemas encontrados e onde sera feito o acompanhamento dos itens corretivos.]_
