Data and analysis for *Einheitlich oder divers…*
================
Johannes Titz, Annika Sternkopf, Toni Zapke

This repository accompanies the paper Sternkopf, Lungwitz, Zapke, &
Titz. *Einheitlich oder divers: Die Methodenlehre im
Bachelor-Psychologiestudium an deutschen Universitäten*

## preparation

I use librarian for library management, please install or modify to use
library

``` r
librarian::shelf(plot.matrix, reshape2, knitr)
```

## use of stats software

``` r
software <- read.csv2("software.csv")

kable(sort(colSums(software[, -1], na.rm = T), decreasing = T))
```

|         |   x |
|:--------|----:|
| R       |  32 |
| SPSS    |  11 |
| JASP    |   8 |
| Jamovi  |   5 |
| MATLAB  |   4 |
| SYSTAT  |   1 |
| JMP     |   0 |
| Minitab |   0 |
| NumPy   |   0 |
| S_Plus  |   0 |
| Stata   |   0 |

## topics covered

table 1

``` r
d <- read.csv2("topics.csv", row.names = 1)
row.names(d)[1] <- "Anonym"
d <- d[, order(names(d))]
kable(sort(colSums(d), decreasing = T))
```

|                                                                                                        |   x |
|:-------------------------------------------------------------------------------------------------------|----:|
| ANOVA_unabhängig_Ba_Vl                                                                                 |  34 |
| Einfache_lineare_RegressionBa_Vl                                                                       |  34 |
| Grundlagen_EffektgrößenBa_Vl                                                                           |  34 |
| KonfidenzintervalleBa_Vl                                                                               |  34 |
| Lage_amp_StreuungsmaßeBa_Vl                                                                            |  34 |
| Messen_amp_Testen_SkalenniveausBa_Vl                                                                   |  34 |
| PoweranalyseBa_Vl                                                                                      |  34 |
| t_Test_abhängig_Ba_Vl                                                                                  |  34 |
| t_Test_unabhängig_Ba_Vl                                                                                |  34 |
| Experimentelle_DesignsBa_Vl                                                                            |  33 |
| Grundlagen_der_Inferenzstatistik_Wahrscheinlichkeitstheorie_Verteilungen_Ba_Vl                         |  33 |
| Grundlagen_SignifikanztestsBa_Vl                                                                       |  33 |
| KorrelationBa_Vl                                                                                       |  33 |
| Messen_amp_Testen_GütekriterienBa_Vl                                                                   |  32 |
| AlltagspsychologievswissenschaftlichePsychologieErklärungwissenschaftlicheMethodeBaVl                  |  30 |
| ANOVA_abhängig_Ba_Vl                                                                                   |  30 |
| WissenschaftstheorieBa_Vl                                                                              |  30 |
| Messen_amp_Testen_Messtheorie_Repräsentationsproblem_Eindeutigkeitsproblem_Bedeutsamkeitsproblem_Ba_Vl |  29 |
| nonparametrisch_Chi_Quadrat_TestBa_Vl                                                                  |  29 |
| PartialkorrelationBa_Vl                                                                                |  29 |
| Probleme.Limitationen_der_klassischen_Inferenzstatistik_Ba_Vl                                          |  29 |
| Multiple_lineare_RegressionBa_Vl                                                                       |  28 |
| Open_Science_Replikation_Ba_Vl                                                                         |  28 |
| BefragungBa_Vl                                                                                         |  26 |
| Algemeines_lineares_Modell_ALM_Ba_Vl                                                                   |  25 |
| ANOVA_mixed_Ba_Vl                                                                                      |  25 |
| Explorative_Datenanalyse_grafische_Darstellung_Ba_Vl                                                   |  25 |
| Rechenregeln_für_Erwartungswert_Varianz_amp_KovarianzBa_Vl                                             |  25 |
| BeobachtungBa_Vl                                                                                       |  24 |
| KontrastanalyseBa_Vl                                                                                   |  22 |
| nonparametrisch_Wilcoxon_TestBa_Vl                                                                     |  22 |
| KovarianzanalyseBa_Vl                                                                                  |  21 |
| nonparametrisch_U_TestBa_Vl                                                                            |  21 |
| ModeratoranalyseBa_Vl                                                                                  |  18 |
| FaktorenanalyseBa_Vl                                                                                   |  17 |
| nonparametrisch_McNemar_TestBa_Vl                                                                      |  16 |
| Bayesianische_StatistikBa_Vl                                                                           |  13 |
| Verfälschte_StichprobenBa_Vl                                                                           |  12 |
| MediatoranalyseBa_Vl                                                                                   |  11 |
| nonparametrisch_weitere_Tests_bitte_im_Freifeld_unten_spezifizieren_Ba_Vl                              |  11 |
| logistische_RegressionBa_Vl                                                                            |  10 |
| qualitative_MethodenBa_Vl                                                                              |  10 |
| MetaanalyseBa_Vl                                                                                       |   8 |
| Umgang_mit_fehlenden_Werten_missing_values_Ba_Vl                                                       |   8 |
| Resampling_VerfahrenBa_Vl                                                                              |   7 |
| ComputermodellierungBa_Vl                                                                              |   5 |
| MANOVABa_Vl                                                                                            |   5 |
| MehrebenenanalyseBa_Vl                                                                                 |   5 |
| PfadanalyseBa_Vl                                                                                       |   5 |
| Rechnen_mit_MatritzenBa_Vl                                                                             |   5 |
| ClusteranalyseBa_Vl                                                                                    |   4 |
| experimentelle_EinzelfallanalyseBa_Vl                                                                  |   3 |
| Randomized_ResponseBa_Vl                                                                               |   3 |
| StrukturgleichungsmodelleBa_Vl                                                                         |   3 |
| ConjointanalyseBa_Vl                                                                                   |   0 |
| DiskriminanzanalyseBa_Vl                                                                               |   0 |
| multidimensionale_SkalierungBa_Vl                                                                      |   0 |

