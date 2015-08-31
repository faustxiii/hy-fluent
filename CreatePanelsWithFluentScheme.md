

# Introduction #

With Fluent Scheme, you  not only are able to carry out not only computation job automation, but also to make your own GUI.


# Details #

Important procedures for Panel creation.


| Procedure Name   | Usage | Commment |
|:-----------------|:------|:---------|
| cx-create-panel  | **(cx-create-panel title update-callback apply-callback)**   | return an panel item |
| cx-show-panel    | **(cx-show-panel panel)** |          |



# Example #

```
(define gui-my-demo-panel
  (let
    (
      (panel #f)
    )
    ;;; Update Callback
    (define (update-cb . args)
      ()
    )
    ;;; Apply Callback
    (define (apply-cb . args)
      ()
    )
    ;;; Creation the Panel
    (lambda args
      (if (not panel)
        ;; create a panel
        (let ()
            (set! panel (cx-create-panel "Demo Panel" apply-cb update-cb))
        )
        ;; Now show it
        (cx-show-panel panel)
      ）
    )
  )
)

;;; call the procedure
(gui-my-demo-panel)
```

# Snapshot #

![http://p.blog.csdn.net/images/p_blog_csdn_net/fox000002/EntryImages/20090919/panel2.jpg](http://p.blog.csdn.net/images/p_blog_csdn_net/fox000002/EntryImages/20090919/panel2.jpg)