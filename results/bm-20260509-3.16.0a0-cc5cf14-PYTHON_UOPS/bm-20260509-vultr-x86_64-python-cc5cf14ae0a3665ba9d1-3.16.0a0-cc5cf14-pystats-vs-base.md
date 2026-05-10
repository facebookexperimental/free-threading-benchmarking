## Execution counts

<details>
<summary> Execution counts for Tier 1 instructions. </summary>


The "miss ratio" column shows the percentage of times the instruction
executed that it deoptimized. When this happens, the base unspecialized
instruction is not counted.

<table>
<thead>
<tr>
<th align="left">Name</th>
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">246,585,006</td>
<td align="right">1</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">GET_ITER_SELF</td>
<td align="right">428,256,955</td>
<td align="right">6</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">311,038,129</td>
<td align="right">5</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">115,485,441</td>
<td align="right">2</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">265,231,504</td>
<td align="right">6</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">68,230,950</td>
<td align="right">2</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">439,271,655</td>
<td align="right">17</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">66,583,079</td>
<td align="right">4</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">569,078,762</td>
<td align="right">39</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">5,799,737,319</td>
<td align="right">472</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,750,714,959</td>
<td align="right">147</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">325,048,719</td>
<td align="right">30</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">322,996,945</td>
<td align="right">30</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">131,278,125</td>
<td align="right">13</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">158,327,530</td>
<td align="right">16</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">194,947,420</td>
<td align="right">22</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,156,330</td>
<td align="right">1</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">10,717,900</td>
<td align="right">3</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">71,245,709</td>
<td align="right">20</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">10,171,093</td>
<td align="right">3</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">57,502,285</td>
<td align="right">23</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">4,807,060</td>
<td align="right">2</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">161,737,354</td>
<td align="right">74</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">354,547,440</td>
<td align="right">180</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">13,919,967</td>
<td align="right">8</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">175,001,236</td>
<td align="right">124</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">5,666,286</td>
<td align="right">5</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">216,495,244</td>
<td align="right">460</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">60,185,631</td>
<td align="right">148</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">2,060,345</td>
<td align="right">6</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">2,711,643,388</td>
<td align="right">8,588</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">617,812,153</td>
<td align="right">2,121</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">129,783,060</td>
<td align="right">460</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">125,241,530</td>
<td align="right">461</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,550,986,911</td>
<td align="right">6,180</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">3,438,362,924</td>
<td align="right">14,652</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,470,165,655</td>
<td align="right">7,098</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">231,319,501</td>
<td align="right">1,154</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,545,680,931</td>
<td align="right">9,445</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">156,733,735</td>
<td align="right">1,005</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,055,825,168</td>
<td align="right">8,047</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">55,338,634</td>
<td align="right">475</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">93,635,491</td>
<td align="right">920</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">676,430,873</td>
<td align="right">8,137</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,830,046,239</td>
<td align="right">22,024</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">4,698,817</td>
<td align="right">64</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">639,796,450</td>
<td align="right">8,899</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">60,543,669</td>
<td align="right">920</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">544,060,219</td>
<td align="right">8,517</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">882,762,694</td>
<td align="right">13,928</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">435,840,246</td>
<td align="right">7,066</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">2,142,967,157</td>
<td align="right">42,726</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">377,355,531</td>
<td align="right">7,540</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">418,983,256</td>
<td align="right">9,552</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">347,746,624</td>
<td align="right">8,180</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,461,109,088</td>
<td align="right">61,192</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">377,583,098</td>
<td align="right">9,634</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">191,195,628</td>
<td align="right">4,945</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">539,980,627</td>
<td align="right">14,580</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">1,821,012,012</td>
<td align="right">57,481</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">1,049,760,770</td>
<td align="right">33,633</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">452,552,749</td>
<td align="right">14,587</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">2,125,452,603</td>
<td align="right">70,142</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">249,987,045</td>
<td align="right">8,758</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">486,651,418</td>
<td align="right">17,178</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">214,162,092</td>
<td align="right">7,764</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,211,970,954</td>
<td align="right">44,521</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">5,758,815,794</td>
<td align="right">217,699</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,785,599,929</td>
<td align="right">113,797</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">4,150,350,902</td>
<td align="right">179,555</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,370,149,575</td>
<td align="right">61,479</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">298,984,253</td>
<td align="right">13,738</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">341,226,793</td>
<td align="right">15,811</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">689,150,003</td>
<td align="right">32,031</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">335,323,737</td>
<td align="right">15,743</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">GET_ITER_VIRTUAL</td>
<td align="right">489,474,896</td>
<td align="right">30,158</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">7,861,523</td>
<td align="right">485</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,615,574,066</td>
<td align="right">169,617</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">113,638,867</td>
<td align="right">7,763</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,201,638,267</td>
<td align="right">88,240</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">529,178,084</td>
<td align="right">39,299</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">14,473,209,581</td>
<td align="right">1,188,199</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">83,601,073</td>
<td align="right">7,092</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">803,819,758</td>
<td align="right">82,533</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">809,216,434</td>
<td align="right">84,873</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">764,864,907</td>
<td align="right">85,592</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">11,444,862,781</td>
<td align="right">1,288,467</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_EX_NON_PY_GENERAL</td>
<td align="right">193,916,569</td>
<td align="right">21,900</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">279,144,033</td>
<td align="right">37,269</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">496,229,604</td>
<td align="right">68,348</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">114,840,944</td>
<td align="right">16,324</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,114,622,746</td>
<td align="right">174,381</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">444,956,514</td>
<td align="right">71,398</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,632,624,530</td>
<td align="right">426,474</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">98,383,181</td>
<td align="right">16,322</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">90,633,656</td>
<td align="right">15,579</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">538,703,355</td>
<td align="right">93,737</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">4,829,832,659</td>
<td align="right">889,581</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">1,876,493,916</td>
<td align="right">354,079</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">74,041,253</td>
<td align="right">16,322</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">6,955,593,607</td>
<td align="right">1,947,673</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,735,836,260</td>
<td align="right">789,064</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">344,881,574</td>
<td align="right">104,407</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">114,327,499</td>
<td align="right">34,902</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">581,986,579</td>
<td align="right">186,339</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">142,312,370</td>
<td align="right">45,961</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">4,361</td>
<td align="right">2</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">828,203,474</td>
<td align="right">394,735</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">77,089,888</td>
<td align="right">37,901</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">64,041,829</td>
<td align="right">39,072</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">1,156,118,513</td>
<td align="right">744,244</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,199,921,174</td>
<td align="right">840,133</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">63,654,641</td>
<td align="right">50,038</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">449,204,951</td>
<td align="right">379,220</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">618,261,155</td>
<td align="right">541,135</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">444,112,734</td>
<td align="right">399,529</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">CALL_EX_PY</td>
<td align="right">23,616,075</td>
<td align="right">21,800</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">328,296,114</td>
<td align="right">354,827</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">361,319,169</td>
<td align="right">407,131</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">368,361,049</td>
<td align="right">707,331</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">874,316,585</td>
<td align="right">2,165,305</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">18,474,830</td>
<td align="right">60,642</td>
<td align="right">-99.7%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">2,385</td>
<td align="right">9</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">1,577,947</td>
<td align="right">5,979</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">14,734,008</td>
<td align="right">63,896</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">41,809,692,552</td>
<td align="right">294,765,807</td>
<td align="right">-99.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">11,985,371,301</td>
<td align="right">118,405,050</td>
<td align="right">-99.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,719,460,799</td>
<td align="right">58,276,395</td>
<td align="right">-98.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">7,366,826,964</td>
<td align="right">116,571,311</td>
<td align="right">-98.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">6,518,730,431</td>
<td align="right">117,522,472</td>
<td align="right">-98.2%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">17,634,389</td>
<td align="right">361,329</td>
<td align="right">-98.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">17,634,411</td>
<td align="right">361,331</td>
<td align="right">-98.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">17,230,862</td>
<td align="right">361,329</td>
<td align="right">-97.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">16,381,499</td>
<td align="right">352,838</td>
<td align="right">-97.8%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">5,075,083,643</td>
<td align="right">117,488,164</td>
<td align="right">-97.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">4,707,942,124</td>
<td align="right">117,487,388</td>
<td align="right">-97.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,960,950,884</td>
<td align="right">118,680,994</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">7,734,964,871</td>
<td align="right">233,186,139</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">3,752,716,758</td>
<td align="right">117,000,105</td>
<td align="right">-96.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">3,296,542,812</td>
<td align="right">116,771,470</td>
<td align="right">-96.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,931,587,491</td>
<td align="right">116,542,987</td>
<td align="right">-94.0%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,903,005,350</td>
<td align="right">117,022,355</td>
<td align="right">-93.9%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">179,011</td>
<td align="right">15,148</td>
<td align="right">-91.5%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">126,934</td>
<td align="right">24,120</td>
<td align="right">-81.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">589,271,028</td>
<td align="right">116,536,320</td>
<td align="right">-80.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">212,388</td>
<td align="right">58,372</td>
<td align="right">-72.5%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">407,301,740</td>
<td align="right">116,544,846</td>
<td align="right">-71.4%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">11,846</td>
<td align="right">4,230</td>
<td align="right">-64.3%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">295,708,076</td>
<td align="right">116,536,320</td>
<td align="right">-60.6%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">11,678</td>
<td align="right">6,146</td>
<td align="right">-47.4%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">6,399</td>
<td align="right">4,174</td>
<td align="right">-34.8%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">172,683,388</td>
<td align="right">116,536,320</td>
<td align="right">-32.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,599,577,992</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_USTR_INT</td>
<td align="right">1,198,906,074</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,079,436,173</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">511,084,047</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">415,369,803</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">195,701,199</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">140,557,823</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">123,951,901</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">116,395,937</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">112,724,677</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">100,136,760</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND_ASYNC_GEN</td>
<td align="right">100,136,760</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">94,136,760</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">80,284,001</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">67,383,456</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">63,654,180</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">62,748,373</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">59,558,652</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INSTRUMENTED_LINE</td>
<td align="right">58,270,440</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">41,927,102</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">40,797,501</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME</td>
<td align="right">29,134,740</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_VALUE</td>
<td align="right">29,134,440</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">21,979,105</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_VIRTUAL</td>
<td align="right">16,436,599</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">13,487,298</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">8,968,253</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_AITER</td>
<td align="right">6,000,000</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">END_ASYNC_FOR</td>
<td align="right">6,000,000</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">5,297,559</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">4,370,514</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND_VIRTUAL</td>
<td align="right">1,317,634</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">235,809</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">124,922</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">68,064</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">49,275</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">39,517</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">14,791</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MATCH_CLASS</td>
<td align="right">14,340</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">9,392</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">3,540</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">3,406</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">2,740</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FROM_DICT_OR_DEREF</td>
<td align="right">1,460</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">1,360</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SETUP_ANNOTATIONS</td>
<td align="right">124</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">120</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">15</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME_CHECK_JIT</td>
<td align="right"></td>
<td align="right">944,068</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right"></td>
<td align="right">130,207</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TRACE_RECORD</td>
<td align="right"></td>
<td align="right">1,000</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

