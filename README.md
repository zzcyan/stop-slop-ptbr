# Stop Slop (português do Brasil)

Skill para o Claude tirar dos textos em português as marcas de escrita de IA.

Adaptação de [stop-slop](https://github.com/hardikpandya/stop-slop), de Hardik Pandya. A original foi feita para inglês e lista vícios do inglês ("Here's the thing", "deep dive", advérbios em -ly). Esta versão mantém as regras de estrutura e troca as listas pelos vícios que a IA deixa em português.

## Instalação no Claude Code

macOS e Linux:

```bash
git clone https://github.com/zzcyan/stop-slop-ptbr.git ~/.claude/skills/stop-slop-ptbr
```

Windows (PowerShell):

```powershell
git clone https://github.com/zzcyan/stop-slop-ptbr.git "$env:USERPROFILE\.claude\skills\stop-slop-ptbr"
```

A skill vale em todos os projetos. Abra uma sessão nova do Claude Code e ela entra sozinha quando o pedido envolve escrever, editar ou revisar texto em português. Para chamar na mão, use `/stop-slop-ptbr`.

Para atualizar:

```bash
git -C ~/.claude/skills/stop-slop-ptbr pull
```

Para remover, apague a pasta `~/.claude/skills/stop-slop-ptbr`.

## Outros usos

- **Projetos do Claude (claude.ai):** envie o `SKILL.md` e os arquivos de `referencias/` para o conhecimento do projeto.
- **Instruções personalizadas:** copie as regras principais do `SKILL.md`.
- **API:** inclua o `SKILL.md` no prompt de sistema.

## O que a skill corta

- **Frases:** aberturas que enrolam ("O ponto é o seguinte", "A verdade é que", "É aí que entra"), enchimento ("Vale ressaltar que", "No cenário atual"), jargão (alavancar, potencializar, robusto, jornada, destravar) e advérbios em -mente. Lista em `referencias/frases.md`.
- **Estruturas:** contraste "não é X, é Y", lista do que a coisa não é, frases picotadas, perguntas retóricas de preparação, coisa agindo como gente, narrador de longe e voz passiva. Lista em `referencias/estruturas.md`.
- **Específico do português:** gerúndio pendurado no fim da frase ("..., garantindo mais agilidade"), "-se" sem dono ("acredita-se", "percebe-se") e substantivo no lugar do verbo ("realizar a análise", "efetuar o pagamento").
- **Ritmo:** travessão, listas de três, frases curtas empilhadas e parágrafos que sempre terminam com frase de efeito.

Os exemplos de antes e depois ficam em `referencias/exemplos.md`.

## Nota de revisão

A skill dá de 1 a 10 em cinco critérios: objetividade, ritmo, confiança, autenticidade e densidade. Abaixo de 35 de 50, o texto volta para revisão.

## Cuidado

As regras são duras: nenhum advérbio em -mente, nenhuma voz passiva, nada de lista de três. Funcionam bem em post, e-mail, mensagem e artigo. Em documentação técnica, contrato ou texto jurídico, revise o resultado antes de usar.

## Licença

MIT. Mantém o aviso de licença do projeto original, de Hardik Pandya.
