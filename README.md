# Assistente de Comando por Voz para Google Colab

Um sistema de reconhecimento de voz que executa ações no Google Colab, especialmente desenvolvido para abrir o YouTube através de comandos de voz.

## 🚀 Funcionalidades
- **Reconhecimento Vocal** em tempo real
- **Conversão Automática** WebM → WAV
- **Ações Específicas** (Abrir YouTube/Sair)
- **Feedback por Voz** usando gTTS (Google)
- **Controle de Tentativas** (3 tentativas máximas)

## 📦 Instalação
```python
!pip install gTTS SpeechRecognition pydub
!apt-get install ffmpeg -qq
🛠️ Como Usar
Execute o script no Google Colab

Permita acesso ao microfone

Comandos válidos:

"youtube" → Abre YouTube

"exit" → Encerra programa

Fale próximo ao microfone após ver "Aguardando comando..."

🔧 Estrutura do Código
plaintext
Copy
AudioRecorder (Classe)
├── JavaScript Encapsulado
├── Gravação WebM (5s)
└── Conversão Base64

Pipeline Principal:
Gravação → Conversão → Reconhecimento → Ação
🚨 Tratamento de Erros
Erro Comum	Solução
Microfone bloqueado	Verificar permissões do navegador
Áudio não reconhecido	Falar mais claro/evitar ruídos
Erro de dependência	Reinstalar pacotes
⚠️ Limitações
Funciona apenas no Google Colab

Requer conexão com internet

Precisão varia com qualidade do áudio

Comandos apenas em inglês

📝 Exemplo Completo de Código
python
Copy
# [Todo o código fornecido na última versão funcional]
# Inclui todas as classes e funções necessárias
🔄 Fluxo de Trabalho
mermaid
Copy
graph TD
    A[Início] --> B{Microfone Ativo?}
    B -->|Sim| C[Gravar 5s]
    C --> D[Converter para WAV]
    D --> E{Comando Válido?}
    E -->|YouTube| F[Abre Site]
    E -->|Exit| G[Encerra]
    E -->|Não| H[Conta Tentativa]
    H -->|3 Erros| G
📌 Dicas Importantes
Primeiro uso pode demorar 10-20s para carregar dependências

Clique manual no player de áudio pode ser necessário

Use fones de ouvido para melhor qualidade de áudio

Teste em ambiente silencioso

📄 Licença
MIT License - Livre para uso e modificação
