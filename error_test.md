```
reference:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_abstract var_x brack_close

test:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_manufacturer var_x brack_close

```
ref:dbo_abstract</br>
test:dbo_manufacturer</br>

----

```
reference:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_abstract var_x brack_close

test:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_manufacturer var_x brack_close

```
ref:dbo_abstract</br>
test:dbo_manufacturer</br>

----

```
reference:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_binomialAuthority var_x brack_close

test:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_binomialAuthority var_x brack_close

```
ref:dbo_species</br>
test:dbo_binomialAuthority</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_binomialAuthority var_x brack_close

test:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_binomialAuthority var_x brack_close

```
ref:dbo_species</br>
test:dbo_binomialAuthority</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_binomialAuthority var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_binomialAuthority var_x brack_close

```
ref:dbo_species</br>
test:dbo_binomialAuthority</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_binomialAuthority var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_binomialAuthority var_x brack_close

```
ref:dbo_species</br>
test:dbo_binomialAuthority</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_class var_x brack_close

test:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_budget var_x brack_close

```
ref:dbo_class</br>
test:dbo_budget</br>

----

```
reference:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_class var_x brack_close

test:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_distributor var_x brack_close

```
ref:dbo_class</br>
test:dbo_distributor</br>

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_class var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_voice var_x brack_close

```
ref:dbo_class</br>
test:dbo_voice</br>

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_class var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_voice var_x brack_close

```
ref:dbo_class</br>
test:dbo_voice</br>

----

```
reference:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_conservationStatus var_x brack_close

test:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_conservationStatus var_x brack_close

```
ref:dbo_species</br>
test:dbo_conservationStatus</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_conservationStatus var_x brack_close

test:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_conservationStatus var_x brack_close

```
ref:dbo_species</br>
test:dbo_conservationStatus</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_conservationStatus var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_conservationStatus var_x brack_close

```
ref:dbo_species</br>
test:dbo_conservationStatus</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_conservationStatus var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_conservationStatus var_x brack_close

```
ref:dbo_species</br>
test:dbo_conservationStatus</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_conservationStatusSystem var_x brack_close

test:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_conservationStatusSystem var_x brack_close

```

----

```
reference:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_conservationStatusSystem var_x brack_close

test:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_conservationStatusSystem var_x brack_close

```

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_conservationStatusSystem var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_conservationStatusSystem var_x brack_close

```

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_conservationStatusSystem var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_conservationStatusSystem var_x brack_close

```

----

```
reference:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_division var_x brack_close

test:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_series var_x brack_close

```
ref:dbo_division</br>
test:dbo_series</br>

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_division var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_series var_x brack_close

```
ref:dbo_division</br>
test:dbo_series</br>

----

```
reference:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_family var_x brack_close

test:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_family var_x brack_close

```
ref:dbo_species</br>
test:dbo_family</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_family var_x brack_close

test:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_family var_x brack_close

```
ref:dbo_species</br>
test:dbo_family</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_family var_x brack_close

test:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_family var_x brack_close

```
ref:dbo_species</br>
test:dbo_family</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_genus var_x brack_close

test:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_series var_x brack_close

```
ref:dbo_genus</br>
test:dbo_series</br>

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_genus var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_series var_x brack_close

```
ref:dbo_genus</br>
test:dbo_series</br>

----

```
reference:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_kingdom var_x brack_close

test:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_species var_x brack_close

```
ref:dbo_kingdom</br>
test:dbo_species</br>

----

```
reference:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_kingdom var_x brack_close

test:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_species var_x brack_close

```
ref:dbo_kingdom</br>
test:dbo_species</br>

----

```
reference:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_kingdom var_x brack_close

test:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_species var_x brack_close

```
ref:dbo_kingdom</br>
test:dbo_species</br>

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_kingdom var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_kingdom var_x brack_close

```
ref:dbo_species</br>
test:dbo_kingdom</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_kingdom var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_kingdom var_x brack_close

```
ref:dbo_species</br>
test:dbo_kingdom</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_order var_x brack_close

test:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_manufacturer var_x brack_close

```
ref:dbo_order</br>
test:dbo_manufacturer</br>

----

```
reference:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_order var_x brack_close

test:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_order var_x brack_close

```

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_order var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_phylum var_x brack_close

```
ref:dbo_species</br>
test:dbo_phylum</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_order var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_phylum var_x brack_close

```
ref:dbo_species</br>
test:dbo_phylum</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_phylum var_x brack_close

test:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_budget var_x brack_close

