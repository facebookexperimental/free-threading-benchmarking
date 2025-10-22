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
<td align="right">2,926,940</td>
<td align="right">11,153,900</td>
<td align="right">281.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">18,699,910</td>
<td align="right">9,433,895</td>
<td align="right">-49.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">13,608,780</td>
<td align="right">7,560,000</td>
<td align="right">-44.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">1,358,660</td>
<td align="right">802,480</td>
<td align="right">-40.9%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">2,264,600</td>
<td align="right">1,649,200</td>
<td align="right">-27.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">4,364,620</td>
<td align="right">3,389,400</td>
<td align="right">-22.3%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,650,340</td>
<td align="right">1,289,320</td>
<td align="right">-21.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">6,457,860</td>
<td align="right">5,190,760</td>
<td align="right">-19.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,410,860</td>
<td align="right">1,962,880</td>
<td align="right">-18.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,546,840</td>
<td align="right">6,202,500</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">6,000,200</td>
<td align="right">5,024,620</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">178,560</td>
<td align="right">149,780</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">3,435,450</td>
<td align="right">2,886,515</td>
<td align="right">-16.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">2,466,360</td>
<td align="right">2,079,180</td>
<td align="right">-15.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">4,376,490</td>
<td align="right">3,826,335</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">2,275,010</td>
<td align="right">1,989,575</td>
<td align="right">-12.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">9,129,770</td>
<td align="right">8,009,215</td>
<td align="right">-12.3%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">10,898,580</td>
<td align="right">9,596,540</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">1,102,500</td>
<td align="right">987,820</td>
<td align="right">-10.4%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">8,286,620</td>
<td align="right">7,456,700</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">3,402,620</td>
<td align="right">3,078,260</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">2,417,720</td>
<td align="right">2,201,240</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">3,159,400</td>
<td align="right">2,903,300</td>
<td align="right">-8.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">51,190,940</td>
<td align="right">47,120,200</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">34,052,700</td>
<td align="right">31,407,180</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">1,957,940</td>
<td align="right">1,810,660</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">956,960</td>
<td align="right">885,840</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">39,342,280</td>
<td align="right">36,598,500</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">6,647,000</td>
<td align="right">6,213,240</td>
<td align="right">-6.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">760,640</td>
<td align="right">712,720</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">152,654,620</td>
<td align="right">143,356,610</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">2,644,080</td>
<td align="right">2,484,720</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">156,000</td>
<td align="right">147,160</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">3,860,780</td>
<td align="right">3,645,300</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,036,340</td>
<td align="right">6,661,260</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">749,300</td>
<td align="right">710,660</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">751,840</td>
<td align="right">713,200</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">1,570,780</td>
<td align="right">1,491,640</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,831,000</td>
<td align="right">1,739,060</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">439,080</td>
<td align="right">417,400</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">3,804,840</td>
<td align="right">3,621,240</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">27,054,110</td>
<td align="right">25,801,915</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">5,778,080</td>
<td align="right">5,519,400</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">12,424,780</td>
<td align="right">11,879,920</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">1,190,080</td>
<td align="right">1,139,360</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">2,559,800</td>
<td align="right">2,452,320</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">901,920</td>
<td align="right">864,880</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">40,877,060</td>
<td align="right">39,305,220</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">1,709,340</td>
<td align="right">1,647,380</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">13,041,460</td>
<td align="right">12,580,400</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">5,170,420</td>
<td align="right">4,988,240</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">23,350,080</td>
<td align="right">22,563,320</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">598,720</td>
<td align="right">578,820</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">23,024,520</td>
<td align="right">22,333,660</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">476,400</td>
<td align="right">462,260</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">6,473,440</td>
<td align="right">6,281,480</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">24,006,580</td>
<td align="right">23,301,200</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">1,084,040</td>
<td align="right">1,052,400</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">26,459,560</td>
<td align="right">25,691,920</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">3,708,640</td>
<td align="right">3,602,320</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">11,109,660</td>
<td align="right">10,793,600</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">39,203,620</td>
<td align="right">38,092,460</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">27,722,060</td>
<td align="right">26,964,120</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">3,333,600</td>
<td align="right">3,421,640</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">13,509,300</td>
<td align="right">13,860,900</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">51,541,460</td>
<td align="right">50,241,580</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">1,471,200</td>
<td align="right">1,434,800</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">743,640</td>
<td align="right">725,440</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">3,256,160</td>
<td align="right">3,176,960</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">11,133,920</td>
<td align="right">10,870,480</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">233,460</td>
<td align="right">228,140</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">3,440,220</td>
<td align="right">3,369,040</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">16,910,120</td>
<td align="right">16,566,770</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">59,600</td>
<td align="right">58,400</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">867,140</td>
<td align="right">849,940</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">1,843,620</td>
<td align="right">1,807,340</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">2,061,000</td>
<td align="right">2,021,620</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">5,048,220</td>
<td align="right">4,958,920</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">3,410,840</td>
<td align="right">3,354,300</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">6,682,440</td>
<td align="right">6,573,060</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">1,720,630</td>
<td align="right">1,694,275</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">2,572,080</td>
<td align="right">2,533,840</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">7,717,980</td>
<td align="right">7,609,180</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">8,560,310</td>
<td align="right">8,441,995</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">4,929,960</td>
<td align="right">4,996,980</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">8,037,680</td>
<td align="right">7,929,600</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">4,201,220</td>
<td align="right">4,145,460</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">4,117,280</td>
<td align="right">4,062,820</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">10,443,480</td>
<td align="right">10,307,780</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">4,987,920</td>
<td align="right">4,925,060</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">100,860</td>
<td align="right">99,700</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">2,576,300</td>
<td align="right">2,553,760</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">8,962,920</td>
<td align="right">8,888,780</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,064,720</td>
<td align="right">1,056,700</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">1,314,060</td>
<td align="right">1,304,420</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">404,160</td>
<td align="right">401,400</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">20,728,000</td>
<td align="right">20,594,700</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">838,800</td>
<td align="right">833,520</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">2,285,330</td>
<td align="right">2,277,334</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">7,620,240</td>
<td align="right">7,594,960</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,783,340</td>
<td align="right">1,779,100</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">796,380</td>
<td align="right">797,820</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">5,134,140</td>
<td align="right">5,128,620</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">1,835,640</td>
<td align="right">1,833,800</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">17,323,930</td>
<td align="right">17,339,235</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">789,000</td>
<td align="right">788,520</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">603,140</td>
<td align="right">603,340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">61,800</td>
<td align="right">61,820</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">646,140</td>
<td align="right">646,340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">216,580</td>
<td align="right">216,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">617,380</td>
<td align="right">617,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">536,720</td>
<td align="right">536,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">565,940</td>
<td align="right">565,900</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">6,068,700</td>
<td align="right">6,068,760</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">6,490,100</td>
<td align="right">6,490,040</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">2,249,020</td>
<td align="right">2,249,020</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">1,605,120</td>
<td align="right">1,605,120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">1,426,860</td>
<td align="right">1,426,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">1,273,140</td>
<td align="right">1,273,140</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">944,280</td>
<td align="right">944,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">618,400</td>
<td align="right">618,400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">551,020</td>
<td align="right">551,020</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">551,020</td>
<td align="right">551,020</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">481,620</td>
<td align="right">481,620</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">376,920</td>
<td align="right">376,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">345,640</td>
<td align="right">345,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">326,460</td>
<td align="right">326,460</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">271,680</td>
<td align="right">271,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">255,120</td>
<td align="right">255,120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">255,120</td>
<td align="right">255,120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">234,600</td>
<td align="right">234,600</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">227,160</td>
<td align="right">227,160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">222,880</td>
<td align="right">222,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">203,340</td>
<td align="right">203,340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">152,400</td>
<td align="right">152,400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">147,840</td>
<td align="right">147,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">110,320</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">109,980</td>
<td align="right">109,980</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">104,640</td>
<td align="right">104,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">100,260</td>
<td align="right">100,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">90,840</td>
<td align="right">90,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">73,840</td>
<td align="right">73,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">73,680</td>
<td align="right">73,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">67,860</td>
<td align="right">67,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">66,900</td>
<td align="right">66,900</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">55,000</td>
<td align="right">55,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">49,580</td>
<td align="right">49,580</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">49,560</td>
<td align="right">49,560</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">49,080</td>
<td align="right">49,080</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">44,340</td>
<td align="right">44,340</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">42,840</td>
<td align="right">42,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">39,900</td>
<td align="right">39,900</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">39,420</td>
<td align="right">39,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">18,360</td>
<td align="right">18,360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">17,760</td>
<td align="right">17,760</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">14,780</td>
<td align="right">14,780</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">13,320</td>
<td align="right">13,320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">13,040</td>
<td align="right">13,040</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">12,360</td>
<td align="right">12,360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">2,700</td>
<td align="right">2,700</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">2,100</td>
<td align="right">2,100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">1,380</td>
<td align="right">1,380</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">900</td>
<td align="right">900</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">900</td>
<td align="right">900</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">780</td>
<td align="right">780</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">660</td>
<td align="right">660</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">600</td>
<td align="right">600</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">420</td>
<td align="right">420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">420</td>
<td align="right">420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">420</td>
<td align="right">420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">320</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">120</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">120</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,403,500</td>
<td align="right">10.1%</td>
<td align="right">1,947,300</td>
<td align="right">8.3%</td>
<td align="right">-19.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">21,304,080</td>
<td align="right">89.6%</td>
<td align="right">21,304,080</td>
<td align="right">91.3%</td>
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
<td align="right">57,780</td>
<td align="right">0.2%</td>
<td align="right">57,780</td>
<td align="right">0.2%</td>
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
<td align="right">6,060</td>
<td align="right">71.8%</td>
<td align="right">14,280</td>
<td align="right">85.7%</td>
<td align="right">135.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,380</td>
<td align="right">28.2%</td>
<td align="right">2,380</td>
<td align="right">14.3%</td>
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
<td align="left">subscr</td>
<td align="right">620</td>
<td align="right">10.2%</td>
<td align="right">8,700</td>
<td align="right">60.9%</td>
<td align="right">1,303.2%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">140</td>
<td align="right">2.3%</td>
<td align="right">220</td>
<td align="right">1.5%</td>
<td align="right">57.1%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">180</td>
<td align="right">3.0%</td>
<td align="right">200</td>
<td align="right">1.4%</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">600</td>
<td align="right">9.9%</td>
<td align="right">640</td>
<td align="right">4.5%</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">660</td>
<td align="right">10.9%</td>
<td align="right">620</td>
<td align="right">4.3%</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">800</td>
<td align="right">13.2%</td>
<td align="right">820</td>
<td align="right">5.7%</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">2,440</td>
<td align="right">40.3%</td>
<td align="right">2,460</td>
<td align="right">17.2%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">180</td>
<td align="right">3.0%</td>
<td align="right">180</td>
<td align="right">1.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">140</td>
<td align="right">2.3%</td>
<td align="right">140</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">100</td>
<td align="right">1.7%</td>
<td align="right">100</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">60</td>
<td align="right">1.0%</td>
<td align="right">60</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">40</td>
<td align="right">0.7%</td>
<td align="right">40</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">20</td>
<td align="right">0.3%</td>
<td align="right">20</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">20</td>
<td align="right">0.3%</td>
<td align="right">20</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">20</td>
<td align="right">0.3%</td>
<td align="right">20</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr other slice</td>
<td align="right">20</td>
<td align="right">0.3%</td>
<td align="right">20</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr ordereddict</td>
<td align="right">20</td>
<td align="right">0.3%</td>
<td align="right">20</td>
<td align="right">0.1%</td>
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
<td align="right">536,720</td>
<td align="right">100.0%</td>
<td align="right">536,840</td>
<td align="right">100.0%</td>
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
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">8,000</td>
<td align="right">0.0%</td>
<td align="right">8,500</td>
<td align="right">0.0%</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">6,919,160</td>
<td align="right">11.7%</td>
<td align="right">6,587,080</td>
<td align="right">11.1%</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">7,051,960</td>
<td align="right">11.9%</td>
<td align="right">6,713,760</td>
<td align="right">11.3%</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">52,220,660</td>
<td align="right">88.1%</td>
<td align="right">52,765,740</td>
<td align="right">88.7%</td>
<td align="right">1.0%</td>
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
<td align="right">147,580</td>
<td align="right">100.0%</td>
<td align="right">141,460</td>
<td align="right">100.0%</td>
<td align="right">-4.1%</td>
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
<td align="right">40</td>
<td align="right">40 / 0 !!</td>
<td align="right">40</td>
<td align="right">40 / 0 !!</td>
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
<td align="right">531,920</td>
<td align="right">97.9%</td>
<td align="right">531,920</td>
<td align="right">97.9%</td>
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
<td align="right">542,140</td>
<td align="right">99.7%</td>
<td align="right">542,140</td>
<td align="right">99.7%</td>
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
<td align="right">11,600</td>
<td align="right">100.0%</td>
<td align="right">11,600</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">757,760</td>
<td align="right">4.8%</td>
<td align="right">709,820</td>
<td align="right">4.5%</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">15,015,980</td>
<td align="right">95.2%</td>
<td align="right">15,015,980</td>
<td align="right">95.5%</td>
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
<td align="right">1,900</td>
<td align="right">0.0%</td>
<td align="right">1,900</td>
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
<td align="right">2,000</td>
<td align="right">68.5%</td>
<td align="right">2,020</td>
<td align="right">68.7%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">920</td>
<td align="right">31.5%</td>
<td align="right">920</td>
<td align="right">31.3%</td>
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
<td align="left">baseobject</td>
<td align="right">460</td>
<td align="right">23.0%</td>
<td align="right">480</td>
<td align="right">23.8%</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">920</td>
<td align="right">46.0%</td>
<td align="right">920</td>
<td align="right">45.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">220</td>
<td align="right">11.0%</td>
<td align="right">220</td>
<td align="right">10.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">120</td>
<td align="right">6.0%</td>
<td align="right">120</td>
<td align="right">5.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">120</td>
<td align="right">6.0%</td>
<td align="right">120</td>
<td align="right">5.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">80</td>
<td align="right">4.0%</td>
<td align="right">80</td>
<td align="right">4.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">40</td>
<td align="right">2.0%</td>
<td align="right">40</td>
<td align="right">2.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">40</td>
<td align="right">2.0%</td>
<td align="right">40</td>
<td align="right">2.0%</td>
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
<td align="right">2,279,490</td>
<td align="right">38.4%</td>
<td align="right">2,270,635</td>
<td align="right">38.3%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,632,700</td>
<td align="right">61.1%</td>
<td align="right">3,632,700</td>
<td align="right">61.2%</td>
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
<td align="right">24,900</td>
<td align="right">0.4%</td>
<td align="right">24,900</td>
<td align="right">0.4%</td>
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
<td align="right">5,340</td>
<td align="right">84.5%</td>
<td align="right">6,199</td>
<td align="right">86.3%</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">980</td>
<td align="right">15.5%</td>
<td align="right">980</td>
<td align="right">13.7%</td>
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
<td align="left">other</td>
<td align="right">400</td>
<td align="right">7.5%</td>
<td align="right">640</td>
<td align="right">10.3%</td>
<td align="right">60.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">2,860</td>
<td align="right">53.6%</td>
<td align="right">3,379</td>
<td align="right">54.5%</td>
<td align="right">18.1%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">1,080</td>
<td align="right">20.2%</td>
<td align="right">1,140</td>
<td align="right">18.4%</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">1,000</td>
<td align="right">18.7%</td>
<td align="right">1,040</td>
<td align="right">16.8%</td>
<td align="right">4.0%</td>
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
<td align="right">4,356,480</td>
<td align="right">14.9%</td>
<td align="right">3,367,780</td>
<td align="right">12.4%</td>
<td align="right">-22.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">211,040</td>
<td align="right">0.7%</td>
<td align="right">186,300</td>
<td align="right">0.7%</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">24,720,050</td>
<td align="right">84.4%</td>
<td align="right">23,476,235</td>
<td align="right">86.8%</td>
<td align="right">-5.0%</td>
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
<td align="right">40</td>
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
<td align="right">7,600</td>
<td align="right">62.7%</td>
<td align="right">21,080</td>
<td align="right">83.9%</td>
<td align="right">177.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">4,520</td>
<td align="right">37.3%</td>
<td align="right">4,060</td>
<td align="right">16.1%</td>
<td align="right">-10.2%</td>
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
<td align="right">1,060</td>
<td align="right">13.9%</td>
<td align="right">15,320</td>
<td align="right">72.7%</td>
<td align="right">1,345.3%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">3,880</td>
<td align="right">51.1%</td>
<td align="right">2,940</td>
<td align="right">13.9%</td>
<td align="right">-24.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">140</td>
<td align="right">1.8%</td>
<td align="right">160</td>
<td align="right">0.8%</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">1,180</td>
<td align="right">15.5%</td>
<td align="right">1,320</td>
<td align="right">6.3%</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">500</td>
<td align="right">6.6%</td>
<td align="right">500</td>
<td align="right">2.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">260</td>
<td align="right">3.4%</td>
<td align="right">260</td>
<td align="right">1.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">220</td>
<td align="right">2.9%</td>
<td align="right">220</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">200</td>
<td align="right">2.6%</td>
<td align="right">200</td>
<td align="right">0.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">120</td>
<td align="right">1.6%</td>
<td align="right">120</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">40</td>
<td align="right">0.5%</td>
<td align="right">40</td>
<td align="right">0.2%</td>
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
<td align="left">generator</td>
<td align="right">4,712,220</td>
<td align="right">4,712,220 / 0 !!</td>
<td align="right">4,712,220</td>
<td align="right">4,712,220 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">3,912,420</td>
<td align="right">3,912,420 / 0 !!</td>
<td align="right">3,912,420</td>
<td align="right">3,912,420 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">1,037,880</td>
<td align="right">1,037,880 / 0 !!</td>
<td align="right">1,037,880</td>
<td align="right">1,037,880 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">559,140</td>
<td align="right">559,140 / 0 !!</td>
<td align="right">559,140</td>
<td align="right">559,140 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">509,640</td>
<td align="right">509,640 / 0 !!</td>
<td align="right">509,640</td>
<td align="right">509,640 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">263,640</td>
<td align="right">263,640 / 0 !!</td>
<td align="right">263,640</td>
<td align="right">263,640 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">147,420</td>
<td align="right">147,420 / 0 !!</td>
<td align="right">147,420</td>
<td align="right">147,420 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">6,900</td>
<td align="right">6,900 / 0 !!</td>
<td align="right">6,900</td>
<td align="right">6,900 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">300</td>
<td align="right">300 / 0 !!</td>
<td align="right">300</td>
<td align="right">300 / 0 !!</td>
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
<td align="right">179,920</td>
<td align="right">0.2%</td>
<td align="right">197,240</td>
<td align="right">0.2%</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">12,314,580</td>
<td align="right">11.1%</td>
<td align="right">11,778,160</td>
<td align="right">10.7%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">29,680,173</td>
<td align="right">26.8%</td>
<td align="right">29,129,888</td>
<td align="right">26.4%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">68,614,487</td>
<td align="right">62.0%</td>
<td align="right">69,287,082</td>
<td align="right">62.8%</td>
<td align="right">1.0%</td>
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
<td align="right">64,320</td>
<td align="right">10.1%</td>
<td align="right">71,900</td>
<td align="right">11.1%</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">572,560</td>
<td align="right">89.9%</td>
<td align="right">578,140</td>
<td align="right">88.9%</td>
<td align="right">1.0%</td>
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
<td align="right">520</td>
<td align="right">0.8%</td>
<td align="right">680</td>
<td align="right">0.9%</td>
<td align="right">30.8%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">2,800</td>
<td align="right">4.4%</td>
<td align="right">3,180</td>
<td align="right">4.4%</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">3,040</td>
<td align="right">4.7%</td>
<td align="right">3,280</td>
<td align="right">4.6%</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">360</td>
<td align="right">0.6%</td>
<td align="right">380</td>
<td align="right">0.5%</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,380</td>
<td align="right">2.1%</td>
<td align="right">1,380</td>
<td align="right">1.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">740</td>
<td align="right">1.2%</td>
<td align="right">740</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">680</td>
<td align="right">1.1%</td>
<td align="right">680</td>
<td align="right">0.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">480</td>
<td align="right">0.7%</td>
<td align="right">480</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">200</td>
<td align="right">0.3%</td>
<td align="right">200</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">180</td>
<td align="right">0.3%</td>
<td align="right">180</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">160</td>
<td align="right">0.2%</td>
<td align="right">160</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">40</td>
<td align="right">0.1%</td>
<td align="right">40</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">40</td>
<td align="right">0.1%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">49,807,660</td>
<td align="right">100.0%</td>
<td align="right">48,790,360</td>
<td align="right">100.0%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="right">1,980</td>
<td align="right">0.0%</td>
<td align="right">1,980</td>
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
<td align="right">13,040</td>
<td align="right">100.0%</td>
<td align="right">13,040</td>
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
<td align="right">529,320</td>
<td align="right">99.9%</td>
<td align="right">529,320</td>
<td align="right">99.9%</td>
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
<td align="right">320</td>
<td align="right">100.0%</td>
<td align="right">320</td>
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
<td align="right">6,066,240</td>
<td align="right">54.9%</td>
<td align="right">6,066,240</td>
<td align="right">54.9%</td>
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
<td align="right">4,987,920</td>
<td align="right">45.1%</td>
<td align="right">4,987,920</td>
<td align="right">45.1%</td>
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
<td align="right">2,400</td>
<td align="right">97.6%</td>
<td align="right">2,460</td>
<td align="right">97.6%</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">60</td>
<td align="right">2.4%</td>
<td align="right">60</td>
<td align="right">2.4%</td>
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
<td align="right">640</td>
<td align="right">26.7%</td>
<td align="right">680</td>
<td align="right">27.6%</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">1,720</td>
<td align="right">71.7%</td>
<td align="right">1,740</td>
<td align="right">70.7%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">40</td>
<td align="right">1.7%</td>
<td align="right">40</td>
<td align="right">1.6%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,184,180</td>
<td align="right">10.3%</td>
<td align="right">1,133,440</td>
<td align="right">9.9%</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">9,263,720</td>
<td align="right">80.5%</td>
<td align="right">9,263,720</td>
<td align="right">80.8%</td>
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
<td align="right">1,058,600</td>
<td align="right">9.2%</td>
<td align="right">1,058,600</td>
<td align="right">9.2%</td>
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
<td align="right">2,280</td>
<td align="right">8.9%</td>
<td align="right">2,300</td>
<td align="right">8.9%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">23,480</td>
<td align="right">91.1%</td>
<td align="right">23,480</td>
<td align="right">91.1%</td>
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
<td align="left">other</td>
<td align="right">52,760</td>
<td align="right">2,314.0%</td>
<td align="right">59,500</td>
<td align="right">2,587.0%</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">480</td>
<td align="right">21.1%</td>
<td align="right">500</td>
<td align="right">21.7%</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1,020</td>
<td align="right">44.7%</td>
<td align="right">1,020</td>
<td align="right">44.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">380</td>
<td align="right">16.7%</td>
<td align="right">380</td>
<td align="right">16.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">200</td>
<td align="right">8.8%</td>
<td align="right">200</td>
<td align="right">8.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">120</td>
<td align="right">5.3%</td>
<td align="right">120</td>
<td align="right">5.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">20</td>
<td align="right">0.9%</td>
<td align="right">20</td>
<td align="right">0.9%</td>
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
<td align="right">73,260</td>
<td align="right">3.0%</td>
<td align="right">73,260</td>
<td align="right">3.0%</td>
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
<td align="right">2,371,580</td>
<td align="right">97.0%</td>
<td align="right">2,371,580</td>
<td align="right">97.0%</td>
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
<td align="right">240</td>
<td align="right">41.4%</td>
<td align="right">240</td>
<td align="right">41.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">340</td>
<td align="right">58.6%</td>
<td align="right">340</td>
<td align="right">58.6%</td>
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
<td align="left">dict subclass no override</td>
<td align="right">200</td>
<td align="right">58.8%</td>
<td align="right">200</td>
<td align="right">58.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">80</td>
<td align="right">23.5%</td>
<td align="right">80</td>
<td align="right">23.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">40</td>
<td align="right">11.8%</td>
<td align="right">40</td>
<td align="right">11.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">20</td>
<td align="right">5.9%</td>
<td align="right">20</td>
<td align="right">5.9%</td>
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
<td align="right">2,736,480</td>
<td align="right">7.2%</td>
<td align="right">2,658,260</td>
<td align="right">7.0%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">34,815,610</td>
<td align="right">91.3%</td>
<td align="right">34,679,635</td>
<td align="right">91.5%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">555,080</td>
<td align="right">1.5%</td>
<td align="right">555,080</td>
<td align="right">1.5%</td>
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
<td align="right">140</td>
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
<td align="right">56,560</td>
<td align="right">90.8%</td>
<td align="right">55,180</td>
<td align="right">90.7%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">5,720</td>
<td align="right">9.2%</td>
<td align="right">5,680</td>
<td align="right">9.3%</td>
<td align="right">-0.7%</td>
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
<td align="right">3,420</td>
<td align="right">59.8%</td>
<td align="right">3,380</td>
<td align="right">59.5%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">780</td>
<td align="right">13.6%</td>
<td align="right">780</td>
<td align="right">13.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">600</td>
<td align="right">10.5%</td>
<td align="right">600</td>
<td align="right">10.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">520</td>
<td align="right">9.1%</td>
<td align="right">520</td>
<td align="right">9.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">260</td>
<td align="right">4.5%</td>
<td align="right">260</td>
<td align="right">4.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">80</td>
<td align="right">1.4%</td>
<td align="right">80</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">40</td>
<td align="right">0.7%</td>
<td align="right">40</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">20</td>
<td align="right">0.3%</td>
<td align="right">20</td>
<td align="right">0.4%</td>
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
<td align="right">6,499,890</td>
<td align="right">89.1%</td>
<td align="right">6,499,215</td>
<td align="right">89.1%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">795,600</td>
<td align="right">10.9%</td>
<td align="right">795,540</td>
<td align="right">10.9%</td>
<td align="right">-0.0%</td>
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
<td align="right">200</td>
<td align="right">25.6%</td>
<td align="right">1,700</td>
<td align="right">74.6%</td>
<td align="right">750.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">580</td>
<td align="right">74.4%</td>
<td align="right">580</td>
<td align="right">25.4%</td>
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
<td align="left">sequence</td>
<td align="right">180</td>
<td align="right">90.0%</td>
<td align="right">1,680</td>
<td align="right">98.8%</td>
<td align="right">833.3%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">20</td>
<td align="right">10.0%</td>
<td align="right">20</td>
<td align="right">1.2%</td>
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
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">352,182,377</td>
<td align="right">34.8%</td>
<td align="right">323,298,737</td>
<td align="right">33.7%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">42,641,330</td>
<td align="right">4.2%</td>
<td align="right">40,304,774</td>
<td align="right">4.2%</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">576,747,420</td>
<td align="right">56.9%</td>
<td align="right">555,602,430</td>
<td align="right">57.9%</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">41,367,473</td>
<td align="right">4.1%</td>
<td align="right">40,375,868</td>
<td align="right">4.2%</td>
<td align="right">-2.4%</td>
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
<td align="right">4,356,480</td>
<td align="right">11.2%</td>
<td align="right">3,367,780</td>
<td align="right">9.3%</td>
<td align="right">-22.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,403,500</td>
<td align="right">6.2%</td>
<td align="right">1,947,300</td>
<td align="right">5.4%</td>
<td align="right">-19.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">757,760</td>
<td align="right">2.0%</td>
<td align="right">709,820</td>
<td align="right">2.0%</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">6,919,160</td>
<td align="right">17.8%</td>
<td align="right">6,587,080</td>
<td align="right">18.1%</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">12,314,580</td>
<td align="right">31.8%</td>
<td align="right">11,778,160</td>
<td align="right">32.4%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">1,184,180</td>
<td align="right">3.1%</td>
<td align="right">1,133,440</td>
<td align="right">3.1%</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">2,279,490</td>
<td align="right">5.9%</td>
<td align="right">2,270,635</td>
<td align="right">6.2%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">795,600</td>
<td align="right">2.1%</td>
<td align="right">795,540</td>
<td align="right">2.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">6,066,240</td>
<td align="right">15.6%</td>
<td align="right">6,066,240</td>
<td align="right">16.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">555,080</td>
<td align="right">1.4%</td>
<td align="right">555,080</td>
<td align="right">1.5%</td>
<td align="right">0.0%</td>
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
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">1,300,300</td>
<td align="right">3.1%</td>
<td align="right">1,062,060</td>
<td align="right">2.6%</td>
<td align="right">-18.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">2,916,280</td>
<td align="right">7.0%</td>
<td align="right">2,635,400</td>
<td align="right">6.5%</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">819,080</td>
<td align="right">2.0%</td>
<td align="right">766,180</td>
<td align="right">1.9%</td>
<td align="right">-6.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">2,387,980</td>
<td align="right">5.8%</td>
<td align="right">2,331,340</td>
<td align="right">5.8%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">5,033,640</td>
<td align="right">12.2%</td>
<td align="right">4,930,860</td>
<td align="right">12.2%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">14,961,220</td>
<td align="right">36.2%</td>
<td align="right">14,686,980</td>
<td align="right">36.4%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,944,380</td>
<td align="right">12.0%</td>
<td align="right">4,985,620</td>
<td align="right">12.3%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">5,982,920</td>
<td align="right">14.5%</td>
<td align="right">5,999,580</td>
<td align="right">14.9%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,058,540</td>
<td align="right">2.6%</td>
<td align="right">1,058,540</td>
<td align="right">2.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">503,480</td>
<td align="right">1.2%</td>
<td align="right">503,480</td>
<td align="right">1.2%</td>
<td align="right">0.0%</td>
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
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">1,824,840</td>
<td align="right">3.0%</td>
<td align="right">1,824,780</td>
<td align="right">3.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">6,690,180</td>
<td align="right">10.8%</td>
<td align="right">6,690,120</td>
<td align="right">10.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">6,690,180</td>
<td align="right">10.8%</td>
<td align="right">6,690,120</td>
<td align="right">10.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">55,110,000</td>
<td align="right">89.2%</td>
<td align="right">55,110,060</td>
<td align="right">89.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">4,865,340</td>
<td align="right">7.9%</td>
<td align="right">4,865,340</td>
<td align="right">7.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">4,864,860</td>
<td align="right">7.9%</td>
<td align="right">4,864,860</td>
<td align="right">7.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">420</td>
<td align="right">0.0%</td>
<td align="right">420</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">339,560</td>
<td align="right">0.5%</td>
<td align="right">339,560</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">412,560</td>
<td align="right">0.7%</td>
<td align="right">412,560</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">496,440</td>
<td align="right">0.8%</td>
<td align="right">496,440</td>
<td align="right">0.8%</td>
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
<td align="right">780,900</td>
<td align="right">1.3%</td>
<td align="right">780,900</td>
<td align="right">1.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">42,150,440</td>
<td align="right">68.2%</td>
<td align="right">42,150,440</td>
<td align="right">68.2%</td>
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
<td align="right">213,619</td>
<td align="right"></td>
<td align="right">181,238</td>
<td align="right"></td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">1,243,032</td>
<td align="right"></td>
<td align="right">1,355,415</td>
<td align="right"></td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">223,658,967</td>
<td align="right">33.8%</td>
<td align="right">211,173,652</td>
<td align="right">31.9%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">1,456,067</td>
<td align="right"></td>
<td align="right">1,536,037</td>
<td align="right"></td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">249,601,841</td>
<td align="right">37.7%</td>
<td align="right">262,487,907</td>
<td align="right">39.6%</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">230,757,948</td>
<td align="right">33.9%</td>
<td align="right">237,583,858</td>
<td align="right">34.9%</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">307,606,500</td>
<td align="right">45.2%</td>
<td align="right">301,181,800</td>
<td align="right">44.3%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">27,260</td>
<td align="right">0.0%</td>
<td align="right">27,820</td>
<td align="right">0.0%</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">35,761,340</td>
<td align="right">5.4%</td>
<td align="right">35,114,380</td>
<td align="right">5.3%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">48,705,934</td>
<td align="right"></td>
<td align="right">47,857,221</td>
<td align="right"></td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">117,325,731</td>
<td align="right">17.2%</td>
<td align="right">116,731,314</td>
<td align="right">17.2%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">286,380</td>
<td align="right">0.4%</td>
<td align="right">287,280</td>
<td align="right">0.4%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">24,584,100</td>
<td align="right">3.6%</td>
<td align="right">24,517,180</td>
<td align="right">3.6%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">153,566,174</td>
<td align="right">23.2%</td>
<td align="right">153,268,396</td>
<td align="right">23.2%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">25,969,221</td>
<td align="right"></td>
<td align="right">26,016,062</td>
<td align="right"></td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">35,259,680</td>
<td align="right">47.0%</td>
<td align="right">35,262,040</td>
<td align="right">47.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">35,282,540</td>
<td align="right"></td>
<td align="right">35,284,900</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">39,423,547</td>
<td align="right"></td>
<td align="right">39,422,323</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">39,755,211</td>
<td align="right">53.0%</td>
<td align="right">39,756,051</td>
<td align="right">53.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">39,441,571</td>
<td align="right">52.6%</td>
<td align="right">39,440,951</td>
<td align="right">52.6%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">894,540</td>
<td align="right"></td>
<td align="right">894,540</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">77,100</td>
<td align="right">8.6%</td>
<td align="right">77,100</td>
<td align="right">8.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">3,000</td>
<td align="right">0.3%</td>
<td align="right">3,000</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
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
<td align="right">1,060</td>
<td align="right">19,460</td>
<td align="right">60,919,623</td>
<td align="right">8,948,990</td>
<td align="right">1,842,790</td>
<td align="right">1,060</td>
<td align="right">19,460</td>
<td align="right">60,980,691</td>
<td align="right">8,951,160</td>
<td align="right">1,841,000</td>
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
<td align="right">4,340</td>
<td align="right"></td>
<td align="right">141,340</td>
<td align="right"></td>
<td align="right">3,156.7%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">1,120</td>
<td align="right">25.8%</td>
<td align="right">2,680</td>
<td align="right">1.9%</td>
<td align="right">139.3%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">620</td>
<td align="right">14.3%</td>
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
<td align="right">40</td>
<td align="right">0.9%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">40</td>
<td align="right">0.9%</td>
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
<td align="right">2,560</td>
<td align="right">59.0%</td>
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
<td align="right">15,294,040</td>
<td align="right"></td>
<td align="right">27,683,320</td>
<td align="right"></td>
<td align="right">81.0%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">261,985,280</td>
<td align="right">1,713.0%</td>
<td align="right">472,234,420</td>
<td align="right">1,705.8%</td>
<td align="right">80.3%</td>
</tr>
<tr>
<td align="left">
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
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
Trace too long
<details>
<summary>ⓘ</summary>

