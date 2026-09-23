# JC Alvos Metálicos — atualização do site

Preparado em 14/09/2026.

## Arquivos

- **index.html**: versão atualizada para colocar na hospedagem.
- **index-original.html**: cópia exata do HTML recebido, para recuperação.
- **MANUTENCAO-MENSAL.md**: roteiro de manutenção e modelo de relatório ao cliente.
- **jc-assinatura-metalica.png**: arte horizontal criada com base na logo enviada; fundo transparente. A mesma imagem já está incorporada ao HTML.
- **ARTE-DA-MARCA.md**: referência, ferramenta e prompt utilizados na criação da arte.

As fotos, os vídeos e o favicon não foram fornecidos. Os caminhos existentes foram preservados. Este pacote não inclui essas mídias; utilize a pasta `midias` e o favicon que já estão na hospedagem. Ao abrir o HTML sozinho no computador, essas imagens e vídeos não aparecerão.

## O que foi alterado

1. Carrinho salvo neste navegador por até 30 dias sem atualização. Restaura somente produtos e opções válidos, com preços do catálogo atual. Nenhum nome, telefone, e-mail ou CEP é salvo junto do carrinho.
2. Busca por nome, categoria e descrição, sem diferenciar maiúsculas ou acentos; ordenação por categoria, nome e preço; contador e mensagem para busca sem resultados. O catálogo agora também reúne os lançamentos, totalizando 37 produtos.
3. Indicação “A partir de” para produtos com opções e uso do menor preço das opções nos cards e na ordenação. Preço com desconto no PIX em destaque, preço normal no cartão logo abaixo e economia indicada na janela do produto. Os valores cadastrados já eram PIX e foram preservados: o normal é calculado dividindo o PIX por 0,90, com arredondamento em centavos. Exemplo: R$ 2.350,00 no PIX e R$ 2.611,11 no cartão. O parcelamento é informado como “em até 3x sem juros”, sem apresentar parcelas iguais que possam divergir do total por centavos.
4. Validação de nome, telefone brasileiro com DDD, e-mail opcional, descrição e CEP opcional. Telefone e CEP recebem formatação durante o preenchimento.
5. Links diretos para produtos e variações, com botão para copiar o link. Exemplo: `https://jcalvosmetalicos.com.br/#produto=P31&variacao=2`. Esses endereços abrem a janela do produto; não são páginas independentes para indexação.
6. Carrinho e mensagem para WhatsApp identificam o subtotal dos produtos no PIX e o frete a confirmar. O site abre uma mensagem pronta; o visitante precisa enviá-la no WhatsApp. Não calcula frete, não cobra pagamento e não confirma pedidos automaticamente.
7. Contatos e dados estruturados padronizados para **(62) 99371-6078**, conforme confirmação do responsável.
8. Vídeos carregados quando entram na área visível, com controles de reprodução e pausa quando saem dela ou a aba fica oculta. Reprodução automática evitada quando o navegador informa preferência por movimento reduzido ou economia de dados. Rotações das imagens ficam suspensas fora da tela.
9. Melhorias de teclado, foco nos diálogos, identificação dos controles e margens no celular. Nas variações, os alvos recebem uma animação de impacto ao selecionar a opção, com rastro, faíscas, recuo e marca central. O efeito acontece uma vez por seleção, sem som, e respeita a preferência de movimento reduzido do navegador. Os controles funcionam também pelo teclado.
10. Integração de estatísticas preparada, inicialmente desligada, com escolha opcional do visitante e opção para revogar no rodapé. Texto de privacidade atualizado para explicar carrinho e medição.
11. Barra de rolagem fina em laranja sobre fundo escuro, rótulos de campos padronizados e menu de ordenação personalizado com seleção destacada. O menu permite uso por mouse, toque e teclado; fecha com Escape ou clique fora e acompanha a limpeza dos filtros.
12. Cabeçalho com moldura suspensa, cantos assimétricos, acabamento escuro e assinatura laranja. A marca mantém a logo original, recebe a legenda “Fabricação nacional”, e a navegação destaca a página ativa. O botão “Meu pedido” abre o carrinho. A versão móvel é compacta e o menu fecha ao navegar, clicar fora ou pressionar Escape. Layout conferido em seis larguras, de 320 a 1865 pixels.
13. Cena de fundo original em canvas para toda a janela do site: silhuetas humanoides clássicas de chapa de ferro, pintura fosca, marcas de uso, haste e base metálicas. Os alvos não acompanham o mouse e ficam imóveis entre os impactos automáticos; o recuo, os projéteis estilizados e as pequenas faíscas foram mantidos. Foram retirados os discos, os anéis luminosos, a grade de perspectiva e os reflexos móveis. A composição substitui a imagem estática da abertura quando o canvas está disponível, fica mais discreta fora dela e permanece atrás do conteúdo, sem bloquear cliques. A cena é decorativa; não apresenta cálculos nem dados balísticos reais.
14. Efeitos curtos de interação em todos os botões e links de ação: leve elevação ao passar o cursor e pressão ao clicar, sem movimentos contínuos. Filtros, variações e controles de quantidade mantêm os efeitos quando são recriados pela página. Também funcionam por teclado e respeitam a preferência de movimento reduzido. O fundo não acompanha esses movimentos de interação.

15. O medalhão circular flutuante da abertura foi substituído por uma assinatura horizontal fixa, com letras metálicas e as três cores da logo. Essa arte foi gerada com ImageGen a partir da referência enviada. A imagem está incorporada ao `index.html`; não é necessário publicar o PNG separado para que a abertura funcione.

