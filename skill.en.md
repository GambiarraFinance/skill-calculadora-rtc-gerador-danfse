id: calculadora-rtc-gerador-danfse
name: DANFSe Generator (Brazilian Federal Revenue)
description: |
  Skill to integrate and use the DANFSe service from the Brazilian Federal Revenue
  (Receita Federal do Brasil). It is an HTTP service in Go that generates the
  DANFSe (Documento Auxiliar da Nota Fiscal de Serviços eletrônica) in PDF from
  the XML of an NFS-e.
triggers: "generate danfse", "danfse pdf nfse", "rtc danfse generator calculator", "brazilian federal revenue danfse", "xml nfse to pdf", "danfse generator go"
---
# DANFSe Generator

## Overview

The DANFSe Service is an open HTTP service from the Brazilian Federal Revenue
(Receita Federal do Brasil), written in Go, that generates the **DANFSe in PDF**
from the **XML of an NFS-e** (electronic Service Invoice).

## When to use this skill

Use this skill when you need to:

- Generate the DANFSe in PDF from the XML of an NFS-e.
- Expose an HTTP service for service document issuance.
- Run the service locally or via Docker.

## How to run

### Requirements

- Go 1.27+
- [Task](https://taskfile.dev/) — optional, but recommended

### With Task

```bash
task run
```

### Without Task

```bash
go run ./cmd/danfse
```

By default, the server starts on port `8080`. To use another port:

```bash
SERVER_PORT=8081 go run ./cmd/danfse
```

You can also define `SERVER_PORT` in a `.env` file, which is loaded automatically
by the Taskfile.

### Docker

```bash
# Build local image
docker build -t danfse-go .

# Run the container
docker run -p 8080:8080 danfse-go
```

## Official repository

https://github.com/ReceitaFederal/calculadora-rtc-gerador-danfse

This skill is maintained in the https://github.com/GambiarraFinance ecosystem.
