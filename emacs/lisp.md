
# Table of Contents

-   [eval](#org0f7e25e)
-   [Output](#org83142a6)
-   [buffer](#orgd90d5f2)
-   [String](#orgd64b0c8)
-   [Arithmetic](#org62e06b5)
-   [Boolean](#org2af5892)
-   [Test equality](#orgb905cfe)
-   [Variables](#orgd6189be)
-   [Block Expression](#org66b708e)
-   [Condition](#org4604863)
-   [Loop](#org04ee582)
-   [Fucntion](#org140f9c8)



<a id="org0f7e25e"></a>

# eval


## eval-last-sexp


## eval-region


<a id="org83142a6"></a>

# Output


## message

(message FORMAT-STRING &rest ARGS)

1.  %d
2.  %s
3.  %S


## insert


## print


## prinl


## princ


<a id="orgd90d5f2"></a>

# buffer


## generate-new-buffer


## switch-to-buffer


## with-output-to-temp-buffer

> (with-output-to-temp-buffer BUFNAME &rest BODY)


<a id="orgd64b0c8"></a>

# String


## length


## substring


## concat


## split-string


## format


<a id="org62e06b5"></a>

# Arithmetic

1.  +
2.  -
3.  \*
4.  /
5.  %
6.  expt


## Test number


### integerp


### floatp


## Convert


### float


### truncate


### floor


### ceiling


### round


### string-to-number


### number-to-string


### format


<a id="org2af5892"></a>

# Boolean

1.  t
2.  nil
3.  ()


## all is false

    (if nil "yes" "no")
    (if () "yes" "no")
    (if '() "yes" "no")
    (if (list) "yes" "no")


## all is true

    (if t "yes" "no")
    (if 0 "yes" "no")
    (if "" "yes" "no")
    (if [] "yes" "no")


## Boolean function

    (and t nil)
    (and t t t nil t)
    
    (or t nil)
    
    (not t)
    (not nil)
    (not 2)


<a id="orgb905cfe"></a>

# Test equality


## =

    (= 3 3)
    (= 3.5 3.5)
    (= 3 3.0)
    
    (= 3 3.0000000000000001)
    (= 3 3.000000000000001)
    
    (/= 3 4)


## string-equal

Only for comparing

    (string-equal "abc" "abc")
    (string-equal "abc" "Abc")
    (string-equal 'abc 'abc)
    (string-equal "abc" 'abc)


## equal

Check datatype and value

    (equal 3 3)
    (equal 3.0 3.0)
    
    (equal 3 3.0)
    
    (equal '(3 4 5) '(3 4 5))
    (equal '(3 4 5) '(3 4 "5"))
    
    (equal "s" "s")
    
    (equal 'abc 'abc)


## eq

Check if is the same object

    (eq 'x 'x)
    (eq 2 2)
    (eq "e" "e")
    (eq 2.1 2.1)
    
    (let (aa bb)
      (setq aa '(3 4))
      (setq bb '(3 4))
      (eq aa bb)
      )
    
    (let (aa bb)
      (setq aa '(3 4))
      (setq bb aa)
      (eq aa bb)
      )


## eql

Check if is the same object only for floating number

    (eql 1.1 1.1)
    (eql 0.0 -0.0)


<a id="orgd6189be"></a>

# Variables


## Global Variables


### setq

Set one or more variables. Return the last value.

    (setq x 3)
    (equal x 3)
    
    (equal
     (setq xa 1 xb 2 xc 3)
     3)
    
    (equal
     (setq xa 1
           xb (+ xa 3))
     4)


### defvar

Declare and assign a variable, and return the SYMBOL.

    (defvar xx 4 "DOCSTRING")


## Local Variables


### let

    (let (a b)
      (setq a 3)
      (setq b 4)
      (+ a b)
      )
    
    ;; convince
    (let ((a 3) (b 4))
      (+ a b)
      )


### let\*

like let, but can use defined earlier symbols.

    (equal
     (let* ((xa 3)
            (xb xa))
       xb)
     3
     )


<a id="org66b708e"></a>

# Block Expression

Like block {} in C-like language

    (progn
      (message "a")
      (message "b"))
    
    (progn 3 5)

<div class="notes" id="orgf071af6">
<p>
(if something
    (progn ; true
      ;; code here
      )
  (progn ; else
    ;; code here
    ))
</p>

</div>


<a id="org4604863"></a>

# Condition


## if

    (if (< 3 2)
        (progn 8)
      (progn 7))
    
    (if (< 3 2)
        (progn 8))


## when

Use "when" when don't want else case.

    (when (< 3 2)
      (message "8"))


<a id="org04ee582"></a>

# Loop


## while

    (let ((x 0))
      (while (< x 4)
        (print (format "number is %d" x))
        (setq x (1+ x))
        ))
    
    (let ((xx '(a b c )))
      (while xx
        (message "%s" (pop xx))
        (sleep-for 1)
        )
      )
    
    (let (xx ii)
      (setq xx [0 1 2 3 4 5])
      (setq ii 0)
    
      (while (< ii (length xx))
        (insert (format "%d" (aref xx ii)))
        (setq ii (1+ ii))
        )
      )


## DONE dotimes

Useful for go over list to get the element, Similar with C-like for-loop?

    (dotimes (i 4)
      (insert (number-to-string i)))
    
    (let ((xx [3 4 5]))
      (dotimes (i (length xx))
        (insert
         (number-to-string (elt xx i)))
        )
      )
    
    (let ((xx [10 20 30 40 50]))
      (catch 'TAG743
        (dotimes (i 99)
          (message "i %s %s" i (aref xx i))
          (if (eq (aref xx i) 30)
              (throw 'TAG743 "got it")
              nil))
        )
      )


<a id="org140f9c8"></a>

# Fucntion


## &rest

\`&rest\` is a way of specifying that the final arguments to a function can be of any type, and can be passed as a variable number of arguments. It is commonly used in Emacs Lisp code to define functions that can be called with a variable number of arguments.


## pop


## aref


## elt


## throw


## catch

