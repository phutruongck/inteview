> # Redux

- `Trước khi redux ra đời, muốn truyền data từ component này sang component khác, ta phải truyền thông qua props => bị re-render tất cả component mỗi lần data thay đổi.`

- `Điều này làm cho ứng dụng react trở lên phức tạp, khó quản lý, giảm hiệu năng.`

- `Redux ra đời để giải quyết vấn đề này, là một thư viện của javascript, không phải của riêng react. Redux giúp ta quản lý các state của ứng dụng được lưu trữ trong store và được chia sẻ tới bất kỳ component nào chúng ta muốn.`

> ## Các thành phần của Redux

1.  ### Actions

    - `Khi chúng ta muốn thực hiện một hành động nào đó (call api chẳng hạn), thì action chính là sự kiện để redux biết được chúng ta muốn thực hiện hành động đó.`
    - `Action được gửi thông qua phương thức store.dispatch()`
    - ```
      export const SET_LOGIN_API = (username, password) => {
        return {
            type: types.SET_LOGIN_API,
            payload: { username, password, },
          };
      };
      ```

2.  ### Reducers

    - `Đây là nơi redux lấy ra state hiện tại của ứng dụng, thực hiện một action, và sau đó trả về một state mới.`
    - ```
        const rootReducer = (state = {}, action) => {
            switch (action.type) {
                case types.SET_LOGIN_API: {
                    return {
                    ...state,
                    ...action.payload,
                };
                }
                default: {
                    return state;
                }
            }
        };
      ```

3.  ### Store
    `Chính là nơi lưu tất cả state của ứng dụng, chúng ta có thể truy cập, cập nhật, thêm, xoá bất cứ thứ gì trong này thông qua phương thức: store.dispatch(action())`
