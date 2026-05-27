
# 📍 Lembretes por Localização - Alarme GPS

Um site web moderno para criar lembretes tipo alarme baseados na localização do usuário. Receba notificações automáticas quando chegar próximo a um local específico!

## ✨ Recursos

- **🎯 Rastreamento de Localização**: Usa geolocalização GPS para rastrear sua posição em tempo real
- **⏰ Alarmes Personalizados**: Crie lembretes com som, vibração ou ambos
- **📍 Raio de Ativação Customizável**: Defina a distância em que o alarme deve disparar (10-5000 metros)
- **💾 Armazenamento Local**: Todos os lembretes são salvos no navegador
- **🔔 Notificações do Navegador**: Receba notificações mesmo com a página em segundo plano
- **📱 Responsivo**: Funciona perfeitamente em desktop, tablet e mobile
- **🎨 Design Moderno**: Interface com tema azul marinho (#191970)

## 🚀 Como Usar

### 1. Abrindo o Site
Abra o arquivo `index.html` em qualquer navegador moderno que suporte:
- Geolocalização (GPS)
- Web Audio API
- LocalStorage
- Notificações

### 2. Permitir Acesso à Localização
Quando a página carregar, o navegador pedirá permissão para acessar sua localização. **Clique em "Permitir"** para que o app funcione corretamente.

### 3. Atualizar Localização
- Clique em **"🔄 Atualizar Localização"** para obter sua posição atual
- Sua latitude, longitude e precisão serão exibidas

### 4. Ativar Rastreamento Contínuo
- Clique em **"📡 Ativar Rastreamento"** para rastreamento em tempo real
- O app verificará continuamente se você está próximo aos seus lembretes

### 5. Criar um Lembrete
Preencha o formulário:
- **Título**: Nome do lembrete (ex: "Ir ao supermercado")
- **Descrição**: Detalhes adicionais (opcional)
- **Latitude/Longitude**: Coordenadas do local (você pode usar "📍 Usar Localização Atual" para preencher automaticamente)
- **Raio de Ativação**: Distância em metros até o local (padrão: 500m)
- **Tipo de Alarme**: Som, Vibração ou Ambos
- **Repetir**: Se deve disparar novamente ao chegar próximo

Clique em **"➕ Adicionar Lembrete"** para criar.

### 6. Gerenciar Lembretes
Na lista de lembretes:
- **Visualize**: Todas as informações do lembrete
- **Distância**: Veja a distância atual até o local
- **Edite**: Clique em "✏️ Editar" para modificar
- **Delete**: Clique em "🗑️ Deletar" para remover

### 7. Quando o Alarme Dispara
Quando você chegar próximo ao local:
1. Um **modal de alarme** aparecerá
2. O **som** tocará (se configurado)
3. O **navegador vibrará** (em dispositivos com suporte)
4. Uma **notificação** será exibida
5. Você pode:
   - **Descartar**: Fechar o alarme
   - **Adiar 5 min**: Silenciar o alarme por 5 minutos

## 📋 Estrutura de Arquivos

```
location-reminders/
├── index.html      # Estrutura HTML
├── styles.css      # Estilos CSS (com cor #191970)
├── script.js       # Lógica JavaScript
└── README.md       # Este arquivo
```

## 🎨 Paleta de Cores

- **Primária**: #191970 (Azul Marinho)
- **Primária Escura**: #0f0f4a
- **Primária Clara**: #2d2d99
- **Destaque**: #00bfff (Azul Ciano)
- **Sucesso**: #00ff00 (Verde)
- **Aviso**: #ffa500 (Laranja)
- **Erro**: #ff3333 (Vermelho)

## 🔧 Tecnologias Utilizadas

- **HTML5**: Estrutura semântica
- **CSS3**: Estilos responsivos com Flexbox e Grid
- **JavaScript**: Lógica da aplicação
- **Geolocation API**: Acesso ao GPS
- **Web Audio API**: Geração de sons
- **LocalStorage**: Persistência de dados
- **Vibration API**: Feedback tátil
- **Notifications API**: Notificações do navegador

## 🌐 Compatibilidade

| Navegador | Suporte |
|-----------|---------|
| Chrome | ✅ Total |
| Firefox | ✅ Total |
| Safari | ✅ Com limitações |
| Edge | ✅ Total |
| Opera | ✅ Total |
| IE | ❌ Não suportado |

## ⚠️ Requisitos

1. **HTTPS** (Geolocalização requer conexão segura em produção)
2. **Permissão de Localização** (necessário permitir no navegador)
3. **LocalStorage ativado** (para salvar lembretes)

## 💡 Dicas de Uso

### Coordenadas Úteis
Para encontrar coordenadas de um local:
- Abra [Google Maps](https://maps.google.com)
- Clique com botão direito no local
- Copie as coordenadas que aparecem no topo

### Exemplos de Localidades
- **São Paulo - Av. Paulista**: -23.561414, -46.656139
- **Rio de Janeiro - Cristo Redentor**: -22.952108, -43.210487
- **Brasília - Esplanade**: -15.793889, -47.879444

### Raios Recomendados
- **Precisão Alta**: 50-100m (chegar bem perto)
- **Precisão Normal**: 200-500m (proximidade moderada)
- **Precisão Baixa**: 1000-2000m (zona geral)

## 🐛 Troubleshooting

### "Geolocalização não suportada"
- Use um navegador moderno (Chrome, Firefox, Safari, Edge)
- Certifique-se de que o site usa HTTPS

### "Permissão de localização negada"
- Verifique as permissões do navegador
- Chrome: Menu → Configurações → Privacidade → Configurações do site → Localização
- Firefox: Menu → Preferências → Privacidade → Permissões → Localização

### Alarme não toca
- Verifique se o volume do navegador está ligado
- Certifique-se de que selecionou "Som" ou "Som + Vibração"
- Alguns navegadores em mobile podem silenciar sons da web

### Lembretes desapareceram
- Os lembretes são armazenados no LocalStorage
- Limpar histórico/cache pode deletar os dados
- Tente recriar os lembretes

## 📝 Exemplos de Uso

### Exemplo 1: Lembrete para Compras
- **Título**: Ir ao Supermercado
- **Local**: Coordenadas do mercado mais próximo
- **Raio**: 500m
- **Alarme**: Som + Vibração
- **Repetir**: Sim

### Exemplo 2: Lembrete para Reunião
- **Título**: Reunião na Empresa
- **Local**: Escritório
- **Raio**: 200m (chegar bem próximo)
- **Alarme**: Som
- **Repetir**: Não

### Exemplo 3: Lembrete para Ponto de Referência
- **Título**: Conhecer o Monumento Histórico
- **Local**: Coordenadas do monumento
- **Raio**: 1000m (zona de turismo)
- **Alarme**: Som
- **Repetir**: Sim

## 🔐 Privacidade

- Todos os dados são armazenados localmente no seu navegador
- Nenhuma informação de localização é enviada para servidores
- Você tem controle total sobre seus lembretes
- Pode deletar tudo a qualquer momento limpando o LocalStorage

## 📱 Dica Mobile

Para melhor experiência em smartphones:
1. Ative o modo de alta precisão (se disponível)
2. Mantenha a aplicação aberta ou em segundo plano
3. Configure o alarme com som + vibração
4. Permita notificações do navegador

## 🚀 Melhorias Futuras

- [ ] Integração com mapas (Google Maps, OpenStreetMap)
- [ ] Sincronização na nuvem
- [ ] Categorias de lembretes
- [ ] Múltiplos usuários
- [ ] Compartilhamento de lembretes
- [ ] Relatórios de visitas
- [ ] Rotas otimizadas
- [ ] API REST para sincronização

## 📄 Licença

Este projeto é de código aberto e livre para usar, modificar e distribuir.

## 👨‍💻 Autor

Desenvolvido como uma aplicação web educacional e prática para demostração de geolocalização e APIs web modernas.

---

**Desenvolvido com ❤️ usando HTML5, CSS3 e JavaScript**

Para dúvidas ou sugestões, abra uma issue no repositório! 🙏
