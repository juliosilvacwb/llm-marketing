# 🤖 Gerador de Conteúdo com IA

Uma aplicação web inteligente que utiliza Inteligência Artificial para gerar conteúdo otimizado para marketing digital, com foco em SEO e escrita persuasiva.

## ✨ Características

- **🎯 SEO Otimizado**: Gera conteúdo otimizado para mecanismos de busca
- **📱 Multiplataforma**: Suporte para Instagram, Facebook, LinkedIn, Blog e E-mail
- **🎨 Tom Personalizado**: Diferentes tons de escrita (Normal, Informativo, Inspirador, Urgente, Informal)
- **👥 Público-alvo Específico**: Adaptação para diferentes demografias
- **📏 Controle de Tamanho**: Conteúdo curto, médio ou longo
- **📞 CTA Personalizado**: Inclusão de chamadas para ação customizadas
- **🏷️ Hashtags Automáticas**: Geração de hashtags relevantes
- **🔍 Palavras-chave SEO**: Otimização com palavras-chave específicas
- **⚡ Interface Intuitiva**: Interface web simples e responsiva com Streamlit

## 🚀 Tecnologias Utilizadas

- **Python 3.8+**
- **Streamlit** - Interface web
- **LangChain** - Framework para aplicações de IA
- **Groq** - API de LLM (Llama 3.1 70B)
- **OpenAI** - API alternativa (GPT-4o-mini)
- **python-dotenv** - Gerenciamento de variáveis de ambiente

## 📋 Pré-requisitos

- Python 3.8 ou superior
- Conta na [Groq](https://console.groq.com/) (gratuita)
- Conta na [OpenAI](https://platform.openai.com/) (opcional)

## 🛠️ Instalação

1. **Clone o repositório**
   ```bash
   git clone https://github.com/seu-usuario/llm-marketing.git
   cd llm-marketing
   ```

2. **Crie um ambiente virtual**
   ```bash
   python -m venv venv
   
   # Windows
   venv\Scripts\activate
   
   # macOS/Linux
   source venv/bin/activate
   ```

3. **Instale as dependências**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure as variáveis de ambiente**
   
   Crie um arquivo `.env` na raiz do projeto:
   ```env
   GROQ_API_KEY=sua_chave_api_groq
   OPENAI_API_KEY=sua_chave_api_openai
   ```

## 🔧 Configuração das APIs

### Groq (Recomendado)
1. Acesse [console.groq.com](https://console.groq.com/)
2. Crie uma conta gratuita
3. Gere sua API key
4. Adicione no arquivo `.env`:
   ```env
   GROQ_API_KEY=groq_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
   ```

### OpenAI (Opcional)
1. Acesse [platform.openai.com](https://platform.openai.com/)
2. Crie uma conta e adicione créditos
3. Gere sua API key
4. Adicione no arquivo `.env`:
   ```env
   OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
   ```

## 🎯 Como Usar

1. **Execute a aplicação**
   ```bash
   streamlit run app.py
   ```

2. **Acesse no navegador**
   ```
   http://localhost:8501
   ```

3. **Preencha os campos**:
   - **Tema**: Assunto principal do conteúdo
   - **Plataforma**: Onde será publicado
   - **Tom**: Estilo de escrita desejado
   - **Tamanho**: Comprimento do texto
   - **Público-alvo**: Demografia específica
   - **CTA**: Chamada para ação (opcional)
   - **Hashtags**: Se deseja incluir hashtags
   - **Palavras-chave**: Para otimização SEO

4. **Clique em "Gerar conteúdo"** e aguarde o processamento

## 📁 Estrutura do Projeto

```
llm-marketing/
├── app.py              # Aplicação principal
├── requirements.txt    # Dependências Python
├── .env               # Variáveis de ambiente (criar)
├── .gitignore         # Arquivos ignorados pelo Git
├── README.md          # Este arquivo
└── venv/              # Ambiente virtual (não versionado)
```

## 🔧 Configurações Avançadas

### Alterando o Modelo de IA

No arquivo `app.py`, você pode alternar entre os modelos:

```python
# Para usar Groq (Llama 3.1 70B)
llm = llama

# Para usar OpenAI (GPT-4o-mini)
llm = chatgpt
```

### Personalizando o Prompt do Sistema

Modifique a mensagem do sistema na função `llm_generate`:

```python
template = ChatPromptTemplate.from_messages([
    ("system", "Sua mensagem personalizada aqui..."),
    ("human", "{prompt}"),
])
```

## 🎨 Exemplos de Uso

### Exemplo 1: Post para Instagram
- **Tema**: Alimentação saudável
- **Plataforma**: Instagram
- **Tom**: Inspirador
- **Tamanho**: Curto
- **Público-alvo**: Jovens adultos
- **CTA**: "Descubra mais receitas saudáveis"
- **Hashtags**: ✅ Ativado

### Exemplo 2: Artigo para Blog
- **Tema**: Saúde mental no trabalho
- **Plataforma**: Blog
- **Tom**: Informativo
- **Tamanho**: Longo
- **Público-alvo**: Geral
- **Palavras-chave**: bem-estar, produtividade, equilíbrio

## 🐛 Solução de Problemas

### Erro de API Key
```
Erro: Invalid API key
```
**Solução**: Verifique se as chaves API estão corretas no arquivo `.env`

### Erro de Conexão
```
Erro: Connection timeout
```
**Solução**: Verifique sua conexão com a internet e tente novamente

### Erro de Dependências
```
ModuleNotFoundError: No module named 'streamlit'
```
**Solução**: Execute `pip install -r requirements.txt`

## 🤝 Contribuindo

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 🙏 Agradecimentos

- [Groq](https://groq.com/) - Por fornecer acesso gratuito ao Llama 3.1 70B
- [LangChain](https://langchain.com/) - Framework para aplicações de IA
- [Streamlit](https://streamlit.io/) - Framework para aplicações web

## 📞 Suporte

Se você encontrar algum problema ou tiver sugestões, por favor:

1. Abra uma [issue](https://github.com/seu-usuario/llm-marketing/issues)
2. Entre em contato: julio.silva.cwb@gmail.com

---

**⭐ Se este projeto foi útil para você, considere dar uma estrela no repositório!** 