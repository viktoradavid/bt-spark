#Systém pro analýzu proudu dat v reálném čase

Současným trendem ve zpracování dat, zejména dat ve velkých objemech, je provádět jejich analýzu v reálném čase. Cílem této bakalářské práce je naimplementovat systém, který by v reálném čase prováděl analýzu příspěvků ze sociální sítě Twitter. K analýze bude použit framework Spark. Výsledky analýzy reprezentující přání uživatelů této sociální sítě budou persistovány ve vhodném úložišti a přístupná pomocí RESTového API. Proveďte následující kroky:

1. Seznamte se s technologiemi, jež se používají pro zpracování proudů dat, zejména s frameworkem Spark.
2. Navrhněte systém, který bude zpracovávat proud dat ze sociální sítě Twitter. Výsledky ukládejte a zpřístupněte pomocí RESTového API.
3. Analyzujte metody používané pro zpracování textu. Vyberte několik základních, které implementujete do vámi navrženého systému tak, aby bylo možno prokázat jeho funkcionalitu.
4. Systém za použití vhodných technologií naimplementujte.
5. Implementaci otestujte.
6. Zhodnoťte dosažené výsledky.


##Available API endpoints:

`http://twitter-wish-api.herokuapp.com/wish/?from=[timestamp]&to=[timestamp]`
- returns list of wishes published in last 10 minutes, unless *from* and *to* parameters are specified.


`http://twitter-wish-api.herokuapp.com/wish/<tweet_id>`
- same as /wish, but returns data for tweet with given id only


`http://twitter-wish-api.herokuapp.com/stats/?from=[timestamp]&to=[timestamp]&density=[density]``
- stats - number of tweets, english tweets, wishes and average sentiment in last 10 minutes or given time interval.




All parameters are optional. [timestamp] is standard unix timestamp.

(Outdated)For example API usage, see:

http://tweet-wishes.s3-website.eu-central-1.amazonaws.com/

http://tweet-wishes.s3-website.eu-central-1.amazonaws.com/wish.html?id=711637967316631552
