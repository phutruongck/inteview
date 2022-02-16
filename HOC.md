> # HOC (Higher-order Component)

    Là một hàm mà nhận vào một component, và trả về một component khác.

    Chú ý rằng, HOC không chỉnh sửa component ban đầu(Wrapper Component) mà nó chỉ bọc component gốc trong một Container. Sau đó nó sẽ truyền thêm một số data, props xuống cho Wrapped Component. HOC không quan tâm dữ diệu được sử dụng như thế nào. Cũng như Wrapped Component không quan tâm data, props đến từ đâu. Nó chỉ việc gọi HOC và xài dữ liệu được truyền từ HOC.

    HOC nên là một pure function nên nó không được phép chỉnh sửa input, và không có side-effect.

> ## Một vài HOC trong React

1. React.memo
2. React.forwardRef
