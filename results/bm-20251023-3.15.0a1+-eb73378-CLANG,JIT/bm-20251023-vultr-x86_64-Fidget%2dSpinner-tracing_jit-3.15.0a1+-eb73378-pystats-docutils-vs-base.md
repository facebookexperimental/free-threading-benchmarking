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
<td align="right">39,693,120</td>
<td align="right">111,627,760</td>
<td align="right">181.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">3,757,340</td>
<td align="right">7,410,940</td>
<td align="right">97.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">89,804,620</td>
<td align="right">12,089,240</td>
<td align="right">-86.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">4,426,260</td>
<td align="right">1,032,620</td>
<td align="right">-76.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">1,656,400</td>
<td align="right">496,040</td>
<td align="right">-70.1%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">5,736,660</td>
<td align="right">1,866,760</td>
<td align="right">-67.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">20,550,680</td>
<td align="right">7,916,200</td>
<td align="right">-61.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">2,437,080</td>
<td align="right">1,033,400</td>
<td align="right">-57.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">108,292,220</td>
<td align="right">47,894,140</td>
<td align="right">-55.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">41,711,700</td>
<td align="right">20,980,820</td>
<td align="right">-49.7%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">7,143,540</td>
<td align="right">3,703,900</td>
<td align="right">-48.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">11,201,240</td>
<td align="right">16,527,260</td>
<td align="right">47.5%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">37,133,580</td>
<td align="right">19,502,520</td>
<td align="right">-47.5%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">36,888,420</td>
<td align="right">19,539,800</td>
<td align="right">-47.0%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">116,243,760</td>
<td align="right">72,519,900</td>
<td align="right">-37.6%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">740,040</td>
<td align="right">513,960</td>
<td align="right">-30.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">4,587,740</td>
<td align="right">3,312,740</td>
<td align="right">-27.8%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">77,527,020</td>
<td align="right">56,212,320</td>
<td align="right">-27.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">92,500</td>
<td align="right">67,400</td>
<td align="right">-27.1%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">8,029,860</td>
<td align="right">5,855,020</td>
<td align="right">-27.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">848,400</td>
<td align="right">622,320</td>
<td align="right">-26.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">22,890,520</td>
<td align="right">16,964,100</td>
<td align="right">-25.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">17,957,580</td>
<td align="right">13,359,680</td>
<td align="right">-25.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">759,540</td>
<td align="right">566,340</td>
<td align="right">-25.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">190,512,060</td>
<td align="right">144,331,100</td>
<td align="right">-24.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">3,844,240</td>
<td align="right">4,769,140</td>
<td align="right">24.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">62,678,740</td>
<td align="right">47,709,500</td>
<td align="right">-23.9%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">16,742,180</td>
<td align="right">12,849,060</td>
<td align="right">-23.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">142,157,240</td>
<td align="right">109,285,940</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">120,119,560</td>
<td align="right">93,104,600</td>
<td align="right">-22.5%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">555,060</td>
<td align="right">672,120</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">177,991,420</td>
<td align="right">142,136,280</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">188,694,800</td>
<td align="right">152,183,700</td>
<td align="right">-19.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">46,146,740</td>
<td align="right">37,307,500</td>
<td align="right">-19.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">201,266,780</td>
<td align="right">162,720,600</td>
<td align="right">-19.2%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">29,083,780</td>
<td align="right">23,606,140</td>
<td align="right">-18.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">204,258,020</td>
<td align="right">166,010,320</td>
<td align="right">-18.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">304,087,740</td>
<td align="right">247,656,160</td>
<td align="right">-18.6%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">26,373,000</td>
<td align="right">21,642,340</td>
<td align="right">-17.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">300,590,040</td>
<td align="right">247,567,700</td>
<td align="right">-17.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">93,091,660</td>
<td align="right">76,959,900</td>
<td align="right">-17.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">34,738,840</td>
<td align="right">28,771,620</td>
<td align="right">-17.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">9,479,340</td>
<td align="right">7,876,560</td>
<td align="right">-16.9%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">32,099,340</td>
<td align="right">26,830,240</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">75,563,280</td>
<td align="right">63,195,540</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">115,324,400</td>
<td align="right">96,575,760</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">295,286,640</td>
<td align="right">247,636,440</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">51,263,940</td>
<td align="right">43,082,740</td>
<td align="right">-16.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">9,028,200</td>
<td align="right">7,606,000</td>
<td align="right">-15.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">200,301,080</td>
<td align="right">170,334,960</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">18,634,140</td>
<td align="right">21,374,600</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,279,510,040</td>
<td align="right">1,091,678,320</td>
<td align="right">-14.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">8,364,240</td>
<td align="right">7,161,500</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">99,040,900</td>
<td align="right">85,241,380</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">19,460,540</td>
<td align="right">16,871,380</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">7,892,960</td>
<td align="right">6,918,820</td>
<td align="right">-12.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">373,064,780</td>
<td align="right">328,135,080</td>
<td align="right">-12.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">4,822,960</td>
<td align="right">4,263,900</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">309,022,920</td>
<td align="right">274,938,380</td>
<td align="right">-11.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">2,915,540</td>
<td align="right">3,206,280</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">5,783,840</td>
<td align="right">5,210,920</td>
<td align="right">-9.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">2,526,360</td>
<td align="right">2,776,480</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">149,000</td>
<td align="right">135,180</td>
<td align="right">-9.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">4,526,080</td>
<td align="right">4,941,620</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">19,928,960</td>
<td align="right">18,170,980</td>
<td align="right">-8.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">10,351,780</td>
<td align="right">11,252,980</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">16,809,420</td>
<td align="right">15,367,700</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">18,808,220</td>
<td align="right">17,195,600</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">22,086,080</td>
<td align="right">20,197,420</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">16,542,640</td>
<td align="right">15,152,980</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">21,795,920</td>
<td align="right">20,004,200</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">5,112,620</td>
<td align="right">4,702,060</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">14,262,520</td>
<td align="right">13,133,880</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">45,207,800</td>
<td align="right">41,736,040</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">9,620,400</td>
<td align="right">8,911,180</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">106,803,820</td>
<td align="right">99,169,300</td>
<td align="right">-7.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">12,003,400</td>
<td align="right">11,165,600</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">34,634,100</td>
<td align="right">36,986,160</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">4,979,940</td>
<td align="right">4,660,840</td>
<td align="right">-6.4%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">4,671,180</td>
<td align="right">4,967,220</td>
<td align="right">6.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">32,274,140</td>
<td align="right">34,122,120</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">51,444,520</td>
<td align="right">48,512,260</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,947,960</td>
<td align="right">1,837,860</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">3,546,580</td>
<td align="right">3,708,380</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">20,433,280</td>
<td align="right">19,531,120</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">15,116,580</td>
<td align="right">14,453,080</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">49,223,240</td>
<td align="right">47,069,220</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">30,067,200</td>
<td align="right">28,880,900</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">30,084,840</td>
<td align="right">28,898,540</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">50,772,540</td>
<td align="right">52,762,820</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">1,131,740</td>
<td align="right">1,175,000</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">703,080</td>
<td align="right">677,660</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">2,840,660</td>
<td align="right">2,740,640</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">7,120,100</td>
<td align="right">7,362,080</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">26,760,120</td>
<td align="right">27,622,120</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">24,461,940</td>
<td align="right">23,765,880</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">23,212,940</td>
<td align="right">22,587,820</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">1,444,900</td>
<td align="right">1,410,240</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">4,202,460</td>
<td align="right">4,133,600</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">73,580,540</td>
<td align="right">72,504,720</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">20,542,720</td>
<td align="right">20,245,540</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">2,031,240</td>
<td align="right">2,002,100</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">19,214,480</td>
<td align="right">18,975,940</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">1,846,620</td>
<td align="right">1,823,980</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">11,367,340</td>
<td align="right">11,240,160</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">2,363,880</td>
<td align="right">2,390,280</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">3,960</td>
<td align="right">4,000</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">24,240</td>
<td align="right">24,000</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">8,611,380</td>
<td align="right">8,528,580</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">10,296,240</td>
<td align="right">10,200,100</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">35,958,580</td>
<td align="right">35,655,400</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">1,697,480</td>
<td align="right">1,686,120</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">9,511,020</td>
<td align="right">9,448,280</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">27,457,860</td>
<td align="right">27,331,900</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">38,709,740</td>
<td align="right">38,882,320</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">61,740</td>
<td align="right">61,580</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">3,427,780</td>
<td align="right">3,420,180</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">7,613,760</td>
<td align="right">7,613,140</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">11,627,520</td>
<td align="right">11,627,520</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">6,143,580</td>
<td align="right">6,143,580</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">6,143,580</td>
<td align="right">6,143,580</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">5,787,480</td>
<td align="right">5,787,480</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">2,731,500</td>
<td align="right">2,731,500</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">2,728,440</td>
<td align="right">2,728,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">1,413,900</td>
<td align="right">1,413,900</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">1,175,460</td>
<td align="right">1,175,460</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">896,340</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">440,400</td>
<td align="right">440,400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">351,240</td>
<td align="right">351,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">267,120</td>
<td align="right">267,120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">228,720</td>
<td align="right">228,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">213,240</td>
<td align="right">213,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">176,880</td>
<td align="right">176,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">156,900</td>
<td align="right">156,900</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">145,320</td>
<td align="right">145,320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">82,320</td>
<td align="right">82,320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">75,960</td>
<td align="right">75,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">73,620</td>
<td align="right">73,620</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">61,740</td>
<td align="right">61,740</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">56,040</td>
<td align="right">56,040</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">49,980</td>
<td align="right">49,980</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">25,680</td>
<td align="right">25,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">14,700</td>
<td align="right">14,700</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">14,640</td>
<td align="right">14,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">11,400</td>
<td align="right">11,400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">7,260</td>
<td align="right">7,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">5,880</td>
<td align="right">5,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">5,880</td>
<td align="right">5,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">5,880</td>
<td align="right">5,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">4,740</td>
<td align="right">4,740</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">3,420</td>
<td align="right">3,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">3,360</td>
<td align="right">3,360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">2,940</td>
<td align="right">2,940</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">2,940</td>
<td align="right">2,940</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">1,920</td>
<td align="right">1,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">1,440</td>
<td align="right">1,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">1,440</td>
<td align="right">1,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">780</td>
<td align="right">780</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">720</td>
<td align="right">720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">300</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">300</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">300</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">240</td>
<td align="right">240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">240</td>
<td align="right">240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FROM_DICT_OR_DEREF</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">60</td>
<td align="right">60</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">5,018,400</td>
<td align="right">2.6%</td>
<td align="right">4,098,720</td>
<td align="right">2.1%</td>
<td align="right">-18.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">23,107,040</td>
<td align="right">11.8%</td>
<td align="right">22,508,260</td>
<td align="right">11.6%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">167,468,520</td>
<td align="right">85.6%</td>
<td align="right">167,298,420</td>
<td align="right">86.2%</td>
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
<td align="right">540</td>
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
<td align="right">105,060</td>
<td align="right">52.4%</td>
<td align="right">78,700</td>
<td align="right">50.1%</td>
<td align="right">-25.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">95,500</td>
<td align="right">47.6%</td>
<td align="right">78,520</td>
<td align="right">49.9%</td>
<td align="right">-17.8%</td>
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
<td align="left">remainder</td>
<td align="right">4,980</td>
<td align="right">4.7%</td>
<td align="right">6,660</td>
<td align="right">8.5%</td>
<td align="right">33.7%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">84,680</td>
<td align="right">80.6%</td>
<td align="right">56,720</td>
<td align="right">72.1%</td>
<td align="right">-33.0%</td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">320</td>
<td align="right">0.3%</td>
<td align="right">360</td>
<td align="right">0.5%</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">3,220</td>
<td align="right">3.1%</td>
<td align="right">3,380</td>
<td align="right">4.3%</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">8,080</td>
<td align="right">7.7%</td>
<td align="right">7,780</td>
<td align="right">9.9%</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">3,160</td>
<td align="right">3.0%</td>
<td align="right">3,180</td>
<td align="right">4.0%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">240</td>
<td align="right">0.2%</td>
<td align="right">240</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">180</td>
<td align="right">0.2%</td>
<td align="right">180</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">100</td>
<td align="right">0.1%</td>
<td align="right">100</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr counter</td>
<td align="right">80</td>
<td align="right">0.1%</td>
<td align="right">80</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">true divide other</td>
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
<td align="right">10,296,240</td>
<td align="right">100.0%</td>
<td align="right">10,200,100</td>
<td align="right">100.0%</td>
<td align="right">-0.9%</td>
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
<td align="right">16,996,980</td>
<td align="right">3.0%</td>
<td align="right">16,235,360</td>
<td align="right">2.8%</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">17,323,680</td>
<td align="right">3.0%</td>
<td align="right">16,550,660</td>
<td align="right">2.9%</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">554,203,880</td>
<td align="right">97.0%</td>
<td align="right">554,435,600</td>
<td align="right">97.1%</td>
<td align="right">0.0%</td>
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
<td align="right">5,280</td>
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
<td align="left">Success</td>
<td align="right">330,660</td>
<td align="right">100.0%</td>
<td align="right">319,300</td>
<td align="right">100.0%</td>
<td align="right">-3.4%</td>
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
<td align="right">160</td>
<td align="right">160 / 0 !!</td>
<td align="right">160</td>
<td align="right">160 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">20</td>
<td align="right">20 / 0 !!</td>
<td align="right">20</td>
<td align="right">20 / 0 !!</td>
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
<td align="right">300</td>
<td align="right">100.0%</td>
<td align="right">300</td>
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
<td align="right">256,600</td>
<td align="right">0.7%</td>
<td align="right">171,700</td>
<td align="right">0.5%</td>
<td align="right">-33.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,683,960</td>
<td align="right">4.6%</td>
<td align="right">1,675,800</td>
<td align="right">4.6%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">34,788,120</td>
<td align="right">94.7%</td>
<td align="right">34,718,120</td>
<td align="right">94.9%</td>
<td align="right">-0.2%</td>
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
<td align="right">5,180</td>
<td align="right">28.2%</td>
<td align="right">3,580</td>
<td align="right">26.4%</td>
<td align="right">-30.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">13,180</td>
<td align="right">71.8%</td>
<td align="right">9,980</td>
<td align="right">73.6%</td>
<td align="right">-24.3%</td>
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
<td align="left">different types</td>
<td align="right">12,720</td>
<td align="right">96.5%</td>
<td align="right">9,500</td>
<td align="right">95.2%</td>
<td align="right">-25.3%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">80</td>
<td align="right">0.6%</td>
<td align="right">100</td>
<td align="right">1.0%</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">200</td>
<td align="right">1.5%</td>
<td align="right">200</td>
<td align="right">2.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">80</td>
<td align="right">0.6%</td>
<td align="right">80</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">40</td>
<td align="right">0.3%</td>
<td align="right">40</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">40</td>
<td align="right">0.3%</td>
<td align="right">40</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">20</td>
<td align="right">0.2%</td>
<td align="right">20</td>
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
<td align="right">8,025,120</td>
<td align="right">12.9%</td>
<td align="right">5,845,940</td>
<td align="right">9.7%</td>
<td align="right">-27.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">54,353,340</td>
<td align="right">87.1%</td>
<td align="right">54,353,340</td>
<td align="right">90.3%</td>
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
<td align="right">4,620</td>
<td align="right">97.5%</td>
<td align="right">8,960</td>
<td align="right">98.7%</td>
<td align="right">93.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">120</td>
<td align="right">2.5%</td>
<td align="right">120</td>
<td align="right">1.3%</td>
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
<td align="left">tuple</td>
<td align="right">1,160</td>
<td align="right">25.1%</td>
<td align="right">2,660</td>
<td align="right">29.7%</td>
<td align="right">129.3%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">1,800</td>
<td align="right">39.0%</td>
<td align="right">3,940</td>
<td align="right">44.0%</td>
<td align="right">118.9%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">860</td>
<td align="right">18.6%</td>
<td align="right">1,520</td>
<td align="right">17.0%</td>
<td align="right">76.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">800</td>
<td align="right">17.3%</td>
<td align="right">840</td>
<td align="right">9.4%</td>
<td align="right">5.0%</td>
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
<td align="right">20,544,760</td>
<td align="right">9.9%</td>
<td align="right">7,853,440</td>
<td align="right">6.2%</td>
<td align="right">-61.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">32,767,260</td>
<td align="right">15.8%</td>
<td align="right">19,531,100</td>
<td align="right">15.3%</td>
<td align="right">-40.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">154,412,580</td>
<td align="right">74.3%</td>
<td align="right">99,878,860</td>
<td align="right">78.4%</td>
<td align="right">-35.3%</td>
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
<td align="right">51,040</td>
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
<td align="right">5,920</td>
<td align="right">0.9%</td>
<td align="right">62,760</td>
<td align="right">13.1%</td>
<td align="right">960.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">618,240</td>
<td align="right">99.1%</td>
<td align="right">415,680</td>
<td align="right">86.9%</td>
<td align="right">-32.8%</td>
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
<td align="left">seq iter</td>
<td align="right">560</td>
<td align="right">9.5%</td>
<td align="right">27,880</td>
<td align="right">44.4%</td>
<td align="right">4,878.6%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">1,000</td>
<td align="right">16.9%</td>
<td align="right">28,480</td>
<td align="right">45.4%</td>
<td align="right">2,748.0%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">320</td>
<td align="right">5.4%</td>
<td align="right">1,620</td>
<td align="right">2.6%</td>
<td align="right">406.2%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">220</td>
<td align="right">3.7%</td>
<td align="right">1,040</td>
<td align="right">1.7%</td>
<td align="right">372.7%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">320</td>
<td align="right">5.4%</td>
<td align="right">840</td>
<td align="right">1.3%</td>
<td align="right">162.5%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">1,260</td>
<td align="right">21.3%</td>
<td align="right">2,280</td>
<td align="right">3.6%</td>
<td align="right">81.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">2,040</td>
<td align="right">34.5%</td>
<td align="right">460</td>
<td align="right">0.7%</td>
<td align="right">-77.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">40</td>
<td align="right">0.7%</td>
<td align="right">40</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">40</td>
<td align="right">0.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">40</td>
<td align="right">0.7%</td>
<td align="right">40</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">40</td>
<td align="right">0.7%</td>
<td align="right">40</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">40</td>
<td align="right">0.7%</td>
<td align="right">40</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
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
<td align="left">enumerate</td>
<td align="right">2,162,220</td>
<td align="right">2,162,220 / 0 !!</td>
<td align="right">2,160,320</td>
<td align="right">2,160,320 / 0 !!</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">48,398,760</td>
<td align="right">48,398,760 / 0 !!</td>
<td align="right">48,395,280</td>
<td align="right">48,395,280 / 0 !!</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">36,919,140</td>
<td align="right">36,919,140 / 0 !!</td>
<td align="right">36,919,000</td>
<td align="right">36,919,000 / 0 !!</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">29,118,840</td>
<td align="right">29,118,840 / 0 !!</td>
<td align="right">29,118,840</td>
<td align="right">29,118,840 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">5,964,960</td>
<td align="right">5,964,960 / 0 !!</td>
<td align="right">5,964,960</td>
<td align="right">5,964,960 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">200,280</td>
<td align="right">200,280 / 0 !!</td>
<td align="right">200,280</td>
<td align="right">200,280 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">198,000</td>
<td align="right">198,000 / 0 !!</td>
<td align="right">198,000</td>
<td align="right">198,000 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">55,380</td>
<td align="right">55,380 / 0 !!</td>
<td align="right">55,380</td>
<td align="right">55,380 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">3,900</td>
<td align="right">3,900 / 0 !!</td>
<td align="right">3,900</td>
<td align="right">3,900 / 0 !!</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">264,323,240</td>
<td align="right">26.1%</td>
<td align="right">220,147,720</td>
<td align="right">23.3%</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">98,386,820</td>
<td align="right">9.7%</td>
<td align="right">84,604,760</td>
<td align="right">9.0%</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">647,981,620</td>
<td align="right">64.1%</td>
<td align="right">639,227,140</td>
<td align="right">67.7%</td>
<td align="right">-1.4%</td>
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
<td align="right">157,180</td>
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
<td align="right">21,960</td>
<td align="right">0.4%</td>
<td align="right">280,040</td>
<td align="right">6.3%</td>
<td align="right">1,175.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">4,928,360</td>
<td align="right">99.6%</td>
<td align="right">4,189,160</td>
<td align="right">93.7%</td>
<td align="right">-15.0%</td>
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
<td align="right">4,800</td>
<td align="right">21.9%</td>
<td align="right">257,000</td>
<td align="right">91.8%</td>
<td align="right">5,254.2%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">2,840</td>
<td align="right">12.9%</td>
<td align="right">4,400</td>
<td align="right">1.6%</td>
<td align="right">54.9%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">9,200</td>
<td align="right">41.9%</td>
<td align="right">13,440</td>
<td align="right">4.8%</td>
<td align="right">46.1%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">240</td>
<td align="right">1.1%</td>
<td align="right">300</td>
<td align="right">0.1%</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">400</td>
<td align="right">1.8%</td>
<td align="right">380</td>
<td align="right">0.1%</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">640</td>
<td align="right">2.9%</td>
<td align="right">660</td>
<td align="right">0.2%</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">1,760</td>
<td align="right">8.0%</td>
<td align="right">1,760</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">420</td>
<td align="right">1.9%</td>
<td align="right">420</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">220</td>
<td align="right">1.0%</td>
<td align="right">220</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">180</td>
<td align="right">0.8%</td>
<td align="right">180</td>
<td align="right">0.1%</td>
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
<td align="right">264,443,040</td>
<td align="right">100.0%</td>
<td align="right">237,536,400</td>
<td align="right">100.0%</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,140</td>
<td align="right">0.0%</td>
<td align="right">2,140</td>
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
<td align="right">1,960</td>
<td align="right">100.0%</td>
<td align="right">1,960</td>
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
<td align="right">75,960</td>
<td align="right">100.0%</td>
<td align="right">75,960</td>
<td align="right">100.0%</td>
<td align="right">0.0%</td>
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
<td align="right">7,260</td>
<td align="right">100.0%</td>
<td align="right">7,260</td>
<td align="right">100.0%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">53,795,560</td>
<td align="right">43.7%</td>
<td align="right">40,722,660</td>
<td align="right">34.1%</td>
<td align="right">-24.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">47,186,000</td>
<td align="right">38.3%</td>
<td align="right">58,491,200</td>
<td align="right">49.0%</td>
<td align="right">24.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">22,072,080</td>
<td align="right">17.9%</td>
<td align="right">20,148,940</td>
<td align="right">16.9%</td>
<td align="right">-8.7%</td>
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
<td align="right">9,900</td>
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
<td align="right">13,600</td>
<td align="right">1.3%</td>
<td align="right">48,080</td>
<td align="right">5.8%</td>
<td align="right">253.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,015,660</td>
<td align="right">98.7%</td>
<td align="right">773,880</td>
<td align="right">94.2%</td>
<td align="right">-23.8%</td>
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
<td align="right">10,940</td>
<td align="right">80.4%</td>
<td align="right">45,200</td>
<td align="right">94.0%</td>
<td align="right">313.2%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">200</td>
<td align="right">1.5%</td>
<td align="right">440</td>
<td align="right">0.9%</td>
<td align="right">120.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">340</td>
<td align="right">2.5%</td>
<td align="right">420</td>
<td align="right">0.9%</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">2,040</td>
<td align="right">15.0%</td>
<td align="right">1,940</td>
<td align="right">4.0%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">1,000</td>
<td align="right">7.4%</td>
<td align="right">1,020</td>
<td align="right">2.1%</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">40</td>
<td align="right">0.3%</td>
<td align="right">40</td>
<td align="right">0.1%</td>
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
<td align="right">267,120</td>
<td align="right">100.0%</td>
<td align="right">267,120</td>
<td align="right">100.0%</td>
<td align="right">0.0%</td>
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
<td align="right">4,583,860</td>
<td align="right">9.7%</td>
<td align="right">3,308,320</td>
<td align="right">7.2%</td>
<td align="right">-27.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">42,562,200</td>
<td align="right">90.3%</td>
<td align="right">42,562,200</td>
<td align="right">92.8%</td>
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
<td align="right">3,760</td>
<td align="right">95.9%</td>
<td align="right">4,300</td>
<td align="right">96.4%</td>
<td align="right">14.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">160</td>
<td align="right">4.1%</td>
<td align="right">160</td>
<td align="right">3.6%</td>
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
<td align="left">py simple</td>
<td align="right">2,440</td>
<td align="right">64.9%</td>
<td align="right">2,820</td>
<td align="right">65.6%</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">1,060</td>
<td align="right">28.2%</td>
<td align="right">1,220</td>
<td align="right">28.4%</td>
<td align="right">15.1%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">220</td>
<td align="right">5.9%</td>
<td align="right">220</td>
<td align="right">5.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">40</td>
<td align="right">1.1%</td>
<td align="right">40</td>
<td align="right">0.9%</td>
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
<td align="right">7,911,300</td>
<td align="right">3.0%</td>
<td align="right">9,495,500</td>
<td align="right">3.7%</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">3,373,940</td>
<td align="right">1.3%</td>
<td align="right">3,541,100</td>
<td align="right">1.4%</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">253,397,060</td>
<td align="right">95.7%</td>
<td align="right">245,497,800</td>
<td align="right">94.9%</td>
<td align="right">-3.1%</td>
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
<td align="right">2,940</td>
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
<td align="left">Success</td>
<td align="right">150,060</td>
<td align="right">46.6%</td>
<td align="right">181,600</td>
<td align="right">52.2%</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">171,780</td>
<td align="right">53.4%</td>
<td align="right">166,420</td>
<td align="right">47.8%</td>
<td align="right">-3.1%</td>
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
<td align="left">mapping</td>
<td align="right">1,860</td>
<td align="right">1.1%</td>
<td align="right">2,060</td>
<td align="right">1.2%</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">41,520</td>
<td align="right">24.2%</td>
<td align="right">38,880</td>
<td align="right">23.4%</td>
<td align="right">-6.4%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">126,960</td>
<td align="right">73.9%</td>
<td align="right">124,020</td>
<td align="right">74.5%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">1,260</td>
<td align="right">0.7%</td>
<td align="right">1,280</td>
<td align="right">0.8%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">160</td>
<td align="right">0.1%</td>
<td align="right">160</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">20</td>
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
<td align="right">48,300,460</td>
<td align="right">100.0%</td>
<td align="right">48,297,740</td>
<td align="right">100.0%</td>
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
<td align="left">Success</td>
<td align="right">380</td>
<td align="right">100.0%</td>
<td align="right">380</td>
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
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">2,340,298,240</td>
<td align="right">34.5%</td>
<td align="right">1,894,487,880</td>
<td align="right">33.2%</td>
<td align="right">-19.0%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">313,441,660</td>
<td align="right">4.6%</td>
<td align="right">254,083,420</td>
<td align="right">4.5%</td>
<td align="right">-18.9%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">381,410,880</td>
<td align="right">5.6%</td>
<td align="right">310,731,580</td>
<td align="right">5.4%</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">3,747,823,600</td>
<td align="right">55.3%</td>
<td align="right">3,243,899,480</td>
<td align="right">56.9%</td>
<td align="right">-13.4%</td>
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
<td align="right">20,544,760</td>
<td align="right">9.8%</td>
<td align="right">7,853,440</td>
<td align="right">4.5%</td>
<td align="right">-61.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">4,583,860</td>
<td align="right">2.2%</td>
<td align="right">3,308,320</td>
<td align="right">1.9%</td>
<td align="right">-27.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">8,025,120</td>
<td align="right">3.8%</td>
<td align="right">5,845,940</td>
<td align="right">3.3%</td>
<td align="right">-27.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">98,386,820</td>
<td align="right">47.0%</td>
<td align="right">84,604,760</td>
<td align="right">48.0%</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">22,072,080</td>
<td align="right">10.5%</td>
<td align="right">20,148,940</td>
<td align="right">11.4%</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">3,373,940</td>
<td align="right">1.6%</td>
<td align="right">3,541,100</td>
<td align="right">2.0%</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">16,996,980</td>
<td align="right">8.1%</td>
<td align="right">16,235,360</td>
<td align="right">9.2%</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">23,107,040</td>
<td align="right">11.0%</td>
<td align="right">22,508,260</td>
<td align="right">12.8%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">10,296,240</td>
<td align="right">4.9%</td>
<td align="right">10,200,100</td>
<td align="right">5.8%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">1,683,960</td>
<td align="right">0.8%</td>
<td align="right">1,675,800</td>
<td align="right">1.0%</td>
<td align="right">-0.5%</td>
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
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">16,383,240</td>
<td align="right">4.3%</td>
<td align="right">9,724,580</td>
<td align="right">3.1%</td>
<td align="right">-40.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">16,384,020</td>
<td align="right">4.3%</td>
<td align="right">9,806,520</td>
<td align="right">3.2%</td>
<td align="right">-40.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">53,792,380</td>
<td align="right">14.1%</td>
<td align="right">40,719,480</td>
<td align="right">13.1%</td>
<td align="right">-24.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">45,153,700</td>
<td align="right">11.8%</td>
<td align="right">34,441,700</td>
<td align="right">11.1%</td>
<td align="right">-23.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">82,021,200</td>
<td align="right">21.5%</td>
<td align="right">64,708,720</td>
<td align="right">20.8%</td>
<td align="right">-21.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">4,487,480</td>
<td align="right">1.2%</td>
<td align="right">5,278,140</td>
<td align="right">1.7%</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">99,061,240</td>
<td align="right">26.0%</td>
<td align="right">86,609,220</td>
<td align="right">27.9%</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">27,959,780</td>
<td align="right">7.3%</td>
<td align="right">24,917,760</td>
<td align="right">8.0%</td>
<td align="right">-10.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">9,618,560</td>
<td align="right">2.5%</td>
<td align="right">8,601,260</td>
<td align="right">2.8%</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">7,587,480</td>
<td align="right">2.0%</td>
<td align="right">7,168,340</td>
<td align="right">2.3%</td>
<td align="right">-5.5%</td>
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
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">8,448,120</td>
<td align="right">2.4%</td>
<td align="right">8,696,440</td>
<td align="right">2.5%</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">39,405,500</td>
<td align="right">11.1%</td>
<td align="right">39,578,080</td>
<td align="right">11.2%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">39,408,980</td>
<td align="right">11.1%</td>
<td align="right">39,581,560</td>
<td align="right">11.2%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">39,752,120</td>
<td align="right">11.2%</td>
<td align="right">39,924,700</td>
<td align="right">11.3%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">39,752,120</td>
<td align="right">11.2%</td>
<td align="right">39,924,700</td>
<td align="right">11.3%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">314,781,760</td>
<td align="right">88.8%</td>
<td align="right">314,530,240</td>
<td align="right">88.7%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">313,603,520</td>
<td align="right">88.5%</td>
<td align="right">313,600,300</td>
<td align="right">88.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">13,627,720</td>
<td align="right">3.8%</td>
<td align="right">13,627,660</td>
<td align="right">3.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">343,140</td>
<td align="right">0.1%</td>
<td align="right">343,140</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">3,420</td>
<td align="right">0.0%</td>
<td align="right">3,420</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">1,826,760</td>
<td align="right">0.5%</td>
<td align="right">1,826,760</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">9,607,200</td>
<td align="right">2.7%</td>
<td align="right">9,607,200</td>
<td align="right">2.7%</td>
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
<td align="right">1,825,296</td>
<td align="right"></td>
<td align="right">2,182,947</td>
<td align="right"></td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">1,407,131,220</td>
<td align="right">27.2%</td>
<td align="right">1,185,910,660</td>
<td align="right">23.2%</td>
<td align="right">-15.7%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">2,182,000,586</td>
<td align="right">42.2%</td>
<td align="right">2,389,039,897</td>
<td align="right">46.7%</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">449,003,482</td>
<td align="right"></td>
<td align="right">407,425,631</td>
<td align="right"></td>
<td align="right">-9.3%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">2,095,332,340</td>
<td align="right">38.5%</td>
<td align="right">1,915,326,000</td>
<td align="right">35.6%</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">2,000,079,629</td>
<td align="right">36.7%</td>
<td align="right">2,166,547,296</td>
<td align="right">40.2%</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">491,540</td>
<td align="right">0.1%</td>
<td align="right">519,400</td>
<td align="right">0.1%</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">36,888,079</td>
<td align="right"></td>
<td align="right">38,837,596</td>
<td align="right"></td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">175,455,920</td>
<td align="right">3.4%</td>
<td align="right">167,496,120</td>
<td align="right">3.3%</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">35,824,198</td>
<td align="right"></td>
<td align="right">37,356,509</td>
<td align="right"></td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">1,256,352,819</td>
<td align="right">23.1%</td>
<td align="right">1,213,946,876</td>
<td align="right">22.5%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">1,411,655,114</td>
<td align="right">27.3%</td>
<td align="right">1,370,654,609</td>
<td align="right">26.8%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">344,660</td>
<td align="right">0.1%</td>
<td align="right">354,320</td>
<td align="right">0.1%</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">91,428,840</td>
<td align="right">1.7%</td>
<td align="right">89,290,920</td>
<td align="right">1.7%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">191,355,124</td>
<td align="right"></td>
<td align="right">189,260,613</td>
<td align="right"></td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">325,720,796</td>
<td align="right"></td>
<td align="right">326,489,756</td>
<td align="right"></td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">10,543,020</td>
<td align="right"></td>
<td align="right">10,541,160</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">300,826,380</td>
<td align="right">50.9%</td>
<td align="right">300,775,140</td>
<td align="right">50.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">300,852,680</td>
<td align="right"></td>
<td align="right">300,808,840</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">288,901,440</td>
<td align="right">48.9%</td>
<td align="right">288,863,120</td>
<td align="right">48.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">289,737,640</td>
<td align="right">49.1%</td>
<td align="right">289,736,840</td>
<td align="right">49.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">26,460</td>
<td align="right">0.3%</td>
<td align="right">26,460</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">120,780</td>
<td align="right">1.1%</td>
<td align="right">120,780</td>
<td align="right">1.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">2,940</td>
<td align="right">0.0%</td>
<td align="right">2,940</td>
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
<td align="right">25,860</td>
<td align="right">73,030,100</td>
<td align="right">1,171,692,171</td>
<td align="right">41,961,563</td>
<td align="right">102,670,077</td>
<td align="right">25,860</td>
<td align="right">73,426,540</td>
<td align="right">1,183,943,700</td>
<td align="right">41,760,820</td>
<td align="right">103,228,960</td>
</tr>
<tr>
<td align="right">2</td>
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
<td align="right">29,820</td>
<td align="right"></td>
<td align="right">5,080,260</td>
<td align="right"></td>
<td align="right">16,936.4%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">340</td>
<td align="right">1.1%</td>
<td align="right">2,660</td>
<td align="right">0.1%</td>
<td align="right">682.4%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">7,320</td>
<td align="right">24.5%</td>
<td align="right">42,820</td>
<td align="right">0.8%</td>
<td align="right">485.0%</td>
</tr>
<tr>
<td align="left">
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
</details>
</td>
<td align="right">60</td>
<td align="right">0.2%</td>
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
<td align="right">7,000</td>
<td align="right">23.5%</td>
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
<td align="right">920</td>
<td align="right">3.1%</td>
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
<td align="right">140</td>
<td align="right">0.5%</td>
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
<td align="right">40</td>
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
<td align="right">14,520</td>
<td align="right">48.7%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">262,995,880</td>
<td align="right"></td>
<td align="right">521,172,180</td>
<td align="right"></td>
<td align="right">98.2%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">5,084,175,420</td>
<td align="right">1,933.2%</td>
<td align="right">9,078,823,020</td>
<td align="right">1,742.0%</td>
<td align="right">78.6%</td>
</tr>
<tr>
<td align="left">
Trace too long
<details>
<summary>ⓘ</summary>

