# Math

**An integer is a collection of positive and negative whole numbers and zero(es); Mathematical operations utilize integers as their primary source of data.**

## General
----------

### **mFloor**
*Rounds **%value** down to the nearest whole number*

* `Parameters` - float **%value**

```csharp
==> mCeil(3.1415);
3
```

### **mCeil**
*Rounds **%value** up to the nearest whole number*

* `Parameters` - float **%value**

```csharp
==> mCeil(3.1415);
4
```

### **mAbs**
*Converts **%value** to an absolute value*

* `Parameters` - float **%value**

```csharp
==> mAbs(-15);
15
```

### **mFloatLength**
*Rounds **%value** to the amount of decimal places specified in **%numDecimals**.*

* `Parameters` - float **%value**, integer **%numDecimals**

```csharp
==> mFloatLength(3.1415, 2);
3.14
```

### **mSqrt**
*Returns the square root of **%value**.*

* `Parameters` - float **%value**

```csharp
==> mSqrt(9);
3
```

### **mPow**
*Raises **%value** to power specified in **%power**.*

* `Parameters` - float **%value**, float **%power**

```csharp
==> mPow(2, 3);
8
```

### **mClamp**
*Limits the **%value** given to in-between the **%low** and **%high** integer values.*

* `Parameters` - integer **%value**, integer **%low**, integer **%high**

```csharp
==> mClamp(7, 5, 10);
7
==> mClamp(3, 5, 10);
5
==> mClamp(13, 5, 10);
10
```

### **mClampF**
*Limits the **%value** given to in-between the **%low** and **%high** float values.*

* `Parameters` - float **%value**, float **%low**, float **%high**

### **mLog**
*Returns the natural [logarithm](https://en.wikipedia.org/wiki/Logarithm), in base 10, of **%value**.*

* `Parameters` - float **%value**

### **mSin**
*Returns the Trigonometric [sine](https://en.wikipedia.org/wiki/Sine), in [radians](https://en.wikipedia.org/wiki/Radian), of **%value**.*

* `Parameters` - float **%value**

### **mSin**
*Returns the Trigonometric [cosine](https://en.wikipedia.org/wiki/Cosine), in [radians](https://en.wikipedia.org/wiki/Radian), of **%value**.*

* `Parameters` - float **%value**

### **mTan**
*Returns the Trigonometric [tangent](https://en.wikipedia.org/wiki/Tangent), in [radians](https://en.wikipedia.org/wiki/Radian), of **%value**.*

* `Parameters` - float **%value**

### **mAsin**
*Returns the Trigonometric [arc-sine](https://en.wikipedia.org/wiki/Arcsine), in [radians](https://en.wikipedia.org/wiki/Radian), of **%value**.*

* `Parameters` - float **%value**

### **mAcos**
*Returns the Trigonometric [arc-cosine](https://en.wikipedia.org/wiki/Arccosine), in [radians](https://en.wikipedia.org/wiki/Radian), of **%value**.*

* `Parameters` - float **%value**

### **mAtan**
*Returns the Trigonometric [arc-tangent](https://en.wikipedia.org/wiki/Arctangent), in [radians](https://en.wikipedia.org/wiki/Radian), of **%value**.*

* `Parameters` - float **%value**

### **mRadToDeg**
*Converts [radian](https://en.wikipedia.org/wiki/Radian) value **%radians** to [degrees](http://en.wikipedia.org/wiki/Degree_(angle)).*

* `Parameters` - float **%radians**

### **mDegToRad**
*Converts [degree](http://en.wikipedia.org/wiki/Degree_(angle)) value **%degrees** to [radians](https://en.wikipedia.org/wiki/Radian).*

* `Parameters` - float **%degees**

### **getMin**
*Returns the smaller of the two **%value1** and **%value2** numbers.*

* `Parameters` - integer **%value1**, integer **%value2**

```csharp
==> getMin(3, 9);
3
```

### **getMax**
*Returns the larger of the two **%value1** and **%value2** numbers.*

* `Parameters` - integer **%value1**, integer **%value2**

```csharp
==> getMax(3, 9);
9
```

### **atoi**
*Returns an integer representation of the string, **%string***

* `Parameters` - string **%string**

```csharp
==> atoi("1337");
1337
```

### **atof**
*Returns a float representation of the string, **%string***

* `Parameters` - string **%string**

```csharp
==> atof("3.14");
3.14
```

## Vectors
----------

### **vectorAdd**
*Adds **%vector1** and **%vector2** together and returns the resulting vector.*

* `Parameters` - vector3f **%vector1**, vector3f **%vector2**

```csharp
==> vectorAdd("1 2 3", "3 2 1");
"4 4 4"
```

### **vectorSub**
*Subtracts **%vector2** from **%vector1** and returns the resulting vector.*

* `Parameters` - vector3f **%vector1**, vector3f **%vector2**

```csharp
==> vectorSub("3 3 3", "2 2 1");
"1 1 2"
```

### **vectorScale**
*Scales (multiplies) the **%vector** by the float **%scalar** and returns it.*

* `Parameters` - vector3f **%vector**, float **%scalar**

```csharp
==> vectorScale("2 2 2", 4);
"8 8 8"
```

### **vectorDot**
*Calculates and returns the [dot product](https://en.wikipedia.org/wiki/Dot_product) of **%vector1** and **%vector2**.*

* `Parameters` - vector3f **%vector1**, vector3f **%vector2**

```csharp
==> vectorDot("2 2 2", "4 4 4");
24
```

### **vectorDist**
*Calculates and returns the distance between **%vector1** and **%vector2**.*

* `Parameters` - vector3f **%vector1**, vector3f **%vector2**

```csharp
==> vectorDist("2 2 2", "4 4 4");
3.4641
```

### **vectorLen**
*Calculates and returns the length of **%vector**.*

* `Parameters` - vector3f **%vector**

```csharp
==> vectorLen("5 5 5");
8.66025
```

### **vectorNormalize**
*[Normalizes](https://en.wikipedia.org/wiki/Normalized_vector) and then returns the vector **%vector** through making its length equal one.*

* `Parameters` - vector3f **%vector**

### **vectorCross**
*Calculates and returns the [cross product](https://en.wikipedia.org/wiki/Cross_product) of **%vector1** and **%vector2**.*

* `Parameters` - vector3f **%vector1**, vector3f **%vector2**