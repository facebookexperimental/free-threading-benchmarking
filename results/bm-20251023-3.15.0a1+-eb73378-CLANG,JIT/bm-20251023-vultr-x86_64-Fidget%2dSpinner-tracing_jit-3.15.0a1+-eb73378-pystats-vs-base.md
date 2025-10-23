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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">743,835,475</td>
<td align="right">1,598,262,611</td>
<td align="right">114.9%</td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">1,684,562</td>
<td align="right">140,421</td>
<td align="right">-91.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">1,375,133,736</td>
<td align="right">126,071,935</td>
<td align="right">-90.8%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,156,329</td>
<td align="right">794,769</td>
<td align="right">-87.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">62,088,880</td>
<td align="right">8,062,985</td>
<td align="right">-87.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">345,643,030</td>
<td align="right">46,719,186</td>
<td align="right">-86.5%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">56,950,334</td>
<td align="right">8,528,689</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">166,050,468</td>
<td align="right">24,901,852</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">249,679,501</td>
<td align="right">43,112,075</td>
<td align="right">-82.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">7,195,406</td>
<td align="right">1,366,477</td>
<td align="right">-81.0%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">9,835,718</td>
<td align="right">1,870,863</td>
<td align="right">-81.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">131,380,678</td>
<td align="right">26,078,973</td>
<td align="right">-80.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">205,200,984</td>
<td align="right">49,743,177</td>
<td align="right">-75.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">97,599,025</td>
<td align="right">24,997,397</td>
<td align="right">-74.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">783,900,012</td>
<td align="right">221,879,697</td>
<td align="right">-71.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">241,728,999</td>
<td align="right">71,365,972</td>
<td align="right">-70.5%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">28,457,520</td>
<td align="right">8,753,939</td>
<td align="right">-69.2%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">139,585,140</td>
<td align="right">43,446,273</td>
<td align="right">-68.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">310,183,357</td>
<td align="right">99,060,095</td>
<td align="right">-68.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">2,075,188</td>
<td align="right">680,158</td>
<td align="right">-67.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">49,565,203</td>
<td align="right">16,272,126</td>
<td align="right">-67.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">320,353,821</td>
<td align="right">105,689,496</td>
<td align="right">-67.0%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">26,549,503</td>
<td align="right">8,933,074</td>
<td align="right">-66.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">274,336,366</td>
<td align="right">94,299,090</td>
<td align="right">-65.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">542,129,112</td>
<td align="right">192,288,685</td>
<td align="right">-64.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">1,214,813</td>
<td align="right">463,757</td>
<td align="right">-61.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">572,172,153</td>
<td align="right">219,353,061</td>
<td align="right">-61.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">279,400,372</td>
<td align="right">107,381,744</td>
<td align="right">-61.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">158,452,444</td>
<td align="right">61,901,768</td>
<td align="right">-60.9%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">64,813,565</td>
<td align="right">25,438,599</td>
<td align="right">-60.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">171,642,397</td>
<td align="right">69,544,409</td>
<td align="right">-59.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">165,455,820</td>
<td align="right">68,412,087</td>
<td align="right">-58.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,351,083,127</td>
<td align="right">582,071,873</td>
<td align="right">-56.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,076,668,454</td>
<td align="right">470,113,472</td>
<td align="right">-56.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">194,807,939</td>
<td align="right">88,222,648</td>
<td align="right">-54.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">813,045,624</td>
<td align="right">372,060,639</td>
<td align="right">-54.2%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">55,173,575</td>
<td align="right">25,607,715</td>
<td align="right">-53.6%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">314,729,422</td>
<td align="right">149,620,124</td>
<td align="right">-52.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,879,198,216</td>
<td align="right">2,326,856,380</td>
<td align="right">-52.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">319,160,890</td>
<td align="right">153,831,758</td>
<td align="right">-51.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">6,445,645,037</td>
<td align="right">3,136,852,100</td>
<td align="right">-51.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">474,334,890</td>
<td align="right">233,298,794</td>
<td align="right">-50.8%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">343,606,451</td>
<td align="right">169,080,408</td>
<td align="right">-50.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">566,651,057</td>
<td align="right">280,331,323</td>
<td align="right">-50.5%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">9,738,721</td>
<td align="right">4,862,941</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,160,388,079</td>
<td align="right">1,082,819,793</td>
<td align="right">-49.9%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">467,639,341</td>
<td align="right">236,112,843</td>
<td align="right">-49.5%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">102,915,241</td>
<td align="right">52,321,365</td>
<td align="right">-49.2%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">331,727,692</td>
<td align="right">172,162,072</td>
<td align="right">-48.1%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">1,062,193,345</td>
<td align="right">564,885,671</td>
<td align="right">-46.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">1,138,258,061</td>
<td align="right">608,561,408</td>
<td align="right">-46.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">43,852,378</td>
<td align="right">23,474,430</td>
<td align="right">-46.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">98,631,029</td>
<td align="right">52,810,199</td>
<td align="right">-46.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">495,978,463</td>
<td align="right">266,914,807</td>
<td align="right">-46.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">371,559,805</td>
<td align="right">202,824,076</td>
<td align="right">-45.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">4,805,967,834</td>
<td align="right">2,628,546,030</td>
<td align="right">-45.3%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">110,723,948</td>
<td align="right">60,684,174</td>
<td align="right">-45.2%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">201,330,139</td>
<td align="right">110,727,411</td>
<td align="right">-45.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">601,350,856</td>
<td align="right">333,696,892</td>
<td align="right">-44.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,937,162,502</td>
<td align="right">1,630,527,459</td>
<td align="right">-44.5%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">106,680,513</td>
<td align="right">60,399,315</td>
<td align="right">-43.4%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">1,232,574</td>
<td align="right">700,470</td>
<td align="right">-43.2%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">659,304,925</td>
<td align="right">375,990,288</td>
<td align="right">-43.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,441,114,305</td>
<td align="right">1,972,761,042</td>
<td align="right">-42.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">137,555,096</td>
<td align="right">79,685,524</td>
<td align="right">-42.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">326,076,973</td>
<td align="right">189,315,120</td>
<td align="right">-41.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,878,233,483</td>
<td align="right">3,421,606,207</td>
<td align="right">-41.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">24,754,061,638</td>
<td align="right">14,526,411,192</td>
<td align="right">-41.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">294,469,942</td>
<td align="right">173,243,741</td>
<td align="right">-41.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">145,103,532</td>
<td align="right">86,172,997</td>
<td align="right">-40.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">204,789,272</td>
<td align="right">122,165,592</td>
<td align="right">-40.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">166,356,574</td>
<td align="right">99,906,203</td>
<td align="right">-39.9%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">875,188,307</td>
<td align="right">526,719,635</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">2,876,167,485</td>
<td align="right">1,731,895,552</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">994,029,135</td>
<td align="right">607,235,981</td>
<td align="right">-38.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">131,623,204</td>
<td align="right">80,821,986</td>
<td align="right">-38.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,634,533,262</td>
<td align="right">1,011,543,007</td>
<td align="right">-38.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,492,621,426</td>
<td align="right">2,172,477,388</td>
<td align="right">-37.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">150,014,195</td>
<td align="right">94,875,954</td>
<td align="right">-36.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">811,076,536</td>
<td align="right">517,126,003</td>
<td align="right">-36.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">294,213,956</td>
<td align="right">188,208,435</td>
<td align="right">-36.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">142,717,993</td>
<td align="right">92,312,194</td>
<td align="right">-35.3%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">71,757,010</td>
<td align="right">46,992,365</td>
<td align="right">-34.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,440,129,677</td>
<td align="right">950,065,263</td>
<td align="right">-34.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">577,961,397</td>
<td align="right">384,781,704</td>
<td align="right">-33.4%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">141,188,969</td>
<td align="right">94,136,760</td>
<td align="right">-33.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">6,124,629,450</td>
<td align="right">4,112,535,721</td>
<td align="right">-32.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,159,370,695</td>
<td align="right">784,058,287</td>
<td align="right">-32.4%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">70,690,423</td>
<td align="right">47,947,777</td>
<td align="right">-32.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">50,573,003</td>
<td align="right">34,433,836</td>
<td align="right">-31.9%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">114,997,437</td>
<td align="right">78,549,716</td>
<td align="right">-31.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,109,550,598</td>
<td align="right">2,127,573,469</td>
<td align="right">-31.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">485,760,040</td>
<td align="right">334,047,666</td>
<td align="right">-31.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">172,411,400</td>
<td align="right">119,592,701</td>
<td align="right">-30.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">4,965,616,609</td>
<td align="right">3,444,826,766</td>
<td align="right">-30.6%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,574,894,355</td>
<td align="right">4,569,861,241</td>
<td align="right">-30.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">373,628,804</td>
<td align="right">260,244,123</td>
<td align="right">-30.3%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">442,902,429</td>
<td align="right">309,132,998</td>
<td align="right">-30.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">315,189,478</td>
<td align="right">220,652,894</td>
<td align="right">-30.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">525,396,381</td>
<td align="right">368,396,557</td>
<td align="right">-29.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">3,974,049</td>
<td align="right">2,798,811</td>
<td align="right">-29.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">96,006,319</td>
<td align="right">124,373,731</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">205,967,469</td>
<td align="right">146,400,430</td>
<td align="right">-28.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">70,070,213</td>
<td align="right">50,241,927</td>
<td align="right">-28.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">3,167,792,857</td>
<td align="right">2,273,223,292</td>
<td align="right">-28.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">611,397,968</td>
<td align="right">439,646,639</td>
<td align="right">-28.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">249,354,279</td>
<td align="right">181,534,949</td>
<td align="right">-27.2%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">1,001,864,365</td>
<td align="right">754,069,285</td>
<td align="right">-24.7%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">17,502,878</td>
<td align="right">13,208,742</td>
<td align="right">-24.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">509,446,612</td>
<td align="right">384,922,282</td>
<td align="right">-24.4%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">54,367,312</td>
<td align="right">67,081,179</td>
<td align="right">23.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">331,904,936</td>
<td align="right">257,302,334</td>
<td align="right">-22.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">40,585,194</td>
<td align="right">31,862,352</td>
<td align="right">-21.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">180,863,719</td>
<td align="right">142,357,278</td>
<td align="right">-21.3%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">41,073,053</td>
<td align="right">32,548,469</td>
<td align="right">-20.8%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">553,334,664</td>
<td align="right">441,751,511</td>
<td align="right">-20.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">15,587,989</td>
<td align="right">12,536,642</td>
<td align="right">-19.6%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">369,301,369</td>
<td align="right">298,294,908</td>
<td align="right">-19.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">8,560,191</td>
<td align="right">6,995,403</td>
<td align="right">-18.3%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">196,697,499</td>
<td align="right">162,725,700</td>
<td align="right">-17.3%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">323,949,428</td>
<td align="right">268,979,493</td>
<td align="right">-17.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">326,002,332</td>
<td align="right">270,856,784</td>
<td align="right">-16.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">59,731,767</td>
<td align="right">49,743,829</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">158,660,697</td>
<td align="right">132,787,743</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">114,562,392</td>
<td align="right">96,316,197</td>
<td align="right">-15.9%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">42,461,499</td>
<td align="right">35,752,991</td>
<td align="right">-15.8%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">61,108,541</td>
<td align="right">51,565,358</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">93,053,504</td>
<td align="right">79,753,054</td>
<td align="right">-14.3%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">6,269,391</td>
<td align="right">5,393,629</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">3,023,920,687</td>
<td align="right">2,654,135,749</td>
<td align="right">-12.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">70,937,747</td>
<td align="right">62,284,888</td>
<td align="right">-12.2%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,151,193,047</td>
<td align="right">1,024,373,324</td>
<td align="right">-11.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">46,434,172</td>
<td align="right">41,600,346</td>
<td align="right">-10.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,544,930,996</td>
<td align="right">1,406,047,149</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">367,101,558</td>
<td align="right">338,830,538</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">10,389,147</td>
<td align="right">9,620,614</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">122,065,495</td>
<td align="right">113,094,554</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">418,752,741</td>
<td align="right">390,442,352</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">3,423,912</td>
<td align="right">3,198,277</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">630,088,168</td>
<td align="right">669,231,904</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">12,123,980</td>
<td align="right">11,397,728</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">235,809</td>
<td align="right">222,353</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">71,547,633</td>
<td align="right">67,478,459</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">593,230,363</td>
<td align="right">559,677,514</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">70,255,285</td>
<td align="right">73,708,597</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">35,435,795</td>
<td align="right">33,750,206</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">143,959,103</td>
<td align="right">137,925,167</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">36,897,410</td>
<td align="right">35,399,842</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">43,316,829</td>
<td align="right">41,891,967</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">22,179,370</td>
<td align="right">21,473,025</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">172,683,388</td>
<td align="right">167,281,630</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">6,775,330</td>
<td align="right">6,590,497</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">302,140,427</td>
<td align="right">294,941,984</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">297,141,912</td>
<td align="right">290,100,969</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">1,890,272,073</td>
<td align="right">1,877,258,578</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">11,666</td>
<td align="right">11,728</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">219,562,308</td>
<td align="right">218,674,065</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">4,510,099</td>
<td align="right">4,492,301</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">222,251</td>
<td align="right">222,781</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">25,553,813</td>
<td align="right">25,522,892</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">6,520</td>
<td align="right">6,525</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">31,203</td>
<td align="right">31,180</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">437,239</td>
<td align="right">437,368</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,440,667</td>
<td align="right">128,462,069</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">91,596</td>
<td align="right">91,588</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">8,975,993</td>
<td align="right">8,975,373</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">331,596</td>
<td align="right">331,577</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">14,736,780</td>
<td align="right">14,737,430</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">9,211,860</td>
<td align="right">9,211,958</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">25,211,120</td>
<td align="right">25,210,920</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">25,553,815</td>
<td align="right">25,553,615</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">8,594,614</td>
<td align="right">8,594,656</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">6,248,578</td>
<td align="right">6,248,570</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_LINE</td>
<td align="right">58,270,440</td>
<td align="right">58,270,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">41,964,183</td>
<td align="right">41,964,183</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RESUME</td>
<td align="right">29,134,740</td>
<td align="right">29,134,740</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_RETURN_VALUE</td>
<td align="right">29,134,440</td>
<td align="right">29,134,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AITER</td>
<td align="right">6,000,000</td>
<td align="right">6,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">6,000,000</td>
<td align="right">6,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_ASYNC_FOR</td>
<td align="right">6,000,000</td>
<td align="right">6,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">73,592</td>
<td align="right">73,592</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">68,063</td>
<td align="right">68,063</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">49,580</td>
<td align="right">49,580</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">47,906</td>
<td align="right">47,906</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">14,747</td>
<td align="right">14,747</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">9,631</td>
<td align="right">9,631</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">3,375</td>
<td align="right">3,375</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">3,352</td>
<td align="right">3,352</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">2,740</td>
<td align="right">2,740</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">2,347</td>
<td align="right">2,347</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FROM_DICT_OR_DEREF</td>
<td align="right">1,460</td>
<td align="right">1,460</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">120</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SETUP_ANNOTATIONS</td>
<td align="right">117</td>
<td align="right">117</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">15</td>
<td align="right">15</td>
<td align="right">0.0%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,350,514,188</td>
<td align="right">7.5%</td>
<td align="right">581,712,214</td>
<td align="right">3.4%</td>
<td align="right">-56.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">61,043,817</td>
<td align="right">0.3%</td>
<td align="right">40,363,149</td>
<td align="right">0.2%</td>
<td align="right">-33.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">16,712,947,143</td>
<td align="right">92.2%</td>
<td align="right">16,580,749,816</td>
<td align="right">96.4%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">1,063</td>
<td align="right">0.0%</td>
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
<td align="right">552,378</td>
<td align="right">32.1%</td>
<td align="right">343,058</td>
<td align="right">30.6%</td>
<td align="right">-37.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,168,031</td>
<td align="right">67.9%</td>
<td align="right">778,392</td>
<td align="right">69.4%</td>
<td align="right">-33.4%</td>
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
<td align="left">and other</td>
<td align="right">317</td>
<td align="right">0.1%</td>
<td align="right">1,077</td>
<td align="right">0.3%</td>
<td align="right">239.7%</td>
</tr>
<tr>
<td align="left">subscr bytes</td>
<td align="right">1,808</td>
<td align="right">0.3%</td>
<td align="right">4,448</td>
<td align="right">1.3%</td>
<td align="right">146.0%</td>
</tr>
<tr>
<td align="left">subscr mappingproxy</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">140</td>
<td align="right">0.0%</td>
<td align="right">133.3%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">7,090</td>
<td align="right">1.3%</td>
<td align="right">13,798</td>
<td align="right">4.0%</td>
<td align="right">94.6%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">11,587</td>
<td align="right">2.1%</td>
<td align="right">1,467</td>
<td align="right">0.4%</td>
<td align="right">-87.3%</td>
</tr>
<tr>
<td align="left">subscr array</td>
<td align="right">36,682</td>
<td align="right">6.6%</td>
<td align="right">6,512</td>
<td align="right">1.9%</td>
<td align="right">-82.2%</td>
</tr>
<tr>
<td align="left">xor int</td>
<td align="right">16,760</td>
<td align="right">3.0%</td>
<td align="right">3,680</td>
<td align="right">1.1%</td>
<td align="right">-78.0%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">11,290</td>
<td align="right">2.0%</td>
<td align="right">2,659</td>
<td align="right">0.8%</td>
<td align="right">-76.4%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">15,422</td>
<td align="right">2.8%</td>
<td align="right">4,364</td>
<td align="right">1.3%</td>
<td align="right">-71.7%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">18,469</td>
<td align="right">3.3%</td>
<td align="right">7,869</td>
<td align="right">2.3%</td>
<td align="right">-57.4%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">36,887</td>
<td align="right">6.7%</td>
<td align="right">16,179</td>
<td align="right">4.7%</td>
<td align="right">-56.1%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">25,648</td>
<td align="right">4.6%</td>
<td align="right">12,380</td>
<td align="right">3.6%</td>
<td align="right">-51.7%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">63,494</td>
<td align="right">11.5%</td>
<td align="right">33,789</td>
<td align="right">9.8%</td>
<td align="right">-46.8%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">41,347</td>
<td align="right">7.5%</td>
<td align="right">24,648</td>
<td align="right">7.2%</td>
<td align="right">-40.4%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">8,368</td>
<td align="right">1.5%</td>
<td align="right">5,231</td>
<td align="right">1.5%</td>
<td align="right">-37.5%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">30,096</td>
<td align="right">5.4%</td>
<td align="right">19,143</td>
<td align="right">5.6%</td>
<td align="right">-36.4%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">109,554</td>
<td align="right">19.8%</td>
<td align="right">82,056</td>
<td align="right">23.9%</td>
<td align="right">-25.1%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">38,233</td>
<td align="right">6.9%</td>
<td align="right">29,273</td>
<td align="right">8.5%</td>
<td align="right">-23.4%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">15,674</td>
<td align="right">2.8%</td>
<td align="right">12,053</td>
<td align="right">3.5%</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">140</td>
<td align="right">0.0%</td>
<td align="right">120</td>
<td align="right">0.0%</td>
<td align="right">-14.3%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">13,958</td>
<td align="right">2.5%</td>
<td align="right">12,760</td>
<td align="right">3.7%</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">2,261</td>
<td align="right">0.4%</td>
<td align="right">2,443</td>
<td align="right">0.7%</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">2,114</td>
<td align="right">0.4%</td>
<td align="right">2,002</td>
<td align="right">0.6%</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">3,100</td>
<td align="right">0.6%</td>
<td align="right">2,971</td>
<td align="right">0.9%</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">1,387</td>
<td align="right">0.3%</td>
<td align="right">1,343</td>
<td align="right">0.4%</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">630</td>
<td align="right">0.1%</td>
<td align="right">648</td>
<td align="right">0.2%</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">subscr range</td>
<td align="right">3,162</td>
<td align="right">0.6%</td>
<td align="right">3,122</td>
<td align="right">0.9%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">subscr deque</td>
<td align="right">115</td>
<td align="right">0.0%</td>
<td align="right">116</td>
<td align="right">0.0%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">subscr counter</td>
<td align="right">26,852</td>
<td align="right">4.9%</td>
<td align="right">26,892</td>
<td align="right">7.8%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">9,121</td>
<td align="right">1.7%</td>
<td align="right">9,123</td>
<td align="right">2.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr other slice</td>
<td align="right">311</td>
<td align="right">0.1%</td>
<td align="right">311</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">or different types</td>
<td align="right">156</td>
<td align="right">0.0%</td>
<td align="right">156</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr structtime</td>
<td align="right">140</td>
<td align="right">0.0%</td>
<td align="right">140</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">41</td>
<td align="right">0.0%</td>
<td align="right">41</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr ordereddict</td>
<td align="right">23</td>
<td align="right">0.0%</td>
<td align="right">23</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">or int</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr enumdict</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="right">201,330,139</td>
<td align="right">100.0%</td>
<td align="right">110,727,411</td>
<td align="right">100.0%</td>
<td align="right">-45.0%</td>
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
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">8,000</td>
<td align="right">0.0%</td>
<td align="right">31,501</td>
<td align="right">0.0%</td>
<td align="right">293.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">184,570,027</td>
<td align="right">1.4%</td>
<td align="right">139,086,357</td>
<td align="right">1.1%</td>
<td align="right">-24.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">181,150,357</td>
<td align="right">1.4%</td>
<td align="right">136,511,523</td>
<td align="right">1.1%</td>
<td align="right">-24.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">12,601,926,233</td>
<td align="right">98.6%</td>
<td align="right">12,505,587,047</td>
<td align="right">98.9%</td>
<td align="right">-0.8%</td>
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
<td align="right">3,641,774</td>
<td align="right">100.0%</td>
<td align="right">2,797,468</td>
<td align="right">100.0%</td>
<td align="right">-23.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">147</td>
<td align="right">0.0%</td>
<td align="right">147</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="left">init not python</td>
<td align="right">266</td>
<td align="right">181.0%</td>
<td align="right">286</td>
<td align="right">194.6%</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">init not simple</td>
<td align="right">731</td>
<td align="right">497.3%</td>
<td align="right">731</td>
<td align="right">497.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">147</td>
<td align="right">100.0%</td>
<td align="right">147</td>
<td align="right">100.0%</td>
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
<td align="right">537,918</td>
<td align="right">96.6%</td>
<td align="right">537,918</td>
<td align="right">96.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">545,009</td>
<td align="right">97.9%</td>
<td align="right">545,009</td>
<td align="right">97.9%</td>
<td align="right">0.0%</td>
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
<td align="right">18,757</td>
<td align="right">100.0%</td>
<td align="right">18,819</td>
<td align="right">100.0%</td>
<td align="right">0.3%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">149,872,904</td>
<td align="right">2.7%</td>
<td align="right">94,748,478</td>
<td align="right">1.8%</td>
<td align="right">-36.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,306,267</td>
<td align="right">0.0%</td>
<td align="right">1,047,201</td>
<td align="right">0.0%</td>
<td align="right">-19.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,316,388,628</td>
<td align="right">97.2%</td>
<td align="right">5,273,361,516</td>
<td align="right">98.2%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="right">119,669</td>
<td align="right">72.1%</td>
<td align="right">105,883</td>
<td align="right">71.9%</td>
<td align="right">-11.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">46,202</td>
<td align="right">27.9%</td>
<td align="right">41,338</td>
<td align="right">28.1%</td>
<td align="right">-10.5%</td>
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
<td align="left">bytes</td>
<td align="right">1,398</td>
<td align="right">1.2%</td>
<td align="right">4,018</td>
<td align="right">3.8%</td>
<td align="right">187.4%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">14,421</td>
<td align="right">12.1%</td>
<td align="right">6,931</td>
<td align="right">6.5%</td>
<td align="right">-51.9%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">1,865</td>
<td align="right">1.6%</td>
<td align="right">1,123</td>
<td align="right">1.1%</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">6,423</td>
<td align="right">5.4%</td>
<td align="right">7,944</td>
<td align="right">7.5%</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">38,928</td>
<td align="right">32.5%</td>
<td align="right">34,008</td>
<td align="right">32.1%</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">10,653</td>
<td align="right">8.9%</td>
<td align="right">9,388</td>
<td align="right">8.9%</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">30,251</td>
<td align="right">25.3%</td>
<td align="right">27,124</td>
<td align="right">25.6%</td>
<td align="right">-10.3%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">9,729</td>
<td align="right">8.1%</td>
<td align="right">9,225</td>
<td align="right">8.7%</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">4,105</td>
<td align="right">3.4%</td>
<td align="right">4,205</td>
<td align="right">4.0%</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">911</td>
<td align="right">0.8%</td>
<td align="right">931</td>
<td align="right">0.9%</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">801</td>
<td align="right">0.7%</td>
<td align="right">802</td>
<td align="right">0.8%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">184</td>
<td align="right">0.2%</td>
<td align="right">184</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">158,391,776</td>
<td align="right">6.7%</td>
<td align="right">61,773,398</td>
<td align="right">2.7%</td>
<td align="right">-61.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,191,460,735</td>
<td align="right">93.2%</td>
<td align="right">2,187,469,371</td>
<td align="right">97.2%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,402,138</td>
<td align="right">0.1%</td>
<td align="right">1,400,826</td>
<td align="right">0.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">42</td>
<td align="right">0.0%</td>
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
<td align="right">58,800</td>
<td align="right">67.5%</td>
<td align="right">126,502</td>
<td align="right">81.7%</td>
<td align="right">115.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">28,320</td>
<td align="right">32.5%</td>
<td align="right">28,320</td>
<td align="right">18.3%</td>
<td align="right">0.0%</td>
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
<td align="right">11,038</td>
<td align="right">18.8%</td>
<td align="right">93,223</td>
<td align="right">73.7%</td>
<td align="right">744.6%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">28,522</td>
<td align="right">48.5%</td>
<td align="right">12,881</td>
<td align="right">10.2%</td>
<td align="right">-54.8%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">10,040</td>
<td align="right">17.1%</td>
<td align="right">12,748</td>
<td align="right">10.1%</td>
<td align="right">27.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">9,200</td>
<td align="right">15.6%</td>
<td align="right">7,650</td>
<td align="right">6.0%</td>
<td align="right">-16.8%</td>
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
<td align="right">310,043,480</td>
<td align="right">16.7%</td>
<td align="right">92,824,526</td>
<td align="right">11.6%</td>
<td align="right">-70.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">61,944,638</td>
<td align="right">3.3%</td>
<td align="right">23,039,729</td>
<td align="right">2.9%</td>
<td align="right">-62.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,489,689,305</td>
<td align="right">80.0%</td>
<td align="right">674,739,520</td>
<td align="right">84.7%</td>
<td align="right">-54.7%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">164,635</td>
<td align="right">0.0%</td>
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
<td align="right">134,076</td>
<td align="right">10.2%</td>
<td align="right">6,229,820</td>
<td align="right">91.3%</td>
<td align="right">4,546.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,174,404</td>
<td align="right">89.8%</td>
<td align="right">594,574</td>
<td align="right">8.7%</td>
<td align="right">-49.4%</td>
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
<td align="left">map</td>
<td align="right">251</td>
<td align="right">0.2%</td>
<td align="right">476,371</td>
<td align="right">7.6%</td>
<td align="right">189,689.2%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">1,177</td>
<td align="right">0.9%</td>
<td align="right">359,727</td>
<td align="right">5.8%</td>
<td align="right">30,463.0%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">51,352</td>
<td align="right">38.3%</td>
<td align="right">4,307,272</td>
<td align="right">69.1%</td>
<td align="right">8,287.7%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">16,337</td>
<td align="right">12.2%</td>
<td align="right">777,227</td>
<td align="right">12.5%</td>
<td align="right">4,657.5%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">5,271</td>
<td align="right">3.9%</td>
<td align="right">137,893</td>
<td align="right">2.2%</td>
<td align="right">2,516.1%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">3,473</td>
<td align="right">2.6%</td>
<td align="right">77,993</td>
<td align="right">1.3%</td>
<td align="right">2,145.7%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">114</td>
<td align="right">0.1%</td>
<td align="right">1,914</td>
<td align="right">0.0%</td>
<td align="right">1,578.9%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">16,190</td>
<td align="right">12.1%</td>
<td align="right">59,615</td>
<td align="right">1.0%</td>
<td align="right">268.2%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">4,161</td>
<td align="right">3.1%</td>
<td align="right">9,831</td>
<td align="right">0.2%</td>
<td align="right">136.3%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">232</td>
<td align="right">0.2%</td>
<td align="right">545</td>
<td align="right">0.0%</td>
<td align="right">134.9%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">10,920</td>
<td align="right">8.1%</td>
<td align="right">3,973</td>
<td align="right">0.1%</td>
<td align="right">-63.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">4,459</td>
<td align="right">3.3%</td>
<td align="right">2,331</td>
<td align="right">0.0%</td>
<td align="right">-47.7%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">1,730</td>
<td align="right">1.3%</td>
<td align="right">970</td>
<td align="right">0.0%</td>
<td align="right">-43.9%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">12,469</td>
<td align="right">9.3%</td>
<td align="right">7,083</td>
<td align="right">0.1%</td>
<td align="right">-43.2%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">5,580</td>
<td align="right">4.2%</td>
<td align="right">6,795</td>
<td align="right">0.1%</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">320</td>
<td align="right">0.2%</td>
<td align="right">280</td>
<td align="right">0.0%</td>
<td align="right">-12.5%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">40</td>
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
<td align="right">126,471,391</td>
<td align="right">126,471,391 / 0 !!</td>
<td align="right">123,354,153</td>
<td align="right">123,354,153 / 0 !!</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">311,635,459</td>
<td align="right">311,635,459 / 0 !!</td>
<td align="right">307,485,933</td>
<td align="right">307,485,933 / 0 !!</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">12,082,113</td>
<td align="right">12,082,113 / 0 !!</td>
<td align="right">12,130,252</td>
<td align="right">12,130,252 / 0 !!</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">101,610,581</td>
<td align="right">101,610,581 / 0 !!</td>
<td align="right">101,219,186</td>
<td align="right">101,219,186 / 0 !!</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">322,214,921</td>
<td align="right">322,214,921 / 0 !!</td>
<td align="right">322,026,255</td>
<td align="right">322,026,255 / 0 !!</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">5,390,703</td>
<td align="right">5,390,703 / 0 !!</td>
<td align="right">5,388,867</td>
<td align="right">5,388,867 / 0 !!</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">172,650,014</td>
<td align="right">172,650,014 / 0 !!</td>
<td align="right">172,617,263</td>
<td align="right">172,617,263 / 0 !!</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">34,819,624</td>
<td align="right">34,819,624 / 0 !!</td>
<td align="right">34,819,578</td>
<td align="right">34,819,578 / 0 !!</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">2,768,970</td>
<td align="right">2,768,970 / 0 !!</td>
<td align="right">2,768,970</td>
<td align="right">2,768,970 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">775,440</td>
<td align="right">775,440 / 0 !!</td>
<td align="right">775,440</td>
<td align="right">775,440 / 0 !!</td>
<td align="right">0.0%</td>
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
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,422,762</td>
<td align="right">0.0%</td>
<td align="right">2,148,746</td>
<td align="right">0.0%</td>
<td align="right">51.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">785,153,136</td>
<td align="right">5.0%</td>
<td align="right">434,399,258</td>
<td align="right">3.1%</td>
<td align="right">-44.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">609,708,003</td>
<td align="right">3.9%</td>
<td align="right">437,699,943</td>
<td align="right">3.1%</td>
<td align="right">-28.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">14,323,879,124</td>
<td align="right">91.1%</td>
<td align="right">13,231,597,477</td>
<td align="right">93.8%</td>
<td align="right">-7.6%</td>
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
<td align="right">464,761</td>
<td align="right">3.0%</td>
<td align="right">1,477,137</td>
<td align="right">14.5%</td>
<td align="right">217.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">14,886,557</td>
<td align="right">97.0%</td>
<td align="right">8,738,628</td>
<td align="right">85.5%</td>
<td align="right">-41.3%</td>
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
<td align="left">not managed dict</td>
<td align="right">1,869</td>
<td align="right">0.4%</td>
<td align="right">257,686</td>
<td align="right">17.4%</td>
<td align="right">13,687.4%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">22,388</td>
<td align="right">4.8%</td>
<td align="right">532,954</td>
<td align="right">36.1%</td>
<td align="right">2,280.5%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">44,316</td>
<td align="right">9.5%</td>
<td align="right">378,929</td>
<td align="right">25.7%</td>
<td align="right">755.1%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">823</td>
<td align="right">0.2%</td>
<td align="right">4,601</td>
<td align="right">0.3%</td>
<td align="right">459.1%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">603</td>
<td align="right">0.1%</td>
<td align="right">1,232</td>
<td align="right">0.1%</td>
<td align="right">104.3%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">47,781</td>
<td align="right">10.3%</td>
<td align="right">74,822</td>
<td align="right">5.1%</td>
<td align="right">56.6%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">22,240</td>
<td align="right">4.8%</td>
<td align="right">30,207</td>
<td align="right">2.0%</td>
<td align="right">35.8%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">7,713</td>
<td align="right">1.7%</td>
<td align="right">10,396</td>
<td align="right">0.7%</td>
<td align="right">34.8%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">17,058</td>
<td align="right">3.7%</td>
<td align="right">13,119</td>
<td align="right">0.9%</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">45,077</td>
<td align="right">9.7%</td>
<td align="right">37,034</td>
<td align="right">2.5%</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">400</td>
<td align="right">0.1%</td>
<td align="right">380</td>
<td align="right">0.0%</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">718</td>
<td align="right">0.2%</td>
<td align="right">742</td>
<td align="right">0.1%</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">4,864</td>
<td align="right">1.0%</td>
<td align="right">4,944</td>
<td align="right">0.3%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">2,373</td>
<td align="right">0.5%</td>
<td align="right">2,397</td>
<td align="right">0.2%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">1,139</td>
<td align="right">0.2%</td>
<td align="right">1,139</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">200</td>
<td align="right">0.0%</td>
<td align="right">200</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">46</td>
<td align="right">0.0%</td>
<td align="right">46</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,705,944,105</td>
<td align="right">99.8%</td>
<td align="right">5,622,293,170</td>
<td align="right">99.7%</td>
<td align="right">-16.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">41,979</td>
<td align="right">0.0%</td>
<td align="right">41,954</td>
<td align="right">0.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">14,612,709</td>
<td align="right">0.2%</td>
<td align="right">14,612,686</td>
<td align="right">0.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">11</td>
<td align="right">0.0%</td>
<td align="right">11</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="right">124,775</td>
<td align="right">100.0%</td>
<td align="right">125,450</td>
<td align="right">100.0%</td>
<td align="right">0.5%</td>
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
<td align="right">65,622,625</td>
<td align="right">100.0%</td>
<td align="right">65,707,027</td>
<td align="right">100.0%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">122</td>
<td align="right">0.0%</td>
<td align="right">122</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="right">2,225</td>
<td align="right">100.0%</td>
<td align="right">2,225</td>
<td align="right">100.0%</td>
<td align="right">0.0%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">128,406,370</td>
<td align="right">17.8%</td>
<td align="right">128,405,906</td>
<td align="right">17.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">593,215,652</td>
<td align="right">82.2%</td>
<td align="right">593,215,681</td>
<td align="right">82.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">14,711</td>
<td align="right">0.0%</td>
<td align="right">14,711</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="right">33,953</td>
<td align="right">98.2%</td>
<td align="right">55,819</td>
<td align="right">98.9%</td>
<td align="right">64.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">616</td>
<td align="right">1.8%</td>
<td align="right">616</td>
<td align="right">1.1%</td>
<td align="right">0.0%</td>
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
<td align="left">async generator send</td>
<td align="right">24,440</td>
<td align="right">72.0%</td>
<td align="right">45,960</td>
<td align="right">82.3%</td>
<td align="right">88.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">5,948</td>
<td align="right">17.5%</td>
<td align="right">6,295</td>
<td align="right">11.3%</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">640</td>
<td align="right">1.9%</td>
<td align="right">660</td>
<td align="right">1.2%</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">2,925</td>
<td align="right">8.6%</td>
<td align="right">2,904</td>
<td align="right">5.2%</td>
<td align="right">-0.7%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">113,414,470</td>
<td align="right">4.1%</td>
<td align="right">74,653,329</td>
<td align="right">2.7%</td>
<td align="right">-34.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">59,648,811</td>
<td align="right">2.1%</td>
<td align="right">49,476,358</td>
<td align="right">1.8%</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,604,404,729</td>
<td align="right">93.8%</td>
<td align="right">2,600,162,167</td>
<td align="right">95.4%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">15,365</td>
<td align="right">0.0%</td>
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
<td align="right">43,984</td>
<td align="right">2.0%</td>
<td align="right">228,157</td>
<td align="right">13.5%</td>
<td align="right">418.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,178,571</td>
<td align="right">98.0%</td>
<td align="right">1,455,734</td>
<td align="right">86.5%</td>
<td align="right">-33.2%</td>
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
<td align="right">20,345</td>
<td align="right">46.3%</td>
<td align="right">205,593</td>
<td align="right">90.1%</td>
<td align="right">910.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">236,191</td>
<td align="right">537.0%</td>
<td align="right">117,928</td>
<td align="right">51.7%</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">3,719</td>
<td align="right">8.5%</td>
<td align="right">2,259</td>
<td align="right">1.0%</td>
<td align="right">-39.3%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">1,729</td>
<td align="right">3.9%</td>
<td align="right">2,326</td>
<td align="right">1.0%</td>
<td align="right">34.5%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">94</td>
<td align="right">0.2%</td>
<td align="right">115</td>
<td align="right">0.1%</td>
<td align="right">22.3%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">749</td>
<td align="right">1.7%</td>
<td align="right">829</td>
<td align="right">0.4%</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">421</td>
<td align="right">1.0%</td>
<td align="right">377</td>
<td align="right">0.2%</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">4,889</td>
<td align="right">11.1%</td>
<td align="right">4,712</td>
<td align="right">2.1%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">7,206</td>
<td align="right">16.4%</td>
<td align="right">7,106</td>
<td align="right">3.1%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">2,988</td>
<td align="right">6.8%</td>
<td align="right">2,994</td>
<td align="right">1.3%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">313</td>
<td align="right">0.7%</td>
<td align="right">313</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">101</td>
<td align="right">0.2%</td>
<td align="right">101</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">89</td>
<td align="right">0.2%</td>
<td align="right">89</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="right">1,232,574</td>
<td align="right">100.0%</td>
<td align="right">700,470</td>
<td align="right">100.0%</td>
<td align="right">-43.2%</td>
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
<td align="right">122,021,769</td>
<td align="right">11.4%</td>
<td align="right">113,050,608</td>
<td align="right">10.7%</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">949,073,122</td>
<td align="right">88.6%</td>
<td align="right">946,980,192</td>
<td align="right">89.3%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,220</td>
<td align="right">0.0%</td>
<td align="right">2,220</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="right">40,810</td>
<td align="right">93.2%</td>
<td align="right">41,028</td>
<td align="right">93.3%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,956</td>
<td align="right">6.8%</td>
<td align="right">2,958</td>
<td align="right">6.7%</td>
<td align="right">0.1%</td>
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
<td align="left">dict subclass no override</td>
<td align="right">3,923</td>
<td align="right">9.6%</td>
<td align="right">14,269</td>
<td align="right">34.8%</td>
<td align="right">263.7%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">136</td>
<td align="right">0.3%</td>
<td align="right">240</td>
<td align="right">0.6%</td>
<td align="right">76.5%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">1,673</td>
<td align="right">4.1%</td>
<td align="right">493</td>
<td align="right">1.2%</td>
<td align="right">-70.5%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">14,377</td>
<td align="right">35.2%</td>
<td align="right">8,238</td>
<td align="right">20.1%</td>
<td align="right">-42.7%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">2,976</td>
<td align="right">7.3%</td>
<td align="right">2,276</td>
<td align="right">5.5%</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">17,329</td>
<td align="right">42.5%</td>
<td align="right">15,076</td>
<td align="right">36.7%</td>
<td align="right">-13.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">328</td>
<td align="right">0.8%</td>
<td align="right">368</td>
<td align="right">0.9%</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">array slice</td>
<td align="right">68</td>
<td align="right">0.2%</td>
<td align="right">68</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">331,280,679</td>
<td align="right">5.8%</td>
<td align="right">256,765,889</td>
<td align="right">4.9%</td>
<td align="right">-22.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">66,398,834</td>
<td align="right">1.2%</td>
<td align="right">57,396,688</td>
<td align="right">1.1%</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,299,259,668</td>
<td align="right">93.0%</td>
<td align="right">4,892,273,638</td>
<td align="right">94.0%</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">6,995</td>
<td align="right">0.0%</td>
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
<td align="right">574,934</td>
<td align="right">30.7%</td>
<td align="right">486,988</td>
<td align="right">30.0%</td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,300,710</td>
<td align="right">69.3%</td>
<td align="right">1,135,515</td>
<td align="right">70.0%</td>
<td align="right">-12.7%</td>
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
<td align="right">76,245</td>
<td align="right">13.3%</td>
<td align="right">152,965</td>
<td align="right">31.4%</td>
<td align="right">100.6%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">382</td>
<td align="right">0.1%</td>
<td align="right">22</td>
<td align="right">0.0%</td>
<td align="right">-94.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">84,213</td>
<td align="right">14.6%</td>
<td align="right">4,875</td>
<td align="right">1.0%</td>
<td align="right">-94.2%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">71,861</td>
<td align="right">12.5%</td>
<td align="right">7,089</td>
<td align="right">1.5%</td>
<td align="right">-90.1%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">9,524</td>
<td align="right">1.7%</td>
<td align="right">5,480</td>
<td align="right">1.1%</td>
<td align="right">-42.5%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">2,621</td>
<td align="right">0.5%</td>
<td align="right">1,521</td>
<td align="right">0.3%</td>
<td align="right">-42.0%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">11,532</td>
<td align="right">2.0%</td>
<td align="right">7,609</td>
<td align="right">1.6%</td>
<td align="right">-34.0%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">308,986</td>
<td align="right">53.7%</td>
<td align="right">298,121</td>
<td align="right">61.2%</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">9,483</td>
<td align="right">1.6%</td>
<td align="right">9,219</td>
<td align="right">1.9%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">memory view</td>
<td align="right">87</td>
<td align="right">0.0%</td>
<td align="right">87</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,204,378</td>
<td align="right">0.1%</td>
<td align="right">453,232</td>
<td align="right">0.0%</td>
<td align="right">-62.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">3,700</td>
<td align="right">0.0%</td>
<td align="right">3,220</td>
<td align="right">0.0%</td>
<td align="right">-13.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,270,926,067</td>
<td align="right">99.9%</td>
<td align="right">1,256,517,986</td>
<td align="right">100.0%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="right">736</td>
<td align="right">7.0%</td>
<td align="right">766</td>
<td align="right">7.2%</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">9,779</td>
<td align="right">93.0%</td>
<td align="right">9,839</td>
<td align="right">92.8%</td>
<td align="right">0.6%</td>
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
<td align="right">99</td>
<td align="right">13.5%</td>
<td align="right">120</td>
<td align="right">15.7%</td>
<td align="right">21.2%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">505</td>
<td align="right">68.6%</td>
<td align="right">514</td>
<td align="right">67.1%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">132</td>
<td align="right">17.9%</td>
<td align="right">132</td>
<td align="right">17.2%</td>
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
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">4,019,985,923</td>
<td align="right">3.0%</td>
<td align="right">2,337,806,743</td>
<td align="right">2.8%</td>
<td align="right">-41.8%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,276,002,561</td>
<td align="right">1.0%</td>
<td align="right">772,140,308</td>
<td align="right">0.9%</td>
<td align="right">-39.5%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">52,002,222,396</td>
<td align="right">38.7%</td>
<td align="right">31,517,458,251</td>
<td align="right">37.7%</td>
<td align="right">-39.4%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">76,952,971,057</td>
<td align="right">57.3%</td>
<td align="right">48,988,273,210</td>
<td align="right">58.6%</td>
<td align="right">-36.3%</td>
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
<td align="left">FOR_ITER</td>
<td align="right">310,043,480</td>
<td align="right">8.6%</td>
<td align="right">92,824,526</td>
<td align="right">4.5%</td>
<td align="right">-70.1%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">158,391,776</td>
<td align="right">4.4%</td>
<td align="right">61,773,398</td>
<td align="right">3.0%</td>
<td align="right">-61.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,350,514,188</td>
<td align="right">37.3%</td>
<td align="right">581,712,214</td>
<td align="right">28.0%</td>
<td align="right">-56.9%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">201,330,139</td>
<td align="right">5.6%</td>
<td align="right">110,727,411</td>
<td align="right">5.3%</td>
<td align="right">-45.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">149,872,904</td>
<td align="right">4.1%</td>
<td align="right">94,748,478</td>
<td align="right">4.6%</td>
<td align="right">-36.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">609,708,003</td>
<td align="right">16.8%</td>
<td align="right">437,699,943</td>
<td align="right">21.0%</td>
<td align="right">-28.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">181,150,357</td>
<td align="right">5.0%</td>
<td align="right">136,511,523</td>
<td align="right">6.6%</td>
<td align="right">-24.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">331,280,679</td>
<td align="right">9.2%</td>
<td align="right">256,765,889</td>
<td align="right">12.3%</td>
<td align="right">-22.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">122,021,769</td>
<td align="right">3.4%</td>
<td align="right">113,050,608</td>
<td align="right">5.4%</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,406,370</td>
<td align="right">3.5%</td>
<td align="right">128,405,906</td>
<td align="right">6.2%</td>
<td align="right">-0.0%</td>
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
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">248,651,374</td>
<td align="right">19.5%</td>
<td align="right">109,188,091</td>
<td align="right">14.1%</td>
<td align="right">-56.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">326,266,651</td>
<td align="right">25.6%</td>
<td align="right">150,668,071</td>
<td align="right">19.5%</td>
<td align="right">-53.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">93,618,063</td>
<td align="right">7.3%</td>
<td align="right">54,868,965</td>
<td align="right">7.1%</td>
<td align="right">-41.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">78,477,963</td>
<td align="right">6.1%</td>
<td align="right">51,243,012</td>
<td align="right">6.6%</td>
<td align="right">-34.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">75,511,415</td>
<td align="right">5.9%</td>
<td align="right">54,278,537</td>
<td align="right">7.0%</td>
<td align="right">-28.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">32,152,900</td>
<td align="right">2.5%</td>
<td align="right">28,067,251</td>
<td align="right">3.6%</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">27,564,123</td>
<td align="right">2.2%</td>
<td align="right">24,978,579</td>
<td align="right">3.2%</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">80,511,235</td>
<td align="right">6.3%</td>
<td align="right">73,535,405</td>
<td align="right">9.5%</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">30,933,616</td>
<td align="right">2.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">30,884,246</td>
<td align="right">2.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">24,854,440</td>
<td align="right">3.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">20,872,266</td>
<td align="right">2.7%</td>
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
<td align="right">4,273,296</td>
<td align="right">0.1%</td>
<td align="right">2,128,101</td>
<td align="right">0.0%</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,026,118,478</td>
<td align="right">76.1%</td>
<td align="right">5,857,009,009</td>
<td align="right">75.7%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">78,007,742</td>
<td align="right">1.0%</td>
<td align="right">76,010,562</td>
<td align="right">1.0%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,692,028,625</td>
<td align="right">84.5%</td>
<td align="right">6,551,009,852</td>
<td align="right">84.7%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">613,945,254</td>
<td align="right">7.8%</td>
<td align="right">605,363,982</td>
<td align="right">7.8%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">1,894,748,115</td>
<td align="right">23.9%</td>
<td align="right">1,881,734,603</td>
<td align="right">24.3%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">1,894,748,115</td>
<td align="right">23.9%</td>
<td align="right">1,881,734,603</td>
<td align="right">24.3%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,280,802,861</td>
<td align="right">16.2%</td>
<td align="right">1,276,370,621</td>
<td align="right">16.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">141,112,765</td>
<td align="right">1.8%</td>
<td align="right">140,848,809</td>
<td align="right">1.8%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,276,526,190</td>
<td align="right">16.1%</td>
<td align="right">1,274,239,145</td>
<td align="right">16.5%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">458,246,253</td>
<td align="right">5.8%</td>
<td align="right">457,714,320</td>
<td align="right">5.9%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">305,854,240</td>
<td align="right">3.9%</td>
<td align="right">305,854,903</td>
<td align="right">4.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">24,439,833</td>
<td align="right">0.3%</td>
<td align="right">24,439,836</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">3,375</td>
<td align="right">0.0%</td>
<td align="right">3,375</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="left">Interpreter mortal increfs</td>
<td align="right">30,315,962,253</td>
<td align="right">31.1%</td>
<td align="right">20,556,828,118</td>
<td align="right">21.4%</td>
<td align="right">-32.2%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">1,475,369,771</td>
<td align="right">1.3%</td>
<td align="right">1,105,155,383</td>
<td align="right">1.0%</td>
<td align="right">-25.1%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">38,021,167,062</td>
<td align="right">39.0%</td>
<td align="right">46,714,294,527</td>
<td align="right">48.7%</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">39,305,994,934</td>
<td align="right">35.1%</td>
<td align="right">32,352,037,633</td>
<td align="right">29.3%</td>
<td align="right">-17.7%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">4,016,235,923</td>
<td align="right">4.1%</td>
<td align="right">3,314,885,353</td>
<td align="right">3.5%</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">4,056,483</td>
<td align="right">2.1%</td>
<td align="right">3,390,883</td>
<td align="right">1.8%</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">2,300,074,768</td>
<td align="right"></td>
<td align="right">1,953,964,265</td>
<td align="right"></td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">47,355,402,945</td>
<td align="right">42.2%</td>
<td align="right">53,040,103,941</td>
<td align="right">48.0%</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">6,230,532</td>
<td align="right"></td>
<td align="right">6,512,580</td>
<td align="right"></td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">13,845,791,930</td>
<td align="right"></td>
<td align="right">13,662,123,949</td>
<td align="right"></td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">13,845,600,010</td>
<td align="right">70.3%</td>
<td align="right">13,661,942,791</td>
<td align="right">70.1%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">5,782,068,426</td>
<td align="right">29.3%</td>
<td align="right">5,753,872,573</td>
<td align="right">29.5%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">6,452,176,760</td>
<td align="right"></td>
<td align="right">6,420,993,544</td>
<td align="right"></td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">5,860,221,974</td>
<td align="right">29.7%</td>
<td align="right">5,832,103,099</td>
<td align="right">29.9%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">2,889,855,749</td>
<td align="right"></td>
<td align="right">2,876,138,324</td>
<td align="right"></td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">61,630,374</td>
<td align="right"></td>
<td align="right">61,909,328</td>
<td align="right"></td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">25,222,819,420</td>
<td align="right">25.8%</td>
<td align="right">25,332,446,786</td>
<td align="right">26.4%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">6,775,536</td>
<td align="right">0.0%</td>
<td align="right">6,799,209</td>
<td align="right">0.0%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">190,517,854</td>
<td align="right"></td>
<td align="right">189,911,190</td>
<td align="right"></td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">23,949,575,720</td>
<td align="right">21.4%</td>
<td align="right">23,893,691,504</td>
<td align="right">21.6%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">56,202,928</td>
<td align="right"></td>
<td align="right">56,140,672</td>
<td align="right"></td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">71,378,012</td>
<td align="right">0.4%</td>
<td align="right">71,431,317</td>
<td align="right">0.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">264,809</td>
<td align="right">0.1%</td>
<td align="right">264,809</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">4,404</td>
<td align="right">0.0%</td>
<td align="right">4,404</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
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
<td align="right">358,124</td>
<td align="right">98,775,759</td>
<td align="right">9,544,198,110</td>
<td align="right">776,465,701</td>
<td align="right">747,993,672</td>
<td align="right">357,669</td>
<td align="right">98,916,343</td>
<td align="right">9,562,006,244</td>
<td align="right">775,398,725</td>
<td align="right">748,357,383</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">15,998</td>
<td align="right">8,734,250</td>
<td align="right">11,440,437,150</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">15,998</td>
<td align="right">8,734,250</td>
<td align="right">11,441,288,766</td>
<td align="right">0</td>
<td align="right">0</td>
</tr>
</tbody>
</table>


