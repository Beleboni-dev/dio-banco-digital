# Banco Digital - README

Este é um simples banco digital desenvolvido em Java, demonstrando o uso dos principais conceitos da Programação Orientada a Objetos (POO). O projeto consiste em um sistema que permite criar contas correntes e contas poupança, realizar transferências entre contas e depositar valores na conta poupança.

## Funcionalidades

### Classes

- **Banco**: Representa o banco digital e possui uma lista de contas.
- **Conta**: Classe abstrata que contém atributos comuns a todas as contas, como agência, número da conta, status (ativa ou inativa) e saldo. Define também o método abstrato `sacar()` para realizar saques.
- **ContaCorrente**: Classe que herda de `Conta`, representando contas correntes. Possui o método `transferir()` para realizar transferências para outras contas.
- **ContaPoupanca**: Classe que herda de `Conta`, representando contas poupança. Possui o método `depositarPoupanca()` para adicionar saldo à conta poupança.

### Interfaces

- **Transferencia**: Interface que define o método `transferir()` para transferências entre contas. Implementada pelas classes `ContaCorrente` e `ContaPoupanca`.

### Aplicação Principal

O arquivo `IPhoneApp.java` contém a aplicação principal que utiliza todas as funcionalidades do banco digital. Nesta classe, são criadas instâncias das classes `ContaCorrente`, `ContaPoupanca` e `Banco`, e são realizadas operações como criar contas, fazer transferências e depositar na conta poupança.

## Conceitos de POO Demonstrados

- **Abstração**: Utilizamos a classe abstrata `Conta` para definir um modelo comum para todas as contas, com o método abstrato `sacar()` sendo implementado nas subclasses concretas `ContaCorrente` e `ContaPoupanca`.
- **Encapsulamento**: Os atributos das classes `Conta`, `ContaCorrente` e `ContaPoupanca` são declarados como privados e acessados por meio de métodos getters e setters, garantindo que somente os métodos das próprias classes possam modificar esses valores.
- **Herança**: As classes `ContaCorrente` e `ContaPoupanca` herdam da classe abstrata `Conta`, aproveitando seus atributos e métodos comuns e adicionando funcionalidades específicas.
- **Polimorfismo**: Através da interface `Transferencia`, as classes `ContaCorrente` e `ContaPoupanca` podem ser tratadas genericamente, permitindo a substituição de objetos durante a execução do programa e facilitando a realização de transferências.
