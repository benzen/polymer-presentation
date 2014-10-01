

# Polymer

> Le web de demain, aujourd'hui

---

Wikipedia.org: Polymer
> du grec polus, plusieurs, et meros, partie

---

Création d'élément HTML sur mesure

---

# Web componnets ?

* Template natifs
* object.observe
* shadow dom

---

# Concepts importants

* Tout peut être un element, visuel ou non
* css non invasif par défaut
* les évènements existent encore

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
 * page router
 * back end complet
 * local-storage

---

# Un aire d'élément (ou l'inverse)

    polymer-element(name="code3-aire", noscript, \attributes="longueur, largeur")
      template
        {{longueur * largeur}}

---

# Change d'aire

    polymer-element(name="code3-aire", noscript, \attributes="longueur, largeur, aire")
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

# Alternatives à Polymer
Firefox *x-tag*

---

# Ressources

Liste de web components: http://webcomponents.org/
Polymer: http://polymer-project.org

---
