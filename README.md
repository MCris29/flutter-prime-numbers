
# Números Primos

App en flutter que genera números primos al presionar el botón.
#### Captura

![image](https://github.com/MCris29/flutter-prime-numbers/blob/master/images/captura.png)


## Función que genera números primos

```javascript
int _init = 1;
int _end = 50;
String _numbers = "";

void _generate_prime_numbers() {
    while (_init < _end) {
      if (_checkPrimerNumber(_init)) {
        setState(() {
          _numbers += _init.toString() + "   ";
        });
      }
      _init++;
    }
  }

  bool _checkPrimerNumber(int value) {
    bool n = true;
    for (var i = 2; i < value; i++) {
      if (value % i == 0) {
        n = false;
        break;
      }
    }
    return n;
  }
```

  