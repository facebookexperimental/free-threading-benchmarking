
# Pystats results

- benchmark: concurrent_imap
- fork: python
- ref: main
- commit hash: 6d93690
- commit date: 2024-10-18T09:26:08-06:00

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
<th align="right">Count</th>
<th align="right">Self</th>
<th align="right">Cumulative</th>
<th align="right">Miss ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">82,676,544</td>
<td align="right">15.1%</td>
<td align="right">15.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">37,904,914</td>
<td align="right">6.9%</td>
<td align="right">22.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">31,761,746</td>
<td align="right">5.8%</td>
<td align="right">27.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">29,038,000</td>
<td align="right">5.3%</td>
<td align="right">33.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">27,073,300</td>
<td align="right">5.0%</td>
<td align="right">38.2%</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">26,691,354</td>
<td align="right">4.9%</td>
<td align="right">43.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">20,535,423</td>
<td align="right">3.8%</td>
<td align="right">46.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">18,180,344</td>
<td align="right">3.3%</td>
<td align="right">50.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">13,714,394</td>
<td align="right">2.5%</td>
<td align="right">52.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">12,481,380</td>
<td align="right">2.3%</td>
<td align="right">54.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">12,287,027</td>
<td align="right">2.2%</td>
<td align="right">57.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">11,811,673</td>
<td align="right">2.2%</td>
<td align="right">59.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">11,722,186</td>
<td align="right">2.1%</td>
<td align="right">61.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">11,639,900</td>
<td align="right">2.1%</td>
<td align="right">63.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">11,460,720</td>
<td align="right">2.1%</td>
<td align="right">65.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">11,390,891</td>
<td align="right">2.1%</td>
<td align="right">67.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">10,921,236</td>
<td align="right">2.0%</td>
<td align="right">69.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">10,845,851</td>
<td align="right">2.0%</td>
<td align="right">71.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">10,088,295</td>
<td align="right">1.8%</td>
<td align="right">73.6%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">9,035,673</td>
<td align="right">1.7%</td>
<td align="right">75.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">7,552,411</td>
<td align="right">1.4%</td>
<td align="right">76.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">7,398,658</td>
<td align="right">1.4%</td>
<td align="right">78.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">7,269,302</td>
<td align="right">1.3%</td>
<td align="right">79.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">7,066,106</td>
<td align="right">1.3%</td>
<td align="right">80.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">5,692,456</td>
<td align="right">1.0%</td>
<td align="right">81.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,592,695</td>
<td align="right">1.0%</td>
<td align="right">82.7%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">5,255,066</td>
<td align="right">1.0%</td>
<td align="right">83.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">5,023,867</td>
<td align="right">0.9%</td>
<td align="right">84.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">4,479,755</td>
<td align="right">0.8%</td>
<td align="right">85.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">4,332,154</td>
<td align="right">0.8%</td>
<td align="right">86.2%</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">4,292,843</td>
<td align="right">0.8%</td>
<td align="right">87.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">4,022,375</td>
<td align="right">0.7%</td>
<td align="right">87.7%</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,429,918</td>
<td align="right">0.6%</td>
<td align="right">88.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">3,409,650</td>
<td align="right">0.6%</td>
<td align="right">89.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">3,388,314</td>
<td align="right">0.6%</td>
<td align="right">89.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">3,290,894</td>
<td align="right">0.6%</td>
<td align="right">90.2%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">2,754,342</td>
<td align="right">0.5%</td>
<td align="right">90.7%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,523,223</td>
<td align="right">0.5%</td>
<td align="right">91.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">2,423,159</td>
<td align="right">0.4%</td>
<td align="right">91.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">2,320,780</td>
<td align="right">0.4%</td>
<td align="right">92.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">2,275,447</td>
<td align="right">0.4%</td>
<td align="right">92.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">2,246,118</td>
<td align="right">0.4%</td>
<td align="right">92.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">2,237,452</td>
<td align="right">0.4%</td>
<td align="right">93.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">2,111,464</td>
<td align="right">0.4%</td>
<td align="right">93.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">2,106,720</td>
<td align="right">0.4%</td>
<td align="right">94.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">1,843,502</td>
<td align="right">0.3%</td>
<td align="right">94.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,621,497</td>
<td align="right">0.3%</td>
<td align="right">94.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,618,123</td>
<td align="right">0.3%</td>
<td align="right">95.0%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,537,679</td>
<td align="right">0.3%</td>
<td align="right">95.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">1,504,215</td>
<td align="right">0.3%</td>
<td align="right">95.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">1,410,121</td>
<td align="right">0.3%</td>
<td align="right">95.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,389,840</td>
<td align="right">0.3%</td>
<td align="right">96.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">1,343,469</td>
<td align="right">0.2%</td>
<td align="right">96.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,326,458</td>
<td align="right">0.2%</td>
<td align="right">96.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">1,260,427</td>
<td align="right">0.2%</td>
<td align="right">96.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">1,155,385</td>
<td align="right">0.2%</td>
<td align="right">97.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">1,140,780</td>
<td align="right">0.2%</td>
<td align="right">97.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">1,112,609</td>
<td align="right">0.2%</td>
<td align="right">97.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">1,051,100</td>
<td align="right">0.2%</td>
<td align="right">97.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">1,004,826</td>
<td align="right">0.2%</td>
<td align="right">97.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">895,081</td>
<td align="right">0.2%</td>
<td align="right">97.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">564,786</td>
<td align="right">0.1%</td>
<td align="right">98.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">527,327</td>
<td align="right">0.1%</td>
<td align="right">98.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">509,225</td>
<td align="right">0.1%</td>
<td align="right">98.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">471,701</td>
<td align="right">0.1%</td>
<td align="right">98.3%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">470,106</td>
<td align="right">0.1%</td>
<td align="right">98.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">445,032</td>
<td align="right">0.1%</td>
<td align="right">98.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">419,704</td>
<td align="right">0.1%</td>
<td align="right">98.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">398,526</td>
<td align="right">0.1%</td>
<td align="right">98.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">348,265</td>
<td align="right">0.1%</td>
<td align="right">98.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">290,621</td>
<td align="right">0.1%</td>
<td align="right">98.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">273,627</td>
<td align="right">0.1%</td>
<td align="right">98.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">266,705</td>
<td align="right">0.0%</td>
<td align="right">98.8%</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">260,060</td>
<td align="right">0.0%</td>
<td align="right">98.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">259,480</td>
<td align="right">0.0%</td>
<td align="right">98.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">254,292</td>
<td align="right">0.0%</td>
<td align="right">99.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">235,656</td>
<td align="right">0.0%</td>
<td align="right">99.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">217,084</td>
<td align="right">0.0%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">215,640</td>
<td align="right">0.0%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">211,460</td>
<td align="right">0.0%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">195,964</td>
<td align="right">0.0%</td>
<td align="right">99.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">190,120</td>
<td align="right">0.0%</td>
<td align="right">99.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">188,203</td>
<td align="right">0.0%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">179,073</td>
<td align="right">0.0%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">171,960</td>
<td align="right">0.0%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">171,960</td>
<td align="right">0.0%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">166,898</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">160,180</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">155,997</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">148,565</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">147,165</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">141,524</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">138,180</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">138,140</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">125,400</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">123,040</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">113,400</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">110,920</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">110,885</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">103,272</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right">40.2%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">95,718</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">95,080</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">89,410</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">88,309</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">88,242</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">85,423</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">82,230</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">76,500</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">74,860</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">73,320</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">71,300</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">69,130</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">58,880</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">53,740</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">53,660</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">51,700</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">50,464</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">50,464</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">42,880</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">40,064</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">35,136</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">32,880</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">32,460</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">31,260</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">25,558</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">21,780</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">20,800</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">18,984</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">18,640</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">10,520</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">10,400</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">9,180</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">8,320</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">5,100</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">4,860</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">2,420</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">1,540</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">1,220</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">1,040</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">980</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">900</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">560</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">500</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">400</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">340</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">320</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">223</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
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

