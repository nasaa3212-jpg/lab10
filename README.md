mvn test

коммандаар тестийг ажиллуулна. Үр дүнгийн тайлан терминаль дээр харагдах ёстой.

mvn site 

коммандаар JaCoCo тайланг target/site дотор хуулах бөгөөд index.html-г нээж JaCoCo тайланг харна.

## Lab10-2: Testing

Энэ лабораторийн хүрээнд `IntQueue` интерфэйсийн шаардлагад үндэслэн unit test-үүд бичсэн. Эхлээд queue хоосон эсэх, enqueue/dequeue дараалал, peek, clear зэрэг үндсэн үйлдлүүдийг specification testing аргаар шалгасан.

Дараа нь `ArrayIntQueue` классын дотоод хэрэгжилтийг structural testing аргаар шалгаж, array дүүрээд resize хийх үед FIFO дараалал зөв хадгалагдаж байгаа эсэхийг тусгайлан тестэлсэн.

Зассан алдаанууд:

1. `isEmpty()` method `size >= 0` гэж үргэлж true буцааж байсан. Үүнийг `size == 0` болгож зассан.
2. `peek()` method хоосон queue дээр null буцаах ёстой боловч array-ийн default 0 утгыг буцааж байсан. Хоосон үед null буцаадаг болгосон.
3. `ensureCapacity()` method wrap-around болсон өгөгдлийг шинэ array руу буруу index дээр хуулж байсан. Resize хийхэд queue-ийн FIFO дараалал алдагдахгүй байхаар зассан.

Тест ажиллуулах команд:

```text
mvn test
```
