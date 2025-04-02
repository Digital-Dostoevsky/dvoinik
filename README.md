# dvoinik

## Tagging

The first round of tagging was completed by Katherine Bowers, Braxton Boyer, Kate Holland, and Elena Vasileva. Each tagger tagged a section of the novella: Kate tagged chapters 1-4, Katherine tagged chapters 5-7, Braxton tagged chapters 8-10, and Elena tagged chapters 11-13. Tags identified formal elements of the text (e.g. chapter headings and paragraph breaks), character names (using <persName>), objects (using <objectName>, locations (using <placeName>, and speech (using <said>). 

## Names

The ```<persName>``` tag was filled in by XML identifiers and information about what kind/part of a name was being used: first names, patronymics, last names, diminutives, epithets, and nicknames. XML ID practices differed depending on what parts of a name were available. Characters with first name and patronymic were assigned three initials, for example, KO for Klara Olsuf'evna. Characters that had only first names (Petrushka, for example) were given an XML ID that reflects their first name (pet). Goliadkin, who is commonly referred to as Gospodin Goliadkin, is given the XML ID gol, while his double, commonly referred to also as Goliadkin (Jr), is given the XML ID dbl. 

Some characters in the novel, even if they have names (which is not always the case), are primarily referred to by their professions or titles (certain servants, officials, public servants, etc.). For these characters, their professions/titles are their XML ID. In some cases, unnamed characters are identified by their profession and a more prominent character to whom they are connected (e.g. "sluga Andreia Filippovicha" has the XML id saf). 

In some cases, characters are identified using an XML ID that begins with "im." This denotes that the character is imaginary, such as when a character has a dream in which conversations happen. Otherwise these XML IDs follow the above conventions. So, for example, imko refers to imagined Klara Olsuf'evna, from whom Goliadkin receives letters.

Groups of individual characters who speak or act as a unit in the text are tagged using ```<personGrp>``` (e.g. a group of young clerks is identified as mch). 

Some names in the text are not tagged as characters at all (that is, they do not get an XML ID). These are minor characters/figures that never speak or are spoken to or that really play no significant role in the text. Any names like this are simply wrapped in a ```<persName>``` tag with no further identifiers. 

The back matter organizes names into different categories/types of characters. These are: fictional (which includes imaginary characters), fictional non-Dostoevsky, historical, and other (which includes only God).


## Objects 

Objects, such as a samovar, are also tagged. Objects are only encoded if they are animated. For example, a samovar that whistles or a wad of money that speaks. These are tagged using <objectName> and are listed in the backmatter. XML IDs are applied that reflect a shorthand identifying the object (e.g. sam for the samovar or wad for the wad of cash).

## Places

Places are tagged more or less in the same way as person names. Each place receives an XML ID, and is identified according to type. Types include: city, street, residence, commercial, country, park, dining, region. 

## Speech

For speech tags, attributes including aloud, direct, who, and toWhom were included in the basic formula below: 

```xml
<said aloud=“” direct=“” who=“” toWhom=“”>[text goes here]</said>.
```

Most of speech tagging was straightforward in this novel, though there are a few peculiarities. 

There are a couple instances where speech not assignable to particular people is more or less just floating around – that is, there is dialogue, but there is no indication who specifically is speaking or being spoken to. In these cases speech is tagged without a who or toWhom. 