<table>
<thead>
<tr>
<th align="left">Pair</th>
<th align="right">Count</th>
<th align="right">Self</th>
<th align="right">Cumulative</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">24,558,883</td>
<td align="right">4.5%</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_FAST</td>
<td align="right">20,944,618</td>
<td align="right">3.8%</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">POP_TOP JUMP_BACKWARD</td>
<td align="right">13,947,393</td>
<td align="right">2.6%</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">CACHE RESUME_CHECK</td>
<td align="right">13,470,496</td>
<td align="right">2.5%</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST RETURN_VALUE</td>
<td align="right">12,543,672</td>
<td align="right">2.3%</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK POP_TOP</td>
<td align="right">12,481,200</td>
<td align="right">2.3%</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE INTERPRETER_EXIT</td>
<td align="right">11,790,839</td>
<td align="right">2.2%</td>
<td align="right">20.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST JUMP_BACKWARD</td>
<td align="right">11,518,188</td>
<td align="right">2.1%</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD FOR_ITER_GEN</td>
<td align="right">11,439,920</td>
<td align="right">2.1%</td>
<td align="right">24.3%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE STORE_FAST</td>
<td align="right">11,439,920</td>
<td align="right">2.1%</td>
<td align="right">26.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN RESUME_CHECK</td>
<td align="right">11,439,920</td>
<td align="right">2.1%</td>
<td align="right">28.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD FOR_ITER_LIST</td>
<td align="right">10,841,215</td>
<td align="right">2.0%</td>
<td align="right">30.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST STORE_FAST_LOAD_FAST</td>
<td align="right">10,400,260</td>
<td align="right">1.9%</td>
<td align="right">32.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST YIELD_VALUE</td>
<td align="right">10,400,000</td>
<td align="right">1.9%</td>
<td align="right">34.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_FAST</td>
<td align="right">8,620,787</td>
<td align="right">1.6%</td>
<td align="right">35.8%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS RESUME_CHECK</td>
<td align="right">7,467,471</td>
<td align="right">1.4%</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">6,577,717</td>
<td align="right">1.2%</td>
<td align="right">38.4%</td>
</tr>
<tr>
<td align="left">NOP LOAD_FAST</td>
<td align="right">6,450,504</td>
<td align="right">1.2%</td>
<td align="right">39.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST PUSH_NULL</td>
<td align="right">6,193,389</td>
<td align="right">1.1%</td>
<td align="right">40.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST LOAD_CONST</td>
<td align="right">5,555,311</td>
<td align="right">1.0%</td>
<td align="right">41.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_FAST</td>
<td align="right">5,180,558</td>
<td align="right">0.9%</td>
<td align="right">42.7%</td>
</tr>
<tr>
<td align="left">COPY STORE_FAST</td>
<td align="right">5,146,560</td>
<td align="right">0.9%</td>
<td align="right">43.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST COPY</td>
<td align="right">5,146,400</td>
<td align="right">0.9%</td>
<td align="right">44.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL LOAD_FAST</td>
<td align="right">5,118,539</td>
<td align="right">0.9%</td>
<td align="right">45.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE POP_TOP</td>
<td align="right">4,885,950</td>
<td align="right">0.9%</td>
<td align="right">46.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_FAST</td>
<td align="right">4,687,409</td>
<td align="right">0.9%</td>
<td align="right">47.3%</td>
</tr>
<tr>
<td align="left">POP_TOP LOAD_FAST</td>
<td align="right">4,462,784</td>
<td align="right">0.8%</td>
<td align="right">48.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST NOP</td>
<td align="right">3,881,069</td>
<td align="right">0.7%</td>
<td align="right">48.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST POP_TOP</td>
<td align="right">3,616,975</td>
<td align="right">0.7%</td>
<td align="right">49.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_FUNCTION_EX</td>
<td align="right">3,338,915</td>
<td align="right">0.6%</td>
<td align="right">50.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT POP_JUMP_IF_FALSE</td>
<td align="right">3,244,123</td>
<td align="right">0.6%</td>
<td align="right">50.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL RESUME_CHECK</td>
<td align="right">3,190,903</td>
<td align="right">0.6%</td>
<td align="right">51.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL CALL_NON_PY_GENERAL</td>
<td align="right">2,861,590</td>
<td align="right">0.5%</td>
<td align="right">51.8%</td>
</tr>
<tr>
<td align="left">SWAP SWAP</td>
<td align="right">2,827,472</td>
<td align="right">0.5%</td>
<td align="right">52.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT LOAD_FAST</td>
<td align="right">2,750,947</td>
<td align="right">0.5%</td>
<td align="right">52.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_ATTR_MODULE</td>
<td align="right">2,748,100</td>
<td align="right">0.5%</td>
<td align="right">53.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_CONST</td>
<td align="right">2,724,941</td>
<td align="right">0.5%</td>
<td align="right">53.8%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL STORE_FAST</td>
<td align="right">2,700,156</td>
<td align="right">0.5%</td>
<td align="right">54.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST POP_JUMP_IF_NOT_NONE</td>
<td align="right">2,685,758</td>
<td align="right">0.5%</td>
<td align="right">54.8%</td>
</tr>
<tr>
<td align="left">COPY LOAD_SPECIAL</td>
<td align="right">2,627,533</td>
<td align="right">0.5%</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL SWAP</td>
<td align="right">2,627,533</td>
<td align="right">0.5%</td>
<td align="right">55.7%</td>
</tr>
<tr>
<td align="left">SWAP LOAD_SPECIAL</td>
<td align="right">2,627,533</td>
<td align="right">0.5%</td>
<td align="right">56.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST CALL_PY_GENERAL</td>
<td align="right">2,626,048</td>
<td align="right">0.5%</td>
<td align="right">56.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE LOAD_FAST</td>
<td align="right">2,591,138</td>
<td align="right">0.5%</td>
<td align="right">57.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_ATTR</td>
<td align="right">2,553,700</td>
<td align="right">0.5%</td>
<td align="right">57.7%</td>
</tr>
<tr>
<td align="left">POP_TOP LOAD_CONST</td>
<td align="right">2,504,263</td>
<td align="right">0.5%</td>
<td align="right">58.1%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL RETURN_VALUE</td>
<td align="right">2,470,787</td>
<td align="right">0.5%</td>
<td align="right">58.6%</td>
</tr>
<tr>
<td align="left">POP_TOP RETURN_CONST</td>
<td align="right">2,435,812</td>
<td align="right">0.4%</td>
<td align="right">59.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT CALL_NON_PY_GENERAL</td>
<td align="right">2,433,212</td>
<td align="right">0.4%</td>
<td align="right">59.5%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL CALL_PY_EXACT_ARGS</td>
<td align="right">2,426,254</td>
<td align="right">0.4%</td>
<td align="right">59.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN LOAD_FAST</td>
<td align="right">2,397,340</td>
<td align="right">0.4%</td>
<td align="right">60.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,364,102</td>
<td align="right">0.4%</td>
<td align="right">60.8%</td>
</tr>
<tr>
<td align="left">PUSH_NULL LOAD_FAST_LOAD_FAST</td>
<td align="right">2,327,408</td>
<td align="right">0.4%</td>
<td align="right">61.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE COPY</td>
<td align="right">2,311,538</td>
<td align="right">0.4%</td>
<td align="right">61.6%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX RETURN_VALUE</td>
<td align="right">2,288,335</td>
<td align="right">0.4%</td>
<td align="right">62.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR PUSH_NULL</td>
<td align="right">2,270,542</td>
<td align="right">0.4%</td>
<td align="right">62.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD FOR_ITER</td>
<td align="right">2,264,302</td>
<td align="right">0.4%</td>
<td align="right">62.9%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD LOAD_FAST</td>
<td align="right">2,263,346</td>
<td align="right">0.4%</td>
<td align="right">63.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">2,245,376</td>
<td align="right">0.4%</td>
<td align="right">63.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE STORE_FAST_STORE_FAST</td>
<td align="right">2,234,958</td>
<td align="right">0.4%</td>
<td align="right">64.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_FALSE</td>
<td align="right">2,234,878</td>
<td align="right">0.4%</td>
<td align="right">64.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_GLOBAL_MODULE</td>
<td align="right">2,218,368</td>
<td align="right">0.4%</td>
<td align="right">64.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST LOAD_FAST</td>
<td align="right">2,194,878</td>
<td align="right">0.4%</td>
<td align="right">65.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE PUSH_NULL</td>
<td align="right">2,193,040</td>
<td align="right">0.4%</td>
<td align="right">65.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR POP_JUMP_IF_FALSE</td>
<td align="right">2,177,720</td>
<td align="right">0.4%</td>
<td align="right">66.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE COMPARE_OP_STR</td>
<td align="right">2,165,505</td>
<td align="right">0.4%</td>
<td align="right">66.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST COPY</td>
<td align="right">2,106,560</td>
<td align="right">0.4%</td>
<td align="right">66.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS POP_TOP</td>
<td align="right">2,091,340</td>
<td align="right">0.4%</td>
<td align="right">67.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST BUILD_TUPLE</td>
<td align="right">2,091,260</td>
<td align="right">0.4%</td>
<td align="right">67.7%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE YIELD_VALUE</td>
<td align="right">2,080,300</td>
<td align="right">0.4%</td>
<td align="right">68.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD NOP</td>
<td align="right">2,080,000</td>
<td align="right">0.4%</td>
<td align="right">68.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST BINARY_OP_ADD_INT</td>
<td align="right">2,075,080</td>
<td align="right">0.4%</td>
<td align="right">68.8%</td>
</tr>
<tr>
<td align="left">COPY STORE_FAST_STORE_FAST</td>
<td align="right">2,074,400</td>
<td align="right">0.4%</td>
<td align="right">69.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST STORE_FAST</td>
<td align="right">2,064,800</td>
<td align="right">0.4%</td>
<td align="right">69.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE STORE_FAST_STORE_FAST</td>
<td align="right">2,064,740</td>
<td align="right">0.4%</td>
<td align="right">69.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST UNPACK_SEQUENCE_TUPLE</td>
<td align="right">2,064,000</td>
<td align="right">0.4%</td>
<td align="right">70.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST LOAD_FAST</td>
<td align="right">1,881,845</td>
<td align="right">0.3%</td>
<td align="right">70.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,812,633</td>
<td align="right">0.3%</td>
<td align="right">71.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES CALL_PY_EXACT_ARGS</td>
<td align="right">1,764,067</td>
<td align="right">0.3%</td>
<td align="right">71.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST LOAD_FAST</td>
<td align="right">1,715,673</td>
<td align="right">0.3%</td>
<td align="right">71.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST POP_JUMP_IF_NONE</td>
<td align="right">1,700,922</td>
<td align="right">0.3%</td>
<td align="right">71.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,538,864</td>
<td align="right">0.3%</td>
<td align="right">72.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR</td>
<td align="right">1,504,380</td>
<td align="right">0.3%</td>
<td align="right">72.5%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_GLOBAL_MODULE</td>
<td align="right">1,460,053</td>
<td align="right">0.3%</td>
<td align="right">72.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,398,061</td>
<td align="right">0.3%</td>
<td align="right">73.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST LOAD_FAST_LOAD_FAST</td>
<td align="right">1,397,172</td>
<td align="right">0.3%</td>
<td align="right">73.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_FAST_LOAD_FAST</td>
<td align="right">1,378,716</td>
<td align="right">0.3%</td>
<td align="right">73.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O POP_TOP</td>
<td align="right">1,377,795</td>
<td align="right">0.3%</td>
<td align="right">73.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST CALL_NON_PY_GENERAL</td>
<td align="right">1,371,407</td>
<td align="right">0.3%</td>
<td align="right">74.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP LOAD_FAST</td>
<td align="right">1,350,839</td>
<td align="right">0.2%</td>
<td align="right">74.3%</td>
</tr>
<tr>
<td align="left">GET_ITER FOR_ITER_LIST</td>
<td align="right">1,346,418</td>
<td align="right">0.2%</td>
<td align="right">74.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST BUILD_TUPLE</td>
<td align="right">1,338,387</td>
<td align="right">0.2%</td>
<td align="right">74.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_PY_EXACT_ARGS</td>
<td align="right">1,333,039</td>
<td align="right">0.2%</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_CONST</td>
<td align="right">1,328,119</td>
<td align="right">0.2%</td>
<td align="right">75.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">1,324,815</td>
<td align="right">0.2%</td>
<td align="right">75.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST TO_BOOL</td>
<td align="right">1,318,399</td>
<td align="right">0.2%</td>
<td align="right">75.7%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT POP_JUMP_IF_FALSE</td>
<td align="right">1,259,547</td>
<td align="right">0.2%</td>
<td align="right">76.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE NOP</td>
<td align="right">1,258,870</td>
<td align="right">0.2%</td>
<td align="right">76.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST TO_BOOL_BOOL</td>
<td align="right">1,258,844</td>
<td align="right">0.2%</td>
<td align="right">76.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE CONTAINS_OP_DICT</td>
<td align="right">1,258,207</td>
<td align="right">0.2%</td>
<td align="right">76.7%</td>
</tr>
</tbody>
</table>


