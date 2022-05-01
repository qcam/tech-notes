# Homoiconicity (tính đồng tượng)
#programming-language #homonicity #lisp

Một ngôn ngữ lập trình được coi là **homoiconic** nếu như chương trình viết bằng ngôn ngữ đó có thể được thao tác (manipulate) như data.

Đại khái là "code as data".

Ví dụ như Lisp, bạn có thể manipulate code như là data.

```lisp
(define (fib n)
    (cond
      ((= n 0) 0)
      ((= n 1) 1)
      (else
        (+ (fib (- n 1))
           (fib (- n 2))))))
```

Về mặt homoiconicity, code này chỉ là 1 list gồm 3 phần tử.

### Một số câu hỏi tự đặt tự suy ngẫm tự trả lời 🤔

##### Vậy Elixir có phải là một ngôn ngữ homoiconic hay không?

Câu trả lời ngắn là không.

Câu trả lời dài hơn thì mặc dù macros của Elixir khá mạnh và bạn có thể thao tác với AST của Elixir thông qua macros. Nhưng ngôn ngữ Elixir không phải là homoiconic.

Tóm lại, Elixir AST là homoiconic, nhưng Elixir thì không. Mà bạn thì code bằng Elixir chứ không code bằng Elixir AST.

Xem thêm tại: http://www.petecorey.com/blog/2017/08/07/what-if-elixir-were-homoiconic/