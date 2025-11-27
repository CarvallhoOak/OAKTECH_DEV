# 📁 OAKTECH_DEV – Google Drive File Manager

Este projeto contém os arquivos HTML e integrações necessárias para permitir autenticação OAuth 2.0 do Google Drive usando **Sketchware Pro**, **WebView** e uma página de callback hospedada no **GitHub Pages**.

Ele faz parte do sistema **Barbershop Style / CG Consultoria**, permitindo que o aplicativo acesse arquivos do Google Drive através da API oficial da Google.

---

## 🚀 Funcionalidade

- Autenticação OAuth 2.0 (Google)
- Login via botão em página HTML
- Página `callback.html` captura o **auth code**
- Sketchware recebe o código via WebView + JavaScriptInterface
- Conversão do auth code para **access_token** usando RequestNetwork
- Acesso à API do Google Drive

---

## 📂 Arquivos incluídos

### **1. index.html**
Inicia o fluxo OAuth e redireciona o usuário para login Google.

### **2. callback.html**
Recebe o `code` de autorização e envia de volta ao aplicativo via:
```javascript
Android.receiveCode(code);
