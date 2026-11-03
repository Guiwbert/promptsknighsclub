# Motion skills (tipografia e Reels)

Skills do Claude Code para animar texto por código, sem depender de modelo de vídeo para desenhar letra.
O Claude Code carrega tudo que está em `.claude/skills/` automaticamente quando a sessão é aberta neste repositório (na nuvem ou no PC).

Origem: [iart-ai](https://github.com/iart-ai), licença MIT (ver `LICENSE-iart-ai`). Copiadas sem alteração.

| Skill | Pacote de origem | Para que serve |
|---|---|---|
| `kinetic-typography` | kinetic-typography-skills @ fccc94b | Títulos, lyric video, reveal por linha/palavra/letra, fonte variável |
| `caption-animation` | tiktok-video-skills @ 2a77533 | Legenda palavra por palavra, karaokê, palavra ativa destacada |
| `short-form-video` | tiktok-video-skills @ 2a77533 | Reels/TikTok: gancho, ritmo, retenção, áreas seguras 9:16 |
| `remotion-video` | motion-design-skills @ 3c129f7 | Renderizar o vídeo final em MP4 a partir de código (React) |
| `beat-sync-editing` | motion-design-skills @ 3c129f7 | Cortes e entradas de texto sincronizados com a batida |
| `animation-principles` | motion-design-skills @ 3c129f7 | Easing e timing para o movimento não parecer barato |
| `motion-art-direction` | motion-design-skills @ 3c129f7 | Linguagem de motion consistente da marca |

## Fluxo recomendado

1. Gerar o vídeo de cena (Veo, Seedance etc.) **sem texto**: incluir `no text, no captions, no typography, no subtitles` no negativo.
2. Pedir a tipografia ao Claude Code, que usa as skills acima e renderiza por código.
3. Juntar as duas camadas (Remotion já compõe vídeo + texto e exporta o MP4).

## Prompts de exemplo

- "Faz um lyric video 9:16 com tipografia cinética sincronizada com essa música. Letra: [...]. Reveal por palavra no refrão, por linha nos versos."
- "Coloca legenda animada palavra por palavra nesse vídeo, estilo Reels, com a palavra ativa em destaque na cor da marca."
- "Cria um title card animado com 'Knights Club' usando mask reveal e easing premium, 1080x1920, 3 segundos."

## Atualizar

```bash
npx skills add iart-ai/kinetic-typography-skills
npx skills add iart-ai/tiktok-video-skills
npx skills add iart-ai/motion-design-skills
```

Obs.: `iart-ai/motion-skills` é só o índice dos pacotes e não contém skills.
