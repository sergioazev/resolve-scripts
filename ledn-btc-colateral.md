# Empréstimo com Bitcoin como Colateral — LEDN
*Raciocínios desenvolvidos em junho de 2026*

---

## 1. O que é

Você deposita Bitcoin como garantia (colateral) e recebe dólares emprestados. É como penhorar uma joia para pegar dinheiro, mas a joia é Bitcoin. Se pagar a dívida, recebe o Bitcoin de volta. Se não pagar, a LEDN fica com o Bitcoin.

---

## 2. Estrutura do empréstimo

- **LTV (Loan-to-Value):** máximo 50% do valor do colateral. Recomendado: 25–40%.
- **Prazo:** 12 meses, renovável.
- **Pagamento:** juros mensais (~9,5% ao ano). Principal devolvido no vencimento em parcela única.
- **Taxa de originação:** 2% cobrada na largada — diluída pelo prazo.
- **Moeda:** USD, USDC ou USDT.
- **Modelo recomendado:** Custódia Pura (Bitcoin não é rehipotecado).

### Diluição da taxa de originação + juros

| Prazo | Custo mensal efetivo |
|---|---|
| 1 mês | ~2,8% |
| 6 meses | ~1,15% |
| 12 meses | ~0,95% |

---

## 3. Se o preço do BTC cair — risco de liquidação

| LTV | Zona de aviso | Chamada de margem | Liquidação |
|---|---|---|---|
| 40% | 70% LTV | 80% LTV | ~83% LTV |
| 25% | 70% LTV | 80% LTV | ~83% LTV |

**Com BTC a $60.000 e LTV de 25%:** liquidação apenas abaixo de ~$18.750 (-69% adicional).

**Com BTC a $60.000 e LTV de 40%:** liquidação abaixo de ~$30.000 (-50% adicional).

### Processo da chamada de margem

1. BTC cai → LTV sobe → aviso da LEDN
2. Prazo de ~72h para reforçar colateral ou pagar parte da dívida
3. Se não agir: liquidação automática (venda do BTC a preço de mercado)
4. Em flash crash: aviso e liquidação podem ocorrer quase simultaneamente

---

## 4. Se o preço do BTC subir

Nada muda no contrato. Você continua devendo o mesmo valor. O LTV cai — você fica mais seguro. Ao quitar no vencimento, recupera o Bitcoin agora mais valorizado.

**Exemplo:** depositou 1 BTC a $60.000, pegou $30.000 (50% LTV). BTC foi a $120.000. Paga $30.000 + juros. Recupera 1 BTC valendo $120.000.

---

## 5. Riscos menos óbvios (traps)

| Risco | Natureza |
|---|---|
| Falência da plataforma | Colateral inacessível mesmo pagando em dia (Celsius, BlockFi já faliram) |
| Flash crash | Liquidação antes de você conseguir reagir |
| Tributação na liquidação | Evento tributável mesmo sendo forçado — imposto sobre ganho de capital |
| Custo > valorização | Se BTC subir menos de 10% aa, teria sido melhor vender e recomprar |
| Não renovação forçada | LEDN pode não renovar — você liquida num momento ruim |
| Concentração na plataforma | Colateral + reserva + acumulação todos na LEDN = risco único |
| Stress operacional | Monitorar preço 24h é psicologicamente caro |

---

## 6. Infraestrutura operacional — USDC/USDT

LEDN aceita USDC e USDT para receber o empréstimo, pagar juros e reforçar colateral. Transferências funcionam 24h, inclusive madrugadas, domingos e feriados. Chegam em minutos.

### Auto Top-Up

Ferramenta da LEDN que puxa automaticamente USDC da sua conta de movimentação para reforçar o colateral se o BTC cair ao limite configurado. Transferência interna — instantânea e gratuita.

### Yield no USDC depositado

USDC parado na LEDN rende ~7% ao ano (varia). A reserva de emergência trabalha enquanto aguarda.

---

## 7. Os quatro baldes — dimensionamento

*Baseado em: empréstimo de $2.000, BTC a $60.000, LTV de 25%, Custódia Pura, bear market em curso (ATH: $126.100 em outubro 2025).*

| Balde | Função | Valor | Onde |
|---|---|---|---|
| **1 — Colateral BTC** | Garantia do empréstimo | 0,133 BTC (~$8.000) | LEDN bloqueado |
| **2 — Extintor USDC** | Auto Top-Up em quedas bruscas | $500 | LEDN rendendo ~7% aa |
| **3 — Reserva externa** | Último recurso fora da LEDN | $300 | Fora da LEDN — nunca entra |
| **4 — Acumulação mensal** | Escudo cambial para quitação | $167/mês | Fora da LEDN até mês 11 |

