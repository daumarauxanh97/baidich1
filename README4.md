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

>Hãy tưởng tượng bạn đang ở Hardee và bạn đặt hàng một món cụ thể, giả sử "Big Hardee" và họ trao nó cho bạn mà không có bất kỳ câu hỏi nào; đây là ví dụ về Simple factory. Nhưng có những trường hợp khi logic tạo ra có thể liên quan đến nhiều bước hơn. Ví dụ: bạn muốn một thỏa thuận Subway tùy chỉnh, bạn có một số tùy chọn về cách thức làm bánh burger của bạn, ví dụ: bạn muốn bánh mì nào? bạn muốn loại nước sốt nào? Bạn muốn phô mai nào? vv Trong trường hợp như vậy builder sẽ giúp bạn.

Nói một cách đơn giản

>Cho phép bạn tạo ra các thuộc tính(phương thức) khác nhau của một đối tượng trong khi tránh ảnh hưởng constructor . Hữu ích khi objects có thể có nhiều thuộc tính(phương thức). Hoặc khi có rất nhiều bước liên quan đến việc tạo ra một object.

Wikipedia nói là

>builder pattern là phần mềm design pattern tạo đối tượng với ý định tìm kiếm một giải pháp cho mô hình chống tạo lồng ghép.

Để tôi nói thêm một chút về mô hình chống tạo lồng ghép là gì. Tại một thời điểm hoặc khác, chúng tôi đã tất cả nhìn thấy một nhà xây dựng như dưới đây:

```php
public function __construct($size, $cheese = true, $pepperoni = true, $tomato = false, $lettuce = true)
{
}
```

>Như bạn có thể thấy; số tham số của constructor có thể nhanh chóng thoát ra khỏi bàn tay và có thể khó hiểu được sắp xếp các tham số. Thêm vào đó danh sách tham số này có thể tiếp tục phát triển nếu bạn muốn thêm nhiều tùy chọn hơn trong tương lai. Điều này được gọi là mô hình chống tạo lồng ghép.

**Ví dụ lập trình**

>Cách thay thế tốt là sử dụng builder pattern. Trước hết, chúng ta có bánh mì kẹp thịt mà chúng tôi muốn làm

```php
class Burger
{
    protected $size;

    protected $cheese = false;
    protected $pepperoni = false;
    protected $lettuce = false;
    protected $tomato = false;

    public function __construct(BurgerBuilder $builder)
    {
        $this->size = $builder->size;
        $this->cheese = $builder->cheese;
        $this->pepperoni = $builder->pepperoni;
        $this->lettuce = $builder->lettuce;
        $this->tomato = $builder->tomato;
    }
}
```

Và sau đó chúng ta có builder

```php
class BurgerBuilder
{
    public $size;

    public $cheese = false;
    public $pepperoni = false;
    public $lettuce = false;
    public $tomato = false;

    public function __construct(int $size)
    {
        $this->size = $size;
    }

    public function addPepperoni()
    {
        $this->pepperoni = true;
        return $this;
    }

    public function addLettuce()
    {
        $this->lettuce = true;
        return $this;
    }

    public function addCheese()
    {
        $this->cheese = true;
        return $this;
    }

    public function addTomato()
    {
        $this->tomato = true;
        return $this;
    }

    public function build(): Burger
    {
        return new Burger($this);
    }
}
```

Sau đó nó có thể sử dụng như sau

```php
$burger = (new BurgerBuilder(14))
                    ->addPepperoni()
                    ->addLettuce()
                    ->addTomato()
                    ->build();
```

**Khi nào thì sử dụng**

>Khi có thể có một số thuộc tính của object và tránh việc chống lại khởi tạo. Sự khác biệt chính của factory pattern là đây; factory pattern được sử dụng khi việc khởi tạo chỉ có một bước trong tiến trình trong khi builder pattern được sử dụng khi có nhiều bước trong quá trình.

# Prototype

Ví dụ thực tế

>Nhớ dolly chứ?chú cừu được nhân bản.Không đi vào chi tiết từ khóa quan trọng ở đây là nhân bản.

Nói một cách đơn giản

