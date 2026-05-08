# Unified Finance

Front to back office software and analytics.

## Front Office

A _holding_ is an _amount_, _instrument_, and _owner_.
Amounts are an integral multiple of the minimum trading
size of an instrument. The set of owners is a hierarcy.
The root owner can have subsidiaries and we can further
partition into corporate units and even individual 
employees. The owner of a holding is a leaf in the
hierarchy that can be used to obtain parent information.

A _position_ is a collection of holdings and is modified
by _exchanges_. An exchange is a trading time and
a pair of holdings. The portfolio is modified
by swapping the amount and instrument of the owners.
A _transaction_ is a group of related exchanges,
e.g., commissions or fees. 

The _mark-to-market_ involves specifying a putative
price $X(i)$ for instruments. Amount $a$ of instrument
$i$ has value $aX(i)$. A more realistic model would
allow price $X(a,i,o)$ to involve the amount and the owner. 

## Mid Office

## Back Office

## Analytics

Every arbitrage-free model is determined by a martingale
measure $M_t$ indexed by instruments and positive measures $D_t$. 
Arbitrage-free prices $X_t$ and cash flows $C_t$
of instruments satisfy
```math
X_t D_t = (X_u D_u + \sum_{t < s \le u} C_s D_s)|_{𝒜_t}
```
where $𝒜_t$ is the partition of the sample space $\Omega$ 
representing information available at time $t$.
