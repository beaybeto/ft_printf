# ft_printf

El objetivo de este proyecto es crear tu propia función printf, y por tanto aprender a trabajar con **funciones variádicas**.

Éstas son funciones que toman un *argumento fijo* y un *número variable de argumentos*. Para ello se usan una serie de **macros** en la función:
 - va_list → para declarar vargs (variable arguments).
 - va_start → acceso a los argumentos de la función variádica. Se le pasa el parámetro definido por va_list, y la cadena de formato (el primer parámetro no variable). ESTO QUIERE DECIR QUE LE INDICAMOS A PARTIR DE QUÉ PARÁMETRO COMIENZAN LOS ARGUMENTOS VARIÁDICOS.
 - va_arg → acceso al siguiente argumento de la función variádica. Se le pasan dos parámetros, que quiere decir DE QUÉ TIPO ES EL SIGUIENTE ARGUMENTO DE LA LISTA.
 - va_end → finaliza el recorrido de los argumentos de la función variádica.

Y el prototipo de la función es:
```
int	ft_printf(char const *format, ...)
```

Uno de los puntos clave en este proyecto es tener claro desde el principio que **ESTA FUNCIÓN RETORNA EL NÚMERO DE CARACTERES IMPRIMIDOS**, y por tanto es conveniente que desde el principio se cree un contador.

## Funciones necesarias a las que llama ft_printf
 - ft_putchar → %c → imprimer un solo carácter
 - ft_putstr → %s → imprime un string
 - ft_putnbr → %i && %d → imprime un entero en base 10. EL ARGUMENTO INT ES CONVERTIDO EN DECIMAL SIGNADO
 - ft_percentage → %% → imprime el símbolo del porcentaje → usaremos putchar
 - ft_print_direction → %p → imprime en formato hexadecimal la dirección del puntero (PARA ELLO SE USA UNSIGNED LONG)
 - ft_print_unsigned_decimal → %u → imprime un entero decimal no signado. EL ARGUMENTO INT ES CONVERTIDO EN DECIMAL UNSIGNED
 - ft_print_hexadecimal_upper && ft_print_hexadecimal_lower → %X && %x → imprime un entero hexadecimal no signado. EL ARGUMENTO INT ES CONVERTIDO EN HEXADECIMAL UNSIGNED
