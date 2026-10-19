# Revisa 2.0 · Seus PDFs, seus estudos

[Baixar APK Android](https://github.com/CBmota41/revisa-android/releases/latest/download/Revisa.apk) · [Abrir no navegador](https://revisa-gabri.web.app/)

O botão **Instalar app** baixa diretamente o APK Android pelo GitHub, no próprio dispositivo.

Entre apenas com um nome de usuário. O perfil é local, sem senha, e permanece aberto ao reabrir o aplicativo. Cada perfil tem sua biblioteca e seu progresso; não há sincronização entre dispositivos.

Escolha **Adicionar PDFs**, selecione um ou vários arquivos do Android ou computador, ajuste o nome de cada matéria e toque em **Ler e gerar estudos**. A biblioteca começa vazia: os materiais de versões anteriores não são carregados automaticamente.

O Revisa lê texto extraível dos PDFs usando PDF.js 6.4.299 (Mozilla, licença Apache 2.0 incluída em vendor/PDFJS-LICENSE.txt). Gera localmente exercícios de completar trechos, definições, referências citadas, datas e afirmações, com respostas, trechos e páginas de origem. Revisão, flashcards e quiz usam a biblioteca importada. Não utiliza serviço externo de IA nem envia PDFs a servidores.

PDFs digitalizados sem texto precisam passar por OCR antes de serem importados. PDFs protegidos precisam ser desbloqueados. Imagens, diagramas e tabelas complexas não são interpretados semanticamente. A qualidade e a quantidade dos exercícios dependem do texto extraído. O limite é de 100 MB por PDF; arquivos duplicados são reconhecidos pelo conteúdo.

Perfil e progresso ficam no armazenamento local; PDFs e estudos ficam no IndexedDB. Limpar os dados do navegador/aplicativo pode apagá-los. **Opções > Salvar backup do progresso** exporta os estudos e o progresso em JSON; os arquivos PDF originais não são incluídos no backup. Guarde os PDFs separadamente. Restaure o JSON para transferir a biblioteca a outro perfil ou dispositivo.

O APK funciona offline desde a instalação. No navegador, aguarde o primeiro carregamento completo para usar offline. Instale atualizações sobre a versão anterior com a mesma assinatura, sem desinstalar. Os dados anteriores permanecem no armazenamento, mas o novo perfil começa com sua própria biblioteca.

Código web em public/. Aplicativo Android em ../revisa-android/. Publicação web: firebase deploy --only hosting --project revisa-gabri. APK e código-fonte distribuídos nas releases do GitHub; a chave de assinatura não é publicada.

Validação: importação de PDF real, geração e fontes, login persistente, perfis separados, quiz com acerto e erro, giro de cartões, progresso após recarregar, backup/restauração da biblioteca e layout móvel. APK assinado com esquemas v2/v3.
