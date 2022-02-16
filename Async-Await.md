> # Đồng bộ (Synchronous)

    Trong quá trình thực thi code, hệ thống sẽ đọc code từ trên xuống dưới, dòng lệnh trên xong thì sẽ thực hiện dòng lệnh dưới.

> # Bất đồng bộ (Asynchronous)

    Khác với đồng bộ, quá trình này sẽ thực hiện không theo thứ tự từ trên xuống dưới.
    Ví dụ: Khi call API login, quá trình này sẽ được xử lý và đợi 1 khoảng thời gian, trong khi đợi kết quả trả về từ API login, ứng dụng sẽ thực thi tiếp các dòng lệnh bên dưới.

    Một số hàm bất đồng bộ trong javascript: setTimeout, setInterval, onclick, scroll, ...

> # Các hàm xử lý bất đồng bộ

## 1. Callback

    Callback hiểu đơn giản là khi truyền hàm A vào hàm B dưới dạng một tham số.

## 2. Promise (ES6)

    Như một "lời hứa" thực hiện một công việc nào đó.
    Ví dụ: khi gọi một api, ta cần chờ một khoảng thời gian nào đó, trong lúc đó ta có thể làm việc khác. Sau khi xử lý xong, sẽ có trường hợp thành công (resolve), trường hợp thất bại (reject)

## 3. Async / Await
