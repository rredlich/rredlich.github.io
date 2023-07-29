---
title: "Sinatra App 01"
date: 2022-08-18T22:15:17-04:00
draft: true
---
## Microlearning, mi primer app con Sinatra

Esta es la primera de varias cápsulas progresivas para desarrollar una aplicación web con Sinatra.

¿Por qué tan pequeñas? Por que si eres como yo, no tienes mucho tiempo para aprender a programar, y pequeño es rápido. Pero más importante, pequeño significa que también es rápido de escribir, y como no tengo mucho tiempo para escribir, acá también pequeño es rápido.

¿Por qué Sinatra? Sinatra es un micro-framework basado en Ruby para desarrollar aplicaciones web extremadamente rápido. Si le agregamos algo de estilos con Bootstrap CSS, tenemos el potencial de hacer pequeñas apps que se ven bien, nuevamente, más rápido.

## Para quién es esta cápsula

## Requerimientos
* Instalar Ruby
* Instalar la gema de sinatra

## La app Sinatra más simple

Crea un archivo myapp.rb y escribe lo siguiente

```ruby
require 'rubygems'
require 'sinatra'

get '/hola' do
  "Hola Mundo!"
end
```

Si ya conoces otros lenguajes de programación, verás que las primeras dos líneas son llamados a las bibliotecas de rubygems y sinatra. Luego, todo lo que está dentro de get es lo que Sinatra ejecutará cuando en el buscador consultes a /hola.

¡Hagamos una prueba! Abre un terminal y ejecuta el primer comando. Deberías ver algo como esto:

```bash
> ruby myapp.rb

== Sinatra (v2.2.1) has taken the stage on 4567 for development with backup from Puma
Puma starting in single mode...
* Puma version: 5.6.4 (ruby 3.0.2-p107) ("Birdie's Version")
*  Min threads: 0
*  Max threads: 5
*  Environment: development
*          PID: 38202
* Listening on http://127.0.0.1:4567
Use Ctrl-C to stop
```

Abre un navegador en tu computador y entra a http://127.0.0.1:4567/hola, deberías ver que tu navegador muestra el texto "Hola Mundo!", y sin tener ningún HTML entremedio.

Hagamos algo un poco más interesante. Podemos pasar un parametro por la URL. Primero, baja su aplicación precionando ctrl+c en el terminal, luego actualiza tu código con lo siguiente:

```ruby
require 'rubygems'
require 'sinatra'

get '/hola/:usuario' do
  "Hola " + params[:usuario] + "!"
end
```




