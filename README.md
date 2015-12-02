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