</details>

## Optimization (Tier 2) stats

<details>
<summary> statistics about the Tier 2 optimizer </summary>

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
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">502,367</td>
<td align="right"></td>
<td align="right">24,299,847</td>
<td align="right"></td>
<td align="right">4,737.1%</td>
</tr>
<tr>
<td align="left">
Trace too long
<details>
<summary>ⓘ</summary>

A trace is truncated because it is longer than the instruction buffer.
</details>
</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">1,576</td>
<td align="right">0.0%</td>
<td align="right">2,526.7%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">693</td>
<td align="right">0.1%</td>
<td align="right">7,352</td>
<td align="right">0.0%</td>
<td align="right">960.9%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">23,056</td>
<td align="right">4.6%</td>
<td align="right">94,022</td>
<td align="right">0.4%</td>
<td align="right">307.8%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">240</td>
<td align="right">1.0%</td>
<td align="right">525</td>
<td align="right">0.6%</td>
<td align="right">118.8%</td>
</tr>
<tr>
<td align="left">
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
</details>
</td>
<td align="right">62</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">217,689</td>
<td align="right">43.3%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it is too short.
</details>
</td>
<td align="right">47,608</td>
<td align="right">9.5%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
</details>
</td>
<td align="right">747</td>
<td align="right">0.1%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
</details>
</td>
<td align="right">624</td>
<td align="right">0.1%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Unknown callee
<details>
<summary>ⓘ</summary>

