Позволяет еще легче писать асинхронный код

**Запуск задач**
- static \<U> CompletableFuture \<U> supplyAsync(Supplier \<U>) - Запускается задача с функцией supplier, и результат выполнения записывается во фьючерс.
- static \<U> CompletableFuture \<U> supplyAsync(Supplier \<U>, ExecutorService) - Запускается задача с функцией supplier, на переданном ExecutorService
- static CompletableFuture \<Void> runAsync(Runnable)
- static CompletableFuture \<Void> runAsync(Runnable, ExecutorService) - аналоги supplyAsync, но с Runnable
**Запуск обработка результата**
- CompletableFuture \<U> thenApply(Function\<? super T, ? extends U>) - функция, которая принимает значение из первого future, обрабатывает его и записывает новое значение в результирующий future
- CompletableFuture \<Void> thenAccept(Consumer\<? super T> block) - функция, принимает значение из первого future и обрабатывает без возвращаемого значения
- static CompletableFuture \<Object> anyOf(CompletableFuture\<?> cfs) - Возвращает новый future,  который завершится когда хотя-бы один из данных завершится
- static CompletableFuture \<Object> allOf(CompletableFuture\<?> cfs) - Возвращает новый future,  который завершится когда все из данных завершатся