# 🚨 Sistema de Detecção de Intrusão com YOLOv8 e OpenCV 

Este projeto implementa um sistema simples de **detecção de intrusão** em vídeo usando o modelo pré-treinado **YOLOv8** da Ultralytics para detectar pessoas, combinado com uma área de alarme definida manualmente.

---

## 📝 Descrição

O sistema processa um vídeo de entrada e identifica pessoas presentes na cena. Se uma pessoa entra em uma área sensível pré-definida (definida por um retângulo com coordenadas específicas), o sistema:

- 👁️ Exibe uma indicação visual destacando a área invadida.
- ⚠️ Imprime no console a mensagem **"Alerta"**.
- 🔔 Executa um alarme sonoro (bipe) para alertar sobre a intrusão.

---

## ⚙️ Pré-requisitos

- 🐍 Python 3.8 ou superior
- 🐍 Biblioteca [Ultralytics YOLO](https://github.com/ultralytics/ultralytics)
- 📷 OpenCV (`opencv-python`)
- 🔊 Biblioteca `winsound` (somente Windows)
- 🔄 `threading` (módulo padrão do Python)

---

## 🚀 Instalação

1. Clone este repositório:

```bash
git clone https://github.com/seuusuario/deteccao_intrusao_yolov8.git
cd deteccao_intrusao_yolov8
````

2. Instale as dependências:

```bash
pip install ultralytics opencv-python
```

> ⚠️ **Nota:** A biblioteca `winsound` é padrão do Windows. Se estiver usando Linux/macOS, será necessário adaptar o som do alarme.

---

## ▶️ Uso

1. Coloque seu vídeo na pasta do projeto (exemplo: `ex01.mp4`).

2. Defina a área sensível editando a variável `area` no código Python (`main.py`):

```python
area = [x1, y1, x2, y2]
```

onde `(x1, y1)` é o canto superior esquerdo e `(x2, y2)` o canto inferior direito do retângulo da zona de alarme.

3. Execute o script:

```bash
python main.py
```

4. A janela exibirá o vídeo com marcações da área sensível e caixas delimitadoras para pessoas detectadas. Quando uma pessoa estiver dentro da área, será exibido um alerta visual e o alarme sonoro será disparado.

---

## ⚠️ Limitações e próximos passos

* Área sensível é definida manualmente no código.
* O modelo YOLOv8 padrão detecta apenas pessoas, não portas, muros ou outras zonas.
* Alarme sonoro funciona apenas no Windows (`winsound`).
* Em um futuro próximo com amostras que detectam automaticamente áreas sensíveis(portas, entradas, cercas, partes de cima do mudo(para saltos))

---

## 📚 Referências

* [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
* [OpenCV](https://opencv.org/)
* [Label Studio](https://labelstud.io/) (para anotação customizada)

---

## 👤 Dev

Gustavo Souza de Lima - [GustavoLimma@email.com](gustavo69gls@email.com)

---
