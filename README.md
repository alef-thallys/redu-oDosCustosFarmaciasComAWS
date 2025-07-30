# IMPLEMENTAÇÃO DE SERVIÇOS NA AWS – RELATÓRIO TÉCNICO

**Responsável:** Alef – Desenvolvedor Backend Júnior  
**Data de Conclusão:** 30/07/2025  

---

## 1. Contexto

Diante da necessidade de **otimização de custos operacionais** e **ganho de escalabilidade**, a Abstergo Industries iniciou um processo de migração e modernização parcial de sua infraestrutura utilizando soluções da AWS.

O projeto teve como objetivo principal implementar **três serviços-chave** da AWS com foco em:

- Redução de gastos com infraestrutura;
- Escalabilidade sob demanda;
- Alta disponibilidade.

---

## 2. Soluções Implementadas

### ☁️ EC2 – Elastic Compute Cloud

**Finalidade:** Hospedagem da aplicação web principal da empresa.

**Motivo da escolha:**  
Permite a criação de servidores virtuais com controle total sobre o ambiente, com escalabilidade e pagamento por uso.

**Configuração realizada:**  
- Instância Linux t3.micro;
- Aplicação web das farmácias implantada via CI/CD;
- Regras de segurança configuradas para permitir apenas portas HTTP/HTTPS.

---

### 📊 Auto Scaling – Elastic Compute Auto Scaling

**Finalidade:** Escalar horizontalmente o serviço conforme demanda.

**Motivo da escolha:**  
Evita desperdício de recursos com instâncias ociosas e garante desempenho em horários de pico.

**Configuração realizada:**  
- Definição de no mínimo 1 e no máximo 3 instâncias;
- Escalonamento automático baseado em métricas de CPU;
- Grupos de Auto Scaling integrados ao EC2 existente.

---

### 🧠 Amazon Aurora (Serverless)

**Finalidade:** Gerenciamento do banco de dados da aplicação.

**Motivo da escolha:**  
Oferece desempenho similar ao de bancos gerenciados tradicionais, com a vantagem da escalabilidade automática e cobrança por segundo.

**Configuração realizada:**  
- Cluster Aurora compatível com PostgreSQL;
- Modo Serverless v2 para autoajuste de capacidade;
- Backups automáticos e replicação ativados.

---

## 3. Resultados Esperados

Após a implementação, os principais ganhos esperados são:

- **Economia direta** com recursos sob demanda;
- **Elasticidade nativa**, sem intervenção manual;
- **Alta disponibilidade** para a aplicação e o banco de dados;
- Ambiente pronto para futuras integrações com outros serviços AWS.

---

## 4. Considerações Finais

A transição parcial para a AWS foi bem-sucedida, atendendo aos critérios técnicos e financeiros estabelecidos pela empresa.

**Recomendações futuras:**
- Avaliar uso de AWS Lambda para funções pontuais;
- Monitorar custos via AWS Cost Explorer;
- Iniciar testes com Amazon CloudFront e S3 para distribuição de conteúdo estático.

---

**Alef**  
*Desenvolvedor Backend Júnior*  
30/07/2025
