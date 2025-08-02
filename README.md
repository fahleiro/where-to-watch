🖥️ Where-To-Watch

Plataforma colaborativa onde os usuários informam em qual serviço de streaming assistiram determinado conteúdo.

⸻

✅ Resumo Funcional
	•	Feed colaborativo estilo Reddit.
	•	Usuários não precisam se cadastrar para usar.
	•	Publicações possuem:
	•	Nome do conteúdo
	•	Plataforma onde foi assistido
	•	Data automática no formato dd/mm/aaaa
	•	Contador de likes e dislikes
	•	Regras de pontuação: score = likes - dislikes
	•	Se score <= -10, a publicação é automaticamente excluída.
	•	Feed exibe as publicações mais recentes primeiro.
	•	Campo de busca por nome do conteúdo filtra o feed.

⸻

🧱 Componentes da Interface

1. 🔍 Barra de Pesquisa (Topo)
	•	Campo de texto para digitar o nome do conteúdo.
	•	Ao digitar, exibe no feed apenas publicações relacionadas.
	•	Limpar o campo retorna ao feed completo.

⸻

2. ➕ Nova Publicação
	•	Campos:
	•	Nome do conteúdo (input texto)
	•	Plataforma (input texto ou dropdown)
	•	Botão “Publicar”
	•	Ao clicar:
	•	Valida os campos.
	•	Gera a data atual (dd/mm/aaaa).
	•	Adiciona publicação no topo do feed.

⸻

3. 📄 Card de Publicação

Cada publicação contém:
	•	📝 Conteúdo
	•	📺 Plataforma
	•	📅 Data
	•	👍 Like e 👎 Dislike com contador.
	•	Sistema de pontuação dinâmica:
	•	Se usuário clicar em dislike e houver pelo menos 1 like → decrementa.
	•	Quando score chega a -10, publicação é excluída automaticamente do feed.

⸻

⚙️ Regras de Negócio
	•	Sem autenticação: qualquer pessoa pode publicar, curtir ou descurtir.
	•	Validação simples: campos de texto obrigatórios na publicação.
	•	Like/Dislike: deve impedir spam (pode-se limitar 1 voto por IP/localStorage opcionalmente).
	•	Data da publicação: sempre gerada pelo sistema (não editável pelo usuário).
	•	Ordenação: publicações ordenadas por mais recentes no topo.