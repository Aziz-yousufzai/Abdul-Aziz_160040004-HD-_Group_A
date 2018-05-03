# Abdul-Aziz_160040004-HD-_Group_A





Copy constructor creates a new object of the same class using an existing object. It creates a copy/replica of the existing object.

It copies value of all member variables from existing object to new object. It copies values member-to-member.

It will be called when

    When an object is constructed based on another object of the same class.
    When an object of the class is passed (to a function) by value as an argument.
    When an object of the class is returned by value.
    When compiler generates a temporary object.

When you need

If the class has pointer variables and has some dynamic memory allocations, then it is a must to have a copy constructor.

As we have class here as: 

class MyString
{
	char * str;
	int size;
	void str_cpy(char* temp_str,int size);
	void str_cat(char* temp_str, int size);
public:
	MyString();
	MyString(char* temp_str);
	MyString(const MyString &ob);
	
	MyString operator+(MyString ob);
	MyString operator+(char* temp_str);
	MyString operator+(const char* temp_str);

	MyString operator+=(MyString ob);
	MyString operator+=(char* temp_str);
	MyString operator+=(const char* temp_str);

	MyString operator=(MyString ob);
	MyString operator=(char* temp_str);
	MyString operator=(const char* temp_str);

	bool operator==(MyString ob);
	bool operator==(char* temp_str);
	bool operator==(const char* temp_str);

	bool operator<(MyString ob);
	bool operator<(char* temp_str);
	bool operator<(const char* temp_str);

	bool operator>(MyString ob);
	bool operator>(char* temp_str);
	bool operator>(const char* temp_str);

	MyString operator++();
	MyString operator++(int notused);
	
	void print_str();
	~MyString();
};

	.: have to use the copy constructor 


If you will not define then

If you don't define copy constructor, 
the C++ compiler creates a default copy constructor for each class which does a member-wise copy (shallow copy) between objects.


the output of the given Schema is:

ABC
DEF
ABCDEFABC
ABC
DEF
DEF
DEF executed
DEP executedDEFABC
ob1 == ob2 [ABC == ABC ]
ob2 < ob3 [ABC <DEF ]
ABCC
ABCC
ABCCC
ABCC



