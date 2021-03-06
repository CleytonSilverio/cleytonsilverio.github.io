## ResponsePersonalLoansList
<a id="schemaResponsePersonalLoansList"></a>

```json
{
  "data": {
    "brand": {
      "name": "string",
      "companies": [
        {
          "name": "string",
          "cnpjNumber": "string",
          "urlComplementaryList": "string",
          "personalLoans": [
            {
              "type": "string",
              "fees": [
                {
                  "service":{
                    "name": "string",
                    "code": "string",
                    "chargingTriggerInfo": "string",
                    "prices": [
                      {
                        "interval": "string",
                        "value": "string",
                        "currency": "string"
                      }
                    ],
                    "minimum": {
                      "value": "string",
                      "currency": "string"
                    },
                    "maximum": {
                      "value": "string",
                      "currency": "string"
                    }
                  }
                }
              ],
              "interestRate": [
                {
                  "fees": [
                    {
                      "referentialRateOrIndexer": "string",
                      "rate": "string",
                    }
                  ],
                  "applications": [
                    {
                      "interval": "string",
                      "rate": "string",
                    }
                  ],
                  "minimumRate": "string",
                  "maximumRate": "string"
                }
              ],
              "requiredWarranties": [
                "string"
              ],
              "termsConditions": "string"
            }
          ]
        }
      ]
    }
  },
  "links": {
    "self": "string",
    "first": "string",
    "prev": "string",
    "next": "string",
    "last": "string"
  },
  "meta": {
    "totalRecords": "integer",
    "totalPages": "integer"
  }
}
```

