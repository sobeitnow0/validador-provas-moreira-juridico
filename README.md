# 🛡️ Coleta e Preservação de Evidências Digitais

Uma ferramenta *Client-Side* focada na geração de cadeia de custódia e preservação de evidências digitais (como vídeos, capturas de tela e documentos). Desenvolvida sob a ótica do **Legal Design** e **Writing UIX**, visando a máxima eficiência probatória no judiciário brasileiro com atrito zero.

---

## 💡 O Problema que Resolvemos
O envio de "prints de WhatsApp" por clientes destrói metadados essenciais e gera provas frágeis e facilmente impugnáveis. 

Este sistema permite que o advogado pegue a evidência original (ex: gravação de tela ou exportação `.txt` do chat), calcule a sua impressão digital matemática (Hash SHA-256) e encapsule tudo em um **Relatório Técnico em PDF** com design limpo e direto, pronto para receber a assinatura eletrônica oficial.

## ✨ Features Principais
*   **100% Client-Side (Privacidade Absoluta):** O arquivo da evidência *nunca* é enviado para a internet. O cálculo criptográfico ocorre na memória RAM do navegador do usuário utilizando a `Web Crypto API` nativa.
*   **Zero Custo de Infraestrutura:** Sendo um site estático (HTML/JS/CSS puro), pode ser hospedado gratuitamente via GitHub Pages.
*   **Legal Design Aplicado:** O relatório PDF abandona o "juridiquês" excessivo e foca no Technical UIX — entregando os metadados de forma clara, estruturada e autoexplicativa para juízes e peritos.
*   **Integração com ICP-Brasil:** O fluxo do sistema prepara a prova para o encerramento legal via Token OAB (assinatura ICP-Brasil), conferindo presunção de veracidade conforme Art. 10, § 1º da Medida Provisória nº 2.200-2/2001.

---

## ⚖️ O Fluxo de Trabalho (Workflow Legal)

A utilização do sistema foi desenhada para ser à prova de erros na rotina do escritório:

1.  **Oriente a Produção da Prova:** O cliente produz a evidência robusta (gravação de tela navegando no aplicativo em vez de um simples print).
2.  **Processe no Sistema:** O advogado insere os dados de contexto e arrasta o arquivo original para o sistema. O Hash SHA-256 é calculado instantaneamente.
3.  **Encapsulamento (PDF):** O sistema gera automaticamente um relatório atestando a integridade daquele arquivo na data da coleta.
4.  **A Chancela (ICP-Brasil):** Fora do sistema, o advogado abre o PDF e assina com seu certificado digital (Token OAB). O carimbo do tempo oficial tranca a prova, garantindo validade jurídica inquestionável.

---

## 🚀 Como Executar e Publicar

Como a arquitetura não depende de banco de dados ou back-end (Node/Python), rodar a ferramenta é trivial:

### Teste Local
Basta clonar o repositório ou baixar o arquivo `index.html` e dar um duplo clique para abrir no seu navegador. 

### Hospedagem Gratuita via GitHub Pages
1. Faça o fork ou clone este repositório.
2. Vá em `Settings > Pages` no seu repositório do GitHub.
3. Em *Source*, selecione o branch `main` e salve.
4. Em instantes, o link seguro (`https://`) estará disponível para uso.
> **Nota técnica:** A geração de hash local via navegador requer um contexto seguro, portanto o uso de HTTPS (fornecido nativamente pelo GitHub Pages) é obrigatório.

---

## 🛠️ Tecnologias Utilizadas
*   **HTML5 / CSS3 / Vanilla JavaScript** (Sem frameworks pesados para garantir carregamento instantâneo).
*   **Web Crypto API:** Motor criptográfico nativo dos navegadores modernos para o SHA-256.
*   **[pdfmake](http://pdfmake.org/):** Biblioteca open-source para a compilação do relatório em PDF diretamente no front-end.

---

## 📝 Personalização
Se você deseja usar este sistema no seu escritório, abra o arquivo `index.html` e edite os dados do "Responsável Técnico" inserindo a sua qualificação, OAB e domínio.
