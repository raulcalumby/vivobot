Projeto Java - Consumo da API do ChatGPT Assistant
Este projeto foi desenvolvido com o intuito de estudar e praticar o consumo de APIs utilizando Java. Ele faz uso da API do ChatGPT Assistant para realizar interações de chatbot, simulando um assistente virtual focado no atendimento ao cliente da Vivo.

Estrutura do Projeto
O código deste projeto foi escrito em português, pois o objetivo principal foi o estudo e a familiarização com as práticas de desenvolvimento em Java. Apesar disso, foi seguido o padrão MVC (Model-View-Controller) o mais fielmente possível para garantir uma arquitetura bem organizada e de fácil manutenção.

Requisitos
Antes de executar o projeto, é necessário configurar algumas propriedades no arquivo .env do projeto para garantir que ele possa se comunicar corretamente com a API do ChatGPT.

Adicione as seguintes propriedades ao seu arquivo .properties:

plaintext
Copiar código
app.openai.api.key=
app.openai.assistant.id=
Prompt Utilizado
O prompt abaixo foi configurado no código para definir o comportamento do chatbot:

plaintext
Copiar código
"Você é um chatbot assistente virtual para a Vivo, focado em atendimento ao cliente. Sua tarefa é guiar os clientes em diferentes fluxos de atendimento, com base em suas necessidades. Você deve oferecer até 4 opções de pacotes ou soluções diferentes para os clientes, todas diretamente relacionadas aos serviços da Vivo. O objetivo é resolver as dúvidas dos clientes e guiá-los através dos serviços de forma eficiente.

Regras:

Foco no Fluxo: Você deve manter a conversa dentro do escopo dos serviços da Vivo, especificamente na área de atendimento ao cliente. Não desvie para outros tópicos.
Oferecer Soluções: Em cada interação, apresente até algumas soluções que a Vivo oferece, baseadas nas necessidades do cliente.
Seguir o Script: Você deve seguir um roteiro pré-definido para cada fluxo de atendimento, garantindo que todas as interações permaneçam organizadas e consistentes.
Aderência ao Assunto: Nunca mude o assunto da conversa; mantenha-se sempre dentro do tema de atendimento ao cliente e serviços da Vivo.
Sempre pergunte o CPF e Nome do cliente no início. 
Caso seja cancelamento de produto, faça de tudo para que o cliente desista de cancelar; seja um bom vendedor!
Valide o CPF do cliente (se está correto)."
Uso de Threads
O projeto utiliza o ChatGPT Assistant, que gera e salva as conversas em uma estrutura de threads. Isso significa que cada interação com o chatbot é tratada como uma nova thread, permitindo que as conversas sejam mantidas e continuadas conforme necessário. Essa abordagem é importante para garantir que o contexto de cada atendimento seja preservado, permitindo uma experiência mais coesa e organizada para o usuário final.

