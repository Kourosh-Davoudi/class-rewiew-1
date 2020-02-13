## Copy File programs

Learning outcomes highlights: 
- using command line arguments
- file operations

**Problem:** Write a program to get the two file names as command-line arguments and create/copy the first file contents to the second file. The name of the program is mycp.cpp, so the execution should be like:

./mycp file1 file2 (create file 2 and copy file1 contents to the file 2)

your program should check if a user provided enough arguments and print an appropriate message.

```C++
#include <iostream>
using namespace std;

class Circle {
  private:  
    int x,y;      // center of circle
    double r;    // radius of circle

  public:
   
    Circle(int =0,int=0, double =1.0);
    void print() const;
    double area() const;

    double operator+(const Circle &) const;

    Circle & operator++();
    Circle operator++(int);

  friend ostream & operator<<(ostream &out, const Circle &);
  friend istream & operator>>(istream &in, Circle &);
};

Circle::Circle(int x,int y, double r)
{
  // Initialize the object here
}

double Circle::area() const {
  // Return the area of a circle  
}

double Circle::operator+(const Circle & c) const
{
   // + Return the area of two circles  

}

Circle & Circle::operator++()
{
  // Increment the radius by 1

  return *this;
}

Circle Circle::operator++(int)
{
  Circle temp = *this;
  
  //increment the radius by 1

  return temp;
}

ostream & operator<<(ostream &out, const Circle &c)
{

  // print a circle in the out stream (the format is the same as print())
  return out;
}

istream & operator>>(istream &in, Circle &c)
{
 
 // Read a circle information form the in stream

  return in;
}


void Circle::print() const
{
  cout << "Circle =(" << x << "," << y << "," << r << ")" << endl;
}



int main()
{
  // Circle a;
  // Circle b(2,3,3.0);

  // a.print();
  // b.print();
  
  // cout << "The area a + b is: " << a+b << endl;
  // ++a;
  // a.print();

  // a++;
  // a.print();

  // cout << a;

  // cin >> a;
  // cout <<a;

  return 0;

}

```
