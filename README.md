# Briefing Pizzaria Deliziosa

## 1) Contexto e Objetivo
**Objetivo do produto:** Plataforma web/mobile para pedidos de pizza com entrega ou retirada, pagamento online e rastreamento do pedido. 
**Proposta de Valor:** Reduzir tempo médio de pedido, diminuir erros de comunicação e aumentar ticket médio via combos/cupons. 

## 2) Público alvo e Personas 
-**Cliente Final(João):** Realiza 3-4 pedidos/mês, busca praticidade e cupons 
-**Atendente:** Monitora a fila, resolve exceções
-**Gestor:** Acompanha vendas, tempo de preparo e satisfação
-**Entregador:** Recebe rota e registra comprovação de entrega 

## 3) Processo atual e dores
Pedidos são feitos por whatsapp/telefone -> erros de sabor/endereço/troco, fila em picos, nenhuma visibilidade de status, chechout demorado

## 4) Escopo do MVP (Produto Mínimo Viável) 
Catálogo (sabores, tamanhos, adicionais), Carrinho, Checkout(Endereço + Pagamento), Pedidos(Status)
Cupons, Administrativo Básico(cardápio, horários, preços, cupons, taxa por zona(perímetro)
**Fora do escopo MVP:** Fidelidade, multilojas, multi-idioma

## Regras de Negócio
1. Pedido só é finalizado com **endereço válido** (CEP+Número)
2. **Área de entrega por zona:** (Z1/Z2) com taxas diferentes
3. **Horário de funcionamento:** Aceita pedidos apenas no intervalo configurado
4. **Tamanho:** (P/M/G) altera preço e tempo de forno
5. **Adicionais:** Borda recheada soma R$8,00 por pizza
6. **Cupons:** Não cumulativos; "PiZZA10" aplica 10% ao subtotal
7. **Tempo estimado** = preparo + fila + entrega por zona (exibir ao cliente)
8. **Pagamento online:** captura imediata; **PIX** confirmação automática
9. **Estoque crítico:** Falta de ingredientes torna sabor indisponível
10. **Pedido mínimo** para entrega (ex.R$30,00)
11. **Retirada no balcão** sem taxa; exigir **código de retirada**
12. **Cancelamento:** Até 2 min após pagamento é automático; depois, via atendente

## 6) Requisitos Funcionais 
**Pedidos:** status, Recebido -> Em preparo -> Saiu para entrega -> Entregue
**Catálogo:** Listar os sabores, tamanhos, combos, busca por ingredientes
**Carrinho:** Alterar quantidades, adicionais, observações
**Endereço:** CEP auto-preenchido, multiplos endereços salvos 
**Pagamento:** Cartão (Gateway) e **PIX** (QR + Confirmação), pagar na retirada 
**Cupons:** Validação, cálculo e auditoria de uso
**Administrativo:** Cardápio, preços, horários, cupons, taxa por zona, fila de pedidos
**Notificações:** e-mail/whatsapp ao mudar de status 

## 7) Requisitos não Funcionais 
**Performance:** resposta < 1s, pico de **100 pedidos/min** em promoções
**Segurança:** LGPD (Consentimento/privacidade) 
**Disponibilidade:** 99.5% no horário de funcionamento; **backup diário** 
**Usabilidade e acessibilidade:** Contraste AA, navegação por teclado
**Compatibilidade:** Responsivo (mobile-first), navegadores modernos
**Observabilidade:** Logs de auditoria (pagamentos, cupons) 

## 8) Integrações 
Pagamentos (gateway + **PIX**), CEP/Mapas (validação e zona), mensageria(whatsapp/smtp(protocolo de e-mail)) 

## Cronograma
-**Sprint 1 (2 sem.):** Catálogo + Carrinho 
-**Sprint 2 (2 sem.):** Checkout + Pagamento 
-**Sprint 3 (2 sem.):** Pedidos + Admin + Métricas 
-**Go-live** (soft launch) 

## Backlog inicial 
1. Como cliente **Listar pedidos**
2. Como cliente **Filtrar Pizzas**
3. Como cliente **Adicionar/Remover pizzas**
4. Como cliente **Aplicar cupom**
5. Como cliente **Calcular taxa/tempo por zona**
6. Como cliente **Salvar endereço**
7. Como cliente **Pagar com pix**
8. Como cliente **Acompanhar status**
9. Como admin **Gerenciar cardápio**
10. Como admin **Definir taxa por zona**
11. Como admin **Criar cupons**
12. Como atendente **cancelar pedido**
13. 
    






