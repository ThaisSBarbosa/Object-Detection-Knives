# Hackathon - TC5 - FIAP IA para Devs

## Descrição
Este projeto utiliza o modelo YOLOv8 para detectar objetos cortantes (como facas) em vídeos. Ele também emite alertas por e-mail com uma imagem capturada do objeto detectado. O código foi desenvolvido para ser executado em qualquer IDE que suporte Python.

---

## Pré-requisitos

1. **Python 3.8 ou superior** instalado.
2. **Bibliotecas necessárias**:
   - `ultralytics`
   - `roboflow`
   - `opencv-python`
   - `yt-dlp`
   - `requests`
3. **Conta no Roboflow** para acessar datasets.
4. **Conta no Mailtrap** para envio de e-mails de alerta.

---

## Instalação

1. Instale as dependências:
   ```bash
   pip install ultralytics roboflow opencv-python yt-dlp requests
   ```

---

## Configuração

1. **Configurar a API Key do Roboflow**:
   - Substitua a chave `roboflow_api_key` no código pela sua chave de API do Roboflow.

2. **Configurar a API Key do Mailtrap**:
   - Substitua o valor de `Authorization` no cabeçalho do e-mail pela sua chave de API do Mailtrap. Altere também o link da API e a conta de email.

3. **Escolha a origem do vídeo**:
   - No código, altere a variável `opcao` para:
     - `1`: Fazer upload de um vídeo.
     - `2`: Baixar um vídeo do YouTube.
     - `3`: Usar um caminho local para o vídeo.

4. **Configurar o modelo YOLOv8**:
   - Certifique-se de que o modelo `best.pt` está no caminho correto especificado no código, caso não queira retreinar o modelo, mas apenas carregá-lo.

---

## Execução

1. Execute o script no terminal ou na sua IDE:
   ```bash
   python nome_do_arquivo.py
   ```

2. O script irá:
   - Processar o vídeo.
   - Detectar objetos cortantes.
   - Emitir alertas por e-mail.
   - Salvar o vídeo processado com as detecções.

---

## Resultados

- O vídeo processado será salvo no caminho especificado pela variável `nome_video_output`.
- O total de objetos detectados será exibido no console.

---

## Observações

- Certifique-se de que o vídeo de entrada está no formato compatível (como `.mp4`).
- Para treinar o modelo YOLOv8, ative a variável `forcar_retreinar_modelo` no código.

---

**Nota**: Este projeto foi desenvolvido como parte do Hackathon TC5 da FIAP.