# YT-video-metadata-recovery
Este é um report, desenvolvido em Python na plataforma Google Colaboratory, que nos permite buscar uma lista de no máx 50 vídeos do Youtube, com seus respectivos metadados (ou seja, 'id', 'title', 'channel', 'date_p', 'description', 'views', 'likes', 'dislikes', 'comments'); além dos seus captions (transcripts/subtitles), quando disponível.

Google Colab --> [Extração de metadados de videos do youtube-v1.0](https://colab.research.google.com/drive/1sOmkq6zT5dyzEvjC9vrMbgc_prcIr_uh?usp=sharing)

<h3> Desenvolvido por:</h3>

* Elton Alencar (enda@icomp.ufam.edu.br)

* Victoria Guimaraes(vsg@icomp.ufam.edu.br)

<h2>Most important links!</h2>

<h3>Google colab</h3>

É um ambiente de desenvolvimento Python, que é executado diretamente no Browser comum (Chrome, Firefox, etc).

* [Overview of Colaboratory Features](https://colab.research.google.com/notebooks/basic_features_overview.ipynb)

* [Olá, este é o Colaboratory](https://colab.research.google.com/notebooks/intro.ipynb#scrollTo=GJBs_flRovLc)

* [l01c01_introduction_to_colab_and_python.ipynb](https://colab.research.google.com/github/tensorflow/examples/blob/master/courses/udacity_intro_to_tensorflow_for_deep_learning/l01c01_introduction_to_colab_and_python.ipynb)

<h3>API do Youtube </h3>

* Acessar o link [https://developers.google.com/youtube/v3/getting-started?hl=pt-br] destinado a desenvolvedores que desejam criar aplicativos que interagem com o YouTube. Ele explica os conceitos básicos do YouTube e da própria API. Também oferece uma visão geral das diferentes funções compatíveis com a API.

* **Precisa ser assistido antes de começar: [Consumindo dados da API do YOUTUBE com Python | Python na Prática #11](https://www.youtube.com/watch?v=olDCJ1w3FLM)**

<h3>youtube-transcript-api 0.4.1</h3>

* Esta é uma API python que permite obter a transcrição / legendas de um determinado vídeo do YouTube. Ele também funciona para legendas geradas automaticamente, suporta tradução de legendas e não requer um navegador headless, como outras soluções baseadas em selênio exigem!

* Link: https://pypi.org/project/youtube-transcript-api/ 

<h2>Getting Started!</h2>

<h3>Google colab</h3>

* Fazer cópia do google colab: [Extração de metadados de videos do youtube-v1.0](https://colab.research.google.com/drive/1sOmkq6zT5dyzEvjC9vrMbgc_prcIr_uh?usp=sharing)


![image](https://user-images.githubusercontent.com/44116770/139159332-57aff8e1-6d24-4951-8f21-a31be5c3f744.png)

<h4> 1 - Executar célula com os install e imports necessários:</h4>

![image](https://user-images.githubusercontent.com/44116770/139159606-da3f5990-8e45-4607-9138-2d5df9497f1a.png)

<h4> 2 - Executar célula de Função e Métodos:</h4>

<h4> 3- Youtube API Key - Chave de segurança</h4>
 
 Para usar YouTube Data API, é necessário que seu aplicativo tenha credenciais de autorização ([Mais sobre, click aqui](https://developers.google.com/youtube/registering_an_application?hl=pt-br)).
 
 3.1 - Crie seu projeto e selecione serviços de API:
 
 3.2 -  Open the Credentials page in the API Console: https://console.developers.google.com/apis/credentials?hl=pt-br.
 
 3.3 - Criar novo projeto:
 
 ![image](https://user-images.githubusercontent.com/44116770/139160689-dd38a432-e0e9-4372-abfc-5e445c906ed6.png)
 
 3.4 - Criar credencial e copiar chave criada:
 
![image](https://user-images.githubusercontent.com/44116770/139160811-b59f9af0-46f8-4d43-b867-eef2d7f9c0ba.png)

![image](https://user-images.githubusercontent.com/44116770/139161018-bce65d6c-c896-4a6b-bd06-e27b7452d3fe.png)

3.5 - Ativar uso da API do YouTube no projeto criado:

![image](https://user-images.githubusercontent.com/44116770/139161576-b791547c-d20d-4b5a-87d2-79b2987d9b68.png)

3.5.1 - buscar pela API do youtube indicada na imagem:

![image](https://user-images.githubusercontent.com/44116770/139161667-7f72d0a2-8a7e-4454-b2c5-0f024bff7ac3.png)

3.5.2 - Ativar API:

![image](https://user-images.githubusercontent.com/44116770/139161717-39594d50-051e-4935-8cbc-17ff18bab187.png)


<h4> 4 - Atualizar o colab com a nova chave de API criada: </h4>

![image](https://user-images.githubusercontent.com/44116770/139161290-85318279-4e8c-4dea-b67b-296574fec514.png)

* executar celulas:

Saída esperada: ![image](https://user-images.githubusercontent.com/44116770/139161905-e5eb2e45-cac2-4b0e-9f42-8f4c36f13cf3.png)

<h4> 5 - Executar células responsáveis por fazer a busca dos vídeos e salvar os dados retornados em um csv </h4>

![image](https://user-images.githubusercontent.com/44116770/139162390-2e425d9c-0165-4339-aa3f-38a56cd9fbcc.png)

* Saída esperada:

![image](https://user-images.githubusercontent.com/44116770/139162485-9ac7e23b-e8ed-4d27-8f63-b60831262cde.png)

<h4> 6 - Executar célula que faz a busca e estração de caption para cada video da lista passada:
  
  ![image](https://user-images.githubusercontent.com/44116770/139162589-42e7720f-2416-4751-83e7-a0d970c5936f.png)

  aguardar:
  
  ![image](https://user-images.githubusercontent.com/44116770/139162626-a12d383a-6617-4e91-89a8-5be9107bd4fc.png)

 <h4> 7 - Visualizando o caption [legenda gerada automaticamente] de um dos vídeos:
   
   ![image](https://user-images.githubusercontent.com/44116770/139163098-7c02471e-2c1c-41c6-ae3c-56a59b871312.png)

   
## Sources:
* [YouTube - Data API](https://developers.google.com/youtube/v3/docs?hl=pt-br)

* [youtube-transcript-api 0.4.1](https://pypi.org/project/youtube-transcript-api/)

* [Google colab](https://colab.research.google.com/notebooks/intro.ipynb#scrollTo=GJBs_flRovLc)
   
