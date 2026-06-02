Sistema Bancário em Python (POO) 🏦

Um sistema bancário via terminal simples, robusto e funcional, desenvolvido inteiramente em Python. Este projeto foi construído aplicando os principais conceitos de Programação Orientada a Objetos (POO) para simular as operações diárias de um banco real.

Funcionalidades

O sistema apresenta um menu interativo que permite realizar as seguintes operações:

* **[nu] Novo Usuário:** Cadastro de clientes (Pessoa Física) informando nome, CPF, data de nascimento e endereço.
* **[nc] Nova Conta:** Vinculação de uma ou mais Contas Correntes a um usuário já cadastrado.
* **[d] Depositar:** Adição de saldo à conta escolhida.
* **[s] Sacar:** Retirada de valores, respeitando regras de negócio (limite de R$ 5.000,00 por operação e máximo de 3 saques diários).
* **[e] Extrato:** Exibição detalhada de todas as movimentações (saques e depósitos) com data e hora exatas, além do saldo atual.
* **[lc] Listar Contas:** Exibe todas as contas cadastradas no sistema.

Arquitetura e Conceitos Aplicados

O código foi estruturado para ser escalável e de fácil manutenção, utilizando:

* **Herança:** Criação de classes específicas (como `PessoaFisica` e `ContaCorrente`) que herdam comportamentos de classes base (`Cliente` e `Conta`).
* **Encapsulamento:** Proteção de dados sensíveis, como o saldo da conta (`_saldo`), acessados de forma segura através de `properties`.
* **Abstração:** Uso de Classes Base Abstratas (`ABC` e `@abstractmethod`) na classe `Transacao`, garantindo um contrato rigoroso para futuras implementações de movimentações financeiras (ex: transferências via Pix).
* **Polimorfismo:** Sobrescrita de métodos como `sacar` na `ContaCorrente` para incluir validações específicas antes de executar o comportamento padrão.

Tecnologias Utilizadas

* **Linguagem:** Python 3.x
* **Bibliotecas Nativas:** `abc` (para classes abstratas), `datetime` (para histórico de transações) e `textwrap` (para formatação visual do menu).

Como Executar

1. Clone este repositório para a sua máquina local:
```bash
git clone https://github.com/lalima13/Banco.git
