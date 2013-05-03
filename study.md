##Grammars
* Ambiguity: Grammar is ambiguous if a concrete sentence can be derived multiple ways
* Associativity
* Precedence
* BNF
* Vocabulary

ex. 

  e ::= if e then e else e | e, e | n
  n ::= 0 | 1
  
  e ::= e + e | e * e | n
  n ::= 0 | 1
  
* Example of ambiguous grammar:
t
  e ::= f && e | f
  f ::= t || f | t
  t = true | false

  A := A & A | V                        
  V := a | b
  
    A                     A
  / | \                 / | \
 A  &  A               A  &  A
 |  |  | \          A & A    / 
 a  &  a & a        a & a & a
  
The grammar above is ambiguous

##Judgements


  precedent    <--- If this is true
'-----------'                                       '------------'  <---- Axiom
 consequence   <--- Then so is this                   consequence
