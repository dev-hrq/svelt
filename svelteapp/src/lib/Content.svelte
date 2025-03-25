<script lang="ts">
  const content = [
    {
      title: 'Fluxo detalhado para criar uma aplicação do zero com ChatGPT, CopyCoder, Cursor e outras ferramentas',
      steps: [
        {
          tool: 'ChatGPT',
          actions: [
            'Utilizar o ChatGPT para gerar a documentação inicial do projeto:',
            '- Exemplo de prompt: "Quero construir um aplicativo de controle de estoque em Next.js. Por favor, crie um documento detalhado de especificações de requisitos."',
            '- Continuar com: "Agora crie a estrutura das páginas com base nesses requisitos."',
            'Com isso, você terá uma base sólida com requisitos funcionais, estrutura de navegação e possíveis endpoints da aplicação.'
          ]
        },
        {
          tool: 'CopyCoder',
          url: 'https://copycoder.ai/',
          actions: [
            'Acesse o site e cole uma imagem conceitual da interface ou do sistema desejado (ex: wireframe feito à mão ou screenshot).',
            'Clique em "Gerar Page Structure" para receber um esqueleto de layout ou código baseado na imagem.',
            'Isso agiliza a prototipagem visual e converte ideias em estrutura HTML/CSS/JS automática.'
          ]
        },
        {
          tool: 'Next.js',
          url: 'https://nextjs.org/docs',
          actions: [
            'Salvar o link da documentação oficial do Next.js como fonte principal para construção da aplicação.',
            'Consultar sobre: rotas baseadas em arquivos, APIs integradas, SSR (Server Side Rendering), ISR (Incremental Static Regeneration), etc.'
          ]
        },
      ]
    }
  ];
</script>

<div class="content">
  {#each content as item}
    <div class="content-item">
      <h1>{item.title}</h1>
      {#each item.steps as step}
        <div class="step">
          <h2>{step.tool}</h2>
          {#if step.url}
            <a href={step.url} target="_blank" rel="noopener noreferrer">{step.url}</a>
          {/if}
          <ul>
            {#each step.actions as action}
              <li>{action}</li>
            {/each}
          </ul>
        </div>
      {/each}
    </div>
  {/each}
</div>

<style>
  /* Layout geral */
  .content {
    margin: 0 auto;
    padding: 2rem;
    max-width: 1100px;
    margin: 0 auto;
    font-family: 'Inter', sans-serif;
    color: var(--text-color);
    background-color: var(--bg-color);
    border-radius: 8px;
    transition: background-color 0.3s ease, color 0.3s ease;
  }

  /* Títulos */
  h1 {
    font-size: 2rem;
    color: var(--text-color);
    margin-bottom: 1rem;
    font-weight: bold;
  }

  h2 {
    font-size: 1.8rem;
    color: var(--text-color);
    margin-bottom: 1rem;
    font-weight: bold;
  }

  /* Links */
  a {
    color: var(--link-color);
    text-decoration: none;
    font-weight: bold;
  }

  a:hover {
    text-decoration: underline;
  }

  /* Estilos das etapas */
  .step {
    padding: 1.5rem;
    margin-bottom: 1.5rem;
    background-color: var(--card-bg);
    border: 1px solid var(--text-color);
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  }

  ul {
    list-style-type: none;
    padding-left: 0;
  }

  li {
    margin-bottom: 0.5rem;
    font-size: 1.1rem;
    color: var(--text-color);
  }

  li:before {
    content: "•";
    color: var(--link-color);
    font-weight: bold;
    display: inline-block;
    width: 1em;
    margin-left: -1em;
  }
</style>
