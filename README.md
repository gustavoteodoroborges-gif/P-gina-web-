# P-gina-web-
<div class="container">
  <div class="login-card">
    <h2>Bem-vindo de volta</h2>
    <p class="subtitle">Insira os seus dados para aceder à sua conta</p>
    
    <form id="loginForm">
      <div class="input-group">
        <label for="email">E-mail</label>
        <input type="email" id="email" placeholder="exemplo@email.com" required>
      </div>
      
      <div class="input-group">
        <label for="password">Palavra-passe</label>
        <input type="password" id="password" placeholder="••••••••" required>
      </div>
      
      <div class="form-actions">
        <label class="remember-me">
          <input type="checkbox"> Lembrar-me
        </label>
        <a href="#" class="forgot-password">Esqueceu-se da senha?</a>
      </div>
      
      <button type="submit" class="btn-primary">Entrar</button>
    </form>
    
    <div class="footer-text">
      Não tem uma conta? <a href="#">Registe-se aqui</a>
    </div>
  </div>
</div>
/* Configurações Globais e Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
  background: linear-gradient(135deg, #e0eafc, #cfdef3);
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

/* Card Principal */
.container {
  width: 100%;
  max-width: 420px;
  padding: 20px;
}

.login-card {
  background: #ffffff;
  padding: 40px 30px;
  border-radius: 16px;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
}

h2 {
  color: #1a1a1a;
  font-size: 28px;
  margin-bottom: 8px;
  font-weight: 600;
}

.subtitle {
  color: #666;
  font-size: 14px;
  margin-bottom: 32px;
}

/* Grupos de Input */
.input-group {
  margin-bottom: 20px;
  text-align: left;
}

.input-group label {
  display: block;
  color: #4a4a4a;
  font-size: 14px;
  margin-bottom: 8px;
  font-weight: 500;
}

.input-group input {
  width: 100%;
  padding: 12px 16px;
  border: 1.5px solid #e0e0e0;
  border-radius: 8px;
  font-size: 15px;
  transition: all 0.3s ease;
  outline: none;
}

/* Aprimoramento de Interface - Feedback Visual de Foco */
.input-group input:focus {
  border-color: #4f46e5;
  box-shadow: 0 0 0 4px rgba(79, 70, 229, 0.1);
}

/* Ações Extras do Formulário */
.form-actions {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 13px;
  margin-bottom: 24px;
}

.remember-me {
  color: #666;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 6px;
}

.forgot-password, .footer-text a {
  color: #4f46e5;
  text-decoration: none;
  font-weight: 500;
}

.forgot-password:hover, .footer-text a:hover {
  text-decoration: underline;
}

/* Botão Principal */
.btn-primary {
  width: 100%;
  padding: 14px;
  background-color: #4f46e5;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 16px;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.2s ease, transform 0.1s ease;
}

.btn-primary:hover {
  background-color: #4338ca;
}

.btn-primary:active {
  transform: scale(0.98);
}

/* Rodapé do Card */
.footer-text {
  text-align: center;
  margin-top: 28px;
  font-size: 14px;
  color: #666;
}
// Simulação de comportamento da interface
document.getElementById('loginForm').addEventListener('submit', function(event) {
  event.preventDefault(); // Impede a página de recarregar
  
  const email = document.getElementById('email').value;
  const password = document.getElementById('password').value;
  
  // Feedback visual simples de sucesso
  if(email && password) {
    alert(`Sucesso! Login efetuado para: ${email}`);
  }
});
