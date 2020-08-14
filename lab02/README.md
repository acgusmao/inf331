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
~~~html
<dcc-trigger label="Science Feed" action="next/science">
</dcc-trigger>

<dcc-trigger label="Design Feed" action="next/design">
</dcc-trigger>

<dcc-rss publish="rss/science" source="https://www.wired.com/category/science/feed">
  <subscribe-dcc topic="next/science" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-rss publish="rss/design" source="https://www.wired.com/category/design/feed">
  <subscribe-dcc topic="next/design" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-aggregator publish="aggregate/science" quantity="3">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-aggregator>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="doctor"
                 speech="Hello, ">
  <subscribe-dcc topic="aggregate/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="nurse"
                 duration="0s"
                 character="nurse"
                 speech="Hello, ">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="patient"
                 duration="0s"
                 character="patient"
                 speech="Hello, ">
  <subscribe-dcc topic="rss/design"></subscribe-dcc>
</dcc-lively-talk>
~~~