## Pair counts

<details>
<summary> Pair counts for top 100 opcode pairs </summary>


Pairs of specialized operations that deoptimize and are then followed by
the corresponding unspecialized instruction are not counted as pairs.

Not included in comparative output.


</details>

## Predecessor/Successor Pairs

<details>
<summary> Top 5 predecessors and successors of each Tier 1 opcode. </summary>


This does not include the unspecialized instructions that occur after a
specialized instruction deoptimizes.

Not included in comparative output.


</details>

## Specialization stats

<details>
<summary> Specialization stats by family </summary>

### BINARY_OP

<details>
<summary> specialization stats for BINARY_OP family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">59,463,935</td>
<td align="right">0.4%</td>
<td align="right">29</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,550,694,729</td>
<td align="right">9.3%</td>
<td align="right">3,206</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">15,082,538,741</td>
<td align="right">90.4%</td>
<td align="right">175,222,482</td>
<td align="right">100.0%</td>
<td align="right">-98.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">274,492</td>
<td align="right">19.4%</td>
<td align="right">3</td>
<td align="right">0.1%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,139,391</td>
<td align="right">80.6%</td>
<td align="right">2,972</td>
<td align="right">99.9%</td>
<td align="right">-99.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">out of range</td>
<td align="right">17,038</td>
<td align="right">6.2%</td>
<td align="right">1</td>
<td align="right">33.3%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">10,944</td>
<td align="right">4.0%</td>
<td align="right">2</td>
<td align="right">66.7%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">subscr array</td>
<td align="right">63,958</td>
<td align="right">23.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">45,235</td>
<td align="right">16.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">21,736</td>
<td align="right">7.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">17,185</td>
<td align="right">6.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">11,631</td>
<td align="right">4.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">11,249</td>
<td align="right">4.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr bytes</td>
<td align="right">11,164</td>
<td align="right">4.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">9,585</td>
<td align="right">3.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">xor int</td>
<td align="right">9,100</td>
<td align="right">3.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">7,985</td>
<td align="right">2.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">7,612</td>
<td align="right">2.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">7,410</td>
<td align="right">2.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">5,836</td>
<td align="right">2.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">4,592</td>
<td align="right">1.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">2,767</td>
<td align="right">1.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr range</td>
<td align="right">1,600</td>
<td align="right">0.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">1,536</td>
<td align="right">0.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">1,328</td>
<td align="right">0.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">1,247</td>
<td align="right">0.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">1,004</td>
<td align="right">0.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">821</td>
<td align="right">0.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">579</td>
<td align="right">0.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">405</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr mappingproxy</td>
<td align="right">240</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr other slice</td>
<td align="right">187</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">160</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr structtime</td>
<td align="right">140</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">or different types</td>
<td align="right">69</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr deque</td>
<td align="right">66</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">22</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">or int</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr re match</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### BINARY_SLICE

