# Canal de licenciamento

Arquivos de status assinados, consultados pelas instalações do sistema.

Cada arquivo em `comandos/` contém um comando assinado (Ed25519) destinado
a uma instalação específica. A instalação consulta o seu arquivo
periodicamente e só aplica o conteúdo se a assinatura conferir com a chave
pública embutida no software.

**Este repositório é público de propósito**: assim as instalações leem sem
nenhuma credencial. Não há segredo aqui — a chave que assina os comandos
nunca sai da máquina do fornecedor, e sem ela nada do que estiver neste
repositório é aceito por instalação nenhuma.

Não edite os arquivos à mão: um conteúdo alterado perde a assinatura e é
descartado pela instalação.

## Endereço de consulta

As instalações consultam **`https://licencas.neohealth.com.br/comandos/<instalação>.json`**,
e não este repositório diretamente. O endereço fica gravado no servidor de
cada cliente: com o domínio na frente, trocar este repositório de conta, de
nome ou de serviço não obriga a entrar em instalação por instalação.

Quem serve o domínio é o Worker do site da NeoHealth, que lê daqui. O
`raw.githubusercontent.com` continua funcionando para as instalações
anteriores a 22/09/2026.
