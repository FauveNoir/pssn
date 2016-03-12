% PSSN — Printer Specification Standard Nomenclatur

The PSSN is a very simple way to describe a printer’s specifications with a minimal information.
It use a serie of cells. Each cell can say if the printer contain or not a feature, or also if a kind of printers contain one model with an optionnal feature.


All cells began by one of `+`, `-`, or `±` indicator, followed by the code of the feature.

`+` is for an existing feature.
`-` is for an non existing feature.
`±` is for an optionnal feature.


The possible feature is the following:

* `t[ype]:<laser|toner|other type>` : specify the printer’s technology.
* `color` : Specify if the printer use color or only support black.
* `net` : Specify if the printer use network connection.
* `scan` : Specify if the printer contain a scanner.
* `fax`
* `rv`
* `f:<maximal acceptable format>:<minimal acceptable format>`
* `c<longeur>:<largeur>:<profondeur>`
* `w<weight>`
* `connect:<serial|usb|other non-network connection type>`


#Order
It is possible to use cells on any order but for much more readeability, it is preferable to began by positive celles, followed by plus-minussed cells, and negative cells. In each one of this tree groups, it is preferable to cite feature in this order: t, color, net, scan, fax, rv, f, c, w.

#The condensed way
It is also possible to only specify the indicators `+`, `-`, and `±` in the canonical order, separted by comma. The non-defined cells will stay blanc between two coma.

    ,±,+,-,-,+,A4,,14Kg

A more condensed coma-free way consist on using letters Y(es) for existing feature, N(o) for unexisting feature, O(ptionnal) for optionnal feature, and I(ndifined) for indefined feauture.

    IOYNNY-A4-I-14Kg

#Examples

The following code is for a printer witch support network, printing on two sides, have A4 as a maximal format supported, have some models with color and other only with black, do not have scanner and no fax.

    +net+rv+f:A4±color-scan-fax
    ,±,+,-,-,+
    IOYNNY
