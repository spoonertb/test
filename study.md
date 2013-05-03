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


precedent/consequence: If precedence is true, then consequence is also true

/consequence: Axiom


e1:=true e2:= v/(e1? e2: e3):= v:   If(e1, e2, e3) => {

##Functions are Values!

f(x: function): function

Higher Order Function

val v1: List[int] = List(1, 2, 3)
def f(x: Int): Int = {x + 1}
v1.map(f) = List(2, 3, 4)


val v1: List[int] = List(1, 2, 3)
def f(acc: Int, x: Int): Int = acc + x
v1.foldLeft(0)(f)

acc   v1 =>   acc`
0     (1,2,3)  1
1     (2,3)    3
3     (3)      6
6     ( )      6

##Currying

f(x, y) => g(y)
  |             
  h(f, 5) => f(5, y) => g(y)
  
  
  function add(x)(y) =
    function(y) {return x + y}
    
    
    
List ---> f(x) - f(x + 1)
val l1 = List(1, 2, 3, 4)
def f(x) = 2x - 1
def deriv(l, f, c) = l match {
  case h1:t1 => (f(c) - f(h1)) :: deriv(t2, f, h1)
  case h1::Nil => (f(h1) - f(c)) :: Nil
  case Nil => Nil
}  