**Custo mensal líquido:** ~$16 (após abater yield do Extintor)
**Taxa mensal efetiva líquida:** ~0,81%

### Lógica de cada balde

- **Extintor:** cobre flash crash sem depender de bancos ou horário comercial
- **Reserva externa:** isolada do risco de contraparte da LEDN
- **Acumulação:** fica exposta à LEDN apenas nos últimos 30–60 dias, minimizando concentração

---

## 8. Escudo Cambial — eliminando o risco do câmbio

A dívida é em dólar. O real pode desvalorizar. Solução:

1. A cada entrada de dinheiro novo em reais, compra o equivalente em USDC
2. Guarda fora da LEDN
3. No vencimento, usa os dólares acumulados para quitar — câmbio travado no momento da compra

Ao final, dívida em dólar encontra reserva em dólar. Risco cambial zerado.

---

## 9. Comparativo com crédito brasileiro

| Modalidade | Taxa mensal | Exige garantia | Burocracia |
|---|---|---|---|
| Cartão rotativo | 15–20% | Não | Não |
| Cheque especial | 8% (teto legal) | Não | Não |
| Empréstimo pessoal | 3–6% | Não | Score + renda |
| Consignado INSS | 1,5–1,8% | Desconto em folha | Ser aposentado |
| Financiamento imobiliário | 0,8–1,1% | O imóvel | Meses de processo |
| **LEDN (este caso)** | **~0,81%** | Bitcoin | Nenhuma |

**Conclusão:** taxa equivalente ao financiamento imobiliário — sem imóvel, sem banco, sem score, sem análise, disponível em minutos a qualquer hora.

---

## 10. Contexto de bear market — dados históricos

**ATH:** $126.100 (outubro 2025)
**Hoje:** $60.000 (junho 2026)
**Queda do ATH:** -52%

### Fundos históricos a partir do ATH

| Ciclo | Queda do ATH | Fundo estimado (base $126.100) | Queda adicional desde $60k |
|---|---|---|---|
| Otimista | -70% | ~$37.800 | -37% |
| Base (2022) | -77% | ~$29.000 | -52% |
| Histórico médio | -84% | ~$20.200 | -66% |
| Histórico extremo | -86% | ~$17.700 | -71% |

**Com LTV de 25%**, liquidação em ~$18.750 — sobrevive a todos os cenários exceto o extremo histórico.

---

## 11. O melhor momento para tomar o empréstimo

**No fundo do bear market** — a lógica é contra-intuitiva mas sólida:

- A distância percentual até a liquidação é a mesma em qualquer preço
- No fundo, o risco de queda adicional é historicamente menor
- O potencial de valorização do colateral é máximo
- Não há competição — o mercado está vazio

```
Estratégia completa:

Agora:         entender, montar baldes, estar preparado
Emergência:    executar se precisar — mercado não decide
No fundo:      executar com convicção — fiat all-in separado,
               colateral captura a recuperação intacto
```

---

## 12. As três fases do fundo de bear — proteção psicológica

**Fase 1 — Pânico:** queda rápida, manchetes apocalípticas. Doloroso mas agudo — passa.

**Fase 2 — Sangue nas ruas:** exaustão, mãos fracas saem. Ainda dá para sentir o mercado.

**Fase 3 — O limbo:** BTC para de cair mas não sobe. Silêncio. Grupos morrem. "Especialistas" somem. Não é dor — é irrelevância. **É essa fase que expulsa mais gente do que o pânico.**

Quem tem memória de ciclo sabe que tem fim. Compra com calma, sem euforia, sem competição.

---

## 13. Princípios que guiam a estratégia

1. **Mercado não decide a execução** — emergência pontual decide
2. **LTV conservador é a primeira linha de defesa** — silenciosa e gratuita
3. **Extintor pré-posicionado** — o segredo é antecipar, não reagir
4. **Não concentrar tudo na LEDN** — dividir os ovos entre dentro e fora da plataforma
5. **Fiat all-in no fundo é separado do empréstimo** — alavancagem nunca entra nessa conta
6. **O papel na gaveta** — decisões tomadas com a cabeça fria, executadas na hora certa

---

*Documento gerado a partir de conversa em junho de 2026.*
