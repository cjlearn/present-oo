# Encapsulation and Information Hiding

## Encapsulation

Encapsulation in OOP is packaging data along with the operations on that data. For instance, in
C++:

``` c++
class TestResult {
private:
  int batch_size;
  int sample_size;
  int failures;
public:
  TestResult(int bsz, int ssz, int failed)
    : batch_size(bsz),
      sample_size(ssz),
      failures(failed) {}
  float failure_rate() const;
  float success_rate() const;
  int expected_good() const;
};
```

## Information Hiding

Encapsulation can be used to implement _information hiding_. Information hiding is segregating
parts of your program so that each is protected from changes in the others. Good application of
information hiding reduces coupling. Reducing coupling is one of the most important aspects of
software design.

In OOP, you use encapsulation to separate your objects into _interface_ and _implementation_.
The interface is what your object's clients can use to query or manipulate it. Its implementation
are the private parts that you can change as needed.  Encapsulated in this way, your object's
clients are structureally immune from the changes you make to the implementation (although you
can certainly change the behavior in a way its clients do not expect).

## Design by Contract

Design by contract is aa formalization of information hiding in your design. A contract consists
of _pre-conditions_, those facts that the caller must ensure are true before calling any of your
object's code, and _post-conditions_, those facts that your code must ensure are true after your
object's code is called. If the caller meets the pre-conditions, your object is responsible to
meet the post-conditions. If the caller does not meet the pre-conditions, your object has no
responsibility.

In design by contract, your object does not need to check that the pre-conditions are met. It is
allowed to operate in a completely undefined manner if the caller does not meet the conditions.
Contrast that to so-called _defensive programming_ where an object is responsible for validating
all inputs before proceeding.







