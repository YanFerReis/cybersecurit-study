# Dia 3 — Port Scanning

Hoje estudei o conceito de **port scanning**, uma técnica utilizada para descobrir quais portas estão abertas em um dispositivo conectado à rede.

Quando uma porta está aberta, normalmente significa que existe um serviço ativo escutando nessa porta e pronto para receber conexões.

Essa técnica é muito utilizada em **segurança da informação**, principalmente em atividades como:

- análise de rede
- auditoria de segurança
- testes de intrusão (pentest)

---

# Ferramenta utilizada

A ferramenta estudada foi o **Nmap (Network Mapper)**.

O Nmap é uma das ferramentas mais utilizadas no mundo para análise de redes e descoberta de serviços.

Ele permite identificar:

- portas abertas
- portas fechadas
- portas filtradas

Além disso, também pode ajudar a identificar quais serviços estão rodando em cada porta.

---

# Comando estudado

O comando básico utilizado para realizar um scan é:
nmap localhost

Esse comando verifica quais portas estão abertas no próprio computador.

Também é possível utilizar:
nmap 127.0.0.1

Esse endereço representa o próprio dispositivo (loopback).

---

# Exemplos de portas comuns

| Porta | Serviço |
|------|------|
| 22 | SSH |
| 53 | DNS |
| 80 | HTTP |
| 443 | HTTPS |

Essas portas são muito comuns em servidores e serviços de rede.

---

# Observação

Neste momento o estudo foi focado na teoria do port scanning.  
O teste prático com Nmap será realizado posteriormente para analisar as portas abertas no sistema.

---

# Resumo do aprendizado

Hoje aprendi que:

- port scanning serve para descobrir portas abertas
- portas abertas geralmente indicam serviços ativos
- ferramentas como Nmap permitem identificar esses serviços
- essa técnica é amplamente utilizada em segurança da informação