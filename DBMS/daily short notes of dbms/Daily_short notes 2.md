## 15 Sept,2023

3 NF form of Normalisation:-
 * A relation will be in 3NF if it is in 2NF and not contain any transitive partial dependency.
 * 3NF is used to reduce the data duplication. It is also used to achieve the data integrity.

**QUESTION on 3 NF Form :-**

* *Ques* :- Given that, R(A,B,C,D,E,F,G,H,I,J,K) 
          and (A,B)-->D ; A -->CE ; B-->G ; G-->H,I ;  C-->J,K

* *ANS* :- ABF<sup>+</sup>={A,B,C,D,E,F,G,H,I,J,K} ; GF<sup>+</sup>={G,F,H,I} ; CF<sup>+</sup>={C,F,J,K}
        ; AF<sup>+</sup>={A,F,C,E,J,K} ;  BF<sup>+</sup>={B,F,G,H,I}
  * candidate key={ABF<sup>+</sup>}

### THE END**************************************************************

## 16 SEP,2023

1. Transitive Dependency :- NON PRIME ATTRIBUTE----> NON PRIME ATTRIBUTE

 * To remove transitive dependency in 3NF form we have 2 options :-
   * CASE 1:- L.H.S can be a candidate key or super key.
   * CASE 2:- RHS has atleast one prime attribute.

2.  **Boyce-Codd Normal Form (BCNF)**
  * The table should be in the 3rd Normal Form.
  * LHS has to be a candidate key /super key.

**QUESTION on BCNF Form :-**

*QUES* :- R(A,B,C,D)  FD={AB-->CD ; D-->B }

 *ANS* :- AB<sup>+</sup>={A,B,C,D} ; AC<sup>+</sup>={A,C} ; AD<sup>+</sup>={A,D,B,C} ;

  * CANDIDATE KEY : {AB,AD} ; PRIME ATTRIBUTE: {A,B,D} ; NON PRIME ATTRIBUTE:{C}

    * This is in 3NF form but not in BCNF Form . To remove this we will split the relation .
   
    * R1: (D,B)  {D-->B}          ;   R2: (D,A,C)  {AD-->C}  [Since, AD was a candidate key ]
   
    * IN THIS GIVEN RELATION WE CAN'T PRESERVE ALL THE DEPENDENCIES.
    * SO,IN BCNF GENERALLY DEPENDENCIES ARE NOT PRESERVED,WHEREAS IT MIGHT BE PRESERVED IN SOME CASES.
   
 3. DECOMPOSTION OF A RELATION :-
  * i. LOSSLESS (Row count remains same).
  * ii. LOSSY (Row count increases).

4. **THREE PROPERTIES OF DECOMPOSTION**
   * R1 U R2 =R
   * R1 ∩ R2 ≠ Φ
   * R1 ∩ R2= Must be a unique key of R1 or R2.
  
5. Concept and Example Related with LOSSLESS AND LOSSY JOIN .
   <img src="https://slideplayer.com/slide/13441100/80/images/5/Lossless-Join+Decomposition.jpg">
   <img src ="https://i.ytimg.com/vi/CSqsjqLnfVo/maxresdefault.jpg">

### THE END**************************************************************


## 18 Sep, 2023

1. 4 NF Normal Form :-
   * 1. It should be in the Boyce-Codd Normal Form (BCNF).
   * 2. The table should not have any Multi-valued Dependency.
    
2. MULTIVALUED DEPENDENCY :-
  * Multivalued dependency occurs when two attributes in a table are independent of each other but, both depend on a third 
     attribute.
  * A multivalued dependency consists of at least two attributes that are dependent on a third attribute that's why it 
      always requires at least three attributes.

  * EXAMPLE:-  <img src="https://scaler.com/topics/images/mvd.webp">
  * **Representation of Multivalued Dependency(MVD)**
      we write MVD as,
                       ***a --> --> b***

3. 5 NF NORMAL FORM:-
   * 1. R should be already in 4NF. 
   *  2. It cannot be further non loss decomposed (join dependency).

4. JOIN DEPENDENCY:-
   * A Join dependency in DBMS is a constraint in DBMS. A table(Suppose R) is considered a join dependency if it can be recreated by simply connecting multiple tables, each containing a subset of the R's attributes.
  
   * <img src="https://haygot.s3.amazonaws.com/questions/927726_917378_ans_b144504ad2ff40c2815816979eac2697.PNG">

   * If lossless decompostion , join dependency should exist in 5 NF form.
   * If lossy decomposition , join dependency shouldn't exist in 5 NF form.
  

### THE END**************************************************************

## 20 Sep, 2023

1. clone the *go mysql server* repository and try to read and understand READme.md file.
2. Define Software:-
   * **FROM USER POINT OF VIEW**:-
      * Software can be finite number of scripts or programs having a proper documentation .
      * A Software must accompany a detail documentation so that anyone can update that software programs .
      * Without documentation no one can fix a bug, update a feauture .
      * Complexity of software :- No single person can update the whole script of software.

  * **FROM DEVELOPER POINT OF VIEW**:-
     * A Software can be a finite no. of scripts or programs having proper test scripts .

3. ITERATIVE WATERFALL MODEL.
4. FORWARD ENGINEERING AND BACKWARD ENGINEERING. 
  

       