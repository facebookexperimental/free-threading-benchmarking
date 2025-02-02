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
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">5,874,312,165</td>
<td align="right">7,797,008</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">112,686,473</td>
<td align="right">1,194,049</td>
<td align="right">-98.9%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">62,370,644</td>
<td align="right">2,090,483</td>
<td align="right">-96.6%</td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">100,136,760</td>
<td align="right">6,000,000</td>
<td align="right">-94.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">728,164,052</td>
<td align="right">52,312,837</td>
<td align="right">-92.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,450,775,519</td>
<td align="right">122,813,291</td>
<td align="right">-91.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">2,710,672,141</td>
<td align="right">270,162,843</td>
<td align="right">-90.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">2,237,564,964</td>
<td align="right">239,342,014</td>
<td align="right">-89.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,756,973,173</td>
<td align="right">190,235,592</td>
<td align="right">-89.2%</td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">1,744,969</td>
<td align="right">200,806</td>
<td align="right">-88.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">569,422,450</td>
<td align="right">71,283,553</td>
<td align="right">-87.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">201,837,793</td>
<td align="right">25,503,482</td>
<td align="right">-87.4%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,389,269,074</td>
<td align="right">186,669,662</td>
<td align="right">-86.6%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">514,292,075</td>
<td align="right">70,672,225</td>
<td align="right">-86.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">419,664,408</td>
<td align="right">58,116,973</td>
<td align="right">-86.2%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">2,122,180,050</td>
<td align="right">296,444,008</td>
<td align="right">-86.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,462,748,116</td>
<td align="right">491,597,232</td>
<td align="right">-85.8%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,229,654,404</td>
<td align="right">322,060,326</td>
<td align="right">-85.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,592,671,245</td>
<td align="right">231,814,425</td>
<td align="right">-85.4%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,222,215,502</td>
<td align="right">193,194,978</td>
<td align="right">-84.2%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">375,899,769</td>
<td align="right">61,902,576</td>
<td align="right">-83.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,636,847,323</td>
<td align="right">295,080,112</td>
<td align="right">-82.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">523,028,351</td>
<td align="right">94,927,585</td>
<td align="right">-81.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">2,475,493,735</td>
<td align="right">476,331,659</td>
<td align="right">-80.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">692,868,254</td>
<td align="right">133,549,162</td>
<td align="right">-80.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">353,332,408</td>
<td align="right">71,066,737</td>
<td align="right">-79.9%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">89,403,085</td>
<td align="right">18,132,478</td>
<td align="right">-79.7%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">156,807,834</td>
<td align="right">33,213,756</td>
<td align="right">-78.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">1,271,339,388</td>
<td align="right">269,396,405</td>
<td align="right">-78.8%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">7,359,764,734</td>
<td align="right">1,633,205,186</td>
<td align="right">-77.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,131,502,741</td>
<td align="right">251,860,720</td>
<td align="right">-77.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">2,877,470,952</td>
<td align="right">678,149,908</td>
<td align="right">-76.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">449,171,762</td>
<td align="right">109,459,704</td>
<td align="right">-75.6%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">649,707,132</td>
<td align="right">158,431,018</td>
<td align="right">-75.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST_MORTAL</td>
<td align="right">1,698,109,690</td>
<td align="right">416,561,379</td>
<td align="right">-75.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">158,442,495</td>
<td align="right">39,440,184</td>
<td align="right">-75.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">268,247,201</td>
<td align="right">67,353,369</td>
<td align="right">-74.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">1,082,071,733</td>
<td align="right">278,327,555</td>
<td align="right">-74.3%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">1,036,243,714</td>
<td align="right">267,099,949</td>
<td align="right">-74.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">544,315,867</td>
<td align="right">141,525,089</td>
<td align="right">-74.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">131,478,300</td>
<td align="right">34,241,977</td>
<td align="right">-74.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,832,952,722</td>
<td align="right">1,541,056,406</td>
<td align="right">-73.6%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">227,317,848</td>
<td align="right">60,391,249</td>
<td align="right">-73.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">562,999,950</td>
<td align="right">153,253,951</td>
<td align="right">-72.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,131,642,832</td>
<td align="right">314,438,324</td>
<td align="right">-72.2%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,550,274,586</td>
<td align="right">712,024,937</td>
<td align="right">-72.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">11,313,690,719</td>
<td align="right">3,172,257,753</td>
<td align="right">-72.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">788,832,695</td>
<td align="right">226,028,571</td>
<td align="right">-71.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">13,842,216,072</td>
<td align="right">3,966,678,503</td>
<td align="right">-71.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,562,433,044</td>
<td align="right">740,285,136</td>
<td align="right">-71.1%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">453,620,258</td>
<td align="right">133,585,554</td>
<td align="right">-70.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">11,000,842,014</td>
<td align="right">3,316,525,592</td>
<td align="right">-69.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">943,876,409</td>
<td align="right">285,049,857</td>
<td align="right">-69.8%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">57,644,934</td>
<td align="right">17,623,601</td>
<td align="right">-69.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">360,191,793</td>
<td align="right">110,312,779</td>
<td align="right">-69.4%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">76,723,029</td>
<td align="right">23,527,709</td>
<td align="right">-69.3%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">35,381,631</td>
<td align="right">11,094,125</td>
<td align="right">-68.6%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">116,449,482</td>
<td align="right">36,932,496</td>
<td align="right">-68.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">203,430,420</td>
<td align="right">65,189,024</td>
<td align="right">-68.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">275,857,290</td>
<td align="right">92,896,937</td>
<td align="right">-66.3%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">592,989,399</td>
<td align="right">206,149,984</td>
<td align="right">-65.2%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">531,806,253</td>
<td align="right">187,648,015</td>
<td align="right">-64.7%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">124,941,918</td>
<td align="right">44,151,648</td>
<td align="right">-64.7%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">63,719,695</td>
<td align="right">22,758,138</td>
<td align="right">-64.3%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,196,505,205</td>
<td align="right">444,688,829</td>
<td align="right">-62.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">38,568,672,590</td>
<td align="right">14,339,991,224</td>
<td align="right">-62.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">93,749,066</td>
<td align="right">35,050,895</td>
<td align="right">-62.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">815,117,404</td>
<td align="right">304,969,955</td>
<td align="right">-62.6%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">127,567,423</td>
<td align="right">48,937,920</td>
<td align="right">-61.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">94,184,560</td>
<td align="right">36,138,468</td>
<td align="right">-61.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">263,404,381</td>
<td align="right">102,983,709</td>
<td align="right">-60.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">239,240,909</td>
<td align="right">95,364,923</td>
<td align="right">-60.1%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">67,308,250</td>
<td align="right">26,881,798</td>
<td align="right">-60.1%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">805,818,729</td>
<td align="right">324,775,586</td>
<td align="right">-59.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">832,433,555</td>
<td align="right">335,630,181</td>
<td align="right">-59.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,178,822,435</td>
<td align="right">886,816,943</td>
<td align="right">-59.3%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">407,693,697</td>
<td align="right">166,140,644</td>
<td align="right">-59.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">404,032,282</td>
<td align="right">169,585,822</td>
<td align="right">-58.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">79,240,355</td>
<td align="right">33,270,369</td>
<td align="right">-58.0%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,156,327</td>
<td align="right">2,588,907</td>
<td align="right">-57.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST_IMMORTAL</td>
<td align="right">6,719,919,895</td>
<td align="right">2,877,180,835</td>
<td align="right">-57.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">94,297,882</td>
<td align="right">40,447,645</td>
<td align="right">-57.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">23,518,250</td>
<td align="right">10,301,250</td>
<td align="right">-56.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">285,129,200</td>
<td align="right">125,811,666</td>
<td align="right">-55.9%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,389,870,771</td>
<td align="right">627,970,027</td>
<td align="right">-54.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">335,657,715</td>
<td align="right">152,631,099</td>
<td align="right">-54.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">247,597,620</td>
<td align="right">113,861,002</td>
<td align="right">-54.0%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,577,606,138</td>
<td align="right">735,042,484</td>
<td align="right">-53.4%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">13,310,751</td>
<td align="right">6,418,284</td>
<td align="right">-51.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">344,837,064</td>
<td align="right">166,849,939</td>
<td align="right">-51.6%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">59,576,148</td>
<td align="right">28,907,588</td>
<td align="right">-51.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">394,121,685</td>
<td align="right">191,472,525</td>
<td align="right">-51.4%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,264,293,455</td>
<td align="right">619,818,643</td>
<td align="right">-51.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">5,298,069,026</td>
<td align="right">2,636,284,858</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">9,737,708</td>
<td align="right">4,861,928</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,667,176,546</td>
<td align="right">1,332,708,899</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,985,575,247</td>
<td align="right">1,992,456,790</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">185,963,506</td>
<td align="right">96,640,445</td>
<td align="right">-48.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">185,865,598</td>
<td align="right">98,024,115</td>
<td align="right">-47.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">294,481,733</td>
<td align="right">157,697,092</td>
<td align="right">-46.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,751,151,640</td>
<td align="right">938,180,499</td>
<td align="right">-46.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">3,424,231,266</td>
<td align="right">1,855,239,467</td>
<td align="right">-45.8%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">15,907,545</td>
<td align="right">8,694,686</td>
<td align="right">-45.3%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">190,778,222</td>
<td align="right">106,859,458</td>
<td align="right">-44.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">258,904,274</td>
<td align="right">148,261,340</td>
<td align="right">-42.7%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">117,219,055</td>
<td align="right">68,044,285</td>
<td align="right">-42.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,617,783,298</td>
<td align="right">3,974,909,823</td>
<td align="right">-39.9%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">182,883,065</td>
<td align="right">111,834,234</td>
<td align="right">-38.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,118,244,542</td>
<td align="right">683,892,141</td>
<td align="right">-38.8%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">100,216,327</td>
<td align="right">61,348,785</td>
<td align="right">-38.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">876,255,419</td>
<td align="right">537,142,084</td>
<td align="right">-38.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">354,303,775</td>
<td align="right">223,619,993</td>
<td align="right">-36.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,524,411,921</td>
<td align="right">2,228,437,227</td>
<td align="right">-36.8%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">858,134,993</td>
<td align="right">545,399,107</td>
<td align="right">-36.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">517,658,472</td>
<td align="right">335,698,361</td>
<td align="right">-35.2%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">96,402,685</td>
<td align="right">64,955,051</td>
<td align="right">-32.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">69,063,751</td>
<td align="right">47,797,381</td>
<td align="right">-30.8%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">334,255,608</td>
<td align="right">233,075,465</td>
<td align="right">-30.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">503,813,325</td>
<td align="right">359,763,428</td>
<td align="right">-28.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">195,700,555</td>
<td align="right">139,892,695</td>
<td align="right">-28.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">8,961,388</td>
<td align="right">6,438,893</td>
<td align="right">-28.1%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,327,516,517</td>
<td align="right">2,393,046,197</td>
<td align="right">-28.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">86,411,170</td>
<td align="right">63,248,043</td>
<td align="right">-26.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">594,513,011</td>
<td align="right">436,977,436</td>
<td align="right">-26.5%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">17,321,626</td>
<td align="right">13,013,298</td>
<td align="right">-24.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">163,270,811</td>
<td align="right">124,848,253</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,008,161,246</td>
<td align="right">784,422,555</td>
<td align="right">-22.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">1,685,920</td>
<td align="right">1,321,382</td>
<td align="right">-21.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">107,120,952</td>
<td align="right">84,257,553</td>
<td align="right">-21.3%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">141,425,273</td>
<td align="right">114,453,913</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">4,389,831</td>
<td align="right">3,659,059</td>
<td align="right">-16.6%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">255,461,333</td>
<td align="right">220,567,412</td>
<td align="right">-13.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,711,927,095</td>
<td align="right">5,002,609,612</td>
<td align="right">-12.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">76,242,971</td>
<td align="right">67,421,416</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">66,152,281</td>
<td align="right">58,746,088</td>
<td align="right">-11.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">344,653,169</td>
<td align="right">314,650,367</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">74,275,947</td>
<td align="right">68,466,037</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">74,905,001</td>
<td align="right">70,041,391</td>
<td align="right">-6.5%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">417,651,959</td>
<td align="right">392,218,822</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,758,056</td>
<td align="right">3,978,210</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">79,660,906</td>
<td align="right">75,058,339</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,147,058,482</td>
<td align="right">1,104,089,846</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">10,289,315</td>
<td align="right">9,959,527</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">61,733,889</td>
<td align="right">60,665,058</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">172,683,388</td>
<td align="right">170,068,018</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">1,666,364,596</td>
<td align="right">1,644,652,903</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">10,804,449</td>
<td align="right">10,704,333</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">68,031,223</td>
<td align="right">67,557,664</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">184,250,792</td>
<td align="right">183,443,440</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">91,536</td>
<td align="right">91,276</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">100,741,593</td>
<td align="right">100,537,234</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">315,288</td>
<td align="right">315,835</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">76,471</td>
<td align="right">76,570</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">1,705,649</td>
<td align="right">1,704,859</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">31,279</td>
<td align="right">31,266</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">6,465</td>
<td align="right">6,467</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">253,401,607</td>
<td align="right">253,471,221</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">10,173,396</td>
<td align="right">10,171,867</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,439,371</td>
<td align="right">128,424,289</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">119,945</td>
<td align="right">119,936</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">20,802,923</td>
<td align="right">20,804,412</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">21,145,409</td>
<td align="right">21,146,898</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">21,145,410</td>
<td align="right">21,146,899</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">14,737,110</td>
<td align="right">14,737,802</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">639,069</td>
<td align="right">639,094</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">302,086,306</td>
<td align="right">302,078,896</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">4,526,927</td>
<td align="right">4,526,944</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,160,274</td>
<td align="right">6,160,282</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_LINE</td>
<td align="right">58,270,440</td>
<td align="right">58,270,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">41,963,282</td>
<td align="right">41,963,282</td>
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
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">8,975,994</td>
<td align="right">8,975,994</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_ASYNC_FOR</td>
<td align="right">6,000,000</td>
<td align="right">6,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AITER</td>
<td align="right">6,000,000</td>
<td align="right">6,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">781,020</td>
<td align="right">781,020</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">80,787</td>
<td align="right">80,787</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">57,418</td>
<td align="right">57,418</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">52,020</td>
<td align="right">52,020</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">47,687</td>
<td align="right">47,687</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">25,191</td>
<td align="right">25,191</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">9,180</td>
<td align="right">9,180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">3,391</td>
<td align="right">3,391</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">3,346</td>
<td align="right">3,346</td>
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
<td align="right">2,390</td>
<td align="right">2,390</td>
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
<td align="right">24</td>
<td align="right">24</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right"></td>
<td align="right">2,128,297,119</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right"></td>
<td align="right">169,356,410</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right"></td>
<td align="right">16,785,846</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">7,743,722,970</td>
<td align="right">89.7%</td>
<td align="right">1,470,279,815</td>
<td align="right">79.2%</td>
<td align="right">-81.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">832,014,031</td>
<td align="right">9.6%</td>
<td align="right">335,469,070</td>
<td align="right">18.1%</td>
<td align="right">-59.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">52,895,801</td>
<td align="right">0.6%</td>
<td align="right">50,996,802</td>
<td align="right">2.7%</td>
<td align="right">-3.6%</td>
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
<td align="right">411,234</td>
<td align="right">29.0%</td>
<td align="right">152,796</td>
<td align="right">13.6%</td>
<td align="right">-62.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,006,273</td>
<td align="right">71.0%</td>
<td align="right">970,482</td>
<td align="right">86.4%</td>
<td align="right">-3.6%</td>
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
<td align="left">xor int</td>
<td align="right">85,540</td>
<td align="right">20.8%</td>
<td align="right">17,020</td>
<td align="right">11.1%</td>
<td align="right">-80.1%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">23,507</td>
<td align="right">5.7%</td>
<td align="right">5,454</td>
<td align="right">3.6%</td>
<td align="right">-76.8%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">11,587</td>
<td align="right">2.8%</td>
<td align="right">2,847</td>
<td align="right">1.9%</td>
<td align="right">-75.4%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">74,214</td>
<td align="right">18.0%</td>
<td align="right">18,473</td>
<td align="right">12.1%</td>
<td align="right">-75.1%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">8,202</td>
<td align="right">2.0%</td>
<td align="right">2,342</td>
<td align="right">1.5%</td>
<td align="right">-71.4%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">2,678</td>
<td align="right">0.7%</td>
<td align="right">836</td>
<td align="right">0.5%</td>
<td align="right">-68.8%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">19,438</td>
<td align="right">4.7%</td>
<td align="right">6,562</td>
<td align="right">4.3%</td>
<td align="right">-66.2%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">1,267</td>
<td align="right">0.3%</td>
<td align="right">510</td>
<td align="right">0.3%</td>
<td align="right">-59.7%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">43,851</td>
<td align="right">10.7%</td>
<td align="right">17,768</td>
<td align="right">11.6%</td>
<td align="right">-59.5%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">43,973</td>
<td align="right">10.7%</td>
<td align="right">18,643</td>
<td align="right">12.2%</td>
<td align="right">-57.6%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">8,507</td>
<td align="right">2.1%</td>
<td align="right">4,207</td>
<td align="right">2.8%</td>
<td align="right">-50.5%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">367</td>
<td align="right">0.1%</td>
<td align="right">187</td>
<td align="right">0.1%</td>
<td align="right">-49.0%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">34,149</td>
<td align="right">8.3%</td>
<td align="right">19,826</td>
<td align="right">13.0%</td>
<td align="right">-41.9%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">38,649</td>
<td align="right">9.4%</td>
<td align="right">24,455</td>
<td align="right">16.0%</td>
<td align="right">-36.7%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">7,194</td>
<td align="right">1.7%</td>
<td align="right">5,766</td>
<td align="right">3.8%</td>
<td align="right">-19.8%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">2,153</td>
<td align="right">0.5%</td>
<td align="right">1,961</td>
<td align="right">1.3%</td>
<td align="right">-8.9%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">1,387</td>
<td align="right">0.3%</td>
<td align="right">1,363</td>
<td align="right">0.9%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">626</td>
<td align="right">0.2%</td>
<td align="right">631</td>
<td align="right">0.4%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">3,147</td>
<td align="right">0.8%</td>
<td align="right">3,147</td>
<td align="right">2.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">or different types</td>
<td align="right">688</td>
<td align="right">0.2%</td>
<td align="right">688</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">90</td>
<td align="right">0.0%</td>
<td align="right">90</td>
<td align="right">0.1%</td>
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
<td align="right">185,963,506</td>
<td align="right">100.0%</td>
<td align="right">96,640,445</td>
<td align="right">100.0%</td>
<td align="right">-48.0%</td>
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
<td align="right">2,474,849,554</td>
<td align="right">30.9%</td>
<td align="right">476,176,529</td>
<td align="right">30.2%</td>
<td align="right">-80.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,515,908,912</td>
<td align="right">69.0%</td>
<td align="right">1,094,602,031</td>
<td align="right">69.4%</td>
<td align="right">-80.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">5,926,894</td>
<td align="right">0.1%</td>
<td align="right">5,830,117</td>
<td align="right">0.4%</td>
<td align="right">-1.6%</td>
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
<td align="right">636,400</td>
<td align="right">84.2%</td>
<td align="right">147,329</td>
<td align="right">55.6%</td>
<td align="right">-76.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">119,414</td>
<td align="right">15.8%</td>
<td align="right">117,594</td>
<td align="right">44.4%</td>
<td align="right">-1.5%</td>
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
<td align="left">list slice</td>
<td align="right">184,494</td>
<td align="right">29.0%</td>
<td align="right">7,084</td>
<td align="right">4.8%</td>
<td align="right">-96.2%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">28,573</td>
<td align="right">4.5%</td>
<td align="right">3,601</td>
<td align="right">2.4%</td>
<td align="right">-87.4%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">166,356</td>
<td align="right">26.1%</td>
<td align="right">24,073</td>
<td align="right">16.3%</td>
<td align="right">-85.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">190,036</td>
<td align="right">29.9%</td>
<td align="right">57,900</td>
<td align="right">39.3%</td>
<td align="right">-69.5%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">47,209</td>
<td align="right">7.4%</td>
<td align="right">35,167</td>
<td align="right">23.9%</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">972</td>
<td align="right">0.2%</td>
<td align="right">752</td>
<td align="right">0.5%</td>
<td align="right">-22.6%</td>
</tr>
<tr>
<td align="left">string slice</td>
<td align="right">3,461</td>
<td align="right">0.5%</td>
<td align="right">3,458</td>
<td align="right">2.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">12,278</td>
<td align="right">1.9%</td>
<td align="right">12,273</td>
<td align="right">8.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">2,940</td>
<td align="right">0.5%</td>
<td align="right">2,940</td>
<td align="right">2.0%</td>
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
<td align="left">array slice</td>
<td align="right">21</td>
<td align="right">0.0%</td>
<td align="right">21</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">11,443,355,153</td>
<td align="right">98.6%</td>
<td align="right">4,504,803,341</td>
<td align="right">97.1%</td>
<td align="right">-60.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">161,150,802</td>
<td align="right">1.4%</td>
<td align="right">134,622,287</td>
<td align="right">2.9%</td>
<td align="right">-16.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">152,070</td>
<td align="right">0.0%</td>
<td align="right">152,062</td>
<td align="right">0.0%</td>
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
<td align="right">21,673</td>
<td align="right">0.0%</td>
<td align="right">21,673</td>
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
<td align="right">3,202,421</td>
<td align="right">100.0%</td>
<td align="right">2,702,396</td>
<td align="right">100.0%</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">497</td>
<td align="right">0.0%</td>
<td align="right">497</td>
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
<td align="right">53.5%</td>
<td align="right">286</td>
<td align="right">57.5%</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">init not simple</td>
<td align="right">730</td>
<td align="right">146.9%</td>
<td align="right">730</td>
<td align="right">146.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">643</td>
<td align="right">129.4%</td>
<td align="right">643</td>
<td align="right">129.4%</td>
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
<td align="right">67,715</td>
<td align="right">10.9%</td>
<td align="right">67,715</td>
<td align="right">10.9%</td>
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
<td align="right">545,100</td>
<td align="right">87.7%</td>
<td align="right">545,100</td>
<td align="right">87.7%</td>
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
<td align="right">18,881</td>
<td align="right">99.2%</td>
<td align="right">18,980</td>
<td align="right">99.2%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">146</td>
<td align="right">0.8%</td>
<td align="right">146</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
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
<td align="right">522,788,067</td>
<td align="right">10.1%</td>
<td align="right">94,791,847</td>
<td align="right">8.3%</td>
<td align="right">-81.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,664,402,825</td>
<td align="right">89.9%</td>
<td align="right">1,048,416,872</td>
<td align="right">91.6%</td>
<td align="right">-77.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,439,927</td>
<td align="right">0.0%</td>
<td align="right">1,440,156</td>
<td align="right">0.1%</td>
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
<td align="right">218,571</td>
<td align="right">81.8%</td>
<td align="right">113,998</td>
<td align="right">70.0%</td>
<td align="right">-47.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">48,708</td>
<td align="right">18.2%</td>
<td align="right">48,742</td>
<td align="right">30.0%</td>
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
<td align="left">set</td>
<td align="right">6,810</td>
<td align="right">3.1%</td>
<td align="right">350</td>
<td align="right">0.3%</td>
<td align="right">-94.9%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">85,420</td>
<td align="right">39.1%</td>
<td align="right">4,562</td>
<td align="right">4.0%</td>
<td align="right">-94.7%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">2,020</td>
<td align="right">0.9%</td>
<td align="right">951</td>
<td align="right">0.8%</td>
<td align="right">-52.9%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">14,461</td>
<td align="right">6.6%</td>
<td align="right">7,841</td>
<td align="right">6.9%</td>
<td align="right">-45.8%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">14,797</td>
<td align="right">6.8%</td>
<td align="right">8,089</td>
<td align="right">7.1%</td>
<td align="right">-45.3%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">1,348</td>
<td align="right">0.6%</td>
<td align="right">1,247</td>
<td align="right">1.1%</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">46,227</td>
<td align="right">21.1%</td>
<td align="right">43,941</td>
<td align="right">38.5%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">971</td>
<td align="right">0.4%</td>
<td align="right">931</td>
<td align="right">0.8%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">30,737</td>
<td align="right">14.1%</td>
<td align="right">30,389</td>
<td align="right">26.7%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">7,763</td>
<td align="right">3.6%</td>
<td align="right">7,680</td>
<td align="right">6.7%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">7,631</td>
<td align="right">3.5%</td>
<td align="right">7,631</td>
<td align="right">6.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">386</td>
<td align="right">0.2%</td>
<td align="right">386</td>
<td align="right">0.3%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,208,067,145</td>
<td align="right">91.5%</td>
<td align="right">321,294,860</td>
<td align="right">82.6%</td>
<td align="right">-85.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">203,358,061</td>
<td align="right">8.4%</td>
<td align="right">65,150,462</td>
<td align="right">16.7%</td>
<td align="right">-68.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,526,286</td>
<td align="right">0.1%</td>
<td align="right">2,526,286</td>
<td align="right">0.6%</td>
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
<td align="right">70,484</td>
<td align="right">58.7%</td>
<td align="right">36,687</td>
<td align="right">42.5%</td>
<td align="right">-47.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">49,545</td>
<td align="right">41.3%</td>
<td align="right">49,545</td>
<td align="right">57.5%</td>
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
<td align="right">24,231</td>
<td align="right">34.4%</td>
<td align="right">9,159</td>
<td align="right">25.0%</td>
<td align="right">-62.2%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">23,240</td>
<td align="right">33.0%</td>
<td align="right">8,830</td>
<td align="right">24.1%</td>
<td align="right">-62.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">11,796</td>
<td align="right">16.7%</td>
<td align="right">7,901</td>
<td align="right">21.5%</td>
<td align="right">-33.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">11,217</td>
<td align="right">15.9%</td>
<td align="right">10,797</td>
<td align="right">29.4%</td>
<td align="right">-3.7%</td>
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
<td align="right">1,450,348,711</td>
<td align="right">27.8%</td>
<td align="right">122,717,663</td>
<td align="right">18.3%</td>
<td align="right">-91.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,593,614,250</td>
<td align="right">69.0%</td>
<td align="right">515,071,914</td>
<td align="right">76.9%</td>
<td align="right">-85.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">164,028,253</td>
<td align="right">3.1%</td>
<td align="right">31,969,028</td>
<td align="right">4.8%</td>
<td align="right">-80.5%</td>
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
<td align="right">3,100,326</td>
<td align="right">88.0%</td>
<td align="right">608,680</td>
<td align="right">87.1%</td>
<td align="right">-80.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">421,180</td>
<td align="right">12.0%</td>
<td align="right">89,998</td>
<td align="right">12.9%</td>
<td align="right">-78.6%</td>
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
<td align="left">string</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">161,898</td>
<td align="right">38.4%</td>
<td align="right">4,466</td>
<td align="right">5.0%</td>
<td align="right">-97.2%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">84,258</td>
<td align="right">20.0%</td>
<td align="right">3,114</td>
<td align="right">3.5%</td>
<td align="right">-96.3%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">35,048</td>
<td align="right">8.3%</td>
<td align="right">5,744</td>
<td align="right">6.4%</td>
<td align="right">-83.6%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">16,146</td>
<td align="right">3.8%</td>
<td align="right">2,710</td>
<td align="right">3.0%</td>
<td align="right">-83.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">12,373</td>
<td align="right">2.9%</td>
<td align="right">2,231</td>
<td align="right">2.5%</td>
<td align="right">-82.0%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">727</td>
<td align="right">0.2%</td>
<td align="right">167</td>
<td align="right">0.2%</td>
<td align="right">-77.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">1,120</td>
<td align="right">0.3%</td>
<td align="right">280</td>
<td align="right">0.3%</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">3,091</td>
<td align="right">0.7%</td>
<td align="right">1,391</td>
<td align="right">1.5%</td>
<td align="right">-55.0%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">3,950</td>
<td align="right">0.9%</td>
<td align="right">1,927</td>
<td align="right">2.1%</td>
<td align="right">-51.2%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">19,333</td>
<td align="right">4.6%</td>
<td align="right">10,601</td>
<td align="right">11.8%</td>
<td align="right">-45.2%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">4,624</td>
<td align="right">1.1%</td>
<td align="right">2,829</td>
<td align="right">3.1%</td>
<td align="right">-38.8%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">6,879</td>
<td align="right">1.6%</td>
<td align="right">4,554</td>
<td align="right">5.1%</td>
<td align="right">-33.8%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">71,542</td>
<td align="right">17.0%</td>
<td align="right">49,813</td>
<td align="right">55.3%</td>
<td align="right">-30.4%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">171</td>
<td align="right">0.0%</td>
<td align="right">131</td>
<td align="right">0.1%</td>
<td align="right">-23.4%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">13,059,220,336</td>
<td align="right">88.1%</td>
<td align="right">5,944,795,383</td>
<td align="right">83.4%</td>
<td align="right">-54.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">874,429,862</td>
<td align="right">5.9%</td>
<td align="right">535,546,992</td>
<td align="right">7.5%</td>
<td align="right">-38.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">879,866,326</td>
<td align="right">5.9%</td>
<td align="right">649,539,073</td>
<td align="right">9.1%</td>
<td align="right">-26.2%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,858,759</td>
<td align="right">0.0%</td>
<td align="right">1,858,759</td>
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
<td align="right">562,052</td>
<td align="right">3.3%</td>
<td align="right">345,433</td>
<td align="right">2.7%</td>
<td align="right">-38.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">16,677,239</td>
<td align="right">96.7%</td>
<td align="right">12,332,693</td>
<td align="right">97.3%</td>
<td align="right">-26.1%</td>
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
<td align="right">80,303</td>
<td align="right">14.3%</td>
<td align="right">40,210</td>
<td align="right">11.6%</td>
<td align="right">-49.9%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">61,415</td>
<td align="right">10.9%</td>
<td align="right">36,913</td>
<td align="right">10.7%</td>
<td align="right">-39.9%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">1,159</td>
<td align="right">0.2%</td>
<td align="right">829</td>
<td align="right">0.2%</td>
<td align="right">-28.5%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">5,975</td>
<td align="right">1.1%</td>
<td align="right">4,727</td>
<td align="right">1.4%</td>
<td align="right">-20.9%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">17,977</td>
<td align="right">3.2%</td>
<td align="right">15,392</td>
<td align="right">4.5%</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">9,146</td>
<td align="right">1.6%</td>
<td align="right">7,970</td>
<td align="right">2.3%</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">2,726</td>
<td align="right">0.5%</td>
<td align="right">2,396</td>
<td align="right">0.7%</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">68,642</td>
<td align="right">12.2%</td>
<td align="right">61,531</td>
<td align="right">17.8%</td>
<td align="right">-10.4%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1,752</td>
<td align="right">0.3%</td>
<td align="right">1,584</td>
<td align="right">0.5%</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">25,195</td>
<td align="right">4.5%</td>
<td align="right">23,447</td>
<td align="right">6.8%</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">525</td>
<td align="right">0.1%</td>
<td align="right">523</td>
<td align="right">0.2%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">5,009</td>
<td align="right">0.9%</td>
<td align="right">5,009</td>
<td align="right">1.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">4,485</td>
<td align="right">0.8%</td>
<td align="right">4,485</td>
<td align="right">1.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">1,101</td>
<td align="right">0.2%</td>
<td align="right">1,101</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">400</td>
<td align="right">0.1%</td>
<td align="right">400</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">180</td>
<td align="right">0.0%</td>
<td align="right">180</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">160</td>
<td align="right">0.0%</td>
<td align="right">160</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property not py function</td>
<td align="right">55</td>
<td align="right">0.0%</td>
<td align="right">55</td>
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
<td align="right">9,357,323,257</td>
<td align="right">99.8%</td>
<td align="right">3,769,452,278</td>
<td align="right">99.6%</td>
<td align="right">-59.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">41,386</td>
<td align="right">0.0%</td>
<td align="right">41,355</td>
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
<td align="right">14,611,930</td>
<td align="right">0.2%</td>
<td align="right">14,611,919</td>
<td align="right">0.4%</td>
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
<td align="right">1,399</td>
<td align="right">0.0%</td>
<td align="right">1,399</td>
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
<td align="right">125,901</td>
<td align="right">100.0%</td>
<td align="right">126,604</td>
<td align="right">100.0%</td>
<td align="right">0.6%</td>
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
<td align="right">66,260,816</td>
<td align="right">100.0%</td>
<td align="right">65,192,002</td>
<td align="right">100.0%</td>
<td align="right">-1.6%</td>
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
<td align="right">2,268</td>
<td align="right">100.0%</td>
<td align="right">2,268</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">592,974,688</td>
<td align="right">82.2%</td>
<td align="right">206,135,273</td>
<td align="right">61.6%</td>
<td align="right">-65.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">128,405,102</td>
<td align="right">17.8%</td>
<td align="right">128,390,022</td>
<td align="right">38.4%</td>
<td align="right">-0.0%</td>
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
<td align="right">33,933</td>
<td align="right">98.2%</td>
<td align="right">33,931</td>
<td align="right">98.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">608</td>
<td align="right">1.8%</td>
<td align="right">608</td>
<td align="right">1.8%</td>
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
<td align="left">list</td>
<td align="right">2,925</td>
<td align="right">8.6%</td>
<td align="right">2,923</td>
<td align="right">8.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">async generator send</td>
<td align="right">24,440</td>
<td align="right">72.0%</td>
<td align="right">24,440</td>
<td align="right">72.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">5,948</td>
<td align="right">17.5%</td>
<td align="right">5,948</td>
<td align="right">17.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">620</td>
<td align="right">1.8%</td>
<td align="right">620</td>
<td align="right">1.8%</td>
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
<td align="right">2,015,440,157</td>
<td align="right">91.1%</td>
<td align="right">1,358,115,150</td>
<td align="right">87.9%</td>
<td align="right">-32.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">76,148,970</td>
<td align="right">3.4%</td>
<td align="right">67,329,318</td>
<td align="right">4.4%</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">119,941,625</td>
<td align="right">5.4%</td>
<td align="right">119,175,540</td>
<td align="right">7.7%</td>
<td align="right">-0.6%</td>
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
<td align="right">54,256</td>
<td align="right">2.3%</td>
<td align="right">52,007</td>
<td align="right">2.2%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,302,316</td>
<td align="right">97.7%</td>
<td align="right">2,288,223</td>
<td align="right">97.8%</td>
<td align="right">-0.6%</td>
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
<td align="right">265,956</td>
<td align="right">490.2%</td>
<td align="right">129,387</td>
<td align="right">248.8%</td>
<td align="right">-51.4%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">6,352</td>
<td align="right">11.7%</td>
<td align="right">4,989</td>
<td align="right">9.6%</td>
<td align="right">-21.5%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">787</td>
<td align="right">1.5%</td>
<td align="right">743</td>
<td align="right">1.4%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">5,364</td>
<td align="right">9.9%</td>
<td align="right">5,144</td>
<td align="right">9.9%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">25,869</td>
<td align="right">47.7%</td>
<td align="right">25,268</td>
<td align="right">48.6%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">2,992</td>
<td align="right">5.5%</td>
<td align="right">2,971</td>
<td align="right">5.7%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">7,735</td>
<td align="right">14.3%</td>
<td align="right">7,735</td>
<td align="right">14.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">1,614</td>
<td align="right">3.0%</td>
<td align="right">1,614</td>
<td align="right">3.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">876</td>
<td align="right">1.6%</td>
<td align="right">876</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">762</td>
<td align="right">1.4%</td>
<td align="right">762</td>
<td align="right">1.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">311</td>
<td align="right">0.6%</td>
<td align="right">311</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">101</td>
<td align="right">0.2%</td>
<td align="right">101</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">94</td>
<td align="right">0.2%</td>
<td align="right">94</td>
<td align="right">0.2%</td>
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
<td align="right">112,686,473</td>
<td align="right">100.0%</td>
<td align="right">1,194,049</td>
<td align="right">100.0%</td>
<td align="right">-98.9%</td>
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
<td align="right">692,685,002</td>
<td align="right">42.7%</td>
<td align="right">133,502,480</td>
<td align="right">42.4%</td>
<td align="right">-80.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">929,612,023</td>
<td align="right">57.3%</td>
<td align="right">181,594,112</td>
<td align="right">57.6%</td>
<td align="right">-80.5%</td>
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
<td align="right">180,276</td>
<td align="right">98.4%</td>
<td align="right">43,700</td>
<td align="right">93.5%</td>
<td align="right">-75.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,016</td>
<td align="right">1.6%</td>
<td align="right">3,022</td>
<td align="right">6.5%</td>
<td align="right">0.2%</td>
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
<td align="right">81,221</td>
<td align="right">45.1%</td>
<td align="right">320</td>
<td align="right">0.7%</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">5,256</td>
<td align="right">2.9%</td>
<td align="right">213</td>
<td align="right">0.5%</td>
<td align="right">-95.9%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">52,368</td>
<td align="right">29.0%</td>
<td align="right">8,143</td>
<td align="right">18.6%</td>
<td align="right">-84.5%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">1,675</td>
<td align="right">0.9%</td>
<td align="right">475</td>
<td align="right">1.1%</td>
<td align="right">-71.6%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">19,337</td>
<td align="right">10.7%</td>
<td align="right">14,750</td>
<td align="right">33.8%</td>
<td align="right">-23.7%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">17,333</td>
<td align="right">9.6%</td>
<td align="right">16,713</td>
<td align="right">38.2%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">3,018</td>
<td align="right">1.7%</td>
<td align="right">3,018</td>
<td align="right">6.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">array slice</td>
<td align="right">68</td>
<td align="right">0.0%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">116,749,674</td>
<td align="right">2.2%</td>
<td align="right">42,301,034</td>
<td align="right">1.6%</td>
<td align="right">-63.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">262,727,537</td>
<td align="right">5.0%</td>
<td align="right">102,531,569</td>
<td align="right">4.0%</td>
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
<td align="right">4,894,687,662</td>
<td align="right">92.8%</td>
<td align="right">2,445,483,992</td>
<td align="right">94.4%</td>
<td align="right">-50.0%</td>
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
<td align="right">2,251,005</td>
<td align="right">78.2%</td>
<td align="right">846,437</td>
<td align="right">67.8%</td>
<td align="right">-62.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">627,420</td>
<td align="right">21.8%</td>
<td align="right">402,614</td>
<td align="right">32.2%</td>
<td align="right">-35.8%</td>
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
<td align="right">130,385</td>
<td align="right">20.8%</td>
<td align="right">13,737</td>
<td align="right">3.4%</td>
<td align="right">-89.5%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">16,018</td>
<td align="right">2.6%</td>
<td align="right">1,738</td>
<td align="right">0.4%</td>
<td align="right">-89.1%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">77,191</td>
<td align="right">12.3%</td>
<td align="right">8,381</td>
<td align="right">2.1%</td>
<td align="right">-89.1%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">10,036</td>
<td align="right">1.6%</td>
<td align="right">6,005</td>
<td align="right">1.5%</td>
<td align="right">-40.2%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">19,121</td>
<td align="right">3.0%</td>
<td align="right">12,113</td>
<td align="right">3.0%</td>
<td align="right">-36.7%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">97,351</td>
<td align="right">15.5%</td>
<td align="right">86,720</td>
<td align="right">21.5%</td>
<td align="right">-10.9%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">12,872</td>
<td align="right">2.1%</td>
<td align="right">11,924</td>
<td align="right">3.0%</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">263,980</td>
<td align="right">42.1%</td>
<td align="right">261,530</td>
<td align="right">65.0%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">382</td>
<td align="right">0.1%</td>
<td align="right">382</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">memory view</td>
<td align="right">84</td>
<td align="right">0.0%</td>
<td align="right">84</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,255,231,921</td>
<td align="right">99.9%</td>
<td align="right">397,701,176</td>
<td align="right">99.7%</td>
<td align="right">-68.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,673,651</td>
<td align="right">0.1%</td>
<td align="right">1,309,164</td>
<td align="right">0.3%</td>
<td align="right">-21.8%</td>
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
<td align="right">3,700</td>
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
<td align="right">949</td>
<td align="right">7.7%</td>
<td align="right">838</td>
<td align="right">6.8%</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">11,400</td>
<td align="right">92.3%</td>
<td align="right">11,460</td>
<td align="right">93.2%</td>
<td align="right">0.5%</td>
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
<td align="right">726</td>
<td align="right">76.5%</td>
<td align="right">615</td>
<td align="right">73.4%</td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">132</td>
<td align="right">13.9%</td>
<td align="right">132</td>
<td align="right">15.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">91</td>
<td align="right">9.6%</td>
<td align="right">91</td>
<td align="right">10.9%</td>
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
<td align="right">7,837,839,134</td>
<td align="right">3.6%</td>
<td align="right">2,178,700,873</td>
<td align="right">2.6%</td>
<td align="right">-72.2%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">89,553,829,540</td>
<td align="right">41.3%</td>
<td align="right">31,400,838,487</td>
<td align="right">37.9%</td>
<td align="right">-64.9%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">118,091,255,439</td>
<td align="right">54.4%</td>
<td align="right">48,163,926,486</td>
<td align="right">58.2%</td>
<td align="right">-59.2%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,505,260,581</td>
<td align="right">0.7%</td>
<td align="right">1,039,167,809</td>
<td align="right">1.3%</td>
<td align="right">-31.0%</td>
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
<td align="right">1,450,348,711</td>
<td align="right">18.5%</td>
<td align="right">122,717,663</td>
<td align="right">5.6%</td>
<td align="right">-91.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">522,788,067</td>
<td align="right">6.7%</td>
<td align="right">94,791,847</td>
<td align="right">4.4%</td>
<td align="right">-81.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">2,474,849,554</td>
<td align="right">31.6%</td>
<td align="right">476,176,529</td>
<td align="right">21.9%</td>
<td align="right">-80.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">692,685,002</td>
<td align="right">8.8%</td>
<td align="right">133,502,480</td>
<td align="right">6.1%</td>
<td align="right">-80.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">262,727,537</td>
<td align="right">3.4%</td>
<td align="right">102,531,569</td>
<td align="right">4.7%</td>
<td align="right">-61.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">832,014,031</td>
<td align="right">10.6%</td>
<td align="right">335,469,070</td>
<td align="right">15.4%</td>
<td align="right">-59.7%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">185,963,506</td>
<td align="right">2.4%</td>
<td align="right">96,640,445</td>
<td align="right">4.4%</td>
<td align="right">-48.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">874,429,862</td>
<td align="right">11.2%</td>
<td align="right">535,546,992</td>
<td align="right">24.6%</td>
<td align="right">-38.8%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,405,102</td>
<td align="right">1.6%</td>
<td align="right">128,390,022</td>
<td align="right">5.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">203,358,061</td>
<td align="right">2.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">67,329,318</td>
<td align="right">3.1%</td>
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
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">270,863,850</td>
<td align="right">18.0%</td>
<td align="right">188,554,175</td>
<td align="right">18.1%</td>
<td align="right">-30.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">371,469,608</td>
<td align="right">24.7%</td>
<td align="right">259,325,447</td>
<td align="right">25.0%</td>
<td align="right">-30.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">92,960,863</td>
<td align="right">6.2%</td>
<td align="right">76,357,802</td>
<td align="right">7.3%</td>
<td align="right">-17.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">86,790,255</td>
<td align="right">5.8%</td>
<td align="right">73,055,096</td>
<td align="right">7.0%</td>
<td align="right">-15.8%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">85,776,919</td>
<td align="right">5.7%</td>
<td align="right">72,798,389</td>
<td align="right">7.0%</td>
<td align="right">-15.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">95,104,319</td>
<td align="right">6.3%</td>
<td align="right">95,073,714</td>
<td align="right">9.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">82,001,921</td>
<td align="right">5.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">81,898,738</td>
<td align="right">5.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">57,259,460</td>
<td align="right">3.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">51,473,974</td>
<td align="right">3.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">24,414,483</td>
<td align="right">2.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">24,066,314</td>
<td align="right">2.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">21,242,743</td>
<td align="right">2.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">20,872,297</td>
<td align="right">2.0%</td>
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
<td align="right">4,273,302</td>
<td align="right">0.1%</td>
<td align="right">2,128,107</td>
<td align="right">0.0%</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">141,112,048</td>
<td align="right">2.0%</td>
<td align="right">132,513,115</td>
<td align="right">1.9%</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">73,565,189</td>
<td align="right">1.0%</td>
<td align="right">71,988,643</td>
<td align="right">1.0%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">5,393,912,548</td>
<td align="right">76.3%</td>
<td align="right">5,294,747,349</td>
<td align="right">76.2%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">5,768,930,419</td>
<td align="right">81.7%</td>
<td align="right">5,691,303,453</td>
<td align="right">82.0%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">962,171,208</td>
<td align="right">13.6%</td>
<td align="right">949,737,127</td>
<td align="right">13.7%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">1,670,840,208</td>
<td align="right">23.7%</td>
<td align="right">1,649,348,664</td>
<td align="right">23.8%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">1,670,840,208</td>
<td align="right">23.7%</td>
<td align="right">1,649,348,664</td>
<td align="right">23.8%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">708,669,000</td>
<td align="right">10.0%</td>
<td align="right">699,611,537</td>
<td align="right">10.1%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">957,894,515</td>
<td align="right">13.6%</td>
<td align="right">947,605,629</td>
<td align="right">13.6%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">276,239,589</td>
<td align="right">3.9%</td>
<td align="right">276,170,278</td>
<td align="right">4.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">24,960,304</td>
<td align="right">0.4%</td>
<td align="right">24,959,372</td>
<td align="right">0.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">262,333,890</td>
<td align="right">3.7%</td>
<td align="right">262,333,982</td>
<td align="right">3.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">3,391</td>
<td align="right">0.0%</td>
<td align="right">3,391</td>
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
<td align="left">Method cache dunder misses</td>
<td align="right">8,082,575</td>
<td align="right"></td>
<td align="right">9,176,450</td>
<td align="right"></td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">4,978,085</td>
<td align="right">2.6%</td>
<td align="right">4,312,485</td>
<td align="right">2.2%</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">28,174,598,784</td>
<td align="right">17.8%</td>
<td align="right">25,952,855,965</td>
<td align="right">16.2%</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">82,167,996,604</td>
<td align="right">52.0%</td>
<td align="right">87,846,879,791</td>
<td align="right">54.7%</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">2,373,012,632</td>
<td align="right"></td>
<td align="right">2,216,210,756</td>
<td align="right"></td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">91,760,445,886</td>
<td align="right">47.0%</td>
<td align="right">96,852,247,670</td>
<td align="right">48.1%</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">73,251,171</td>
<td align="right"></td>
<td align="right">76,311,802</td>
<td align="right"></td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">46,351,445,755</td>
<td align="right">23.7%</td>
<td align="right">47,968,296,010</td>
<td align="right">23.8%</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">65,975,828</td>
<td align="right"></td>
<td align="right">67,939,119</td>
<td align="right"></td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">12,563,021,193</td>
<td align="right">67.1%</td>
<td align="right">12,248,116,807</td>
<td align="right">66.7%</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">12,563,142,594</td>
<td align="right"></td>
<td align="right">12,248,247,409</td>
<td align="right"></td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">25,502,945,030</td>
<td align="right">16.1%</td>
<td align="right">25,025,392,060</td>
<td align="right">15.6%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">22,205,832,307</td>
<td align="right">14.0%</td>
<td align="right">21,860,716,622</td>
<td align="right">13.6%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">24,083,576,219</td>
<td align="right">12.3%</td>
<td align="right">23,788,993,983</td>
<td align="right">11.8%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">6,092,240,319</td>
<td align="right">32.5%</td>
<td align="right">6,041,313,772</td>
<td align="right">32.9%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">6,170,634,583</td>
<td align="right">32.9%</td>
<td align="right">6,119,753,747</td>
<td align="right">33.3%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">6,745,562,829</td>
<td align="right"></td>
<td align="right">6,691,094,442</td>
<td align="right"></td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">33,162,757,970</td>
<td align="right">17.0%</td>
<td align="right">32,921,943,884</td>
<td align="right">16.3%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">2,870,567,401</td>
<td align="right"></td>
<td align="right">2,851,404,143</td>
<td align="right"></td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">195,004,621</td>
<td align="right"></td>
<td align="right">194,323,092</td>
<td align="right"></td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">6,712,251</td>
<td align="right">0.0%</td>
<td align="right">6,706,550</td>
<td align="right">0.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">71,682,013</td>
<td align="right">0.4%</td>
<td align="right">71,733,425</td>
<td align="right">0.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">410,620</td>
<td align="right">0.2%</td>
<td align="right">410,620</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">4,406</td>
<td align="right">0.0%</td>
<td align="right">4,406</td>
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
<td align="right">360,041</td>
<td align="right">106,211,298</td>
<td align="right">9,657,083,388</td>
<td align="right">782,845,994</td>
<td align="right">757,008,931</td>
<td align="right">358,879</td>
<td align="right">106,111,311</td>
<td align="right">9,709,359,089</td>
<td align="right">794,510,843</td>
<td align="right">755,893,052</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">15,998</td>
<td align="right">8,734,437</td>
<td align="right">11,218,999,484</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">15,998</td>
<td align="right">8,734,437</td>
<td align="right">11,219,502,802</td>
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
<td align="right">29</td>
<td align="right">29</td>
<td align="right">0.0%</td>
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
<td align="right">160</td>
<td align="right">160 / 0 !!</td>
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
<td align="right">160</td>
<td align="right">160 / 0 !!</td>
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
<td align="right">2,474</td>
<td align="right">2,474</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-02-02
