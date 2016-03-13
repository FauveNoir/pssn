# PSSN

![Logo](./pssnlogo.png)
The PSSN is a very simple way to describe a printer’s specifications with a minimal expression.
The PSSN is*n’t* designed to replace code name of printers but only to describe there feature. For example, two different printers from two constructors could share the same pssn.
It use a serie of cells. Each cell can say if the printer contain or not a feature, or also if a kind of printers contain one model with an optional feature.


All cells began by one of `+`, `-`, or `±` indicator, followed by the code of the feature.

`+` is for an existing feature.
`-` is for an non existing feature.
`±` is for an optional feature.


The possible feature is the following:

* `t[ype]:<laser|toner|matricial|plomb’s amovible character|other type>` : specify the printer’s technology.
* `color` : Specify if the printer use color or only support black.
* `net` : Specify if the printer use network connection.
* `scan` : Specify if the printer contain a scanner.
* `fax`
* `rv`
* `f:<maximal acceptable format>:<minimal acceptable format>`
* `c<longeur>:<largeur>:<profondeur>`, by default, is meter.
* `w<weight>`, by default is gram.
* `connect:<serial|usb|other non-network connection type>`


#Order
It is possible to use cells on any order but for much more readability, it is preferable to began by positive cells, followed by plus-minussed cells, and negative cells. In each one of this tree groups, it is preferable to cite feature in this order: t, color, net, scan, fax, rv, f, c, w.

#The condensed way
##With coma’s separation
It is also possible to only specify the indicators `+`, `-`, and `±` in the canonical order, separated by comma. The non-defined cells will stay blanc between two coma.

    ,±,+,-,-,+,A4,,14Kg

##With letters
A more condensed coma-free way consist on using letters Y(es) for existing feature, N(o) for unexisting feature, O(ptionnal) for optional feature, and I(ndifined) for undefined feature.

    IOYNNY-A4-I-14Kg
    IOYNNY-A4-I-14K
    IOYNNY-A4-I-14000

##With numbers
It’s like commas but it have to contain only numbers.
The existing feature is represented by 1, the non existing by 2, the optional feature 3, the undefined by 0, and the cell’s separator is a dash `-`. If you have to specify a lent, the default unit is meter, a weight the default is gram. For page format, you have to specify lent separated by a dash.

    031221-0.229-0.21-0-14000

#Examples

The following code is for a printer witch support network, printing on two sides, have A4 as a maximal format supported, have some models with color and other only with black, do not have scanner and no fax.

    +net+rv+f:A4±color-scan-fax
    ,±,+,-,-,+
    IOYNNY

#Normalised tag
So, a normalised tag could be add to printers box, for the previous PSSN example, the tag is like :

![Example tag](./tagexample.png)
