# Kyivstar Big Data School Test Assignment

https://bigdata.kyivstar.ua/school/

## Data description

* tabular_data.csv
* hashed_data.csv
* train_target.csv
* test_target.csv

Ці файли допоможуть вирішити аналітичну задачу. Необхідно побудувати модель, що виявлятиме сегмент батьків серед абонентів ПрАТ «Київстар».

Це задача бінарної класифікації:
«1» – в абонента є діти, віком від 0 до 14 років (і він належить до сегмента батьків);
«0» – в абонента немає дітей даного віку (і він не у сегменті батьків).
Файли tabular_data.csv і hashed_data.csv ̶ тут описові характеристики щодо 4871 абонента («ID» – це ідентифікатор абонента).
Файл train_target.csv ̶ це дані щодо цільової мітки (чи належить абонент до сегмента батьків).
Файл test_target.csv ̶ це список абонентів, за якими ми й будемо оцінювати якість ваших моделей.

* Файл tabular_data.csv містить числові дані щодо активності абонента протягом трьох періодів.
Period – номер періоду (періоди послідовні, 1 – найдавніший);
ID – ідентифікатор абонента;
V1 – V43 – дані щодо активності абонента протягом періоду.

* Файл hashed_data.csv – тут набір захешованих значень однієї категоріальної змінної для абонента.
ID – ідентифікатор абонента;
HASH – хеш від значення категоріальної змінної.

* Файл train_target.csv – тут дані з цільовою міткою. 
ID – ідентифікатор абонента; 
TARGET – значення цільової мітки (1 – належить до сегмента батьків, 0 – не належить до сегмента батьків).

* Файл test_target.csv – список абонентів, яким потрібно зробити передбачення за допомогою ваших моделей. 
ID – ідентифікатор абонента; 
SCORE – ймовірність того, що абонент належить до сегмента батьків (класу «1»). Цю імовірність визначає ваша модель.

До речі, моделі ми будемо оцінювати за такою метрикою – ROC-AUC. (https://uk.wikipedia.org/wiki/ROC-%D0%BA%D1%80%D0%B8%D0%B2%D0%B0)

### У чому ж завдання?

Потрібно побудувати модель на абонентах, цільова мітка по яких міститься у файлі train_target.
Для цього вам необхідно використати дані з файлів tabular_data та hashed_data. Після цього, використовуючи вашу модель, потрібно для абонентів з файлу test_target оцінити SCORE – ймовірність того, що абонент відноситься до сегменту батьків. Зверніть увагу, що необхідно спрогнозувати факт відношення до сегменту батьків, без прив'язки до періоду.


