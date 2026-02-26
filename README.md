<div align="center">

# 🧪 Rick & Morty Explorer

<img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" />
<img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart" />
<img src="https://img.shields.io/badge/REST_API-007AFF?style=for-the-badge&logo=json&logoColor=white" alt="REST API" />

<p align="center">
  Aplicativo mobile desenvolvido em Flutter focado no consumo eficiente de APIs REST, renderização de listas complexas e arquitetura em camadas.
</p>

</div>

---

## 📖 Sobre o Projeto

Este projeto foi construído como um estudo de caso arquitetural (desafio técnico) para demonstrar a capacidade de traduzir protótipos de alta fidelidade (Figma) em interfaces responsivas e funcionais. O aplicativo consome a API pública do *Rick and Morty* para renderizar catálogos de personagens com listagem infinita e detalhamento completo de metadados.

### ✨ Funcionalidades Principais
- **[x] Infinite Scrolling:** Listagem de personagens otimizada para baixo consumo de memória.
- **[x] Navegação Dinâmica:** Roteamento de telas passando objetos tipados para detalhamento.
- **[x] Tratamento de Estados:** Feedback visual completo para o usuário (Loading, Error e Success).
- **[x] UI Pixel-Perfect:** Fidelidade máxima ao protótipo de design exigido.

---

## 🏗️ Arquitetura e Engenharia

Para garantir que a base de código seja escalável, testável e de fácil manutenção, o projeto adota uma **Arquitetura em Camadas (Layered Architecture)**, separando estritamente a interface do usuário da lógica de acesso a dados.

```text
lib/
 ├── data/
 │    ├── models/       # Classes fortemente tipadas para parsing seguro do JSON da API.
 │    └── services/     # Isolamento da lógica de rede (HTTP) e tratamento de erros.
 ├── presentation/
 │    ├── screens/      # Views principais (HomeScreen, DetailScreen).
 │    └── widgets/      # Componentes isolados e reutilizáveis (CharacterCard).
 └── utils/
      └── constants     # Gerenciamento de chaves, URLs e temas unificados.
