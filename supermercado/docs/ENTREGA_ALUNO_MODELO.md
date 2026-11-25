# Entrega do Projeto — Mercado Viva

## 1. Identificação

- **Aluno:** Nicolas Rodrigues Gallina
- **Prontuário:** SP3194108
- **Disciplina:** Laboratório de Programação 1
- **Professor:** Celso Gonsalez Saes
- **Projeto:** Mercado Viva — Sistema de gerenciamento de supermercado
- **Data da entrega:** 25/11/2026

## 2. Links do projeto

- **Sistema publicado:** [Acessar Mercado Viva](https://nicolas-gallina-sp-3194108-um79.vercel.app)
- **Repositório GitHub:** [NicolasGallina01/Nicolas-Gallina-SP3194108](https://github.com/NicolasGallina01/Nicolas-Gallina-SP3194108)

O sistema está publicado na Vercel e pode ser acessado pelo endereço de produção informado acima. O código-fonte está disponível no repositório GitHub indicado.

## 3. Descrição geral

O Mercado Viva é um sistema acadêmico de gerenciamento de supermercado, desenvolvido em Python com Flask. A aplicação reúne funcionalidades de administração e operação de caixa, integrando produtos, estoque, compras, vendas e informações financeiras em um banco de dados relacional.

O sistema utiliza arquitetura MVC e aplicação multipágina (MPA), com páginas renderizadas por Flask e Jinja2. A persistência dos dados em produção é realizada em PostgreSQL hospedado no Neon, enquanto a aplicação web está hospedada na Vercel.

## 4. Tecnologias utilizadas

- **Linguagem:** Python 3.12.
- **Backend:** Flask.
- **Interface:** HTML, CSS, JavaScript e templates Jinja2.
- **Acesso a dados:** SQLAlchemy ORM.
- **Banco de dados de produção:** PostgreSQL, hospedado no Neon.
- **Migrações do banco:** Alembic.
- **Hospedagem da aplicação:** Vercel.
- **Controle de versão e repositório:** Git e GitHub.

## 5. Funcionalidades implementadas

### 5.1. Autenticação e controle de acesso

- Login com perfis de administrador e operador.
- Controle de acesso conforme o perfil do usuário.
- Proteções de segurança, incluindo hash de senhas, proteção CSRF e bloqueio temporário após tentativas inválidas de login.

### 5.2. Administração

- Cadastro e gerenciamento de produtos e categorias.
- Cadastro e gerenciamento de fornecedores.
- Gerenciamento de usuários operadores.
- Consulta e controle do estoque, incluindo estoque mínimo e histórico de ajustes.
- Registro de compras e recebimento de mercadorias.
- Consulta de informações financeiras e relatórios.

### 5.3. Operação de caixa e vendas

- Abertura, movimentação e fechamento de caixa por operador.
- Registro de vendas com itens e quantidades.
- Simulação de pagamentos em dinheiro, débito, crédito e Pix.
- Cálculo de valores recebidos e troco.
- Cancelamento administrativo de vendas, com atualização correspondente do estoque e do financeiro.

### 5.4. Relatórios e recursos adicionais

- Gráficos e relatórios por período.
- Exportação de dados para Excel.
- Impressão de comprovantes e geração de ticket em formato adequado para impressão.
- Opções de interface com os temas Aurora e Tropical.

## 6. Banco de dados e persistência

Em produção, o sistema utiliza PostgreSQL hospedado no Neon. A estrutura do banco é gerenciada por migrações Alembic. Os módulos compartilham o mesmo banco relacional para manter a consistência das operações, como vendas, movimentações de estoque e registros financeiros.

## 7. Validações realizadas na versão publicada

As verificações funcionais abaixo foram realizadas no ambiente publicado:

- [x] Acesso ao sistema pelo endereço público de produção.
- [x] Login com a conta de administrador.
- [x] Login com a conta de operador.
- [x] Realização de venda pela conta de operador.
- [x] Verificação de que a venda permanece registrada após sair e entrar novamente.
- [x] Verificação da persistência dos dados após novo deploy.
- [x] Verificação dos módulos de compras, estoque e financeiro.
- [x] Verificação do fechamento de caixa.
- [x] Verificação dos relatórios e da exportação para Excel.

## 8. Contas para avaliação

Foram criadas contas específicas para a avaliação do sistema, com os perfis de administrador e operador. As credenciais de acesso foram encaminhadas ao professor separadamente, por canal privado, para evitar a exposição de senhas no repositório público.

## 9. Observações e limitações

O Mercado Viva é um simulador acadêmico. As operações de pagamento são simuladas e não realizam transações bancárias reais. O sistema não emite documentos fiscais e não possui integração real com adquirentes, TEF ou serviços de Pix.

As funcionalidades de crédito e débito são registradas para fins de simulação, sem processamento por instituições financeiras ou conciliação externa.

---

**Nicolas Rodrigues Gallina**  
**Prontuário: SP3194108**
