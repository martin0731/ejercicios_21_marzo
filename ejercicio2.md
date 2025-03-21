```mermaid
classDiagram
    class Auto {
        - string placa
        - string modelo
        - bool disponible
        + Auto(string p, string m)
        + ~Auto()
        + string getPlaca() const
        + string getModelo() const
        + bool estaDisponible() const
        + void rentar()
        + void devolver()
    }

    class Cliente {
        - int id
        - string nombre
        + Cliente(int i, string n)
        + ~Cliente()
        + int getId() const
        + string getNombre() const
    }

    class Contrato {
        - Cliente* cliente
        - Auto* autoRentado
        - int dias
        + Contrato(Cliente* c, Auto* a, int d)
        + ~Contrato()
    }

    class AgenciaRenta {
        - string nombre
        - vector <Auto*> autos
        - vector <Cliente*> clientes
        + AgenciaRenta(string n)
        + ~AgenciaRenta()
        + void agregarAuto(Auto* autoPrt)
        + void agregarCliente(Cliente* clientePrt)
        + void mostrarInfo() const
    }

    AgenciaRenta o-- Auto 
    AgenciaRenta o-- Cliente 
    Cliente  --o Contrato 
    Auto --o Contrato 
```