</details>

## Predecessor/Successor Pairs

<details>
<summary> Top 5 predecessors and successors of each Tier 1 opcode. </summary>


This does not include the unspecialized instructions that occur after a
specialized instruction deoptimizes.

### BINARY_SLICE

<details>
<summary> Successors and predecessors for BINARY_SLICE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">31,480</td>
<td align="right">95.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">680</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">680</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">40</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">31,440</td>
<td align="right">95.6%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">680</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">680</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">80</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### CACHE

<details>
<summary> Successors and predecessors for CACHE </summary>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">13,470,496</td>
<td align="right">98.1%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">239,419</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">11,740</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">2,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">960</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR

<details>
<summary> Successors and predecessors for BINARY_SUBSCR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,040,080</td>
<td align="right">93.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">71,544</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">905</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,039,920</td>
<td align="right">93.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">70,124</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">1,020</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">905</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_INPLACE_ADD_UNICODE

<details>
<summary> Successors and predecessors for BINARY_OP_INPLACE_ADD_UNICODE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">51,600</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">60</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">40</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">51,640</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">60</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### CHECK_EXC_MATCH

<details>
<summary> Successors and predecessors for CHECK_EXC_MATCH </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">29,744</td>
<td align="right">74.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">10,220</td>
<td align="right">25.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">80</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">40,064</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### DELETE_SUBSCR

<details>
<summary> Successors and predecessors for DELETE_SUBSCR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">72,659</td>
<td align="right">43.5%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">51,639</td>
<td align="right">30.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">42,480</td>
<td align="right">25.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">113,759</td>
<td align="right">68.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">32,160</td>
<td align="right">19.3%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">20,479</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">500</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>


</details>

### END_FOR

<details>
<summary> Successors and predecessors for END_FOR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">20,800</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">20,800</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### EXIT_INIT_CHECK

<details>
<summary> Successors and predecessors for EXIT_INIT_CHECK </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">138,140</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">138,140</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### FORMAT_SIMPLE

<details>
<summary> Successors and predecessors for FORMAT_SIMPLE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">52,000</td>
<td align="right">54.7%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">42,880</td>
<td align="right">45.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">200</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">73,320</td>
<td align="right">77.1%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">21,520</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">240</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>


</details>

### GET_ITER

<details>
<summary> Successors and predecessors for GET_ITER </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">1,040,000</td>
<td align="right">64.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">450,432</td>
<td align="right">27.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">86,765</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">21,460</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">10,400</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">1,346,418</td>
<td align="right">83.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">123,234</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">76,167</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">21,698</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">21,600</td>
<td align="right">1.3%</td>
</tr>
</tbody>
</table>


</details>

### INTERPRETER_EXIT

<details>
<summary> Successors and predecessors for INTERPRETER_EXIT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">11,790,839</td>
<td align="right">86.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,041,460</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">882,095</td>
<td align="right">6.4%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_BUILD_CLASS

<details>
<summary> Successors and predecessors for LOAD_BUILD_CLASS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">880</td>
<td align="right">89.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">100</td>
<td align="right">10.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">980</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_LOCALS

<details>
<summary> Successors and predecessors for LOAD_LOCALS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">900</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">900</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### MAKE_FUNCTION

<details>
<summary> Successors and predecessors for MAKE_FUNCTION </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">113,400</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">74,860</td>
<td align="right">66.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">21,440</td>
<td align="right">18.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">10,800</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">4,560</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">980</td>
<td align="right">0.9%</td>
</tr>
</tbody>
</table>


</details>

### NOP

<details>
<summary> Successors and predecessors for NOP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,881,069</td>
<td align="right">34.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">2,080,000</td>
<td align="right">18.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,258,870</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,240,568</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">1,151,167</td>
<td align="right">10.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">6,450,504</td>
<td align="right">56.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,173,330</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,091,240</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,073,260</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">1,061,420</td>
<td align="right">9.3%</td>
</tr>
</tbody>
</table>


</details>

### POP_EXCEPT

<details>
<summary> Successors and predecessors for POP_EXCEPT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COPY</td>
<td align="right">20,860</td>
<td align="right">41.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">18,644</td>
<td align="right">36.9%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">10,840</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">60</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">60</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RERAISE</td>
<td align="right">20,860</td>
<td align="right">41.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">18,644</td>
<td align="right">36.9%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">10,240</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">340</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">200</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>


</details>

### POP_TOP

<details>
<summary> Successors and predecessors for POP_TOP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">12,481,200</td>
<td align="right">46.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,885,950</td>
<td align="right">18.3%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">3,616,975</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">2,091,340</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">1,377,795</td>
<td align="right">5.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">13,947,393</td>
<td align="right">52.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,462,784</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,504,263</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">2,435,812</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">1,240,568</td>
<td align="right">4.6%</td>
</tr>
</tbody>
</table>


</details>

### PUSH_EXC_INFO

<details>
<summary> Successors and predecessors for PUSH_EXC_INFO </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">28,004</td>
<td align="right">55.5%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">10,460</td>
<td align="right">20.7%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">10,220</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">1,120</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">320</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">29,684</td>
<td align="right">58.8%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">10,400</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">10,200</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">180</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>


</details>

### PUSH_NULL

<details>
<summary> Successors and predecessors for PUSH_NULL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">6,193,389</td>
<td align="right">57.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">2,270,542</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">2,193,040</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">83,760</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">58,880</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,118,539</td>
<td align="right">47.2%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">2,861,590</td>
<td align="right">26.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,327,408</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">389,385</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">86,120</td>
<td align="right">0.8%</td>
</tr>
</tbody>
</table>


</details>

### RETURN_GENERATOR

<details>
<summary> Successors and predecessors for RETURN_GENERATOR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">31,420</td>
<td align="right">96.8%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">860</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">180</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">10,400</td>
<td align="right">32.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">10,400</td>
<td align="right">32.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">10,400</td>
<td align="right">32.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">680</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">460</td>
<td align="right">1.4%</td>
</tr>
</tbody>
</table>


</details>

### RETURN_VALUE

