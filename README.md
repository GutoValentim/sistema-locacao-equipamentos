# sistema-locacao-equipamentos
Sistema de Locação de Equipamentos para Eventos

## Cadastro de Equipamentos
- Cadastrar equipamentos de 3 categorias:
    ### I) Equipamentos de som
    - Código de identifificação
    - Descrição
    - Valor da diária
    - Potência em watts
    > Quantidade de canais de áudio
    ### II) Equipamentos de Iluminação
    - Código
    - Descrição
    - Valor da diária
    > Tipo de iluminação:
    >  1. LED
    >  2. Refletor
    >  3. Laser
    - Potência em watts
    ### III) Equipamentos de projeção
    - Código de identificação
    - Descrição
    - Valor diária
    > Resolução:
    >  1. HD
    >  2. Full HD
    >  3. 4k

    > Luminosidade em lúmens

### 1. Cadastrar equipamentos
### 2. Listar equipamentos cadastrados
### 3. Consultar equipamentos por código
### 4. Listar equipamentos disponíveis para locação

## Cadastro de clientes
### 1. Cadastrar com:
    > 1. Identificação
    > 2. Telefone
    > 3. E-mail
### 2. Consultar cadastrados

## Gerenciamento de locações
- Registrar uma locação para determinado cliente, contendo um ou mais equipamentos e a quantidade de dias
- Impedir locação de equipamentos já alugados
- Impedir inclusão duplicada de equipamento na mesma locação
- Calcular o valor individual de cada equipamengto e o valor total da locação
- Registrar devolução dos equipamentos, tornando-os disponíveis e calculando multa em caso de atraso
- Manter histórico de locações realizadas

## Cálculo de valores
- Varia conforme a categoria do equipamento:
    ### Som:
    Valor diária * quantidade de dias
    ### Iluminação:
    (Valor diária * quantidade de dias) * 1.10
    ### Projeção:
    - if (dias < 5) {Valor diária * quantidade de dias}
    - else (dias >= 5) {(Valor diária * quantidade de dias) * 0.90} 

    > Implementado utilizando POLIMORFISMO

    > Diferentes equipamentos passam a ser tratados de maneira uniforme

    > Não há necessidade de verificar explicitamente a categoria de cada equipamento

## Consultas e relatórios
- Listar as locações ativas
- Consultar histórico de locação de determinado cliente
- Exibir detalhes de uma locação:
    - Cliente
    - Equipamentos
    - Valores individuais
    - Valor total

## Requisitos:
### I) Linguagem = Java
### II) Mínimo de 10 classes
### III) Utilizar:
    > 1. Herança para representar categorias de equipamentos
    > 2. Polimorfismo para valores das locações
### IV) Classes organizadas em pacotes
    > Seperação de responsabilidades do sistema
    > Interface com usuário
    > Regras de negócio
### V) Encapsulamento, relacionamentos entre objetos e coleções Java
### VI) Tratamento de operações inválidas, utilizando exceções
### VII) Interação com usuário = Interface Gráfica (GUI)
### VIII) Não há necessidade de DB ou persistência de arquivos
### IX) Atributos e métodos static apenas na main e em constantes
### X) Sem uso de IA


        