A trace is truncated because it is longer than the instruction buffer.
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">220</td>
<td align="right">0.2%</td>
<td align="right">220 / 0 !!</td>
</tr>
<tr>
<td align="left">
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
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
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
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
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">1,120</td>
<td align="right"></td>
<td align="right">2,680</td>
<td align="right"></td>
<td align="right">139.3%</td>
</tr>
<tr>
<td align="left">
Optimizer successes
<details>
<summary>ⓘ</summary>

The number of traces that were successfully optimized.
</details>
</td>
<td align="right">1,120</td>
<td align="right">100.0%</td>
<td align="right">2,640</td>
<td align="right">98.5%</td>
<td align="right">135.7%</td>
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
<td align="right">6,917,780</td>
<td align="right">75.4%</td>
<td align="right">35,939,540</td>
<td align="right">86.4%</td>
<td align="right">419.5%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">9,175,040</td>
<td align="right"></td>
<td align="right">41,615,360</td>
<td align="right"></td>
<td align="right">353.6%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">172,320</td>
<td align="right">1.9%</td>
<td align="right">729,280</td>
<td align="right">1.8%</td>
<td align="right">323.2%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">2,083,820</td>
<td align="right">22.7%</td>
<td align="right">4,943,900</td>
<td align="right">11.9%</td>
<td align="right">137.3%</td>
</tr>
<tr>
<td align="left">
Freed memory size
<details>
<summary>ⓘ</summary>

