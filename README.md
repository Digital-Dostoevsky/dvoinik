# prestuplenie_i_nakazanie

## Automated Tagging

The first round of tagging was completed by developer Simon Wiles. Simon automated the initial steps of name tagging, place tagging, and speech tagging. For name tagging, Simon wrapped in a simple <persName> tag any name that appeared in the novel. (He was provided with a list of names beforehand.) The process for tagging places – with the <placeName> tag – was essentially the same (Simon was also provided with a list of places beforehand). Lastly, Simon automated the basic tagging of speech by encoding what appeared to be instances of speech (strings of text set off by specific punctuation) in the following way: 

```xml
<said aloud=“” direct=“” who=“” toWhom=“”>[text goes here]</said>.
```

Automated name and place tagging was mostly successful. Only the occasional name or place was missed, and very rarely was something that was not a name or a place tagged as if it was. For example: sometimes capitalized words at the beginning of a sentence – e.g. “Барин” – were falsely tagged as person names.

Automated speech tagging was a little more complicated due to the patterning of punctuation markings. Not infrequently were passages of text marked erroneously. Moreover, closing speech tags ```(</said>)``` had a tendency to appear in the wrong places. Complications arose too in instances where there was speech inside of speech. In general, though, any problems with automated tagging of speech could be easily addressed by paying close attention while reading. 

After the automated tagging, our next step was to manually populate the blank spaces in ```<persName>```, ```<placeName>```, and ```<said>``` tags.

## Names

The ```<persName>``` tag was filled in by XML identifiers and information about what kind/part of a name was being used: first names, patronymics, last names, diminutives, epithets, and nicknames. XML ID practices differed depending on what parts of a name were available. Characters with first name, last name, and patronymic were assigned three initials, for example, RRR for Rodion Romanovich Raskol'nikov. Some characters had only two names, such as first name and patronymic (for example, Porfirii Petrovich or Lizaveta Ivanovna). These characters were assigned XML IDs that reflected the first syllables of their initials (for example, porpe or lizi). Characters that had only first names (servants, for example) were given an XML ID that connects their first name with a more prominent character with whom they are associated (e.g. Afanasii Ivanovich's servant Vasia is identified as vasai). In some cases, to differentiate from characters with the same name in other novels in the corpus, pn was added to designate that the character is in Prestuplenie i nakazankie (for example, pnnast for Nastas'ia). Some characters who are most commonly known not by their name, but by a specific word (for example, the pawnbroker is often called starushka) have an XML ID that reflects this (for example, star for starushka).

Some characters in the novel, even if they have names (which is not always the case), are primarily referred to by their professions or titles (certain servants, officials, public servants, etc.). For these characters, their professions/titles are their XML ID.

Some characters are referred to entirely by their relationship to other characters (e.g Svidrigailov's wife and her parents or the girls that Svidrigailov "helped"). Characters such as these receive an XML ID with a reference to the named character to whom they are attached: "svidnev" for Svidrigailov's unnamed fiancée, "papsvidnev" for her father, "mamsvidnev" for her mother. Characters that are more numerous, for example, the girls that Svidrigailov "helped" receive a number and a reference to the character to whom they are attached: “devsvid1” for the first to appear, and so on.

In some cases, characters are identified using an XML ID that begins with "im." This denotes that the character is imaginary, such as when a character has a dream in which conversations happen. Otherwise these XML IDs follow the above conventions. So, for example, the unnamed mother of the unnamed girl who appears in Svidrigailov's second dream is identified as "mamimdev2".

Groups of individual characters who speak or act as a unit in the text are tagged using ```<personGrp>``` (e.g. Katerina Ivanovna's children are identified as "detmar").

Some names in the text are not tagged as characters at all (that is, they do not get an XML ID). These are minor characters/figures that never speak or are spoken to or that really play no significant role in the text. Any names like this are simply wrapped in a ```<persName>``` tag with no further identifiers. 

The back matter organizes names into different categories/types of characters. These are: fictional (which includes imaginary characters), fictional non-Dostoevsky, historical, and other (which primarily includes religious figures). 

## Places

Places are tagged more or less in the same way as person names. Each place receives an XML ID, and all places are grouped into different categories in the back matter. These categories are: fictional, St Petersburg, Russia, city (including cities that are in Russia such as St Petersburg), country, continent, and other. Other is a catch-all, which includes a mixture of Biblical places (e.g. Golgotha and Sodom), historical places (e.g. Rus'), named regions (e.g. Dagestan, Schleswig-Holstein), and natural features (e.g. Mont Blanc, the North Pole, and the Bay of Naples). 

## Speech

Most of speech tagging was straightforward in this novel, though there are a few peculiarities. 

There are a couple instances where speech not assignable to particular people is more or less just floating around – that is, there is dialogue, but there is no indication who specifically is speaking or being spoken to. In these cases speech is tagged without a who or toWhom. 

## Odds and ends

To distinguish dreams in the narrative, we use ```<seg type="dream">```.
