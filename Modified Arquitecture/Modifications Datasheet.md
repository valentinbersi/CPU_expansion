<table>
  <tr>
    <th>Instruction</th>
    <th>CodOp</th>
    <th>Format</th>
    <th>Action</th>
  </tr>
  <tr>
    <td>SIG Rx</td>
    <td>01001</td>
    <td>B</td>
    <td>Rx ← Rx + 1, does not update the flags</td>
  </tr>
  <tr>
    <td>MIX Rx Ry</td>
    <td>01011</td>
    <td>A</td>
    <td>Rx ← Ry1 Rx6 Ry3 Rx4 Ry5 Rx2 Ry7 Rx0</td>
  </tr>
  <tr>
    <td>NEG Rx</td>
    <td>01010</td>
    <td>B</td>
    <td>Rx ← -Rx</td>
  </tr>
  <tr>
    <td>JMPR Rx</td>
    <td>01100</td>
    <td>B</td>
    <td>PC ← Rx</td>
  </tr>
  <tr>
    <td>JCR Rx</td>
    <td>01101</td>
    <td>B</td>
    <td>Si flagC == 1 entonces PC ← Rx</td>
  </tr>
  <tr>
    <td>JZR Rx</td>
    <td>01110</td>
    <td>B</td>
    <td>Si flagZ == 1 entonces PC ← Rx</td>
  </tr>
  <tr>
    <td>JNR Rx</td>
    <td>01111</td>
    <td>B</td>
    <td>Si flagN == 1 entonces PC ← Rx</td>
  </tr>
  <tr>
    <td>CALL Rx M</td>
    <td>11100</td>
    <td>D</td>
    <td>Rx ← Rx + 1, Mem[Rx] ← PC, PC ← M</td>
  </tr>
  <tr>
    <td>RET Rx</td>
    <td>11101</td>
    <td>B</td>
    <td>PC <- Mem[Rx], Rx ← Rx - 1</td>
  </tr>
  <tr>
    <td>STR [Rx+cte5], Ry</td>
    <td>10010</td>
    <td>E</td>
    <td>Mem[Rx + cte5] ← Ry</td>
  </tr>
  <tr>
    <td>LOAD Rx, [Ry+cte5]</td>
    <td>10011</td>
    <td>E</td>
    <td>Rx ← Mem[Ry + cte5]</td>
  </tr>
  <tr>
    <td>WFLAGS cte3</td>
    <td>00010</td>
    <td>E</td>
    <td>Flags ← cte3</td>
  </tr>
  <tr>
    <td>RFLAGS Rx</td>
    <td>11110</td>
    <td>B</td>
    <td>Rx ← Flags</td>
  </tr>
</table>