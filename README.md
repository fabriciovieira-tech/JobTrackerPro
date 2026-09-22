# 💼 JobTracker Pro — Gestor de candidaturas e métricas de mercado

O **JobTracker Pro** é uma aplicação web intuitiva e centralizada, desenvolvida para simplificar a organização da sua busca por emprego. Com ele, você registra suas candidaturas, acompanha o andamento de cada processo seletivo em tempo real e recebe alertas automáticos sobre vagas que precisam de acompanhamento.

A nova versão traz armazenamento seguro na nuvem e um painel de métricas interativo, transformando seu histórico de candidaturas em **dados estratégicos** para compreender padrões do mercado de trabalho.

---

## ✨ Funcionalidades principais

- 📝 **Cadastro rápido de candidaturas:** Informe o cargo, a empresa, a data da candidatura e o status inicial em poucos cliques.
- 📊 **Tabela de acompanhamento ativo:** Visualize todas as suas vagas registradas com ordenação automática pela última atualização.
- 🔄 **Gestão completa de status:** Altere o status da vaga (*Aguardando chamada, Em entrevista, Aprovado, Rejeitado*) diretamente na tabela.
- 🗑️ **Exclusão isolada de registros:** Remova candidaturas indesejadas com segurança por meio de um modal de confirmação, garantindo que o restante do seu histórico não seja afetado.
- ⏰ **Alertas de estagnação (follow-up):** Notificação automática na parte superior da tela e identificadores visuais para vagas que estão há mais de **7 dias sem atualização**.
- 📈 **Dashboard de métricas interativo:** Acompanhe dados como frequência de cargos, recorrência por empresas e status geral. Agora com **suporte a alternância de visualização** entre gráficos de barras e gráficos de pizza, adaptando-se à sua preferência.
- ☁️ **Persistência em nuvem (Firebase):** Seus dados são salvos em tempo real e com segurança na nuvem. Você pode fechar a página ou atualizar o navegador sem medo de perder nenhuma informação.

---

## 🚀 Como executar o projeto

Como o **JobTracker Pro** foi desenvolvido como uma aplicação web de página única (SPA), executá-lo é extremamente simples. 

### Pré-requisitos
Um navegador web moderno com acesso à internet (para carregar os estilos, ícones, gráficos e conectar ao banco de dados).

### Passo a passo

1. **Baixe ou clone o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/jobtracker-pro.git
   ```
2. **Navegue até a pasta do projeto:**
   ```bash
   cd jobtracker-pro
   ```
3. **Abra o arquivo no navegador:**
   - Dê um duplo clique no arquivo `index.html`; **ou**
   - Arraste o arquivo `index.html` e solte dentro do seu navegador aberto.

*(Nota para desenvolvedores: Para que o salvamento em nuvem funcione no seu próprio repositório, insira as credenciais do seu projeto Firebase nas variáveis globais no início do script).*

---

## 📖 Como usar

1. **Registrar uma vaga:**
   - Preencha o formulário na lateral esquerda com o **Cargo**, a **Empresa**, a **Data da candidatura** e o **Status inicial**.
   - Clique em **Registrar vaga**. A candidatura aparecerá imediatamente na tabela ao lado e será salva na nuvem.

2. **Atualizar ou excluir o andamento:**
   - Na tabela de candidaturas, navegue até a coluna **Ações**.
   - Para mudar o andamento, selecione o novo status no menu suspenso.
   - Para deletar uma vaga, clique no botão de **Lixeira vermelha** e confirme a exclusão no aviso que aparecerá na tela.

3. **Acompanhar alertas:**
   - Caso uma vaga fique sem alteração por 7 dias ou mais, uma barra amarela surgirá no topo da página sugerindo um *follow-up*, e um ícone de relógio será exibido ao lado do cargo.

4. **Analisar as métricas:**
   - Role a página até a seção inferior **Dashboard de métricas** para conferir seus dados.
   - Use os botões **Barras** ou **Pizza** no canto superior direito do painel para alterar o formato dos gráficos dinamicamente.

---

## 📂 Estrutura do projeto

```text
├── index.html        # Aplicação completa (HTML, Tailwind CSS, Chart.js e Lógica Firebase)
└── README.md         # Documentação e guia de uso do projeto
```

---

## 🤝 Contribuições

Contribuições são sempre bem-vindas! Se você tem sugestões de melhorias, novas funcionalidades ou correções de bugs:

1. Faça um **Fork** do projeto.
2. Crie uma **Branch** para sua funcionalidade (`git checkout -b feature/nova-funcionalidade`).
3. Faça o **Commit** de suas alterações (`git commit -m 'Adiciona nova funcionalidade'`).
4. Envie para a Branch (`git push origin feature/nova-funcionalidade`).
5. Abra um **Pull Request**.

---

## 📄 Licença

Este projeto está sob a licença [MIT](https://opensource.org/licenses/MIT) — sinta-se livre para usá-lo, modificá-lo e compartilhá-lo.