A trace is abandoned because the target of a call is unknown.
</details>
</td>
<td align="right">213,952</td>
<td align="right">42.6%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">231,341,483,183</td>
<td align="right">5,313.7%</td>
<td align="right">355,925,954,195</td>
<td align="right">6,050.3%</td>
<td align="right">53.9%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">4,353,705,071</td>
<td align="right"></td>
<td align="right">5,882,818,893</td>
<td align="right"></td>
<td align="right">35.1%</td>
</tr>
</tbody>
</table>

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
<td align="left">
Optimizer successes
<details>
<summary>ⓘ</summary>

The number of traces that were successfully optimized.
</details>
</td>
<td align="right">19,756</td>
<td align="right">85.7%</td>
<td align="right">92,755</td>
<td align="right">98.7%</td>
<td align="right">369.5%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">23,056</td>
<td align="right"></td>
<td align="right">94,022</td>
<td align="right"></td>
<td align="right">307.8%</td>
</tr>
<tr>
<td align="left">
Optimizer no memory
<details>
<summary>ⓘ</summary>

The number of optimizations that failed due to no memory.
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Remove globals builtins changed
<details>
<summary>ⓘ</summary>

The builtins changed during optimization
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">
Remove globals incorrect keys
<details>
<summary>ⓘ</summary>

