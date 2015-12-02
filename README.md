# block-lambda-proc
1. Block

    Block đơn giản chỉ là tập hợp các lệnh thành một khối
    Được đặt trong dấu {...}
    Trong ruby thì block phổ biến và dễ dùng hơn so với lambda và proc
    Ví dụ 1 block
```
array = [1, 2, 3]
array.collect! do |n|
  n + 1
end
puts array.inspect
# => [2, 3, 4]
or 
[1, 2, 3].each {|x| puts x}
```
Khi sử dụng block thì có hạn chế đó là khi ta muốn thay đổi đầu vào thì ta phải viết lại toàn bộ block để hiển thị giá trị cho input mới
2. Proc

    Cấu trúc của block là đơn giản tiện dụng dễ dùng, nhưng khi ta thay đổi input thì ta lại phải viết block mới, việc này dẫn tới trùng lặp code, vì vậy ta có Proc để giải quyết vấn đề này
    1 proc thực chất là 1block được đặt tên
    Ví dụ
```
proc = Proc.new {|x| puts x + 1}
```
Gọi proc

  Đối với input truyền vào là 1 mảng 
  ```
  [1, 2, 3].each(&proc)
  ```
  Với 1 giá trị có thể gọi 
  ```
  proc.call(2)
  ```
