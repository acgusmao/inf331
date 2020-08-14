# Tarefa sobre catálogo de componentes
[notebook/components-01-catalog.ipynb](notebook/components-01-catalog.ipynb)

# Tarefa Web Components 1
~~~html
<dcc-trigger label="Mundo" 
	action="noticia/mundo/politica"
	value="Mundo - politica">
</dcc-trigger>

<dcc-trigger label="Brasil P"
	action="noticia/brasil/politica"
	value="Brasil - politica">
</dcc-trigger>

<dcc-trigger label="Brasil E"
	action="noticia/brasil/esporte"
	value="Brasil - esporte">
</dcc-trigger>

<dcc-trigger label="Bahia"
	action="noticia/bahia/esporte"
	value="Bahia - esporte">
</dcc-trigger>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="doctor"
                 speech="Quero saber sobre: ">
                 <subscribe-dcc topic="#/politica"></subscribe-dcc>
</dcc-lively-talk>
<dcc-lively-talk duration="0s"
                 character="nurse"
                 speech="Quero saber sobre: ">
                 <subscribe-dcc topic="noticia/brasil/#"></subscribe-dcc>
</dcc-lively-talk>
<dcc-lively-talk duration="0s"
                 character="patient"
                 speech="Quero saber sobre: ">
                 <subscribe-dcc topic="#"></subscribe-dcc>
</dcc-lively-talk>
~~~

# Tarefa Web Components 2

TBD
