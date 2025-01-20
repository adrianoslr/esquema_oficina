# Sistema de Controle de Oficina Mecânica

Este projeto apresenta um esquema conceitual para um sistema de controle e gerenciamento de ordens de serviço em uma oficina mecânica. Ele foi desenvolvido para atender aos requisitos descritos na narrativa do desafio.

## Descrição do Esquema Conceitual

### Entidades:
1. **Cliente**
   - Representa os clientes da oficina.
   - Atributos:
     - ID_Cliente (chave primária)
     - Nome
     - CPF/CNPJ
     - Telefone
     - Endereço

2. **Veículo**
   - Representa os veículos atendidos na oficina.
   - Atributos:
     - ID_Veículo (chave primária)
     - Placa
     - Modelo
     - Ano
     - Marca
     - ID_Cliente (chave estrangeira)

3. **Ordem de Serviço (OS)**
   - Representa uma ordem de serviço emitida para um veículo.
   - Atributos:
     - N_OS (chave primária)
     - Data_Emissão
     - Data_Conclusão
     - Valor_Total
     - Status
     - ID_Veículo (chave estrangeira)

4. **Serviço**
   - Representa os serviços disponíveis na oficina.
   - Atributos:
     - ID_Serviço (chave primária)
     - Descrição
     - Preço_Base

5. **Peça**
   - Representa as peças utilizadas nos serviços.
   - Atributos:
     - ID_Peça (chave primária)
     - Descrição
     - Preço_Unitário
     - Quantidade

6. **Equipe**
   - Representa uma equipe de mecânicos.
   - Atributos:
     - ID_Equipe (chave primária)
     - Nome_Equipe

7. **Mecânico**
   - Representa os mecânicos que compõem uma equipe.
   - Atributos:
     - ID_Mecânico (chave primária)
     - Nome
     - Endereço
     - Especialidade
     - ID_Equipe (chave estrangeira)

8. **Serviço_Realizado**
   - Entidade associativa entre OS e Serviço.
   - Atributos:
     - ID_Serviço_Realizado (chave primária)
     - ID_OS (chave estrangeira)
     - ID_Serviço (chave estrangeira)
     - Quantidade
     - Valor_Calculado

9. **Peça_Utilizada**
   - Entidade associativa entre OS e Peça.
   - Atributos:
     - ID_Peça_Utilizada (chave primária)
     - ID_OS (chave estrangeira)
     - ID_Peça (chave estrangeira)
     - Quantidade
     - Valor_Calculado

## Relacionamentos
- Cliente possui um ou mais veículos.
- Veículo está associado a uma ou mais ordens de serviço (OS).
- OS inclui serviços e utiliza peças.
- Equipes realizam serviços nas ordens de serviço.
- Cada equipe é composta por mecânicos.

## Diagrama Conceitual
Veja o diagrama abaixo ou [clique aqui para editar no Lucidchart](https://mlai.lucid.app/plugin/edit/aiplugin_a306a58e-fb4b-44c0-931d-d35f30978367).

![Diagrama Conceitual](https://mlai.lucid.app/plugin/images/aiplugin_a306a58e-fb4b-44c0-931d-d35f30978367)

---

### Próximos Passos
1. Adicionar o esquema lógico baseado no conceitual.
2. Implementar o banco de dados usando uma tecnologia de sua escolha.
3. Testar as consultas e operações no banco.

