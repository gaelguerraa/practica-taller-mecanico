Responder: ¿qué pasaría si intentaras borrar un Cliente que todavía tiene un Vehiculo?
MySQL rechaza el borrado porque la llave foránea Vehiculo_clienteId_fkey
protege la relación y usa ON DELETE RESTRICT. Primero deben eliminarse o
reasignarse los vehículos relacionados. Esto evita que queden vehículos sin un
cliente válido
