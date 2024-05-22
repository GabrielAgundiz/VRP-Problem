# VRP-Problem

Tomamos como situacion ficticia que Coca Cola, como proveedor de bebidas, ha establecido una colaboración con las sucursales de Pollo Matón en Monterrey para abastecerse con sus productos. Con el fin de optimizar la distribución y asegurar un servicio eficiente, la empresa cuenta con tres camiones disponibles para llevar a cabo las entregas durante el día.

El desafío consiste en diseñar la mejor ruta para la distribución de productos de Coca Cola a todas las sucursales de Pollo Matón en Monterrey. Esta ruta debe ser planificada de manera que se minimice la distancia recorrida, maximizando así la eficiencia en la entrega.

El objetivo consiste en encontrar la ruta óptima para cada camión, considerando la ubicación de los centros de distribución de Coca-Cola y las sucursales de Pollo Matón. Minimizando asi la distancia total recorrida de todas las rutas.

Se debe tener en cuenta la capacidad de carga de cada camión para garantizar que se pueda satisfacer la demanda de cada sucursal.

# Solucion Propuesta

Para facilitar el proceso de lectura de datos, se re-organizaron los datos de Excel en donde se modificaron los valores de las distancias entre las sucursales además en otra hoja de Excel se especificó la demanda correspondiente de cada sucursal 

Se obtiene la información necesaria, como distancias entre sucursales y centros de distribución, así como la demanda de cada sucursal, desde un archivo Excel. Se realiza una limpieza de datos para asegurar que los formatos sean adecuados para el procesamiento.

Cada sucursal se asigna al centro de distribución más cercano utilizando una heurística basada en la distancia mínima, garantizando eficiencia en términos de distancia.

Utilizando la heurística del vecino más cercano, se generan rutas iniciales para los camiones. Este método selecciona iterativamente el nodo más cercano no visitado, proporcionando una ruta inicial rápida y eficiente.

Se ajustan las rutas generadas para asegurar que cada camión regrese a su centro de distribución al finalizar la ruta, cerrando así el circuito de entrega.

Se utiliza la búsqueda tabú con best improvement para optimizar las rutas iniciales. Este método permite explorar movimientos subóptimos temporales y evitar óptimos locales, utilizando una lista tabú para evitar regresar a soluciones recientemente visitadas. La búsqueda iterativa de la mejor mejora posible permite encontrar rutas más eficientes y reducir la distancia total recorrida. 

# Resultados

Se tomaron en cuenta cuatro centros de distribución de Coca Cola: Lincoln, Universidad, Insurgentes y Guadalupe. Tras ejecutar el algoritmo con diversos parámetros e iteraciones, se obtuvieron los siguientes resultados:

Centro de distribución: Coca Cola Universidad:

Camión 1:
Recorrido > Pollo matón Girasoles > Pollo matón Escobedo > Pollo matón Concordia > Pollo matón Montes Berneses > Coca Cola Universidad
Demanda total: 2740 kg
Distancia de la ruta: 35.9 km

Camión 2:
Recorrido > Pollo matón Rodrigo Gómez > Pollo matón San Nicolás > Pollo matón Santo Domingo > Pollo matón Centro > Pollo matón Centrika > Coca Cola Universidad
Demanda total: 2930 kg
Distancia de la ruta: 28.5 km

Camión 3:
Recorrido > Pollo matón Las Puentes > Pollo matón Cordillera de los Andes > Coca Cola Universidad
Demanda total: 995 kg
Distancia de la ruta: 17.2 km

Centro de distribución: Coca Cola Lincoln:

Recorrido > Pollo Matón Lincoln > Pollo Matón Solidaridad > Pollo Matón Aztlan > Pollo Matón Cumbres
Demanda total > 2340 kg
Distancia total de la ruta > 30.29 km

Centro de distribución: Coca Cola Insurgentes:

Recorrido > Pollo matón Santa Catarina > Pollo matón Lázaro Cárdenas > Pollo matón Simón Bolívar 
Demanda total: 2070 kg
Distancia de la ruta: 44.4 km


Centro de distribución: Coca Cola Guadalupe:

Recorrido > Pollo matón Revolución > Pollo matón Lindavista
Demanda total: 1696 kg
Distancia de la ruta: 19.9 km

Distancia total recorrida: 176.20 km
