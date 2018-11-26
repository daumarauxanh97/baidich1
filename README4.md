![Design Patterns dành cho mọi người](https://cloud.githubusercontent.com/assets/11269635/23065273/1b7e5938-f515-11e6-8dd3-d0d58de6bb9a.png)

***

<p align="center">
🎉 Giải thích cực kì đơn giản về design patterns! 🎉
</p>
<p align="center">
Là một chủ đề có thể  dễ dàng khiến cho tâm trí của bất kì ai lay động. Ở đây tôi sẽ cố gắng khiến cho nó in sâu trong tâm trí bạn (và có thể là cả của tôi nữa) bằng việc giải thích chúng theo cách <i>đơn giản nhất</i> có thể.
</p>

***

<sub>Xem qua [blog](http://kamranahmed.info) của tôi và tương tác trên [Twitter](https://twitter.com/kamranahmedse).</sub>

# Giới thiệu

Design patterns là giải pháp cho các vấn đề định ky,hướng dẫn xử lý các vấn đề nhất định.Chúng không phải là class,package hay library mà bạn cho vào ứng dụng của bạn và đợi điều kì diệu xảy ra.Đây là những hướng dẫn về cách giải quyết các vấn đề nhất định trong những tình huống nhất định.

  >Design patterns là giải pháp cho các vấn đề định ky,hướng dẫn xử lý các vấn đề nhất định
  
Wikipedia miêu tả chúng như là

  >Trong lĩnh vực kĩ nghệ phần mềm, một phần mềm design patterns là một giải pháp tái sử dụng chung cho một vấn đề thường xảy ra trong một ngữ cảnh cụ thể trong thiết kế phần mềm. Nó không phải là một thiết kế hoàn chỉnh có thể được chuyển trực tiếp thành mã nguồn hay mã máy. Nó là một mô tả hoặc mẫu để làm thế nào để giải quyết một vấn đề có thể được sử dụng trong nhiều tình huống khác nhau.
  
⚠️ Hãy cẩn thận
-----------------
- Design patterns không phải là giải pháp cho tất cả các vấn đề của bạn.

- Đừng cố ép buộc chúng; những điều xấu được cho là sẽ xảy ra, nếu làm như vậy.

- Nhớ trong đầu rằng Desgin patterns là giải pháp cho vấn đề,chứ không phải là giải pháp tìm ra vấn đề; vì vậy suy nghĩ quá.

- Nếu được sử dụng đúng chỗ một cách chính xác, chúng có thể là một vị cứu tinh; hoặc có thể dẫn đến một mớ code hỗn độn kinh khủng.

 >Cũng lưu ý rằng các code dưới đây là trong PHP-7, tuy nhiên điều này không cản trở bạn bởi vì các khái niệm là giống nhau.
 
 # Các kiểu của Design patterns
 
 - Creational
 
 - Structural
 
 - Behavioral
 
 # Creational Design patterns
 
 Nói một cách đơn giản
 
 >Creational Design patterns tập trung hướng tới cách khởi tạo một đối tượng hoặc một nhóm đối tượng liên quan
 
 Wikipedia nói là
 
 >Trong lĩnh vực kĩ nghệ phần mềm,Creational Design patterns là Design patterns xử lý các cơ chế tạo đối tượng, cố gắng tạo các đối tượng theo cách phù hợp với tình huống. Hình thức tạo đối tượng cơ bản có thể dẫn đến các vấn đề về thiết kế hoặc thêm độ phức tạp vào thiết kế. Creational Design patterns giải quyết vấn đề này bằng một cách nào đó kiểm soát việc tạo đối tượng này.
 
 - Simple Factory
 
 - Factory Method
 
 - Abstract Factory
 
 - Builder
 
 - Prototype
 
 - Singleton
 
 🏠 Simple Factory
--------------

Ví dụ thực tế

>Giả sử, bạn đang xây dựng một ngôi nhà và bạn cần cửa ra vào. Bạn có thể mặc quần áo thợ mộc, lấy một ít gỗ, keo, đinh và tất cả các dụng cụ cần thiết để xây cửa và bắt đầu xây dựng nó trong nhà của bạn hoặc bạn chỉ cần gọi nhà máy và cái cửa đã được xây dựng sẵn chuyển đến cho bạn để bạn không cần phải tìm hiểu bất cứ điều gì về việc làm ra cửa hay đối phó với mớ hỗn độn mà đi kèm với việc làm ra nó.

Nói một cách đơn giản

>Simple Factory chỉ đơn giản là tạo ra những phiên bản cho client mà không cần lộ ra bất kì một tý logic nào về việc khởi tạo nào tới phía client.

 Wikipedia nói là
 
 >Trong lập trình hướng đối tượng (OOP), một factory là một object để tạo các object khác - một factory chính xác là một function  hoặc method trả về các object của một nguyên mẫu hoặc class khác nhau từ các cuộc method gọi, được giả định là "mới".

Ví dụ về lập trình

Trước hết chúng ta có giao diện cửa và việc thực 

```php
interface Door
{
    public function getWidth(): float;
    public function getHeight(): float;
}

class WoodenDoor implements Door
{
    protected $width;
    protected $height;

    public function __construct(float $width, float $height)
    {
        $this->width = $width;
        $this->height = $height;
    }

    public function getWidth(): float
    {
        return $this->width;
    }

    public function getHeight(): float
    {
        return $this->height;
    }
}
```

Sau đó, chúng ta có nhà máy sản xuất cửa và trả về nó

```php
class DoorFactory
{
    public static function makeDoor($width, $height): Door
    {
        return new WoodenDoor($width, $height);
    }
}
```

Sau đó nó có thể sử dụng như sau

```php
// Make me a door of 100x200
$door = DoorFactory::makeDoor(100, 200);

echo 'Width: ' . $door->getWidth();
echo 'Height: ' . $door->getHeight();

// Make me a door of 50x100
$door2 = DoorFactory::makeDoor(50, 100);
```

**Khi nào sử dụng**

Khi tạo một đối tượng không chỉ là một vài nhiệm vụ và liên quan đến một số logic,hợp lý khi đặt nó trong một factory chuyên dụng thay vì lặp lại cùng đoạn code ở khắp mọi nơi.

🏭 Factory Method
--------------

Ví dụ thực tế

>Giả sử trong trường hợp là một người quản lý tuyển dụng.Để một người phỏng vấn cho mọi vị trí là điều không thể.Dựa trên các công việc đang tuyển,cô ấy phai quyết định và ủy nhiệm các bước phỏng vấn cho những người khác.

Nói một cách đơn giản

>Nó cung cấp một cách để ủy thác các logic về khởi tạo cho các class con. 

Wikipedia nói là

Trong lập trình dựa trên class factory method pattern là một creational pattern sử dụng các factory method để giải quyết vấn đề về khởi tạo các object mà không cần xác định chính xác class của object sẽ được tạo ra.Điều này được thực hiện bằng cách tạo ra những object thông qua việc gọi một factory method- hoặc được chỉ định trong interface và implement bởi các class con, hoặc được implement trong class cơ sở và ghi đè tùy ý bởi các class dẫn xuất - thay vì được gọi thông qua hàm khởi tạo.

**Ví dụ về lập trình**

Lấy ví dụ quản lý tuyển dụng của chúng ta ở trên. Trước hết, chúng ta có một giao diện người phỏng vấn và một số triển khai cho nó


```php
interface Interviewer
{
    public function askQuestions();
}

class Developer implements Interviewer
{
    public function askQuestions()
    {
        echo 'Asking about design patterns!';
    }
}

class CommunityExecutive implements Interviewer
{
    public function askQuestions()
    {
        echo 'Asking about community building';
    }
}
```

Bây giờ chúng ta tạo ra `HiringManager`

```php
abstract class HiringManager
{

    // Factory method
    abstract protected function makeInterviewer(): Interviewer;

    public function takeInterview()
    {
        $interviewer = $this->makeInterviewer();
        $interviewer->askQuestions();
    }
}

```

Bây giờ bất kỳ con nào cũng có thể kế thừa và cung cấp  imterviewer yêu cầu


```php
class DevelopmentManager extends HiringManager
{
    protected function makeInterviewer(): Interviewer
    {
        return new Developer();
    }
}

class MarketingManager extends HiringManager
{
    protected function makeInterviewer(): Interviewer
    {
        return new CommunityExecutive();
    }
}
```

Sau đó nó có thể sử dụng như sau

```php
$devManager = new DevelopmentManager();
$devManager->takeInterview(); // Output: Asking about design patterns

$marketingManager = new MarketingManager();
$marketingManager->takeInterview(); // Output: Asking about community building.
```

Khi nào sư dụng

>Hữu ích khi một số xử lý chung trong một class nhưng class con được yêu cầu được động trong thời gian chạy. Hay nói cách khác, khi khách hàng không biết chính xác class con nào nó có thể cần.


🔨 Abstract Factory
----------------

Ví dụ thực tế

>Mở rộng ví dụ cửa của chúng ta từ Simple Factory.  Căn cứ vào nhu cầu của bạn, bạn có thể nhận được một cánh cửa gỗ từ một cửa hàng cửa gỗ, cửa sắt từ một cửa hàng cưa sắt hoặc cửa PVC từ cửa hàng liên quan.Thêm vào đó là bạn cần người với các đặc điểm khác nhau để phù hợp với cái cửa đó, ví dụ như bạn cần một thợ mộc cho chiếc cửa gỗ, thợ hàn cho chiếc cửa sắt,... Và giờ bạn đã thấy sự phụ thuộc khác nhau giữa những chiếc cửa, cửa gỗ cần thợ mộc, cửa sắt cần thợ hàn,..

Nói một cách đơn giản

>Một factory của các factory; một factory nhóm các cá nhân nhưng các factory liên quan / phụ thuộc với nhau mà không cần chỉ định các class cụ thể của chúng.

Wikipedia nói là

>The abstract factory pattern cung cấp một cách để gói gọn một nhóm các factory riêng lẻ có một chủ đề chung mà không cần chỉ định các class cụ thể của chúng.

Ví dụ lập trình

Diễn giải ví dụ cưa ở trên.Đầu tiên chúng ta có một interface `Door` và một vài thực hiện cho nó

```php
interface Door
{
    public function getDescription();
}

class WoodenDoor implements Door
{
    public function getDescription()
    {
        echo 'I am a wooden door';
    }
}

class IronDoor implements Door
{
    public function getDescription()
    {
        echo 'I am an iron door';
    }
}
```

Sau đó chúng ta có chuyên gia cho mỗi loại cửa

```php
interface DoorFittingExpert
{
    public function getDescription();
}

class Welder implements DoorFittingExpert
{
    public function getDescription()
    {
        echo 'I can only fit iron doors';
    }
}

class Carpenter implements DoorFittingExpert
{
    public function getDescription()
    {
        echo 'I can only fit wooden doors';
    }
}
```

Bây giờ chúng ta có abstract factory sẽ cho phép chúng ta tạo ra một nhóm các object có liên quan tới nhau. ví dụ như nhà máy cửa gỗ sẽ tạo ra cửa gỗ và chuyên gia phù hợp với cửa gỗ, và nhà máy cửa sắt tạo ta cửa sắt và chuyên gia phù hợp với cửa sắt.


```php
interface DoorFactory
{
    public function makeDoor(): Door;
    public function makeFittingExpert(): DoorFittingExpert;
}

// Wooden factory to return carpenter and wooden door
class WoodenDoorFactory implements DoorFactory
{
    public function makeDoor(): Door
    {
        return new WoodenDoor();
    }

    public function makeFittingExpert(): DoorFittingExpert
    {
        return new Carpenter();
    }
}

// Iron door factory to get iron door and the relevant fitting expert
class IronDoorFactory implements DoorFactory
{
    public function makeDoor(): Door
    {
        return new IronDoor();
    }

    public function makeFittingExpert(): DoorFittingExpert
    {
        return new Welder();
    }
}
```

Sau đó nó có thể sử dụng như sau

```php
$woodenFactory = new WoodenDoorFactory();

$door = $woodenFactory->makeDoor();
$expert = $woodenFactory->makeFittingExpert();

$door->getDescription();  // Output: I am a wooden door
$expert->getDescription(); // Output: I can only fit wooden doors

// Same for Iron Factory
$ironFactory = new IronDoorFactory();

$door = $ironFactory->makeDoor();
$expert = $ironFactory->makeFittingExpert();

$door->getDescription();  // Output: I am an iron door
$expert->getDescription(); // Output: I can only fit iron doors
```

Như bạn có thể thấy các nhà máy sản xuất cửa gỗ đã đóng gói các`carpenter` và `wooden door` nhà máy cửa sắt cũng đã đóng gói `iron door` và `welder`. Và do đó nó đã giúp chúng ta đảm bảo rằng đối với mỗi cánh cửa được tạo ra, chúng ta không nhận nhầm chuyên gia. 

**Khi nào sử dụng**

Khi có sự tương quan giữa phụ thuộc và các logic khởi tạo liên quan không đơn giản

👷 Builder
--------------------------------------------

Ví dụ thực tế


















 

