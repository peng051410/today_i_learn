
# Table of Contents

-   [eval](#org514934c)
-   [Output](#org4edd338)
-   [buffer](#org0983881)
-   [String](#org373562b)
-   [Arithmetic](#org170f827)
-   [Boolean](#orgc1bfe69)
-   [Test equality](#orge873d75)
-   [Variables](#org437ab81)
-   [Block Expression](#org0ee40a2)
-   [Condition](#org419bcfa)
-   [Loop](#org99526ad)
-   [List](#orgea5044c)
-   [Vector](#org2b784f2)
-   [Sequence](#orgf945699)
-   [Hash Table](#org18c2053)
-   [Association List](#orgf6209ba)
-   [Function](#org577a840)
-   [Fucntions](#org328704b)



<a id="org514934c"></a>

# eval


## eval-last-sexp


## eval-region


<a id="org4edd338"></a>

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


<a id="org0983881"></a>

# buffer


## generate-new-buffer


## switch-to-buffer


## with-output-to-temp-buffer

> (with-output-to-temp-buffer BUFNAME &rest BODY)


<a id="org373562b"></a>

# String


## length


## substring


## concat


## split-string


## format


<a id="org170f827"></a>

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


<a id="orgc1bfe69"></a>

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


<a id="orge873d75"></a>

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


<a id="org437ab81"></a>

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


<a id="org0ee40a2"></a>

# Block Expression

Like block {} in C-like language

    (progn
      (message "a")
      (message "b"))
    
    (progn 3 5)

<div class="notes" id="orga8757ea">
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


<a id="org419bcfa"></a>

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


<a id="org99526ad"></a>

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


<a id="orgea5044c"></a>

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


<a id="org2b784f2"></a>

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


<a id="orgf945699"></a>

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


<a id="org18c2053"></a>

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


<a id="orgf6209ba"></a>

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


<a id="org577a840"></a>

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


<a id="org328704b"></a>

# Fucntions


## &rest

\`&rest\` is a way of specifying that the final arguments to a function can be of any type, and can be passed as a variable number of arguments. It is commonly used in Emacs Lisp code to define functions that can be called with a variable number of arguments.


## pop


## aref


## elt


## throw


## catch

