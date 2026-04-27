# Facebook Marketplace Posting Automation

## 📋 Description
This project aims to automate the creation of listings on Facebook Marketplace through interface automation using the libraries **PyAutoGUI**, **PyTesseract**, **Keyboard**, **Tkinter**, and **Webbrowser**.

The automation:
- Checks whether the user is logged into Facebook.
- Accesses the Marketplace.
- Creates listings automatically based on predefined variables without repeating photos.
- Adds photos, title, price, category, condition, color, brand, description, tags, location, and delivery options.

## 🎯 Motivation
The motivation for developing this project came from a real need I encountered while doing freelance work in sales. During that time, I had to manually create multiple listings on Facebook Marketplace and realized how repetitive and exhausting the process was. This led to the idea of automating these postings, optimizing time and making the process more efficient. Additionally, I am currently learning Python and studying with the book *Think Python*, so this project also serves as a practical opportunity to apply what I’ve been learning.

## ✅ Features
- Automatic Facebook login verification using OCR.
- Popup notification if the user is not logged in.
- Automated creation of multiple listings.
- Automatic image insertion and form filling.
- Configuration of sales location and delivery options.

## 🛠 Technologies Used
- Python 3.11+
- PyAutoGUI
- PyTesseract
- Keyboard
- Tkinter
- Pillow
- Webbrowser

## 📂 Project Structure
``` bash
Automacao-com-python/
│
├─ controle_interface/
│ ├─ marketplace.png
│ ├─ novo.png
│ ├─ item.png
│ ├─ fotos.png
│ ├─ moveis.png
│ ├─ cond_novo.png
│
├─ publicar_marketplace.py (main automation script)
├─ README.md
├─ englishversion.md
```

## ⚙️ Initial Setup
1. Clone or download the repository.
2. Make sure **Tesseract OCR** is installed and configured in your PATH.
3. Install the dependencies:
```bash
pip install pyautogui pytesseract keyboard pillow
```
4. In the ```posicao.py``` file, adjust the path variables and images according to your local environment. Important: the code uses generic paths and placeholders — you must update them to match your environment.
Example initial configuration in the code:
```python
# Path to the image folder
caminho = r"C:/your/path/to/images"

# Default listing data
titulo = 'Your custom title here'
preco = 'Price value'
cores = 'Available colors'
marca = 'Your brand'
descricao = 'Detailed product description'

# List of posting locations
locais = ['List of cities']

# Additional settings
retirada = True
entrega = True
iniciar_em = 0
maximo_post = 10
tempo_espera = 20  # time between each post
```

## ▶️ How to Use
1. Run the publicar_marketplace.py script.
2. Facebook will open automatically.
3. The system will check if you are logged in. If not, a popup will be displayed and the automation will retry after 1 minute.
4. Once logged in, the posting process will start automatically.
5. The script will publish listings sequentially based on the configured information.
   
## 📸 Important Notes
Interface images may need to be updated if Facebook’s layout changes.
Use the same screen resolution used when creating the images to avoid detection failures.
The system is set to attempt login verification up to 5 times before aborting.

## 👩‍💻 Author
Project created by Ana Luisa Rodrigues.

## 💡 Contributions
Contributions are very welcome! If you would like to suggest improvements, open an issue or submit a pull request.

⚠ Warning: This automation is intended for personal use. Any commercial use or use that violates Facebook’s terms of service is the sole responsibility of the user.
