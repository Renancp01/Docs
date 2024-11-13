
https://sandbox-dock.devcdt.com.br/pier/v2/api/accounts/{account-id}/debt-stage
curl --request GET \
  --url https://sandbox-dock.devcdt.com.br/pier/v2/api/accounts/{account-id}/debt-stage \
  --header 'Accept: application/json' \
  --header 'access_token: 123'
  
  200
{
  "id": 1,
  "account_id": 1,
  "dock_flag_stop": true,
  "dock_update_date": "2023-12-15T11:00:00Z",
  "issuer_stage": 1,
  "issuer_update_date": "2023-12-15T11:00:00Z",
  "curing_stage": 1,
  "curing_update_date": "2023-12-15T11:00:00Z"
}

403
{
  "message": "Forbidden"
}

404
{
  "id": "a3d6e02b-8f20-4c4e-8e40-c4aa8083d070",
  "description": "Not Found",
  "code": "404"
}

500
{
  "error": {
    "id": "c3e6e02b-8f20-4c4e-8e40-c4aa8083d070",
    "description": "Internal server error",
    "code": "500"
  }
}


===//

curl --request POST \
  --url https://sandbox-dock.devcdt.com.br/pier/v2/api/accounts/{account-id}/debt-stage \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --header 'access_token: 123' \
  --data '{
  "issuer_stage": 1
}'

200

{
  "id": 1,
  "account_id": 1,
  "dock_flag_stop": true,
  "dock_update_date": "2023-12-15T11:00:00Z",
  "issuer_stage": 1,
  "issuer_update_date": "2023-12-15T11:00:00Z",
  "curing_stage": 1,
  "curing_update_date": "2023-12-15T11:00:00Z"
}

400
{
  "error": {
    "id": "a3d6e02b-8f20-4c4e-8e40-c4aa8083d070",
    "description": "Bad request",
    "code": "400",
    "error_details": [
      {
        "attribute": "body",
        "messages": [
          "BODY_EMPTY"
        ]
      }
    ]
  }
}

403
{
  "message": "Forbidden"
}

404
{
  "id": "a3d6e02b-8f20-4c4e-8e40-c4aa8083d070",
  "description": "Not Found",
  "code": "404"
}

422
{
  "id": "a3d6e02b-8f20-4c4e-8e40-c4aa8083d070",
  "description": "Marcação do estágio já encontra-se habilitada para a conta informada",
  "code": "ACC-002"
}

500
{
  "error": {
    "id": "c3e6e02b-8f20-4c4e-8e40-c4aa8083d070",
    "description": "Internal server error",
    "code": "500"
  }
}



curl --request PATCH \
  --url https://sandbox-dock.devcdt.com.br/pier/v2/api/accounts/{account-id}/debt-stage \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --data '{
  "issuer_stage": 1
}'


200

{
  "id": 1,
  "account_id": 1,
  "dock_flag_stop": true,
  "dock_update_date": "2023-12-15T11:00:00Z",
  "issuer_stage": 1,
  "issuer_update_date": "2023-12-15T11:00:00Z",
  "curing_stage": 1,
  "curing_update_date": "2023-12-15T11:00:00Z"
}

400:
{
  "error": {
    "id": "a3d6e02b-8f20-4c4e-8e40-c4aa8083d070",
    "description": "Bad request",
    "code": "400",
    "error_details": [
      {
        "attribute": "body",
        "messages": [
          "INVALID_DATA_TYPE"
        ]
      }
    ]
  }
}

403
{
  "message": "Forbidden"
}

404

{
  "id": "a3d6e02b-8f20-4c4e-8e40-c4aa8083d070",
  "description": "Not Found",
  "code": "ACC-007"
}

422
{
  "id": "a3d6e02b-8f20-4c4e-8e40-c4aa8083d070",
  "description": "Conta informada não contém estágio emissor definido",
  "code": "ACC-015"
}

500:
{
  "error": {
    "id": "c3e6e02b-8f20-4c4e-8e40-c4aa8083d070",
    "description": "Internal server error",
    "code": "500"
  }
}




curl --request POST \
  --url https://sandbox.conductor.com.br/pier/v2/api/contas/{id}/normalizacao \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --header 'access_token: 123' \
  --header 'login: '

400
Conta status conta não encontrado
Conta não pode ser normalizada devido ao status conta
Conta estado conta não encontrado
Conta não pode ser normalizada devido ao saldo positivo
Conta parâmetro do emissor não encontrado
Conta pessoa não encontrada
Conta não pode ser normalizada devido ao documento inválido
Conta tipo de ajuste não encontrado
Conta cartão não encontrado
Limite disponibilidade não encontrado


















