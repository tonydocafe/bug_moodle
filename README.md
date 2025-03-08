
#### Implementação de Salvamento Automático
##### Descrição
Este código implementa um sistema de salvamento automático para uma aplicação web. Ele é composto por duas partes: um trecho PHP no servidor e um código JavaScript no cliente. O salvamento automático é realizado a cada 60 segundos sem a necessidade de o usuário clicar em um botão de salvar.
#### Funcionamento
#### PHP
O código PHP verifica se o parâmetro autosave foi enviado no pedido. Caso o parâmetro seja verdadeiro, o código executa o método process_attempt() no objeto $attemptobj, o qual é responsável por processar e salvar os dados da tentativa.
A função process_attempt() é chamada com o timestamp atual (time()) e outros parâmetros, além da variável $page (que pode ser relacionada a uma página de formulário ou contexto de tentativa).
Após o processamento, o código responde com um JSON contendo o status do salvamento, informando ao cliente que a tentativa foi salva.



#### Considerações Finais
Esse sistema de salvamento automático é útil em aplicações que exigem que o usuário não perca seu progresso em formulários longos, como em testes ou submissões de conteúdo.


# 📝 Salvar Texto Automaticamente com XAMPP  

Este projeto permite salvar automaticamente um texto digitado em um campo de entrada para um banco de dados **MySQL** usando **PHP** e **JavaScript**. O salvamento ocorre a cada **2 segundos após a última digitação**.  

O sistema utiliza **XAMPP** para fornecer um ambiente local com **Apache, PHP e MySQL**.  

## 📌 Requisitos  

- **XAMPP** instalado  
- **Apache e MySQL ativados no XAMPP**  
- **Banco de dados MySQL configurado**  

## 🛠️ Configuração  

### 1️⃣ Iniciar o XAMPP  
1. Abra o **XAMPP Control Panel**  
2. Inicie o **Apache e o MySQL**  

### 2️⃣ Criar o Banco de Dados  
1. Acesse **phpMyAdmin** em:  
http://localhost/phpmyadmin/

PHP
----------------------------------------------------------------------------
O script PHP recebe uma requisição do tipo POST, verifica se há um campo chamado texto na requisição e tenta armazenar esse conteúdo em um banco de dados MySQL, garantindo que não haja duplicatas.

.JS
------------------------------------------------------------------------------
JavaScript implementa um sistema de salvamento automático e manual de um texto digitado pelo usuário, enviando-o para um servidor via fetch(). Ele evita envios repetidos e fornece feedback visual ao usuário.