The keys in the globals dictionary aren't what was expected
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>

### JIT memory stats

<details>
<summary> JIT memory stats </summary>

<table>
<thead>
<tr>
<th align="left"></th>
<th align="right">Base Size (bytes)</th>
<th align="right">Base Ratio</th>
<th align="right">Head Size (bytes)</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">
Freed memory size
<details>
<summary>ⓘ</summary>

The size of the memory freed from the JIT traces
</details>
</td>
<td align="right">815,104</td>
<td align="right">0.5%</td>
<td align="right">133,275,648</td>
<td align="right">10.3%</td>
<td align="right">16,250.8%</td>
</tr>
<tr>
<td align="left">
Code size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the code of the JIT traces
</details>
</td>
<td align="right">133,304,726</td>
<td align="right">75.3%</td>
<td align="right">1,086,482,281</td>
<td align="right">83.7%</td>
<td align="right">715.0%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">177,147,904</td>
<td align="right"></td>
<td align="right">1,298,219,008</td>
<td align="right"></td>
<td align="right">632.8%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">3,216,592</td>
<td align="right">1.8%</td>
<td align="right">21,008,720</td>
<td align="right">1.6%</td>
<td align="right">553.1%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">40,606,750</td>
<td align="right">22.9%</td>
<td align="right">190,635,210</td>
<td align="right">14.7%</td>
<td align="right">369.5%</td>
</tr>
<tr>
<td align="left">
Trampoline size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the trampolines of the JIT traces
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### JIT trace total memory histogram

