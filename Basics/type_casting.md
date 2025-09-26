
**Type Casting :**



Type casting is mainly of two types:

●*Widening (Implicit) Casting*
●*Narrowing (Explicit) Casting*

1.**Widening Casting (Implicit Conversion) -**



class WideningExample
{
  public static void main(String args[])
  {
    int num = 100;
 
  
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
