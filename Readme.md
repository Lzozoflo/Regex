*This project has been created by Florent Cretin.*
<!-- Ceci sont des commentaire pour avec mes font et mes icon personnaliser -->
<!-- 𝔸 𝔹 ℂ 𝔻 𝔼 𝔽 𝔾 ℍ 𝔾 𝕁 𝕂 𝕃 𝕄 ℕ 𝕆 ℙ ℚ ℝ 𝕊 𝕋 𝕌 𝕍 𝕎 𝕏 𝕐 ℤ -->
<!-- 𝕒 𝕓 𝕔 𝕕 𝕖 𝕗 𝕘 𝕙 𝕚 𝕛 𝕜 𝕝 𝕞 𝕟 𝕠 𝕡 𝕢 𝕣 𝕤 𝕥 𝕦 𝕧 𝕨 𝕩 𝕪 𝕫  -->
<!-- 𝟘 𝟙 𝟚 𝟛 𝟜 𝟝 𝟞 𝟟 𝟠 𝟡 -->
<!-- 🗎 🖋 👀 🗣 … -->
<!-- Double-struck font -->
<!-- 𝔸𝔹ℂ𝔻𝔼𝔽𝔾ℍ𝕀𝕁𝕂𝕃𝕄ℕ𝕆ℙℚℝ𝕊𝕋𝕌𝕍𝕎𝕏𝕐ℤ𝕒𝕓𝕔𝕕𝕖𝕗𝕘𝕙𝕚𝕛𝕜𝕝𝕞𝕟𝕠𝕡𝕢𝕣𝕤𝕥𝕦𝕧𝕨𝕩𝕪𝕫𝟘𝟙𝟚𝟛𝟜𝟝𝟞𝟟𝟠𝟡 -->


<!-- [Tag-test]: url -->
[Tag_video_jason]: https://www.youtube.com/watch?v=f3QwwnvSQ50
[Tag_github_jason]: https://github.com/jasonchampagne/FormationVideo/blob/master/Ressources/Aide/expressions-rationnelles.md

[Tag-requirements-regexr]: https://regexr.com/
[Tag-requirements-regex101]: https://regex101.com/

# Regex

<span style="color: red;">Texte rouge</span>
<span style="color: #4CAF50;">Texte vert</span>
<span style="color: rgb(255, 165, 0);">Texte orange</span>
![Status](https://img.shields.io/badge/STATUS-IN%20PROGRESS-yellow)

<details>
<summary>
    <strong id="summary">🗓 𝕊ummary</strong>
</summary>

- [𝔻escription](#description)
- [𝕆bjectives](#objectives)
- [🕑 𝕃earning ℙrogression](#learningprogression)
- [🛠 ℝequirements](#requirements)
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
<summary id="microsummary" ><strong><em>Micro summary</em></strong></summary>

- [Debut de phrase](#debutphrase)
- [Fin de phrase](#finphrase)
- [Exemple debut + fin](#exdebutfin)
- [Les Alternation / Parenthèses](#alteranationparen)
- [Exemple debut + fin + alternation](#exdebutfinalternation)
- [Quantificateur](#quantificateur)
- [Class](#class)

</details>

---

<details>
<summary><strong id="debutphrase">Debut de phrase</strong></summary>

>- `'^'`
>>Qui commence part "word": `'^word'`

- [Micro Summary](#microsummary)

</details>

---

<details>
<summary><strong id="finphrase">Fin de phrase</strong></summary>

>- `'$'`
>>Qui fini part "word": `'word$'`


- [Micro Summary](#microsummary)

</details>

---

<details>
<summary><strong id="exdebutfin">Exemple debut + fin</strong></summary>

>Commence part `'word1'` avec un space entre les 2 `' '` plus fini part `'1word'`:
>>- `'^word1'` + `' '` + `'1word$'`
>>- `'^word1 1word$'` recherche `'word1 1word'`


- [Micro Summary](#microsummary)

</details>

---

<details>
<summary><strong id="alteranationparen">Les Alternation / Parenthèses</strong></summary>

>- `'(…|…)'`
>>Qui a `'oui'` ou `'non'` au debut:
>>`'^(oui|non)'`


- [Micro Summary](#microsummary)

</details>

---

<details>
<summary><strong id="exdebutfinalternation">Exemple debut + fin + alternation</strong></summary>

>Commence part `'word1 '` avec un mots qui est soit `'oui'`/`'non'` puis fini part `' 1word'`:
>>- `'^word1 '` + `'(oui|non)'` + `' 1word$'`
>>- `'^word1 (oui|non) 1word$'` recherche `'word1 oui 1word'`/`'word1 non 1word'`


- [Micro Summary](#microsummary)

</details>

---

<details>
<summary><strong id="quantificateur">Quantificateur</strong></summary>

>- `?` (0 ou 1 fois)
>- `*` (0 plusieur fois)
>- `+` (1 plusieur fois)
>>- ab+ le + s’applique uniquement à b
>>- (ab)+ le + s’applique au groupe "ab"
>>- `'1?'`: `''` / `'1'`
>>- `'(12)*'`: `''`, `'12'`, `'1212'`, `'121212'`, `'12121212'`, …
>>- `'12+'`: `'12'`, `'122'`, `'1222'`, `'1222'`, …
>
>- `{N}` (N fois)
>- `{N,}` (au minimum N fois)
>- `{N, I}` (entre N et I fois)
>>- `'n{2}'`: `'nn'` 
>>- `'n{2,}'`: `'nn'` `'nnnn'` `'nnnnn'` …
>>- `'n{2,4}'`: `'nn'` `'nnn'` `'nnnn'`
>- . tout charactère sauf le \n


- [Micro Summary](#microsummary)

</details>

---

<details>
<summary><strong id="class">Class</strong></summary>

>- `'[abcd]'`: `'a'`, `'b'`, `'c'`, `'d'`
>- `'[a-d]'`: `'a'`, `'b'`, `'c'`, `'d'`
>- `'^[a-z]+$'` accepte seulement un chaine de charactère minuscule
>
>Ce métacharactère `'^'` est utiliser pour inverse la class exemple:
>- `'^[^a-z]+$'` accepte une string de tout sauf les charactère de 'a' à 'z' 
>- `'[^a-zA-Z]'` accepte seulement un charactère non alpha


- [Micro Summary](#microsummary)

</details>

---

- [🗓 𝕊ummary](#summary)
<br>

---

<br>

<h2 id="requirements">🛠 ℝequirements</h2>

>Navitageur pour utiliser quelque site
>- [regexr][Tag-requirements-regexr]
>- [regex101][Tag-requirements-regex101]
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