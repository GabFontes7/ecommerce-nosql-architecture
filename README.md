# 📦 Amazonas E-Commerce - Arquitetura de Dados NoSQL

![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)

Este repositório contém o **Relatório de Consultoria de Arquitetura de Dados** para a plataforma Amazonas E-Commerce. O projeto simula a implementação de uma infraestrutura robusta, escalável e de alta disponibilidade utilizando **MongoDB Atlas**.

## 🚀 Visão Geral do Projeto

O objetivo foi projetar e implementar um ecossistema de dados capaz de suportar o volume transacional de um e-commerce de grande porte, focando em:
- **Escalabilidade Horizontal:** Preparação para Sharding.
- **Alta Disponibilidade:** Uso de Replica Sets com failover automático.
- **Performance:** Modelagem de documentos embutidos para reduzir latência.

## 🛠️ Tecnologias Utilizadas

- **Banco de Dados:** MongoDB Atlas (Cloud SaaS)
- **Infraestrutura:** AWS (Região: sa-east-1 / São Paulo)
- **Interface de Gestão:** MongoDB Compass
- **Modelo de Dados:** NoSQL orientado a documentos (JSON-like)

## 🏗️ Destaques da Arquitetura

### 1. Alta Disponibilidade (Replica Set)
Implementação de um cluster com **3 nós (1 Primary e 2 Secondaries)**. Isso garante que o sistema permaneça online mesmo em caso de falha física de um dos servidores, com replicação de dados em tempo real.

### 2. Estratégia de Particionamento (Sharding)
Planejamento de distribuição de carga via **Hashed Sharding** utilizando a chave `customer_id`, garantindo que os dados sejam espalhados uniformemente entre os Shards durante picos de acesso.

### 3. Segurança e Governança
- Conformidade com a **LGPD**.
- Criptografia em repouso (AES-256) e em trânsito (TLS/SSL).
- Controle de acesso baseado em Roles (RBAC).

## 📊 Estrutura do Banco de Dados
O banco `amazonas_db` conta com 8 coleções principais:
`customers`, `products`, `orders`, `carts`, `payments`, `shipments`, `reviews` e `returns`.

## 📂 Arquivos no Repositório
- `Relatório de Consultoria - Amazonas.pdf`: Documento executivo detalhado.
- `Documentação Técnica.pdf`: Detalhes de implementação e métricas.

---
**Projeto desenvolvido como estudo de caso para arquitetura de sistemas distribuídos e bancos de dados NoSQL.**
