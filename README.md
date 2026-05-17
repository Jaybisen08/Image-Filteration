# 🖼️ Image Filter Application

<div align="center">

✨ *A simple image editing web app built using Streamlit & Pillow* ✨

</div>

---

# 📌 Description

The **Image Filter Application** is a simple and interactive web application built using **Python**, **Streamlit**, and **Pillow (PIL)**.  

Users can upload images and apply different filters such as:

🎨 Grayscale  
🌫️ Blur  
🪄 Emboss  

The processed image can also be downloaded directly from the application.

---

# 🚀 Features

✅ Upload PNG/JPG/JPEG images  
✅ Apply multiple image filters  
✅ Real-time image preview  
✅ Download filtered image  
✅ Beginner-friendly project  
✅ Interactive UI with Streamlit  

---

# 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| 🐍 Python | Programming Language |
| 🎈 Streamlit | Web Application Framework |
| 🖼️ Pillow (PIL) | Image Processing |

---

# 📂 Project Structure

```bash
📦 Image-Filter-App
 ┣ 📜 app.py
 ┣ 📜 requirements.txt
 ┗ 📜 README.md
```

---

# ⚙️ Installation

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

---

## 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 📦 Requirements

Create a `requirements.txt` file and add:

```txt
streamlit
pillow
```

---

# ▶️ Run the Application

```bash
streamlit run app.py
```

---

# 💻 Source Code

```python
import streamlit as st
from PIL import Image, ImageFilter

st.title("Image Filter Application")

file = st.file_uploader(
    "select image", type=["png", "jpg", "jpeg"]
)

if file:

    option = st.selectbox(
        label="select filter option",
        options=["Real", "GrayScale", "Blur", "Emboss"]
    )

    img = Image.open(file)

    if option == "GrayScale":
        img = img.convert("L")

    if option == "Blur":
        img = img.filter(ImageFilter.BLUR)

    if option == "Emboss":
        img = img.filter(ImageFilter.EMBOSS)

    st.image(img)

    file.seek(0)
    img.save(file, format="PNG")

    st.download_button(
        "download",
        data=file,
        file_name="image.png"
    )
```

---

# 🎨 Available Filters

| Filter | Description |
|--------|-------------|
| 🖼️ Real | Original Image |
| ⚫ GrayScale | Converts image to black & white |
| 🌫️ Blur | Applies blur effect |
| 🪄 Emboss | Adds emboss texture effect |

---

# 📸 Output Preview

📷 Upload an image → Apply filter → Download processed image

---

# 🌟 Future Improvements

🔹 Add more filters  
🔹 Brightness & contrast adjustment  
🔹 AI image enhancement  
🔹 Image resizing feature  
🔹 Rotate & crop tools  
🔹 Dark mode UI  

---

# 👨‍💻 Author

## Jay Bisen

💡 Passionate about AI, ML & Web Development

---

# 📄 License

📝 This project is open-source and available under the **MIT License**.

---

<div align="center">

⭐ If you like this project, don't forget to star the repository ⭐

</div># Image-Filteration
