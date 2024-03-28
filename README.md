# Passo-a-passo para utilizar o análise de imagem 4.0 com o AI Vision Service
Caso você nunca tenha entrado em contato com o ambiente Azure, sugiro você começar por [este repositório](https://github.com/HugoCSouza/inicio-azure). Nele, eu ensino a configuração inicial do ambiente Azure para a criação de um modelo de Machine Learning.

## Primeiros passos
Entre no portal do [Azure]([url](https://portal.azure.com/#home)https://portal.azure.com/#home), logue na sua conta microsoft, e ao abrir sua interface, clique em criar um recurso.
![criando um recurso](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/afaa8215-5a16-43e7-81f2-6c937887732c)

No menu lateral esquerdo, em categorias, clique em "IA + Machine Learning" e selecione a opção **"Azure AI Services"**. (Obs: caso não seja encontrado direto clicando em "IA + Machine Learning", clique dentro dessa aba em "Veja mais em todos os serviços" e clique novamente em "IA + Machine Learning")
![Azure IA Services](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/9603e9d8-e1ea-4c3f-b7a5-7e1c481da8e4)

Dentro do Azure AI Services, escolha a aplicação que mais faz sentido de acordo com sua aplicação. Neste caso, criaremos um modelo de *"Face API"*, um de *"Computer vision"* e um de *"Document Intelligence"*.
![modelos](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/da43fc9d-fe6d-4f57-b22d-15f4f27ea62d)

Ao criar cada instância, deve se definir o nome, localização, tipo de assinatura, grupo de recursos, e preço (neste caso, Free). A configuração é similar para todos os modelos, basta preencher esse primeiro cenário e clicar em "examinar+criar" e se tudo estiver certo criar.
![criação](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/1d830901-73a6-43ac-a16a-881cde53aef8)

Após criar todos os modelos, deve se direcionar para o [Vision Studio]([url](https://portal.vision.cognitive.azure.com/)https://portal.vision.cognitive.azure.com/) para manipular as IAs.

## Vision Studio
A interface inicial no Vision Studio está demonstrada na imagem abaixo. Nela, você vai definir, a partir de um recurso, de tipo de aplicação será utilizada.
![Vision Studio](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/f7561ddf-2827-449e-aec5-c1bf2d2fe2c3)
Começaremos pelo modelo de reconhecimento facial, clicando em Face e selecionando a opção *"Detect faces in an image"*.
![escolha](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/0f6e049d-fbcb-461c-8c79-cfb7b4cc9957)

### Face API
Na seção *"Try out"*, marque a caixa de seleção e clique em *"please, select a resource"*. Nesta janela que abrir, selecione o recurso de *"Face API"* que você iniciou.
![image](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/6b102c0b-5241-4d57-873a-2e91c59206e4)
Ao descer a página, teremos algumas imagens de demonstração. Na caixa ao lado será infomada a resposta da IA conforme o que foi encontrada na imagem e se o rosto encontrada está ou não de máscara. Você pode enviar suas próprias imagens clicando onde a seta está indicando. 
![image](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/c3052418-260e-4bf6-ac20-8549eb170130)
Na caixa destacada, pode-se trocar o tipo de saída, sendo o arquivo JSON, um arquivo de saída com mais parâmetros de como foi reconhecida a face. Você pode alternar a saída ao seu bel-prazer
![image](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/3d8705cb-ec91-4014-93a5-8916901a3f14)
Na [pasta de imagens](inputs/faceapi), há algumas imagens que você pode utilizar para verificar o funcionamento da IA. Podemos ver que ela reconhece várias faces em uma imagem:
![image](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/4595ace0-50e7-4b72-b905-75d26fcf1c37)
Ou um rosto desenhado:
![image](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/7b8504fe-71b5-4370-9bf6-b298947f0e73)

As respostas de cada imagem em JSON está disponível tambem [neste repositório](outputs/faceapi).

### Computer vision
Para verificar a como a IA de visão computacional funciona, utilizaremos a função de adicionar legendas a imagem (em inglês, *"Add captions to image"*).
![image](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/5dc33017-0d24-40f4-9bb7-5a3a26835273)

Fazendo o mesmo processo de selecionar o recurso, concorda com os termos, temos imagens demonstrativas. Como podemos ver na imagem, a IA atribui uma legenda conforme a imagem. Na [pasta de imagens](url), terão 3 imagens diferentes para que você também possa testar a IA.
![image](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/a1d69832-e940-4ae7-8cee-b8fe7b2a1530)

Assim, como no exemplo anterior as [entradas](inputs/visual-computing) e [respostas em JSON](outputs/visual-computing) de cada imagem que disponibilizada neste repositório.

### Document Intelligence
Para utilizar a visão computacional para detectar texto em imagens, vamos selecionar o modelo *"Extract text from images"* dentro da aba *"Optical character recognition"*.
![image](https://github.com/HugoCSouza/imagem-aivision-azure/assets/150296370/365c9bc9-2a59-4ade-931e-08087e8833e5)

As [imagens de entrada](inputs/text-intelligence) e [saidas da IA](outputs/text-intelligence) estão disponíveis dentro desse repositório para verificação.

## Não se esqueça de excluir os recursos após o aprendizado para que não gere posíveis custos futuramente!

#### Este repositório foi feito com objetivo de demonstrar a configuração básica de uma ferramenta de AI Vision dentro do Azure, além de servir como base de avaliação dentro do bootcamp " Microsoft Azure AI Fundamentals" ministrado pela DIO. Qualquer sugestão, pode solicitar um pull request ou entrar em contato comigo via [linkedin](https://www.linkedin.com/in/hugo-cs-souza/)