```
ref:dbo_phylum</br>
test:dbo_budget</br>

----

```
reference:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_phylum var_x brack_close

test:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_budget var_x brack_close

```
ref:dbo_phylum</br>
test:dbo_budget</br>

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_phylum var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_language var_x brack_close

```
ref:dbo_phylum</br>
test:dbo_language</br>

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_phylum var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_voice var_x brack_close

```
ref:dbo_phylum</br>
test:dbo_voice</br>

----

```
reference:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_synonym var_x brack_close

test:select var_x where brack_open dbr_Mycoplasma_mycoides dbo_species var_x1 sep_dot var_x1 dbo_predecessor var_x brack_close

```
ref:dbr_Crotalus_mitchellii_muertensis</br>
test:dbr_Mycoplasma_mycoides</br>
ref:dbo_synonym</br>
test:dbo_predecessor</br>

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_synonym var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_predecessor var_x brack_close

```
ref:dbo_synonym</br>
test:dbo_predecessor</br>

----

```
reference:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_thumbnail var_x brack_close

test:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_distributor var_x brack_close

```
ref:dbo_thumbnail</br>
test:dbo_distributor</br>

----

```
reference:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_thumbnail var_x brack_close

test:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_budget var_x brack_close

```
ref:dbo_thumbnail</br>
test:dbo_budget</br>

----

```
reference:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_wikiPageExternalLink var_x brack_close

test:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_family var_x1 sep_dot var_x1 dbo_wikiPageExternalLink var_x brack_close

```
ref:dbo_species</br>
test:dbo_family</br>

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_wikiPageExternalLink var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_family var_x1 sep_dot var_x1 dbo_wikiPageExternalLink var_x brack_close

```
ref:dbo_species</br>
test:dbo_family</br>

----

```
reference:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_wikiPageID var_x brack_close

test:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_extinctionYear var_x brack_close

```
ref:dbo_species</br>
test:dbo_extinctionYear</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_wikiPageID var_x brack_close

test:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_extinctionYear var_x brack_close

```
ref:dbo_species</br>
test:dbo_extinctionYear</br>
ref:var_x1</br>
test:var_x</br>
ref:sep_dot</br>
test:brack_close
</br>
Wrong number of tokens

----

```
reference:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_wikiPageID var_x brack_close

test:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_family var_x1 sep_dot var_x1 dbo_wikiPageID var_x brack_close

```
ref:dbo_species</br>
test:dbo_family</br>

----

```
reference:select var_x where brack_open dbr_Black-chinned_emperor_tamarin dbo_species var_x1 sep_dot var_x1 dbo_wikiPageRedirects var_x brack_close

test:select var_x where brack_open dbr_Black-chinned_emperor_tamarin dbo_family var_x1 sep_dot var_x1 dbo_wikiPageRedirects var_x brack_close

```
ref:dbo_species</br>
test:dbo_family</br>

----

```
reference:select count attr_open wildcard attr_close as var_x where brack_open dbr_Black-chinned_emperor_tamarin dbo_species var_x1 sep_dot var_x1 dbo_wikiPageRedirects var_x brack_close

test:select count attr_open wildcard attr_close as var_x where brack_open dbr_Black-chinned_emperor_tamarin dbo_family var_x1 sep_dot var_x1 dbo_division var_x brack_close

```
ref:dbo_species</br>
test:dbo_family</br>
ref:dbo_wikiPageRedirects</br>
test:dbo_division</br>

----

```
reference:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_species var_x1 sep_dot var_x1 dbo_wikiPageRevisionID var_x brack_close

test:select var_x where brack_open dbr_Cyclura_cychlura_figginsi dbo_family var_x1 sep_dot var_x1 dbo_wikiPageRevisionID var_x brack_close

```
ref:dbo_species</br>
test:dbo_family</br>

----

```
reference:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_species var_x1 sep_dot var_x1 dbo_wikiPageRevisionID var_x brack_close

test:select var_x where brack_open dbr_Crotalus_mitchellii_muertensis dbo_family var_x1 sep_dot var_x1 dbo_wikiPageRevisionID var_x brack_close

```
ref:dbo_species</br>
test:dbo_family</br>

----

```
reference:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_species var_x1 sep_dot var_x1 dbo_wikiPageRevisionID var_x brack_close

test:select var_x where brack_open dbr_University_of_Maryland_Arboretum_&_Botanical_Garden dbo_family var_x1 sep_dot var_x1 dbo_wikiPageRevisionID var_x brack_close

```
ref:dbo_species</br>
test:dbo_family</br>

----