The size of the memory freed from the JIT traces
</details>
</td>
<td align="right">81,920</td>
<td align="right">0.9%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
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
<td align="left">440</td>
<td align="right">39.3%</td>
<td align="left">1,000</td>
<td align="right">37.9%</td>
<td align="right">127.3%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">420</td>
<td align="right">37.5%</td>
<td align="left">520</td>
<td align="right">19.7%</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">220</td>
<td align="right">19.6%</td>
<td align="left">620</td>
<td align="right">23.5%</td>
<td align="right">181.8%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">40</td>
<td align="right">3.6%</td>
<td align="left">180</td>
<td align="right">6.8%</td>
<td align="right">350.0%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">140</td>
<td align="right">5.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">180</td>
<td align="right">6.8%</td>
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
<td align="left"><= 32</td>
<td align="right">160</td>
<td align="right">14.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">520</td>
<td align="right">46.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">300</td>
<td align="right">26.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">140</td>
<td align="right">12.5%</td>
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
<td align="right">20</td>
<td align="right">1.8%</td>
<td align="right">420</td>
<td align="right">15.7%</td>
<td align="right">2,000.0%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">560</td>
<td align="right">50.0%</td>
<td align="right">640</td>
<td align="right">23.9%</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">340</td>
<td align="right">30.4%</td>
<td align="right">600</td>
<td align="right">22.4%</td>
<td align="right">76.5%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">200</td>
<td align="right">17.9%</td>
<td align="right">500</td>
<td align="right">18.7%</td>
<td align="right">150.0%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">60</td>
<td align="right">2.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">140</td>
<td align="right">5.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">220</td>
<td align="right">8.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">60</td>
<td align="right">2.2%</td>
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
<td align="left">_PUSH_FRAME</td>
<td align="right">7,960</td>
<td align="right">7,679,200</td>
<td align="right">96,372.4%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">7,960</td>
<td align="right">1,529,640</td>
<td align="right">19,116.6%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">7,960</td>
<td align="right">1,370,280</td>
<td align="right">17,114.6%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">7,960</td>
<td align="right">1,025,800</td>
<td align="right">12,786.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">7,960</td>
<td align="right">997,340</td>
<td align="right">12,429.4%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">7,960</td>
<td align="right">884,320</td>
<td align="right">11,009.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">10,800</td>
<td align="right">399,600</td>
<td align="right">3,600.0%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">41,360</td>
<td align="right">1,385,700</td>
<td align="right">3,250.3%</td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right">11,600</td>
<td align="right">253,420</td>
<td align="right">2,084.7%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">15,640</td>
<td align="right">279,080</td>
<td align="right">1,684.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">20,720</td>
<td align="right">286,620</td>
<td align="right">1,283.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">5,800</td>
<td align="right">76,920</td>
<td align="right">1,226.2%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">49,660</td>
<td align="right">454,300</td>
<td align="right">814.8%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">473,100</td>
<td align="right">3,437,900</td>
<td align="right">626.7%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">25,480</td>
<td align="right">132,960</td>
<td align="right">421.8%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">214,340</td>
<td align="right">1,058,140</td>
<td align="right">393.7%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">9,840</td>
<td align="right">46,120</td>
<td align="right">368.7%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">1,210,020</td>
<td align="right">5,464,940</td>
<td align="right">351.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right">60,040</td>
<td align="right">260,020</td>
<td align="right">333.1%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_ANY_SET</td>
<td align="right">43,940</td>
<td align="right">184,720</td>
<td align="right">320.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">465,660</td>
<td align="right">1,820,620</td>
<td align="right">291.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">171,900</td>
<td align="right">630,140</td>
<td align="right">266.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">190,900</td>
<td align="right">627,840</td>
<td align="right">228.9%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">2,580</td>
<td align="right">7,860</td>
<td align="right">204.7%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">2,580</td>
<td align="right">7,860</td>
<td align="right">204.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">2,580</td>
<td align="right">7,860</td>
<td align="right">204.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">584,680</td>
<td align="right">1,776,260</td>
<td align="right">203.8%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">482,140</td>
<td align="right">1,450,100</td>
<td align="right">200.8%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_OVERFLOWED</td>
<td align="right">190,540</td>
<td align="right">551,380</td>
<td align="right">189.4%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">482,140</td>
<td align="right">1,369,320</td>
<td align="right">184.0%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">7,012,800</td>
<td align="right">18,896,080</td>
<td align="right">169.5%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">29,700</td>
<td align="right">72,280</td>
<td align="right">143.4%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">3,297,280</td>
<td align="right">7,858,140</td>
<td align="right">138.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">5,494,640</td>
<td align="right">11,541,220</td>
<td align="right">110.0%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">2,878,480</td>
<td align="right">6,030,820</td>
<td align="right">109.5%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">1,036,620</td>
<td align="right">2,048,000</td>
<td align="right">97.6%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">36,640,700</td>
<td align="right">68,221,420</td>
<td align="right">86.2%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">48,886,920</td>
<td align="right">90,673,460</td>
<td align="right">85.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">1,618,880</td>
<td align="right">2,983,900</td>
<td align="right">84.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">51,080</td>
<td align="right">93,140</td>
<td align="right">82.3%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">117,260</td>
<td align="right">209,200</td>
<td align="right">78.4%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">12,415,560</td>
<td align="right">21,652,500</td>
<td align="right">74.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">623,340</td>
<td align="right">1,079,540</td>
<td align="right">73.2%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">628,220</td>
<td align="right">1,084,040</td>
<td align="right">72.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">777,240</td>
<td align="right">1,320,980</td>
<td align="right">70.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">1,044,520</td>
<td align="right">1,747,680</td>
<td align="right">67.3%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">157,940</td>
<td align="right">262,740</td>
<td align="right">66.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right">660,460</td>
<td align="right">1,086,300</td>
<td align="right">64.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">592,740</td>
<td align="right">955,200</td>
<td align="right">61.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">29,460</td>
<td align="right">47,460</td>
<td align="right">61.1%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">778,260</td>
<td align="right">1,212,020</td>
<td align="right">55.7%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">2,466,980</td>
<td align="right">3,766,160</td>
<td align="right">52.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">203,420</td>
<td align="right">97,160</td>
<td align="right">-52.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">17,460</td>
<td align="right">26,300</td>
<td align="right">50.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_SLICE</td>
<td align="right">17,460</td>
<td align="right">26,300</td>
<td align="right">50.6%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">16,209,060</td>
<td align="right">24,282,360</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">64,480</td>
<td align="right">96,120</td>
<td align="right">49.1%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">2,371,660</td>
<td align="right">3,487,320</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">1,447,420</td>
<td align="right">2,118,380</td>
<td align="right">46.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">1,485,940</td>
<td align="right">2,108,820</td>
<td align="right">41.9%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">149,160</td>
<td align="right">204,920</td>
<td align="right">37.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">2,548,100</td>
<td align="right">3,474,800</td>
<td align="right">36.4%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">12,365,900</td>
<td align="right">16,529,380</td>
<td align="right">33.7%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">594,420</td>
<td align="right">395,980</td>
<td align="right">-33.4%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">4,769,360</td>
<td align="right">6,333,860</td>
<td align="right">32.8%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">381,760</td>
<td align="right">506,720</td>
<td align="right">32.7%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">3,793,500</td>
<td align="right">2,629,900</td>
<td align="right">-30.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">887,340</td>
<td align="right">1,134,760</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">2,960,000</td>
<td align="right">3,775,500</td>
<td align="right">27.6%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">285,460</td>
<td align="right">363,260</td>
<td align="right">27.3%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">4,412,700</td>
<td align="right">5,540,360</td>
<td align="right">25.6%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">2,143,900</td>
<td align="right">2,689,600</td>
<td align="right">25.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">4,412,700</td>
<td align="right">5,532,480</td>
<td align="right">25.4%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">17,000</td>
<td align="right">21,240</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">2,565,040</td>
<td align="right">3,178,700</td>
<td align="right">23.9%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">406,420</td>
<td align="right">500,400</td>
<td align="right">23.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">73,760</td>
<td align="right">89,860</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">4,718,020</td>
<td align="right">5,743,740</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">1,715,600</td>
<td align="right">2,078,680</td>
<td align="right">21.2%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">1,851,000</td>
<td align="right">2,239,020</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">2,062,160</td>
<td align="right">2,478,220</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">5,258,140</td>
<td align="right">6,271,700</td>
<td align="right">19.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">2,960,880</td>
<td align="right">3,510,300</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">2,960,880</td>
<td align="right">3,509,140</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">1,118,580</td>
<td align="right">1,310,540</td>
<td align="right">17.2%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">3,998,840</td>
<td align="right">4,682,300</td>
<td align="right">17.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">4,751,660</td>
<td align="right">5,464,220</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">473,200</td>
<td align="right">406,180</td>
<td align="right">-14.2%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">2,177,580</td>
<td align="right">2,470,340</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">661,740</td>
<td align="right">573,700</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">3,038,160</td>
<td align="right">2,703,580</td>
<td align="right">-11.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">5,800</td>
<td align="right">6,380</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right">809,420</td>
<td align="right">877,140</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">1,122,780</td>
<td align="right">1,216,200</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">1,644,320</td>
<td align="right">1,777,520</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">2,756,400</td>
<td align="right">2,536,680</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">287,100</td>
<td align="right">309,640</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">1,092,380</td>
<td align="right">1,171,520</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">9,055,180</td>
<td align="right">9,706,880</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">1,619,580</td>
<td align="right">1,698,780</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_TUPLE</td>
<td align="right">240,720</td>
<td align="right">251,860</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_LIST</td>
<td align="right">41,380</td>
<td align="right">43,220</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">41,380</td>
<td align="right">43,220</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">350,820</td>
<td align="right">360,460</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">536,520</td>
<td align="right">550,660</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">963,360</td>
<td align="right">983,220</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">1,960</td>
<td align="right">1,920</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">838,500</td>
<td align="right">846,680</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,133,080</td>
<td align="right">1,141,100</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">1,871,860</td>
<td align="right">1,864,240</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">32,140</td>
<td align="right">32,020</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">1,733,740</td>
<td align="right">1,737,560</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">60,340</td>
<td align="right">60,240</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">14,860</td>
<td align="right">14,840</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">122,660</td>
<td align="right">122,500</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">195,200</td>
<td align="right">195,000</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">60,040</td>
<td align="right">59,980</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">596,560</td>
<td align="right">596,360</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">364,500</td>
<td align="right">364,560</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">7,960</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">10,688,780</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">6,050,300</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">4,668,300</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right"></td>
<td align="right">1,612,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right"></td>
<td align="right">1,571,840</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">1,302,040</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right"></td>
<td align="right">1,141,100</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right"></td>
<td align="right">771,660</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right"></td>
<td align="right">590,000</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">556,180</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right"></td>
<td align="right">508,120</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right"></td>
<td align="right">505,780</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right"></td>
<td align="right">483,140</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right"></td>
<td align="right">387,180</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right">378,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right"></td>
<td align="right">361,020</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LEN</td>
<td align="right"></td>
<td align="right">358,660</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_1</td>
<td align="right"></td>
<td align="right">321,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right"></td>
<td align="right">316,060</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right"></td>
<td align="right">288,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right"></td>
<td align="right">231,220</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">215,480</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right"></td>
<td align="right">215,280</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS</td>
<td align="right"></td>
<td align="right">215,280</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right"></td>
<td align="right">183,600</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right"></td>
<td align="right">182,180</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION_AND_LOCK</td>
<td align="right"></td>
<td align="right">182,180</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">182,180</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_PROPERTY_FRAME</td>
<td align="right"></td>
<td align="right">159,360</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">158,580</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right"></td>
<td align="right">145,180</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right"></td>
<td align="right">135,700</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right"></td>
<td align="right">121,220</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right"></td>
<td align="right">108,800</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right"></td>
<td align="right">89,480</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right"></td>
<td align="right">89,480</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_FOR</td>
<td align="right"></td>
<td align="right">89,420</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right"></td>
<td align="right">80,820</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right"></td>
<td align="right">79,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_0</td>
<td align="right"></td>
<td align="right">75,220</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SEND_GEN_FRAME</td>
<td align="right"></td>
<td align="right">62,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right"></td>
<td align="right">61,960</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right"></td>
<td align="right">61,960</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PY_FRAME_GENERAL</td>
<td align="right"></td>
<td align="right">60,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right"></td>
<td align="right">50,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right"></td>
<td align="right">43,380</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">42,800</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_INIT_CHECK</td>
<td align="right"></td>
<td align="right">38,640</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_AND_ALLOCATE_OBJECT</td>
<td align="right"></td>
<td align="right">38,640</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CREATE_INIT_FRAME</td>
<td align="right"></td>
<td align="right">38,640</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right"></td>
<td align="right">38,240</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right"></td>
<td align="right">37,040</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right"></td>
<td align="right">36,960</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right"></td>
<td align="right">36,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right"></td>
<td align="right">28,780</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_TUPLE_1</td>
<td align="right"></td>
<td align="right">28,780</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NULL</td>
<td align="right"></td>
<td align="right">28,780</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_2</td>
<td align="right"></td>
<td align="right">28,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">28,360</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_SEND</td>
<td align="right"></td>
<td align="right">25,280</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">21,680</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right"></td>
<td align="right">19,980</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right"></td>
<td align="right">19,900</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right"></td>
<td align="right">18,200</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">16,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SWAP_3</td>
<td align="right"></td>
<td align="right">14,280</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right"></td>
<td align="right">12,280</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE</td>
<td align="right"></td>
<td align="right">6,320</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_2</td>
<td align="right"></td>
<td align="right">5,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right"></td>
<td align="right">5,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right"></td>
<td align="right">5,320</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right"></td>
<td align="right">3,500</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right"></td>
<td align="right">2,760</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right"></td>
<td align="right">2,760</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT</td>
<td align="right"></td>
<td align="right">2,760</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right"></td>
<td align="right">1,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right"></td>
<td align="right">1,080</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right"></td>
<td align="right">520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_KW_NON_PY</td>
<td align="right"></td>
<td align="right">480</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE_KW</td>
<td align="right"></td>
<td align="right">480</td>
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
<td align="left">CALL</td>
<td align="right">40</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">20</td>
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
Stats gathered on: 2025-10-22