<details>
<summary> specialization stats for BINARY_SLICE family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">544,060,219</td>
<td align="right">100.0%</td>
<td align="right">8,517</td>
<td align="right">100.0%</td>
<td align="right">-100.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL

<details>
<summary> specialization stats for CALL family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">189,292,999</td>
<td align="right">1.5%</td>
<td align="right">29,809</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">12,686,547,639</td>
<td align="right">98.5%</td>
<td align="right">119,059,608</td>
<td align="right">100.0%</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">192,872,430</td>
<td align="right">1.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">146</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,791,673</td>
<td align="right">100.0%</td>
<td align="right">28,563</td>
<td align="right">100.0%</td>
<td align="right">-99.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">init not simple</td>
<td align="right">771</td>
<td align="right">528.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">265</td>
<td align="right">181.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">146</td>
<td align="right">100.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### CALL_FUNCTION_EX

<details>
<summary> specialization stats for CALL_FUNCTION_EX family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">20,083</td>
<td align="right">63.2%</td>
<td align="right">900</td>
<td align="right">12.8%</td>
<td align="right">-95.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">23,357</td>
<td align="right">73.5%</td>
<td align="right">4,026</td>
<td align="right">57.1%</td>
<td align="right">-82.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">8,404</td>
<td align="right">100.0%</td>
<td align="right">3,020</td>
<td align="right">100.0%</td>
<td align="right">-64.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### CALL_KW

