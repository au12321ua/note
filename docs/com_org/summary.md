一些汇总内容：

# 常用指令

| Instruction | Opcode  | Funct3 | Funct6/7 | type |
| :---------: | :-----: | :----: | :------: | :--: |
|     add     | 0110011 |  000   | 0000000  |  R   |
|     sub     | 0110011 |  000   | 0100000  |  R   |
|     sll     | 0110011 |  001   | 0000000  |  R   |
|     xor     | 0110011 |  100   | 0000000  |  R   |
|     srl     | 0110011 |  101   | 0000000  |  R   |
|     sra     | 0110011 |  101   | 0000000  |  R   |
|     or      | 0110011 |  110   | 0000000  |  R   |
|     and     | 0110011 |  111   | 0000000  |  R   |
|    lr.d     | 0110011 |  011   | 0001000  |  R   |
|    sc.d     | 0110011 |  011   | 0001100  |  R   |
|     lb      | 0000011 |  000   |   n.a.   |  I   |
|     lh      | 0000011 |  001   |   n.a.   |  I   |
|     lw      | 0000011 |  010   |   n.a.   |  I   |
|     ld      | 0000011 |  011   |   n.a.   |  I   |
|     lbu     | 0000011 |  100   |   n.a.   |  I   |
|     lhu     | 0000011 |  101   |   n.a.   |  I   |
|     lwu     | 0000011 |  110   |   n.a.   |  I   |
|    addi     | 0010011 |  000   |   n.a.   |  I   |
|    slli     | 0010011 |  001   |  000000  |  I   |
|    xori     | 0010011 |  100   |   n.a.   |  I   |
|    srli     | 0010011 |  101   |  000000  |  I   |
|    srai     | 0010011 |  101   |  010000  |  I   |
|     ori     | 0010011 |  110   |   n.a.   |  I   |
|    andi     | 0010011 |  111   |   n.a.   |  I   |
|    jalr     | 1100111 |  000   |   n.a.   |  I   |
|     sb      | 0100011 |  000   |   n.a.   |  S   |
|     sh      | 0100011 |  001   |   n.a.   |  S   |
|     sw      | 0100011 |  010   |   n.a.   |  S   |
|     sd      | 0100011 |  111   |   n.a.   |  S   |
|     beq     | 1100111 |  000   |   n.a.   |  B   |
|     bne     | 1100111 |  001   |   n.a.   |  B   |
|     blt     | 1100111 |  100   |   n.a.   |  B   |
|     bge     | 1100111 |  101   |   n.a.   |  B   |
|    bltu     | 1100111 |  110   |   n.a.   |  B   |
|    bgeu     | 1100111 |  111   |   n.a.   |  B   |
|     lui     | 0110111 |  n.a.  |   n.a.   |  U   |
|     jal     | 1101111 |  n.a.  |   n.a.   |  UJ  |