|     Nome      |  Tipo                                                  | Obrigatório  |                            Definição                  |
|:------------  |:---------------------------------                      |:-----------  |:----------------------------------------------------  |
| data          | object                                                 | Sim          |                                                       |
|   brand       | [PersonalLoanBrand](#schemaPersonalLoanBrand)          | Sim          | Organização titular das dependências                                            |
| links         | [LinksPaginated](#schemaLinksPaginated)                | Sim          |                                                       |
| meta          | [MetaPaginated](#schemaMetaPaginated)                  | Sim          |                                                       |

## PersonalLoanBrand
<a id="schemaPersonalLoanBrand"></a>

```json
{
  "name": "string",
  "companies": [
    {
      "name": "string",
      "cnpjNumber": "string",
      "urlComplementaryList": "string",
      "personalLoans": [
        {
          "type": "string",
          "fees": [
            {
              "service":{
                "name": "string",
                "code": "string",
                "chargingTriggerInfo": "string",
                "prices": [
                  {
                    "interval": "string",
                    "value": "string",
                    "currency": "string"
                  }
                ],
                "minimum": {
                  "value": "string",
                  "currency": "string"
                },
                "maximum": {
                  "value": "string",
                  "currency": "string"
                }
              }
            }
          ],
          "interestRate": [
            {
              "fees": [
                {
                  "referentialRateOrIndexer": "string",
                  "rate": "string",
                }
              ],
              "applications": [
                {
                  "interval": "string",
                  "rate": "string",
                }
              ],
              "minimumRate": "string",
              "maximumRate": "string"
            }
          ],
          "requiredWarranties": [
            "string"
          ],
          "termsConditions": "string"
        }
      ]
    }
  ]
}
```

|     Nome     |  Tipo                                                      | Obrigatório  |                            Definição                         |
|:------------ |:---------------------------------                          |:-----------  |:----------------------------------------------------         |
| name         | string                                                     | Sim          | Nome da marca proprietária da dependência (titular).  |
| companies    | [PersonalLoanCompany](#schemaPersonalLoanCompany)  | Sim          | Lista de instituições pertencentes à marca             |

## PersonalLoanCompany
<a id="schemaPersonalLoanCompany"></a>

```json
{
  "name": "string",
  "cnpjNumber": "string",
  "urlComplementaryList": "string",
  "personalLoans": [
    {
      "type": "string",
      "fees": [
        {
          "service":{
            "name": "string",
            "code": "string",
            "chargingTriggerInfo": "string",
            "prices": [
              {
                "interval": "string",
                "value": "string",
                "currency": "string"
              }
            ],
            "minimum": {
              "value": "string",
              "currency": "string"
            },
            "maximum": {
              "value": "string",
              "currency": "string"
            }
          }
        }
      ],
      "interestRate": [
        {
          "fees": [
            {
              "referentialRateOrIndexer": "string",
              "rate": "string",
            }
          ],
          "applications": [
            {
              "interval": "string",
              "rate": "string",
            }
          ],
          "minimumRate": "string",
          "maximumRate": "string"
        }
      ],
      "requiredWarranties": [
        "string"
      ],
      "termsConditions": "string"
    }
  ]
}
```

|     Nome             |  Tipo                               | Obrigatório |                            Definição                                                                                                                                                                                               |  Restrição                                                                                              |
|:------------         |:---------------------------------   |:----------- |:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------|
| name                 | string                              | Sim         | Nome da Instituição, pertencente à marca, responsável pela comercialização das modalidades de Empréstimos para Pessoas Físicas consultadas.                                                                                        |                                                                                                         | 
| cnpjNumber           | string                              | Sim         | O responsável pela comercialização das modalidades de Empréstimos para Pessoas Físicas consultadas - o CNPJ corresponde ao número de inscrição no Cadastro de Pessoa Jurídica. Deve-se ter apenas os números do CNPJ, sem máscara. |                                                                                                         |
| urlComplementaryList | [URIString](#commonFieldURIString)  | Não         | URL do link que conterá a lista complementar com os nomes e CNPJs agrupados sob o mesmo cnpjNumber. Os contidos nessa lista possuem as mesmas características para produtos e serviços.                                            | Será obrigatorimente preenchido se houver lista complementar com os nomes e CNPJs a ser disponibilizada |
| personalLoans        | [PersonalLoan](#schemaPersonalLoan) | Sim         | Empréstimos Pessoas Físicas                                                                                                                                                                                                        |                                                                                                         |

## PersonalLoan
<a id="schemaPersonalLoan"></a>

```json
 {
  "type": "string",
  "fees": [
    {
      "service":{
        "name": "string",
        "code": "string",
        "chargingTriggerInfo": "string",
        "prices": [
          {
            "interval": "string",
            "value": "string",
            "currency": "string"
          }
        ],
        "minimum": {
          "value": "string",
          "currency": "string"
        },
        "maximum": {
          "value": "string",
          "currency": "string"
        }
      }
    }
  ],
  "interestRate": [
    {
      "fees": [
        {
          "referentialRateOrIndexer": "string",
          "rate": "string",
        }
      ],
      "applications": [
        {
          "interval": "string",
          "rate": "string",
        }
      ],
      "minimumRate": "string",
      "maximumRate": "string"
    }
  ],
  "requiredWarranties": [
    "string"
  ],
  "termsConditions": "string"
}
```

|     Nome            |  Tipo                                                       | Obrigatório  |                            Definição                         |
|:------------        |:---------------------------------                           |:-----------  |:----------------------------------------------------         |
| type                | [Enum PersonalLoanType](#schemaEnumPersonalLoanType)     | Sim          | Modalidades de empréstimos ofertados para pessoas Físicas, conforme Circular <a href='https://www.bcb.gov.br/pre/normativos/busca/downloadNormativo.asp?arquivo=/Lists/Normativos/Attachments/51025/Circ_4015_v1_O.pdf' target="_blank">4015-Bacen</a>|
| fees                | [LoanFee](#schemaLoanFee)                               | Sim          | Tarifas cobradas sobre Serviços ofertados à Modalidade de Empréstimo                                                                                                                                                                                  |
| interestRate       | [LoanInterestRate](#schemaLoanInterestRate)             | Sim          | Taxas de juros remuneratórias                                                                                                                                                                                                                         |
| requiredWarranties  | [Enum RequiredWarranty](#schemaEnumRequiredWarranty)  | Sim          | Relação de garantias exigidas, segundo documento <a href='https://www.bcb.gov.br/estabilidadefinanceira/scrdoc3040' target="_blank">3040 do Bacen</a>                                                                                                 |
| termsConditions     | string                                                      | Sim          | Campo aberto para informar as condições contratuais relativas ao produto ou serviço informado. Pode ser informada a URL ([URIString](#commonFieldURIString)) referente ao endereço onde constam as condições informadas.   |

### Enum PersonalLoanType
<a id="schemaEnumPersonalLoanType"></a>

| Propriedade  | Código                        | Definição
|:------------ |:------                       |:------
| type         | ADIANTAMENTO_DEPOSITANTE    | Adiantamento a depositante
| type         | EMPRESTIMO_CREDITO_PESSOAL_CONSIGNADO  | Crédito pessoal consignado
| type         | EMPRESTIMO_CREDITO_PESSOAL_NAO_CONSIGNADO  | Crédito pessoal não consignado
| type         | EMPRESTIMO_HOME_EQUITY | Home equity
| type         | EMPRESTIMO_MICROCREDITO_PRODUTIVO_ORIENTADO | Microcrédito produtivo orientado
| type         | EMPRESTIMO_CHEQUE_ESPECIAL | Cheque especial
| type         | EMPRESTIMO_CONTA_GARANTIDA  | Conta garantida

### Enum RequiredWarranty
<a id="schemaEnumRequiredWarranty"></a>

| Propriedade  | Código                                        | Definição                                    
|:------------ |:------                                       |:------
| requiredWarranty        | CESSAO_DIREITOS_CREDITORIOS     | Cessão de direitos creditórios
| requiredWarranty        | CAUCAO                          | Caução
| requiredWarranty        | PENHOR                          | Penhor
| requiredWarranty        | ALIENACAO_FIDUCIARIA            | Alienação fiduciária
| requiredWarranty        | HIPOTECA                        | Hipoteca
| requiredWarranty        | OPERACOES_GARANTIDAS_PELO_GOVERNO    | Operações garantidas pelo governo
| requiredWarranty        | OUTRAS_GARANTIAS_NAO_FIDEJUSSORIAS  | Outras garantias não fidejussórias
| requiredWarranty        | SEGUROS_ASSEMELHADOS            | Seguros e assemelhados
| requiredWarranty        | GARANTIA_FIDEJUSSORIA           | Garantia fidejussória
| requiredWarranty        | BENS_ARRENDADOS                 | Bens arrendados
| requiredWarranty        | GARANTIAS_INTERNACIONAIS        | Garantias internacionais
| requiredWarranty        | OPERACOES_GARANTIDAS_OUTRAS_ENTIDADES
  | Operações garantidas por outras entidades
| requiredWarranty        | ACORDOS_COMPENSACAO             | Acordos de compensação
| requiredWarranty        | NAO_APLICAVEL                   | Não aplicável

## LoanFee
<a id="schemaLoanFee"></a>

```json
{
  "service":{
    "name": "string",
    "code": "string",
    "chargingTriggerInfo": "string",
    "prices": [
      {
        "interval": "string",
        "value": "string",
        "currency": "string"
      }
    ],
    "minimum": {
      "value": "string",
      "currency": "string"
    },
    "maximum": {
      "value": "string",
      "currency": "string"
    }
  }
}
```
|     Nome            |  Tipo                                           | Obrigatório  |                            Definição                         | Restrições
|:------------        |:---------------------------------               |:-----------  |:----------------------------------------------------         | :------
| name         | string                                          | Sim          | Nomes das Tarifas cobradas sobre Serviços relacionados à Modalidade informada do Empréstimo para pessoa física/jurídica.    | NA
| code         | string                                          | Sim          | Sigla de identificação do serviço relacionado à Modalidade informada de Empréstimo para pessoa física/jurídica.             | NA
| chargingTriggerInfo | string                                          | Sim          | Fatos geradores de cobrança que incidem sobre as Modalidades informada de Empréstimos para pessoa física/jurídica.        | NA
| prices               | [Price](#schemaPrice)                         | Sim          | Valor da mediana da tarifa, relativa ao serviço ofertado, informado no período.                                                       | NA
| minimum             | [MinimumPrice](#schemaMinimumPrice)           | Sim          | Valor mínimo cobrado para a tarifa de serviços sobre a base de clientes no mês de referência. | NA
| maximum             | [MaximumPrice](#schemaMaximumPrice)           | Sim          | Valor máximo cobrado para a tarifa de serviços sobre a base de clientes no mês de referência. | NA

## LoanInterestRate
<a id="schemaLoanInterestRate"></a>

```json
{
  "fees": [
    {
      "referentialRateIndexer": "string",
      "rate": "string"
    }
  ],
  "applications": [
    {
      "interval": "string",
      "rate": "string",
    }
  ],
  "minimumRate": "string",
  "maximumRate": "string"
}
```

| Nome                | Tipo                                            | Obrigatório | Definição                                                 |
|:----------------    |:------                                          |:----------- |:-------------------------------                           |
| fees            | [FeeReferentialRateIndexer](#schemaFeeReferentialRateIndexer)    | Sim            | Tipos de taxas referenciais ou indexadores, conforme Anexo 5: Taxa referencial ou Indexador (Indx), do Documento 3040 |
| applications        | [Application](#schemaApplication)                         | Sim          | Valor da mediana da taxa de remuneração relativa ao serviço ofertado.                                                       | 
| minimumRate         | string     | Sim          | Percentual mínimo cobrado (taxa efetiva) no mês de referência, para o Empréstimo contratado. A apuração pode acontecer com até 4 casas decimais. O preenchimento deve respeitar as 4 casas decimais, mesmo que venham preenchidas com zeros (representação de porcentagem p.ex: 0.1500. Este valor representa 15%. O valor 1 representa 100%) | 
| maximumRate         | string     | Sim          | Percentual máximo cobrado (taxa efetiva) no mês de referência, para o Empréstimo contratado. A apuração pode acontecer com até 4 casas decimais. O preenchimento deve respeitar as 4 casas decimais, mesmo que venham preenchidas com zeros (representação de porcentagem p.ex: 0.1500. Este valor representa 15%. O valor 1 representa 100%) | 

