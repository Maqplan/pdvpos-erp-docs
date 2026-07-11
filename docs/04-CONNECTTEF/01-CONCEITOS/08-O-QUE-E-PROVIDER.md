<!-- NAVIGATION:START -->
---
[README ConnectTEF](../README.md) | [Índice da Seção](README.md) | [Anterior](07-O-QUE-E-SITEF.md) | [Proximo](09-O-QUE-E-INTENT.md)
---
> **Caminho:** [Inicio](../README.md) / Conceitos / O que e Provider
<!-- NAVIGATION:END -->

# O que � o Provider Android?

O Provider Android � um mecanismo de comunica��o entre aplica��es que permite compartilhar dados e funcionalidades de forma padronizada dentro do sistema operacional Android.

No ConnectTEF, ele � utilizado como uma das formas de integra��o entre aplica��es Android e a plataforma, permitindo que o sistema solicite opera��es de pagamento utilizando recursos nativos do pr�prio Android.

---

# Objetivo

Apresentar o conceito de Provider Android e explicar como ele � utilizado pelo ConnectTEF para integrar aplica��es Android aos SmartPOS.

---

# O problema

Aplica��es Android podem se comunicar de diversas maneiras.

Entre elas:

- APIs REST
- Intents
- Services
- Sockets
- Content Providers

Cada abordagem possui vantagens dependendo da arquitetura da aplica��o.

Quando a integra��o acontece entre aplica��es executando no mesmo dispositivo Android, normalmente � desej�vel utilizar mecanismos nativos do sistema operacional.

� nesse cen�rio que o Provider se torna uma excelente alternativa.

---

# O que � um Provider?

Um Provider (Content Provider) � um componente do Android respons�vel por disponibilizar informa��es ou servi�os para outras aplica��es.

Ele funciona como uma interface padronizada para troca de informa��es entre aplicativos.

No contexto do ConnectTEF, essa interface � utilizada para solicitar opera��es de pagamento sem necessidade de comunica��o via rede.

---

# Como funciona?

```text
Aplica��o Android

        �

        ?

Provider Android

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

Toda a comunica��o acontece localmente dentro do dispositivo.

---

# Quando utilizar?

O Provider � recomendado quando:

- a aplica��o � Android;
- o ConnectTEF est� instalado no mesmo SmartPOS;
- deseja-se utilizar comunica��o nativa;
- busca-se menor lat�ncia;
- n�o h� necessidade de chamadas REST.

---

# Vantagens

A integra��o via Provider oferece diversos benef�cios.

Entre eles:

- comunica��o local;
- menor lat�ncia;
- integra��o nativa com Android;
- menor depend�ncia da rede;
- arquitetura desacoplada;
- melhor experi�ncia para o usu�rio.

---

# Provider x API REST

| Provider Android | API REST |
|------------------|----------|
| Comunica��o local | Comunica��o via HTTP |
| Android | Multiplataforma |
| Menor lat�ncia | Maior flexibilidade |
| N�o depende de servidor local | Pode acessar servi�os remotos |
| Ideal para SmartPOS Android | Ideal para Web, Desktop e integra��es externas |

As duas abordagens s�o suportadas pelo ConnectTEF.

A escolha depende da arquitetura da aplica��o.

---

# Provider x Intent

Embora ambos sejam mecanismos nativos do Android, eles possuem objetivos diferentes.

| Provider | Intent |
|----------|--------|
| Compartilha dados e servi�os | Solicita execu��o de a��es |
| Comunica��o estruturada | Comunica��o orientada a eventos |
| Ideal para integra��o cont�nua | Ideal para chamadas pontuais |
| Maior controle sobre a troca de informa��es | Implementa��o geralmente mais simples |

O ConnectTEF oferece suporte �s duas modalidades.

---

# O papel do ConnectTEF

O ConnectTEF abstrai toda a complexidade da comunica��o com o SmartPOS.

Independentemente de a aplica��o utilizar Provider, Intent ou API REST, o fluxo operacional da plataforma permanece o mesmo.

Isso permite que diferentes arquiteturas utilizem o ConnectTEF sem alterar a l�gica de neg�cio do sistema.

---

# Quando N�O utilizar

O Provider normalmente n�o � recomendado quando:

- a aplica��o � Web;
- o sistema � Desktop;
- a integra��o ocorre entre servidores;
- deseja-se acessar a plataforma remotamente.

Nesses cen�rios, normalmente recomenda-se utilizar a API REST do ConnectTEF.

---

# Resumo

O Provider Android � um mecanismo nativo do Android utilizado pelo ConnectTEF para integrar aplica��es executadas no mesmo dispositivo.

Essa abordagem oferece comunica��o local, menor lat�ncia e uma integra��o transparente com o ecossistema da plataforma, sendo especialmente indicada para aplica��es Android executadas em SmartPOS.

---

# Pr�ximo cap�tulo

Agora conheceremos o **Android Intent**, outro mecanismo de comunica��o suportado pelo ConnectTEF para integra��o entre aplica��es Android.

<!-- NAVIGATION_FOOTER:START -->
---
### Veja tambem
- [README ConnectTEF](../README.md)
- [Índice da Seção](README.md)
- [O que e Intent](09-O-QUE-E-INTENT.md)
---
**Navegacao:** [Anterior](07-O-QUE-E-SITEF.md) | [Inicio](../README.md) | [Proximo](09-O-QUE-E-INTENT.md)
<!-- NAVIGATION_FOOTER:END -->