<details>
<summary> JIT trace total memory histogram </summary>

<table>
<thead>
<tr>
<th align="left">Size (bytes)</th>
<th align="left">Base Count</th>
<th align="right">Base Ratio</th>
<th align="left">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><= 4,096</td>
<td align="left">8,185</td>
<td align="right">41.3%</td>
<td align="left">29,840</td>
<td align="right">32.2%</td>
<td align="right">264.6%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">6,949</td>
<td align="right">35.0%</td>
<td align="left">24,462</td>
<td align="right">26.4%</td>
<td align="right">252.0%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">3,026</td>
<td align="right">15.3%</td>
<td align="left">19,843</td>
<td align="right">21.4%</td>
<td align="right">555.8%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">1,376</td>
<td align="right">6.9%</td>
<td align="left">11,636</td>
<td align="right">12.5%</td>
<td align="right">745.6%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left">300</td>
<td align="right">1.5%</td>
<td align="left">5,267</td>
<td align="right">5.7%</td>
<td align="right">1,655.7%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">1,749</td>
<td align="right">1.9%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### Trace length histogram

<details>
<summary> trace length histogram </summary>

<table>
<thead>
<tr>
<th align="left">Range</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><= 8</td>
<td align="right">1,053</td>
<td align="right">4.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">814</td>
<td align="right">3.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">3,582</td>
<td align="right">15.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">7,647</td>
<td align="right">33.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">4,419</td>
<td align="right">19.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">4,212</td>
<td align="right">18.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">1,201</td>
<td align="right">5.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right">128</td>
<td align="right">0.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### Optimized trace length histogram

