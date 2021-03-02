# Zamkovets Vladislav

## My contacts
* ### Social networks
  * [Vkontakte](https://vk.com/el_taurus)
  * [Instagram](https://www.instagram.com/el_taurus_z/?hl=ru)
  * [GitHub](https://github.com/Kolip-03)
* ### Telephone number
  * **+375 29 101-47-29**

## Some information about me

My main goal is to become a **front-end developer**. It is difficult to find a more purposeful person than me. I am good at understanding any information. I am a fast learner and quickly get into the job. I have good communication skills, I can communicate with people and find a common language with them. Unfortunately, I have no work experience, but before signing up for these courses, I independently and intensively studied programming languages such as **JS** and **C++**, as well as markup languages **HTML** and **CSS**. I am sure that in the future it will help me become a good **front - end developer** and do my job perfectly.

## My skills in programming
* ### Programming languages
  * **JS**
  * **C++**
* ### Markup languages
  * **HTML**
  * **CSS**
* ### Development tools
  * **Visual Studio**
  * **Visual Studio Code**
  
  ## My code example
  * **C++(OOP) Code**
``` C++
template <class T>
class Tran // класс транзакции
{
	// смарт указатели
	T* that; // указатель на данное состояние
	T* prev; // указатель на предыдущее состояние
public:
	Tran() :prev(NULL), that(new T) {} // конструктор
	Tran(const Tran& obj) : // конструктор копирования
		that(new T(*(obj.that))), prev(NULL) {}
	~Tran() { delete that;  delete prev; } // деструктор
	Tran& operator=(const Tran& obj); // перегрузка операции присваивания
	void Show(int); // отображение значений предидущего и текущего обекта класса

	bool Begin(); // начало транзакции
	void Commit(); // закрепление транзакции
	void Back(); // возврат
	T* operator->(); // перегрузка операции ->
};

template <class T>
Tran<T>& Tran<T>::operator=(const Tran<T>& obj)
{
	if (this != &obj) // проверка на случай обдж=обдж
	{
		delete that; // удаление текущего значения объекта
		that = new T(*(obj.that)); // создание и копирование
	}
	return *this;
}
```
