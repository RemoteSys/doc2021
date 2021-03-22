---
# ANOVA - workflow




1. `data` - *dict*, {czynnik1: [...], czynnik2: [...], wyniki: [....])
2. `sr` - *float*, średnia ogólna ($\bar{x}$)

---

# Obliczenia wspólne

1. `zakres`: *dict*, {grupa1: (start,stop), grupa2: (start,stop), ... }

    > wyznaczenie zakresów indeksów dzielących dane na grupy wg wybranego czynnika


2. `srGr` - *dict*, {grupa1: (nj, sri), grupa2: (nj, sri), ... }

    >liczności i średnie w grupach  ($\bar{x_j}$)




# `MSA` średnia z sumy kwadratów (`SSA`)
  
1. `ssa_i` - *dict*, {grupa1: ssa_i, grupa2: ssa_i, ... }

    $$ssa_i = n_j \cdot(\bar{x_j}-\bar{x})^2$$

    >kwadraty odchyleń średnich grupowych od średniej ogólnej ogólnej

2. `ssa` - *float*

      $$ssa = \sum_{j=1}^p  ssa_i$$

    >suma kwadratów odchyleń średnich grupowych od średniej ogólnej


3.  `msa` - *float*, 

    $$msa = \frac{ssa}{p-1}$$

    >uśredniona wartość sumy kwadratów SSA

---

#  `MSR` średnia z sumy kwadratów `SSR`

1. `ssr_i` - *dict*, 

    $$ssr_i=\sum_{ij=1}^{n_j} (x_{ij}-\bar{x_j})^2$$

    >sumy kwadratów różnic wyników i średniej w grupach
    
2. '`ssr` - *float*

    $$ssr = \sum_{j=1}^p ssr_i$$

    >suma $ssr_i$ z wszystkich *p* grup

3. `msr` - *float*

    $$msr = \frac{ssr}{n-p}$$

---

# Statystyka `F`

$$F = \frac{msa}{msr}$$












