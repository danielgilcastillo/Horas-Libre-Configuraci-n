SOLID Refactorización de Código

Este repositorio contiene un ejemplo de refactorización de código para aplicar los principios SOLID, mejorando la flexibilidad, mantenibilidad y escalabilidad del diseño.

Principios SOLID

Este proyecto aplica los siguientes principios SOLID:

1. SRP (Single Responsibility Principle)**: Cada clase tiene una única responsabilidad. Por ejemplo, `LamparaAccion` maneja el encendido/apagado, mientras que `LamparaLog` maneja el registro de logs.
2. OCP (Open/Closed Principle)**: El sistema permite la extensión mediante la implementación de interfaces (`Encendible` y `Hacerlog`) sin modificar las clases existentes.
3. LSP (Liskov Substitution Principle)**: Clases derivadas (`LamparaAccion`, `LamparaLog`) pueden sustituir a las clases base sin alterar la funcionalidad del sistema.
4. ISP (Interface Segregation Principle)**: Interfaces especializadas (`Encendible` y `Hacerlog`) evitan que las clases implementen métodos innecesarios.
5. DIP (Dependency Inversion Principle)**: `Interruptor` y `GestorDispositivos` dependen de abstracciones (interfaces) en lugar de implementaciones concretas, facilitando la inyección de dependencias y el desacoplamiento.

Estructura del Proyecto

- Encendible**: Interface para dispositivos que pueden encenderse y apagarse.
- Hacerlog**: Interface para dispositivos que pueden registrar logs.
- Lampara**: Clase base que mantiene el estado de la lámpara.
- LamparaAccion**: Clase que implementa `Encendible`, controlando el encendido y apagado de la lámpara.
- LamparaLog**: Clase que implementa `Hacerlog`, manejando el registro de eventos de la lámpara.
- GestorDispositivos**: Clase que combina `Encendible` y `Hacerlog` para gestionar los dispositivos.
- Interruptor**: Clase que controla el estado del `GestorDispositivos`.

Para probar el sistema:

Para comprobar el funcionamiento correcto del código, el método main en MainApp ha sido actualizado para simular el encendido y apagado de la lámpara y registrar estos eventos en la consola.