<details>
<summary> Successors and predecessors for RETURN_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">12,543,672</td>
<td align="right">61.1%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">2,470,787</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">2,288,335</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">1,088,789</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">545,685</td>
<td align="right">2.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">11,790,839</td>
<td align="right">57.4%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">4,885,950</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,025,260</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">951,137</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">338,500</td>
<td align="right">1.6%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SUBSCR

<details>
<summary> Successors and predecessors for STORE_SUBSCR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">21,440</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20,720</td>
<td align="right">38.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">10,440</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">640</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">200</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">31,960</td>
<td align="right">59.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">20,440</td>
<td align="right">38.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">640</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">300</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">120</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL

<details>
<summary> Successors and predecessors for TO_BOOL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,318,399</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">2,421</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">880</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">798</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">720</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,127,689</td>
<td align="right">85.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">193,242</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">2,421</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,126</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">380</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### UNARY_INVERT

<details>
<summary> Successors and predecessors for UNARY_INVERT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">218,367</td>
<td align="right">62.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">129,818</td>
<td align="right">37.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">348,265</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### UNARY_NOT

<details>
<summary> Successors and predecessors for UNARY_NOT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">95,638</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">80</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">95,718</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### WITH_EXCEPT_START

<details>
<summary> Successors and predecessors for WITH_EXCEPT_START </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">10,400</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">10,320</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">80</td>
<td align="right">0.8%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP

<details>
<summary> Successors and predecessors for BINARY_OP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">719,890</td>
<td align="right">46.8%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">348,265</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">218,367</td>
<td align="right">14.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">86,409</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">51,680</td>
<td align="right">3.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COPY</td>
<td align="right">566,632</td>
<td align="right">36.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">316,690</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">218,627</td>
<td align="right">14.2%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">218,367</td>
<td align="right">14.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">89,622</td>
<td align="right">5.8%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_LIST

<details>
<summary> Successors and predecessors for BUILD_LIST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">147,099</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">123,214</td>
<td align="right">27.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">65,289</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">59,625</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">34,125</td>
<td align="right">7.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">159,899</td>
<td align="right">35.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">148,419</td>
<td align="right">33.4%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">123,214</td>
<td align="right">27.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">10,240</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">880</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_MAP

<details>
<summary> Successors and predecessors for BUILD_MAP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,056,740</td>
<td align="right">43.6%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,040,080</td>
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">167,539</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">83,760</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">32,180</td>
<td align="right">1.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,350,839</td>
<td align="right">55.7%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,040,020</td>
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">31,600</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">140</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_SET

<details>
<summary> Successors and predecessors for BUILD_SET </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">20</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">20</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_STRING

<details>
<summary> Successors and predecessors for BUILD_STRING </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">51,800</td>
<td align="right">70.6%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">21,520</td>
<td align="right">29.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">51,600</td>
<td align="right">70.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">21,440</td>
<td align="right">29.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">200</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">80</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_TUPLE

<details>
<summary> Successors and predecessors for BUILD_TUPLE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,091,260</td>
<td align="right">36.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,338,387</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">1,040,020</td>
<td align="right">18.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,025,260</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">64,949</td>
<td align="right">1.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">2,080,300</td>
<td align="right">36.5%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">1,040,080</td>
<td align="right">18.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,024,000</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">1,023,960</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">218,287</td>
<td align="right">3.8%</td>
</tr>
</tbody>
</table>


</details>

### CALL

<details>
<summary> Successors and predecessors for CALL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,900</td>
<td align="right">22.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,549</td>
<td align="right">15.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">4,772</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">3,469</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,506</td>
<td align="right">7.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">5,040</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">4,120</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">3,726</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">3,180</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">2,640</td>
<td align="right">7.5%</td>
</tr>
</tbody>
</table>


</details>

### CALL_FUNCTION_EX

<details>
<summary> Successors and predecessors for CALL_FUNCTION_EX </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,338,915</td>
<td align="right">74.5%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">1,140,780</td>
<td align="right">25.5%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">2,288,335</td>
<td align="right">51.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,087,200</td>
<td align="right">24.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">1,023,960</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">69,280</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">10,600</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### CALL_INTRINSIC_1

<details>
<summary> Successors and predecessors for CALL_INTRINSIC_1 </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">400</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">340</td>
<td align="right">85.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">60</td>
<td align="right">15.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_KW

<details>
<summary> Successors and predecessors for CALL_KW </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,540</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">520</td>
<td align="right">33.8%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">220</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">200</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">200</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">120</td>
<td align="right">7.8%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP

<details>
<summary> Successors and predecessors for COMPARE_OP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">173,860</td>
<td align="right">97.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">996</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">880</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">700</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">628</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">92,710</td>
<td align="right">51.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">82,877</td>
<td align="right">46.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,968</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">996</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">422</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### CONTAINS_OP

<details>
<summary> Successors and predecessors for CONTAINS_OP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">120</td>
<td align="right">37.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">120</td>
<td align="right">37.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">80</td>
<td align="right">25.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">120</td>
<td align="right">37.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">100</td>
<td align="right">31.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">80</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">20</td>
<td align="right">6.2%</td>
</tr>
</tbody>
</table>


</details>

### CONVERT_VALUE

<details>
<summary> Successors and predecessors for CONVERT_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">21,400</td>
<td align="right">49.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">21,400</td>
<td align="right">49.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">40</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">40</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">42,880</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### COPY

<details>
<summary> Successors and predecessors for COPY </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,146,400</td>
<td align="right">43.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">2,311,538</td>
<td align="right">19.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,106,560</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,082,980</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">566,632</td>
<td align="right">4.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,146,560</td>
<td align="right">43.9%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">2,627,533</td>
<td align="right">22.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">2,074,400</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,039,840</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">566,312</td>
<td align="right">4.8%</td>
</tr>
</tbody>
</table>


</details>

### COPY_FREE_VARS

<details>
<summary> Successors and predecessors for COPY_FREE_VARS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CACHE</td>
<td align="right">239,419</td>
<td align="right">50.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">218,747</td>
<td align="right">46.5%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">10,360</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">980</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">300</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">468,846</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">860</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">400</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### DELETE_ATTR

<details>
<summary> Successors and predecessors for DELETE_ATTR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">155,997</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">103,998</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">51,679</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">280</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### DICT_MERGE

<details>
<summary> Successors and predecessors for DICT_MERGE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,056,820</td>
<td align="right">92.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">83,760</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">1,140,780</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### EXTENDED_ARG

<details>
<summary> Successors and predecessors for EXTENDED_ARG </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">340</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">340</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER

<details>
<summary> Successors and predecessors for FOR_ITER </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">2,264,302</td>
<td align="right">97.6%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">21,698</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">21,600</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">11,180</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">2,000</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">1,212,040</td>
<td align="right">52.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">1,050,660</td>
<td align="right">45.3%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">21,580</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">21,500</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">10,320</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>


</details>

### IMPORT_FROM

<details>
<summary> Successors and predecessors for IMPORT_FROM </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">146,605</td>
<td align="right">99.6%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">560</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">144,745</td>
<td align="right">98.4%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">2,420</td>
<td align="right">1.6%</td>
</tr>
</tbody>
</table>


</details>

### IMPORT_NAME

<details>
<summary> Successors and predecessors for IMPORT_NAME </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">148,565</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">146,605</td>
<td align="right">98.7%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">1,860</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">100</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### IS_OP

<details>
<summary> Successors and predecessors for IS_OP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">51,680</td>
<td align="right">60.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">31,780</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,843</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">120</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">84,923</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">500</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>


</details>

### JUMP_BACKWARD

<details>
<summary> Successors and predecessors for JUMP_BACKWARD </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">13,947,393</td>
<td align="right">48.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">11,518,188</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">1,050,400</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">1,040,000</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,011,834</td>
<td align="right">3.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">11,439,920</td>
<td align="right">39.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">10,841,215</td>
<td align="right">37.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">2,264,302</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,263,346</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,080,000</td>
<td align="right">7.2%</td>
</tr>
</tbody>
</table>


</details>

### JUMP_BACKWARD_NO_INTERRUPT

<details>
<summary> Successors and predecessors for JUMP_BACKWARD_NO_INTERRUPT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">18,644</td>
<td align="right">98.2%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">340</td>
<td align="right">1.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">17,644</td>
<td align="right">92.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,340</td>
<td align="right">7.1%</td>
</tr>
</tbody>
</table>


</details>

### JUMP_FORWARD

<details>
<summary> Successors and predecessors for JUMP_FORWARD </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">344,940</td>
<td align="right">65.4%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">80,605</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">48,162</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">32,180</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">10,360</td>
<td align="right">2.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">235,647</td>
<td align="right">44.7%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">147,099</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">58,562</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">41,979</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">32,860</td>
<td align="right">6.2%</td>
</tr>
</tbody>
</table>


</details>

### LIST_APPEND

<details>
<summary> Successors and predecessors for LIST_APPEND </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">171,960</td>
<td align="right">59.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">64,969</td>
<td align="right">22.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">47,492</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">6,160</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">290,621</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### LIST_EXTEND