## distance matrix

``` r
# all pairs for comparisons
pairs <- expand.grid(rownames(d), rownames(d))

# find all 01 patterns (row 0, col 1)
comps <- unlist(Map(\(x, y) table(paste0(d[x, ], d[y, ]))["01"],
                    pairs[, 1],
                    pairs[, 2]))

pairs <- cbind(pairs, value = comps)
pairs[is.na(pairs)] <- 0

# reshape into matrix
mtrx <- acast(pairs, Var1 ~ Var2, value.var = "value")
```

make function for plot for different formats:

``` r
theplot <- function() {
  par(mar=c(5.1, 5.1, 0.5, 0.5)*4.1)
  plot(
       mtrx,
       fmt.cell = "%.0f",
       main = "",
       xlab = "",
       ylab = "",
       key = NULL,
       #col = gray.colors(10, start = 0, end = 1),
       col = RColorBrewer::brewer.pal(max(mtrx), "Greys"),
       na.col = "black",
       axis.col = list(side=1, las=2),
       axis.row = list(side=2, las=1)
  )
}
```

save plots:

``` r
png("distances.png", width = 15*65, height = 15*65)
theplot()
```

    ## Warning in RColorBrewer::brewer.pal(max(mtrx), "Greys"): n too large, allowed maximum for palette Greys is 9
    ## Returning the palette you asked for with that many colors

``` r
dev.off()
```

    ## png 
    ##   2

``` r
setEPS()
postscript("distances.eps", width = 15*0.9, height = 15*0.9)
theplot()
```

    ## Warning in RColorBrewer::brewer.pal(max(mtrx), "Greys"): n too large, allowed maximum for palette Greys is 9
    ## Returning the palette you asked for with that many colors

``` r
dev.off()
```

    ## png 
    ##   2

plot:

![](distances.png)
