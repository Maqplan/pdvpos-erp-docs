<!-- NAVIGATION:START -->
---
[README ConnectTEF](../README.md) | [Índice da Seção](README.md) | [Anterior](08-O-QUE-E-PROVIDER.md) | [Proximo](10-O-QUE-E-API-LOCAL.md)
---
> **Caminho:** [Inicio](../README.md) / Conceitos / O que e Intent
<!-- NAVIGATION:END -->

# O que � Android Intent?

O Android Intent � um mecanismo nativo do sistema operacional Android utilizado para permitir que uma aplica��o solicite a execu��o de uma a��o em outra aplica��o.

No ConnectTEF, esse mecanismo permite que um aplicativo comercial solicite opera��es de pagamento ao aplicativo respons�vel pela integra��o com o SmartPOS de forma simples, segura e utilizando recursos nativos do Android.

---

# Objetivo

Compreender o conceito de Android Intent e entender quando essa forma de integra��o � a mais indicada para aplica��es Android.

---

# O problema

Aplica��es Android frequentemente precisam compartilhar funcionalidades.

Por exemplo:

- solicitar um pagamento;
- imprimir um comprovante;
- abrir uma tela espec�fica;
- capturar informa��es do usu�rio;
- executar um servi�o externo.

Sem um mecanismo padronizado, cada aplica��o precisaria implementar sua pr�pria forma de comunica��o.

O Android Intent resolve esse problema.

---

# O que � um Intent?

Um Intent � uma mensagem enviada de uma aplica��o para outra solicitando que uma determinada a��o seja executada.

O Android identifica qual aplica��o � respons�vel por aquela a��o e realiza a comunica��o automaticamente.

Essa abordagem reduz o acoplamento entre os aplicativos.

---

# Como funciona?

```text
Aplica��o Comercial

        �

        ?

Android Intent

        �

        ?

ConnectTEF

        �

        ?

SmartPOS

        �

        ?

Pagamento
```

A aplica��o comercial apenas solicita a opera��o.

O ConnectTEF assume toda a comunica��o com o SmartPOS e retorna o resultado ao aplicativo de origem.

---

# Quando utilizar?

A integra��o via Intent � recomendada quando:

- a aplica��o � Android;
- o ConnectTEF est� instalado no mesmo dispositivo;
- deseja-se uma integra��o simples;
- as opera��es s�o pontuais;
- pretende-se utilizar mecanismos nativos do Android.

---

# Vantagens

A utiliza��o de Intents oferece diversas vantagens.

Entre elas:

- integra��o simples;
- baixo acoplamento;
- comunica��o nativa do Android;
- menor esfor�o de desenvolvimento;
- f�cil manuten��o;
- compatibilidade com SmartPOS Android.

---

# Intent x Provider

Embora ambos sejam mecanismos nativos do Android, possuem caracter�sticas diferentes.

| Android Intent | Provider Android |
|----------------|------------------|
| Comunica��o baseada em a��es | Comunica��o baseada em dados e servi�os |
| Implementa��o simples | Maior flexibilidade |
| Ideal para opera��es pontuais | Ideal para integra��es cont�nuas |
| Baixo acoplamento | Compartilhamento estruturado de informa��es |

O ConnectTEF oferece suporte �s duas abordagens.

A escolha depende da arquitetura da aplica��o.

---

# Intent x API REST

| Android Intent | API REST |
|----------------|----------|
| Comunica��o local | Comunica��o via HTTP |
| Apenas Android | Multiplataforma |
| N�o depende de servidor | Pode ser utilizada remotamente |
| Ideal para SmartPOS | Ideal para Web e Desktop |

---

# O papel do ConnectTEF

Independentemente da forma de integra��o utilizada, o ConnectTEF mant�m exatamente o mesmo fluxo operacional.

Ap�s receber a solicita��o atrav�s do Intent, a plataforma:

- interpreta a opera��o;
- comunica-se com o SmartPOS;
- acompanha a transa��o;
- devolve o resultado ao aplicativo.

Toda a complexidade permanece encapsulada na plataforma.

---

# Quando N�O utilizar?

O Android Intent normalmente n�o � recomendado quando:

- a aplica��o n�o � Android;
- ERP e SmartPOS executam em dispositivos diferentes;
- deseja-se integra��o remota;
- o sistema precisa atender aplica��es Web ou Desktop.

Nesses cen�rios, normalmente recomenda-se utilizar a API REST do ConnectTEF.

---

# Benef�cios

Ao utilizar Android Intent com o ConnectTEF:

- a integra��o permanece desacoplada;
- a comunica��o � nativa do Android;
- reduz-se o esfor�o de desenvolvimento;
- a manuten��o torna-se mais simples;
- o sistema permanece preparado para futuras evolu��es da plataforma.

---

# Resumo

O Android Intent � um mecanismo nativo utilizado para comunica��o entre aplica��es Android.

No ConnectTEF, ele permite que aplica��es comerciais solicitem opera��es de pagamento de forma simples, utilizando recursos do pr�prio sistema operacional, enquanto toda a l�gica de comunica��o com o SmartPOS permanece centralizada na plataforma.

---

# Pr�ximo cap�tulo

Agora conheceremos a **API Local**, uma das formas de integra��o disponibilizadas pelo ConnectTEF para comunica��o entre aplica��es executadas no mesmo ambiente.

<!-- NAVIGATION_FOOTER:START -->
---
### Veja tambem
- [README ConnectTEF](../README.md)
- [Índice da Seção](README.md)
- [O que e API Local](10-O-QUE-E-API-LOCAL.md)
---
**Navegacao:** [Anterior](08-O-QUE-E-PROVIDER.md) | [Inicio](../README.md) | [Proximo](10-O-QUE-E-API-LOCAL.md)
<!-- NAVIGATION_FOOTER:END -->
