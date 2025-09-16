
**Type Casting :**

In Java, type casting is the process of converting a variable of one data type into another. Since Java is strongly typed, 
you cannot assign values of one type to another incompatible type without explicit conversion.

Type casting is mainly of two types:

●*Widening (Implicit) Casting*
●*Narrowing (Explicit) Casting*

1.**Widening Casting (Implicit Conversion) -**



class WideningExample
{
  public static void main(String args[])
  {
    int num = 100;
    double d = num; * int automatically converted to double *
    System.out.println("Integer: " + num);
    System.out.println("Double (after widening): " + d);
  }
}


  {
    double d = 99.99;
    int num = (int) d; * double explicitly converted to int *
    System.out.println("Double: " + d);
    System.out.println("Integer (after narrowing): " + num);
  }
}


● Widening is safe and automatic.
● Narrowing requires explicit cast and may lose precision.
● Type casting works only between compatible data types.
● Strings and objects need special conversion methods, not primitive casting.
