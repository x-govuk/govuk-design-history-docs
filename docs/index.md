---
homepage: true
layout: product
includeInBreadcrumbs: true
title: A design history for your GOV.UK service
description: Document and share design decisions. Create a permanent record of how your service has developed over time.
image:
  src: /assets/homepage-illustration.svg
  alt: Eleventy’s possum mascot hanging on a red balloon and floating above a laptop.
startButton:
  href: /get-started
---
<div class="govuk-grid-row">
{% for item in collections["homepage"] | reverse %}
  <section class="govuk-grid-column-one-half-from-desktop govuk-!-margin-bottom-8">
    <h2 class="govuk-heading-m govuk-!-font-size-27">{{ item.data.title | smart }}</h2>
    <p class="govuk-body">{{ item.data.description | markdown("inline") }}</p>
    <p class="govuk-body"><a class="govuk-link govuk-!-font-weight-bold" href="{{ item.url | url }}">{{ item.data.linkText }}</a></p>
  </section>
{% endfor %}
  <section class="govuk-grid-column-full">
    <hr class="govuk-section-break govuk-section-break--visible govuk-section-break--xl govuk-!-margin-top-0">
    <h2 class="govuk-heading-m govuk-!-font-size-27">Contribute</h2>
    <p class="govuk-body">This project is public and contributions are welcome from anyone.</p>
    <p class="govuk-body"><a class="govuk-link govuk-!-font-weight-bold" href="https://github.com/x-govuk/govuk-design-history-template">View this project on GitHub</a></p>
  </section>
</div>
