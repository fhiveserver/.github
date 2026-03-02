<div align="center">

# Fhive

**Ferramentas PHP para o padrão HL7/FHIR de interoperabilidade em saúde.**

[![FHIR R4](https://img.shields.io/badge/FHIR-R4-brightgreen?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xMiAyQzYuNDggMiAyIDYuNDggMiAxMnM0LjQ4IDEwIDEwIDEwIDEwLTQuNDggMTAtMTBTMTcuNTIgMiAxMiAyem0tMSAxNXYtNEg3bDUtOXY0aDRsLTUgOXoiLz48L3N2Zz4=)](https://hl7.org/fhir/R4/)
[![PHP 8.5+](https://img.shields.io/badge/PHP-8.5%2B-777BB4?style=flat-square&logo=php&logoColor=white)](https://php.net)
[![Laravel](https://img.shields.io/badge/Laravel-12-FF2D20?style=flat-square&logo=laravel&logoColor=white)](https://laravel.com)
[![Servidor FHIR](https://img.shields.io/badge/Servidor%20FHIR-dev.fhir.app-0ea5e9?style=flat-square)](https://dev.fhir.app/fhir/R4/metadata)

</div>

---

## O que é FHIR?

**FHIR** *(Fast Healthcare Interoperability Resources)* é o padrão internacional criado pela HL7 para troca de informações de saúde entre sistemas — prontuários, laboratórios, farmácias, planos de saúde, dispositivos médicos e muito mais.

Em vez de cada hospital reinventar a roda para conversar com cada laboratório, o FHIR define uma linguagem comum: recursos como `Patient`, `Observation`, `Medication`, `DiagnosticReport` — todos via API REST, JSON ou XML.

É o padrão adotado pelo **RNDS** (Rede Nacional de Dados em Saúde) no Brasil, pelo **US Core** nos EUA, e por dezenas de países ao redor do mundo. Se você trabalha com saúde digital, cedo ou tarde vai se deparar com ele.

---

## O que fazemos aqui

A Fhive nasceu de uma pergunta simples: *por que não existe um ecossistema FHIR sólido para PHP?*

O ecossistema Java tem o HAPI. O .NET tem o Firely SDK. O Python tem o fhir.resources. E o PHP — a linguagem que roda boa parte da web — ficou de fora.

Nossa missão é mudar isso.

Estamos construindo um conjunto de ferramentas PHP para quem quer trabalhar com FHIR sem abandonar o ecossistema que já conhece e ama:

- **Um servidor FHIR completo** em Laravel/PHP, com conformidade ao padrão R4
- **Bibliotecas open-source** para quem precisa integrar FHIR em qualquer aplicação PHP
- **Ferramentas de desenvolvimento** que tornam o trabalho com FHIR mais simples e produtivo

---

## Projetos open-source

### [`flier`](https://github.com/fhiveserver/flier) — Fluent FHIR for PHP/Laravel

A maneira mais expressiva de trabalhar com FHIR em PHP. Builder fluente de recursos, busca por parâmetros e suporte a JSON Patch — tudo com a elegância que você espera do ecossistema Laravel.

```php
$patient = Flier::resource('Patient')
    ->set('name[0].family', 'Silva')
    ->set('name[0].given[0]', 'João')
    ->set('birthDate', '1990-05-15')
    ->build();
```

> Mais repositórios a caminho — estamos abrindo o código aos poucos, conforme amadurecemos cada componente.

---

## Servidor FHIR para desenvolvedores

Mantemos um servidor FHIR R4 disponível publicamente em:

**[https://dev.fhive.app/fhir/R4/metadata](https://dev.fhive.app/fhir/R4/metadata)**

Você pode usá-lo para explorar a API, testar integrações e experimentar o padrão FHIR na prática.

> **Atenção:** Este é um ambiente de desenvolvimento. O banco de dados pode ser **resetado a qualquer momento sem aviso prévio**. Não armazene dados reais ou que você não possa perder.

**Em breve:** Um servidor FHIR público e estável para testes, com dados sintéticos persistentes e documentação completa.

---

## Como contribuir

O FHIR é complexo. PHP é familiar. A combinação dos dois pode facilitar a vida de muita gente no setor de saúde — e precisamos de ajuda para chegar lá.

Se você é desenvolvedor PHP e tem curiosidade sobre saúde digital, há espaço para você aqui:

- **Reporte bugs** e comportamentos inesperados nas issues
- **Sugira melhorias** — uma API melhor, mais cobertura da spec, casos de uso reais
- **Abra PRs** — desde correções simples até novas features
- **Compartilhe** — mostre o projeto para quem trabalha com saúde e tecnologia

Não precisa ser especialista em FHIR para contribuir. Se você manja de PHP, Laravel, testes ou documentação, já tem muito a oferecer.

Comece por [`flier`](https://github.com/fhiveserver/flier) — é o repositório mais maduro e o melhor ponto de entrada.

---

## Sobre o projeto

A Fhive é um projeto independente, construído por desenvolvedores que acreditam que o acesso a ferramentas de qualidade não deveria ser um privilégio de quem usa Java ou .NET.

Saúde é um direito. Interoperabilidade também deveria ser.

---

<div align="center">

**[GitHub](https://github.com/fhiveserver)** · **[Servidor FHIR](https://dev.fhir.app)** · **[HL7/FHIR R4](https://hl7.org/fhir/R4/)**

*Feito com PHP, Laravel e muito carinho pelo ecossistema de saúde digital.*

</div>