<details>
<summary> specialization stats for CALL_KW family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">75,763</td>
<td align="right">88.2%</td>
<td align="right">2,089</td>
<td align="right">49.4%</td>
<td align="right">-97.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">74,009</td>
<td align="right">86.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">10,092</td>
<td align="right">100.0%</td>
<td align="right">2,141</td>
<td align="right">100.0%</td>
<td align="right">-78.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP

<details>
<summary> specialization stats for COMPARE_OP family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,734,187</td>
<td align="right">0.0%</td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">529,021,063</td>
<td align="right">9.0%</td>
<td align="right">23,289</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,320,556,063</td>
<td align="right">90.9%</td>
<td align="right">116,793,491</td>
<td align="right">100.0%</td>
<td align="right">-97.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">135,086</td>
<td align="right">71.2%</td>
<td align="right">1,000</td>
<td align="right">6.2%</td>
<td align="right">-99.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">54,520</td>
<td align="right">28.8%</td>
<td align="right">15,010</td>
<td align="right">93.8%</td>
<td align="right">-72.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">tuple</td>
<td align="right">42,611</td>
<td align="right">31.5%</td>
<td align="right">20</td>
<td align="right">2.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">27,733</td>
<td align="right">20.5%</td>
<td align="right">980</td>
<td align="right">98.0%</td>
<td align="right">-96.5%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">27,248</td>
<td align="right">20.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">15,563</td>
<td align="right">11.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">5,789</td>
<td align="right">4.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">5,571</td>
<td align="right">4.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">4,852</td>
<td align="right">3.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">3,420</td>
<td align="right">2.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">1,056</td>
<td align="right">0.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">628</td>
<td align="right">0.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">534</td>
<td align="right">0.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">81</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### CONTAINS_OP

<details>
<summary> specialization stats for CONTAINS_OP family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,188,607,124</td>
<td align="right">90.4%</td>
<td align="right">164</td>
<td align="right">12.4%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">231,279,891</td>
<td align="right">9.6%</td>
<td align="right">1,152</td>
<td align="right">87.4%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,379,490</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">27,702</td>
<td align="right">42.2%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">37,940</td>
<td align="right">57.8%</td>
<td align="right">2</td>
<td align="right">100.0%</td>
<td align="right">-100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">str</td>
<td align="right">13,078</td>
<td align="right">34.5%</td>
<td align="right">2</td>
<td align="right">100.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">14,290</td>
<td align="right">37.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">5,526</td>
<td align="right">14.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">5,046</td>
<td align="right">13.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER

<details>
<summary> specialization stats for FOR_ITER family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,469,938,867</td>
<td align="right">28.6%</td>
<td align="right">3,865</td>
<td align="right">2.5%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,505,782,050</td>
<td align="right">68.2%</td>
<td align="right">144,605</td>
<td align="right">95.3%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">163,357,464</td>
<td align="right">3.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">3,087,999</td>
<td align="right">93.3%</td>
<td align="right">2,587</td>
<td align="right">80.0%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">220,866</td>
<td align="right">6.7%</td>
<td align="right">646</td>
<td align="right">20.0%</td>
<td align="right">-99.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">enumerate</td>
<td align="right">17,322</td>
<td align="right">7.8%</td>
<td align="right">2</td>
<td align="right">0.3%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">1,485</td>
<td align="right">0.7%</td>
<td align="right">2</td>
<td align="right">0.3%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">4,691</td>
<td align="right">2.1%</td>
<td align="right">642</td>
<td align="right">99.4%</td>
<td align="right">-86.3%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">80,629</td>
<td align="right">36.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">43,834</td>
<td align="right">19.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">41,779</td>
<td align="right">18.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">9,045</td>
<td align="right">4.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">7,856</td>
<td align="right">3.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">7,395</td>
<td align="right">3.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">5,091</td>
<td align="right">2.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">1,523</td>
<td align="right">0.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">106</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">66</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">44</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### GET_ITER