<details>
<summary> Successors and predecessors for LIST_EXTEND </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">34,685</td>
<td align="right">50.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">34,025</td>
<td align="right">49.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">360</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">60</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">34,185</td>
<td align="right">49.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">34,025</td>
<td align="right">49.2%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">400</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">340</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">160</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR

<details>
<summary> Successors and predecessors for LOAD_ATTR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">2,553,700</td>
<td align="right">59.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,504,380</td>
<td align="right">35.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">170,987</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">35,120</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">17,169</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">2,270,542</td>
<td align="right">52.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">941,049</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">297,679</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">218,287</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">148,019</td>
<td align="right">3.4%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_CONST

<details>
<summary> Successors and predecessors for LOAD_CONST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,555,311</td>
<td align="right">30.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,724,941</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">2,504,263</td>
<td align="right">13.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,328,119</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,158,235</td>
<td align="right">6.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,555,311</td>
<td align="right">30.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">2,626,048</td>
<td align="right">14.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,106,560</td>
<td align="right">11.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">2,075,080</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,881,845</td>
<td align="right">10.4%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_DEREF

<details>
<summary> Successors and predecessors for LOAD_DEREF </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">457,406</td>
<td align="right">81.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">51,680</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">51,680</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,020</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">840</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">458,346</td>
<td align="right">81.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">103,360</td>
<td align="right">18.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,060</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">740</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">680</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST

<details>
<summary> Successors and predecessors for LOAD_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">20,944,618</td>
<td align="right">25.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">8,620,787</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">6,450,504</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">5,180,558</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">5,118,539</td>
<td align="right">6.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">24,558,883</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">12,543,672</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">6,193,389</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">3,338,915</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,724,941</td>
<td align="right">3.3%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST_AND_CLEAR

<details>
<summary> Successors and predecessors for LOAD_FAST_AND_CLEAR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">GET_ITER</td>
<td align="right">123,234</td>
<td align="right">65.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">64,969</td>
<td align="right">34.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SWAP</td>
<td align="right">123,234</td>
<td align="right">65.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">64,969</td>
<td align="right">34.5%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST_CHECK

<details>
<summary> Successors and predecessors for LOAD_FAST_CHECK </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,041,880</td>
<td align="right">90.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">82,150</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">30,555</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">380</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">380</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">1,039,920</td>
<td align="right">90.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">82,070</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">30,515</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">1,880</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">380</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST_LOAD_FAST

<details>
<summary> Successors and predecessors for LOAD_FAST_LOAD_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">2,327,408</td>
<td align="right">19.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,397,172</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,378,716</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,127,869</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,120,180</td>
<td align="right">9.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">2,091,260</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,715,673</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,398,061</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,397,172</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">1,371,407</td>
<td align="right">11.6%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_GLOBAL

<details>
<summary> Successors and predecessors for LOAD_GLOBAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,020</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">2,860</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">2,456</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,320</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">2,240</td>
<td align="right">8.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">8,564</td>
<td align="right">33.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">6,027</td>
<td align="right">23.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">3,420</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,000</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,300</td>
<td align="right">5.1%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_NAME

<details>
<summary> Successors and predecessors for LOAD_NAME </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">1,700</td>
<td align="right">35.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,220</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">980</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">280</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">140</td>
<td align="right">2.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,420</td>
<td align="right">29.2%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">1,080</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">820</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">660</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">440</td>
<td align="right">9.1%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_SPECIAL

<details>
<summary> Successors and predecessors for LOAD_SPECIAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COPY</td>
<td align="right">2,627,533</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">2,627,533</td>
<td align="right">50.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SWAP</td>
<td align="right">2,627,533</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,426,254</td>
<td align="right">46.2%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">199,519</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,140</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">620</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_SUPER_ATTR

<details>
<summary> Successors and predecessors for LOAD_SUPER_ATTR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">560</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">220</td>
<td align="right">39.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">80</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">80</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">80</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">60</td>
<td align="right">10.7%</td>
</tr>
</tbody>
</table>


</details>

### MAKE_CELL

<details>
<summary> Successors and predecessors for MAKE_CELL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">206,740</td>
<td align="right">79.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">52,360</td>
<td align="right">20.1%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">960</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">206,740</td>
<td align="right">79.5%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">52,420</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">900</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>


</details>

### MAP_ADD

<details>
<summary> Successors and predecessors for MAP_ADD </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">20</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">20</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_FALSE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_FALSE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">3,244,123</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,234,878</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">2,177,720</td>
<td align="right">19.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">1,259,547</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">1,004,046</td>
<td align="right">9.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,687,409</td>
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,378,716</td>
<td align="right">12.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,328,119</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">1,258,870</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">763,174</td>
<td align="right">7.0%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_NONE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_NONE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,700,922</td>
<td align="right">92.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">119,180</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">21,660</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">1,060</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">680</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">NOP</td>
<td align="right">1,151,167</td>
<td align="right">62.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">385,491</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">200,174</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">42,060</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">32,560</td>
<td align="right">1.8%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_NOT_NONE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_NOT_NONE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,685,758</td>
<td align="right">79.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">522,506</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">103,360</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">50,052</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">20,678</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,591,138</td>
<td align="right">76.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">285,686</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">97,907</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">93,620</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">83,093</td>
<td align="right">2.5%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_TRUE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_TRUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,127,689</td>
<td align="right">44.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">1,099,402</td>
<td align="right">43.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">82,877</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">54,927</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">53,200</td>
<td align="right">2.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,127,869</td>
<td align="right">44.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">793,078</td>
<td align="right">31.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">315,581</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">91,832</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">69,324</td>
<td align="right">2.7%</td>
</tr>
</tbody>
</table>


</details>

### RAISE_VARARGS

<details>
<summary> Successors and predecessors for RAISE_VARARGS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">10,460</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">60</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COPY</td>
<td align="right">10,460</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### RERAISE

<details>
<summary> Successors and predecessors for RERAISE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">20,860</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">10,400</td>
<td align="right">33.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">10,460</td>
<td align="right">50.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">10,400</td>
<td align="right">49.9%</td>
</tr>
</tbody>
</table>


</details>

### RETURN_CONST

<details>
<summary> Successors and predecessors for RETURN_CONST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">2,435,812</td>
<td align="right">48.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">976,536</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">763,174</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">315,581</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">285,686</td>
<td align="right">5.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,616,975</td>
<td align="right">72.0%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">882,095</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">193,190</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">138,140</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">93,307</td>
<td align="right">1.9%</td>
</tr>
</tbody>
</table>


</details>

### SET_FUNCTION_ATTRIBUTE

<details>
<summary> Successors and predecessors for SET_FUNCTION_ATTRIBUTE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">74,860</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">72,680</td>
<td align="right">97.1%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">1,280</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">680</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">180</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">40</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### STORE_ATTR

<details>
<summary> Successors and predecessors for STORE_ATTR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">101,180</td>
<td align="right">63.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">31,200</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">24,520</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">1,900</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">620</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">82,800</td>
<td align="right">51.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">24,100</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">22,000</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">21,560</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">4,220</td>
<td align="right">2.6%</td>
</tr>
</tbody>
</table>


</details>

### STORE_DEREF

<details>
<summary> Successors and predecessors for STORE_DEREF </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">103,360</td>
<td align="right">39.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">103,360</td>
<td align="right">39.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">51,680</td>
<td align="right">19.9%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">900</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">180</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">103,280</td>
<td align="right">39.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">51,680</td>
<td align="right">19.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">51,680</td>
<td align="right">19.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">51,640</td>
<td align="right">19.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">860</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>


</details>

### STORE_FAST

<details>
<summary> Successors and predecessors for STORE_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">11,439,920</td>
<td align="right">36.0%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">5,146,560</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">2,700,156</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">2,064,800</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,160,413</td>
<td align="right">3.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">11,518,188</td>
<td align="right">36.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,620,787</td>
<td align="right">27.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">5,146,400</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">3,881,069</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,158,235</td>
<td align="right">3.6%</td>
</tr>
</tbody>
</table>


</details>

### STORE_FAST_LOAD_FAST

<details>
<summary> Successors and predecessors for STORE_FAST_LOAD_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">10,400,260</td>
<td align="right">89.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,212,040</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">21,440</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">6,160</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">10,400,000</td>
<td align="right">89.3%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,040,000</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">172,000</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">21,360</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">6,160</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### STORE_FAST_STORE_FAST

<details>
<summary> Successors and predecessors for STORE_FAST_STORE_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">2,234,958</td>
<td align="right">30.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,074,400</td>
<td align="right">28.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">2,064,740</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">1,024,020</td>
<td align="right">13.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">540</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,194,878</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,064,800</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,050,400</td>
<td align="right">14.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,040,500</td>
<td align="right">14.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">1,024,020</td>
<td align="right">13.8%</td>
</tr>
</tbody>
</table>


</details>

### STORE_GLOBAL

<details>
<summary> Successors and predecessors for STORE_GLOBAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">60</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">20</td>
<td align="right">25.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">40</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">40</td>
<td align="right">50.0%</td>
</tr>
</tbody>
</table>


