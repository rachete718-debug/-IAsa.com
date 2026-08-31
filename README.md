
bash

cd /home/claude/iasa && python3 << 'PYEOF'
import json
parts = json.load(open('/tmp/parts.json'))

head = parts['head_top'].format(
    desc="IASA — Tarifs détaillés pour la création de sites web, les vidéos UGC IA et le montage vidéo. Devis gratuit sous 24h.",
    title="Tarifs — IASA Agence Créative & Digitale"
) + parts['style_block'] + '\n'

nav = parts['nav_common'].format(tarifs_active=' class="active-link"', apropos_active='')

content = '''
<section id="page-hero" style="padding-top:150px;">
  <div class="sec-head reveal">
    <div>
      <div class="sec-tag mono">TARIFICATION</div>
      <div class="sec-title">Une tarification claire, sans surprise</div>
    </div>
    <p class="sec-desc">Trois expertises, des tarifs de départ transparents, et le détail complet de chaque prestation ci-dessous. Devis précis en moins de 24h.</p>
  </div>
</section>

<section style="padding-top:0;">
  <div class="offers-grid">
    <div class="offer-card reveal">
      <div class="offer-name mono">MONTAGE VIDÉO</div>
      <div class="offer-price">25$<span> à partir de</span></div>
      <div class="offer-sub">Montage dynamique pour réseaux sociaux et publicités.</div>
      <ul class="offer-list">
        <li>Cuts rythmés + sous-titres animés</li>
        <li>1 format livré (Reels, TikTok ou Shorts)</li>
        <li>1 révision incluse</li>
        <li>Livraison sous 3 à 5 jours</li>
      </ul>
      <a href="https://wa.me/243835526603?text=Bonjour%20IASA%2C%20je%20suis%20int%C3%A9ress%C3%A9%28e%29%20par%20l%27offre%20Montage%20vid%C3%A9o." class="offer-cta" target="_blank" rel="noopener">Choisir cette offre</a>
    </div>
    <div class="offer-card featured reveal">
      <div class="offer-badge">Populaire</div>
      <div class="offer-name mono">VIDÉOS UGC IA</div>
      <div class="offer-price">50$<span> à partir de</span></div>
      <div class="offer-sub">Avatars IA, voix IA et scénario sur mesure pour votre marque.</div>
      <ul class="offer-list">
        <li>Avatar + voix IA au choix</li>
        <li>Scénario adapté à votre produit</li>
        <li>Sous-titres animés inclus</li>
        <li>2 révisions incluses</li>
      </ul>
      <a href="https://wa.me/243835526603?text=Bonjour%20IASA%2C%20je%20suis%20int%C3%A9ress%C3%A9%28e%29%20par%20l%27offre%20Vid%C3%A9os%20UGC%20IA." class="offer-cta" target="_blank" rel="noopener">Choisir cette offre</a>
    </div>
    <div class="offer-card reveal">
      <div class="offer-name mono">SITES WEB</div>
      <div class="offer-price">150$<span> à partir de</span></div>
      <div class="offer-sub">Site vitrine moderne, rapide et pensé pour convertir.</div>
      <ul class="offer-list">
        <li>Design sur mesure &amp; responsive</li>
        <li>Bouton WhatsApp intégré</li>
        <li>Formulaire de contact</li>
        <li>Optimisation performance</li>
      </ul>
      <a href="https://wa.me/243835526603?text=Bonjour%20IASA%2C%20je%20suis%20int%C3%A9ress%C3%A9%28e%29%20par%20un%20site%20web." class="offer-cta" target="_blank" rel="noopener">Choisir cette offre</a>
    </div>
  </div>

  <div class="price-table reveal" style="margin-top:56px;">
    <div class="price-row head"><div>Prestation</div><div>Tarif</div><div>Détail</div></div>
    <div class="price-group-label mono">🎬 MONTAGE VIDÉO</div>
    <div class="price-row"><div class="pr-name">Vidéos courtes (&lt; 30s)</div><div class="pr-price">Dès 15$</div><div class="pr-note">Retouche simple, format unique, sous-titres.</div></div>
    <div class="price-row"><div class="pr-name">Reels / TikTok / Shorts</div><div class="pr-price">Dès 25$</div><div class="pr-note">Cuts rythmés, habillage et sous-titres animés.</div></div>
    <div class="price-row"><div class="pr-name">YouTube (long format)</div><div class="pr-price">Dès 90$</div><div class="pr-note">Montage complet 5 à 15 minutes.</div></div>
    <div class="price-group-label mono">🎥 VIDÉOS UGC IA</div>
    <div class="price-row"><div class="pr-name">Avatar + voix IA</div><div class="pr-price">Dès 50$</div><div class="pr-note">Scénario sur mesure, sous-titres animés inclus.</div></div>
    <div class="price-row"><div class="pr-name">Vlogs IA</div><div class="pr-price">Dès 70$</div><div class="pr-note">Format long, plusieurs scènes, narration IA.</div></div>
    <div class="price-group-label mono">💻 SITES WEB</div>
    <div class="price-row"><div class="pr-name">Site vitrine</div><div class="pr-price">Dès 150$</div><div class="pr-note">Vitrine responsive, WhatsApp &amp; formulaire intégrés.</div></div>
    <div class="price-row"><div class="pr-name">Solutions business avancées</div><div class="pr-price">Sur devis</div><div class="pr-note">Automatisation, IA, réservation, intégrations — projets pouvant atteindre 1000$ et plus selon les fonctionnalités.</div></div>
  </div>
</section>

<section>
  <div class="sec-head reveal">
    <div>
      <div class="sec-tag mono">À SAVOIR</div>
      <div class="sec-title">Ce qui est inclus dans chaque tarif</div>
    </div>
  </div>
  <div class="stat-bar reveal">
    <div class="stat-item"><span class="stat-ic">⚡</span><div><b>&lt; 24h</b><span>Temps de réponse</span></div></div>
    <div class="stat-item"><span class="stat-ic">🎯</span><div><b>3 expertises</b><span>Web · UGC IA · Vidéo</span></div></div>
    <div class="stat-item"><span class="stat-ic">🛠️</span><div><b>100%</b><span>Projets suivis de A à Z</span></div></div>
    <div class="stat-item"><span class="stat-ic">💬</span><div><b>Gratuit</b><span>Premier devis</span></div></div>
  </div>
</section>

<section>
  <div class="cta-banner reveal">
    <div class="sec-tag mono" style="justify-content:center;">VOTRE PROJET</div>
    <h2>Une question sur un tarif ? <span class="grad-text">Écrivez-nous directement.</span></h2>
    <p>Décrivez votre besoin et recevez un devis précis, adapté à votre projet, en moins de 24h.</p>
    <div class="cta-actions">
      <a href="https://wa.me/243835526603?text=Bonjour%20IASA%2C%20j%27ai%20une%20question%20sur%20vos%20tarifs." class="btn-primary" target="_blank" rel="noopener">Discuter de mon projet</a>
      <a href="apropos.html" class="btn-ghost">En savoir plus sur IASA</a>
    </div>
  </div>
</section>
'''

html = head + nav + content + parts['footer_common'] + parts['script_common']
open('tarifs.html', 'w').write(html)
print("tarifs.html written:", len(html))
PYEOF
Sortie

tarifs.html written: 57953