<details>
<summary> specialization stats for GET_ITER family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">191,146,374</td>
<td align="right">17.2%</td>
<td align="right">2,840</td>
<td align="right">8.1%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">917,624,433</td>
<td align="right">82.7%</td>
<td align="right">30,164</td>
<td align="right">85.9%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">107,418</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">39,703</td>
<td align="right">77.5%</td>
<td align="right">60</td>
<td align="right">2.9%</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">11,549</td>
<td align="right">22.5%</td>
<td align="right">2,045</td>
<td align="right">97.1%</td>
<td align="right">-82.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">other</td>
<td align="right">39,703</td>
<td align="right">100.0%</td>
<td align="right">60</td>
<td align="right">100.0%</td>
<td align="right">-99.8%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR

<details>
<summary> specialization stats for LOAD_ATTR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">839,662,059</td>
<td align="right">4.9%</td>
<td align="right">6</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">807,738,214</td>
<td align="right">4.7%</td>
<td align="right">46,948</td>
<td align="right">3.3%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">15,607,568,907</td>
<td align="right">90.4%</td>
<td align="right">1,337,541</td>
<td align="right">94.0%</td>
<td align="right">-100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">15,921,661</td>
<td align="right">98.7%</td>
<td align="right">36,905</td>
<td align="right">97.4%</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">215,572</td>
<td align="right">1.3%</td>
<td align="right">980</td>
<td align="right">2.6%</td>
<td align="right">-99.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">method</td>
<td align="right">41,401</td>
<td align="right">19.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">31,272</td>
<td align="right">14.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">16,998</td>
<td align="right">7.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">12,444</td>
<td align="right">5.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">7,121</td>
<td align="right">3.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">3,877</td>
<td align="right">1.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">3,108</td>
<td align="right">1.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">1,424</td>
<td align="right">0.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">888</td>
<td align="right">0.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">650</td>
<td align="right">0.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">623</td>
<td align="right">0.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">462</td>
<td align="right">0.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">422</td>
<td align="right">0.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">220</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">62</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">slot after items</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">audited slot</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">4</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### LOAD_GLOBAL

<details>
<summary> specialization stats for LOAD_GLOBAL family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">14,611,301</td>
<td align="right">0.1%</td>
<td align="right">32,400</td>
<td align="right">0.0%</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">10,916,492,188</td>
<td align="right">99.9%</td>
<td align="right">120,620,465</td>
<td align="right">99.9%</td>
<td align="right">-98.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">52,303</td>
<td align="right">0.0%</td>
<td align="right">8,202</td>
<td align="right">0.0%</td>
<td align="right">-84.3%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,462</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">123,635</td>
<td align="right">100.0%</td>
<td align="right">31,496</td>
<td align="right">100.0%</td>
<td align="right">-74.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### LOAD_SUPER_ATTR

<details>
<summary> specialization stats for LOAD_SUPER_ATTR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">70,953,593</td>
<td align="right">100.0%</td>
<td align="right">4</td>
<td align="right">30.8%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">108</td>
<td align="right">0.0%</td>
<td align="right">5</td>
<td align="right">38.5%</td>
<td align="right">-95.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">2,277</td>
<td align="right">100.0%</td>
<td align="right">4</td>
<td align="right">100.0%</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### RESUME

<details>
<summary> specialization stats for RESUME family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">152,386</td>
<td align="right">46.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">150,266</td>
<td align="right">46.5%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">173,231</td>
<td align="right">53.5%</td>
<td align="right">15,148</td>
<td align="right">100.0%</td>
<td align="right">-91.3%</td>
</tr>
</tbody>
</table>


</details>

### SEND

<details>
<summary> specialization stats for SEND family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">589,254,646</td>
<td align="right">96.4%</td>
<td align="right">116,536,320</td>
<td align="right">100.0%</td>
<td align="right">-80.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">21,975,699</td>
<td align="right">3.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">32,734</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">991</td>
<td align="right">24.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">3,034</td>
<td align="right">75.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">other</td>
<td align="right">3,034</td>
<td align="right">100.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### STORE_ATTR

