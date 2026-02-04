# migrant-nocturnality

Estimating the proportion of European migratory birds that migrate by day vs. by night vs. both.

## Procedure overview

1. **Compile life-history traits.** Start with the Storchova & Horak dataset of life-history characteristics for European birds, and retain the columns that identify facultative, short-distance, and long-distance migrants. These are used to flag species as migratory.  
2. **Add population estimates.** Join the life-history table to population estimates from the European bird population dataset (OPS EU28), keeping the latest year per species and reconciling any taxonomic name updates so that datasets align.  
3. **Classify nocturnality.** Manually classify each species as nocturnal, diurnal, or both based on limited literature research and field experience (stored in `species_list_nocturnality.xlsx`).  
4. **Filter to migratory species.** Keep species that are migratory and have a nocturnality classification.  
5. **Summarize totals and proportions.** Sum population totals within each migration type (nocturnal, diurnal, both), then compute proportions relative to the overall migratory total.  
6. **Visualize.** Plot the distribution of migratory birds by migration time of day and export the figure to `nocturnality.pdf`.

## Data sources

* **Life-history traits:** Storchova & Horak dataset (European birds).  
* **Population estimates:** OPS EU28 population dataset (latest year per species).  
* **Nocturnality classification:** Manual classification based on literature review and field experience.
