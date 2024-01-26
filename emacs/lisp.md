
# Table of Contents

-   [eval](#org1b973d4)
-   [Output](#org29f220e)
-   [buffer](#org5e91c4a)
-   [String](#org90fd733)
-   [Arithmetic](#org031ce9d)
-   [Boolean](#orgfbe2f88)
-   [Test equality](#org739874d)
-   [Variables](#org2ec934b)
-   [Block Expression](#org3bfd6bd)
-   [Condition](#orgcbf86d8)
-   [Loop](#org594beaa)
-   [List](#orge708ee9)
-   [Vector](#orgafd9438)
-   [Sequence](#org839b785)
-   [Hash Table](#org8b15874)
-   [Association List](#org8fbf8da)
-   [Function](#org5adca01)
-   [Exit](#org2a02caf)
-   [Apply Function(List to Args)](#org92eaace)
-   [Symbol](#orgd1afd11)
-   [Special Form](#orgabca074)
-   [Cheeck If func/var is defined](#org53df814)
-   [Regular Expression](#orgd782919)
-   [DateTime](#orgec6c3db)
-   [Builtin Fucntions](#org0546f30)
-   [Find Document](#org8e385c5)
-   [Hook](#org701b33e)
-   [Search In Manual](#org3e935b4)
-   [Code Navigate Command](#org3ae19ee)
-   [Write Major Mode](#org98e717f)
-   [Character Type](#org22301d5)
-   [Syntax Table](#org65cbd02)
-   [Sample](#org5849cfe)
-   [Quotes](#orgbdfe962)
-   [Macro](#orgd2d6fcf)



<a id="org1b973d4"></a>

# eval


## eval-last-sexp


## eval-region


<a id="org29f220e"></a>

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


<a id="org5e91c4a"></a>

# buffer


## generate-new-buffer


## switch-to-buffer


## with-output-to-temp-buffer

> (with-output-to-temp-buffer BUFNAME &rest BODY)


<a id="org90fd733"></a>

# String


## length


## substring


## concat


## split-string


## format


<a id="org031ce9d"></a>

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


<a id="orgfbe2f88"></a>

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


<a id="org739874d"></a>

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


<a id="org2ec934b"></a>

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

    (setq my-var nil)
    (defvar my-var t)
    (message "var is %s" my-var)


### defcustom

    (defcustom my-option t
      "My user option."
      :set (lambda (sym val)
             (set-default sym val)
             (message "Set %s to %s" sym val)))


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


## File local variable

    (setq-local my-var t)
    ;; or (set (make-local-variable 'my-var) t)
    
    ;; Then descirbe-variable my-var will show:
    ;; my-var’s value is t
    ;; Local in buffer *Org Src lisp.org[ emacs-lisp ]*; global value is the same.
    
    ;; Not documented as a variable.


### Automatic buffer local variable

    (defvar-local my-automatical-local-var t)
    ;; or (make-variable-buffer-local 'my-automatical-local-var)


## Binding

Default is dynamic binding


### Lexical binding

1.  faster
2.  less error-prone
3.  prefered

    ;;; -*- lexical-binding: t; -*-


### Dynamic binding

    ;; -*- lexical-binding: t; -*-
    
    (defun a-exists-only-in-my-body (a)
      (other-function))
    
    (defun other-function ()
      (message "I see `a', its value is %s" a))
    
    (a-exists-only-in-my-body t)


### Special variable

    ;;; -*- lexical-binding: t; -*-
    
    (defun some-other-function ()
      (message "I see `c', its value is: %s" c))
    
    (defvar c t)
    
    (let ((a "I'm lexically bound")
          (c "I'm special and therefore dynamically bound"))
      (some-other-function)
      (message "I see `a', its values is: %s" a))


### Variable conflict

    (let ((vars ()))
      (mapatoms
       (lambda (cand)
         (when (and (boundp cand)
                    (not (keywordp cand))
                    (special-variable-p cand)
                    (not (string-match "-"
                                       (symbol-name cand))))
           (push cand vars))))
      vars) ;; => (t obarray noninteractive debugger nil)


<a id="org3bfd6bd"></a>

# Block Expression

Like block {} in C-like language

    (progn
      (message "a")
      (message "b"))
    
    (progn 3 5)

<div class="notes" id="orge844863">
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


<a id="orgcbf86d8"></a>

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


<a id="org594beaa"></a>

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


<a id="orge708ee9"></a>

# List

底层为 **cons** 结构，高效的栈结构


## 常用操作

1.  car
2.  cdr
3.  push
4.  pop
5.  nth
6.  nthcdr
7.  butlast
8.  last
9.  length
10. cons


## Create List

    (setq xx (list 1 "b" 3))
    (message "%S" xx)
    
    (setq xxx '(a b c))
    (message "%S" xxx)
    
    (let (x y z)
      (setq x 3)
      (setq y 4)
      (setq z 5)
      (message "%S" (list x y z)))


### Create List of Same Value

    (equal (make-list 3 0) '(0 0 0))


### Create List of Range of Nubmers

    (equal
     (number-sequence 5)
     '(5))
    
    (equal
     (number-sequence 2 5)
     '(2 3 4 5))
    
    
    (equal
     (number-sequence 0 9 3)
     '(0 3 6 9))
    
    (equal
     (number-sequence 0 9 2)
     '(0 2 4 6 8))
    
    (equal
     (number-sequence 4 0 -1)
     '(4 3 2 1 0))
    
    (equal
     (number-sequence 2.2 5.3)
     '(2.2 3.2 4.2 5.2))


### Empty List

empty list equals nil

    (eq '() (list))
    (eq '() nil)
    (eq (list ) nil)


## List Length

    (equal (length '("a" "b" "c")) 3)


## Add to List

Use cons

    (equal
     (cons "a" '("c" "d"))
     '("a" "c" "d"))
    
    (equal
     (cons '("a" "b") '("c" "d"))
     '(("a" "b") "c" "d"))


## Get Elament from List

    (equal
     (car '("a" "b" "c"))
     "a")
    
    (equal
     (cdr '(0 1 2 3 4))
     '(1 2 3 4))
    
    ;; index
    (equal
     (nth 1 '(0 1 2 3 4))
     1)
    
    
    ;; do cdr nth times
    (equal
     (nthcdr 2 '(0 1 2 3 4))
     '(2 3 4))
    
    ;; without last n
    (equal
     (butlast '(0 1 2 3 4 5))
     '(0 1 2 3 4))
    
    (equal
     (butlast '(0 1 2 3 4 5) 2)
     '(0 1 2 3))
    
    ;; get actual last item
    (equal
     (car (last (list "a" "b" "c")))
     "c")
    
    (equal
     (last (list "a" "b" "c"))
     (cons "c" nil))
    
    (equal
     (last '(0 1 2 3 4 5 6) 2)
     '(5 6))


## Modify List


### Add Element

-   push

        (setq xx '(1))
        (eq (push 2 xx) xx)
        (equal xx '(2 1))
        
        (setq xx '((1 2) (3 4) (5 6)))
        (equal
         (push "b" (nth 1 xx))
         '("b" 3 4))
        
        (equal
         xx
         '((1 2) ("b" 3 4) (5 6)))
        
        (setq xx [(1 2) (3 4) (5 6)])
        (equal
         (push "b" (aref xx 1))
         '("b" 3 4))
        (equal
         xx
         [(1 2) ("b" 3 4) (5 6)])

-   add-to-list

        (setq xx '(1 2 3))
        (eq
         (add-to-list 'xx "a")
         xx)
        
        (equal
         xx
         '("a" 1 2 3))


### Rm Element

-   pop

        (setq xx '(1 2 3 4))
        (equal (pop xx) 1)
        (equal xx '(2 3 4))

-   nbutlast

        (setq xx '(0 1 2 3))
        (equal (nbutlast xx 1) '(0 1 2))
        (equal xx '(0 1 2))


### Replace Element

-   setcar

        (setq xx '(1 2 3 4))
        (equal (setcar xx "a") "a")
        (equal xx '("a" 2 3 4))

-   setcdr

        (setq xx '(1 2 3 4))
        (equal
         (setcdr xx (cons "a" nil))
         (cons "a" nil))
        
        (equal xx '(1 "a"))


## Check Element Exit in List

    ;; if exist, resturn list start with occurrence
    (member "4" '("3" "4" "5"))
    (member-ignore-case "A" '("b" "a"))


## Rm Item from List


### Delete

    (setq xx '(3 4 5))
    (remq 4 xx)
    (equal xx '(3 4 5))
    
    (setq xx '(3 4 5))
    (setq xx (delq 4 xx))


### Delete Duplicate

    (let (xx)
      (setq xx '(3 4 5 3 2))
      (setq xx (delete-dups xx)))


## Convert List


### Sequence to Vector

    (equal
     (vconcat [3 4] ["a" "b"])
     [3 4 "a" "b"])
    
    (equal
     (vconcat [3 4] '("a" "b"))
     [3 4 "a" "b"])
    
    
    (equal
     (vconcat [3 4] "ab")
     [3 4 97 98])


### Sequence to List

    (equal
     (list 1 2 3 4)
     (append (list 1 2) (list 3 4)))
    
    (equal
     (append [1 2 3] nil)
     '(1 2 3))
    
    ;; create improper list
    (equal
     (append [1 2 3] [4 5])
     '(1 2 3 . [4 5]))
    
    (equal
     (append [1 2 3] [4 5] nil)
     '(1 2 3 4 5))
    
    (equal
     (append [1 2 3] [4 5] '(6))
     '(1 2 3 4 5 6))


### Sequence to String

    (string-equal
     (mapconcat 'number-to-string '(1 2 3) ",")
     "1,2,3")
    
    (string-equal
     (mapconcat 'identity '("a" "b" "c") ",")
     "a,b,c")
    
    (string-equal
     (mapconcat 'number-to-string [1 2 3] ",")
     "1,2,3")


<a id="orgafd9438"></a>

# Vector

Ordered sequence, implement by arrys


## Create Vector

    (equal
     (make-vector 5 0)
     [0 0 0 0 0])
    
    ;; with evaluated variable
    (let (xx)
      (setq xx 3)
      (equal
       (vector 1 2 xx)
       [1 2 3]))
    
    (let (aa xx)
      (setq aa 4
            xx [3 aa 5])
      (equal
       'aa
       (aref xx 1)))


## Fill Vector

    (setq xx [3 4 5])
    (eq
     (fillarray xx 1)
     xx)
    (equal xx [1 1 1])
    
    (equal
     (fillarray [3 4 5] 1)
     [1 1 1])


## Length

    (equal
     (length (vector 7 4 5))
     3)


## Get Element

    (equal
     (aref ["a" "b" "c"] 0)
     "a")


## Change Element

    (setq xx [3 4 5])
    (equal (aset xx 0 "b") "b")
    (equal xx ["b" 4 5])


## Nested Vector

    [[1 2] [3 4]]
    [8 [3 [2 9] c] 7 [4 "b"]]


<a id="org839b785"></a>

# Sequence

Sequence is not a real type, it contains List, Vector, String type.It's a abstract type, Yes, We see OOP shadow in elisp.


## Sequence Function


### Check Sequence

    (equal
     (seqp '(1 2 3))
     t)
    
    (equal
     (seq-length '(1 2 3))
     3)
    
    (equal
     (seq-empty-p '())
     t)
    
    (equal
     (seq-empty-p '(1 2 3))
     nil)


### Sort

    (equal
     (nreverse '(1 2 3 4))
     '(4 3 2 1))
    
    (equal
     (sort '(1 4 5 3) '<)
     '(1 3 4 5))


### Get

    (equal
     (seq-elt '(1 2 3 4) 1)
     2)


### Min, Max

    (equal
     (seq-min '(1 2 3 4))
     1)
    
    (equal
     (seq-max '(1 2 3 4))
     4)


### Insert Items

    (seq-mapcat
     (lambda (x)
       (if (eq 0 (mod x 2))
           (list x x)
         (list x)))
     '(1 2 3 4))


### Take Element

    (equal
     (seq-take '(1 2 3 4) 1)
     '(1))
    
    (equal
     (seq-take-while (lambda (elt) (> elt 0)) '(1 2 3 -1 -2))
     '(1 2 3))
    
    
    (equal
     (seq-drop '(1 2 3 4) 1)
     '(2 3 4))
    
    (equal
     (seq-drop-while (lambda (elt) (> elt 0)) '(1 2 3 -1 -2))
     '(-1 -2))
    
    (equal
     (seq-subseq '(1 2 3 4 5) 1 3)
     '(2 3))
    
    (equal
     (seq-filter (lambda (elt) (> elt 0)) '(1 2 3 -1 -2))
     '(1 2 3))
    
    (equal
     (seq-remove (lambda (elt) (> elt 0)) '(1 2 3 -1 -2))
     '(-1 -2))
    
    (equal
     (seq-uniq '(1 2 3 2 3 -1))
     '(1 2 3 -1))


### Delte Element

1.  remove
    1.  original seq not changed

2.  delete
    1.  original seq destroyed

    (setq xx '(3 4 5))
    (remove 4 xx) ; (3 5)
    (message "%S" xx) (3 4 5)
    
    (setq xx '(3 4 5))
    (setq xx (delete 4 xx))
    
    (setq xx [3 4 5])
    (setq xx (delete 4 xx))


### Loop

    (seq-do (lambda (elt) (message "%s" elt)) '(2 4 6))
    
    ;; see https://stackoverflow.com/questions/63306647/various-forms-of-looping-and-iteration-in-elisp
    (setq xx '(1 2 3))
    (seq-doseq (ite xx) (message "%s" ite))
    
    ;;https://www.gnu.org/software/emacs/manual/html_node/elisp/Sequence-Functions.html
    (seq-map (lambda (elt) (+ 1 elt)) '(2 3 4))
    (seq-mapn #'+ '(1 2 3) '(2 3 4))
    (seq-reduce #'+ '(2 3 4) 10)
    
    (seq-every-p (lambda (elt) (> elt 10)) '(11 22)) ;; t
    (seq-some (lambda (elt) (> elt 10)) '(1 22)) ;; t


### Check Existance

    (seq-contains '(1 2 3 4) 1)
    (equal
     (seq-find (lambda (elt) (> elt 0)) '(-2 1 -1))
     1)
    (equal
     (seq-position '(1 2 3 4) 3)
     2)
    (equal
     (seq-count (lambda (elt) (> elt 10)) '(1 2 23 34))
     2)


### Restructure

    (equal
     (seq-partition '(1 2 3 4) 2)
     '((1 2) (3 4)))
    (equal
     (seq-group-by (lambda (elt) (+ 1 elt)) '(1 2 3 4))
     '((2 1) (3 2) (4 3) (5 4)))
    (equal
     (seq-into '(1 2 3 4) 'vector)
     [1 2 3 4])


### Copy, Join

    (equal
     (copy-sequence '(1 2 3))
     '(1 2 3))
    
    (equal
     (seq-concatenate 'vector '(1 2 3 4))
     [1 2 3 4])
    
    (equal
     (seq-intersection '(1 2 3) '(2 3 4))
     '(2 3))
    
    (equal
     (seq-difference '(1 2 3) '(2 3 4))
     '(1))


### Binding

    (equal
     (seq-let [first second] [1 2 3 4]
       (list first second))
     '(1 2))
    
    (let ((a nil)
          (b nil))
      (seq-setq (_ a _ b) '(1 2 3 4))
      (list a b)
      )


## Sequence Iteration


### Map a Function to List

    (equal
     (mapcar 'car '((1 2) (3 4) (5 6)))
     '(1 3 5)
     )
    
    (equal
     (mapcar (lambda (x) (aref x 0)) [[1 2] [3 4] [5 6]])
     '(1 3 5)
     )
    
    (equal
     (mapcar '1+ [0 1 2])
     '(1 2 3))
    
    (mapc
     (lambda (x)
       (insert (number-to-string x)))
     (number-sequence 1 9))
    
    (mapc 'my-update-footer
          (list "~/x1.html" "~/x2.html" "~/x3.html"))
    
    
    (let (xx)
      (setq xx (number-sequence 1 5))
      (dolist (n xx)
        (insert (number-to-string n))))


<a id="org8b15874"></a>

# Hash Table

    ;; create
    (setq xx (make-hash-table :test 'equal))
    
    ;; put
    (let ((xx (make-hash-table :test 'equal)))
      (puthash 'aa 9 xx)
      xx)
    
    ;; rm
    (let ((xx (make-hash-table :test 'equal)))
      (puthash 'aa 9 xx)
      (puthash 'bb 10 xx)
      (remhash 'aa xx)
      xx
      )
    
    ;; get
    (let ((xx (make-hash-table :test 'equal)))
      (puthash 'aa 9 xx)
      (gethash 'bb xx)
      (gethash 'bb xx 10)
      )
    
    ;; count
    (let ((xx (make-hash-table :test 'equal)))
      (puthash 'aa 9 xx)
      (hash-table-count xx)
      )
    
    ;; clear
    (let ((xx (make-hash-table :test 'equal)))
      (puthash 'aa 9 xx)
      (hash-table-count xx)
      (clrhash xx)
      (hash-table-count xx)
      )
    
    ;; map
    (setq xx (make-hash-table :test 'equal))
    (puthash "aa" 19 xx)
    (puthash "aa" 20 xx)
    (puthash "aa" 17 xx)
    (puthash "aa" 21 xx)
    
    (maphash
     (lambda (k v)
       (princ (format "%s, %s" k v))
       (princ "\n"))
     xx)
    
    ;; get keys
    (setq xx
          #s(hash-table
             size 30
             test equal
             data (
                   "aa" 3
                   "bb" 9
                   "cc" 5)))
    (require 'subr-x)
    (hash-table-keys xx)
    
    ;; get values
    (setq xx (make-hash-table :test 'equal))
    (puthash "aa" "19" xx)
    (puthash "bb" "20" xx)
    
    (require 'subr-x)
    (hash-table-values xx)


<a id="org8fbf8da"></a>

# Association List

1.  Is List
2.  Value type
3.  Each ele is a Cons Pair
    1.  (cons <key> <val>)
4.  Ordered
5.  Can have duplicate keys
6.  Hard to modify

    (list
     (cons <k1> <v1>)
     (cons <k2> <v2>)
     )
    
    '(
      (<k1> . <v1)
      (<k2> . <v2)
      )


## Create Alist

    (setq
     xx
     (list
      (cons "aa" 23)
      (cons "bb" 24)
      (cons "cc" 33)
      ))
    
    
    (setq
     xx
     '(
       ("aa" . 23)
       ("bb" . 24)
       ("cc" . 34)
       ))
    
    
    (setq
     xx
     (list
      (cons 'aa 23)
      (cons 'bb 24)
      (cons 'cc 34)
      ))
    
    (setq
     xx
     '(
       (aa . 23)
       (bb . 24)
       (cc . 34)
       ))


## Get V by K

alist-get

    (setq
     xx
     '(("aa" . 23)
       ("bb" . 24)
       ("cc" . 34)))
    (equal
     (alist-get "bb" xx 999 nil 'string-equal)
     24)
    (equal
     (alist-get "dd" xx 999 nil 'string-equal)
     999)
    
    (setq
     xx
     '((aa . 23)
       (bb . 24)
       (cc . 34)))
    (equal
     (alist-get 'bb xx 999)
     24)
    (equal
     (alist-get 'dd xx 999)
     999)


## Get Pair by K

    (setq xx
          '((aa . 23)
            (bb . 24)
            (cc . 34)))
    ;;checked by equal
    (assoc 'aa xx)
    
    (setq xx
          '((aa . 23)
            (bb . 24)
            (cc . 34)))
    ;; checked by eq
    (assq 'aa xx)


## Get Pair by V

    (setq xx
          '(("aa" . 23)
            ("bb" . 24)
            ("cc" . 34)))
    (rassoc 24 xx)
    
    (setq xx
          '((aa . 23)
            (bb . 24)
            (cc . 34)))
    (rassq 24 xx)


## Add a Ele

    (setq xx
          '(("aa" . 23)
            ("bb" . 24)))
    (push '("cc" . 33) xx)
    
    
    (setq xx
          '(("aa" . 23)
            ("bb" . 24)))
    ;; if key not exist
    (when (not (assoc "cc" xx))
      (push '("cc" . 33) xx))


## Del Pairs by K

    (setq xx
          '(("aa" . 23)
            ("bb" . 24)))
    (setq xx (assoc-delete-all "bb" xx))


<a id="org5adca01"></a>

# Function


## Define Func

    (defun ff()
      "print yay"
      (message "Yay!"))
    
    (defun gg (x)
      "add two"
      (+ x 2))
    
    (defun ff (x y)
      "add x and y"
      (+ x y))


## Func Parameters


### Optional Params

    (defun ff (aa bb &optional cc dd)
      "test optional params"
      (interactive)
      (message "%s %s %s %s" aa bb cc dd))
    
    (ff 1 2)
    (ff 1 2 3)
    (ff 1 2 3 4)


### Rest Params

1.  Emacs lisp don't support params default value.
2.  Emacs lisp don't support params type checking.

    (defun ff (aa bb &rest cc)
      "test rest arguments"
      (message "%s" cc))
    
    (ff "1" "2" "3" "4")


### Named Params

    (defun my-f (x &rest keyword-args)
      "demo of using plist as optional named params with default value"
      (interactive)
      (let ((a (or (plist-get keyword-args :a) 1))
            (b (or (plist-get keyword-args :b) 2))
            (c (or (plist-get keyword-args :c) 3)))
        (format "param values: x %s, a %s, b %s, c %s" x a b c)))
    
    (my-f 3 :b 4 :xx 9)
    
    
    (defun my-g (x &optional xOpt)
      "demo of using alist as optional named param with default value"
      (interactive)
      (let ((y1 (or (cdr (assoc "y1" xOpt)) 1))
            (y2 (or (cdr (assoc "y2" xOpt)) 2))
            (y3 (or (cdr (assoc "y3" xOpt)) 3))
            )
        (message "param values: x %s, y1 %s, y2 %s, y3 %s" x y1 y2 y3)
        ))
    
    ;; Association list
    (my-g 3 '(("y2" . 99)))


## Lambda (Anonymous Function)


### Define Lambda

    (lambda (x)
      (1+ x))
    
    (lambda (x)
      "toy lambda example. given x, return (list 1 2 3 x)"
      (let (a b c)
        (setq a 1)
        (setq b 2)
        (setq c 3)
        (list a b c x)))


### Apply the Lambda to Value

    ((lambda (x)
       (1+ x)) 3)
    
    ;; general use case
    (mapcar
     (lambda (x) (aref x 1))
     [[1 2] [3 4] [5 6]])
    
    (lambda (x y)
      (+ x y))
    
    ((lambda (x y)
       (+ x y))
     3 4)


### Nested Lambda

    ((lambda (x)
       ((lambda (x)
          (1+ x)) x)) 3)


### Nmaed Lambda

    (fset 'f1 (lambda (y) "add 1 to arg" (1+ y)))
    (f1 2)


### Define Inner Function

    (defun f1 (x)
      "DOCSTRING"
      (interactive)
      (let (f2)
        ;; fest wil make f2 to global
        (fset 'f2 (lambda (y) "add 1 to arg" (1+ y)))
        (f2 x)))
    
    (equal
     (f1 2)
     3)
    
    (equal
     (fboundp 'f2)
     t)
    
    (equal
     (f2 2)
     3)


### Later invoke

    (setq my-f (lambda (x y ) (+ x y)))
    (equal
     (funcall my-f 1 2)
     3)
    
    ;invalid
    ;; (my-f 1 2)


## Function Type

1.  lambda
2.  primitive
3.  special form
4.  macro
5.  command
6.  function


### Check Symbol's type

    (special-form-p 'progn)
    (macrop 'when)
    (commandp 'count-words)
    (functionp 'buffer-file-name)
    ;; is variable
    (boundp 'buffer-file-name)


### Check Primitive

    ;; lisp
    (subrp (symbol-function 'list))
    (subrp (symbol-function '+))
    
    ;; form by C
    (subrp (symbol-function 'while))
    (subrp (symbol-function 'save-excursion))
    
    ;; command by C
    (subrp (symbol-function 'goto-char))
    (subrp (symbol-function 'beginning-of-line))
    (subrp (symbol-function 'forward-word))
    
    ;; lambda is a macro
    (subrp (symbol-function 'lambda))
    
    ;; return cell value
    (symbol-function 'setq)

> Search all use **apropos**


## Prefix funcion

We can use **-, +, \*** in names

    ;; (1+ x) is the same as (+ x 1).
    (equal
     (1+ 42)
     43)
    
    ;; (1- x) is the same as (- x 1). Note that the short name may be confusing: (1- x) does not mean 1-x; rather, it means x-1.
    (equal
     (1- 100)
     99)


## Local function

    (flet ((go (x) (+ 2 x))) (go 3))


<a id="org2a02caf"></a>

# Exit


## Exit a Func/Iteration

1.  throw
2.  cache

    (defun xx-test-exit (x)
      (catch 'aaa
        (if (> x 5)
            (progn
              (throw 'aaa "yes"))
            (progn
              "no"))))
    (string-equal (xx-test-exit 2) "no")
    (string-equal (xx-test-exit 6) "yes")
    
    (let ((xseq [0 1 2 3 4 5]))
      (catch 'bbb
        (mapc
         (lambda (x)
           (message "%s" x)
           (when (equal x 3) (throw 'bbb x)))
         xseq)
        nil))
    (seq-some (lambda (x) (eq 5 x)) [4 5 6])


## Exit by Error

1.  error
2.  user-error

    (defun test-exit-f ()
      (interactive)
      (if (y-or-n-p "invoke user-error to exit?")
          (user-error "Error, because: %s" "you said so!")
        (progn
          (message "went on"))))


<a id="org92eaace"></a>

# Apply Function(List to Args)


## apply

    (defun ff (x y z)
      (format "%s %s %s" x y z))
    
    (equal
     (ff 2 3 4)
     "2 3 4")
    
    (setq xx '(2 3 4))
    (equal
     (apply 'ff xx)
     "2 3 4")
    
    (setq xx '(3 4))
    (equal
     (apply 'ff 2 xx)
     "2 3 4")


## funcall

1.  When function name is a variable, value known only at run-time.

    (defun ff (x y z)
      (format "%s %s %s" x y z))
    
    (equal
     (ff 2 3 4)
     "2 3 4")
    
    (equal
     (funcall 'ff 2 3 4)
     "2 3 4")


<a id="orgd1afd11"></a>

# Symbol

1.  like common language identifer
2.  held unevaluated
3.  store multiple values
4.  symbolic, variable or function name is value and symbol
    1.  transform source code at runtime

    (setq x 4)
    
    (set
     (intern
      (concat
       (symbol-name 'x)
       (number-to-string (symbol-value 'x))))
     (1+ (symbol-value 'x)))
    
    (symbol-value 'x4)


## Quoting Symbol

1.  quote
    1.  return argument without evaluating it.
    2.  hold evaluation

    ;; (set x 3)
    (setq x 3)
    
    (setq f 'cos)
    (setq f 'sqrt)
    
    (mapcar 'cos '(1 2 3))
    
    (mapcar f '(1 2 3))


## Symbol cell

1.  print name
    1.  string
2.  value
    1.  symbol's value
3.  function
    1.  function definition object
4.  property list
    1.  list of name/value pairs


<a id="orgabca074"></a>

# Special Form

Non-standard evaluation strategy

1.  and
2.  or
3.  catch
4.  while
5.  cond
6.  condition-case
7.  defconst
8.  let
9.  let\*
10. prog1
11. prog2
12. progn
13. setq
14. setq-default
15. interactive
16. lambda
17. quote
18. function
19. save-current-buffer
20. save-excursion
21. save-restriction
22. track-mouse
23. unwind-protect


<a id="org53df814"></a>

# Cheeck If func/var is defined


## Check Func

    (equal
     (fboundp 'info)
     t)
    (equal
     (fboundp 'setq)
     t)
    (equal
     (fboundp 'xyx)
     nil)


## Check Variable

    (equal
     (boundp 'auto-mode-alist)
     t)
    (equal
     (boundp 'default-input-method)
     t)
    (equal
     (boundp 'nil)
     t)
    (equal
     (boundp 'xyz)
     nil)


## Check Package(Feature)

    (equal
     (featurep 'ibuffer)
     nil)
    (equal
     (featurep 'org)
     t)


<a id="orgd782919"></a>

# Regular Expression


## Regex Functions


### on Buffer

-   search-forward

-   re-search-forward

        (let ((case-fold-search nil))
          (re-search-forward "[0-9])+"))
        ;; 100 cat

-   re-search-backward

-   skip-chars-forward

-   skip-chars-backward


### Matching String

-   string-match

        (equal
         (string-match "3" "xx3x")
         2)

-   replace-regexp-in-string

        (equal
         (replace-regexp-in-string "</*div>" "<p>" "<div>something</div>")
         "<p>something<p>")


### Replace Match

    (let ((case-fold-search nil))
      (re-search-forward "x\\([0-9]+\\)" nil t)
      (replace-match "ID \\1"))
    
    ;; x803 -> ID803


<a id="orgec6c3db"></a>

# DateTime


## Format Date

    (format-time-string "%Y-%m-%d")


## Unix Time Format

    (format-time-string "%s")


## Get Named Month And Week

    (format-time-string "%B")
    (format-time-string "%b")
    
    (format-time-string "%A")
    (format-time-string "%a")


## Ordernal Date Format

    (format-time-string "%Y-%j")


## Parse Date Time

1.  parse-time-string returns
2.  (SEC MIN HOUR DAY MON YEAR DOW DST TZ)
3.  if a element is nil or -1, it means unknown

    (equal
     (parse-time-string "Date: Mon, 01 Aug 2011 12:24:51 -0400")
     '(51 24 12 1 8 2011 1 -1 -14400))
    
    (equal
      (parse-time-string "2007, August 1")
     '(nil nil nil 1 8 2007 nil -1 nil))


<a id="org0546f30"></a>

# Builtin Fucntions


## &rest

\`&rest\` is a way of specifying that the final arguments to a function can be of any type, and can be passed as a variable number of arguments. It is commonly used in Emacs Lisp code to define functions that can be called with a variable number of arguments.


## pop


## aref


## elt


## throw


## catch


## caar

Get first ele of first set

    (setq my-list '((1 2) (3 4) (5 6)))
    (setq result (caar my-list))
    (equal result 1)


## assoc

Find matched list from list by the key

    (setq trees '((pine . cones) (oak . acorns) (maple . seeds)))
    
    (equal
     (assoc 'oak trees)
     '(oak . acorns))
    ;; 返回 (oak . acorns)
    
    (equal
     (cdr (assoc 'oak trees))
     'acorns
     )
    ;; 返回 acorns
    
    (equal
     (assoc 'birch trees)
     nil)
    ;; 返回 nil


## regexp-opt

Generate simple regex expression for string list, it endeavor to optimistic reg results for speed

    (regexp-opt '("alex" "albert" "alois" "bummer"))


## identity


<a id="org8e385c5"></a>

# Find Document


## aprops

List all Symbol


## apropos-command

List all command


## apropos-variable

List all variable


## apropos-value

List all variable names value


<a id="org701b33e"></a>

# Hook

1.  is a variable
2.  value is a list of functions
3.  like event
4.  each Major Mode usually have at least 1 hook.
5.  avoid using lambda
    1.  unreadable
    2.  can't be removed using **remove-hook**


<a id="org3e935b4"></a>

# Search In Manual


## elisp-index-search

Search lisp manual


## emacs-index-search

Search emacs manual


<a id="org3ae19ee"></a>

# Code Navigate Command

I think vim action can replace below command perfectly.


## backward-sexp


## forward-sexp


## backward-up-list


## down-list


## backward-list


## forward-list


<a id="org98e717f"></a>

# Write Major Mode


## What is it?

1.  a collectiong of emacs behaviors.
2.  basic mode is **fundamental-mode**


## List Major modes

1.  apropos-command, type "-mode"
2.  look variable **auto-mode-alist**


## Set Default Major Mode


### Set New Empty Buffer Mode

    (setq initial-major-mode 'python-mode)


### Remap a Default Major Mode

    (if (< emacs-major-version 29)
        (add-to-list 'auto-mode-alist '("\\.css\\'" . xah-css-mode))
      (add-to-list 'auto-mode-alist '(css-mode . xah-css-mode)))


### Associate Major Mode by File Name Extension

    (add-to-list
     'auto-mode-alist
     '("\\.html?\\'" . xah-html-mode))


### Remove File Extension Association

    (setq auto-mode-alist (rassq-delete-all 'js-mode auto-mode-alist))
    
    ;; check if mode is in the list
    (rassoc 'js-mode auto-mode-alist)


### Associate Major Mode by First Line in File

    (add-to-list 'magic-mode-alist '("<!doctype html>" . xah-html-mode))
    (add-to-list 'magic-mode-alist '("<!DOCTYPE html>" . xah-html-mode))


### How Emacs Determines Which Major Mode to Load

1.  file first line contain "-**- mode: xx-**-"
2.  unix “shebang” syntax (For example, #!/usr/bin/perl)
3.  first line with **magic-mode-alist**
4.  file name with **auto-mode-alist**


## Major Mode for Syntax Coloring

    (setq mymath-highlights
          '(("Sin\\|Cos\\|Sum" . 'font-lock-function-name-face)
            ("Pi\\|Infinity" . 'font-lock-constant-face)))
    
    (define-derived-mode mymath-mode fundamental-mode "mymath"
      "major mode for editing mymath language code."
      (setq font-lock-defaults '(mymath-highlights)))


### Test Code

    Sin[x]^2 + Cos[y]^2 == 1
    Pi^2/6 == Sum[1/x^2,{x,1,Infinity}]


### Mode for a Language that Has ample keywords

    (setq mylsl-font-lock-keywords
          (let* (
                (x-keywords '("break" "default" "do" "else" "for" "if" "return" "state" "while"))
                (x-types '("float" "integer" "key" "list" "rotation" "string" "vector"))
                (x-constants '("ACTIVE" "AGENT" "ALL_SIDES" "ATTACH_BACK"))
                (x-events '("at_rot_target" "at_target" "attach"))
                (x-functions '("llAbs" "llAcos" "llAddToLandBanList" "llAddToLandPassList"))
    
                (x-keywords-regexp (regexp-opt x-keywords 'words))
                (x-types-regexp (regexp-opt x-types 'words))
                (x-constans-regexp (regexp-opt x-constants 'words))
                (x-events-regexp (regexp-opt x-events 'words))
                (x-functions-regexp (regexp-opt x-functions 'words)))
            ;;The `( ,a ,b …) is a lisp special syntax to evaluate parts of elements inside the list. Inside the paren, elements preceded by a , will be evaluated.
            `(
              (,x-types-regexp . 'font-lock-type-face)
              (,x-constans-regexp . 'font-lock-constant-face)
              (,x-events-regexp . 'font-lock-builtin-face)
              (,x-functions-regexp . 'font-lock-function-name-face)
              (,x-keywords-regexp . 'font-lock-keyword-face)
              )
            ))
    
    (define-derived-mode mylsl-mode c-mode "lsl mode"
      "Major mode for editing LSL"
    
      (setq font-lock-defaults '(mylsl-font-lock-keywords)))

-   Test Code

        // sample LSL file
        
        // Examples of variable declaration and assignment:
        integer score = 0;
        string mySay = "i ♥ you";
        vector v = <3,4,5>;
        list myList= [2,4,7,3];
        
        // Example of defining a function.
        // built-in function's names start with “ll” (Linden Library).
        integer sum(integer a, integer b)
        {
            integer result = a + b;
            return result;
        }
        
         default
         {
             state_entry()
             {
                 llSay(0, mySay);
             }
        
             touch_start(integer total_number)
             {
                 if (score == 1) {
                     llSay(0, mySay);
                 } else {
                     llWhisper(0, "Ouch!");
                 }
             }
         }


## Font Lock Mode


### Font-lock-mode

1.  buffer-local minor mode
2.  default for all buffers
3.  high-level API
4.  color text in two ways:
    1.  Syntactic fontification
    2.  Search based fotification
5.  2 things to do coloring job
    1.  Syntax Table
    2.  font-lock-defaults


### font-lock-defaults

1.  buffer local variable
2.  designed as a config for the purpose of syntax coloring


### font-lock-defaults Value Structure

1.  font-lock-keywords
2.  font-lock-keywords-only
3.  font-lock-keywords-case-fold-search
4.  font-lock-syntax-table


### Sample

    (defvar my-highlights nil "first elefor `font-lock-defaults`")
    
    (setq my-highlights
          '(("<h1>\\|</h1>" . 'font-lock-function-name-face)
            ;; 1 means match regex group 1
            ("<h1>\\([^<]+?\\)</h1>" . (1 'font-lock-constant-face))))
    
    (define-derived-mode myhtml-mode fundamental-mode "my"
      "major mode for editing my language code."
      (setq font-lock-defaults '(my-highlights)))

    <h1>something</h1>


## Search Web Command

    (require 'browse-url)
    
    (defun my-lookup-wikipedia ()
      (interactive)
      (let (word)
        (setq word
              (if (use-region-p)
                  (buffer-substring-no-properties (region-beginning) (region-end))
                (current-word)))
        (setq word (replace-regexp-in-string " " "_" word))
        (browse-url (concat "http://en.wikipedia.org/wiki/" word))))


## Create Hook

    2023-12-05 16:12(defvar xah-html-browse-url-of-buffer-hook nil
     "Hook for `xah-html-browse-url-of-buffer'. Hook functions are called before switching to browser.")
    
    (defun xah-html-browse-url-of-buffer ()
      "View current buffer in default browser, but save first.
    Hook `xah-html-browse-url-of-buffer-hook' is run before saving and before opening in browser.
    Version 2020-06-26 2021-06-26"
      (interactive)
      (let (($url (buffer-file-name)))
        (run-hooks 'xah-html-browse-url-of-buffer-hook)
        (when (buffer-modified-p) (save-buffer))
        (print $url)
        (browse-web $url )))
    
    (add-hook 'xah-html-browse-url-of-buffer-hook 'xah-insert-date)


## Keyword Completion

1.  complete-symbol
2.  completion-at-point


### completion-at-point

Add completion function to the list **completion-at-point-functions**

    (setq xx-keywords
          '("touch"
            "touch_start"
            "touch_end"
            "for"
            "foreach"
            "forall"))
    
    (defun xx-completion-at-point()
      "This is the function to be used for the hook `completion-at-point-functions'"
      (interactive)
      (let* (
             (bds (bounds-of-thing-at-point 'symbol))
             (start (car bds))
             (end (cdr bds)))
        (list start end xx-keywords . nil)))
    
    (define-derived-mode xx-mode c-mode "xx"
      "Major mode for editing xx lang code."
      (add-hook 'completion-at-point-functions 'xx-completion-at-point nil 'local))


### try-completion

Return the maximal match

    (equal (try-completion
            "c"
            '(
              "amc"
              "amb"))
           nil)
    
    
    (equal (try-completion
            "amb"
            '(
              "amc"
              "amb"))
           t)
    
    (equal (try-completion
            "ah"
            '(
              "amc"
              "amb"
              "ahu"))
           "ahu")
    
    (equal (try-completion
            "a"
            '(
              "amc"
              "amb"))
           "am")


### all-completions

Returns a list of all matches

    (equal
     (all-completions
      "c"
      '(
        "amc"
        "amb"
        ))
     nil)
    
    (equal
     (all-completions
      "amb"
      '(
        "amc"
        "amb"
        ))
     '("amb"))
    
    (equal
     (all-completions
      "ah"
      '(
        "amc"
        "amb"
        "ahu"
        ))
     '("ahu"))
    
    (equal
     (all-completions
      "a"
      '(
        "amc"
        "amb"
        ))
     '("amc" "amb"))


## Major Mode Names


### name own major mode "xx"

1.  For all Symbols, should start with "xx-"
2.  File name should be "xx-mode.el"
3.  Command name to invoke the mode should be "xx-mode"
4.  Package's feature name should be "xx", (provide 'xx)


### Value of Varialbe "major-mode"

major-mode is built-in Buffer Local Variable

1.  Value is a Lisp Symbol
2.  Value is use to check current major mode
3.  Value is as the command name
4.  Value is automatically set when use **define-derived-mode**


## Provide, require, features


### features

Global variable, value is list of Symbols


### provide

Add symbol to features list


### require

load symbol


## Load


### load

Read and eval a file

Search rule

1.  File has suffix, search file in variable "load-path"
2.  no suffix, find order is:
    1.  filename.elc
    2.  filename.el
    3.  filename


### load-file

Load one specific file, file should be full path


### autoload

Associates a function name with a file path, and load the file and execute the function when a function is called.

it can save startup time.


## No Namespace

Elisp no namespace, everything is global.


<a id="org22301d5"></a>

# Character Type


## Char Syntax

    (equal 97 ?a)
    (equal 97 (string-to-char "a"))


## Char Func

1.  char-before
2.  char-after
3.  char-to-string
4.  string-to-char
5.  char-equal


<a id="org65cbd02"></a>

# Syntax Table


## Syntax Table is Local to Buffer

Each buffer has its own version of syntax table.


## View Current Syntax Table

Use **describe-syntax**

1.  leat is char
2.  middle is the char's syntax class abbreviation


## Syntax Classes

Each syntax class is identified by a 1-char code.


## Determine Cursor position


### Check If Cursor is inside String

    (nth 3 (syntax-ppss))


### Check If Cursor is inside Comment

    (nth 4 (syntax-ppss))


## Find Matching Bracket Char

    (defun xah-get-matching-bracket (@bracket-char-string)
      ""
      (interactive)
      (let (($syntableValue (aref (syntax-table) (string-to-char @bracket-char-string))))
        (if (or
             (eq (car $syntableValue ) 4) ; syntax table, code 4 is open bracket
             (eq (car $syntableValue ) 5) ; syntax table, code 5 is close bracket
             )
            (char-to-string (cdr $syntableValue))
          nil
            )))
    
    (xah-get-matching-bracket "(") ; ")"
    (xah-get-matching-bracket ")" ) ; "("
    (xah-get-matching-bracket "[" ) ; "]"
    (xah-get-matching-bracket "]" ) ; "["
    (xah-get-matching-bracket "「" ) ; "」"
    (xah-get-matching-bracket "」" ) ; "「"
    (xah-get-matching-bracket "【" ) ; "】"
    (xah-get-matching-bracket "】" ) ; "【"


<a id="org5849cfe"></a>

# Sample


## Write a variable which is list type to file

    (defun alist-to-string (alist)
      "Convert an association list to a string, with each key-value pair on a separate line."
      (mapconcat (lambda (pair)
                   (format "| `%s` | `%s` |" (car pair) (cdr pair)))
                 alist
                 "\n"))
    
    (write-region (alist-to-string (symbol-value 'eaf-file-manager-keybinding)) nil "output.md")


<a id="orgbdfe962"></a>

# Quotes

Quote 'x refer to the name rather then the value of x. 'x ≈ (quote x).

    '(+ 1 2) ;; result (+ 1 2)


<a id="orgd2d6fcf"></a>

# Macro

Create new function that language doesn't give.

1.  Happens before runtime

    (defmacro let1 (var val &rest body) `(let ((,var ,val)) ,@body))
    ;; macroexpand for debug
    (macroexpand '(let1 x "5" (message x)))
    
    ;; not use progn
    ;; No progn; (first x y z) ≈ x
    (defmacro first (&rest body)
     (car `,@body))
    (first 1 2 3)
    (macroexpand '(first x y z))
    
    ;; use progn
    (defmacro not-first (&rest body) `(progn ,@(cdr `,@body)))
    (macroexpand '(not-first x y z))
    ;; `,@body       ⇒ (x y z)
    ;; (cdr `,@body) ⇒ (y z)
    ;; `(progn ,@(cdr `,@body))
    ;;        ⇒ (progn y z)