<details>
<summary> specialization stats for STORE_ATTR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,607,167,264</td>
<td align="right">93.6%</td>
<td align="right">174,381</td>
<td align="right">77.7%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">63,590,158</td>
<td align="right">2.3%</td>
<td align="right">35,231</td>
<td align="right">15.7%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">116,001,727</td>
<td align="right">4.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">2,226,532</td>
<td align="right">98.8%</td>
<td align="right">11,907</td>
<td align="right">80.4%</td>
<td align="right">-99.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">25,942</td>
<td align="right">1.2%</td>
<td align="right">2,900</td>
<td align="right">19.6%</td>
<td align="right">-88.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">class attr simple</td>
<td align="right">11,088</td>
<td align="right">42.7%</td>
<td align="right">1,920</td>
<td align="right">66.2%</td>
<td align="right">-82.7%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1,669</td>
<td align="right">6.4%</td>
<td align="right">980</td>
<td align="right">33.8%</td>
<td align="right">-41.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">90,137</td>
<td align="right">347.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">5,172</td>
<td align="right">19.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">3,040</td>
<td align="right">11.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">1,999</td>
<td align="right">7.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">933</td>
<td align="right">3.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">525</td>
<td align="right">2.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">291</td>
<td align="right">1.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">225</td>
<td align="right">0.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">88</td>
<td align="right">0.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">60</td>
<td align="right">0.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">48</td>
<td align="right">0.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### STORE_SLICE

<details>
<summary> specialization stats for STORE_SLICE family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">112,724,677</td>
<td align="right">100.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### STORE_SUBSCR

<details>
<summary> specialization stats for STORE_SUBSCR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">617,728,332</td>
<td align="right">37.7%</td>
<td align="right">1,057</td>
<td align="right">6.3%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,021,631,511</td>
<td align="right">62.3%</td>
<td align="right">14,626</td>
<td align="right">87.3%</td>
<td align="right">-100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">80,810</td>
<td align="right">96.4%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,011</td>
<td align="right">3.6%</td>
<td align="right">1,064</td>
<td align="right">100.0%</td>
<td align="right">-64.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">other</td>
<td align="right">40,590</td>
<td align="right">50.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">26,138</td>
<td align="right">32.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">9,008</td>
<td align="right">11.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">2,669</td>
<td align="right">3.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">1,511</td>
<td align="right">1.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">849</td>
<td align="right">1.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">array slice</td>
<td align="right">45</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL

<details>
<summary> specialization stats for TO_BOOL family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">102,662,647</td>
<td align="right">1.6%</td>
<td align="right">18</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">444,644,957</td>
<td align="right">7.0%</td>
<td align="right">50,945</td>
<td align="right">3.6%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,773,315,109</td>
<td align="right">91.3%</td>
<td align="right">1,335,409</td>
<td align="right">94.9%</td>
<td align="right">-100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">1,985,061</td>
<td align="right">88.3%</td>
<td align="right">17,373</td>
<td align="right">84.9%</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">262,227</td>
<td align="right">11.7%</td>
<td align="right">3,080</td>
<td align="right">15.1%</td>
<td align="right">-98.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">dict</td>
<td align="right">8,330</td>
<td align="right">3.2%</td>
<td align="right">100</td>
<td align="right">3.2%</td>
<td align="right">-98.8%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">66,005</td>
<td align="right">25.2%</td>
<td align="right">1,980</td>
<td align="right">64.3%</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">4,028</td>
<td align="right">1.5%</td>
<td align="right">1,000</td>
<td align="right">32.5%</td>
<td align="right">-75.2%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">140,447</td>
<td align="right">53.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">28,223</td>
<td align="right">10.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">8,071</td>
<td align="right">3.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">3,500</td>
<td align="right">1.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">3,380</td>
<td align="right">1.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">221</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">memory view</td>
<td align="right">22</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE

<details>
<summary> specialization stats for UNPACK_SEQUENCE family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,243,921,022</td>
<td align="right">99.9%</td>
<td align="right">90,073</td>
<td align="right">93.8%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,567,928</td>
<td align="right">0.1%</td>
<td align="right">3,132</td>
<td align="right">3.3%</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,640</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Failure</td>
<td align="right">435</td>
<td align="right">4.3%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">9,644</td>
<td align="right">95.7%</td>
<td align="right">2,847</td>
<td align="right">100.0%</td>
<td align="right">-70.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">sequence</td>
<td align="right">319</td>
<td align="right">73.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">65</td>
<td align="right">14.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">51</td>
<td align="right">11.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>


</details>

## Specialization effectiveness

<details>
<summary> specialization effectiveness </summary>


All entries are execution counts. Should add up to the total number of
Tier 1 instructions executed.

<table>
<thead>
<tr>
<th align="left">Instructions</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,477,575,512</td>
<td align="right">0.6%</td>
<td align="right">9,158</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">6,603,978,785</td>
<td align="right">2.8%</td>
<td align="right">429,403</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">92,401,844,071</td>
<td align="right">39.1%</td>
<td align="right">769,886,215</td>
<td align="right">34.3%</td>
<td align="right">-99.2%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">135,904,724,161</td>
<td align="right">57.5%</td>
<td align="right">1,474,963,562</td>
<td align="right">65.7%</td>
<td align="right">-98.9%</td>
</tr>
</tbody>
</table>

### Deferred by instruction

<details>
<summary> Breakdown of deferred (not specialized) instruction counts by family </summary>

