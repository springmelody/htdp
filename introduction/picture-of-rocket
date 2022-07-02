#lang htdp/bsl

(require 2htdp/image)
(require 2htdp/universe)

;constants
(define WIDTH 100)
(define HEIGHT 400)
(define V 3)
(define X 50)

(define MTSCN (empty-scene WIDTH HEIGHT))
(define ROCKET (bitmap "rocket.png"))
(define ROCKET-CENTER-TO-TOP
  (- HEIGHT (/ (image-height ROCKET) 2)))

  
;functions
(define (picture-of-rocket t)
  (cond
    [(<= (distance t) ROCKET-CENTER-TO-TOP)
      (place-image ROCKET X (distance t) MTSCN)]
    [(> (distance t) ROCKET-CENTER-TO-TOP)
      (place-image ROCKET X ROCKET-CENTER-TO-TOP MTSCN)]))

(define (distance t)
  (* V t))

(animate picture-of-rocket)