# Representação Semântica de Claims Patentárias

Este repositório reúne os materiais produzidos em um experimento de representação computacional de conhecimento tecnológico expresso em claims patentárias por meio de ontologias.

O experimento integra o projeto de Iniciação Científica **“Representação Computacional de Conhecimento Tecnológico Expresso em Claims Patentárias por Meio de Estruturas Semânticas”** e utiliza como domínio tecnologias robóticas patentárias relacionadas à Petrobras.

## Objetivo

Investigar como entidades, componentes, funções, mecanismos e relações tecnológicas presentes em claims patentárias podem ser representados por meio de uma ontologia.

A análise considera quatro dimensões:

- **o que é** — entidades, componentes e artefatos;
- **o que faz** — funções e capacidades;
- **como faz** — mecanismos e modos de operação;
- **como se relaciona** — relações estruturais e funcionais.

## Corpus utilizado

Nesta etapa foram utilizadas duas patentes:

- **BR 102024019190-0 A2** — Sistema drone-crawler para preparação de superfícies metálicas;
- **BR 102020026473-7** — Robô submarino e método para detecção de desagregação de NORM em sistema de produção.

A primeira patente foi utilizada para a construção do núcleo ontológico inicial. A segunda foi utilizada em um experimento de reutilização parcial da estrutura criada.

Uma terceira patente, **PI 9904364-5 — Veículo telecomandado para operações no interior de dutos**, permanece disponível para etapas posteriores.

## Planilhas de análise

As planilhas utilizadas durante o experimento estão disponíveis em:

https://docs.google.com/spreadsheets/d/1dB8wqrEcCWH3vbDZ3nRHlAOSIwHsIfDuWJjiy33JVjQ/edit?usp=sharing

Elas registram a descrição das patentes, a análise das claims, a estruturação da ontologia e a comparação entre as patentes utilizadas.

## Ontologia preliminar

A primeira versão da ontologia foi deliberadamente reduzida e não representa todo o conteúdo das claims.

O núcleo inclui categorias como `EntidadeTecnologica`, `Sistema`, `Veiculo`, `Componente`, `FuncaoTecnologica` e `Mecanismo`.

Entre os conceitos modelados estão `Crawler`, `Drone`, `Motor`, `Roda`, `Ima`, `SistemaDeAdesao`, `SistemaDeLocomocao`, `FuncaoDeAdesao`, `FuncaoDeLocomocao` e `MecanismoDeAdesaoMagnetica`.

As principais relações utilizadas são `hasComponent`, `hasSubsystem`, `performsFunction` e `operatesThrough`.

Exemplo:

```text
SistemaLocomocao_1
    hasComponent Motor_1
    hasComponent Roda_1
    performsFunction FuncaoLocomocao_1
```

A ontologia foi implementada no **Protégé**, utilizando classes, propriedades, indivíduos e relações entre indivíduos.

## Reutilização entre patentes

Após a construção do núcleo inicial, parte da patente do robô submarino foi integrada ao mesmo modelo.

Conceitos gerais como `Sistema`, `Veiculo`, `Componente` e `Roda` puderam ser reutilizados. A segunda patente também introduziu conceitos específicos, como sistemas de detecção NORM e emissão de ultrassom, evidenciando a necessidade de expansão controlada do modelo.

## Resultados preliminares

O experimento permitiu construir uma ontologia preliminar a partir de claims patentárias, representar entidades, componentes, funções e mecanismos, explicitar relações estruturais e funcionais e reutilizar parte da estrutura em uma segunda patente.

Os resultados são preliminares e correspondem a uma avaliação exploratória da representação e reutilização do modelo.
