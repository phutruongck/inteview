> # React Component

`1 component là một block code độc lập, có thể tái sử dụng, nó chia UI thành nhiều phần nhỏ. Một web page hoặc UI từ nhiều block code(components). Componet sẽ luôn lắng nghe sự thay đổi của STATE để render lại UI cho người dùng.`

`Việc chia source code thành các components giúp ta rất nhiều. Mỗi component có code JS và CSS riêng, chúng có thể tái sử dụng, dễ đọc, dễ viết, dễ test. React có 2 loại component: Funtional (Stateless) và Class (Stateful).`

> ## Class Component

`Class components là những class ES6. Chúng phức tạp hơn functional components ở chỗ nó còn có: phương thức khởi tạo (constructor), life-cycle, hàm render() và quản lý state (data).`

1. Là một class ES6, nó sẽ là một component khi nó "kế thừa" React.Component.
2. Có thể nhận props (trong hàm khởi tạo) nếu cần.
3. Được khởi tạo với 1 vòng lifecycle hoàn chỉnh.
4. Phải có 1 method render() trả về 1 React element (JSX), or null.

> ## Functional Component

`1 functional component là một hàm Javascript (hoặc ES6) trả về 1 phần tử/1 element React. Theo official docs của React, hàm dưới đây là một component React hợp lệ: Function này là một component React hợp lệ vì nó nhận một "props" (viết tắt của properties) làm tham số và trả về 1 React element.`

1. Một function Javascript / ES6 function
2. Phải trả về 1 React element
3. Nhận props làm tham số nếu cần

> ## Sự khác nhau giữa Class Component vs Functional Component

### 1. Class Component

`Class Component - Stateful Components: Với Class Component chúng ta có thể sử dụng được state một cách dễ dàng khi khởi tạo (init) state ngay trong phương thức constructor của Class Component bằng this.state`

### 2. Functional Component

`Functional Component - Stateless Components: Trái ngược với Class Component, Functional Component trước đây vốn không thể làm những thứ phức tạp như làm việc quản lí với state. Nhưng với những bản mới nhất của React đã cập nhật thêm React Hooks để cho phép chúng ta làm việc đó thông qua những function như useState() . Các ban có thể vào trang chủ của React để đọc chi tiết về chúng. Những bài viết sau trong series này mình sẽ đề cập về hooks hay lifecycles của Component.`
