> # Middleware

- `Trong quá trình thao tác với state, có nhiều vấn đề khác xảy ra, ví dụ như bất đồng bộ. Ví dụ: có một action call API, đây là một action bất đồng bộ, vậy phải đợi cho qua trình này thực hiện xong mới tiến hành dispatch vào reducer.`

- `Reducer không thể xử lý các hàm như setTimeout, setInterval.`

- `Middleware như là thành phần đứng giữa action và reducer để xử lý các side effect (ví dụ như trên)`

> ## Redux-Thunk

- `Về action trong redux chỉ đơn thuần trả về plain object có chứa 1 field là type, và payload.`

- `Redux-thunk là một middleware cho phép action trả về một function thay vì plain object.`

- `Ví dụ: Ta cần call api login, đầu tiên ta dispatch 1 action để thông báo rằng dữ liệu đang được gửi đi, nếu thành công, dispatch 1 action thông báo thành công và nếu thất bại, dispatch 1 action thông báo thất bại.`

> ## Redux-Saga

- `Cũng tương tự như redux-thunk, saga cung cấp cho chúng ta các hàm helper effect, nó trả về một effect object chứa các thông tin giúp cho redux có thể thực hiện các hành động khác.`

- `Các hàm helper effect này sẽ được thực thi trong các generator function.`

- `Generator function (ES6) là một function đặc biệt, nó có thể tạm dừng để thực thi một việc khác, hoặc gọi đến một generator khác.`

- `Một số helper của generator function trong redux-saga:`

1. takeEvery(): thực thi và trả về kết quả của mọi actions được gọi.
2. takeLastest(): Nếu chúng ta thực hiện nhiều actions, nó sẽ chỉ thực thi và trả về kết quả của actions cuối cùng.
3. take(): tạm dừng cho đến khi nhận được actions.
4. put(): dispatch một action.
5. call(): gọi function, nếu trả về một promise, tạm dừng saga cho đến khi promise được giải quyết.
6. race(): chạy nhiều effect đồng thời, sau đó huỷ tất cả nếu một trong số đó kết thúc.
