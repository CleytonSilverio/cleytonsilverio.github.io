## ResponsePersonalCreditCards
<a id="schemaResponsePersonalCreditCards"></a>

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
          "personalCreditCards": [
            {
              "name": "string",
              "identification": {
                "product": {
                  "type": "string",
                  "additionalInfo": "string"
                },
                "creditCard": {
                  "network": "string",
                  "additionalInfo": "string"
                }
              },
              "rewardsProgram": {
                "hasRewardProgram": "string",
                "rewardProgramInfo": "string"
              },
              "fees": [
                {
                  "service": {
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
                    },
                    "customers": [
                      {
                        "frequency": "string",
                        "rate": "string"
                      }
                    ]
                  }
                }
              ],
              "interest": {
                "feeRate": {
                  "prices": [
                    [
                      {
                        "interval": "string",
                        "rate": "string"
                      }
                    ]
                  ],
                  "minimumRate": "string",
                  "maximumRate": "string",
                  "fees": [
                    {
                      "referentialRateIndexer": "string",
                      "rate": "string"
                    }
                  ],
                  "customers": [
                    {
                      "frequency": "1_FAIXA_CLIENTE",
                      "rate": "0.1500"
                    }
                  ]
                },
                "instalmentRate": {
                  "prices": [
                    [
                      {
                        "interval": "string",
                        "rate": "string"
                      }
                    ]
                  ],
                  "minimumRate": "string",
                  "maximumRate": "string",
                  "fees": [
                    {
                      "referentialRateIndexer": "string",
                      "rate": "string"
                    }
                  ],
                  "customers": [
                    {
                      "frequency": "1_FAIXA_CLIENTE",
                      "rate": "0.1500"
                    }
                  ]
                },
                "interestRates": [{
                  "code": "string",
                  "additionalInfo": "string",
                  "prices": [
                    [
                      {
                        "interval": "string",
                        "rate": "string"
                      }
                    ]
                  ],
                  "minimumRate": "string",
                  "maximumRate": "string",
                  "fees": [
                    {
                      "referentialRateIndexer": "string",
                      "rate": "string"
                    }
                  ],
                  "customers": [
                    {
                      "frequency": "1_FAIXA_CLIENTE",
                      "rate": "0.1500"
                    }
                  ]
                }]
              },
              "termsConditions": {
                "minimumFeeRate": "string",
                "additionalInfo": "string",
                "elegibilityCriteriaInfo": "string",
                "closingProcessInfo": "string"
              }
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

|     Nome          |  Tipo                                                       | Obrigatório  |                            Definição                                                                      |
|:------------------|:----------------------------------------------------------- |:------------ |:--------------------------------------------------------------------------------------------------------- | 
| data              | object                                                      | Sim          |                                                                                                           |
| » brand           | [PersonalCreditCardBrand](#schemaPersonalCreditCardBrand)   | Sim          | Dados da Marca selecionada que fornecem produtos e serviços de cartões de crédito para pessoa jurídica    |
| links             | [LinksPaginated](#schemaLinksPaginated)                     | Sim          |                                                                                                           |
| meta              | [MetaPaginated](#schemaMetaPaginated)                       | Sim          |                                                                                                           |

## PersonalCreditCardBrand
<a id="schemaPersonalCreditCardBrand"></a>

```json
{
  "name": "string",
  "companies": [
    {
      "name": "string",
      "cnpjNumber": "string",
      "urlComplementaryList": "string",
      "personalCreditCards": [
        {
          "name": "string",
          "identification": {
            "product": {
              "type": "string",
              "additionalInfo": "string"
            },
            "creditCard": {
              "network": "string",
              "additionalInfo": "string"
            }
          },
          "rewardsProgram": {
            "hasRewardProgram": "string",
            "rewardProgramInfo": "string"
          },
          "fees": [
            {
              "service": {
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
                },
                "customers": [
                  {
                    "frequency": "string",
                    "rate": "string"
                  }
                ]
              }
            }
          ],
          "interest": {
            "feeRate": {
              "prices": [
                [
                  {
                    "interval": "string",
                    "rate": "string"
                  }
                ]
              ],
              "minimumRate": "string",
              "maximumRate": "string",
              "fees": [
                {
                  "referentialRateIndexer": "string",
                  "rate": "string"
                }
              ],
              "customers": [
                {
                  "frequency": "1_FAIXA_CLIENTE",
                  "rate": "0.1500"
                }
              ]
            },
            "instalmentRate": {
              "prices": [
                [
                  {
                    "interval": "string",
                    "rate": "string"
                  }
                ]
              ],
              "minimumRate": "string",
              "maximumRate": "string",
              "fees": [
                {
                  "referentialRateIndexer": "string",
                  "rate": "string"
                }
              ],
              "customers": [
                {
                  "frequency": "1_FAIXA_CLIENTE",
                  "rate": "0.1500"
                }
              ]
            },
            "interestRates": [{
              "code": "string",
              "additionalInfo": "string",
              "prices": [
                [
                  {
                    "interval": "string",
                    "rate": "string"
                  }
                ]
              ],
              "minimumRate": "string",
              "maximumRate": "string",
              "fees": [
                {
                  "referentialRateIndexer": "string",
                  "rate": "string"
                }
              ],
              "customers": [
                {
                  "frequency": "1_FAIXA_CLIENTE",
                  "rate": "0.1500"
                }
              ]
            }]
          },
          "termsConditions": {
            "minimumFeeRate": "string",
            "additionalInfo": "string",
            "elegibilityCriteriaInfo": "string",
            "closingProcessInfo": "string"
          }
        }
      ]
    }
  ]
}
```

|     Nome     |  Tipo                                                               | Obrigatório  |                            Definição                                                                                                                                                                                                      |
|:-------------|:--------------------------------------------------------------------|:-----------  |:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name         | string                                                              | Sim          | Nome da Marca reportada pelo participante do Open Banking. O conceito a que se refere a 'marca' é em essência uma promessa da empresa em fornecer uma série específica de atributos, benefícios e serviços uniformes aos clientes         |
| companies    | [[PersonalCreditCardCompanies](#schemaPersonalCreditCardCompanies)] | Sim          | Lista de instituições pertencentes a marca                                                                                                                                                                                                |

## PersonalCreditCardCompanies 
<a id="schemaPersonalCreditCardCompanies"></a>

```json
{
  "name": "string",
  "cnpjNumber": "string",
  "urlComplementaryList": "string",
  "personalCreditCards": [
    {
      "name": "string",
      "identification": {
        "product": {
          "type": "string",
          "additionalInfo": "string"
        },
        "creditCard": {
          "network": "string",
          "additionalInfo": "string"
        }
      },
      "rewardsProgram": {
        "hasRewardProgram": "string",
        "rewardProgramInfo": "string"
      },
      "fees": [
        {
          "service": {
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
            },
            "customers": [
              {
                "frequency": "string",
                "rate": "string"
              }
            ]
          }
        }
      ],
      "interest": {
        "feeRate": {
          "prices": [
            [
              {
                "interval": "string",
                "rate": "string"
              }
            ]
          ],
          "minimumRate": "string",
          "maximumRate": "string",
          "fees": [
            {
              "referentialRateIndexer": "string",
              "rate": "string"
            }
          ],
          "customers": [
            {
              "frequency": "1_FAIXA_CLIENTE",
              "rate": "0.1500"
            }
          ]
        },
        "instalmentRate": {
          "prices": [
            [
              {
                "interval": "string",
                "rate": "string"
              }
            ]
          ],
          "minimumRate": "string",
          "maximumRate": "string",
          "fees": [
            {
              "referentialRateIndexer": "string",
              "rate": "string"
            }
          ],
          "customers": [
            {
              "frequency": "1_FAIXA_CLIENTE",
              "rate": "0.1500"
            }
          ]
        },
        "interestRates": [{
          "code": "string",
          "additionalInfo": "string",
          "prices": [
            [
              {
                "interval": "string",
                "rate": "string"
              }
            ]
          ],
          "minimumRate": "string",
          "maximumRate": "string",
          "fees": [
            {
              "referentialRateIndexer": "string",
              "rate": "string"
            }
          ],
          "customers": [
            {
              "frequency": "1_FAIXA_CLIENTE",
              "rate": "0.1500"
            }
          ]
        }]
      },
      "termsConditions": {
        "minimumFeeRate": "string",
        "additionalInfo": "string",
        "elegibilityCriteriaInfo": "string",
        "closingProcessInfo": "string"
      }
    }
  ]
}
```

|     Nome             |  Tipo                                                | Obrigatório    |    Definição                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:---------------------|:-----------------------------------------------------|:-------------- |:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                 | string                                               | Sim            | Nome da Instituição, pertencente à marca, responsável pela modalidade de Conta de Pagamento Pós Paga (Cartão)  para Pessoa Natural. p.ex.'Empresa da Organização A'                                                                                                                                                                                                                                                                                                          |
| cnpjNumber           | string                                               | Sim            | Número completo do CNPJ da instituição. O CNPJ corresponde ao número de inscrição no Cadastro de Pessoa Jurídica. Deve-se ter apenas os números do CNPJ, sem máscara                                                                                                                                                                                                                                                                                                         |
| urlComplementaryList | string                                               | Não            | URL de link para lista complementar com os nomes e CNPJs agrupados para o caso instituições ofertantes de produtos e serviços com as mesmas características. URL do link que conterá a lista complementar com os nomes e CNPJs agrupados sob o mesmo cnpjNumber.Endereço eletrônico de acesso ao canal. URLs são limitadas a 2048 caracteres mas, para o contexto do Sistema Financeiro aberto, será adotado a metade deste tamanho. Ex. 'https://example.com/mobile-banking'|
| personalCreditCards  | [[PersonalCreditCard](#schemaPersonalCreditCard)]    | Sim            | Lista  de cartões de crédito                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

## PersonalCreditCard
<a id="schemaPersonalCreditCard"></a>

```json
{
  "name": "string",
  "identification": {
    "product": {
      "type": "string",
      "additionalInfo": "string"
    },
    "creditCard": {
      "network": "string",
      "additionalInfo": "string"
    }
  },
  "rewardsProgram": {
    "hasRewardProgram": "string",
    "rewardProgramInfo": "string"
  },
  "fees": [
    {
      "service": {
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
        },
        "customers": [
          {
            "frequency": "string",
            "rate": "string"
          }
        ]
      }
    }
  ],
  "interest": {
    "feeRate": {
      "prices": [
        [
          {
            "interval": "string",
            "rate": "string"
          }
        ]
      ],
      "minimumRate": "string",
      "maximumRate": "string",
      "fees": [
        {
          "referentialRateIndexer": "string",
          "rate": "string"
        }
      ],
      "customers": [
        {
          "frequency": "1_FAIXA_CLIENTE",
          "rate": "0.1500"
        }
      ]
    },
    "instalmentRate": {
      "prices": [
        [
          {
            "interval": "string",
            "rate": "string"
          }
        ]
      ],
      "minimumRate": "string",
      "maximumRate": "string",
      "fees": [
        {
          "referentialRateIndexer": "string",
          "rate": "string"
        }
      ],
      "customers": [
        {
          "frequency": "1_FAIXA_CLIENTE",
          "rate": "0.1500"
        }
      ]
    },
    "interestRates": [{
      "code": "string",
      "additionalInfo": "string",
      "prices": [
        [
          {
            "interval": "string",
            "rate": "string"
          }
        ]
      ],
      "minimumRate": "string",
      "maximumRate": "string",
      "fees": [
        {
          "referentialRateIndexer": "string",
          "rate": "string"
        }
      ],
      "customers": [
        {
          "frequency": "1_FAIXA_CLIENTE",
          "rate": "0.1500"
        }
      ]
    }]
  },
  "termsConditions": {
    "minimumFeeRate": "string",
    "additionalInfo": "string",
    "elegibilityCriteriaInfo": "string",
    "closingProcessInfo": "string"
  }
}
```

|     Nome              |  Tipo                                                                       | Obrigatório |                            Definição                                                                                                                                                                                                                                                        |
|:----------------------|:----------------------------------------------------------------------------|:------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                  | string                                                                      | Sim         | Denominação/Identificação do nome da conta de pagamento pós-paga (cartão).Conforme CIRCULAR Nº 3.680,BCB, 2013: 'conta de pagamento pós-paga: destinada à execução de transações de pagamento que independem do aporte prévio de recursos' p.ex. 'Cartão Universitário Bem-Vindo'           |
| identification        | [PersonalCreditCardIdentification](#schemaPersonalCreditCardIdentification) | Sim         | Informações de identificação do cartão de crédito                                                                                                                                                                                                                                           |
| rewardsProgram        | [PersonalCreditCardRewardProgram](#schemaPersonalCreditCardRewardProgram)   | Sim         | Informações sobre programas de recompensa presentes no cartão de crédito                                                                                                                                                                                                                    |
| fees                  | [PersonalCreditCardFee](#schemaPersonalCreditCardFee)                       | Sim         | Informações sobre tarifas cobradas sobre o produto e serviços                                                                                                                                                                                                                               |
| interest              | [CreditCardInterest](#schemaCreditCardInterest)                             | Sim         | Informações sobre taxas de juros                                                                                                                                                                                                                                                            |
| termsConditions       | [CreditCardTermsConditions](#schemaCreditCardTermsConditions)               | Sim         | Informações sobre termos e condições para aquisição e cancelamento                                                                                                                                                                                                                          |


## PersonalCreditCardIdentification
<a id="schemaPersonalCreditCardIdentification"></a>

```json
{
  "product":{
    "type": "string",
    "additionalInfo": "string"
  },
  "creditCard":{
    "network": "string",
    "additionalInfo": "string"
  }
}
```

|     Nome          |  Tipo        | Obrigatório    |    Definição                   |
|:----------------- |:------------ |:-------------- |:------------------------------ |
| product           | [PersonalCreditCardIdentificationProduct](#schemaPersonalCreditCardIdentificationProduct)       | Sim            | Categoria atribuída a um cartão de pagamento, sob uma certa denominação, que lhe agrega um conjunto de vantagens, diferenciando-o de acordo com o perfil do portador  |
| creditCard        | [PersonalCreditCardIdentificationCreditCard](#schemaPersonalCreditCardIdentificationCreditCard) | Sim            | Categoria de Bandeiras de Cartões de Crédito |

## PersonalCreditCardIdentificationProduct
<a id="schemaPersonalCreditCardIdentificationProduct"></a>

```json
{
  "type": "string",
  "additionalInfo": "string"
}
```

|     Nome          |  Tipo                                                                          | Obrigatório    |    Definição                                                                                                                                                                                                                                                                                                                       |
|:----------------- |:------------------------------------------------------------------------------ |:-------------- |:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| type              | [Enum PersonalCreditCardProductType](#schemaEnumPersonalCreditCardProductType) | Sim            | Categoria atribuída a um cartão de pagamento, sob uma certa denominação, que lhe agrega um conjunto de vantagens, diferenciando-o de acordo com o perfil do portador. Essa categoria é definida pelo BACEN e está contida no documento de nome 'Elaboração e Remessa de Informações Relativas aos Cartões de Pagamento  Emissores' |
| additionalInfo    | string                                                                         | Não            | Informações complementares se tipo de Cartão 'OUTROS'                                                                                                                                                                                                                                                                              |

### Enum PersonalCreditCardProductType
<a id="schemaEnumPersonalCreditCardProductType"></a>

| Propriedade         | Código                     | Definição                  |
|:------------------- |:-------------------------- |:-------------------------- |
| productType         | CLASSIC_NACIONAL           | Classic Nacional           |
| productType         | CLASSIC_INTERNACIONAL      | Classic Internacional      |
| productType         | GOLD                       | Gold                       |
| productType         | PLATINUM                   | Platinum                   |
| productType         | INFINITE                   | Infinite                   |
| productType         | ELECTRON                   | Electron                   |
| productType         | STANDARD_NACIONAL          | Standard Nacional          |
| productType         | STANDARD_INTERNACIONAL     | Standard Internacional     |
| productType         | ELETRONIC                  | Classic Nacional           |
| productType         | BLACK                      | Classic Internacional      |
| productType         | REDESHOP                   | Gold                       |
| productType         | MAESTRO_MASTERCARD_MAESTRO | Maestro Mastercard maestro |
| productType         | GREEN                      | green                      |
| productType         | BLUE                       | blue                       |
| productType         | BLUEBOX                    | blue box                   |
| productType         | PROFISSIONAL_LIBERAL       | profissional liberal       |
| productType         | CHEQUE_ELETRONICO          | cheque eletronico          |
| productType         | CORPORATIVO                | corporativo                |
| productType         | EMPRESARIAL                | Empresarial                |
| productType         | COMPRAS                    | compras                    |
| productType         | OUTROS                     | outros                     |

## PersonalCreditCardIdentificationCreditCard
<a id="schemaPersonalCreditCardIdentificationCreditCard"></a>

```json
{
  "network": "string",
  "additionalInfo": "string"
}
```

|     Nome          |  Tipo                                                                      | Obrigatório    |    Definição                                                                                                                                                                                                                                                                                                                              |
|:----------------- |:-------------------------------------------------------------------------- |:-------------- |:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------  |
| network           | [Enum PersonalCreditCardBrandCode](#schemaEnumPersonalCreditCardBrandCode) | Sim            | Categoria de Bandeiras de Cartões. Bandeira é a detentora de todos os direitos e deveres da utilização da marca estampada no cartão, inclusive as bandeiras pertencentes aos emissores. Essas bandeiras estão definidas em documento do BACEN de nome 'Elaboração e Remessa de Informações Relativas aos Cartões de Pagamento  Emissores' |
| additionalInfo    | string                                                                     | Sim            | Texto livre para especificar categoria de bandeira marcada como 'Outras'                                                                                                                                                                                                                                                                  |

### Enum PersonalCreditCardBrandCode
<a id="schemaEnumPersonalCreditCardBrandCode"></a>

| Propriedade       | Código            | Definição           |
|:------------------|:------------------|:------------------- |
| creditCardNetwork | VISA              | Visa                |
| creditCardNetwork | MASTERCARD        | MasterCard          |
| creditCardNetwork | AMERICAN_EXPRESS  | American Express    |
| creditCardNetwork | DINERS_CLUB       | Diners Club         |
| creditCardNetwork | HIPERCARD         | Hipercard           |
| creditCardNetwork | BANDEIRA_PROPRIA  | Bandeira própria    |
| creditCardNetwork | CHEQUE_ELETRONICO | Cheque Eletrônico   |
| creditCardNetwork | ELO               | Elo                 |
| creditCardNetwork | OUTRAS            | Outras              |

## PersonalCreditCardRewardProgram
<a id="schemaPersonalCreditCardRewardProgram"></a>

```json
{
  "hasRewardProgram": "boolean",
  "rewardProgramInfo": "string"
}
```

|     Nome            |  Tipo           | Obrigatório     |    Definição                                                                                                                                                  |
|:--------------------|:--------------- |:--------------  |:------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| hasRewardProgram    | boolean         | Sim             | Indicador da existência de programa de fidelidade/recompensa associado à conta                                                                                |
| rewardProgramInfo   | string          | Não             | Informações de termos e condições do programa de fidelidade/recompensa. Pode ser informada a URL referente ao endereço onde constam as condições informadas   |

## PersonalCreditCardFee
<a id="schemaPersonalCreditCardFee"></a>

```json
{
  "service": {
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
      },
      "customers": [
        {
          "frequency": "string",
          "rate": "string"
        }
      ]
  }
}
```

|     Nome   |  Tipo                                                               | Obrigatório     |    Definição                                                                               |
|:-----------|:--------------------------------------------------------------------|:----------------|:------------------------------------------------------------------------------------------ |
| service    | [[PersonalCreditCardService](#schemaPersonalCreditCardService)]     | Sim             | Lista das Tarifas cobradas sobre Serviço relacionadas a Modalidade de Pagamento Pós-Pagas  |

## PersonalCreditCardService
<a id="schemaPersonalCreditCardService"></a>

```json
{
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
  },
  "customers": [
    {
      "frequency": "string",
      "rate": "string"
    }
  ]
}
```

|     Nome            |  Tipo                                                                                   | Obrigatório     |    Definição                                                                                                                                                                                                                                                       |
|:------------------- |:---------------------------------------------------------------------------------------|:-----------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| name                | [Enum PersonalCreditCardFeesServiceName](#schemaEnumPersonalCreditCardFeesServiceName) | Sim              | Lista de denominação de Serviços relacionados à Modalidade de Contas de Pagamento Pós-Pagas, para pessoa natural (Vide Enum)                                                                                                                                       |
| code                | [Enum PersonalCreditCardFeesServiceCode](#schemaEnumPersonalCreditCardFeesServiceCode) | Sim              | Sigla de identificação do Serviço relacionado à Modalidade de Contas de Pagamento Pós-Pagas para pessoa natural informada. (Vide Enum)                                                                                                                             |
| chargingTriggerInfo | string                                                                                 | Sim              | Fatos geradores de cobrança que incidem sobre as Modalidades de  Contas de Pagamento Pós-Pagas informada, para pessoa natural. Conforme serviços prioritários previstos na resolução 3919.                                                                         |
| prices              | [[Price](#schemaPrice)]                                                                | Sim              | Informações sobre a tarifa cobrada, relativa ao serviço relacionado à Modalidade informada de Contas de Pagamento Pós-Pagas para pessoa jurídica                                                                                                                   |
| minimum             | [[MinimumPrice](#schemaMinimumPrice)]                                                  | Sim              | Percentual mínimo cobrado (taxa efetiva) no mês de referência, pela utilização do crédito rotativo(A apuração deve pode ser feita com até 4 casas decimais. A representação de porcentagem p.ex: do 0.1500 representa 15%. Desta forma, o valor 1 representa 100%) |
| maximum             | [[MaximumPrice](#schemaMaximumPrice)]                                                  | Sim              | Percentual máximo cobrado (taxa efetiva) no mês de referência, pela utilização do crédito rotativo(A apuração deve pode ser feita com até 4 casas decimais. A representação de porcentagem p.ex: do 0.1500 representa 15%. Desta forma, o valor 1 representa 100%) |
| customers           | [[Customer](#schemaCustomer)]                                                          | Sim              | Lista percentual de clientes por faixa de preço                                                                                                                                                                                                                    |

### Enum PersonalCreditCardFeesServiceName
<a id="schemaEnumPersonalCreditCardFeesServiceName"></a>

| Propriedade                 | Código                                                  |
|:----------------------------|:--------------------------------------------------------|
| name                        | ANUIDADE_CARTAO_BASICO_NACIONAL                         |
| name                        | ANUIDADE_CARTAO_BASICO_INTERNACIONAL                    |
| name                        | UTILIZACAO_CANAIS_ATENDIMENTO_RETIRADA_ESPECIE_BRASIL   |
| name                        | UTILIZACAO_CANAIS_ATENDIMENTO_RETIRADA_ESPECIE_EXTERIOR |
| name                        | AVALIACAO_EMERGENCIAL_CREDITO                           |
| name                        | FORNECIMENTO_SEGUNDA_VIA_FUNCAO_CREDITO                 |
| name                        | PAGAMENTO_CONTAS_UTILIZANDO_FUNCAO_CREDITO              |
| name                        | SMS                                                     |

### Enum PersonalCreditCardFeesServiceCode
<a id="schemaEnumPersonalCreditCardFeesServiceCode"></a>

| Propriedade                 | Código                        |
|:----------------------------|:------------------------------|
| code                        | ANUIDADE_NACIONAL             |
| code                        | ANUIDADE_INTERNACIONAL        |
| code                        | SAQUE_CARTAO_BRASIL           |
| code                        | SAQUE_CARTAO_EXTERIOR         |
| code                        | AVALIACAO_EMERGENCIAL_CREDITO |
| code                        | EMISSAO_SEGUNDA_VIA           |
| code                        | TARIFA_PAGAMENTO_CONTAS       |
| code                        | SMS                           |