<table>
<thead>
<tr>
<th align="left">Name</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,550,694,729</td>
<td align="right">22.8%</td>
<td align="right">3,206</td>
<td align="right">1.3%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,469,938,867</td>
<td align="right">21.6%</td>
<td align="right">3,865</td>
<td align="right">1.6%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">544,060,219</td>
<td align="right">8.0%</td>
<td align="right">8,517</td>
<td align="right">3.4%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">529,021,063</td>
<td align="right">7.8%</td>
<td align="right">23,289</td>
<td align="right">9.4%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">807,738,214</td>
<td align="right">11.9%</td>
<td align="right">46,948</td>
<td align="right">18.9%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">444,644,957</td>
<td align="right">6.5%</td>
<td align="right">50,945</td>
<td align="right">20.5%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">189,292,999</td>
<td align="right">2.8%</td>
<td align="right">29,809</td>
<td align="right">12.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">617,728,332</td>
<td align="right">9.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">231,279,891</td>
<td align="right">3.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">191,146,374</td>
<td align="right">2.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">35,231</td>
<td align="right">14.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">32,400</td>
<td align="right">13.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">4,026</td>
<td align="right">1.6%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### Misses by instruction

<details>
<summary> Breakdown of misses (specialized deopts) instruction counts by family </summary>

<table>
<thead>
<tr>
<th align="left">Name</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">48,990,674</td>
<td align="right">3.3%</td>
<td align="right">15</td>
<td align="right">0.2%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">365,116,478</td>
<td align="right">24.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">256,834,351</td>
<td align="right">17.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">95,759,690</td>
<td align="right">6.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">89,516,960</td>
<td align="right">6.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">86,856,769</td>
<td align="right">5.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">81,817,108</td>
<td align="right">5.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">81,436,928</td>
<td align="right">5.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">77,358,447</td>
<td align="right">5.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">47,384,650</td>
<td align="right">3.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">8,202</td>
<td align="right">89.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_EX_NON_PY_GENERAL</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">460</td>
<td align="right">5.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_EX_PY</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">440</td>
<td align="right">4.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">21</td>
<td align="right">0.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">6</td>
<td align="right">0.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">5</td>
<td align="right">0.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>


</details>

## Call stats

<details>
<summary> Inlined calls and frame stats </summary>


This shows what fraction of calls to Python functions are inlined (i.e.
not having a call at the C level) and for those that are not, where the
call comes from.  The various categories overlap.

Also includes the count of frame objects created.

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">5,002</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">3,406</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">140,980,853</td>
<td align="right">1.8%</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">305,069,656</td>
<td align="right">4.0%</td>
<td align="right">128</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">458,542,652</td>
<td align="right">6.0%</td>
<td align="right">8,045</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">547,825,828</td>
<td align="right">7.1%</td>
<td align="right">16,567</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">1,825,302,684</td>
<td align="right">23.7%</td>
<td align="right">58,669</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">1,825,302,684</td>
<td align="right">23.7%</td>
<td align="right">58,669</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,277,476,856</td>
<td align="right">16.6%</td>
<td align="right">42,102</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,277,468,448</td>
<td align="right">16.6%</td>
<td align="right">42,102</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">70,510,713</td>
<td align="right">0.9%</td>
<td align="right">360,967</td>
<td align="right">0.2%</td>
<td align="right">-99.5%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,573,677,764</td>
<td align="right">85.4%</td>
<td align="right">117,522,511</td>
<td align="right">50.2%</td>
<td align="right">-98.2%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">5,873,510,976</td>
<td align="right">76.3%</td>
<td align="right">234,016,704</td>
<td align="right">100.0%</td>
<td align="right">-96.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">11,304</td>
<td align="right">0.0%</td>
<td align="right">2,022</td>
<td align="right">0.0%</td>
<td align="right">-82.1%</td>
</tr>
</tbody>
</table>


</details>

## Object stats

<details>
<summary> Allocations, frees and dict materializatons </summary>


Below, "allocations" means "allocations that are not from a freelist".
Total allocations = "Allocations from freelist" + "Allocations".

"Inline values" is the number of values arrays inlined into objects.

