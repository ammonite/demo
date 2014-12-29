http://interactivepython.org/courselib/static/pythonds/Recursion/recursionsimple.html#lst-recstack

def listsum(numList):
    theSum = 0
    for i in numList:
        theSum = theSum + i
    return theSum

print(listsum([1,3,5,7,9]))

def listsum(numList):
   if len(numList) == 1:
        return numList[0]
   else:
        return numList[0] + listsum(numList[1:])

print(listsum([1,3,5,7,9]))

def toStr(n,base):
   convertString = "0123456789ABCDEF"
   if n < base:
      return convertString[n]
   else:
      return toStr(n//base,base) + convertString[n%base]

print(toStr(1453,16))

from pythonds.basic.stack import Stack

rStack = Stack()

def toStr(n,base):
    convertString = "0123456789ABCDEF"
    while n > 0:
        if n < base:
            rStack.push(convertString[n])
        else:
            rStack.push(convertString[n % base])
        n = n // base
    res = ""
    while not rStack.isEmpty():
        res = res + str(rStack.pop())
    return res

print(toStr(1453,16))
http://www.cis.upenn.edu/~matuszek/cis554-2012/Pages/recursion-in-python.html

def factorial(n):
    "Computes the factorial of its argument."
    if n == 0:
        return 1
    else:
        return factorial(n - 1) * n

def factorial(n):
    if n == 0:
        return 1
    else:
        return n * (n - 1) * factorial(n - 2)