</details>

### STORE_NAME

<details>
<summary> Successors and predecessors for STORE_NAME </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">4,560</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">3,520</td>
<td align="right">18.9%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">2,420</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,860</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">1,860</td>
<td align="right">10.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">9,920</td>
<td align="right">53.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,860</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">1,700</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,380</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">980</td>
<td align="right">5.3%</td>
</tr>
</tbody>
</table>


</details>

### SWAP

<details>
<summary> Successors and predecessors for SWAP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SWAP</td>
<td align="right">2,827,472</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">2,627,533</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">1,039,920</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">134,810</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">123,234</td>
<td align="right">1.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SWAP</td>
<td align="right">2,827,472</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">2,627,533</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,039,840</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">199,939</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">123,214</td>
<td align="right">1.7%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">340</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">280</td>
<td align="right">23.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">140</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">120</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">100</td>
<td align="right">8.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">540</td>
<td align="right">44.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">440</td>
<td align="right">36.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">100</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">60</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">40</td>
<td align="right">3.3%</td>
</tr>
</tbody>
</table>


</details>

### YIELD_VALUE

<details>
<summary> Successors and predecessors for YIELD_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">10,400,000</td>
<td align="right">83.3%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">2,080,300</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">11,439,920</td>
<td align="right">91.7%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">1,041,460</td>
<td align="right">8.3%</td>
</tr>
</tbody>
</table>


</details>

### RESUME

<details>
<summary> Successors and predecessors for RESUME </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL</td>
<td align="right">4,120</td>
<td align="right">49.5%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">2,240</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">900</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">400</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">220</td>
<td align="right">2.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,320</td>
<td align="right">39.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">2,240</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">980</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">760</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">380</td>
<td align="right">4.6%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_ADD_FLOAT

<details>
<summary> Successors and predecessors for BINARY_OP_ADD_FLOAT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">102,459</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">813</td>
<td align="right">0.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">102,497</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">775</td>
<td align="right">0.8%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_ADD_INT

<details>
<summary> Successors and predecessors for BINARY_OP_ADD_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,075,080</td>
<td align="right">98.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">31,440</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">200</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SWAP</td>
<td align="right">1,039,920</td>
<td align="right">49.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,023,980</td>
<td align="right">48.6%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">31,480</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">10,320</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">680</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_ADD_UNICODE

<details>
<summary> Successors and predecessors for BINARY_OP_ADD_UNICODE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">3,520</td>
<td align="right">69.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">680</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">300</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">280</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">280</td>
<td align="right">5.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,060</td>
<td align="right">40.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">1,760</td>
<td align="right">34.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">920</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">300</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">60</td>
<td align="right">1.2%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_MULTIPLY_FLOAT

<details>
<summary> Successors and predecessors for BINARY_OP_MULTIPLY_FLOAT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">171,920</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">171,920</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_SUBTRACT_FLOAT

<details>
<summary> Successors and predecessors for BINARY_OP_SUBTRACT_FLOAT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">82,070</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">80</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">80</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">82,230</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_SUBTRACT_INT

<details>
<summary> Successors and predecessors for BINARY_OP_SUBTRACT_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">172,648</td>
<td align="right">67.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">70,484</td>
<td align="right">27.7%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">10,920</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">240</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">242,052</td>
<td align="right">95.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">10,320</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,260</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">600</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_DICT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_DICT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">186,260</td>
<td align="right">88.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">22,640</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,420</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">186,660</td>
<td align="right">88.3%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">21,400</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,600</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">1,120</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">340</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_GETITEM

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_GETITEM </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">60</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">60</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_LIST_INT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_LIST_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">67,970</td>
<td align="right">76.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">21,320</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">120</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">68,010</td>
<td align="right">76.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">20,720</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">680</td>
<td align="right">0.8%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_STR_INT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_STR_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">171,920</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">171,960</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_TUPLE_INT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_TUPLE_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">110,860</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">60</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">99,180</td>
<td align="right">89.4%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">10,360</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,380</td>
<td align="right">1.2%</td>
</tr>
</tbody>
</table>


</details>

### CALL_ALLOC_AND_ENTER_INIT

<details>
<summary> Successors and predecessors for CALL_ALLOC_AND_ENTER_INIT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">61,960</td>
<td align="right">44.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">51,640</td>
<td align="right">37.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">21,920</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,240</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">880</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">137,840</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">300</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BOUND_METHOD_EXACT_ARGS

<details>
<summary> Successors and predecessors for CALL_BOUND_METHOD_EXACT_ARGS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">43,000</td>
<td align="right">48.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">17,680</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">16,680</td>
<td align="right">18.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">10,320</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">280</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">88,242</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BOUND_METHOD_GENERAL

<details>
<summary> Successors and predecessors for CALL_BOUND_METHOD_GENERAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">64,540</td>
<td align="right">52.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">47,720</td>
<td align="right">38.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">10,620</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">160</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">112,680</td>
<td align="right">91.6%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">10,360</td>
<td align="right">8.4%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BUILTIN_CLASS

<details>
<summary> Successors and predecessors for CALL_BUILTIN_CLASS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">1,023,960</td>
<td align="right">76.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">122,510</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">96,049</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">33,945</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">33,945</td>
<td align="right">2.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,088,789</td>
<td align="right">81.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">123,010</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">86,765</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">33,945</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">10,840</td>
<td align="right">0.8%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BUILTIN_FAST

<details>
<summary> Successors and predecessors for CALL_BUILTIN_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">409,650</td>
<td align="right">45.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">214,299</td>
<td align="right">23.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">114,968</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">64,060</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">46,684</td>
<td align="right">5.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">348,390</td>
<td align="right">38.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">309,257</td>
<td align="right">34.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">66,210</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">46,684</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">32,140</td>
<td align="right">3.6%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BUILTIN_FAST_WITH_KEYWORDS

<details>
<summary> Successors and predecessors for CALL_BUILTIN_FAST_WITH_KEYWORDS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,122,288</td>
<td align="right">50.2%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,023,960</td>
<td align="right">45.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">30,515</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">21,480</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">21,460</td>
<td align="right">1.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">2,091,340</td>
<td align="right">93.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">96,108</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">49,104</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BUILTIN_O

<details>
<summary> Successors and predecessors for CALL_BUILTIN_O </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">171,920</td>
<td align="right">79.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">43,580</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">140</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">171,920</td>
<td align="right">79.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">21,480</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">21,400</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">500</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">300</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### CALL_ISINSTANCE

<details>
<summary> Successors and predecessors for CALL_ISINSTANCE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">272,647</td>
<td align="right">99.6%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">420</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">340</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">220</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">273,407</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">220</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### CALL_KW_NON_PY

<details>
<summary> Successors and predecessors for CALL_KW_NON_PY </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">189,600</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">520</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">73,360</td>
<td align="right">38.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">51,920</td>
<td align="right">27.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">32,200</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">22,060</td>
<td align="right">11.6%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">10,220</td>
<td align="right">5.4%</td>
</tr>
</tbody>
</table>


</details>

### CALL_KW_PY

<details>
<summary> Successors and predecessors for CALL_KW_PY </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">110,685</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">200</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">110,885</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_LEN

<details>
<summary> Successors and predecessors for CALL_LEN </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">364,764</td>
<td align="right">86.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">54,380</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">560</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">210,548</td>
<td align="right">50.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">61,960</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">47,191</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">42,800</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">33,945</td>
<td align="right">8.1%</td>
</tr>
</tbody>
</table>


</details>

### CALL_LIST_APPEND

<details>
<summary> Successors and predecessors for CALL_LIST_APPEND </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">64,869</td>
<td align="right">73.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">21,960</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">500</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">500</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">380</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">64,909</td>
<td align="right">73.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">20,720</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,240</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">880</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">500</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>


</details>

### CALL_METHOD_DESCRIPTOR_FAST

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,012,294</td>
<td align="right">72.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">366,946</td>
<td align="right">26.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">7,660</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,060</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">880</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,160,413</td>
<td align="right">83.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">219,287</td>
<td align="right">15.8%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">6,160</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">1,080</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">760</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">114,740</td>
<td align="right">91.5%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">10,320</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">220</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">120</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">61,620</td>
<td align="right">49.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">42,960</td>
<td align="right">34.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20,760</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_METHOD_DESCRIPTOR_NOARGS

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_NOARGS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,538,864</td>
<td align="right">95.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">77,199</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">620</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">580</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">560</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,040,920</td>
<td align="right">64.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">286,547</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">92,630</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">48,740</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">46,684</td>
<td align="right">2.9%</td>
</tr>
</tbody>
</table>


</details>

### CALL_METHOD_DESCRIPTOR_O

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_O </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,324,815</td>
<td align="right">88.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">100,620</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">52,240</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">21,420</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,740</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,377,795</td>
<td align="right">91.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">100,560</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">24,200</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">680</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_NON_PY_GENERAL

