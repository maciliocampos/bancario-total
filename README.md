# Painel WhatsApp Bancário Total com Integração LM Studio

Um painel completo para WhatsApp que permite envio de mensagens em massa e resposta automática com IA usando LM Studio.

## Recursos

- Interface visual para gerenciamento de WhatsApp
- Envio de mensagens em massa para vários contatos
- Integração com LM Studio para resposta automática com IA
- Histórico de mensagens enviadas e recebidas
- Detecção de interesse do cliente em fechar negócio

## Instalação

Esse projeto foi configurado para funcionar com apenas um clique no Windows 11.

### Pré-requisitos

- Node.js (versão 14 ou superior) instalado no seu computador
  - Baixe em: https://nodejs.org/ (escolha a versão LTS)
- LM Studio instalado e configurado
  - Configure o servidor da API na porta 1234
  - Carregue o modelo `gemma-3-12b-it@q4_k_m` (ou atualize o código para usar outro modelo)

### Instruções

1. Descompacte o arquivo ZIP em qualquer pasta do seu computador
2. Inicie o LM Studio e habilite o servidor de API na porta 1234
3. Dê dois cliques no arquivo `iniciar-projeto.bat`
4. Aguarde a instalação e inicialização
5. O navegador abrirá automaticamente com o painel

## Como usar

1. **Conexão**:
   - Na primeira execução, você verá um QR Code
   - Abra o WhatsApp no seu celular
   - Toque em Menu > WhatsApp Web > Vincular dispositivo
   - Escaneie o QR Code

2. **Cadastro de números**:
   - Adicione os números no formato DDDNúmero (ex: 11987654321)
   - Um número por linha
   - Clique em "Salvar Lista"

3. **Mensagem**:
   - Digite a mensagem que deseja enviar
   - Clique em "Salvar Mensagem"

4. **Envio**:
   - Clique no botão "Enviar mensagem para lista"
   - Aguarde a confirmação
   - As mensagens aparecerão no histórico

5. **Resposta Automática**:
   - O sistema responderá automaticamente a todas as mensagens recebidas
   - Utiliza o LM Studio com o modelo configurado
   - Detecta intenções de fechamento de negócio

## Detecção de Interesse em Fechar Negócio

O sistema detecta automaticamente quando:

1. Um cliente demonstra interesse em fechar negócio (palavras-chave como "quero contratar", "fechar negócio", etc.)
2. A IA indica que um negócio foi fechado com o cliente

Quando isso acontece, uma notificação é enviada para o número configurado (5574991027579).

## Configurações Avançadas

Para personalizar as configurações do sistema:

- Altere o modelo de IA no arquivo `backend/index.js`
- Modifique os números para alerta de fechamento
- Ajuste as palavras-chave de detecção de intenção

## Solução de Problemas

- **QR Code não aparece**: Reinicie o aplicativo e verifique as permissões do navegador
- **Erro de conexão**: Verifique se o WhatsApp no celular está conectado à internet
- **LM Studio não responde**: Verifique se o servidor de API está ativo na porta 1234

## Suporte

Para dúvidas ou problemas com o painel, consulte a documentação ou entre em contato com o suporte.
