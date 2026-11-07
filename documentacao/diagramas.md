```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#800020','primaryTextColor':'#FFFFFF','primaryBorderColor':'#5A0016','lineColor':'#888888'}}}%%
classDiagram
    class Usuaria {
        +int id
        +String nome
        +String telefone
        +String interfaceCamuflada
        +cadastrarContato()
        +acionarAlerta()
    }

    class ContatoConfianca {
        +int id
        +String nome
        +String telefone
        +receberAlerta()
    }

    class ComandoOculto {
        +String sequencia
        +validar()
    }

    class Alerta {
        +int id
        +DateTime dataHora
        +double latitude
        +double longitude
        +String status
        +cancelar()
    }

    class Viatura {
        +int id
        +String prefixo
        +confirmarAtendimento()
    }

    Usuaria "1" --> "1..*"
