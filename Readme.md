*This project has been created by Florent Cretin.*
<!-- 𝔸 𝔹 ℂ 𝔻 𝔼 𝔽 𝔾 ℍ 𝔾 𝕁 𝕂 𝕃 𝕄 ℕ 𝕆 ℙ ℚ ℝ 𝕊 𝕋 𝕌 𝕍 𝕎 𝕏 𝕐 ℤ -->
<!-- 🗎 🖋 👀 🗣 … -->

[Tag_video_jason]: https://www.youtube.com/watch?v=f3QwwnvSQ50
[Tag_github_jason]: https://github.com/jasonchampagne/FormationVideo/blob/master/Ressources/Aide/expressions-rationnelles.md

[Tag-requirements-regexr]: https://regexr.com/
[Tag-requirements-regex101]: https://regex101.com/

# Regex



<details>
<summary style="font-size: 2em;"><strong id="summary" >🗓 𝕊ummary</strong></summary>

- [𝔻escription](#description)
- [𝕆bjectives](#objectives)
- [🕑 𝕃earning ℙrogression](#learningprogression)
- [🛠 ℝequirements](#requirements)
- [𝕌sage](#objectives)
- [𝕃earning Notes](#learning-notes)
- [ℝesources](#resources)
- [🖋 𝔸uthor](#author)

</details>

<h2 id="description">𝔻escription</h2>

>Dans le cours javascript il parlais de regex alors j'ai fait une petit pause de ce cours pour allez voir une [video][Tag_video_jason]
>
>J'ai aussi pour but de faire un parseur regex un jour car la meilleur facon d'apprendre est de faire...


- [🗓 𝕊ummary](#summary)
<br>

---

<br>

<h2 id="objectives">𝕆bjectives</h2>

> - Comprendre une ligne de regex
> - Savoir ecrire une ligne de regex

- [🗓 𝕊ummary](#summary)
<br>

---

<br>

<h2 id="learningprogression">🕑 𝕃earning ℙrogression</h2>


<details>
<summary><strong>Debut de phrase</strong></summary>

>>- `'^'`
>>>Qui commence part "word": `'^word'`

</details>

---

<details>
<summary><strong>Fin de phrase</strong></summary>
>>- `'$'`
>>>Qui fini part "word": `'word$'`

</details>

---

<details>
<summary><strong>Exp debut + fin</strong></summary>
>>Commence part `'word1'` avec un space entre les 2 `' '` plus fini part `'1word'`:
>>>- `'^word1'` + `' '` + `'1word$'`
>>>- `'^word1 1word$'` recherche `'word1 1word'`

</details>

---

<details>
<summary><strong>Les Alternation / Parenthèses</strong></summary>
>>- `'(…|…)'`
>>>Qui a `'oui'` ou `'non'` au debut:
>>>`'^(oui|non)'`

</details>

---

<details>
<summary><strong>Exp debut + fin + alternation</strong></summary>

>>Commence part `'word1 '` avec un mots qui est soit `'oui'`/`'non'` puis fini part `' 1word'`:
>>>- `'^word1 '` + `'(oui|non)'` + `' 1word$'`
>>>- `'^word1 (oui|non) 1word$'` recherche `'word1 oui 1word'`/`'word1 non 1word'`

</details>

---

<details>
<summary><strong>Quantificateur</strong></summary>

>>- `?` (0 ou 1 fois)
>>- `*` (0 plusiseur fois)
>>- `+` (1 plusiseur fois)
>>>- ab+ le + s’applique uniquement à b
>>>- (ab)+ le + s’applique au groupe "ab"
>>>- `'1?'`: `''` / `'1'`
>>>- `'(12)*'`: `''`, `'12'`, `'1212'`, `'121212'`, `'12121212'`, …
>>>- `'12+'`: `'12'`, `'122'`, `'1222'`, `'1222'`, …
>
>>- `{N}` (N fois)
>>- `{N,}` (au minimum N fois)
>>- `{N, I}` (entre N et I fois)
>>>- `'n{2}'`: `'nn'` 
>>>- `'n{2,}'`: `'nn'` `'nnnn'` `'nnnnn'` …
>>>- `'n{2,4}'`: `'nn'` `'nnn'` `'nnnn'`
>>- . tout charactère sauf le \n

</details>

---

<details>
<summary><strong>Class</strong></summary>

>>- `'[abcd]'`: `'a'`, `'b'`, `'c'`, `'d'`
>>- `'[a-d]'`: `'a'`, `'b'`, `'c'`, `'d'`
>>- `'^[a-z]+$'` accepte seulement un chaine de charactère minuscule
>
>Ce métacharactère `'^'` est utiliser pour inverse la class exemple:
>>- `'^[^a-z]+$'` accepte une string de tout sauf les charactère de 'a' à 'z' 
>>- `'[^a-zA-Z]'` accepte seulement un charactère non alpha

</details>

---

- [🗓 𝕊ummary](#summary)
<br>

---

<br>

<h2 id="requirements">🛠 ℝequirements</h2>

>Navitageur pour utiliser quelque site
>>- [regexr][Tag-requirements-regexr]
>>- [regex101][Tag-requirements-regex101]
>
>Un terminal pour faire des rechercher regex avec grep
>Un language avec une lib(ou non) regex exp python(`import re`) c(`#include <regex.h>`) js(pas d'import requis)
>il faut faire attention a certain langague ne sont pas forcement compatibil avec la norme regex

- [🗓 𝕊ummary](#summary)
<br>

---

<br>

<h2 id="resources">ℝesources</h2>

>- [Une video de jason champagne/fromation video/evolunoob][Tag_video_jason]
>- [Le markdown de la meme personne][Tag_github_jason]

- [🗓 𝕊ummary](#summary)
<br>

---

<br>

<h2 id="author">🖋 𝔸uthor</h2>

All implementation decisions and documentation were written and validated by the project author.


<br>

---

<br>

- [🗓 𝕊ummary](#summary)