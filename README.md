## Análise de imagens no Vision Studio

Este projeto demonstra como utilizar o Vision Studio para analisar imagens. 

### Processo 

1. Criar um recurso de Azure AI
2. Conectar o serviço Azure AI ao Vision Studio
3. Gerar legendas para uma imagem
4. Marcação de imagens
5. Detecção de objetos
6. Limpeza

### Criar um recurso de Azure AI

1. Em um browser, abra o [Portal Azure](https://portal.azure.com/?azure-portal=true), logando com uma conta associada com uma subscrição do Azure.
2. Clique no botão **+ Create a resource** e pesquise por *Azure AI service*. Selecione  o plano **create a 
Azure AI services**.
3. Na página **Create Azure AI services**, configure-o com as seguintes configurações:
- **Subscription**: *Sua subscrição Azure*.
- **Resource group**: *Selecione ou crie um grupo de recurso com um nome único*.
- **Region**: East US
- **Name**: *Informe um nome único*.
- **Pricing tier**: *Standard S0*.
- **By checking this box I acknowledge that I have read and understood all the terms below**: *Selected.*
4. Selecione **Review + create** então **Create** e aguarde o deploy ser realizado.

### Conectar o serviço Azure AI ao Vision Studio

1. Em um browser, abra o [Vision Studio](https://portal.vision.cognitive.azure.com/), logando com uma conta associada com uma subscrição do Azure.
2. Clique em **View all resources** e selecione o recurso criado anteriormente e clique em **Select as default resource**.

### Gerar legendas para uma imagem

1. Em um navegador, vá para o [Vision Studio](https://portal.vision.cognitive.azure.com/?azure-portal=true).
2. Na página inicial **Introdução ao Vision**, selecione a guia **Análise de imagem** e, em seguida, seleciona o bloco **Adicionar legendas às imagens**.
3. No subtítulo **Experimente**, reconheça a política de uso de recusos lendo e marcando a caixa.
4. Na pasta **inputs** desse repositório contém algumas imagens para ser usadas no teste.
5. Realize o upload da imagem **store-camera-1.jpg** da pasta **inputs**.
6. Observe o texto da leganda gerado, visível no painel à direita da imagem **Atributos Detectados**.
7. Abaixo a imagem anexada e o resultado com as legendas da imagem criada

![store-camera-1.jpg](/inputs/store-camera-1.jpg)
![caption-image-result.png](/outputs/caption-image-result.png)

8. Agora vamos realizar o processo de legenda densa, onde ele fornece várias legendas legíveis para uma imagem, uma descrevendo o conteúdo da imagem, e outras, cada uma cobrindo os objetos essenciais detectados na imagem. Cada objeto possui uma caixa delimitadora, que define as coordenadas dos pixesl na imagem associada ao objeto.

![dense-caption-result.png](/outputs/dense-caption-result.png)

### Marcação de imagens

1. Retorne para a página inicial do Vision Studio, e então selecione o bloc **Extraia tags comuns de imagens** na guia **Análise de imagem**.
2. Em **Escolha o modelo que deseja experimentar**, deixe selecionado **Produto pré-construído vs. modelo de lacuna**. Em **Escolha seu idioma**, selecione **Inglês** ou um idioma de sua preferência.
3. Selecione a imagem **store-camera-2.jpg** da pasta **inputs** deste repositório.
4. Abaixo veja a imagem utilizada e o resultado obtido.

![store-camera-2.jpg](/inputs/store-camera-2.jpg)
![tags-from-image-result.png](/outputs/tags-from-image-result.png)

5. Revise a lista de tags extraídas da imagem e a pontuação de confiança de cada uma no painel de atributos detectados. Aqui a pontuação de confiança é probabilidade de o texto do atributo detectado descrever o que realmente está na imagem.

### Detecção de objetos

1. Retorne para a página inicial do Vision Studio, e então selecione o bloc **Detecte objetos comuns em imagens** na guia **Análise de imagem**.
2. Em **Escolha o modelo que deseja experimentar**, deixe selecionado **Produto pré-construído vs. modelo de lacuna**.
3. Selecione a imagem **store-camera-3.jpg** da pasta **inputs** deste repositório.

![store-camera-3.jpg](/inputs/store-camera-3.jpg)
![detect-object-in-images-result](/outputs/detect-object-in-images-result.png)

4. Passe o cursos do mouse sobre os objetos na lista de atributos detectados para destacar a caixa delimitadora do objeto na imagem.
5. Mova o controle deslizante **Threshold value** até que um valor de 70 seja exibido à direita do controle deslizante. Observe o que acontece com os objetos da lista. O controle deslizante de limite especifica que somente objetos identificados com uma pontuação de confiança ou probabilidade maior que o limite devem ser exibidos.

![detect-object-in-images-result2](/outputs/detect-object-in-images-result2.png)

### Limpeza

1. Abra o [Portal Azure](https://portal.azure.com/) e selecione o grupo de recursos que contém o recurso que você criou.
2. Selecione o recurso e clique em **Deletar** e então **Sim** para confirmar. O recurso foi deletado.