<details>
<summary> Successors and predecessors for CALL_NON_PY_GENERAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">2,861,590</td>
<td align="right">31.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,433,212</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,371,407</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">828,282</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">418,999</td>
<td align="right">4.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,700,156</td>
<td align="right">29.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">2,470,787</td>
<td align="right">27.3%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">1,050,320</td>
<td align="right">11.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">945,329</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">795,330</td>
<td align="right">8.8%</td>
</tr>
</tbody>
</table>


</details>

### CALL_PY_EXACT_ARGS

<details>
<summary> Successors and predecessors for CALL_PY_EXACT_ARGS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">2,426,254</td>
<td align="right">32.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,764,067</td>
<td align="right">23.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,333,039</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,139,345</td>
<td align="right">15.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">220,434</td>
<td align="right">2.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">7,467,471</td>
<td align="right">98.9%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">52,360</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">31,420</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">980</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_PY_GENERAL

<details>
<summary> Successors and predecessors for CALL_PY_GENERAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,626,048</td>
<td align="right">77.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">280,356</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">218,287</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">115,269</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">89,622</td>
<td align="right">2.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">3,190,903</td>
<td align="right">93.6%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">218,747</td>
<td align="right">6.4%</td>
</tr>
</tbody>
</table>


</details>

### CALL_STR_1

<details>
<summary> Successors and predecessors for CALL_STR_1 </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">21,740</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">40</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20,460</td>
<td align="right">93.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">680</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">340</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">300</td>
<td align="right">1.4%</td>
</tr>
</tbody>
</table>


</details>

### CALL_TUPLE_1

<details>
<summary> Successors and predecessors for CALL_TUPLE_1 </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">1,050,320</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,050,380</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_TYPE_1

<details>
<summary> Successors and predecessors for CALL_TYPE_1 </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">460</td>
<td align="right">44.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">360</td>
<td align="right">34.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">120</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">60</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">40</td>
<td align="right">3.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">580</td>
<td align="right">55.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">300</td>
<td align="right">28.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">80</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">40</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">40</td>
<td align="right">3.8%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP_FLOAT

<details>
<summary> Successors and predecessors for COMPARE_OP_FLOAT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">500</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">500</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP_INT

<details>
<summary> Successors and predecessors for COMPARE_OP_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,078,024</td>
<td align="right">32.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,044,620</td>
<td align="right">31.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">989,074</td>
<td align="right">30.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">48,225</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">42,800</td>
<td align="right">1.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">3,244,123</td>
<td align="right">98.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">45,363</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">628</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">340</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP_STR

<details>
<summary> Successors and predecessors for COMPARE_OP_STR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,165,505</td>
<td align="right">95.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">98,740</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">10,660</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">422</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">2,177,720</td>
<td align="right">95.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">54,927</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">21,400</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">21,400</td>
<td align="right">0.9%</td>
</tr>
</tbody>
</table>


</details>

### CONTAINS_OP_DICT

<details>
<summary> Successors and predecessors for CONTAINS_OP_DICT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,258,207</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">1,760</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,259,547</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">500</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">380</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CONTAINS_OP_SET

<details>
<summary> Successors and predecessors for CONTAINS_OP_SET </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,760</td>
<td align="right">72.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">640</td>
<td align="right">26.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">20</td>
<td align="right">0.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,920</td>
<td align="right">79.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">500</td>
<td align="right">20.7%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER_GEN

<details>
<summary> Successors and predecessors for FOR_ITER_GEN </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">11,439,920</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">20,720</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">11,439,920</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">20,720</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER_LIST

<details>
<summary> Successors and predecessors for FOR_ITER_LIST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">10,841,215</td>
<td align="right">88.2%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,346,418</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">98,894</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">10,400,260</td>
<td align="right">84.6%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,040,000</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">310,437</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">294,318</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">131,738</td>
<td align="right">1.1%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER_RANGE

<details>
<summary> Successors and predecessors for FOR_ITER_RANGE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">119,597</td>
<td align="right">61.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">76,167</td>
<td align="right">38.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">200</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">141,139</td>
<td align="right">72.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">34,185</td>
<td align="right">17.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">20,640</td>
<td align="right">10.5%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER_TUPLE

<details>
<summary> Successors and predecessors for FOR_ITER_TUPLE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">28,980</td>
<td align="right">53.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">21,600</td>
<td align="right">40.2%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">2,740</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">300</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">120</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">22,660</td>
<td align="right">42.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">21,260</td>
<td align="right">39.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">6,160</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">2,740</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">640</td>
<td align="right">1.2%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_CLASS

<details>
<summary> Successors and predecessors for LOAD_ATTR_CLASS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">99,564</td>
<td align="right">70.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">41,180</td>
<td align="right">29.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">540</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">240</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">42,800</td>
<td align="right">30.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">37,049</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">31,000</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">30,555</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">120</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_CLASS_WITH_METACLASS_CHECK

<details>
<summary> Successors and predecessors for LOAD_ATTR_CLASS_WITH_METACLASS_CHECK </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">240</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">80</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">80</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">80</td>
<td align="right">33.3%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_INSTANCE_VALUE

<details>
<summary> Successors and predecessors for LOAD_ATTR_INSTANCE_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">24,558,883</td>
<td align="right">90.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,398,061</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">1,039,840</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">45,548</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">21,360</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">6,577,717</td>
<td align="right">24.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,180,558</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">2,553,700</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,311,538</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,218,368</td>
<td align="right">8.2%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_METHOD_LAZY_DICT

<details>
<summary> Successors and predecessors for LOAD_ATTR_METHOD_LAZY_DICT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">235,436</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">220</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">93,788</td>
<td align="right">39.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">77,199</td>
<td align="right">32.8%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">64,169</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">340</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">160</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_METHOD_NO_DICT

<details>
<summary> Successors and predecessors for LOAD_ATTR_METHOD_NO_DICT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">6,577,717</td>
<td align="right">90.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">457,325</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">65,180</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">48,400</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">48,400</td>
<td align="right">0.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,750,947</td>
<td align="right">37.8%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">2,433,212</td>
<td align="right">33.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,538,864</td>
<td align="right">21.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">376,870</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">107,749</td>
<td align="right">1.5%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_METHOD_WITH_VALUES

<details>
<summary> Successors and predecessors for LOAD_ATTR_METHOD_WITH_VALUES </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,364,102</td>
<td align="right">54.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">1,039,920</td>
<td align="right">24.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">581,579</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">218,287</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">52,460</td>
<td align="right">1.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">1,764,067</td>
<td align="right">40.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,120,180</td>
<td align="right">25.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">963,371</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">280,356</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">120,884</td>
<td align="right">2.8%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_MODULE

<details>
<summary> Successors and predecessors for LOAD_ATTR_MODULE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,748,100</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">4,042</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,600</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">600</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">2,193,040</td>
<td align="right">79.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">218,287</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">103,360</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">58,240</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">57,420</td>
<td align="right">2.1%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES

<details>
<summary> Successors and predecessors for LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">378,787</td>
<td align="right">74.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">129,738</td>
<td align="right">25.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">400</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">300</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">218,327</td>
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">129,818</td>
<td align="right">25.5%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">48,400</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">48,400</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">21,720</td>
<td align="right">4.3%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_PROPERTY

<details>
<summary> Successors and predecessors for LOAD_ATTR_PROPERTY </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">212,485</td>
<td align="right">79.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">51,900</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,240</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">460</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">340</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">241,925</td>
<td align="right">90.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">24,320</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">460</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_SLOT

<details>
<summary> Successors and predecessors for LOAD_ATTR_SLOT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">72,040</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">3,700</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">500</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">260</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">48,400</td>
<td align="right">63.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">21,860</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,020</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,840</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">560</td>
<td align="right">0.7%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_GLOBAL_BUILTIN

<details>
<summary> Successors and predecessors for LOAD_GLOBAL_BUILTIN </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,812,633</td>
<td align="right">32.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">1,173,330</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,092,470</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">411,772</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">379,367</td>
<td align="right">6.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,397,340</td>
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,235,268</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,092,470</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">457,406</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">272,647</td>
<td align="right">4.9%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_GLOBAL_MODULE

<details>
<summary> Successors and predecessors for LOAD_GLOBAL_MODULE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">2,218,368</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,460,053</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,235,268</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,233,376</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">636,302</td>
<td align="right">6.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">2,748,100</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">2,165,505</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">975,083</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">828,282</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">719,890</td>
<td align="right">7.1%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_SUPER_ATTR_ATTR

<details>
<summary> Successors and predecessors for LOAD_SUPER_ATTR_ATTR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">58,800</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">80</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">58,880</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_SUPER_ATTR_METHOD

<details>
<summary> Successors and predecessors for LOAD_SUPER_ATTR_METHOD </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">398,306</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">220</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">240,727</td>
<td align="right">60.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">147,019</td>
<td align="right">36.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">10,740</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### RESUME_CHECK

<details>
<summary> Successors and predecessors for RESUME_CHECK </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CACHE</td>
<td align="right">13,470,496</td>
<td align="right">35.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">11,439,920</td>
<td align="right">30.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">7,467,471</td>
<td align="right">19.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">3,190,903</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">1,087,200</td>
<td align="right">2.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20,944,618</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">12,481,200</td>
<td align="right">32.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,812,633</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,460,053</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">700,027</td>
<td align="right">1.8%</td>
</tr>
</tbody>
</table>


