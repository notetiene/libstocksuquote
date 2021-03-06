# The Stocks Quotes Library Utility (libustocks)
Version 0.5.1 November 26, 2014

Libstocks is a C library which can be included in any software to fetch stocks
quotes.

Maintained by Etienne Prud'homme (e.e.f.prudhomme@gmail.com)  
Originally written by Eric Laeuffer (laeuffer@cybercable.fr)  

## Features:

  * Support of a lot of markets : 
United States

    * Canada
    * Mexico
    * Brasil
    * Argentina
    * Venezuela
    * Chili
    * Australia
    * and European markets
    * (See at the end for symbols as exemples)
  * Proxy support
  * Currency exchange rates
  * Historical stocks quotes from http://chart.yahoo.com/d Unfortunately this feature just supports US stocks.
  * This package includes a small client which can show you how to use libstocks

## How to use libstocks_client

`$ libstocks_client "symbols"`

for exemple :

`$ libstocks_client "RHAT+13000.PA"`

This displays the quotes of RedHat and Alcatel (Paris) stocks like this:

    
    "17h36" 
    ----------------------------------------
    | Symbol    | "13000.PA"               |
    | Price     | 71.50                    |
    | Yesterday | 72.50                    |
    | Open      | 70.70                    |
    | Min       | 69.40                    |
    | Max       | 73.50                    |
    | Var       | -1.00  (-1.38 %)         |
    | Volume    | 5050319                  |
    ----------------------------------------
    
    "4:01PM" "6/23/2000"
    ----------------------------------------
    | Symbol    | "RHAT"                   |
    | Price     | 31.38                    |
    | Yesterday | 34.19                    |
    | Open      | 30.56                    |
    | Min       | 35.44                    |
    | Max       | 35.50                    |
    | Var       | -2.81  (-8.23 %)         |
    | Volume    | 8312600                  |
    ----------------------------------------

To access US quotes just use the stocks symbol to grep or with the .US
extension (RHAT=Red Hat Inc) and to acces european stocks use the stock symbol
with the country extension (13000.PA=Alcatel Paris)

_Note: use yahoo symbol lookup to find stocks symbol)_

All symbols have to be separated **by "+" caracter.**

As exemple some symbols:

    
    USA : BOBJ.US, ENT.US
    CANADA: BMO.TO, IN.M, COT.V
    AUSTRALIA: BII.AX, BKL.AX
    MEXICO: TELMEXL.MX, TELECOMA1.MX, GFBO.MX
    BRASIL: ACES4.SA, TLPP4.SA, FNOR11.SA
    ARGENTINA: PCH.BA, IRS.BA, ERC.BA
    VENEZUELA: MPA.CR, EDC.CR, HLB.CR
    CHILI: END.SN, CIC.SN, LAB.SN
    NORWAY: STA.OL, IGE.OL, AVE.OL
    DANMARK: ISS.CO, DCO.CO, NBH.CO, TLD.CO
    GERMANY: 508900.F, 510440.F, 901599.FX, 542700.FX, 622700.FX
    ITALY: PLV.MI, HPI.MI, MB.MI, NM.MI
    SPAIN: TEF.MC, TAZ.MC, EUR.MC
    SWEDEN: VIKT.ST, TLOG.ST, CONN.ST, SION.ST
    UNITED KINGDOM: VOD.L, RTO.L, BPA.L

Here my test command:

    
    $ libstocks_client "BMO.TO+IN.M+COT.V+BOBJ.US+ENT.US+BII.AX+TELMEXL.MX+ACES4.SA
    +PCH.BA+MPA.CR+END.SN+LAB.SN+STA.OL+ISS.CO+508900.F+901599.FX+PLV.MI+TEF.MC
    +VIKT.ST+VOD.L+13000.PA"

## To get historical quotes:

    
    $ libstocks_client BOBJ 2000/01/01 2000/08/01

_(the date format is YY/MM/DD)_

This exemple displays on the screen the DATE, OPEN, HIGH, LOW, CLOSE, VOLUME