<details>
<summary> optimized trace length histogram </summary>

<table>
<thead>
<tr>
<th align="left">Range</th>
<th align="right">Base Count</th>
<th align="right">Base Ratio</th>
<th align="right">Head Count</th>
<th align="right">Head Ratio</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><= 4</td>
<td align="right">673</td>
<td align="right">2.9%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">526</td>
<td align="right">2.3%</td>
<td align="right">788</td>
<td align="right">0.8%</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">1,988</td>
<td align="right">8.6%</td>
<td align="right">12,944</td>
<td align="right">13.8%</td>
<td align="right">551.1%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">7,051</td>
<td align="right">30.6%</td>
<td align="right">23,914</td>
<td align="right">25.4%</td>
<td align="right">239.2%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">6,044</td>
<td align="right">26.2%</td>
<td align="right">23,784</td>
<td align="right">25.3%</td>
<td align="right">293.5%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">1,858</td>
<td align="right">8.1%</td>
<td align="right">14,784</td>
<td align="right">15.7%</td>
<td align="right">695.7%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">1,385</td>
<td align="right">6.0%</td>
<td align="right">11,432</td>
<td align="right">12.2%</td>
<td align="right">725.4%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">231</td>
<td align="right">1.0%</td>
<td align="right">3,693</td>
<td align="right">3.9%</td>
<td align="right">1,498.7%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">1,396</td>
<td align="right">1.5%</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### Trace run length histogram

<details>
<summary> trace run length histogram </summary>


</details>

### Uop execution stats

