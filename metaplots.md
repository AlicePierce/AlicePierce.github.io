---
layout: page
title: Chromatin Feature Distribution Explorer
subtitle: Explore the distribution of chromatin features binned by gene architecture in *Arabidopsis thaliana*
full-width: true
---

<div style="max-width: 860px; margin: 0 auto 1.5rem;">
<p style="color:#555; font-size:0.95rem; margin:0;">
  Select a <strong>gene feature</strong> (e.g., intron number, first intron position) and a <strong>chromatin feature</strong> (e.g., ATAC, H3K36me3) to view metaplots showing the average distribution of chromatin marks 3kb upstream and downstream the TSS, grouped by quantile bins of the selected gene feature. Data from <a href="https://www.biorxiv.org/content/10.1101/2025.10.15.682614v1.full" target="_blank">Pierce et al. 2025</a>.
</p>
</div>

<div class="shiny-embed-wrap">
  <iframe
    src="https://019cfe39-f92b-1309-1542-44776b7fd7cc.share.connect.posit.cloud/"
    title="Chromatin Feature Explorer — interactive metaplot app"
    allowfullscreen>
  </iframe>
</div>

<p style="font-size:0.82rem; color:#aaa; text-align:center; margin-top:0.5rem;">
  Built with <a href="https://shiny.posit.co/" target="_blank">R Shiny</a> &amp; <a href="https://ggplot2.tidyverse.org/" target="_blank">ggplot2</a> · Pierce et al. 2025 ·
  <a href="https://github.com/AlicePierce/IntronArchitecture" target="_blank">View code on GitHub</a>
</p>
