# Agente-AzureFrontierGirls
Agente teste do Foundry, como desafio do Azure Frontier Girls de AI Foundry.

## Introdução
Este projeto implementa um agente do "Foundry Agent Framework" para gerenciar e automatizar a lista de compras doméstica.  
O agente será capaz de processar comandos em linguagem natural para adicionar, remover e alterar quantidades de itens, aplicar regras de restrição (listas proibidas) e enviar lista de itens por e-mail.

## Tecnologias utilizadas
Foundry Agent Framework: Base para a construção e orquestração do agente  
Implantação: gpt-4o-mini  
Conhecimento: Arquivo txt contendo uma lista de itens inicial  
Ações: Envio de email

## Instruções e funcionamento do Agente
Adiciona item novo  
Aumenta/diminui quantidade de item existente  
Exclui item  
Impede itens proibidos (bebida alcoólica e enlatados)  
Envia email com lista atualizada  

### Fluxograma
![Fluxograma](Fluxo.jpg)

### Lista Inicial de Mantimentos
![Lista de mantimentos incial](ListaInicialMantimentos.jpg)

### Configuração do agente - Prints
![configuração do agente1.1](cfg1Agente.jpg)
![configuração do agente1.2](cfg2Agente.jpg)

### Video da configuração do agente 
![Video de configuração do agente](cfgAgente.gif)

### Demonstração da execução do agente
![Demonstração do agente](videochat.gif)

### Logs threads da execução
![Threasds da execução](Videologsthread.gif)

## Links de Referencias
[AI Foundry](https://learn.microsoft.com/en-us/azure/ai-foundry/agents/overview?view=foundry-classic)

[Challenge Azure Frontier Girls](https://github.com/Miyake-Diogo/AzureFrontierGirls-AI-Challenge/tree/main)

## Considerações/dificuldades
Em muitos testes, o agente não fazia a analise do arquivo txt na base de conhecimento, para validar o item solicitado pelo user. De modo, que trazia informações erradas. Nesses casos, era necessário pedir no chat para que ele usasse o arquivo.txt para continuar com os testes corretamente. Alterei várias vezes o prompt de instrução, mas mesmo assim, algumas iterações não saiam conforme o esperado. 
O envio de email era pra ser somente quando o usuário pedisse pra enviar, mas o agente dava a opção de envio de email, sem um pedido do usuário.