</details>

### STORE_ATTR_INSTANCE_VALUE

<details>
<summary> Successors and predecessors for STORE_ATTR_INSTANCE_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,245,376</td>
<td align="right">55.8%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,039,840</td>
<td align="right">25.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">674,179</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">30,960</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">21,360</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,011,834</td>
<td align="right">25.2%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">976,536</td>
<td align="right">24.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">640,966</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">603,979</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">253,060</td>
<td align="right">6.3%</td>
</tr>
</tbody>
</table>


</details>

### STORE_ATTR_SLOT

<details>
<summary> Successors and predecessors for STORE_ATTR_SLOT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">49,300</td>
<td align="right">69.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">21,860</td>
<td align="right">30.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">140</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">70,660</td>
<td align="right">99.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">320</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">320</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SUBSCR_DICT

<details>
<summary> Successors and predecessors for STORE_SUBSCR_DICT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,085,814</td>
<td align="right">77.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">218,287</td>
<td align="right">15.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">84,700</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">20,440</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">580</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,230,981</td>
<td align="right">87.3%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">74,300</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">52,600</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">51,640</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">500</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_ALWAYS_TRUE

<details>
<summary> Successors and predecessors for TO_BOOL_ALWAYS_TRUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">120</td>
<td align="right">53.8%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">63</td>
<td align="right">28.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">40</td>
<td align="right">17.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">140</td>
<td align="right">62.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">83</td>
<td align="right">37.2%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_BOOL

<details>
<summary> Successors and predecessors for TO_BOOL_BOOL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,258,844</td>
<td align="right">36.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">634,701</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">348,390</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">330,274</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">273,407</td>
<td align="right">8.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">2,234,878</td>
<td align="right">65.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,099,402</td>
<td align="right">32.1%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">95,638</td>
<td align="right">2.8%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_INT

<details>
<summary> Successors and predecessors for TO_BOOL_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COPY</td>
<td align="right">566,312</td>
<td align="right">56.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">218,627</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">218,547</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">500</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">500</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,004,046</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">780</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_LIST

<details>
<summary> Successors and predecessors for TO_BOOL_LIST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">168,159</td>
<td align="right">77.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">48,225</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">500</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">140</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">168,279</td>
<td align="right">77.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">48,805</td>
<td align="right">22.5%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_NONE

<details>
<summary> Successors and predecessors for TO_BOOL_NONE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">364,741</td>
<td align="right">77.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">53,280</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">42,700</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">10,320</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">380</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">418,501</td>
<td align="right">88.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">53,200</td>
<td align="right">11.3%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_STR

<details>
<summary> Successors and predecessors for TO_BOOL_STR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">6,160</td>
<td align="right">67.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,280</td>
<td align="right">24.8%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">560</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">120</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">60</td>
<td align="right">0.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">7,140</td>
<td align="right">77.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">2,040</td>
<td align="right">22.2%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE_TUPLE

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE_TUPLE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,064,000</td>
<td align="right">97.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">46,684</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">100</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">2,064,740</td>
<td align="right">97.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">46,724</td>
<td align="right">2.2%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE_TWO_TUPLE

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE_TWO_TUPLE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,050,660</td>
<td align="right">46.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">1,039,920</td>
<td align="right">46.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">131,738</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">11,720</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">11,200</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">2,234,958</td>
<td align="right">99.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">10,980</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>


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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">1,529,507</td>
<td align="right">35.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,733,795</td>
<td align="right">63.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">41,479</td>
<td align="right">1.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">1,453</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">7,494</td>
<td align="right">83.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">add different types</td>
<td align="right">2,832</td>
<td align="right">37.8%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">2,440</td>
<td align="right">32.6%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">1,229</td>
<td align="right">16.4%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">793</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">200</td>
<td align="right">2.7%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">32,880</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR

<details>
<summary> specialization stats for BINARY_SUBSCR family </summary>

<table>
<thead>
<tr>
<th align="left">Kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">1,111,404</td>
<td align="right">65.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">583,810</td>
<td align="right">34.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">300</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">905</td>
<td align="right">75.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">buffer int</td>
<td align="right">885</td>
<td align="right">97.8%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">20</td>
<td align="right">2.2%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">19,266</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">19,046,275</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">5,580</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">16,750</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">820</td>
<td align="right">53.2%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">175,687</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,532,145</td>
<td align="right">96.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">34,696</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">2,390</td>
<td align="right">59.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,624</td>
<td align="right">40.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">float long</td>
<td align="right">1,011</td>
<td align="right">62.3%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">340</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">273</td>
<td align="right">16.8%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,262,847</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">140</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">2,318,060</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">23,997,451</td>
<td align="right">91.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">720</td>
<td align="right">26.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">2,000</td>
<td align="right">73.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">other</td>
<td align="right">600</td>
<td align="right">30.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">600</td>
<td align="right">30.0%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">380</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">240</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">140</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">40</td>
<td align="right">2.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">4,258,890</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">41,750,931</td>
<td align="right">88.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">908,017</td>
<td align="right">1.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">36,521</td>
<td align="right">72.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">14,157</td>
<td align="right">27.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">method</td>
<td align="right">4,578</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">2,829</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">2,452</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">1,440</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">660</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">260</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">120</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">80</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">60</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">40</td>
<td align="right">0.3%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">13,574</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">800</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">15,652,150</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">28,840</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">12,084</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">260</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">457,406</td>
<td align="right">99.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">300</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">153,920</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,749,555</td>
<td align="right">88.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">344,120</td>
<td align="right">8.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">10,800</td>
<td align="right">85.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,900</td>
<td align="right">15.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">property</td>
<td align="right">1,080</td>
<td align="right">56.8%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">520</td>
<td align="right">27.4%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">200</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">100</td>
<td align="right">5.3%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">52,720</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,410,121</td>
<td align="right">96.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">300</td>
<td align="right">31.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">640</td>
<td align="right">68.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">py simple</td>
<td align="right">440</td>
<td align="right">68.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">200</td>
<td align="right">31.2%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">1,321,011</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,131,829</td>
<td align="right">79.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">880</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">3,026</td>
<td align="right">55.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">2,421</td>
<td align="right">44.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">mapping</td>
<td align="right">971</td>
<td align="right">40.1%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">800</td>
<td align="right">33.0%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">370</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">200</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">80</td>
<td align="right">3.3%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,357,582</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">540</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">357,483,122</td>
<td align="right">65.4%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">11,080,496</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">176,352,160</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,363,612</td>
<td align="right">0.2%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">4,258,890</td>
<td align="right">38.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">2,318,060</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,529,507</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,321,011</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">1,111,404</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">175,687</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">153,920</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">52,720</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">32,880</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">19,266</td>
<td align="right">0.2%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">753,583</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">344,120</td>
<td align="right">25.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">124,314</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">41,479</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">34,636</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">24,780</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">18,180</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">10,660</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">5,100</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,140</td>
<td align="right">0.2%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">13,724,855</td>
<td align="right">36.2%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">24,220,839</td>
<td align="right">63.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">13,724,855</td>
<td align="right">36.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">12,671,735</td>
<td align="right">33.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">1,053,120</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">460</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">12,670,295</td>
<td align="right">33.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">980</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">1,124,220</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">1,087,540</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">403,210</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">50,824</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">25,569,994</td>
<td align="right">67.4%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">17,639,602</td>
<td align="right">41.9%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">17,650,613</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">24,432,520</td>
<td align="right">58.1%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">24,176,032</td>
<td align="right">57.5%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">148,296</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">108,192</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">24,787,000</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">652,118</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">205,039,811</td>
<td align="right">52.5%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">221,644,633</td>
<td align="right">50.3%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">55,745,061</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">78,253,340</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">89,876,924</td>
<td align="right">23.0%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">93,590,046</td>
<td align="right">21.3%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">40,253,308</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">46,791,483</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">1,600</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (str subclass)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">4,864,166</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">91,350</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">132,009</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">13,524,692</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">46,131</td>
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
<th align="right">Collections</th>
<th align="right">Objects collected</th>
<th align="right">Object visits</th>
</tr>
</thead>
<tbody>
<tr>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
</tr>
<tr>
<td align="right">1</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
</tr>
<tr>
<td align="right">2</td>
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
<th align="right">Count</th>
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
<td align="right">0</td>
</tr>
<tr>
<td align="left">
set bases
<details>
<summary>ⓘ</summary>

Setting the bases of a class, `cls.__bases__ = ...`
</details>
</td>
<td align="right">0</td>
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
</tr>
<tr>
<td align="left">
func modification
<details>
<summary>ⓘ</summary>

Modifying a function, e.g. `func.__defaults__ = ...`, etc.
</details>
</td>
<td align="right">0</td>
</tr>
<tr>
<td align="left">
watched dict modification
<details>
<summary>ⓘ</summary>

A watched dict has been modified
</details>
</td>
<td align="right">0</td>
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
<th align="right">Count</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Number of data files</td>
<td align="right">40</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-10-18
