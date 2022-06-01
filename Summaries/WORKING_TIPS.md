It's not even as much about coding for most senior positions. You have to be able to understand the context and motivations for the software, which means you need to know the company and the market it caters to. Then you need to be able to distinguish between what's important and the random bullshit the various management people come up with, AND convince them that if they want a working product they'll have to adjust their expectations. Then that needs to be converted into models, processes, restrictions and whatnot, before you can even think about coding.

I like to mention something like this when interviewing (of which I recently did a bit of) but instead of phrasing it the way you did I like to say that, **when you get user feature requests they don't always make a lot of sense but if you go to the person making the request, a lot of times you can figure out the problem they are trying to solve and come up with a better solution that even they like more.**
Users are good at identifying problem areas but not always so good at finding solutions.

Teaching Stakeholders how to convey what they need instead of how they need something done is one of the skills you need at this level. 

This is why I push user stories to anyone that just doesn't get this. User stories are not required to be able to write code, there are lots of ways of conveying this information. But for those that just have no idea, this gives them a structure/template to follow and avoids having to have endless conversations arguing about whether they're telling you what/why or rather how.

Stakeholders don't like to be told their 'how' is not the best path, because they are already out of their depth, and tend to take it as 'You won't implement my idea, aren't you supposed to work for ME/US?'. They take it very personally.

One of the best tools I’ve found for pushing back without getting axed is “Saying no by saying yes…but”. When management comes with a request and whether or not it can get worked into the project, you say something like “Yes, but… it’s going to take X resources, probably push our schedule out Y longer, and we’ll need to deprioritize Z features.” The response is usually, “Oh… yeah that’s probably not a good idea”. Now you don’t have extra work on your/your teams plate and your management feels like they came to good conclusion on their own.

*I just had a boss that hated anyone saying no to her. She wanted something done, and if you said you couldn't do it, or it wasn't a good idea, you'd be in her sights. If you said, okay I'll look into it. And a day or two later tell her what it'd take to get it done, or explain why it wasn't feasible, she was much more accepting about it. The delay was the key because by then she had something else on her mind and the thing from the other day was not pressing anymore.*

*This person is emotionally driven and unfit for product positions. Everything is pressing probably because they cannot identify any problems, nor argue about anything from a position of competence, and are being pressed by someone higher up.*

"No take, only throw."

- companies that want experienced applicants, but refuse to create experienced workers.


## Nederlands werktips

Dat is wel even een vraag zeg, er zijn zoveel type bugs ;)

De basis van een bug fixen is begrijpen waar het mis gaat en waarom.

Stel je hebt een null pointer error (oftewel, het verwachte object bestaat niet), dan zul je een vrij duidelijke exception krijgen met het regel nummer waar dat fout gaat. Dus het waar is dan vrij makkelijk gevonden.

De volgende stap is waarom. Bij null pointers zijn het dan typisch 1 van twee dingen. Ten eerste, je code zou met null om moeten kunnen gaan, maar kan dat niet, of je zou op dat moment geen null waarde mogen hebben. Bijvoorbeeld een todo item zou altijd een creator moeten hebben.

Vanaf daar zoek je uit welke van die twee situaties het is. Vaak is dat een stukje domein kennis, maar je kunt bijvoorbeeld ook in het object kijken naar hoe relaties beschreven zijn. Stel dat de waarde dan niet null mag zijn, dan moet je verder zoeken naar de plaatsen waar die waarde gezet wordt en of het op 1 van die locaties een null kan zijn. Bijvoorkeur test je dan een keer dat het inderdaad fout gaat op die manier, omdat je daarmee dan ook kan zien of het weer goed gaat.

Persoonlijk vind ik het altijd belangrijk om even de tijd te nemen om echt te begrijpen waarom het mis gaat en niet aan symptoom bestrijding te doen. Bij die null pointer kun je gewoon een check toevoegen of de waarde niet null is. Daarom komt die specifieke foutmelding niet meer voor. Maar je hebt de eigenlijke bug niet opgelost. Het werkt vaak goed om gewoon waarom te blijven vragen aan jezelf als je denkt dat je een uitleg hebt. Ok, het probleem is dat die waarde null is. Waarom is dat een probleem?

Verder is bugs oplossen ook echt iets waar je vanzelf beter in wordt, je leert herkennen wanneer je dieper moet duiken en wanneer je iets gewoon kan fixen.

Open source projecten zijn leuk, maar vaak te intimiderend voor junioren om echt in te duiken. De bugs die niet gelijk opgepakt worden zijn vaak ook te complex.

Oftewel, vooral doorgaan. Als je iets open source zoekt pak dan vooral een heel klein project wat misschien niet eens meer onderhouden wordt waar mensen wel wat issues voor gemeld hebben. Daar is vaak wel wat laag hangend fruit te vinden. Daarnaast is code lezen ook al heel nuttig. Pak een willekeurige functie in een stuk code en probeer te begrijpen of deze goed werkt.