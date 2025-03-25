# Fluxo de Informações - Documentação

Este é um projeto Svelte que documenta o fluxo de informações para criar aplicações do zero utilizando diferentes ferramentas como ChatGPT, CopyCoder e Cursor.

## Visão Geral

O projeto consiste em uma aplicação web que apresenta um guia estruturado sobre o fluxo de trabalho para desenvolvimento de aplicações, utilizando ferramentas modernas de IA e desenvolvimento.

## Tecnologias Utilizadas

- Svelte
- TypeScript
- Vite
- CSS Moderno

## Estrutura do Projeto

```
svelteapp/
├── src/
│   ├── lib/
│   │   ├── Content.svelte    # Componente principal com o conteúdo do fluxo
│   │   └── Counter.svelte    # Componente de exemplo
│   ├── App.svelte           # Componente raiz da aplicação
│   ├── app.css             # Estilos globais
│   └── main.ts            # Ponto de entrada da aplicação
├── public/               # Arquivos estáticos
└── package.json        # Dependências e scripts
```

## Funcionalidades

- Exibição estruturada do fluxo de trabalho
- Links para documentações relevantes
- Interface responsiva e moderna
- Organização clara das etapas do processo

## Como Executar

1. Instale as dependências:
```bash
npm install
```

2. Execute o servidor de desenvolvimento:
```bash
npm run dev
```

3. Acesse a aplicação em `http://localhost:5173`

## Desenvolvimento

O projeto está estruturado em componentes Svelte, com o componente principal `Content.svelte` contendo a estrutura de dados do fluxo de informações. A aplicação utiliza TypeScript para maior segurança e manutenibilidade do código.

### Estrutura de Dados

O conteúdo é organizado em uma estrutura que inclui:
- Título da seção
- Lista de ferramentas
- Ações específicas para cada ferramenta
- Links para documentação relevante

## Contribuição

Para contribuir com o projeto:
1. Faça um fork do repositório
2. Crie uma branch para sua feature
3. Faça commit das suas alterações
4. Envie um pull request

## Licença

MIT