<details>
<summary> uop execution stats </summary>

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
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right">3,985</td>
<td align="right">9,631,497</td>
<td align="right">241,593.8%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">54,160</td>
<td align="right">105,354,936</td>
<td align="right">194,425.4%</td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_1</td>
<td align="right">269,900</td>
<td align="right">200,344,723</td>
<td align="right">74,129.2%</td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_0</td>
<td align="right">352,940</td>
<td align="right">161,216,213</td>
<td align="right">45,578.1%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right">449,298</td>
<td align="right">192,669,954</td>
<td align="right">42,782.4%</td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right">449,298</td>
<td align="right">192,669,954</td>
<td align="right">42,782.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NULL</td>
<td align="right">270,020</td>
<td align="right">101,270,628</td>
<td align="right">37,404.9%</td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">263</td>
<td align="right">95,149</td>
<td align="right">36,078.3%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">160,148</td>
<td align="right">39,534,581</td>
<td align="right">24,586.3%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">212,260</td>
<td align="right">48,642,286</td>
<td align="right">22,816.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">471,948</td>
<td align="right">65,182,589</td>
<td align="right">13,711.4%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">954,726</td>
<td align="right">97,093,675</td>
<td align="right">10,069.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">363,240</td>
<td align="right">35,182,347</td>
<td align="right">9,585.7%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LEN</td>
<td align="right">1,120,240</td>
<td align="right">84,370,266</td>
<td align="right">7,431.4%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">5,364,242</td>
<td align="right">305,719,012</td>
<td align="right">5,599.2%</td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">163,738</td>
<td align="right">8,170,837</td>
<td align="right">4,890.2%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">2,477,668</td>
<td align="right">98,801,997</td>
<td align="right">3,887.7%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right">56,140,165</td>
<td align="right">2,129,971,387</td>
<td align="right">3,694.0%</td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">26,932</td>
<td align="right">902,814</td>
<td align="right">3,252.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right">23,245,502</td>
<td align="right">699,039,344</td>
<td align="right">2,907.2%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">21,901,065</td>
<td align="right">646,539,466</td>
<td align="right">2,852.1%</td>
</tr>
<tr>
<td align="left">_IMPORT_NAME</td>
<td align="right">27,762</td>
<td align="right">811,765</td>
<td align="right">2,824.0%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">23,670,736</td>
<td align="right">530,094,978</td>
<td align="right">2,139.5%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">28,058,849</td>
<td align="right">591,609,608</td>
<td align="right">2,008.5%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">28,058,849</td>
<td align="right">591,609,608</td>
<td align="right">2,008.5%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION_AND_LOCK</td>
<td align="right">29,686,209</td>
<td align="right">592,866,952</td>
<td align="right">1,897.1%</td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right">46,427,104</td>
<td align="right">598,366,462</td>
<td align="right">1,188.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">23,189,260</td>
<td align="right">276,418,912</td>
<td align="right">1,092.0%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">2,834,024</td>
<td align="right">25,576,556</td>
<td align="right">802.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">2,522,739</td>
<td align="right">16,750,690</td>
<td align="right">564.0%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">8,093,835</td>
<td align="right">53,176,495</td>
<td align="right">557.0%</td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right">56,148,891</td>
<td align="right">359,351,062</td>
<td align="right">540.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS</td>
<td align="right">3,106,080</td>
<td align="right">17,101,650</td>
<td align="right">450.6%</td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right">9,548</td>
<td align="right">49,850</td>
<td align="right">422.1%</td>
</tr>
<tr>
<td align="left">_PY_FRAME_KW</td>
<td align="right">12,237,291</td>
<td align="right">63,541,912</td>
<td align="right">419.2%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_KW</td>
<td align="right">12,237,291</td>
<td align="right">62,777,901</td>
<td align="right">413.0%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">5,884,815</td>
<td align="right">29,787,782</td>
<td align="right">406.2%</td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right">508,019,574</td>
<td align="right">2,379,055,890</td>
<td align="right">368.3%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">6,137,792</td>
<td align="right">27,598,058</td>
<td align="right">349.6%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">51,809,561</td>
<td align="right">232,139,205</td>
<td align="right">348.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">21,198,257</td>
<td align="right">90,125,843</td>
<td align="right">325.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right">42,172,928</td>
<td align="right">176,776,532</td>
<td align="right">319.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_EXTEND</td>
<td align="right">52,687,141</td>
<td align="right">220,219,198</td>
<td align="right">318.0%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">161,035,011</td>
<td align="right">654,582,932</td>
<td align="right">306.5%</td>
</tr>
<tr>
<td align="left">_GUARD_BINARY_OP_EXTEND</td>
<td align="right">62,227,141</td>
<td align="right">246,184,018</td>
<td align="right">295.6%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">214,345,287</td>
<td align="right">836,977,169</td>
<td align="right">290.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">237,253,742</td>
<td align="right">924,614,617</td>
<td align="right">289.7%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">111,036,577</td>
<td align="right">427,195,351</td>
<td align="right">284.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">136,472,141</td>
<td align="right">522,750,931</td>
<td align="right">283.0%</td>
</tr>
<tr>
<td align="left">_PY_FRAME_GENERAL</td>
<td align="right">45,540,800</td>
<td align="right">174,045,233</td>
<td align="right">282.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">1,323,217</td>
<td align="right">4,944,047</td>
<td align="right">273.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">82,564,084</td>
<td align="right">296,696,358</td>
<td align="right">259.4%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">920,227,297</td>
<td align="right">3,287,458,673</td>
<td align="right">257.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">920,184,857</td>
<td align="right">3,286,760,280</td>
<td align="right">257.2%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">59,184,907</td>
<td align="right">198,069,274</td>
<td align="right">234.7%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">5,031,398</td>
<td align="right">16,680,483</td>
<td align="right">231.5%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">217,964,985</td>
<td align="right">688,077,785</td>
<td align="right">215.7%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">9,888,557</td>
<td align="right">30,633,770</td>
<td align="right">209.8%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">364,500</td>
<td align="right">1,115,742</td>
<td align="right">206.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">45,499,670</td>
<td align="right">138,912,114</td>
<td align="right">205.3%</td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right">118,787,328</td>
<td align="right">359,083,896</td>
<td align="right">202.3%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">40,807,623</td>
<td align="right">122,131,787</td>
<td align="right">199.3%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">967,662,494</td>
<td align="right">2,881,160,699</td>
<td align="right">197.7%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">64,250,594</td>
<td align="right">184,529,527</td>
<td align="right">187.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">26,137,232</td>
<td align="right">73,693,385</td>
<td align="right">181.9%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">10,088,679</td>
<td align="right">27,484,042</td>
<td align="right">172.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">337,632,045</td>
<td align="right">887,736,480</td>
<td align="right">162.9%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">967,662,494</td>
<td align="right">2,428,945,488</td>
<td align="right">151.0%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">77,261,102</td>
<td align="right">193,451,849</td>
<td align="right">150.4%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">967,662,494</td>
<td align="right">2,420,610,150</td>
<td align="right">150.2%</td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right">47,734,139</td>
<td align="right">118,582,412</td>
<td align="right">148.4%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">2,397,440,899</td>
<td align="right">5,857,555,478</td>
<td align="right">144.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">345,586,121</td>
<td align="right">840,446,524</td>
<td align="right">143.2%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">69,094,889</td>
<td align="right">164,736,462</td>
<td align="right">138.4%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">174,383,886</td>
<td align="right">413,728,007</td>
<td align="right">137.3%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">750,237,687</td>
<td align="right">1,748,856,354</td>
<td align="right">133.1%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">750,380,347</td>
<td align="right">1,749,162,753</td>
<td align="right">133.1%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">263,469,479</td>
<td align="right">612,762,614</td>
<td align="right">132.6%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">52,932,020</td>
<td align="right">120,877,432</td>
<td align="right">128.4%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">52,932,020</td>
<td align="right">120,876,832</td>
<td align="right">128.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">90,677,910</td>
<td align="right">201,807,865</td>
<td align="right">122.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">3,265,354,636</td>
<td align="right">7,251,242,185</td>
<td align="right">122.1%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">611,996,504</td>
<td align="right">1,354,243,369</td>
<td align="right">121.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">900,380,128</td>
<td align="right">1,967,653,751</td>
<td align="right">118.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_TUPLE</td>
<td align="right">35,941,400</td>
<td align="right">77,317,959</td>
<td align="right">115.1%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_FLOAT</td>
<td align="right">298,345,881</td>
<td align="right">637,794,888</td>
<td align="right">113.8%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">42,078,620</td>
<td align="right">88,300,578</td>
<td align="right">109.8%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right">775,374,192</td>
<td align="right">1,619,158,143</td>
<td align="right">108.8%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">450,781,074</td>
<td align="right">928,691,232</td>
<td align="right">106.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">2,665,095,883</td>
<td align="right">5,458,609,384</td>
<td align="right">104.8%</td>
</tr>
<tr>
<td align="left">_EXPAND_METHOD</td>
<td align="right">5,976,000</td>
<td align="right">11,812,160</td>
<td align="right">97.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">1,748,431,000</td>
<td align="right">3,325,714,778</td>
<td align="right">90.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">94,628,877</td>
<td align="right">179,322,366</td>
<td align="right">89.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right">429,239,042</td>
<td align="right">789,249,405</td>
<td align="right">83.9%</td>
</tr>
<tr>
<td align="left">_CHECK_METHOD_VERSION</td>
<td align="right">5,976,000</td>
<td align="right">10,929,500</td>
<td align="right">82.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">3,745,873,640</td>
<td align="right">6,841,187,047</td>
<td align="right">82.6%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">1,079,652,386</td>
<td align="right">1,892,717,818</td>
<td align="right">75.3%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">44,368,140</td>
<td align="right">76,332,516</td>
<td align="right">72.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">304,711,809</td>
<td align="right">523,891,126</td>
<td align="right">71.9%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_OVERFLOWED</td>
<td align="right">144,983,587</td>
<td align="right">248,861,149</td>
<td align="right">71.6%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">488,643,802</td>
<td align="right">837,252,573</td>
<td align="right">71.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">1,074,713,527</td>
<td align="right">1,807,095,638</td>
<td align="right">68.1%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">146,225,820</td>
<td align="right">245,422,402</td>
<td align="right">67.8%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">50,628,850</td>
<td align="right">16,790,385</td>
<td align="right">-66.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,046,039,705</td>
<td align="right">1,697,823,550</td>
<td align="right">62.3%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">213,637,320</td>
<td align="right">344,795,136</td>
<td align="right">61.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">1,781,318,394</td>
<td align="right">2,870,330,054</td>
<td align="right">61.1%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">237,193,280</td>
<td align="right">364,481,094</td>
<td align="right">53.7%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">33,528,158,745</td>
<td align="right">51,026,563,994</td>
<td align="right">52.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">404,658,256</td>
<td align="right">615,550,643</td>
<td align="right">52.1%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">38,093,474,674</td>
<td align="right">57,748,460,399</td>
<td align="right">51.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_FLOAT</td>
<td align="right">667,851,901</td>
<td align="right">1,011,687,211</td>
<td align="right">51.5%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right">37,039,760</td>
<td align="right">55,746,907</td>
<td align="right">50.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">3,445,911</td>
<td align="right">5,131,094</td>
<td align="right">48.9%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right">305,788,274</td>
<td align="right">454,465,101</td>
<td align="right">48.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">1,972,489,249</td>
<td align="right">2,926,409,065</td>
<td align="right">48.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">802,108,679</td>
<td align="right">1,188,105,169</td>
<td align="right">48.1%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">2,191,253,508</td>
<td align="right">3,224,968,699</td>
<td align="right">47.2%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">569,140,269</td>
<td align="right">836,729,330</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">733,956,790</td>
<td align="right">1,074,189,749</td>
<td align="right">46.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">427,723,907</td>
<td align="right">623,453,724</td>
<td align="right">45.8%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">427,723,907</td>
<td align="right">623,453,724</td>
<td align="right">45.8%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">406,690,156</td>
<td align="right">587,686,013</td>
<td align="right">44.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right">403,392,661</td>
<td align="right">579,333,123</td>
<td align="right">43.6%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">40,824,726</td>
<td align="right">58,441,513</td>
<td align="right">43.2%</td>
</tr>
<tr>
<td align="left">_CALL_KW_NON_PY</td>
<td align="right">19,731,666</td>
<td align="right">28,234,161</td>
<td align="right">43.1%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE_KW</td>
<td align="right">19,731,666</td>
<td align="right">28,234,161</td>
<td align="right">43.1%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">252,648,121</td>
<td align="right">360,088,943</td>
<td align="right">42.5%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,652,727,191</td>
<td align="right">3,757,999,484</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">154,370,328</td>
<td align="right">218,587,021</td>
<td align="right">41.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">2,602,101,201</td>
<td align="right">3,678,429,381</td>
<td align="right">41.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">1,367,799,599</td>
<td align="right">1,918,526,788</td>
<td align="right">40.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right">248,909,661</td>
<td align="right">347,704,013</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">37,123,103</td>
<td align="right">51,574,057</td>
<td align="right">38.9%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">267,807,753</td>
<td align="right">367,344,376</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">1,239,566,240</td>
<td align="right">1,699,845,743</td>
<td align="right">37.1%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">512,457,819</td>
<td align="right">697,804,193</td>
<td align="right">36.2%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">573,328,659</td>
<td align="right">779,574,530</td>
<td align="right">36.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">1,656,392,397</td>
<td align="right">2,246,158,419</td>
<td align="right">35.6%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">346,469,879</td>
<td align="right">468,266,049</td>
<td align="right">35.2%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">4,239,335,403</td>
<td align="right">5,666,072,666</td>
<td align="right">33.7%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">140,122,676</td>
<td align="right">186,853,813</td>
<td align="right">33.4%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">3,619,748,281</td>
<td align="right">4,808,629,144</td>
<td align="right">32.8%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">4,484,333,852</td>
<td align="right">5,880,228,584</td>
<td align="right">31.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">45,444,857</td>
<td align="right">59,315,578</td>
<td align="right">30.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">1,016,575,069</td>
<td align="right">1,316,904,351</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">156,757,059</td>
<td align="right">202,991,417</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right">103,178,700</td>
<td align="right">132,744,560</td>
<td align="right">28.7%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">1,495,951,197</td>
<td align="right">1,921,924,676</td>
<td align="right">28.5%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">233,408,249</td>
<td align="right">299,571,595</td>
<td align="right">28.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">142,238,307</td>
<td align="right">182,531,754</td>
<td align="right">28.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_DICT</td>
<td align="right">657,588,816</td>
<td align="right">840,496,166</td>
<td align="right">27.8%</td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">46,444,694</td>
<td align="right">33,768,434</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">340,710,360</td>
<td align="right">428,650,420</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">799,901,312</td>
<td align="right">1,001,407,174</td>
<td align="right">25.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">7,718,377,029</td>
<td align="right">9,658,990,401</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">409,400,187</td>
<td align="right">512,310,817</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">3,705,303,886</td>
<td align="right">4,632,196,862</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">410,260,767</td>
<td align="right">512,634,925</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right">982,829,517</td>
<td align="right">1,227,575,828</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">182,151,312</td>
<td align="right">226,941,237</td>
<td align="right">24.6%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">5,988,562,462</td>
<td align="right">7,456,788,729</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">234,655,433</td>
<td align="right">291,493,219</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">19,954,728</td>
<td align="right">24,785,248</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,123,240,005</td>
<td align="right">1,391,654,493</td>
<td align="right">23.9%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE</td>
<td align="right">265,835,176</td>
<td align="right">328,943,068</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">155,495,534</td>
<td align="right">191,903,541</td>
<td align="right">23.4%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">2,832,406,093</td>
<td align="right">3,475,336,631</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,303,434,901</td>
<td align="right">2,822,595,570</td>
<td align="right">22.5%</td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right">899,831,056</td>
<td align="right">1,098,573,250</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">3,866,115,190</td>
<td align="right">4,717,533,595</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">345,775,945</td>
<td align="right">416,958,209</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">26,715,013</td>
<td align="right">31,921,257</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,206,680,466</td>
<td align="right">1,438,625,951</td>
<td align="right">19.2%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">3,609,849,907</td>
<td align="right">4,284,552,958</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">2,345,782,880</td>
<td align="right">2,771,322,125</td>
<td align="right">18.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">182,690,748</td>
<td align="right">215,524,794</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">976,111,797</td>
<td align="right">1,148,206,295</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">263,274,974</td>
<td align="right">309,608,190</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">2,141,356,686</td>
<td align="right">2,494,109,681</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">1,212,714,853</td>
<td align="right">1,402,777,363</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">3,879,492,723</td>
<td align="right">4,486,113,651</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">471,717,352</td>
<td align="right">544,318,799</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">3,755,811,616</td>
<td align="right">4,333,204,109</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">47,062,820</td>
<td align="right">54,237,197</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">10,637,123,816</td>
<td align="right">12,224,923,314</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">754,556,366</td>
<td align="right">861,396,500</td>
<td align="right">14.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_LIST</td>
<td align="right">105,457,097</td>
<td align="right">120,219,924</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">2,723,841,411</td>
<td align="right">3,059,798,568</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,479,076,357</td>
<td align="right">1,657,682,322</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">1,101,811,634</td>
<td align="right">1,234,355,036</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,368,815,264</td>
<td align="right">2,648,161,073</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">191,609,882</td>
<td align="right">169,926,883</td>
<td align="right">-11.3%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,345,308,739</td>
<td align="right">1,494,124,709</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">380,133,630</td>
<td align="right">421,983,726</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">46,687,414</td>
<td align="right">51,705,859</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT__NO_DECREF_INPUTS</td>
<td align="right">430,309,104</td>
<td align="right">476,245,279</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right">421,109,310</td>
<td align="right">376,472,619</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,014,622,136</td>
<td align="right">1,119,715,715</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">70,350,182</td>
<td align="right">77,074,066</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_OVERFLOWED</td>
<td align="right">1,228,429,102</td>
<td align="right">1,345,229,058</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">_COPY_2</td>
<td align="right">1,533,580,158</td>
<td align="right">1,666,754,068</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">70,350,182</td>
<td align="right">76,384,306</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">78,215,044</td>
<td align="right">84,276,278</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_ANY_SET</td>
<td align="right">1,198,887,372</td>
<td align="right">1,286,607,554</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">47,882,593</td>
<td align="right">44,466,952</td>
<td align="right">-7.1%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">485,047,588</td>
<td align="right">519,066,510</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">120,157,171</td>
<td align="right">128,488,375</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">876,883,752</td>
<td align="right">934,349,672</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">3,530,385</td>
<td align="right">3,756,018</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">876,883,752</td>
<td align="right">930,598,343</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">1,011,704,326</td>
<td align="right">1,071,253,515</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">_SWAP_3</td>
<td align="right">758,452,303</td>
<td align="right">786,516,344</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">_POP_TOP_INT</td>
<td align="right">16,730,708</td>
<td align="right">17,333,842</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">60,012,240</td>
<td align="right">61,406,803</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">79,515,446</td>
<td align="right">80,972,582</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">80,015,830</td>
<td align="right">81,400,260</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">40,187,757</td>
<td align="right">40,873,882</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">569,327,453</td>
<td align="right">565,297,697</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">425,721,392</td>
<td align="right">427,782,978</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_SLICE</td>
<td align="right">425,721,392</td>
<td align="right">427,782,978</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_STORE_SLICE</td>
<td align="right">111,492,300</td>
<td align="right">112,024,400</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">498,445,573</td>
<td align="right">500,729,116</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">886,618,654</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_ANEXT</td>
<td align="right">94,136,760</td>
<td align="right">94,136,760</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT__NO_DECREF_INPUTS</td>
<td align="right">71,999,640</td>
<td align="right">71,999,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">5,464,787,622</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">493,297,413</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">266,478,426</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_CHECK_FUNC</td>
<td align="right"></td>
<td align="right">97,045,202</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_INIT_CALL</td>
<td align="right"></td>
<td align="right">97,043,742</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">85,988,621</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_AND_ALLOCATE_OBJECT</td>
<td align="right"></td>
<td align="right">56,026,081</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CREATE_INIT_FRAME</td>
<td align="right"></td>
<td align="right">55,143,001</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_INIT_CHECK</td>
<td align="right"></td>
<td align="right">55,046,281</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_FOR</td>
<td align="right"></td>
<td align="right">36,251,360</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SEND_GEN_FRAME</td>
<td align="right"></td>
<td align="right">33,552,878</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right"></td>
<td align="right">21,669,505</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_COMMON_CONSTANT</td>
<td align="right"></td>
<td align="right">19,742,125</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_TYPE_1</td>
<td align="right"></td>
<td align="right">18,871,484</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right"></td>
<td align="right">17,778,639</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT</td>
<td align="right"></td>
<td align="right">17,046,994</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right"></td>
<td align="right">17,040,796</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_3</td>
<td align="right"></td>
<td align="right">13,141,207</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_2</td>
<td align="right"></td>
<td align="right">12,620,500</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right"></td>
<td align="right">12,128,677</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_PROPERTY_FRAME</td>
<td align="right"></td>
<td align="right">7,571,327</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_SEND</td>
<td align="right"></td>
<td align="right">7,198,215</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_STR_1</td>
<td align="right"></td>
<td align="right">6,073,517</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_AWAITABLE</td>
<td align="right"></td>
<td align="right">5,401,758</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right"></td>
<td align="right">5,361,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INSERT_NULL</td>
<td align="right"></td>
<td align="right">1,694,518</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SPECIAL</td>
<td align="right"></td>
<td align="right">1,694,518</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right"></td>
<td align="right">1,685,382</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right"></td>
<td align="right">1,198,439</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_METHOD_VERSION_KW</td>
<td align="right"></td>
<td align="right">764,011</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXPAND_METHOD_KW</td>
<td align="right"></td>
<td align="right">764,011</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_IMPORT_FROM</td>
<td align="right"></td>
<td align="right">742,028</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_EXCEPT</td>
<td align="right"></td>
<td align="right">30,721</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_TUPLE_1</td>
<td align="right"></td>
<td align="right">28,780</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_ATTR</td>
<td align="right"></td>
<td align="right">17,871</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right"></td>
<td align="right">14,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_EX</td>
<td align="right"></td>
<td align="right">13,456</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">620</td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### Pair counts

