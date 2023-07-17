# Proyecto-casas-santiago
El problema consiste en desarrollar un modelo predictivo que permita determinar el precio de las casas en la Región Metropolitana de Santiago de Chile, tomando en cuenta una serie de variables.

## Obtención de la data

Los datos fueron obtenidos de la página web **https://www.portalinmobiliario.com/** mediante web scraping con los frameworks Beautiful Soup y Selenium. No obstante, es relevante destacar que actualmente esta técnica no es considerada escalable debido a que estos frameworks no son lo suficientemente eficientes para este propósito. Asimismo, el uso del framework Scrapy no es posible debido a que la página presenta diferentes formatos al momento de realizar el request.

### Descripción de variables

A continuación se listan todas las variables presentadas de la data con su respectiva descripción:

- Precio: Es la variable objetivo, indica el valor de casa en CLP.
- Comuna: Es una variable categórica que indica la comuna donde se encuentra la casa.
- Barrio: Es una variable categórica que indica en que barrio se cuentra la casa.

#### Tabla principal

1. Superficie total: Superficie total del terreno donde se encuentra la casa en metros cuadrados.
2. Superficie útil: Superficie construida en metros cuadrados.
3. Dormitorios: Cantidad de dormitorios por casa.
4. Baños: Cantidad de baños por casa.
5. Estacionamientos: Cantidad de estacionamientos disponibles por casa.
6. Bodegas: Cantidad de bodegas disponibles por casa.
7. Cantidad de pisos: Número de pisos de cada casa.
8. Tipo de casa: Tipo de casa, en este caso solo se extrajeron datos de "Casas".
9. Antigüedad: Años de antigüedad de cada casa.
10. Gastos comunes: Son los gastos comunes de cada casa.

Las variables de las tablas de seguridad, ambiente, servicios, comodidades y equipamiento y condiciones especiales son binarias, solo pueden tomar un valor si o no.

#### Tabla de seguridad

1. Alarma 
2. Conserjería
3. Portón automático
4. Con condominio cerrado
5. Acceso controlado

#### Tabla de ambiente

1. Quincho
2. Piscina
3. Closets
4. Baño de visitas
5. Terraza
6. Comedor
7. Walk-in clóset
8. Homeoffice
9. Living
10. Patio
11. Dormitorio en suite
12. Balcón
13. Mansarda
14. Jardín
15. Cocina
16. Dormitorio y baño de servicio
17. Playroom
18. Logia
19. Desayunador

#### Tabla de servicios

1. Acceso a internet
2. Aire acondicionado
3. Calefacción
4. TV por cable
5. Línea telefónica
6. Gas natural
7. Generador eléctrico
8. Con energia solar
9. Con conexión para lavarropas
10. Agua corriente
11. Cisterna
12. Caldera

#### Tabla de comodidaes y equipamiento

1. Chimenea
2. Gimnasio
3. Jacuzzi
4. Estacionamiento de visitas
5. Área de cine
6. Área de juegos infantiles
7. Con área verde
8. Ascensor
9. Cancha de básquetbol
10. Con cancha de fútbol
11. Cancha de paddle
12. Cancha de tenis
13. Con cancha polideportiva
14. Salón de fiestas
15. Sauna
16. Refrigerador

#### Tabla de condiciones especiales

1. Amoblado

#### Tabla de información de la zona

Todas las variables de esta tabla estan a 2km de distancia de la dirección de la casa y estan experasadas en cantidad. Además solo pueden tener un valor máximo de 5, que es la cantidad mostrada en la página web.

- Transporte:
    1. Estaciones de metro
    2. Paraderos
- Educación:
    1. Jardines infantiles
    2. Colegios
    3. Universidades
- Áreas verdes:
    1. Plazas
- Comercios:
    1. Supermercados
    2. Farmacias
    3. Centros comerciales
- Salud:
    1. Hospitales
    2. Clínicas

En total se tiene un total de 76 variables dependientes.
