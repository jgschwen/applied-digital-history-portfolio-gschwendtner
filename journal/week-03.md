# Week 3 Journal

**Topic:** Cleaning and Normalizing Historical Data:	OpenRefine

**Time it took me:** approx. 3.5 hours

## Log / Questions to be answered while working on the project

1.	What does one row represent?
   
One unit of observation, in this case a historical photograph.

2.	Which columns describe the historical object?

`title_raw` describes the content of the photograph, `object_type_raw` describes what type of object/file/physical item it is. 

3.	Which columns describe its archival or digital representation?

`record_id`, `holding_institution_raw`, `box_folder_raw`, `filename_raw`

4.	Which columns appear suitable for a controlled vocabulary?

Everything with `_raw` in its name, except maybe for `title_raw` and `notes_raw` can and should be fully standardized.

5.	Which columns contain uncertainty that should not simply be deleted?

The uncertain dates in `date_raw` for sure. For `title_raw` and `notes_raw`, the full text is likely also relevant.

In `creator_raw`, research should be done whether e.g. an entry with only the surname provided is really the same creator as a creator with the that surname plus a first name, for example. In the `country_raw` column, the fact that these are historical photographs might mean that borders have changed, so descriptions should not be standardized to modern-day states only.

I would generally not delete any data but rather add more columns with normalized/standardized data.

---

Record two examples for each category:

•	a difference that is probably typographical;

`Austria ` and `Austria`

`France ` and `France`

•	a difference that probably represents two labels for the same concept;

`Danmark` and `Denmark`

`Public Domain` and `public domain`

•	a difference that should not be resolved without more evidence.

`Bohemia` and `Czech Rep.`

`Public domain?` and `Public Domain`

---

In your notes, record:

•	the values you merged; the preferred value you selected; why that level of specificity is appropriate.

I merged `photo` into `photograph`. I chose the longer version for completeness.

I also merged `photo;print` into `photo print`. I decided it likely meant the same in the context of it being a record of a single object, and adding the space instead of the semicolon made it a more understandable label. 

I left `photograph/print` untouched, since I did not want to assume it was a print, since in the original labelling process it could have been part of a broader category and could be either `photograph` or `photo print`. 

I am assuming that `photograph` is a more general description and could also include negatives, for example, or recordings of photos not done on paper, whereas `photo print` is clearly a print.

---

Record one rejection:

I rejected merging `Kasebier, Gertrude`, and `Käsebier, Gertrude`. The likelihood of them being the same person is high, but the umlaut diacritics aren’t optional – the equivalent for Käsebier would be Kaesebier. Also, I did not merge `Atget, E.` and `Atget, Eugène`, because the former could refer to a different Atget.

I increased the radius when using nearest neighbor functions to get more merge suggestions.

---

Choose one group of multilingual place variants that you are confident represents the same city.

1.	Create a text facet on place_norm.

2.	Use the facet's edit option to replace each selected variant with one preferred form.

3.	Record the mapping in your notes.

I merged `Prague`, `Praha` and `Prag` into Prague.

---

An exception I found concerning how the date normalization works: `PHO-089` has `n.d.` (no date) in `date_raw`, this is denoted as `exact` in `date_certainty`. This happens because the script falls back on `exact` if no other exception applies (`if(value.find(/\d{4}/).length() > 1, "range", "exact")`), and not whether it even is a number or any valid date at all.

---

When would a separate subject table be preferable to storing several subjects in one cell?

---

Duplicates facet: 

_Ask whether identical titles are sufficient evidence that the records describe the same object._

My answer: In general: No, because the same scene can be photographed by different people and/or at different times. Also, it could be different versions of the same image, like one full-size version and one cropped version. Even if all other data also appear the same (date, location, photographer, description, etc.), we have no timestamps for these types of images, so it could be that the same photographer took multiple different pictures of the same scene on the same day.

---

Duplicate candidates: `PHO-073` and `PHO-094`: date, photographer, location, subject, description, object type all match, location is the same, file name is the same, box/folder is the same. However: one of them has “verso stamped” in the notes, the other one does not. Might be a sign against it being a duplicate. Information on the backside of `PHO-094` would help. I am hesitant to call it a duplicate yet, but it is very likely.
For `PHO-025` and `PHO-098`, absolutely everything matches except for case of the creator’s name, likely a duplicate. My decision is yes, duplicate.


## 1. What material did I work with?


## 2.	What transformation did the tool perform?


## 3.	Which decisions did I make?


## 4. What failed, remained unclear, or produced an unexpected result?


## 5.	What does the output allow me to infer historically?


## 6.	What does the output not allow me to infer?


## 7.	Could this method contribute to my final project? Why or why not?

