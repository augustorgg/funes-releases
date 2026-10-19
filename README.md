# Funes — APKs

Funes é um app Android pessoal para estudar inglês com revisão espaçada. Este repositório guarda só os APKs publicados nas [Releases](https://github.com/augustorgg/funes-releases/releases). O código-fonte não é público.

## Instalar ou atualizar

1. No celular, abra a [última Release](https://github.com/augustorgg/funes-releases/releases/latest) e baixe o `funes-<versão>.apk`.
2. Abra o arquivo baixado. Na primeira vez, o Android pede para deixar o navegador instalar apps: permita.
3. Num Samsung com o Auto Blocker ligado, a instalação é bloqueada. Desligue em Configurações > Segurança e privacidade > Auto Blocker, instale e ligue de novo.
4. Para atualizar, faça o mesmo com a versão nova. Ela entra por cima e o progresso fica.

O app também avisa quando há versão nova: Créditos > "Procurar atualização". É o único momento em que ele usa a internet.

Se o Android disser que o pacote conflita com um app já instalado, **não desinstale**: o progresso iria junto. Isso quer dizer que o APK não foi assinado pela chave do Funes. As notas de cada Release trazem:
- o `versionCode`;
- o commit do código;
- o sha256 do APK;
- o SHA-256 do certificado: `ee4cbeb7928474db907987448f4aa16110973d8ecaa486060e0167a327c3a68a`.

## Licenças

- **App (código):** não é software livre; todos os direitos reservados.
- **Deck-semente** (dentro do APK e anexo de cada Release como `funes-<versão>-deck-semente.tsv`):
  - Adapta a New General Service List (NGSL) 1.2, de Browne, C., Culligan, B. e Phillips, J. (https://www.newgeneralservicelist.com), licenciada sob CC BY-SA 4.0.
  - Mudanças: palavras filtradas para os níveis A2–B1, rank mantido, traduções e frases de exemplo geradas por LLM e não revisadas.
  - O deck é distribuído sob CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/).
  - A coluna `cefr` (e o prefixo `cefrj16` da chave) vem da CEFR-J Wordlist 1.6 e segue os termos dela: "The CEFR-J Wordlist Version 1.6. Compiled by Yukio Tono, Tokyo University of Foreign Studies. Retrieved from https://www.cefr-j.org/data/CEFRJ_wordlist_ver1.6.zip on 19/10/26."
- **Agendamento:** port do FSRS-6 do [py-fsrs](https://github.com/open-spaced-repetition/py-fsrs) 6.3.2, sob a licença MIT:

  > MIT License
  >
  > Copyright (c) 2022 Open Spaced Repetition
  >
  > Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
  >
  > The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
  >
  > THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

- **Bibliotecas dentro do APK:** todas sob Apache License 2.0, com o texto em [LICENSE-APACHE-2.0.txt](LICENSE-APACHE-2.0.txt). Nenhuma traz arquivo NOTICE. São elas:
  - Kotlin;
  - kotlinx.coroutines;
  - kotlinx.serialization;
  - AndroidX: Core, Activity, Lifecycle, Compose, Room, SQLite e dependências;
  - Koin;
  - Stately.
