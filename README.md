# SkillMatch

Este projeto foi desenvolvido como um Desafio de Projeto da DIO de Vibe Coding utilizando o Lovable. A proposta é criar um gerador de curriculos otimizado para ATS.

# Prompt Utilizado

```markdown
# PROMPT ÚNICO — MATCHCV | PLATAFORMA SAAS DE MATCHMAKING DE VAGAS E CURRÍCULOS ATS

Crie do zero uma aplicação web SaaS completa, moderna, profissional e responsiva, focada em empregabilidade, inteligência artificial, matchmaking de vagas de emprego e criação de currículos personalizados e otimizados para sistemas ATS (Applicant Tracking Systems).

O objetivo é desenvolver uma plataforma que ajude usuários a encontrar oportunidades de emprego compatíveis com seu perfil profissional e, principalmente, criar versões personalizadas do próprio currículo para cada vaga, aumentando suas chances de passar pelos filtros automatizados de recrutamento.

A aplicação deve ser desenvolvida integralmente dentro do ecossistema Lovable, utilizando os recursos nativos disponíveis, sem depender de plataformas externas para construir, hospedar ou operar o produto.

O produto deve ter aparência de uma startup SaaS profissional, com qualidade visual comparável a plataformas como Linear, Teal, Huntr e Notion.

**IMPORTANTE: Nesta primeira versão, NÃO implementar login, cadastro, autenticação, recuperação de senha ou qualquer tipo de barreira de acesso. O usuário deve entrar diretamente na aplicação e começar a utilizar todas as funcionalidades disponíveis. Não criar tela de login ou cadastro. A aplicação deve abrir diretamente no dashboard ou na experiência inicial de utilização.**

---

# 1. IDENTIDADE VISUAL E DESIGN SYSTEM

Utilize obrigatoriamente **Shadcn UI como design system**, com componentes baseados em Radix UI e estilização com Tailwind CSS.

A interface deve ser minimalista, elegante, moderna, intuitiva e transmitir confiança, tecnologia e profissionalismo.

### Paleta de cores

A identidade visual deve utilizar predominantemente três cores:

- Azul-claro: cor principal da identidade visual, utilizada em botões primários, elementos de destaque, links e indicadores.
- Branco: cor predominante dos fundos, cards, superfícies e áreas de conteúdo.
- Amarelo-claro: cor secundária para destaques, notificações positivas, indicadores e elementos que mereçam atenção.

Sugestão de paleta:

- Primary Blue: #69B9E8
- Light Blue: #EAF6FD
- Soft Blue: #D5EDFA
- White: #FFFFFF
- Light Yellow: #FFF4C7
- Soft Yellow: #FFFAE8
- Text Primary: #243447
- Text Secondary: #718096
- Border: #E5EDF3
- Background: #F7FAFC

Utilize tons escuros apenas para textos e contraste.

### Diretrizes visuais

- Design limpo e com bastante espaço em branco.
- Cards com bordas suaves e cantos arredondados.
- Sombras discretas.
- Tipografia moderna e altamente legível.
- Ícones Lucide.
- Microinterações e transições suaves.
- Sidebar elegante e organizada.
- Botões com estados hover, active, disabled e loading.
- Skeleton loaders durante carregamentos.
- Toasts para feedback de ações.
- Layout totalmente responsivo para desktop, tablet e dispositivos móveis.
- Evitar excesso de gradientes, cores fortes, elementos decorativos e informações desnecessárias.

Não utilize uma aparência genérica de template de dashboard. Desenvolva uma identidade visual consistente e reconhecível.

---

# 2. CONCEITO E FUNCIONAMENTO DO PRODUTO

A plataforma terá quatro pilares principais:

1. Perfil profissional do usuário.
2. Matchmaking inteligente de vagas.
3. Análise de compatibilidade entre usuário e oportunidade.
4. Geração de currículos personalizados e ATS Friendly para cada vaga.

O princípio fundamental é que o usuário tenha um currículo-base armazenado na plataforma e possa gerar diferentes versões adaptadas às exigências de cada oportunidade.

Exemplo:

Um usuário possui experiência com Java, Python, SQL e Spring Boot.

Ele encontra três oportunidades:

- Desenvolvedor Backend Java.
- Desenvolvedor Python Júnior.
- Analista de Dados Júnior.

A plataforma deverá analisar cada descrição de vaga e gerar uma versão específica do currículo, destacando as experiências, competências e conhecimentos verdadeiros do usuário que sejam mais relevantes para aquela oportunidade.

IMPORTANTE: Nunca inventar experiências profissionais, qualificações, certificações, habilidades ou resultados. A IA deve trabalhar exclusivamente com informações fornecidas ou confirmadas pelo usuário.

---

# 3. EXPERIÊNCIA INICIAL E PERFIL PROFISSIONAL

Como não haverá autenticação nesta primeira versão, criar uma experiência inicial simples e direta.

Ao acessar o site, o usuário deverá conseguir começar imediatamente, sem preencher cadastro ou criar uma conta.

Apresentar uma tela inicial de configuração do perfil profissional, com opção de preencher manualmente ou importar um currículo existente.

Permitir pular etapas e completar o perfil posteriormente.

### Informações pessoais

- Nome completo.
- E-mail.
- Telefone.
- Cidade e estado.
- País.
- LinkedIn.
- GitHub.
- Portfólio ou site pessoal.

### Objetivo profissional

- Cargo desejado.
- Área de atuação.
- Nível profissional: Estágio, Júnior, Pleno, Sênior ou Especialista.
- Tipo de contrato: CLT, PJ, Estágio ou Freelancer.
- Modelo de trabalho: Presencial, Híbrido ou Remoto.
- Pretensão salarial (opcional).
- Localidades de interesse.

### Experiência profissional

Permitir adicionar múltiplas experiências:

- Empresa.
- Cargo.
- Data de início.
- Data de término.
- Emprego atual.
- Descrição das atividades.
- Principais responsabilidades.
- Resultados alcançados.

### Formação acadêmica

- Instituição.
- Curso.
- Grau acadêmico.
- Data de início.
- Data de conclusão ou previsão.
- Situação atual.

### Competências

Permitir cadastrar habilidades técnicas e comportamentais.

Exemplos:

- Java.
- Python.
- JavaScript.
- SQL.
- PostgreSQL.
- Spring Boot.
- Git.
- Docker.
- Comunicação.
- Trabalho em equipe.

### Importação de currículo

Permitir:

- Fazer upload de currículo em PDF ou DOCX.
- Extrair automaticamente informações do documento.
- Interpretar as informações utilizando IA.
- Preencher automaticamente os campos do perfil.
- Permitir revisão e edição manual antes de salvar.

O perfil deverá ser armazenado localmente nesta primeira versão, utilizando uma solução de persistência adequada no navegador, para que os dados continuem disponíveis ao retornar à aplicação no mesmo dispositivo e navegador.

Criar uma estrutura preparada para futuramente migrar os dados para um banco de dados com autenticação.

---

# 4. DASHBOARD PRINCIPAL

Criar um dashboard moderno e personalizado.

### Cabeçalho

- Saudação personalizada.
- Nome do usuário, quando informado.
- Avatar opcional.
- Notificações.
- Acesso às configurações.

### Indicadores principais

Exibir cards com:

- Total de vagas compatíveis.
- Vagas salvas.
- Currículos gerados.
- Média de compatibilidade das vagas encontradas.

### Seção: Melhores oportunidades para você

Apresentar vagas recomendadas de acordo com o perfil profissional do usuário.

Cada card deve apresentar:

- Nome da empresa.
- Cargo.
- Localidade.
- Modalidade de trabalho.
- Faixa salarial, quando disponível.
- Nível de experiência.
- Percentual de compatibilidade.
- Botão para visualizar a vaga.
- Botão para salvar a vaga.
- Botão para gerar currículo personalizado.

### Seção: Atividade recente

Mostrar:

- Últimas vagas visualizadas.
- Últimos currículos gerados.
- Últimas vagas salvas.
- Últimas análises realizadas.

### Seção: Complemente seu perfil

Exibir recomendações para melhorar a qualidade do matchmaking.

Exemplos:

- Adicionar habilidades técnicas.
- Completar experiências profissionais.
- Adicionar LinkedIn.
- Atualizar o currículo-base.

---

# 5. MATCHMAKING INTELIGENTE DE VAGAS

Esta é uma das funcionalidades centrais da plataforma.

Criar um mecanismo de correspondência entre o perfil profissional do usuário e as vagas disponíveis.

O sistema deverá analisar:

- Cargo desejado.
- Área profissional.
- Nível de experiência.
- Habilidades técnicas.
- Habilidades comportamentais.
- Experiência profissional.
- Formação acadêmica.
- Localidade.
- Modelo de trabalho.
- Tipo de contratação.
- Requisitos obrigatórios.
- Requisitos desejáveis.

### Cálculo de compatibilidade

Cada vaga deverá receber um percentual de compatibilidade de 0% a 100%.

O cálculo deverá considerar uma ponderação configurável, inicialmente:

- Habilidades técnicas: 35%.
- Experiência profissional: 25%.
- Cargo e área de atuação: 15%.
- Nível de senioridade: 10%.
- Formação acadêmica: 5%.
- Modelo de trabalho e localização: 10%.

A compatibilidade não deve ser baseada apenas na presença de palavras-chave.

Utilize análise semântica e IA para compreender o significado dos requisitos e comparar com as informações do candidato.

### Classificação dos resultados

- 90% a 100%: Excelente compatibilidade.
- 75% a 89%: Alta compatibilidade.
- 60% a 74%: Compatibilidade moderada.
- Abaixo de 60%: Baixa compatibilidade.

### Explicação do Match

Ao abrir uma vaga, mostrar detalhadamente:

**Pontos fortes:**

- Competências que correspondem aos requisitos.
- Experiências relevantes.
- Formação compatível.

**Pontos de atenção:**

- Competências ausentes.
- Experiências que poderiam ser mais bem demonstradas.
- Requisitos que o usuário ainda não atende.

**Recomendação da IA:**

Explicar se vale a pena se candidatar e quais aspectos do currículo devem receber maior destaque.

Nunca afirmar que o candidato será aprovado ou contratado.

---

# 6. BUSCA E AQUISIÇÃO DE VAGAS

Criar uma página dedicada à descoberta de oportunidades.

A aplicação deverá permitir que o usuário encontre vagas por meio de:

- Cargo.
- Empresa.
- Área profissional.
- Localidade.
- Modelo de trabalho.
- Nível de experiência.
- Tipo de contrato.
- Palavras-chave.

Criar filtros avançados e ordenação por:

- Maior compatibilidade.
- Mais recentes.
- Maior salário.
- Menor distância, quando aplicável.

### Integração de vagas

Preparar a arquitetura para receber vagas de diferentes fontes.

Priorizar:

- APIs oficiais de plataformas de recrutamento.
- Integrações autorizadas com sistemas de ATS.
- Fontes públicas de vagas.
- Cadastro manual de oportunidades.
- Importação de vagas por URL.
- Importação de descrições de vagas por texto.

Não realizar scraping de plataformas sem autorização ou violar seus termos de uso.

Cada vaga deve armazenar:

- Identificador.
- Cargo.
- Empresa.
- Descrição completa.
- Requisitos obrigatórios.
- Requisitos desejáveis.
- Localidade.
- Modalidade.
- Faixa salarial.
- Data de publicação.
- Fonte.
- URL original de candidatura.

Criar mecanismo para identificar vagas duplicadas.

IMPORTANTE: Não apresentar vagas fictícias como oportunidades reais. Se não houver integração ativa com uma fonte de vagas, deixar isso claro e utilizar vagas demonstrativas identificadas como exemplos.

---

# 7. CURRÍCULO-BASE

Criar uma área chamada "Meu Currículo".

O usuário terá um currículo-base que servirá como fonte de informações para todas as versões personalizadas.

Permitir:

- Visualizar currículo.
- Editar informações.
- Adicionar experiências.
- Adicionar formação acadêmica.
- Adicionar competências.
- Adicionar certificações.
- Adicionar projetos.
- Adicionar idiomas.
- Adicionar links profissionais.
- Importar currículo existente.
- Exportar currículo-base em PDF.

O currículo-base deve funcionar como um banco de informações profissionais, permitindo reutilizar os dados sem precisar preencher tudo novamente.

Criar histórico de alterações e salvar automaticamente as modificações.

---

# 8. GERADOR DE CURRÍCULOS PERSONALIZADOS E ATS FRIENDLY

Esta é a principal funcionalidade comercial da plataforma.

Ao selecionar uma vaga, o usuário poderá clicar em:

**"Criar currículo para esta vaga".**

O sistema deverá iniciar um processo de análise e personalização utilizando inteligência artificial.

### Etapa 1 — Análise da vaga

A IA deverá extrair:

- Cargo.
- Responsabilidades.
- Requisitos obrigatórios.
- Requisitos desejáveis.
- Habilidades técnicas.
- Habilidades comportamentais.
- Palavras-chave relevantes.
- Formação exigida.
- Experiência exigida.

### Etapa 2 — Comparação com o currículo-base

Comparar os requisitos com as informações do candidato.

Identificar:

- Competências correspondentes.
- Experiências relevantes.
- Projetos relacionados.
- Palavras-chave que já estão presentes.
- Informações verdadeiras que podem receber maior destaque.

### Etapa 3 — Geração do currículo

Gerar uma nova versão personalizada, mantendo a veracidade das informações.

A IA deverá:

- Adaptar o título profissional.
- Criar um resumo profissional direcionado à vaga.
- Reorganizar competências.
- Destacar experiências relevantes.
- Melhorar a descrição de atividades.
- Utilizar palavras-chave da descrição da vaga de forma natural.
- Melhorar a clareza e objetividade.
- Corrigir erros gramaticais.
- Utilizar verbos de ação.
- Priorizar informações relevantes para a oportunidade.

Não adicionar palavras-chave artificialmente ou inserir competências que o usuário não possui.

Se uma informação importante estiver ausente, solicitar confirmação ao usuário.

### Etapa 4 — Otimização ATS

O currículo deverá seguir boas práticas de compatibilidade com sistemas ATS:

- Layout simples e profissional.
- Estrutura de uma coluna.
- Seções convencionais.
- Títulos de seção reconhecíveis.
- Texto selecionável.
- Evitar tabelas complexas.
- Evitar gráficos e elementos decorativos.
- Evitar barras de proficiência.
- Evitar informações importantes em cabeçalhos e rodapés.
- Utilizar fontes convencionais.
- Manter hierarquia visual clara.
- Utilizar palavras-chave relevantes naturalmente.
- Datas e cargos em formatos consistentes.

Criar uma estrutura padronizada:

1. Informações de contato.
2. Resumo profissional.
3. Competências técnicas.
4. Experiência profissional.
5. Projetos relevantes.
6. Formação acadêmica.
7. Certificações.
8. Idiomas.

Permitir ocultar seções que não sejam relevantes.

### Etapa 5 — Visualização e edição

Criar um editor de currículo com:

- Pré-visualização em tempo real.
- Edição de textos.
- Reordenação de seções.
- Adição e remoção de informações.
- Escolha entre modelos ATS.
- Botão para regenerar uma seção utilizando IA.
- Botão para restaurar a versão anterior.

### Etapa 6 — Exportação

Permitir exportar em:

- PDF.
- DOCX.

Os documentos exportados devem manter a formatação e ser adequados para leitura automatizada.

Cada currículo gerado deverá ser salvo como uma versão independente, vinculada à vaga correspondente.

Nome sugerido:

"Currículo - Desenvolvedor Backend Java - Empresa".

---

# 9. ANALISADOR ATS

Criar uma funcionalidade chamada "Analisador ATS".

O usuário poderá:

- Enviar um currículo.
- Selecionar uma vaga cadastrada.
- Colar uma descrição de vaga.
- Solicitar uma análise de compatibilidade.

O sistema deverá apresentar:

### Pontuação ATS estimada

Uma pontuação de 0 a 100 baseada em critérios transparentes.

Analisar:

- Correspondência de palavras-chave.
- Compatibilidade das competências.
- Organização do documento.
- Clareza das experiências.
- Estrutura das seções.
- Formatação.
- Correspondência com os requisitos.

### Relatório de análise

Mostrar:

- Pontos positivos.
- Palavras-chave encontradas.
- Palavras-chave ausentes.
- Competências correspondentes.
- Requisitos não demonstrados.
- Problemas de estrutura.
- Sugestões de melhoria.

IMPORTANTE: A pontuação deve ser apresentada como uma estimativa interna de qualidade e não como uma nota oficial de qualquer sistema ATS.

---

# 10. GERENCIAMENTO DE VAGAS

Criar uma seção chamada "Minhas Vagas".

Permitir organizar oportunidades em um quadro de acompanhamento.

Status:

- Interessado.
- Salvo.
- Preparando candidatura.
- Candidatado.
- Entrevista.
- Aprovado.
- Rejeitado.
- Arquivado.

Cada oportunidade deverá possuir:

- Informações da vaga.
- Empresa.
- Compatibilidade.
- Data em que foi salva.
- Data da candidatura.
- Currículo utilizado.
- Anotações pessoais.
- Histórico de alterações de status.
- Link para candidatura.

Criar visualização em cards e em lista.

---

# 11. BIBLIOTECA DE CURRÍCULOS

Criar uma página chamada "Meus Currículos".

Mostrar todos os currículos gerados pelo usuário.

Cada item deverá exibir:

- Nome da versão.
- Empresa.
- Cargo.
- Data de criação.
- Compatibilidade com a vaga.
- Formato disponível.

Ações:

- Visualizar.
- Editar.
- Duplicar.
- Renomear.
- Baixar PDF.
- Baixar DOCX.
- Excluir.

Manter o currículo-base separado dos currículos personalizados.

---

# 12. INTELIGÊNCIA ARTIFICIAL

Utilizar recursos de inteligência artificial disponíveis no ecossistema Lovable e integrações compatíveis, preferencialmente por meio de Lovable Cloud e funções de backend seguras.

A IA será responsável por:

- Interpretar currículos.
- Extrair informações de documentos.
- Interpretar descrições de vagas.
- Comparar perfis profissionais.
- Calcular compatibilidade.
- Identificar palavras-chave.
- Recomendar oportunidades.
- Reescrever experiências profissionais.
- Criar resumos profissionais.
- Gerar currículos personalizados.
- Analisar compatibilidade ATS.

### Regras da IA

1. Nunca inventar informações sobre o usuário.
2. Nunca adicionar experiências não fornecidas.
3. Nunca inventar resultados quantitativos.
4. Nunca afirmar que uma habilidade existe sem evidências no perfil.
5. Priorizar informações relevantes para cada vaga.
6. Explicar as recomendações.
7. Preservar a identidade profissional do candidato.
8. Solicitar confirmação quando necessário.
9. Não garantir aprovação em processos seletivos.
10. Não utilizar informações sensíveis ou características pessoais para discriminar candidatos.

Criar prompts internos específicos para cada tarefa, evitando utilizar um único prompt genérico para todas as funcionalidades.

Todas as chamadas de IA devem ocorrer de maneira segura, sem expor chaves de API no frontend.

---

# 13. ESTRUTURA DE NAVEGAÇÃO

Criar uma sidebar com as seguintes opções:

1. Dashboard.
2. Encontrar vagas.
3. Meu currículo.
4. Gerar currículo.
5. Analisador ATS.
6. Minhas vagas.
7. Meus currículos.
8. Meu perfil.
9. Configurações.

A sidebar deve possuir ícones Lucide e indicar visualmente a página ativa.

No mobile, utilizar navegação adaptada com menu recolhível.

---

# 14. BANCO DE DADOS E PERSISTÊNCIA

Nesta primeira versão, não implementar autenticação.

Utilizar uma arquitetura que permita ao usuário começar imediatamente, sem conta.

Priorizar persistência local no navegador, com uma camada de serviços organizada para facilitar futura migração para Lovable Cloud e banco de dados.

Utilizar localStorage ou IndexedDB conforme a necessidade de armazenamento.

Arquivos de currículos devem ser tratados com atenção ao armazenamento, evitando limites inadequados do localStorage.

Estruturar os dados de maneira equivalente a:

### users_profiles

- id
- full_name
- email
- phone
- city
- state
- country
- linkedin_url
- github_url
- portfolio_url
- professional_title
- desired_position
- experience_level
- preferred_work_model
- employment_type
- salary_expectation
- created_at
- updated_at

### experiences

- id
- company
- position
- description
- start_date
- end_date
- is_current

### education

- id
- institution
- course
- degree
- start_date
- end_date
- status

### skills

- id
- name
- category
- proficiency

### certifications

- id
- name
- institution
- issue_date
- expiration_date
- credential_url

### projects

- id
- name
- description
- technologies
- project_url

### jobs

- id
- title
- company
- description
- requirements
- desirable_skills
- location
- work_model
- salary_min
- salary_max
- employment_type
- experience_level
- source
- application_url
- published_at
- created_at

### job_matches

- id
- job_id
- compatibility_score
- matching_skills
- missing_skills
- recommendations
- created_at

### saved_jobs

- id
- job_id
- status
- notes
- application_date
- created_at
- updated_at

### resumes

- id
- name
- resume_type
- original_job_id
- content
- created_at
- updated_at

### resume_versions

- id
- resume_id
- job_id
- version_name
- content
- ats_score
- file_url
- created_at

### ats_analyses

- id
- resume_id
- job_id
- score
- strengths
- missing_keywords
- recommendations
- created_at

Criar relacionamentos, validações e índices adequados.

### Privacidade e segurança

- Não solicitar cadastro ou autenticação.
- Não expor dados pessoais em URLs.
- Não compartilhar informações profissionais entre sessões ou usuários.
- Tratar arquivos enviados de forma segura.
- Não armazenar chaves de API no frontend.
- Utilizar funções server-side para operações sensíveis.
- Informar claramente que os dados desta versão ficam armazenados localmente no navegador.
- Permitir exportar os dados do usuário.
- Permitir apagar todos os dados armazenados localmente.

Preparar a arquitetura para futura implementação de contas individuais, autenticação e sincronização em nuvem, sem implementar esses recursos agora.

---

# 15. EXPERIÊNCIA DO USUÁRIO

A experiência deve ser simples, mesmo para pessoas que não possuem conhecimentos técnicos.

O usuário deve conseguir:

1. Entrar na plataforma diretamente.
2. Preencher seu perfil profissional.
3. Importar seu currículo.
4. Visualizar oportunidades compatíveis.
5. Entender por que uma vaga combina com seu perfil.
6. Selecionar uma oportunidade.
7. Gerar um currículo personalizado.
8. Revisar o documento.
9. Baixar o currículo.
10. Acompanhar sua candidatura.

Reduzir ao máximo a quantidade de etapas desnecessárias.

Utilizar mensagens claras, linguagem acessível e feedback visual em todas as ações.

A plataforma deverá ser inteiramente em português brasileiro (pt-BR), incluindo datas, textos, moedas e mensagens.

Preparar a arquitetura para uma futura internacionalização.

---

# 16. PLANOS E MONETIZAÇÃO

Preparar a arquitetura para um modelo SaaS freemium.

### Plano gratuito

- Acesso direto à plataforma.
- Perfil profissional.
- Currículo-base.
- Visualização de vagas.
- Quantidade limitada de análises.
- Quantidade limitada de currículos personalizados.

### Plano Pro

- Matchmaking avançado.
- Mais análises de compatibilidade.
- Geração ampliada de currículos.
- Analisador ATS completo.
- Histórico de versões.
- Exportação PDF e DOCX.
- Recomendações avançadas de IA.

Não implementar cobrança real inicialmente. Apenas preparar a arquitetura para futura integração com pagamentos e controle de assinaturas.

---

# 17. PÁGINAS DA APLICAÇÃO

Criar as seguintes páginas:

- `/` — Dashboard ou página inicial de utilização.
- `/onboarding` — Configuração inicial opcional do perfil, sem cadastro.
- `/dashboard` — Painel principal.
- `/jobs` — Busca de vagas.
- `/jobs/:id` — Detalhes da oportunidade.
- `/matches` — Vagas compatíveis.
- `/resume` — Currículo-base.
- `/resume/create/:jobId` — Gerador personalizado.
- `/resume/:id` — Visualização e edição do currículo.
- `/ats-analyzer` — Analisador ATS.
- `/applications` — Acompanhamento de candidaturas.
- `/my-resumes` — Biblioteca de currículos.
- `/profile` — Perfil profissional.
- `/settings` — Configurações.

Não criar rotas `/login` ou `/register`.

Todas as páginas devem ser acessíveis diretamente, sem autenticação.

---

# 18. LANDING PAGE

Criar uma página inicial pública com aparência de startup SaaS premium, mas sem obrigar o usuário a passar por uma página de apresentação antes de usar a ferramenta.

A página inicial deverá combinar uma apresentação compacta do produto com acesso imediato às funcionalidades.

### Hero section

Headline:

**"Encontre a vaga certa. Apresente o currículo ideal."**

Subheadline:

"Descubra oportunidades compatíveis com seu perfil e crie currículos personalizados, otimizados para ATS e direcionados para cada oportunidade."

CTA principal:

"Começar agora"

CTA secundário:

"Conhecer a plataforma"

Criar uma ilustração visual do funcionamento do produto, mostrando:

- Perfil profissional.
- Vaga encontrada.
- Compatibilidade de 92%.
- Currículo personalizado.
- Indicador de otimização ATS.

### Seção de benefícios

- Descubra vagas que combinam com você.
- Entenda sua compatibilidade com cada oportunidade.
- Personalize seu currículo com inteligência artificial.
- Melhore a estrutura do currículo para sistemas ATS.
- Organize suas candidaturas em um só lugar.

### Seção: Como funciona

1. Preencha seu perfil profissional.
2. Descubra vagas compatíveis.
3. Gere um currículo direcionado para cada oportunidade.
4. Candidate-se com mais confiança.

### CTA final

"Seu próximo emprego pode começar com o currículo certo."

Botão: "Começar gratuitamente".

O botão deve levar diretamente à experiência de utilização, sem exigir login ou cadastro.

---

# 19. REQUISITOS TÉCNICOS E DE QUALIDADE

- Utilizar React, TypeScript e Tailwind CSS.
- Utilizar Shadcn UI obrigatoriamente.
- Utilizar Lucide Icons.
- Utilizar Lovable Cloud para recursos de backend e IA quando necessário e disponível.
- Criar componentes reutilizáveis.
- Separar lógica de negócio, componentes e serviços.
- Utilizar tipagem forte.
- Criar tratamento de erros.
- Implementar estados de carregamento.
- Implementar validação de formulários.
- Criar páginas responsivas.
- Garantir acessibilidade.
- Otimizar carregamento e desempenho.
- Evitar componentes gigantes e código duplicado.
- Não utilizar dados fictícios como dados reais.
- Criar estados vazios bem elaborados.
- Garantir consistência visual entre todas as páginas.
- Não implementar autenticação nesta versão.
- Não exigir cadastro.
- Não bloquear funcionalidades com telas de login.

---

# 20. ORIENTAÇÕES DE IMPLEMENTAÇÃO

Desenvolva a aplicação como um produto real, não apenas como um protótipo visual.

Priorize a implementação funcional de cada recurso.

Não crie botões decorativos ou funcionalidades que não executam ações reais.

Não simule análises de IA como se fossem resultados verdadeiros.

Quando uma integração ainda não estiver configurada, apresentar um estado informativo e orientar o usuário.

Implementar persistência real dos dados no navegador.

Todas as operações de criação, edição, exclusão e consulta devem funcionar.

### Ordem de desenvolvimento

1. Criar a estrutura visual e o design system.
2. Implementar navegação sem autenticação.
3. Implementar persistência local.
4. Desenvolver onboarding e perfil profissional.
5. Desenvolver currículo-base.
6. Desenvolver cadastro e importação de vagas.
7. Desenvolver mecanismo de matchmaking.
8. Desenvolver integração com IA.
9. Desenvolver gerador de currículos ATS.
10. Desenvolver analisador ATS.
11. Desenvolver gerenciamento de candidaturas.
12. Desenvolver exportação PDF e DOCX.
13. Desenvolver landing page.
14. Realizar testes de funcionamento, responsividade e segurança.

### INSTRUÇÃO FINAL

Construa uma plataforma SaaS completa, com arquitetura organizada, design consistente e funcionalidades reais.

O Shadcn UI deve ser utilizado como base de todos os componentes de interface.

Mantenha rigorosamente a identidade visual em azul-claro, branco e amarelo-claro.

O resultado deve transmitir a sensação de um produto tecnológico profissional, confiável e pronto para evoluir comercialmente.

**Nome provisório do produto: MatchCV.**

O usuário deve conseguir acessar e utilizar a plataforma imediatamente, sem login, senha, cadastro ou autenticação.

Desenvolva a aplicação pensando em escalabilidade, experiência do usuário, privacidade dos dados e qualidade dos currículos gerados.

Não se limite a criar uma dashboard bonita: construa um produto funcional de ponta a ponta, priorizando a qualidade do matchmaking e a geração de currículos personalizados e verdadeiramente compatíveis com boas práticas ATS.
```

# Resultado Final

Acesse o projeto [aqui](https://screenshot-to-spark-9690.lovable.app)

<img width="1534" height="694" alt="image" src="https://github.com/user-attachments/assets/51530e34-17b8-4e0a-ba14-0f84d6ffb872" />
