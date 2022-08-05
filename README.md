<h1>The Awesome _printf() function</h1>
<h4>_printf - formatted output conversion</h4>

<h2>Description</h2>
<h4>The <b>_printf()</b> function produce output according to a format as described below. Also, write output to stdout, the standard output stream.

The <b>\_printf()</b> function write the output under the control of a format string that specifies how subsequent arguments (or arguments accessed via the variable-length argument facilities of stdarg(3) are converted for output.</h4>

<h2>Format of the format string</h2>
<h4>The format string is a character string, beginning and ending inits initial shift state, if any. The format string is composed of zero or more directives: ordinary characters (not %), which are copied unchanged to the output stream; and conversion specifications, each of which results in fetching zero or more subsequent arguments. Each conversion specification is introduced by the character % and ends with conversion specifier.</h4>

<h2>Conversion specifiers</h2>
<h4>A character that specifies the type of conversion to be applied. The conversion specifiers and their meaning are:

<ul>
<li>d, i: The int argument should be signed decimal notation, and the resulting number is written.</li>
<li>c: The int argument is converted to a char, and the resulting character is written.</li>
<li>s: The const char * argument is expected to be a pointer to an array of character type (pointer to a string). Characters from the array are written up to (but not including) a terminating null byte ('\0').</li>
<li>%: A '%' is written. No argument is converted. The complete conversion specification is '%%'.</li>
</ul>
</h4>

<h2>About Functions</h2>
<h3>int _write(char c)</h3>
<h4>This function gets a char parameter and writes the parameter to the stdout, the standard output stream.</h4>

<h3>int _print_a_char (va_list args)</h3>
<h4>This function gets a variadic arguments list, traverse the list, prints each character of char type and returns the length of the character.</h4>

<h3>int _print_a_string (va_list args)</h3>
<h4>This function gets a variadic arguments list, traverse the list, prints each string and returns the length of the string.</h4>

<h3>int _print_a_integer (va_list args)</h3>
<h4>This function gets a variadic arguments list, traverse the list, prints each number of int type and returns the length of the integer.</h4>

<h3>int _print_format (const char *format, va_list args)</h3>
<h4>This function gets a format to be printed and a variadic arguments list, next to check if the format is valid or invalid and according with the verification the resulting output is written to the standard output stream and returns the format length.</h4>

<h3>int _print_spec (char format, va_list args):</h3>
<h4>This function gets a format valid to be printed and a variadic arguments list to find the format in the list and selects the appropriate function to execute and writes the format to the standard output stream and returns the length of the valid format.</h4>

<h3>int _print_invalid_spec (char prev_format, char format, int count)</h3>
<h4>This function gets the previous format of the current format, the actual format and the current count of printed characters. Next, the invalid format is written to the standard output stream and returns the length of the invalid format.</h4>

<h3>void _recursion_integer(int a)</h3>
<h4>This function gets an integer and prints the last digit of the number as recursion is applied.</h4>

<h3>int _validate_char(char _type)</h3>
<h4>Gets a type and checks if the passed parameter is present in a structure of valid conversion specifiers. Next, returns if the parameter is valid or invalid.</h4>

<h2>Return Value</h2>
<h4>Upon successful return, the _printf() function return the number of characters printed (excluding the null byte used to end output to strings).

If an output error is encountered, a negative value is returned.</h4>

<h2>Authors</h2>
<h3>t-Spirit & godwhin</h3>
