# Prova-Desafio Banco de Dados

## Desafio 3

![Atividade Lógica MER e DER](./MER_DER_Lógico.drawio.png)
![Atividade Lógica MER e DER](./conceitual.drawio.png)

## Dicionário de Dados
| Entidade | Atributo | Tipo | Tamanho | Descrição |
|-|-|-|-|-|
| Usuario | id | Inteiro | 11 | Identificador, PK, Auto incrementável |
| Usuario | nome | Texto | 100 | Nome do usuário |
| Usuario | email | Texto | 100 | E-mail do usuário |
| Usuario | cargo | Texto | 50 | Cargo do usuário |
| Usuario | departamento | Texto | 50 | Departamento do usuário |
| Usuario | status | Texto | 20 | Status do usuário (ex: Ativo, Inativo) |
| Servidor | id | Inteiro | 11 | Identificador, PK, Auto incrementável |
| Servidor | nome | Texto | 100 | Nome do servidor |
| Servidor | hostname | Texto | 50 | Hostname do servidor |
| Servidor | ip | Texto | 50 | Endereço IP do servidor |
| Servidor | sistema_operacional | Texto | 50 | Sistema operacional do servidor |
| Servidor | ambiente | Texto | 50 | Ambiente do servidor (ex: Desenvolvimento, Testes, Produção) |
| Conta | id_conta | Inteiro | 11 | Identificador, PK, Auto incrementável |
| Conta | id_usuario | Inteiro | 11 | Identificador do usuário, FK referenciando Usuario (id) |
| Conta | id_servidor | Inteiro | 11 | Identificador do servidor, FK referenciando Servidor (id) |
| Conta | login | Texto | 50 | Login da conta |
| Conta | status | Texto | 20 | Status da conta (ex: Ativa, Inativa) |
| Conta | data_criacao | Data | 10 | Data de criação da conta |
| Conta | data_expiracao | Data | 10 | Data de expiração da conta |
| Perfil | id_perfil | Inteiro | 11 | Identificador, PK, Auto incrementável |
| Perfil | nome | Texto | 50 | Nome do perfil (ex: Leitura, Operador, Desenvolvedor, Administrador, DBA, Auditor) |
| Perfil | descricao | Texto | 255 | Descrição do perfil de acesso |
| Perfil | nivel_acesso | Inteiro | 11 | Nível numérico de acesso do perfil |
| Acesso | id_acesso | Inteiro | 11 | Identificador, PK, Auto incrementável |
| Acesso | id_conta | Inteiro | 11 | Identificador da conta, FK referenciando Conta (id_conta) |
| Acesso | id_perfil | Inteiro | 11 | Identificador do perfil, FK referenciando Perfil (id_perfil) |
| Acesso | data_inicio | Data | 10 | Data de início do acesso |
| Acesso | data_fim | Data | 10 | Data de término do acesso |
| Acesso | status | Texto | 20 | Status do acesso (ex: Ativo, Expirado, Revogado) |
