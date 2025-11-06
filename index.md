---
title: Pagina Principale del Blog
# Puoi rimuovere feature_text e feature_image se non li vuoi
# Se vuoi l'immagine "Hero" in cima come sciauerta.it, mantienile e cambia i valori
feature_text: |
  ## Benvenuto nel Blog
  Scegli l'area tematica che preferisci per iniziare la lettura dei nostri approfondimenti.
feature_image: "/assets/images/header-blog.jpg" 
excerpt: "Qui troverai i nostri articoli suddivisi in tre aree tematiche principali."
---

<div class="container content landing-page">
    <section class="intro-block">
        <p>Il nostro blog è strutturato per offrirti contenuti chiari e ben organizzati.</p>
    </section>

    <section class="category-grid">
        {% for cat in site.my_categories %}
        <div class="category-card">
            <h2>{{ cat.name }}</h2>
            <p>{{ cat.description }}</p>
            <a href="{{ cat.slug | relative_url }}/" class="button primary">Esplora {{ cat.name }} &rarr;</a>
        </div>
        {% endfor %}
    </section>
</div>