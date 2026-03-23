# Dia 2 — Portas de Rede

Hoje estudei o conceito de **portas de rede** e como elas são utilizadas para separar diferentes tipos de comunicação dentro de um dispositivo conectado à internet.

As portas permitem que um único computador ou servidor execute vários serviços ao mesmo tempo sem que os dados se misturem.

---

# O que são Portas de Rede

As portas são **números utilizados para identificar serviços específicos dentro de um dispositivo conectado a uma rede**.

Cada porta funciona como um canal de comunicação para um serviço específico.

Quando um pacote de dados chega ao dispositivo, o sistema operacional verifica qual porta está sendo utilizada e encaminha a informação para a aplicação correta.

Por exemplo, um servidor pode receber ao mesmo tempo:

- requisições de páginas web
- transferências de arquivos
- mensagens de e-mail

Cada um desses serviços utiliza portas diferentes.

---

# Como as Portas Funcionam

Toda comunicação na internet utiliza dois elementos principais:

**Endereço IP** → identifica o dispositivo na rede  
**Porta** → identifica qual serviço dentro do dispositivo deve receber os dados

Podemos representar assim:

IP + Porta = Serviço específico

Exemplo:

192.168.1.1:80

192.168.1.1 → endereço do servidor  
80 → porta utilizada pelo serviço web (HTTP)

---

# Intervalo de Portas

As portas variam de:

0 até 65535

Elas são divididas em três categorias principais.

---

# 1. Well-Known Ports (0–1023)

São portas reservadas para serviços padrão da internet.

Exemplos:

| Porta | Serviço |
|------|------|
| 20 / 21 | FTP (transferência de arquivos) |
| 22 | SSH (acesso remoto seguro) |
| 23 | Telnet |
| 25 | SMTP (envio de e-mails) |
| 53 | DNS |
| 80 | HTTP |
| 443 | HTTPS |

Essas portas são amplamente conhecidas e utilizadas por serviços essenciais da internet.

---

# 2. Registered Ports (1024–49151)

Essas portas são utilizadas por aplicações específicas registradas.

Exemplos:

| Porta | Serviço |
|------|------|
| 3306 | MySQL |
| 5432 | PostgreSQL |
| 8080 | HTTP alternativo |

---

# 3. Dynamic / Ephemeral Ports (49152–65535)

Essas portas são utilizadas temporariamente pelo sistema operacional para conexões de saída.

Por exemplo:

Quando um navegador acessa um site, o computador usa uma porta aleatória dessa faixa.

---

# Exemplo de Comunicação

Quando um usuário acessa um site:

Computador do usuário → utiliza uma porta aleatória  
Servidor web → utiliza a porta 80 ou 443

Exemplo de fluxo de comunicação:

PC:52014 → Servidor:443

Isso permite que o servidor saiba para qual aplicação enviar a resposta.

---

# Importância das Portas na Segurança de Rede

As portas são extremamente importantes na segurança de redes.

Ferramentas de segurança analisam quais portas estão:

- abertas
- fechadas
- filtradas

Estados possíveis:

**Porta aberta**  
Existe um serviço ativo escutando nessa porta.

**Porta fechada**  
Nenhum serviço está utilizando essa porta.

**Porta filtrada**  
A porta está bloqueada por um firewall.

Ataques frequentemente tentam explorar **portas abertas com serviços vulneráveis**.

Por isso, monitorar portas abertas é uma prática importante em segurança da informação.

---

# Ferramentas para Análise de Portas

Algumas ferramentas utilizadas para analisar portas e serviços de rede incluem:

- netstat
- ss
- nmap
- lsof

Exemplo de comando com Nmap:
nmap 192.168.1.1


Esse comando verifica quais portas estão abertas em um dispositivo.

---

# Resumo do Dia

Hoje aprendi que:

- portas identificam serviços dentro de um dispositivo
- cada serviço utiliza uma porta específica
- existem 65.535 portas possíveis
- portas são fundamentais para comunicação em rede
- portas abertas podem representar riscos de segurança