>Tạo một object dựa trên object đã tồn tại thông qua việc nhân bản.

Wikipedia nói là

>The prototype pattern là 1 creational design pattern trong phát triển phần mềm.Nó được sử dụng khi object cần tạo được xác định bởi một cá thể nguyên mẫu, được sao chép để tạo ra các object mới.

Tóm lại, nó cho phép bạn tạo một bản sao của một object hiện có và sửa đổi nó theo nhu cầu của bạn, thay vì trải qua những rắc rối khi tạo một object từ đầu và thiết lập nó.

**Ví dụ lập trình**

Trong PHP có thể xử lý dễ dàng bằng sủ dung `clone`

```php
class Sheep
{
    protected $name;
    protected $category;

    public function __construct(string $name, string $category = 'Mountain Sheep')
    {
        $this->name = $name;
        $this->category = $category;
    }

    public function setName(string $name)
    {
        $this->name = $name;
    }

    public function getName()
    {
        return $this->name;
    }

    public function setCategory(string $category)
    {
        $this->category = $category;
    }

    public function getCategory()
    {
        return $this->category;
    }
}
```

Sau đó, nó có thể được nhân bản như sau

```php
$original = new Sheep('Jolly');
echo $original->getName(); // Jolly
echo $original->getCategory(); // Mountain Sheep

// Clone and modify what is required
$cloned = clone $original;
$cloned->setName('Dolly');
echo $cloned->getName(); // Dolly
echo $cloned->getCategory(); // Mountain sheep
```

Khi bạn sử dụng phương thức `__clone` để chỉnh sửa hoạt động nhân bản. 

**Khi nào sư dụng**

Khi một object được yêu cầu tương tự như object hiện có hoặc khi việc tạo ra sẽ tốn kém hơn so với nhân bản.

💍 Singleton
------------

Ví dụ thực tế

Tại một thời điểm một quốc gia chỉ có 1 tổng thống.Tổng thống phải làm việc, bất cứ khi nào có nhiệm vụ. Tổng thống ở đây là singleton.

Nói một cách đơn giản

Đảm bảo rằng chỉ có một object của một class cụ thể được tạo ra.

Wikipedia nói là

>Trong lĩnh vực kĩ nghệ phần mềm singleton pattern la một phần mềm design pattern hạn chế sự khởi tạo của một class với một object. Điều này rất hữu ích khi cần chính xác  một object để điều phối các hành động trên toàn hệ thống.

Singleton pattern được coi là một anti-pattern và nên tránh lạm dụng nó . Nó không nhất thiết là xấu và có thể có một số trường hợp sử dụng hợp lệ nhưng nên được sử dụng thận trọng vì nó giới thiệu một trạng thái toàn cầu trong ứng dụng của bạn và thay đổi nó ở một nơi có thể ảnh hưởng đến các khu vực khác và nó có thể trở nên khá khó khăn để gỡ lỗi. Điều tệ hại khác về chúng là nó làm cho mã của bạn được kết hợp quá chặt chẽ cộng với thay đổi singleton có thể khó khăn.

Ví dụ lập trình


Để tạo ra một singleton, làm cho constructor private, vô hiệu hóa nhân bản, vô hiệu hóa phần mở rộng và tạo một biến tĩnh để chứa cá thể đó

```php
final class President
{
    private static $instance;

    private function __construct()
    {
        // Hide the constructor
    }

    public static function getInstance(): President
    {
        if (!self::$instance) {
            self::$instance = new self();
        }

        return self::$instance;
    }

    private function __clone()
    {
        // Disable cloning
    }

    private function __wakeup()
    {
        // Disable unserialize
    }
}
```
Sau đó để sử dụng

```php
$president1 = President::getInstance();
$president2 = President::getInstance();

var_dump($president1 === $president2); // true
```

Structural Design Patterns
==========================

Nói một cách đơn giản

> Structural patterns chủ yếu quan tâm đến thành phần đối tượng hay nói cách khác là các thực thể có thể sử dụng lẫn nhau như thế nào. Hoặc có thể giải thích một cách là, họ giúp trả lời "Làm thế nào để xây dựng một thành phần phần mềm?"

