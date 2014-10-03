

# Polymer

> Le web de demain, aujourd'hui

---

Wikipedia.org: Polymer
> du grec polus, plusieurs, et meros, partie

---

## Objectif:
Élément HTML sur mesure

## Moyen:
Librairie( Web Components )

---

# Web Components ?

* Template natifs
* object.observe
* shadow dom
* html import
* custom element

---

# Concepts importants( Web Components )

* Tout peut être un element, visuel ou non
* css non invasif par défaut
* les évènements ne sont pas mort

---

# Polymer Vs. Web components

* Polyfill
* lib de "simplification"

---

# Polymer Vs. Angular.js

    Polymer = Directive( Angular.js) - Angular.js

---

# Elements non visuel

 * appel ajax
 * local-storage
 * routeur de page
 * back end complet


---

# Un aire d'élément (ou l'inverse)

    polymer-element(name="code3-aire-text", noscript, \attributes="longueur, largeur")
      template
        {{longueur * largeur}}

---

# Change d'aire

    polymer-element(name="code3-aire-valeur", noscript, \attributes="longueur, largeur, aire")
      script.
        Polymer({
          longueurChanged:function(){
            computeAire()
          },
          longueurChanged:function(){
            computeAir()
          },
          computeAire:function(){
            this.aire = this.largueur * this.longueur;
          }
        })

---

# Exemple d'appel ajax declaratif

    polymer-element(name="code3-auto-save-form", noscript)
      template
        core-ajax(url="/api/run", method="POST", auto, params="{{ run }}")
        form
          core-field
            label Date
            core-input(value="{{run.date}}", type="date")
          core-field
            label Distance
            core-input(value="{{run.distance}}", type="number")

---

# T'as l'air différent

    polymer-element(name="code3-button", noscript, \attributes="color, text")
      template
        button {{text}}
      style
        button {
          background-color: {{ color }};
       }

---

# Ca manque de logique tout ça !!

    polymer-element(name="code3-click-counter")
      template
        button(label="click me", on-click="{{inc}}")
        label Nombre de click
          span#counterView

      script.
        Polymer({
          counter:0,
          inc:function(){
            counter++
            this.$.counterView.innerHtml = counter
          }
        })


---

# Un aire *import* ant

    head
      link(rel="import", href="bower-components/code3-button/code3-button.html")

---

# Mes outils marchent encore ?


---

Option dev tools

<img src="print-screen/devtools-options.png"/>

---

Propriété d'éléments

<img src="print-screen/element-properties.png"/>
---

Inspection d'élément

<img src="print-screen/shadow-dom-inspect.png"/>

---

Inspection css

<img src="print-screen/shadow-dom-css-inspection.png"/>

---

Ok ca marche dans chrome, mais les autres ?

http://www.polymer-project.org/resources/compatibility.html

<img src="print-screen/compatibility-matrix.png"/>

---

# Alternatives à Polymer

* Api natives
* Firefox *x-tag* [xtags.org](xtags.org)
* Bosonic [bosonic.github.com](bosonic.github.com)

---

# Ressources

* Liste de web components: http://webcomponents.org/
* Polymer: http://polymer-project.org

---

[benzen.github.io](https://benzen.github.io)

[benjamin.dreux@code3.ca](mailto:benjamin.dreux@code3.ca)

[@BenjaminDreux](https://twitter.com/BenjaminDreux)

---
