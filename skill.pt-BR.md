id: calculadora-rtc-gerador-danfse
name: Gerador DANFSe (Receita Federal)
description: |
  Skill para integrar e utilizar o serviço DANFSe da Receita Federal do Brasil.
  É um serviço HTTP em Go que gera o DANFSe (Documento Auxiliar da Nota Fiscal de
  Serviços eletrônica) em PDF a partir do XML de uma NFS-e.
triggers: "gerar danfse", "danfse pdf nfse", "calculadora rtc gerador danfse", "receita federal danfse", "xml nfse para pdf", "gerador danfse go"
---
# Gerador DANFSe

## Visão geral

O DANFSe Service é um serviço HTTP aberto da Receita Federal do Brasil, escrito em
Go, que gera o **DANFSe em PDF** a partir do **XML de uma NFS-e** (Nota Fiscal de
Serviços eletrônica).

## Quando usar esta skill

Use esta skill quando precisar:

- Gerar o DANFSe em PDF a partir do XML de uma NFS-e.
- Expor um serviço HTTP para emissão de documentos fiscais de serviços.
- Rodar o serviço localmente ou via Docker.

## Como executar

### Pré-requisitos

- Go 1.27+
- [Task](https://taskfile.dev/) — opcional, mas recomendado

### Com Task

```bash
task run
```

### Sem Task

```bash
go run ./cmd/danfse
```

Por padrão, o servidor inicia na porta `8080`. Para usar outra porta:

```bash
SERVER_PORT=8081 go run ./cmd/danfse
```

Também é possível definir `SERVER_PORT` em um arquivo `.env`, que é carregado
automaticamente pelo Taskfile.

### Docker

```bash
# Gerar imagem local
docker build -t danfse-go .

# Rodar o container
docker run -p 8080:8080 danfse-go
```

## Repositório oficial

https://github.com/ReceitaFederal/calculadora-rtc-gerador-danfse

Este skill é mantido no ecossistema https://github.com/GambiarraFinance.
