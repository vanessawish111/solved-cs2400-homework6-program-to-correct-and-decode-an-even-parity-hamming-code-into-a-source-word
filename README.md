Download Link: https://assignmentchef.com/product/solved-cs2400-homework6-program-to-correct-and-decode-an-even-parity-hamming-code-into-a-source-word
<br>
Write an ARM program to <strong>correct</strong> and <strong>decode</strong> an <strong>even-parity</strong> <strong>Hamming code</strong> into a <strong>source word</strong>

<ul>

 <li>in the data area, o define a symbol called <strong>MAX_LEN</strong> and equivalent it with a number like 100

  <ul>

   <li>declare and initialize a <strong><em>NULL-terminated string</em></strong> as a <strong>Hamming code</strong>, label it as <strong>HCode,</strong> and initialize it using the value of your choice (each byte is the ASCII of a bit in your Hamming code). For example, the string could be “11111100<strong>0</strong>001101”, 0x0 for <strong><em>case 1</em></strong></li>

   <li>reserve a <strong><em>chunk of zeroed memory</em></strong> with a length of <strong>MAX_LEN</strong> bytes, label this chunk of memory as</li>

  </ul></li>

</ul>

<strong>SrcWord</strong>, which will be used to store a Null-terminated string representing the corrected <strong>source word</strong>.

<ul>

 <li>Store each one of the above four labels as a word with an address label, e.g., “adrHCode DCD HCode” for HCode, and <strong>EXPORT</strong> each address label, e.g., “EXPORT adrHCode”.</li>

</ul>

<ul>

 <li>in the main program, o go through the Hamming code string via examining EACH bit (data bit and check bit), count the total number of 1’s in EACH check bit’s parity and update the relevant counters for the check-bits.

  <ul>

   <li>go through the counters to find all the <strong>check bits</strong> whose <strong>parities</strong> are NOT <strong>even</strong>, and add together the <strong>sequence numbers</strong> of all those <strong>check bits </strong>whose <strong>parities</strong> are NOT <strong>even</strong>.</li>

   <li>use the above sum of the <strong>sequence numbers</strong> to find THE INCORRECT bit if ANY in Hamming code , and</li>

  </ul></li>

</ul>

<strong>invert</strong> this bit

<ul>

 <li>go through the CORRECTED <strong>hamming code</strong> to retrieve the <strong>source word</strong>, and store the source word at SRC_WORD as a NULL-terminated string.</li>

</ul>

<strong>Suggested Test cases for your program: </strong>

<strong><em>Case 1</em></strong>: use “11111100<strong>0</strong>001101” as the Hamming code, your program is going to detect that bit #9 in this Hamming code is transmitted wrong, correct it as ‘<strong>1</strong>’, and extract the source word “11101001101” as a NULL-terminated string at

SRC_WORD

<strong><em>Case 2</em></strong>: use “010011100101” as the Hamming code, your program is going to detect that NO bit in this Hamming code has an even-parity-error, and extract the source word “01110101” as a NULL-terminated string at SRC_WORD

More cases: you may use HW5a posted on blackboard to find more pairs of Hamming code and source word, then

<ul>

 <li>use this Hamming code as the No-Even-Parity-Error case like case 2</li>

 <li>invert ONE bit in this Hamming code and use it as the Even-Parity-Error case like case 1</li>

</ul>