Wikipedia nói là
> Trong lĩnh vực kĩ nghệ phần mềm,  Structural design patterns là các design pattern làm dễ dàng thiết kế bằng cách xác định một cách đơn giản để nhận ra mối quan hệ giữa các thực thể.

 * [Adapter](#-adapter)
 * [Bridge](#-bridge)
 * [Composite](#-composite)
 * [Decorator](#-decorator)
 * [Facade](#-facade)
 * [Flyweight](#-flyweight)
 * [Proxy](#-proxy)

🔌 Adapter
-------
Ví dụ thực tế
>Giả sử rằng bạn có một số hình ảnh trong thẻ nhớ của bạn và bạn cần phải chuyển chúng vào máy tính của bạn. Để chuyển chúng, bạn cần một loại bộ điều hợp tương thích với cổng máy tính của bạn để bạn có thể gắn thẻ nhớ vào máy tính. Trong trường hợp này đầu đọc thẻ là một bộ chuyển đổi.
>Một ví dụ khác sẽ là bộ điều hợp nguồn nổi tiếng; một ổ ba chân cắm không thể được kết nối với một giắc cắm 2 chân, nó cần phải sử dụng một bộ chuyển đổi điện mà làm cho nó tương thích với ổ cắm 2 chân.
>Một ví dụ nưa sẽ là một phiên dịch viên phiên dịch lời người này nói cho người kia

In plain words
> Adapter pattern lets you wrap an otherwise incompatible object in an adapter to make it compatible with another class.

Wikipedia says
> In software engineering, the adapter pattern is a software design pattern that allows the interface of an existing class to be used as another interface. It is often used to make existing classes work with others without modifying their source code.

**Programmatic Example**

Consider a game where there is a hunter and he hunts lions.

First we have an interface `Lion` that all types of lions have to implement

```php
interface Lion
{
    public function roar();
}

class AfricanLion implements Lion
{
    public function roar()
    {
    }
}

class AsianLion implements Lion
{
    public function roar()
    {
    }
}
```
And hunter expects any implementation of `Lion` interface to hunt.
```php
class Hunter
{
    public function hunt(Lion $lion)
    {
        $lion->roar();
    }
}
```

Now let's say we have to add a `WildDog` in our game so that hunter can hunt that also. But we can't do that directly because dog has a different interface. To make it compatible for our hunter, we will have to create an adapter that is compatible

```php
// This needs to be added to the game
class WildDog
{
    public function bark()
    {
    }
}

// Adapter around wild dog to make it compatible with our game
class WildDogAdapter implements Lion
{
    protected $dog;

    public function __construct(WildDog $dog)
    {
        $this->dog = $dog;
    }

    public function roar()
    {
        $this->dog->bark();
    }
}
```
And now the `WildDog` can be used in our game using `WildDogAdapter`.

```php
$wildDog = new WildDog();
$wildDogAdapter = new WildDogAdapter($wildDog);

$hunter = new Hunter();
$hunter->hunt($wildDogAdapter);
```

🚡 Bridge
------
Real world example
> Consider you have a website with different pages and you are supposed to allow the user to change the theme. What would you do? Create multiple copies of each of the pages for each of the themes or would you just create separate theme and load them based on the user's preferences? Bridge pattern allows you to do the second i.e.

![With and without the bridge pattern](https://cloud.githubusercontent.com/assets/11269635/23065293/33b7aea0-f515-11e6-983f-98823c9845ee.png)

In Plain Words
> Bridge pattern is about preferring composition over inheritance. Implementation details are pushed from a hierarchy to another object with a separate hierarchy.

Wikipedia says
> The bridge pattern is a design pattern used in software engineering that is meant to "decouple an abstraction from its implementation so that the two can vary independently"

**Programmatic Example**

Translating our WebPage example from above. Here we have the `WebPage` hierarchy

```php
interface WebPage
{
    public function __construct(Theme $theme);
    public function getContent();
}

class About implements WebPage
{
    protected $theme;

    public function __construct(Theme $theme)
    {
        $this->theme = $theme;
    }

    public function getContent()
    {
        return "About page in " . $this->theme->getColor();
    }
}

class Careers implements WebPage
{
    protected $theme;

    public function __construct(Theme $theme)
    {
        $this->theme = $theme;
    }

    public function getContent()
    {
        return "Careers page in " . $this->theme->getColor();
    }
}
```
And the separate theme hierarchy
```php

interface Theme
{
    public function getColor();
}

class DarkTheme implements Theme
{
    public function getColor()
    {
        return 'Dark Black';
    }
}
class LightTheme implements Theme
{
    public function getColor()
    {
        return 'Off white';
    }
}
class AquaTheme implements Theme
{
    public function getColor()
    {
        return 'Light blue';
    }
}
```
And both the hierarchies
```php
$darkTheme = new DarkTheme();

$about = new About($darkTheme);
$careers = new Careers($darkTheme);

echo $about->getContent(); // "About page in Dark Black";
echo $careers->getContent(); // "Careers page in Dark Black";
```

🌿 Composite
-----------------

Real world example
> Every organization is composed of employees. Each of the employees has the same features i.e. has a salary, has some responsibilities, may or may not report to someone, may or may not have some subordinates etc.

In plain words
> Composite pattern lets clients treat the individual objects in a uniform manner.

Wikipedia says
> In software engineering, the composite pattern is a partitioning design pattern. The composite pattern describes that a group of objects is to be treated in the same way as a single instance of an object. The intent of a composite is to "compose" objects into tree structures to represent part-whole hierarchies. Implementing the composite pattern lets clients treat individual objects and compositions uniformly.

**Programmatic Example**

Taking our employees example from above. Here we have different employee types

```php
interface Employee
{
    public function __construct(string $name, float $salary);
    public function getName(): string;
    public function setSalary(float $salary);
    public function getSalary(): float;
    public function getRoles(): array;
}

class Developer implements Employee
{
    protected $salary;
    protected $name;
    protected $roles;
    
    public function __construct(string $name, float $salary)
    {
        $this->name = $name;
        $this->salary = $salary;
    }

    public function getName(): string
    {
        return $this->name;
    }

    public function setSalary(float $salary)
    {
        $this->salary = $salary;
    }

    public function getSalary(): float
    {
        return $this->salary;
    }

    public function getRoles(): array
    {
        return $this->roles;
    }
}

class Designer implements Employee
{
    protected $salary;
    protected $name;
    protected $roles;

    public function __construct(string $name, float $salary)
    {
        $this->name = $name;
        $this->salary = $salary;
    }

    public function getName(): string
    {
        return $this->name;
    }

    public function setSalary(float $salary)
    {
        $this->salary = $salary;
    }

    public function getSalary(): float
    {
        return $this->salary;
    }

    public function getRoles(): array
    {
        return $this->roles;
    }
}
```

Then we have an organization which consists of several different types of employees

```php
class Organization
{
    protected $employees;

    public function addEmployee(Employee $employee)
    {
        $this->employees[] = $employee;
    }

    public function getNetSalaries(): float
    {
        $netSalary = 0;

        foreach ($this->employees as $employee) {
            $netSalary += $employee->getSalary();
        }

        return $netSalary;
    }
}
```

And then it can be used as

```php
// Prepare the employees
$john = new Developer('John Doe', 12000);
$jane = new Designer('Jane Doe', 15000);

// Add them to organization
$organization = new Organization();
$organization->addEmployee($john);
$organization->addEmployee($jane);

echo "Net salaries: " . $organization->getNetSalaries(); // Net Salaries: 27000
```

☕ Decorator
-------------

Real world example

> Imagine you run a car service shop offering multiple services. Now how do you calculate the bill to be charged? You pick one service and dynamically keep adding to it the prices for the provided services till you get the final cost. Here each type of service is a decorator.

In plain words
> Decorator pattern lets you dynamically change the behavior of an object at run time by wrapping them in an object of a decorator class.

Wikipedia says
> In object-oriented programming, the decorator pattern is a design pattern that allows behavior to be added to an individual object, either statically or dynamically, without affecting the behavior of other objects from the same class. The decorator pattern is often useful for adhering to the Single Responsibility Principle, as it allows functionality to be divided between classes with unique areas of concern.

**Programmatic Example**

Lets take coffee for example. First of all we have a simple coffee implementing the coffee interface

```php
interface Coffee
{
    public function getCost();
    public function getDescription();
}

class SimpleCoffee implements Coffee
{
    public function getCost()
    {
        return 10;
    }

    public function getDescription()
    {
        return 'Simple coffee';
    }
}
```
We want to make the code extensible to allow options to modify it if required. Lets make some add-ons (decorators)
```php
class MilkCoffee implements Coffee
{
    protected $coffee;

    public function __construct(Coffee $coffee)
    {
        $this->coffee = $coffee;
    }

    public function getCost()
    {
        return $this->coffee->getCost() + 2;
    }

    public function getDescription()
    {
        return $this->coffee->getDescription() . ', milk';
    }
}

class WhipCoffee implements Coffee
{
    protected $coffee;

    public function __construct(Coffee $coffee)
    {
        $this->coffee = $coffee;
    }

    public function getCost()
    {
        return $this->coffee->getCost() + 5;
    }

    public function getDescription()
    {
        return $this->coffee->getDescription() . ', whip';
    }
}

class VanillaCoffee implements Coffee
{
    protected $coffee;

    public function __construct(Coffee $coffee)
    {
        $this->coffee = $coffee;
    }

    public function getCost()
    {
        return $this->coffee->getCost() + 3;
    }

    public function getDescription()
    {
        return $this->coffee->getDescription() . ', vanilla';
    }
}
```

Lets make a coffee now

```php
$someCoffee = new SimpleCoffee();
echo $someCoffee->getCost(); // 10
echo $someCoffee->getDescription(); // Simple Coffee

$someCoffee = new MilkCoffee($someCoffee);
echo $someCoffee->getCost(); // 12
echo $someCoffee->getDescription(); // Simple Coffee, milk

$someCoffee = new WhipCoffee($someCoffee);
echo $someCoffee->getCost(); // 17
echo $someCoffee->getDescription(); // Simple Coffee, milk, whip

$someCoffee = new VanillaCoffee($someCoffee);
echo $someCoffee->getCost(); // 20
echo $someCoffee->getDescription(); // Simple Coffee, milk, whip, vanilla
```

📦 Facade
----------------

Real world example
> How do you turn on the computer? "Hit the power button" you say! That is what you believe because you are using a simple interface that computer provides on the outside, internally it has to do a lot of stuff to make it happen. This simple interface to the complex subsystem is a facade.

In plain words
> Facade pattern provides a simplified interface to a complex subsystem.

Wikipedia says
> A facade is an object that provides a simplified interface to a larger body of code, such as a class library.

**Programmatic Example**

Taking our computer example from above. Here we have the computer class

```php
class Computer
{
    public function getElectricShock()
    {
        echo "Ouch!";
    }

    public function makeSound()
    {
        echo "Beep beep!";
    }

    public function showLoadingScreen()
    {
        echo "Loading..";
    }

    public function bam()
    {
        echo "Ready to be used!";
    }

    public function closeEverything()
    {
        echo "Bup bup bup buzzzz!";
    }

    public function sooth()
    {
        echo "Zzzzz";
    }

    public function pullCurrent()
    {
        echo "Haaah!";
    }
}
```
Here we have the facade
```php
class ComputerFacade
{
    protected $computer;

    public function __construct(Computer $computer)
    {
        $this->computer = $computer;
    }

    public function turnOn()
    {
        $this->computer->getElectricShock();
        $this->computer->makeSound();
        $this->computer->showLoadingScreen();
        $this->computer->bam();
    }

    public function turnOff()
    {
        $this->computer->closeEverything();
        $this->computer->pullCurrent();
        $this->computer->sooth();
    }
}
```
Now to use the facade
```php
$computer = new ComputerFacade(new Computer());
$computer->turnOn(); // Ouch! Beep beep! Loading.. Ready to be used!
$computer->turnOff(); // Bup bup buzzz! Haah! Zzzzz
```

🍃 Flyweight
---------

Real world example
> Did you ever have fresh tea from some stall? They often make more than one cup that you demanded and save the rest for any other customer so to save the resources e.g. gas etc. Flyweight pattern is all about that i.e. sharing.

In plain words
> It is used to minimize memory usage or computational expenses by sharing as much as possible with similar objects.

Wikipedia says
> In computer programming, flyweight is a software design pattern. A flyweight is an object that minimizes memory use by sharing as much data as possible with other similar objects; it is a way to use objects in large numbers when a simple repeated representation would use an unacceptable amount of memory.

**Programmatic example**

Translating our tea example from above. First of all we have tea types and tea maker

```php
// Anything that will be cached is flyweight.
// Types of tea here will be flyweights.
class KarakTea
{
}

// Acts as a factory and saves the tea
class TeaMaker
{
    protected $availableTea = [];

    public function make($preference)
    {
        if (empty($this->availableTea[$preference])) {
            $this->availableTea[$preference] = new KarakTea();
        }

        return $this->availableTea[$preference];
    }
}
```

Then we have the `TeaShop` which takes orders and serves them

```php
class TeaShop
{
    protected $orders;
    protected $teaMaker;

    public function __construct(TeaMaker $teaMaker)
    {
        $this->teaMaker = $teaMaker;
    }

    public function takeOrder(string $teaType, int $table)
    {
        $this->orders[$table] = $this->teaMaker->make($teaType);
    }

    public function serve()
    {
        foreach ($this->orders as $table => $tea) {
            echo "Serving tea to table# " . $table;
        }
    }
}
```
And it can be used as below

```php
$teaMaker = new TeaMaker();
$shop = new TeaShop($teaMaker);

$shop->takeOrder('less sugar', 1);
$shop->takeOrder('more milk', 2);
$shop->takeOrder('without sugar', 5);

$shop->serve();
// Serving tea to table# 1
// Serving tea to table# 2
// Serving tea to table# 5
```

🎱 Proxy
-------------------
Real world example
> Have you ever used an access card to go through a door? There are multiple options to open that door i.e. it can be opened either using access card or by pressing a button that bypasses the security. The door's main functionality is to open but there is a proxy added on top of it to add some functionality. Let me better explain it using the code example below.

In plain words
> Using the proxy pattern, a class represents the functionality of another class.

Wikipedia says
> A proxy, in its most general form, is a class functioning as an interface to something else. A proxy is a wrapper or agent object that is being called by the client to access the real serving object behind the scenes. Use of the proxy can simply be forwarding to the real object, or can provide additional logic. In the proxy extra functionality can be provided, for example caching when operations on the real object are resource intensive, or checking preconditions before operations on the real object are invoked.

**Programmatic Example**

Taking our security door example from above. Firstly we have the door interface and an implementation of door

```php
interface Door
{
    public function open();
    public function close();
}

class LabDoor implements Door
{
    public function open()
    {
        echo "Opening lab door";
    }

    public function close()
    {
        echo "Closing the lab door";
    }
}
```
Then we have a proxy to secure any doors that we want
```php
class SecuredDoor
{
    protected $door;

    public function __construct(Door $door)
    {
        $this->door = $door;
    }

    public function open($password)
    {
        if ($this->authenticate($password)) {
            $this->door->open();
        } else {
            echo "Big no! It ain't possible.";
        }
    }

    public function authenticate($password)
    {
        return $password === '$ecr@t';
    }

    public function close()
    {
        $this->door->close();
    }
}
```
And here is how it can be used
```php
$door = new SecuredDoor(new LabDoor());
$door->open('invalid'); // Big no! It ain't possible.

$door->open('$ecr@t'); // Opening lab door
$door->close(); // Closing lab door
```
Yet another example would be some sort of data-mapper implementation. For example, I recently made an ODM (Object Data Mapper) for MongoDB using this pattern where I wrote a proxy around mongo classes while utilizing the magic method `__call()`. All the method calls were proxied to the original mongo class and result retrieved was returned as it is but in case of `find` or `findOne` data was mapped to the required class objects and the object was returned instead of `Cursor`.























 

