# 🚀 Desafio de Arquitetura AWS: Monitoramento e Backup Seguro de Arquivos Sensíveis

[![AWS](https://img.shields.io/badge/AWS-Cloud-orange?logo=amazon-aws)](https://aws.amazon.com/)
[![EC2](https://img.shields.io/badge/EC2-Instance-green?logo=amazon-aws)]
[![S3](https://img.shields.io/badge/S3-Bucket-yellow?logo=amazon-aws)]

---

## 🎯 Objetivo
Aplicar conceitos de arquitetura AWS em um cenário prático de cibersegurança, implementando:

- Armazenamento seguro de arquivos sensíveis.
- Monitoramento automático de alterações.
- Processamento temporário e backup seguro.
- Centralização de logs para compliance.
- Documentação de boas práticas e insights técnicos.

---

## 📂 Cenário Proposto
Criar uma solução para monitoramento e backup seguro de arquivos sensíveis utilizando:

- **Amazon S3**: Armazenamento seguro de arquivos, logs e relatórios.
- **AWS Lambda**: Função automática para validar arquivos e gerar alertas.
- **EC2 + EBS**: Processamento adicional e armazenamento temporário, com snapshots periódicos.

---

## 🗂 Fluxo da Arquitetura

```text
[Usuário / Aplicação]
          │
          ▼
   [S3 Bucket] ──► Armazena arquivos sensíveis
          │
   (Trigger: Evento de criação/alteração)
          ▼
 [Lambda Function] ──► Valida arquivos e envia alertas de segurança
          │
   (Processamento adicional)
          ▼
  [EC2 Instance + EBS] ──► Armazena temporariamente e realiza análises
          │
   (Snapshots periódicos)
          ▼
   [S3 Bucket de Logs] ──► Centraliza logs para auditoria e compliance

----


## Descrição detalhada do fluxo:

1. Usuário envia arquivos sensíveis para o bucket principal do S3.

2. Lambda é acionada automaticamente em eventos de criação/alteração:

3. Valida tipo e tamanho do arquivo.

4. Gera logs e envia alertas de segurança.

5. Arquivos podem ser processados temporariamente em EC2 com EBS.

6. Snapshots periódicos do EBS garantem backup seguro.

7. Logs de atividades centralizados no S3 garantem auditoria e compliance.


---

