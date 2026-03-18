---
layout: page
title: Chromatin Feature Scatterplot Explorer
subtitle: Explore the relationship between gene features and chromatin features in *Arabidopsis thaliana*
full-width: true
---

<div style="max-width: 860px; margin: 0 auto 1.5rem;">
<p style="color:#555; font-size:0.95rem; margin:0;">
  Select a <strong>gene region</strong> (whole gene, exons, or introns), a <strong>gene feature</strong> (e.g., intron number, gene length), and a <strong>chromatin feature</strong> (e.g., H3K36me3, ATAC) to view scatterplots showing the mean chromatin feature signal across intron architecture quantile bins. Data from <a href="https://www.biorxiv.org/content/10.1101/2025.10.15.682614v1.full" target="_blank">Pierce et al. 2025</a>.
</p>
</div>

<div class="shiny-embed-wrap">
  <iframe
    src="https://019cfe48-7a85-83ce-bf7b-0bb2f22d9e34.share.connect.posit.cloud/"
    title="Gene × Chromatin Feature Explorer — interactive scatterplot app"
    allowfullscreen>
  </iframe>
</div>

<p style="font-size:0.82rem; color:#aaa; text-align:center; margin-top:0.5rem;">
  Built with <a href="https://shiny.posit.co/" target="_blank">R Shiny</a> &amp; <a href="https://ggplot2.tidyverse.org/" target="_blank">ggplot2</a> · Pierce et al. 2025 ·
  <a href="https://github.com/AlicePierce/IntronArchitecture" target="_blank">View code on GitHub</a>
</p>
