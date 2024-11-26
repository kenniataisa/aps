```mermaid

    usecaseDiagram

    actor Cliente as "Cliente"
    actor SistemaBancario as "Sistema Bancário"

    Cliente --> (Inserir Cartão)
    Cliente --> (Digitar Senha)
    Cliente --> (Escolher Depósito)
    Cliente --> (Informar Quantia)
    Cliente --> (Confirmar Depósito)
    Cliente --> (Pegar Comprovante)

    SistemaBancario --> (Verificar Cartão e Senha)
    SistemaBancario --> (Checar Limite de Depósito)
    SistemaBancario --> (Emitir Comprovante)
    SistemaBancario --> (Atualizar Conta)
    SistemaBancario --> (Gravar Transação)

    (Verificar Cartão e Senha) .> (Digitar Senha)
    (Checar Limite de Depósito) .> (Informar Quantia)
    (Emitir Comprovante) .> (Confirmar Depósito)
    (Gravar Transação) .> (Confirmar Depósito)
```