## Tarefa 1
> ![Diagrama de Orquestração](images/componentizacao-negocio.png)

## Tarefa 2
> ![Diagrama de Orquestração](images/componentizacao-tecnico-view.png)

## Tarefa 3
> ![Diagrama de Orquestração](images/componentizacao-tecnico-model.png)

## Tarefa 4

### Serviço `Open Library`
* **Título do serviço**: `Books API`
* **Breve descrição**:
  > The Open Library Books API provides a programmatic client-side method for querying information of books using Javascript.
* **URL completa da requisição**: `https://openlibrary.org/api/books?bibkeys=ISBN:0201558025,LCCN:93005405&format=json`

### Serviço Exemplo com parametro de ISBN e formato JSON
* **Cabeçalho HTTP da chamada**:
~~~http
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9,pt;q=0.8,fr;q=0.7
Cache-Control: max-age=0
Connection: keep-alive
Host: openlibrary.org
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: none
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 6.3; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.135 Safari/537.36
~~~
* **Cabeçalho HTTP da resposta**:
~~~http
Access-Control-Allow-Method: GET, OPTIONS
Access-Control-Allow-Origin: *
Access-Control-Max-Age: 86400
Connection: keep-alive
Content-Type: application/json
Date: Fri, 28 Aug 2020 00:22:57 GMT
Server: nginx/1.4.6 (Ubuntu)
Transfer-Encoding: chunked
X-OL-Stats: "IB 2 0.063 MC 2 0.001 TT 0 0.068"
~~~
* **Parametros da chamada**:
~~~http
bibkeys: ISBN:0201558025,LCCN:93005405
format: json
~~~
* **Conteúdo da resposta**:
~~~json
Conteúdo da resposta:
{"LCCN:93005405": {"bib_key": "LCCN:93005405", "preview": "noview", "thumbnail_url": "https://covers.openlibrary.org/b/id/240726-S.jpg", "preview_url": "https://openlibrary.org/books/OL1397864M/Zen_speaks", "info_url": "https://openlibrary.org/books/OL1397864M/Zen_speaks"}, "ISBN:0201558025": {"bib_key": "ISBN:0201558025", "preview": "restricted", "thumbnail_url": "https://covers.openlibrary.org/b/id/135182-S.jpg", "preview_url": "https://archive.org/details/concretemathemat00grah_444", "info_url": "https://openlibrary.org/books/OL1429049M/Concrete_mathematics"}}
~~~
### Serviço Exemplo com parametro de ISBN, detalhes e formato JSON
* **Detalhes do livro no formato JSON**:
https://openlibrary.org/api/books?bibkeys=ISBN:9780980200447&jscmd=details&format=json
* **Cabeçalho HTTP da chamada**:
~~~http
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9,pt;q=0.8,fr;q=0.7
Cache-Control: max-age=0
Connection: keep-alive
Host: openlibrary.org
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: none
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 6.3; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.135 Safari/537.36
~~~
* **Cabeçalho HTTP da resposta**:
~~~http
Access-Control-Allow-Method: GET, OPTIONS
Access-Control-Allow-Origin: *
Access-Control-Max-Age: 86400
Connection: keep-alive
Content-Type: application/json
Date: Fri, 28 Aug 2020 00:31:06 GMT
Server: nginx/1.4.6 (Ubuntu)
Transfer-Encoding: chunked
X-OL-Stats: "IB 1 0.065 MC 3 0.005 TT 0 0.073"
~~~
* **Parametros da chamada**:
~~~http
bibkeys: ISBN:9780980200447
jscmd: details
format: json
~~~
* **Conteúdo da resposta**:
~~~json
{"ISBN:9780980200447": {"info_url": "https://openlibrary.org/books/OL22853304M/Slow_reading", "bib_key": "ISBN:9780980200447", "preview_url": "https://archive.org/details/slowreading00mied", "thumbnail_url": "https://covers.openlibrary.org/b/id/5546156-S.jpg", "details": {"number_of_pages": 92, "table_of_contents": [{"level": 0, "label": "", "pagenum": "", "title": "The personal nature of slow reading"}, {"level": 0, "label": "", "pagenum": "", "title": "Slow reading in an information ecology"}, {"level": 0, "label": "", "pagenum": "", "title": "The slow movement and slow reading"}, {"level": 0, "label": "", "pagenum": "", "title": "The psychology of slow reading"}, {"level": 0, "label": "", "pagenum": "", "title": "The practice of slow reading."}], "contributors": [{"role": "Cover Photographs", "name": "C. Ekholm"}], "isbn_10": ["1936117363"], "covers": [5546156], "lc_classifications": ["Z1003 .M58 2009"], "latest_revision": 22, "ocaid": "slowreading00mied", "weight": "1 grams", "source_records": ["marc:marc_loc_updates/v37.i01.records.utf8:4714764:907", "marc:marc_loc_updates/v37.i24.records.utf8:7913973:914", "marc:marc_loc_updates/v37.i30.records.utf8:11406606:914", "ia:slowreading00mied", "marc:marc_openlibraries_sanfranciscopubliclibrary/sfpl_chq_2018_12_24_run04.mrc:135742902:2094"], "title": "Slow reading", "languages": [{"key": "/languages/eng"}], "subjects": ["Books and reading", "Reading"], "publish_country": "mnu", "by_statement": "by John Miedema.", "oclc_numbers": ["297222669"], "type": {"key": "/type/edition"}, "physical_dimensions": "7.81 x 5.06 x 1 inches", "revision": 22, "publishers": ["Litwin Books"], "description": "\"A study of voluntary slow reading from diverse angles\"--Provided by publisher.", "physical_format": "Paperback", "last_modified": {"type": "/type/datetime", "value": "2019-07-16T22:44:09.608703"}, "key": "/books/OL22853304M", "authors": [{"name": "John Miedema", "key": "/authors/OL6548935A"}], "publish_places": ["Duluth, Minn"], "pagination": "80p.", "classifications": {}, "created": {"type": "/type/datetime", "value": "2009-01-07T22:16:11.381678"}, "lccn": ["2008054742"], "notes": "Includes bibliographical references and index.", "identifiers": {"amazon": ["098020044X"], "google": ["4LQU1YwhY6kC"], "goodreads": ["6383507"], "librarything": ["8071257"]}, "isbn_13": ["9780980200447", "9781936117369"], "dewey_decimal_class": ["028/.9"], "local_id": ["urn:sfpl:31223095026424"], "publish_date": "March 2009", "works": [{"key": "/works/OL13694821W"}]}, "preview": "borrow"}}
~~~