<details>
<summary> Pair counts for top 100 Non-JIT uop pairs </summary>


Pairs of specialized operations that deoptimize and are then followed by
the corresponding unspecialized instruction are not counted as pairs.

Not included in comparative output.


</details>

### Unsupported opcodes

<details>
<summary> unsupported opcodes </summary>

<table>
<thead>
<tr>
<th align="left">Opcode</th>
<th align="right">Base Count</th>
<th align="right">Head Count</th>
<th align="right">Change</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">23,767</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">23,001</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,830</td>
<td align="right"></td>
<td align="right"></td>
</tr>
</tbody>
</table>


</details>

### Optimizer errored out with opcode

<details>
<summary> Optimization stopped after encountering this opcode </summary>


</details>


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
watched dict modification
<details>
<summary>ⓘ</summary>

A watched dict has been modified
</details>
</td>
<td align="right">120</td>
<td align="right">286</td>
<td align="right">138.3%</td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
</details>
</td>
<td align="right">120</td>
<td align="right">286</td>
<td align="right">138.3%</td>
</tr>
<tr>
<td align="left">
set class
<details>
<summary>ⓘ</summary>

Setting an object's class, `obj.__class__ = ...`
</details>
</td>
<td align="right">22,592</td>
<td align="right">22,592</td>
<td align="right">0.0%</td>
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
<td align="right">22</td>
<td align="right">0.0%</td>
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
func modification
<details>
<summary>ⓘ</summary>

Modifying a function, e.g. `func.__defaults__ = ...`, etc.
</details>
</td>
<td align="right">313</td>
<td align="right">313</td>
<td align="right">0.0%</td>
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
<td align="right">2,436</td>
<td align="right">2,436</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-10-23