A trace is truncated because it is longer than the instruction buffer.
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">520</td>
<td align="right">0.0%</td>
<td align="right">520 / 0 !!</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
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
<td align="right">4,720</td>
<td align="right">64.5%</td>
<td align="right">42,240</td>
<td align="right">98.6%</td>
<td align="right">794.9%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">7,320</td>
<td align="right"></td>
<td align="right">42,820</td>
<td align="right"></td>
<td align="right">485.0%</td>
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
Code size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the code of the JIT traces
</details>
</td>
<td align="right">32,532,320</td>
<td align="right">75.9%</td>
<td align="right">456,768,680</td>
<td align="right">83.2%</td>
<td align="right">1,304.0%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">42,844,160</td>
<td align="right"></td>
<td align="right">549,109,760</td>
<td align="right"></td>
<td align="right">1,181.6%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">740,480</td>
<td align="right">1.7%</td>
<td align="right">9,129,280</td>
<td align="right">1.7%</td>
<td align="right">1,132.9%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">9,566,640</td>
<td align="right">22.3%</td>
<td align="right">83,169,560</td>
<td align="right">15.1%</td>
<td align="right">769.4%</td>
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
<tr>
<td align="left">
Freed memory size
<details>
<summary>ⓘ</summary>

The size of the memory freed from the JIT traces
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">108,216,320</td>
<td align="right">19.7%</td>
<td align="right">108,216,320 / 0 !!</td>
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
<td align="left">1,720</td>
<td align="right">36.4%</td>
<td align="left">13,900</td>
<td align="right">32.9%</td>
<td align="right">708.1%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">1,980</td>
<td align="right">41.9%</td>
<td align="left">10,940</td>
<td align="right">25.9%</td>
<td align="right">452.5%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">540</td>
<td align="right">11.4%</td>
<td align="left">10,120</td>
<td align="right">24.0%</td>
<td align="right">1,774.1%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">420</td>
<td align="right">8.9%</td>
<td align="left">4,800</td>
<td align="right">11.4%</td>
<td align="right">1,042.9%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left">60</td>
<td align="right">1.3%</td>
<td align="left">1,780</td>
<td align="right">4.2%</td>
<td align="right">2,866.7%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">700</td>
<td align="right">1.7%</td>
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
<td align="left"><= 16</td>
<td align="right">40</td>
<td align="right">0.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">1,060</td>
<td align="right">14.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">2,420</td>
<td align="right">33.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">580</td>
<td align="right">7.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">2,960</td>
<td align="right">40.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">260</td>
<td align="right">3.6%</td>
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
<td align="left"><= 16</td>
<td align="right">380</td>
<td align="right">5.2%</td>
<td align="right">5,300</td>
<td align="right">12.4%</td>
<td align="right">1,294.7%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">1,980</td>
<td align="right">27.0%</td>
<td align="right">11,360</td>
<td align="right">26.5%</td>
<td align="right">473.7%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">1,600</td>
<td align="right">21.9%</td>
<td align="right">12,560</td>
<td align="right">29.3%</td>
<td align="right">685.0%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">280</td>
<td align="right">3.8%</td>
<td align="right">6,800</td>
<td align="right">15.9%</td>
<td align="right">2,328.6%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">420</td>
<td align="right">5.7%</td>
<td align="right">4,440</td>
<td align="right">10.4%</td>
<td align="right">957.1%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">60</td>
<td align="right">0.8%</td>
<td align="right">1,100</td>
<td align="right">2.6%</td>
<td align="right">1,733.3%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">660</td>
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
<td align="left">_BINARY_OP</td>
<td align="right">1,320</td>
<td align="right">1,445,500</td>
<td align="right">109,407.6%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">18,740</td>
<td align="right">4,287,440</td>
<td align="right">22,778.5%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">187,100</td>
<td align="right">20,545,320</td>
<td align="right">10,880.9%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">270,260</td>
<td align="right">14,634,320</td>
<td align="right">5,314.9%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">270,260</td>
<td align="right">14,634,320</td>
<td align="right">5,314.9%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right">1,054,040</td>
<td align="right">35,109,200</td>
<td align="right">3,230.9%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">46,580</td>
<td align="right">1,436,240</td>
<td align="right">2,983.4%</td>
</tr>
<tr>
<td align="left">_CALL_KW_NON_PY</td>
<td align="right">1,220</td>
<td align="right">35,880</td>
<td align="right">2,841.0%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE_KW</td>
<td align="right">1,220</td>
<td align="right">35,880</td>
<td align="right">2,841.0%</td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right">396,780</td>
<td align="right">9,266,640</td>
<td align="right">2,235.5%</td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right">187,840</td>
<td align="right">4,173,620</td>
<td align="right">2,121.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">1,730,720</td>
<td align="right">36,990,180</td>
<td align="right">2,037.3%</td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right">2,464,380</td>
<td align="right">46,182,720</td>
<td align="right">1,774.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">363,240</td>
<td align="right">5,236,340</td>
<td align="right">1,341.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">187,840</td>
<td align="right">2,695,760</td>
<td align="right">1,335.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NULL</td>
<td align="right">187,100</td>
<td align="right">2,528,080</td>
<td align="right">1,251.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right">304,040</td>
<td align="right">3,721,580</td>
<td align="right">1,124.0%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,861,320</td>
<td align="right">21,423,960</td>
<td align="right">1,051.0%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">2,803,920</td>
<td align="right">29,495,600</td>
<td align="right">951.9%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">2,901,920</td>
<td align="right">29,911,360</td>
<td align="right">930.7%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">140,700</td>
<td align="right">1,327,000</td>
<td align="right">843.1%</td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">140,700</td>
<td align="right">1,327,000</td>
<td align="right">843.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">1,280</td>
<td align="right">11,620</td>
<td align="right">807.8%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">457,900</td>
<td align="right">3,991,380</td>
<td align="right">771.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION_AND_LOCK</td>
<td align="right">1,897,620</td>
<td align="right">15,891,540</td>
<td align="right">737.4%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">183,560</td>
<td align="right">1,400,740</td>
<td align="right">663.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">449,840</td>
<td align="right">3,087,060</td>
<td align="right">586.3%</td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right">9,400,700</td>
<td align="right">62,419,820</td>
<td align="right">564.0%</td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right">329,440</td>
<td align="right">1,924,800</td>
<td align="right">484.3%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">241,740</td>
<td align="right">1,170,980</td>
<td align="right">384.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">32,380</td>
<td align="right">144,840</td>
<td align="right">347.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_SLICE</td>
<td align="right">32,380</td>
<td align="right">144,840</td>
<td align="right">347.3%</td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right">351,300</td>
<td align="right">1,548,020</td>
<td align="right">340.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">63,840</td>
<td align="right">257,040</td>
<td align="right">302.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">8,990,980</td>
<td align="right">35,810,220</td>
<td align="right">298.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">30,701,000</td>
<td align="right">121,504,480</td>
<td align="right">295.8%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right">9,246,380</td>
<td align="right">36,557,640</td>
<td align="right">295.4%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">22,380,800</td>
<td align="right">87,968,760</td>
<td align="right">293.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">1,011,420</td>
<td align="right">3,937,620</td>
<td align="right">289.3%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">2,832,540</td>
<td align="right">10,893,380</td>
<td align="right">284.6%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">82,380</td>
<td align="right">308,460</td>
<td align="right">274.4%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">82,380</td>
<td align="right">308,460</td>
<td align="right">274.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_LIST</td>
<td align="right">13,760</td>
<td align="right">48,720</td>
<td align="right">254.1%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">18,086,760</td>
<td align="right">55,951,500</td>
<td align="right">209.4%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">18,229,420</td>
<td align="right">56,220,880</td>
<td align="right">208.4%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">12,480</td>
<td align="right">37,100</td>
<td align="right">197.3%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">22,380,800</td>
<td align="right">65,938,200</td>
<td align="right">194.6%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">22,380,800</td>
<td align="right">65,896,440</td>
<td align="right">194.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">43,680</td>
<td align="right">126,480</td>
<td align="right">189.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_TUPLE</td>
<td align="right">43,680</td>
<td align="right">126,480</td>
<td align="right">189.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">21,251,080</td>
<td align="right">59,110,940</td>
<td align="right">178.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_OVERFLOWED</td>
<td align="right">1,331,440</td>
<td align="right">3,549,820</td>
<td align="right">166.6%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">26,866,380</td>
<td align="right">71,210,520</td>
<td align="right">165.1%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">39,508,240</td>
<td align="right">103,508,140</td>
<td align="right">162.0%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">14,643,780</td>
<td align="right">37,974,480</td>
<td align="right">159.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_OVERFLOWED</td>
<td align="right">1,769,200</td>
<td align="right">4,315,040</td>
<td align="right">143.9%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">3,273,180</td>
<td align="right">7,960,340</td>
<td align="right">143.2%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">17,415,960</td>
<td align="right">42,184,320</td>
<td align="right">142.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">1,030,740</td>
<td align="right">2,434,420</td>
<td align="right">136.2%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">1,030,740</td>
<td align="right">2,434,420</td>
<td align="right">136.2%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">1,025,980</td>
<td align="right">2,381,780</td>
<td align="right">132.1%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">64,344,160</td>
<td align="right">149,131,500</td>
<td align="right">131.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">1,011,420</td>
<td align="right">2,280,600</td>
<td align="right">125.5%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">17,049,300</td>
<td align="right">38,279,340</td>
<td align="right">124.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">1,017,140</td>
<td align="right">2,274,940</td>
<td align="right">123.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">192,940</td>
<td align="right">429,480</td>
<td align="right">122.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">137,520</td>
<td align="right">298,660</td>
<td align="right">117.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">110,570,420</td>
<td align="right">237,321,500</td>
<td align="right">114.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">4,423,360</td>
<td align="right">9,409,340</td>
<td align="right">112.7%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">57,468,640</td>
<td align="right">118,387,560</td>
<td align="right">106.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">4,326,960</td>
<td align="right">8,881,360</td>
<td align="right">105.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">57,468,640</td>
<td align="right">117,835,020</td>
<td align="right">105.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">2,589,760</td>
<td align="right">5,258,780</td>
<td align="right">103.1%</td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_0</td>
<td align="right">187,100</td>
<td align="right">6,860</td>
<td align="right">-96.3%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_KW</td>
<td align="right">304,900</td>
<td align="right">14,160</td>
<td align="right">-95.4%</td>
</tr>
<tr>
<td align="left">_PY_FRAME_KW</td>
<td align="right">304,900</td>
<td align="right">14,160</td>
<td align="right">-95.4%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">16,191,180</td>
<td align="right">31,240,180</td>
<td align="right">92.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">15,678,460</td>
<td align="right">30,113,740</td>
<td align="right">92.1%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">44,802,780</td>
<td align="right">85,197,460</td>
<td align="right">90.2%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">223,487,640</td>
<td align="right">417,664,040</td>
<td align="right">86.9%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">43,847,520</td>
<td align="right">81,059,640</td>
<td align="right">84.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">43,847,520</td>
<td align="right">81,014,420</td>
<td align="right">84.8%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">223,300,300</td>
<td align="right">409,546,580</td>
<td align="right">83.4%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">47,188,680</td>
<td align="right">83,840,880</td>
<td align="right">77.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right">2,864,500</td>
<td align="right">5,070,940</td>
<td align="right">77.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">242,650,840</td>
<td align="right">424,702,440</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">273,542,320</td>
<td align="right">475,646,700</td>
<td align="right">73.9%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">905,790,120</td>
<td align="right">1,562,257,960</td>
<td align="right">72.5%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">118,150,220</td>
<td align="right">197,236,780</td>
<td align="right">66.9%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">12,123,180</td>
<td align="right">20,159,200</td>
<td align="right">66.3%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">751,912,140</td>
<td align="right">1,244,259,160</td>
<td align="right">65.5%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">8,399,840</td>
<td align="right">13,877,480</td>
<td align="right">65.2%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">391,800</td>
<td align="right">141,680</td>
<td align="right">-63.8%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">316,820</td>
<td align="right">515,040</td>
<td align="right">62.6%</td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right">3,780</td>
<td align="right">5,920</td>
<td align="right">56.6%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">9,393,760</td>
<td align="right">14,658,820</td>
<td align="right">56.0%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">9,393,760</td>
<td align="right">14,646,300</td>
<td align="right">55.9%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">39,300</td>
<td align="right">61,220</td>
<td align="right">55.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">51,661,100</td>
<td align="right">79,849,320</td>
<td align="right">54.6%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">4,179,840</td>
<td align="right">6,359,020</td>
<td align="right">52.1%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">24,781,160</td>
<td align="right">37,467,380</td>
<td align="right">51.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">211,100</td>
<td align="right">316,300</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">16,485,360</td>
<td align="right">24,664,840</td>
<td align="right">49.6%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">1,147,780</td>
<td align="right">586,180</td>
<td align="right">-48.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">1,147,780</td>
<td align="right">586,180</td>
<td align="right">-48.9%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">9,393,760</td>
<td align="right">13,899,580</td>
<td align="right">48.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">4,653,380</td>
<td align="right">6,835,500</td>
<td align="right">46.9%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">3,280,840</td>
<td align="right">4,772,220</td>
<td align="right">45.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">914,780</td>
<td align="right">499,240</td>
<td align="right">-45.4%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE</td>
<td align="right">7,811,560</td>
<td align="right">11,348,260</td>
<td align="right">45.3%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">61,541,760</td>
<td align="right">88,139,740</td>
<td align="right">43.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">54,851,640</td>
<td align="right">78,447,960</td>
<td align="right">43.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">22,634,080</td>
<td align="right">32,266,840</td>
<td align="right">42.6%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">4,201,420</td>
<td align="right">5,959,400</td>
<td align="right">41.8%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LEN</td>
<td align="right">187,100</td>
<td align="right">110,060</td>
<td align="right">-41.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">93,658,860</td>
<td align="right">128,397,020</td>
<td align="right">37.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,352,580</td>
<td align="right">3,191,100</td>
<td align="right">35.6%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">68,714,100</td>
<td align="right">91,904,640</td>
<td align="right">33.7%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">28,908,760</td>
<td align="right">38,090,580</td>
<td align="right">31.8%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">13,418,140</td>
<td align="right">17,308,060</td>
<td align="right">29.0%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">5,019,900</td>
<td align="right">6,440,200</td>
<td align="right">28.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">15,403,820</td>
<td align="right">11,064,760</td>
<td align="right">-28.2%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">14,476,440</td>
<td align="right">18,346,340</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">34,410,420</td>
<td align="right">43,574,180</td>
<td align="right">26.6%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">14,281,520</td>
<td align="right">10,628,400</td>
<td align="right">-25.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">1,621,760</td>
<td align="right">2,032,160</td>
<td align="right">25.3%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">3,374,660</td>
<td align="right">4,212,460</td>
<td align="right">24.8%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">16,668,880</td>
<td align="right">12,748,060</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">40,651,540</td>
<td align="right">50,196,540</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">33,134,700</td>
<td align="right">25,640,180</td>
<td align="right">-22.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">117,060</td>
<td align="right">90,660</td>
<td align="right">-22.6%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">34,100</td>
<td align="right">41,700</td>
<td align="right">22.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">7,301,900</td>
<td align="right">5,713,320</td>
<td align="right">-21.8%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">9,898,600</td>
<td align="right">12,051,340</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right">7,672,320</td>
<td align="right">9,223,020</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">35,957,780</td>
<td align="right">43,113,760</td>
<td align="right">19.9%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">3,643,320</td>
<td align="right">4,338,660</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">4,834,140</td>
<td align="right">3,937,420</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">137,520</td>
<td align="right">162,940</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">15,400,860</td>
<td align="right">12,659,400</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">15,400,860</td>
<td align="right">12,659,400</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">27,494,400</td>
<td align="right">22,705,480</td>
<td align="right">-17.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">16,450,920</td>
<td align="right">13,617,960</td>
<td align="right">-17.2%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">17,153,520</td>
<td align="right">14,219,840</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">34,712,120</td>
<td align="right">40,496,880</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">35,336,560</td>
<td align="right">40,964,720</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">50,054,740</td>
<td align="right">57,982,740</td>
<td align="right">15.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">15,704,720</td>
<td align="right">13,240,380</td>
<td align="right">-15.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">79,855,200</td>
<td align="right">91,907,940</td>
<td align="right">15.1%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">27,330,200</td>
<td align="right">31,325,080</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_1</td>
<td align="right">186,980</td>
<td align="right">160,060</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">_PY_FRAME_GENERAL</td>
<td align="right">16,745,980</td>
<td align="right">14,395,920</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right">43,064,680</td>
<td align="right">37,587,920</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">43,090,360</td>
<td align="right">37,764,340</td>
<td align="right">-12.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">7,874,380</td>
<td align="right">8,760,900</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">34,010,000</td>
<td align="right">37,231,700</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">19,927,900</td>
<td align="right">21,719,620</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">15,825,620</td>
<td align="right">16,985,980</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">9,580,400</td>
<td align="right">10,257,000</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">212,260</td>
<td align="right">226,080</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right">4,882,320</td>
<td align="right">4,620,520</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">12,171,200</td>
<td align="right">12,714,260</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">2,341,740</td>
<td align="right">2,437,880</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_DICT</td>
<td align="right">23,620,800</td>
<td align="right">22,758,800</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right">34,227,100</td>
<td align="right">32,997,520</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">73,446,080</td>
<td align="right">72,709,900</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">27,699,660</td>
<td align="right">27,937,840</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">17,500</td>
<td align="right">17,480</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">4,008,480</td>
<td align="right">4,008,360</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">22,110,740</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">117,060</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">168,337,840</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">20,729,980</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right"></td>
<td align="right">19,139,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right"></td>
<td align="right">19,139,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right"></td>
<td align="right">17,630,920</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_FOR</td>
<td align="right"></td>
<td align="right">17,348,480</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">6,710,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right"></td>
<td align="right">3,440,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right"></td>
<td align="right">3,439,640</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_STR_1</td>
<td align="right"></td>
<td align="right">2,349,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right">1,613,980</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right"></td>
<td align="right">1,275,540</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_CHECK_FUNC</td>
<td align="right"></td>
<td align="right">1,204,200</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_INIT_CALL</td>
<td align="right"></td>
<td align="right">1,202,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_AND_ALLOCATE_OBJECT</td>
<td align="right"></td>
<td align="right">963,500</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right"></td>
<td align="right">663,500</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right"></td>
<td align="right">571,020</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">318,340</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SWAP_3</td>
<td align="right"></td>
<td align="right">243,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS</td>
<td align="right"></td>
<td align="right">225,980</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right"></td>
<td align="right">116,820</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right"></td>
<td align="right">110,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right"></td>
<td align="right">109,820</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CREATE_INIT_FRAME</td>
<td align="right"></td>
<td align="right">97,840</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right"></td>
<td align="right">97,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right"></td>
<td align="right">68,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_TYPE_1</td>
<td align="right"></td>
<td align="right">68,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_PROPERTY_FRAME</td>
<td align="right"></td>
<td align="right">41,760</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_INIT_CHECK</td>
<td align="right"></td>
<td align="right">31,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">25,060</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">700</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">620</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right"></td>
<td align="right">160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_ANY_SET</td>
<td align="right"></td>
<td align="right">160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right"></td>
<td align="right">60</td>
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
<td align="right">900</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">140</td>
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
set class
<details>
<summary>ⓘ</summary>

Setting an object's class, `obj.__class__ = ...`
</details>
</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right"></td>
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
<td align="right">0</td>
<td align="right"></td>
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
<td align="right">0</td>
<td align="right">0</td>
<td align="right"></td>
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
<td align="right">20</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-10-23