The cache hit/miss numbers are for the MRO cache, split into dunder and
other names.

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">4,027,523</td>
<td align="right">2.1%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">307,249</td>
<td align="right">0.2%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">4,404</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">2,200,624,271</td>
<td align="right"></td>
<td align="right">174,539</td>
<td align="right"></td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">193,262,128</td>
<td align="right"></td>
<td align="right">23,705</td>
<td align="right"></td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">13,096,608,665</td>
<td align="right">69.4%</td>
<td align="right">1,930,366</td>
<td align="right">1.5%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">13,099,706,181</td>
<td align="right"></td>
<td align="right">1,954,646</td>
<td align="right"></td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">71,504,337</td>
<td align="right">0.4%</td>
<td align="right">20,961</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">2,889,887,169</td>
<td align="right"></td>
<td align="right">856,833</td>
<td align="right"></td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">20,490,476,955</td>
<td align="right">19.3%</td>
<td align="right">6,714,429</td>
<td align="right">0.9%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">6,676,969</td>
<td align="right">0.0%</td>
<td align="right">3,682</td>
<td align="right">0.0%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">56,828,181</td>
<td align="right"></td>
<td align="right">38,801</td>
<td align="right"></td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">51,338,597</td>
<td align="right"></td>
<td align="right">35,963</td>
<td align="right"></td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">24,276,158,276</td>
<td align="right">26.3%</td>
<td align="right">27,209,512</td>
<td align="right">3.6%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">29,174,684,762</td>
<td align="right">27.5%</td>
<td align="right">34,012,958</td>
<td align="right">4.5%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">6,292,762</td>
<td align="right"></td>
<td align="right">12,711</td>
<td align="right"></td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">21,747,207,572</td>
<td align="right">23.6%</td>
<td align="right">129,011,868</td>
<td align="right">17.3%</td>
<td align="right">-99.4%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">41,592,169,180</td>
<td align="right">45.1%</td>
<td align="right">356,966,482</td>
<td align="right">47.8%</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">54,226,116,382</td>
<td align="right">51.2%</td>
<td align="right">475,103,669</td>
<td align="right">63.4%</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">6,389,403,617</td>
<td align="right"></td>
<td align="right">124,898,631</td>
<td align="right"></td>
<td align="right">-98.0%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">5,786,445,808</td>
<td align="right">30.6%</td>
<td align="right">123,546,433</td>
<td align="right">98.5%</td>
<td align="right">-97.9%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">5,708,264,502</td>
<td align="right">30.2%</td>
<td align="right">123,521,790</td>
<td align="right">98.4%</td>
<td align="right">-97.8%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">4,591,285,888</td>
<td align="right">5.0%</td>
<td align="right">233,276,302</td>
<td align="right">31.3%</td>
<td align="right">-94.9%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">2,025,341,836</td>
<td align="right">1.9%</td>
<td align="right">233,151,496</td>
<td align="right">31.1%</td>
<td align="right">-88.5%</td>
</tr>
<tr>
<td align="left">Materialize dict (str subclass)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

## GC stats

<details>
<summary> GC collections and effectiveness </summary>


Collected/visits gives some measure of efficiency.

<table>
<thead>
<tr>
<th align="right">Generation</th>
<th align="right">Base Collections</th>
<th align="right">Base Objects collected</th>
<th align="right">Base Object visits</th>
<th align="right">Base Reachable from roots</th>
<th align="right">Base Not reachable from roots</th>
<th align="right">Head Collections</th>
<th align="right">Head Objects collected</th>
<th align="right">Head Object visits</th>
<th align="right">Head Reachable from roots</th>
<th align="right">Head Not reachable from roots</th>
</tr>
</thead>
<tbody>
<tr>
<td align="right">0</td>
<td align="right">326,353</td>
<td align="right">53,738,726</td>
<td align="right">6,535,876,170</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
</tr>
<tr>
<td align="right">1</td>
<td align="right">29,304</td>
<td align="right">17,161,887</td>
<td align="right">4,527,995,783</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">18,613</td>
<td align="right">50,044,777</td>
<td align="right">15,227,115,736</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
</tr>
</tbody>
</table>


</details>

## Optimization (Tier 2) stats

<details>
<summary> statistics about the Tier 2 optimizer </summary>


</details>

## Rare events

<details>
<summary> Counts of rare/unlikely events </summary>

<table>
<thead>
<tr>
<th align="left">Event</th>
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
set class
<details>
<summary>ⓘ</summary>

Setting an object's class, `obj.__class__ = ...`
</details>
</td>
<td align="right">22,592</td>
<td align="right">0</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
set bases
<details>
<summary>ⓘ</summary>

Setting the bases of a class, `cls.__bases__ = ...`
</details>
</td>
<td align="right">22</td>
<td align="right">0</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
func modification
<details>
<summary>ⓘ</summary>

Modifying a function, e.g. `func.__defaults__ = ...`, etc.
</details>
</td>
<td align="right">314</td>
<td align="right">0</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
watched dict modification
<details>
<summary>ⓘ</summary>

A watched dict has been modified
</details>
</td>
<td align="right">6,183,744</td>
<td align="right">1</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
set eval frame func
<details>
<summary>ⓘ</summary>

Setting the PEP 523 frame eval function `_PyInterpreterState_SetFrameEvalFunc()`
</details>
</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
builtin dict
<details>
<summary>ⓘ</summary>

Modifying the builtins, `__builtins__.__dict__[var] = ...`
</details>
</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
</details>
</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

## Meta stats

<details>
<summary> Meta statistics </summary>

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Number of data files</td>
<td align="right">2,394</td>
<td align="right">642</td>
<td align="right">-73.2%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2026-05-10
