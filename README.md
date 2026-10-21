# Lísia Helena Guerra | Gestão Condominial

Landing page de apresentação da Lísia Helena Guerra, síndica profissional em Porto Alegre.

Feita com [Astro](https://astro.build) e [Tailwind CSS](https://tailwindcss.com) v4.

## Seções

A página é montada em `src/pages/index.astro`, na seguinte ordem:

| Seção          | Componente               | Âncora          |
| :------------- | :----------------------- | :-------------- |
| Hero           | `Hero.astro`             | —               |
| A Especialista | `ExecutiveProfile.astro` | `#sobre`        |
| Certificações  | `Certificates.astro`     | `#certificados` |
| Áreas de Atuação | `Services.astro`       | `#servicos`     |
| Dúvidas        | `Faq.astro`              | `#faq`          |
| Chamada final  | `FinalCTA.astro`         | —               |

Além disso, `Header.astro` e `Footer.astro` ficam fixos na página, `AnimatedBackground.astro` desenha o fundo animado e `FloatingWhatsApp.astro` mostra o botão flutuante do WhatsApp.

## Estrutura

```text
/
├── public/                 # Arquivos servidos como estão (favicon)
├── src/
│   ├── assets/             # Imagens otimizadas pelo Astro
│   │   └── certificados/   # Imagens da seção de certificações
│   ├── components/         # Seções e elementos da página
│   ├── pages/index.astro   # Página única
│   ├── styles/global.css   # Tema (cores e fontes) e estilos globais
│   └── config.js           # Número e mensagem padrão do WhatsApp
└── package.json
```

## Como editar

- **WhatsApp:** o número e a mensagem padrão ficam em `src/config.js`. O script em `WhatsAppScript.astro` monta o link do WhatsApp só no momento do clique, em qualquer elemento com a classe `js-wa-link`.
- **Certificados:** para trocar uma imagem, substitua o arquivo em `src/assets/certificados/` mantendo o mesmo nome. As legendas e os textos alternativos ficam no topo de `src/components/Certificates.astro`.
- **Cores e fontes:** definidas no bloco `@theme` de `src/styles/global.css`.

## Comandos

Requer Node.js 22.12 ou superior. Rode os comandos na raiz do projeto:

| Comando           | Ação                                          |
| :---------------- | :-------------------------------------------- |
| `npm install`     | Instala as dependências                       |
| `npm run dev`     | Inicia o servidor local em `localhost:4321`   |
| `npm run build`   | Gera o site de produção em `./dist/`          |
| `npm run preview` | Visualiza o build localmente antes do deploy  |

## Licença

Todos os direitos reservados. O repositório é público para consulta, mas o código, o design, os textos e as imagens não podem ser copiados ou reutilizados sem autorização. Veja o arquivo [LICENSE](LICENSE).
