> # React Suspense

## 1. Concurrent Mode

    Đây là một kỹ thuật cho phép chúng ta thực hiện một số công việc (như fetch data từ api) song song với quá trình render component.

    Nó giúp tăng tốc trang web khi load dữ liệu từ server, đặc biệt với các thiết bị low-end như mobile. Lưu ý rằng API của concurrent mode vẫn còn đang trong quá trình thử nghiệm.

## 2. React.Suspense

    Trong React, một khi bạn muốn fetch data thì bạn sẽ làm như thế nào? Có phải là bạn sẽ gọi API trong React.useEffect, có nghĩa là bạn gọi API sau khi component đã render.

    Vậy liệu có cách nào bạn vừa render app và vừa fetch data. Với concurrent mode bạn sẽ làm được điều đó. Điều này sẽ giúp bạn tận dụng tối đa thời gian để fetch data trước khi component render. Bạn sẽ gọi API trước và chuẩn bị sẵn sàng data để render component. Nó giúp giảm thời gian render component. Thậm chí bạn có thể fetch data trước khi toàn app render.

```
function Component() {
    if (data) {
        return <div>{data.message}</div>
    }

    throw promise
        // React sẽ theo dõi throw promise và tìm "Suspense" component gần nhất
        // và chờ quá trình render cho đến khi promise được hoàn thành
    }

    ReactDOM.createRoot(rootEl).render(
        <React.Suspense fallback={<div>loading...</div>}>
            <Component />
        </React.Suspense>,
    )
```

    React.Suspense sẽ chờ một cái gì đó (gọi API) hoàn thành trước khi component có thể render và trong thời gian chờ nó sẽ hiển thị fallback. Khi wrap component bên trong React.Suspense thì component sẽ chờ cho đến khi promise được hoàn thành, sau đó component mới được render.

    Và tất nhiên là React chỉ chờ một mình <Component />, những component khác trong app được render bình thường.
