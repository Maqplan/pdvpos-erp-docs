<!-- NAVIGATION:START -->
---
[README ConnectTEF](../README.md) | [Índice da Seção](README.md) | [Anterior](09-O-QUE-E-INTENT.md) | [Próximo](11-O-QUE-E-API-REST.md)
---
> **Caminho:** [Início](../README.md) / Conceitos / O que e API Local
<!-- NAVIGATION:END -->

# O que � a API Local?

A API Local � uma interface de comunica��o disponibilizada pelo ConnectTEF que permite que aplica��es executadas no mesmo computador ou na mesma rede local se comuniquem com a plataforma utilizando requisi��es HTTP.

Ela foi projetada para simplificar a integra��o de sistemas Desktop, aplica��es legadas e ambientes locais, oferecendo uma interface moderna sem exigir comunica��o direta com os SmartPOS.

---

# Objetivo

Compreender o conceito da API Local, seu funcionamento e os cen�rios em que ela representa a melhor alternativa de integra��o com o ConnectTEF.

---

# O problema

Muitos sistemas comerciais ainda executam localmente.

� comum encontrar:

- ERPs Desktop
- PDVs Windows
- Aplica��es Delphi
- Sistemas C#
- Aplica��es Java
- Sistemas legados

Esses sistemas normalmente precisam conversar com dispositivos presentes na mesma loja.

Criar integra��es espec�ficas para cada fabricante aumenta significativamente o custo de desenvolvimento.

A API Local foi criada para resolver esse problema.

---

# Como funciona?

O ConnectTEF disponibiliza um servi�o HTTP executando localmente.

O ERP envia requisi��es para esse servi�o.

A plataforma interpreta os comandos e realiza toda a comunica��o com o SmartPOS.

```text
ERP / PDV

      �

HTTP Local

      �

      ?

API Local ConnectTEF

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

Para o ERP, a integra��o acontece atrav�s de uma API HTTP convencional.

Toda a complexidade permanece encapsulada na plataforma.

---

# Por que utilizar uma API Local?

A API Local oferece uma forma simples de modernizar sistemas existentes.

Em vez de implementar protocolos espec�ficos para cada equipamento, o ERP passa a utilizar uma interface HTTP padronizada.

Essa abordagem facilita o desenvolvimento, reduz o acoplamento e simplifica futuras evolu��es da plataforma.

---

# Quando utilizar?

A API Local � recomendada quando:

- o sistema � Desktop;
- o ERP e o ConnectTEF executam no mesmo computador;
- os equipamentos est�o na mesma rede local;
- deseja-se comunica��o HTTP sem depender de servi�os externos;
- busca-se uma integra��o simples e padronizada.

---

# API Local x API REST

Embora ambas utilizem HTTP, elas atendem cen�rios diferentes.

| API Local | API REST |
|------------|----------|
| Comunica��o local | Comunica��o remota |
| Executa no ambiente do cliente | Executa atrav�s da infraestrutura da plataforma |
| Ideal para sistemas Desktop | Ideal para aplica��es Web e SaaS |
| Baixa lat�ncia | Maior flexibilidade |
| N�o depende de acesso externo | Pode ser acessada pela Internet |

A escolha depende da arquitetura da aplica��o.

---

# API Local x Provider Android

| API Local | Provider Android |
|------------|------------------|
| HTTP | Comunica��o nativa Android |
| Desktop e aplica��es locais | Aplica��es Android |
| Multiplataforma | Exclusivo para Android |
| Integra��o via rede local | Integra��o dentro do dispositivo |

---

# Benef�cios

A utiliza��o da API Local proporciona:

- integra��o simples atrav�s de HTTP;
- menor acoplamento entre ERP e SmartPOS;
- baixo impacto em sistemas legados;
- arquitetura padronizada;
- evolu��o transparente da plataforma;
- menor custo de manuten��o.

---

# O papel do ConnectTEF

A API Local � apenas uma das portas de entrada da plataforma.

Independentemente da tecnologia utilizada pelo ERP, o ConnectTEF continua respons�vel por:

- interpretar as requisi��es;
- comunicar-se com os SmartPOS;
- controlar o fluxo das transa��es;
- padronizar os retornos;
- disponibilizar novos recursos da plataforma.

Isso permite que diferentes tecnologias utilizem exatamente a mesma infraestrutura.

---

# Quando N�O utilizar?

A API Local normalmente n�o � indicada quando:

- a aplica��o est� hospedada na nuvem;
- o sistema � um SaaS acessado remotamente;
- o ERP n�o possui acesso ao ambiente local;
- a comunica��o precisa ocorrer atrav�s da Internet.

Nesses cen�rios, recomenda-se utilizar a **API REST** do ConnectTEF.

---

# Resumo

A API Local � uma interface HTTP executada localmente que permite integrar aplica��es Desktop e sistemas locais ao ConnectTEF utilizando uma arquitetura moderna, simples e padronizada.

Ela reduz a complexidade da integra��o e permite que o ERP utilize uma �nica interface para acessar todo o ecossistema de pagamentos.

---

# Pr�ximo cap�tulo

Agora conheceremos a **API REST**, a principal interface de integra��o do ConnectTEF para aplica��es Web, SaaS e sistemas distribu�dos.

<!-- NAVIGATION_FOOTER:START -->
---
### Veja também
- [README ConnectTEF](../README.md)
- [Índice da Seção](README.md)
- [O que e API Rest](11-O-QUE-E-API-REST.md)
---
**Navegação:** [Anterior](09-O-QUE-E-INTENT.md) | [Início](../README.md) | [Próximo](11-O-QUE-E-API-REST.md)
<!-- NAVIGATION_FOOTER:END -->