### Animação contínua e fluidez

O botão de pausa foi removido, conforme solicitado. A cena roda continuamente enquanto a página está visível, inclusive com produto ou carrinho aberto, sem acompanhar o cursor. Preferências antigas de pausa salvas na sessão são ignoradas. A aba oculta suspende o processamento e a animação volta automaticamente quando a página fica visível. O fundo não usa a preferência de movimento reduzido para parar; os efeitos dos botões e os vídeos mantêm seus comportamentos anteriores.

A animação tem alvo de 60 quadros por segundo, com limite também em telas de alta frequência. Texturas dos alvos e máscaras de contraste são preparadas uma vez e reutilizadas; marcas de impacto atualizam somente a camada necessária. A resolução do canvas é limitada para reduzir o custo de desenho. Não há som, biblioteca externa nem arquivo de vídeo para esse fundo. Os demais arquivos de mídia do site continuam necessários para logo do cabeçalho, fotos e vídeos dos produtos.

Verificações da versão atual: arte transparente e sem flutuação, ausência de controle de pausa, animação ativa mesmo com preferência antiga de pausa salva, continuidade durante produto e carrinho, layout nas larguras de 320 e 390 pixels e ausência de erros de JavaScript. Medição em Chrome local, janela de 1600 × 1000, por aproximadamente 3 segundos: 60 fps, 181 quadros; mediana de 0,2 ms e percentil 95 de 0,4 ms no trabalho JavaScript de desenho. Esses tempos não incluem todo o trabalho de GPU/composição. O resultado local não garante 60 fps em todos os aparelhos; conferir também após a publicação.

## Colocar no ar

1. Faça um backup da versão atualmente publicada e de suas mídias. O `index-original.html` deste pacote é apenas o HTML recebido nesta conversa e pode ser diferente da versão no servidor.
2. Substitua somente o `index.html` na mesma pasta da hospedagem. Preserve `midias` e o favicon. Não é necessário publicar o backup nem os documentos deste pacote.
3. Caso a hospedagem use cache, atualize-o pelo painel.
4. Confira no endereço público: fotos, vídeos, catálogo, uma variação de produto, carrinho após atualizar a página e link direto de um produto.
5. Confira o número e a mensagem ao abrir o WhatsApp. Não é necessário enviar um pedido para verificar a mensagem.

Esta entrega não foi publicada na hospedagem.

## Ativar as estatísticas

Falta o ID de medição da conta Google Analytics do cliente. A integração permanece desligada até ele ser informado.

No `index.html`, procure `analyticsId: ''` e coloque o ID entre as aspas, por exemplo `analyticsId: 'G-XXXXXXXXXX'`. O exemplo não é uma conta válida. Não insira senha nem chave de acesso.

Na configuração do fluxo web do GA4, desative a **medição otimizada** para que as interações automáticas não dupliquem os eventos implementados. Esta versão envia explicitamente os seguintes eventos:

| Evento | O que representa |
|---|---|
| `page_view` | Visita ao início ou ao catálogo |
| `view_item` | Abertura de um produto |
| `add_to_cart` | Adição de um produto ao carrinho |
| `whatsapp_click` | Clique para abrir o WhatsApp; identifica a origem, como carrinho ou orçamento |

Para analisar a origem dos contatos, cadastre no GA4 uma dimensão personalizada de escopo de evento para o parâmetro `origem`. O interesse por produto utiliza os campos de item enviados nos eventos de comércio eletrônico. É possível marcar `whatsapp_click` como evento principal, entendendo que ele não comprova conversa nem venda.

Após configurar e publicar, autorize a medição no aviso do site, abra um produto, adicione-o ao carrinho e verifique a chegada dos eventos no relatório em tempo real da conta. Depois teste a recusa e a alteração da preferência pelo rodapé. Bloqueadores, recusa de consentimento e restrições do navegador podem reduzir os números registrados.

O código não envia nome, telefone, e-mail, CEP, descrição do pedido ou termo de busca para seus eventos. O Google Analytics tem seu próprio processamento técnico quando autorizado. As estatísticas dependem do serviço externo; não existe um painel administrativo embutido no HTML.

Referência: [documentação oficial de eventos do Google Analytics](https://developers.google.com/analytics/devguides/collection/ga4/events).

## Verificação realizada

Testes em navegador Chrome local: inicialização sem erros de JavaScript; 37 produtos; busca e ausência de resultados; ordenação crescente e decrescente; link com variação; carrinho após recarregar; quantidades; validação de CEP, telefone e e-mail; dados da mensagem do WhatsApp; restauração de carrinho adulterado sem confiar em preço ou texto externos; produto inexistente; layout e ausência de rolagem horizontal no celular; autorização e revogação de estatísticas usando um serviço simulado.

Nenhuma mensagem foi enviada ao WhatsApp. O Analytics real não foi ativado nem recebeu os dados dos testes. A qualidade e a disponibilidade das mídias, o ganho de velocidade com os arquivos reais e o recebimento de eventos na conta do cliente ainda precisam ser conferidos no ambiente publicado.

A apresentação de preços foi conferida em 70 combinações de produtos/opções. O carrinho mantém os valores PIX originais. Também foram verificados a economia exibida, a animação de impacto, a manutenção de foco pelo teclado, o movimento reduzido e a ausência de rolagem horizontal nas larguras de 320 e 390 pixels.

## Recuperação

Se precisar desfazer esta atualização, use o backup que foi feito da hospedagem. Se ele corresponder ao HTML originalmente enviado, uma alternativa é publicar `index-original.html` com o nome `index.html`. Preserve as mídias durante a troca.
