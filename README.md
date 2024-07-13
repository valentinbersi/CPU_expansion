# CPU Expansion
 A task from the subject Computer Organization.

The subject consisted on modifing the given CPU and it's assembler. The next modifications where made to the arquitecture:

<ul>
    <li>
        Added the instruction SIG that increases the value of a register by 1 without updating the flags. This operations does not requiere new circuits.
    </li><p>
    <li>
        Added the instruction MIX that mixes the values of two registers. The result of using two 8 bit numbers represented like A7−0 y B7−0 is: B1 A6 B3 A4 B5 A2 B7 A0. This operation requieres a new circuit called mixer, this operation is accessed via the ALU.
    </li><p>
    <li>
        Added the instruction NEG that returns the inversive additive of a number without updating the flags. This instrucctions doesn´t requiere new circuits.
    </li><p>
    <li>
        Added the instructions JMPR, JZR, JNR and JCR to make a jump taking a register as parameter.
    </li><p>
    <li>
        Added the instructions CALL and RET to enable the modularization of code for the CPU. The register given to this instructions is the one used as stack pointer. These instructions don´t requiere new circuits.
    </li><p>
    <li>
        Modified the instructions STR and LOAD to be able to receive an offset in the memory address. This instructions requiered an extension of the decoder to decode the 5 bit offset.
    </li><p>
    <li>
        Added the instructions WFLAGS and RFLAGS to read and write the flags. This instructions requiere a conection from the X register input to the ALU to be able to write the flags.
    </li>
</ul>

Also, the assembler was modified to parse the new instructions and the modifications of the existing ones.

The instruction ADC was removed due to the 32 operations limit (5 bit operations)
