<!-- NAVIGATION:START -->
---
[README ConnectTEF](../README.md) | [Índice da Seção](README.md) | [Anterior](../00-INTRODUCTION/MODULES-INDEX.md) | [Proximo](01-O-QUE-E-TEF.md)
---
> **Caminho:** [Inicio](../README.md) / Conceitos / README
<!-- NAVIGATION:END -->

# Conceitos Fundamentais

Antes de iniciar a integra��o com o ConnectTEF, � importante compreender os principais conceitos utilizados ao longo da documenta��o.

Este m�dulo apresenta os componentes que fazem parte do ecossistema de pagamentos, as tecnologias suportadas pela plataforma e os diferentes modelos de integra��o dispon�veis.

O objetivo n�o � ensinar como implementar uma integra��o, mas fornecer a base conceitual necess�ria para compreender a arquitetura e as APIs do ConnectTEF.

---

# Objetivo deste m�dulo

Ao concluir esta se��o voc� compreender�:

- o que � TEF;
- o que � um SmartPOS;
- o papel das adquirentes e facilitadoras;
- como funcionam os sistemas legados baseados em INTPOS;
- o conceito do Gerenciador Padr�o;
- como funcionam Provider Android, Android Intent, API Local e API REST;
- como todos esses elementos fazem parte do ecossistema ConnectTEF.

---

# O que voc� encontrar�

## TEF

Entenda o conceito de Transfer�ncia Eletr�nica de Fundos e seu papel na automa��o comercial.

?? [**01-O-QUE-E-TEF.md**](01-O-QUE-E-TEF.md)

---

## SmartPOS

Conhe�a os terminais inteligentes utilizados pelo ConnectTEF e como eles diferem das solu��es tradicionais de pagamento.

?? [**02-O-QUE-E-SMARTPOS.md**](02-O-QUE-E-SMARTPOS.md)

---

## Adquirente

Entenda o papel das empresas respons�veis pelo processamento e autoriza��o das transa��es financeiras.

?? [**03-O-QUE-E-ADQUIRENTE.md**](03-O-QUE-E-ADQUIRENTE.md)

---

## Facilitadora

Conhe�a as empresas que simplificam o acesso aos meios de pagamento e sua participa��o no ecossistema.

?? [**04-O-QUE-E-FACILITADORA.md**](04-O-QUE-E-FACILITADORA.md)

---

## Gerenciador Padr�o

Descubra como o ConnectTEF permite integrar sistemas legados baseados em INTPOS sem alterar o ERP.

?? [**05-O-QUE-E-GERENCIADOR-PADRAO.md**](05-O-QUE-E-GERENCIADOR-PADRAO.md)

---

## INTPOS

Conhe�a o padr�o tradicional de comunica��o baseado em troca de arquivos e sua import�ncia para sistemas legados.

?? [**06-O-QUE-E-INTPOS.md**](06-O-QUE-E-INTPOS.md)

---

## SiTef

Entenda o conceito do SiTef e sua rela��o com a arquitetura do ConnectTEF.

?? [**07-O-QUE-E-SITEF.md**](07-O-QUE-E-SITEF.md)

---

## Provider Android

Conhe�a uma das formas nativas de integra��o entre aplica��es Android e o ConnectTEF.

?? [**08-O-QUE-E-PROVIDER.md**](08-O-QUE-E-PROVIDER.md)

---

## Android Intent

Entenda como aplica��es Android podem solicitar opera��es ao ConnectTEF utilizando recursos do pr�prio sistema operacional.

?? [**09-O-QUE-E-INTENT.md**](09-O-QUE-E-INTENT.md)

---

## API Local

Conhe�a a interface HTTP local destinada principalmente a aplica��es Desktop e ambientes locais.

?? [**10-O-QUE-E-API-LOCAL.md**](10-O-QUE-E-API-LOCAL.md)

---

## API REST

Entenda a principal interface de integra��o do ConnectTEF para aplica��es Web, SaaS e arquiteturas modernas.

?? [**11-O-QUE-E-API-REST.md**](11-O-QUE-E-API-REST.md)

---

## Gloss�rio

Consulte rapidamente os principais termos utilizados em toda a documenta��o.

?? [**12-GLOSSARIO.md**](12-GLOSSARIO.md)

---

# Como os conceitos se relacionam

```text
                 Cliente
                    �
                    ?
              ERP / PDV
                    �
                    ?
              ConnectTEF
                    �
      +-------------+--------------+
      ?             ?              ?
 API REST     API Local      Android
                                   �
                          +-----------------+
                          ?                 ?
                     Provider          Intent
                    �
                    ?
               SmartPOS
                    �
        +-----------------------+
        ?                       ?
   Adquirente             Facilitadora
                    �
                    ?
        Institui��o Financeira
```

Todos esses conceitos fazem parte da mesma arquitetura e ser�o aprofundados ao longo da documenta��o.

---

# Qual integra��o devo escolher?

O ConnectTEF oferece diferentes formas de integra��o para atender diversos cen�rios tecnol�gicos.

| Cen�rio | Integra��o recomendada |
|---------|------------------------|
| ERP Desktop | API Local |
| ERP Web | API REST |
| ERP SaaS | API REST |
| Aplica��o Android | Provider Android |
| Integra��o Android simplificada | Android Intent |
| ERP legado com INTPOS | Gerenciador Padr�o |
| Sistemas compat�veis com SiTef | Compatibilidade SiTef |

Cada tecnologia ser� detalhada nas pr�ximas se��es.

---

# Para quem este m�dulo � indicado

Este conte�do � recomendado para:

- Desenvolvedores
- Arquitetos de Software
- Integradores
- Parceiros White Label
- Revendedores
- Equipes T�cnicas
- Consultores

---

# Ordem recomendada de leitura

Para melhor compreens�o da plataforma, recomendamos seguir esta sequ�ncia:

1. O que � TEF
2. O que � SmartPOS
3. O que � Adquirente
4. O que � Facilitadora
5. O que � Gerenciador Padr�o
6. O que � INTPOS
7. O que � SiTef
8. O que � Provider Android
9. O que � Android Intent
10. O que � API Local
11. O que � API REST
12. Gloss�rio

Essa sequ�ncia foi planejada para apresentar os conceitos do mais geral para o mais espec�fico.

---

# Pr�ximo m�dulo

Depois de compreender os conceitos fundamentais, prossiga para **Arquitetura**, onde ser� apresentada a organiza��o interna do ConnectTEF, seus componentes, fluxos de comunica��o e princ�pios arquiteturais.

---

# Resumo

O m�dulo **Conceitos** estabelece a base de conhecimento necess�ria para compreender o ecossistema ConnectTEF.

Ao finalizar esta se��o, voc� ter� uma vis�o clara dos principais participantes do ecossistema de pagamentos, das tecnologias suportadas e das diferentes formas de integra��o disponibilizadas pela plataforma.

<!-- NAVIGATION_FOOTER:START -->
---
### Veja tambem
- [README ConnectTEF](../README.md)
- [Índice da Seção](README.md)
- [O que e TEF](01-O-QUE-E-TEF.md)
---
**Navegacao:** [Anterior](../00-INTRODUCTION/MODULES-INDEX.md) | [Inicio](../README.md) | [Proximo](01-O-QUE-E-TEF.md)
<!-- NAVIGATION_FOOTER:END -->
