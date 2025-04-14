# 🧠 colab-llm

Run **local LLM models on Google Colab** and access them remotely via API — ideal for lightweight, cost-effective development and testing using [Ollama](https://ollama.com/) and [Cloudflare Tunnel](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/).

> ✅ Access your Colab-hosted LLM API from anywhere — even inside VS Code using the [ROO Code](https://marketplace.visualstudio.com/items?itemName=roo-ai.roo) extension!

---

## 🚀 Try it now

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/colab-llm/blob/main/colab-llm.ipynb)

---

## 🧩 Features

- 🔥 Run advanced LLMs (like Qwen, LLaMA3, Mistral, DeepSeek) in Colab using [Ollama](https://ollama.com/)
- 🌐 Expose the model via secure public URL using `cloudflared`
- 🧑‍💻 Integrate with [ROO Code](https://roo.dev) in VS Code for seamless coding assistance
- ✅ Automatically detects and waits for Ollama to be ready before tunneling
- 💡 Simple, professional, and reusable setup

---

## 🛠️ Requirements

- A Google Colab account
- A GPU runtime (preferably **T4 High-RAM** or better)
- No installation or cloud account needed for Cloudflare tunneling

---

## 📝 How It Works

1. Installs and launches **Ollama** in the background
2. Pulls the selected model (e.g., `maryasov/qwen2.5-coder-cline:7b-instruct-q8_0`)
3. Waits until Ollama is running and responsive
4. Starts a **Cloudflare tunnel** to expose `http://localhost:11434`
5. Prints a public `.trycloudflare.com` URL — ready to use

---

### ▶️ Usage Instructions

Follow these steps to get your local LLM running in Colab and accessible via public API:

1. **Import the `.ipynb` notebook into your Google Colab**  
   - Open [colab.research.google.com](https://colab.research.google.com) and upload the notebook.
   - Or use the "Open in Colab" badge above.

2. **Choose the runtime as `T4 GPU`**  
   - Go to `Runtime > Change runtime type` → select:
     - Hardware accelerator: **GPU**
     - GPU type: **T4**
   - **Note: Colab GPU sessions last up to ~3 hours before disconnecting. Then you can restart it.**

3. **Run all cells**  
   - Click `Runtime > Run all`  
   - Wait for the cells to complete. Model download can take a few minutes.

4. **Verify the API is working in Step 7**  
   - You'll see a generated public `trycloudflare.com` URL
   - The cell will also run a test `curl` request

5. **Click the public link**  
   - You should see the message: **“Ollama is running”**
   - This confirms the API is live and ready to be used from tools like **curl** or **ROO Code in VS Code**

---

## 💡 Use with ROO Code (VS Code Extension)

1. Install [ROO Code extension](https://marketplace.visualstudio.com/items?itemName=roo-ai.roo)
2. Open extension settings
3. Choose API Provider as **Ollama**
4. Paste the public URL from Colab (e.g. `https://bold-sky-1234.trycloudflare.com`) **(Do not include `/` at the end of the link)**
5. Choose your model
6. Done! You can now prompt your Colab-hosted model from your local VS Code 💬

---

## 🤝 Contributions

Feel free to open issues, suggest improvements, or submit pull requests. Let's make local model hosting accessible for everyone!