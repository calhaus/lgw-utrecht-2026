# LGW × U? — Planeador 2026 (PWA)

Aplicação web independente para os festivais Le Guess Who? e U? em Utrecht, 5–8 novembro de 2026.

## Publicar gratuitamente no GitHub Pages

1. Extrair o ZIP.
2. Criar um repositório GitHub novo, por exemplo `lgw-utrecht-2026` (público se estiveres no plano gratuito).
3. Na página do repositório, escolher **Add file → Upload files** e enviar **o conteúdo desta pasta**, e não o ZIP. Manter `index.html`, `manifest.webmanifest`, `sw.js`, `.nojekyll` e a pasta `icons/` na raiz.
4. Premir **Commit changes**.
5. Ir a **Settings → Pages → Build and deployment**, escolher **Deploy from a branch**, branch `main` e pasta `/(root)`, e **Save**.
6. O endereço será `https://TEU_UTILIZADOR.github.io/lgw-utrecht-2026/` se usares esse nome de repositório.
7. Abrir o link por HTTPS (não o HTML local) e tocar em **Instalar app** para ver instruções ou iniciar a instalação quando o navegador permitir.

## Privacidade

O site, o seu código e as preferências partilhadas como estado inicial são públicos. **Não existem contas nem sincronização**: as alterações de cada visitante ficam guardadas localmente em `localStorage` do seu navegador, neste endereço de origem. Usar **Guardar JSON** para fazer uma cópia de segurança. É possível que a aplicação instalada no iPhone utilize armazenamento diferente do Safari normal, e a transferência para outro dispositivo requer exportação/importação.

Informações de voos/hotel, sem dados identificadores de reservas, estão incluídas como logística pública. Nenhum PDF, código de bilhete, referência de voo da reserva, email pessoal ou ficheiro JSON completo com dados pessoais faz parte deste pacote.

## Funcionamento offline

A aplicação guarda os ficheiros principais via service worker na primeira visita em HTTPS. Programação e classificações funcionam sem rede depois dessa visita. **Mapas, percursos e horários/compras de comboio precisam de Internet**.

## Atualizações

Editar `index.html` no repositório e aguardar publicação. As classificações do visitante não são alteradas quando se publica uma nova versão, pois ficam no browser. Para forçar uma nova predefinição nos visitantes que já utilizaram a app, cada um deve usar o botão **Repor seleção partilhada** ou importar outro JSON.

Se alterares os ficheiros offline (index.html, ícones...), atualiza a constante `CACHE_NAME` no ficheiro `sw.js` (por ex. `...-v2`) para distribuir a atualização do cache. Poderá ser necessário fechar/reabrir a aplicação para a nova versão entrar em vigor.
