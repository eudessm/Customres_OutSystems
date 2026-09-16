# Customres_OutSystems
App para customers em OutSystems
from pathlib import Path
import shutil
import zipfile

base = Path("/mnt/data/customer-github-readme")
img_dir = base / "docs" / "images"
img_dir.mkdir(parents=True, exist_ok=True)

# Copia a imagem fornecida para ser usada diretamente pelo README no GitHub.
shutil.copy2("/mnt/data/home.png", img_dir / "home.png")

readme = r"""# Customer — Lista de Contatos

Aplicação web desenvolvida com **OutSystems** para gerenciamento e visualização de uma lista de contatos de clientes.

O projeto foi criado com foco em praticar desenvolvimento low-code, organização de dados, construção de interfaces e integração com arquivos **Excel**, disponibilizando uma experiência simples para importar, consultar e exportar informações de clientes.

---

## 📸 Preview

### Tela principal

A aplicação apresenta uma interface limpa e objetiva, permitindo visualizar os contatos cadastrados em formato de tabela.

![Tela principal do Customer](docs/images/home.png)

---

## 🎯 Sobre o projeto

O **Customer** é um sistema de gerenciamento de contatos desenvolvido na plataforma **OutSystems**.

A proposta é centralizar informações básicas dos clientes em uma tela única, facilitando a consulta dos dados e permitindo trabalhar com informações provenientes de arquivos Excel.

O projeto também demonstra recursos comuns em aplicações corporativas, como:

- Listagem de registros;
- Organização de informações em tabela;
- Ordenação de dados;
- Importação de dados através de Excel;
- Exportação da lista para Excel;
- Autenticação/acesso ao sistema;
- Exibição de dados de contato;
- Interface web responsiva e organizada.

---

## ⚙️ Funcionalidades

### 📋 Lista de clientes

A tela principal apresenta os contatos cadastrados em uma tabela contendo:

| Campo | Descrição |
|---|---|
| **Nome** | Nome completo do cliente |
| **Endereço** | Endereço cadastrado |
| **Telefone** | Número de telefone |
| **Email** | E-mail para contato |

A tabela possui recursos de ordenação, facilitando a localização e organização dos registros.

### 📥 Importação de Excel

A aplicação disponibiliza a opção **Import Excel**, permitindo selecionar um arquivo para carregar informações de clientes para o sistema.

Fluxo:

```text
Selecionar arquivo
       ↓
Importar Excel
       ↓
Processar dados
       ↓
Atualizar lista de clientes