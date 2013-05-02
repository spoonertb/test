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
  
  e ::= f && e | f
  f ::= t || f | t
  t = true | false
