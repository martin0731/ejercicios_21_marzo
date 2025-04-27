```mermaid
classDiagram
    class Habitacion {
        - int numero
        - string tipo
        - bool ocupada
        + Habitacion(int num, string t)
        + ~Habitacion()
        + int getNumero() const
        + string getTipo() const
        + bool estaOcupada() const
        + void ocupar()
        + void desocupar()
    }

    class Cliente {
        - int id
        - string nombre
        + Cliente(int i, string n)
        + ~Cliente()
        + int getId() const
        + string getNombre() const
    }

    class Hotel {
        - string nombre
        - vector<Habitacion> habitaciones
        - vector<Cliente*> clientes
        + Hotel(string n)
        + ~Hotel()
        + void agregarHabitacion(int numero, string tipo)
        + void registrarCliente(Cliente* cliente)
        + void mostrarInfo() const
    }

    Hotel *-- Habitacion 
    Hotel o-- Cliente
```
