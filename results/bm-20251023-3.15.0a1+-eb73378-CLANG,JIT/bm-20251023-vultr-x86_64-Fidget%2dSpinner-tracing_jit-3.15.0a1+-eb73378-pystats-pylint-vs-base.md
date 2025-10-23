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
<td align="right">13,463,400</td>
<td align="right">360.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">796,380</td>
<td align="right">59,460</td>
<td align="right">-92.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">18,697,912</td>
<td align="right">6,537,817</td>
<td align="right">-65.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,064,720</td>
<td align="right">471,580</td>
<td align="right">-55.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">646,140</td>
<td align="right">288,160</td>
<td align="right">-55.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">4,374,492</td>
<td align="right">2,104,257</td>
<td align="right">-51.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">603,140</td>
<td align="right">305,860</td>
<td align="right">-49.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">476,400</td>
<td align="right">255,140</td>
<td align="right">-46.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">3,433,452</td>
<td align="right">1,901,297</td>
<td align="right">-44.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">4,364,620</td>
<td align="right">2,423,000</td>
<td align="right">-44.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">13,608,780</td>
<td align="right">7,671,160</td>
<td align="right">-43.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">216,580</td>
<td align="right">140,600</td>
<td align="right">-35.1%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">3,708,640</td>
<td align="right">2,467,620</td>
<td align="right">-33.5%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">2,273,012</td>
<td align="right">1,531,877</td>
<td align="right">-32.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,410,860</td>
<td align="right">1,668,240</td>
<td align="right">-30.8%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">2,264,600</td>
<td align="right">1,570,980</td>
<td align="right">-30.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">1,570,780</td>
<td align="right">1,094,360</td>
<td align="right">-30.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">9,127,772</td>
<td align="right">6,376,697</td>
<td align="right">-30.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">617,380</td>
<td align="right">455,160</td>
<td align="right">-26.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">2,283,332</td>
<td align="right">1,692,337</td>
<td align="right">-25.9%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,546,840</td>
<td align="right">5,701,540</td>
<td align="right">-24.5%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">6,000,200</td>
<td align="right">4,555,020</td>
<td align="right">-24.1%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,650,340</td>
<td align="right">1,254,360</td>
<td align="right">-24.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">1,314,060</td>
<td align="right">1,000,680</td>
<td align="right">-23.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">6,457,860</td>
<td align="right">4,958,440</td>
<td align="right">-23.2%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">8,286,620</td>
<td align="right">6,388,880</td>
<td align="right">-22.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">3,256,160</td>
<td align="right">2,550,980</td>
<td align="right">-21.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">6,473,440</td>
<td align="right">5,079,380</td>
<td align="right">-21.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">156,000</td>
<td align="right">126,720</td>
<td align="right">-18.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">1,957,940</td>
<td align="right">1,599,340</td>
<td align="right">-18.3%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">2,466,360</td>
<td align="right">2,038,020</td>
<td align="right">-17.4%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">178,560</td>
<td align="right">149,780</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">39,342,280</td>
<td align="right">33,335,580</td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">6,647,000</td>
<td align="right">5,640,520</td>
<td align="right">-15.1%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">10,898,580</td>
<td align="right">9,449,140</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">749,300</td>
<td align="right">658,900</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">751,840</td>
<td align="right">661,440</td>
<td align="right">-12.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">956,960</td>
<td align="right">846,620</td>
<td align="right">-11.5%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">3,159,400</td>
<td align="right">2,808,900</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">27,052,112</td>
<td align="right">24,058,557</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">536,720</td>
<td align="right">478,820</td>
<td align="right">-10.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">16,906,124</td>
<td align="right">15,091,814</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">1,102,500</td>
<td align="right">984,840</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">867,140</td>
<td align="right">774,920</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">3,333,600</td>
<td align="right">2,987,420</td>
<td align="right">-10.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">760,640</td>
<td align="right">686,640</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">152,650,624</td>
<td align="right">137,858,874</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">34,052,700</td>
<td align="right">30,993,140</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">2,417,720</td>
<td align="right">2,201,240</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">39,203,620</td>
<td align="right">35,832,880</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">51,190,940</td>
<td align="right">46,854,900</td>
<td align="right">-8.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">4,201,220</td>
<td align="right">3,851,800</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">12,424,780</td>
<td align="right">11,417,140</td>
<td align="right">-8.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">26,459,560</td>
<td align="right">24,390,400</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">1,084,040</td>
<td align="right">1,002,380</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">565,940</td>
<td align="right">526,220</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">23,350,080</td>
<td align="right">21,802,320</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">3,804,840</td>
<td align="right">3,557,160</td>
<td align="right">-6.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">2,576,300</td>
<td align="right">2,416,220</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">3,402,620</td>
<td align="right">3,193,340</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">2,559,800</td>
<td align="right">2,402,760</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">27,722,060</td>
<td align="right">26,036,520</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">3,860,780</td>
<td align="right">3,626,200</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,831,000</td>
<td align="right">1,729,020</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">8,558,312</td>
<td align="right">8,082,937</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">1,471,200</td>
<td align="right">1,391,800</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">743,640</td>
<td align="right">703,940</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">5,778,080</td>
<td align="right">5,474,140</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">40,877,060</td>
<td align="right">38,976,660</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">5,170,420</td>
<td align="right">4,936,900</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">598,720</td>
<td align="right">571,960</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">439,080</td>
<td align="right">419,660</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">2,061,000</td>
<td align="right">1,969,880</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">13,509,300</td>
<td align="right">12,929,580</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">234,600</td>
<td align="right">224,620</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">13,041,460</td>
<td align="right">12,488,880</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">2,644,080</td>
<td align="right">2,534,020</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">901,920</td>
<td align="right">864,880</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">233,460</td>
<td align="right">223,960</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">1,358,660</td>
<td align="right">1,304,620</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">1,709,340</td>
<td align="right">1,643,720</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">51,541,460</td>
<td align="right">49,672,180</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">8,962,920</td>
<td align="right">8,676,100</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">23,024,520</td>
<td align="right">22,294,500</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">8,037,680</td>
<td align="right">7,802,560</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">24,006,580</td>
<td align="right">23,315,980</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">838,800</td>
<td align="right">814,680</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">11,133,920</td>
<td align="right">10,860,900</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">1,835,640</td>
<td align="right">1,792,380</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,783,340</td>
<td align="right">1,742,180</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">59,600</td>
<td align="right">58,400</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">11,109,660</td>
<td align="right">10,900,260</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,036,340</td>
<td align="right">6,908,740</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">20,728,000</td>
<td align="right">20,361,920</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">3,410,840</td>
<td align="right">3,350,700</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">1,843,620</td>
<td align="right">1,811,580</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">4,117,280</td>
<td align="right">4,047,480</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">2,572,080</td>
<td align="right">2,532,920</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">404,160</td>
<td align="right">398,040</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">6,682,440</td>
<td align="right">6,597,240</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">7,717,980</td>
<td align="right">7,620,260</td>
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
<td align="left">CALL_TYPE_1</td>
<td align="right">222,880</td>
<td align="right">220,320</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">10,443,480</td>
<td align="right">10,331,760</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">4,929,960</td>
<td align="right">4,880,020</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">789,000</td>
<td align="right">782,160</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">3,440,220</td>
<td align="right">3,410,860</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">1,426,860</td>
<td align="right">1,414,880</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">1,605,120</td>
<td align="right">1,593,140</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">17,321,932</td>
<td align="right">17,208,517</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">5,048,220</td>
<td align="right">5,015,540</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">1,273,140</td>
<td align="right">1,269,900</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">1,718,632</td>
<td align="right">1,722,797</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">2,249,020</td>
<td align="right">2,244,320</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">5,134,140</td>
<td align="right">5,126,940</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">61,800</td>
<td align="right">61,820</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">6,490,100</td>
<td align="right">6,490,260</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">7,620,240</td>
<td align="right">7,620,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">6,068,700</td>
<td align="right">6,068,700</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">1,190,080</td>
<td align="right">1,190,080</td>
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
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">227,160</td>
<td align="right">227,160</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">57,780</td>
<td align="right">0.2%</td>
<td align="right">19,620</td>
<td align="right">0.1%</td>
<td align="right">-66.0%</td>
</tr>
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
<td align="right">1,653,060</td>
<td align="right">7.2%</td>
<td align="right">-31.2%</td>
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
<td align="right">21,359,120</td>
<td align="right">92.7%</td>
<td align="right">0.3%</td>
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
<td align="right">13,880</td>
<td align="right">89.3%</td>
<td align="right">129.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,380</td>
<td align="right">28.2%</td>
<td align="right">1,660</td>
<td align="right">10.7%</td>
<td align="right">-30.3%</td>
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
<td align="right">8,760</td>
<td align="right">63.1%</td>
<td align="right">1,312.9%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">2,440</td>
<td align="right">40.3%</td>
<td align="right">2,040</td>
<td align="right">14.7%</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">140</td>
<td align="right">2.3%</td>
<td align="right">160</td>
<td align="right">1.2%</td>
<td align="right">14.3%</td>
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
<td align="right">660</td>
<td align="right">4.8%</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">660</td>
<td align="right">10.9%</td>
<td align="right">620</td>
<td align="right">4.5%</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">800</td>
<td align="right">13.2%</td>
<td align="right">820</td>
<td align="right">5.9%</td>
<td align="right">2.5%</td>
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
<td align="right">478,820</td>
<td align="right">100.0%</td>
<td align="right">-10.8%</td>
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
<td align="right">10,740</td>
<td align="right">0.0%</td>
<td align="right">34.2%</td>
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
<td align="right">6,753,940</td>
<td align="right">11.4%</td>
<td align="right">-2.4%</td>
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
<td align="right">6,885,760</td>
<td align="right">11.6%</td>
<td align="right">-2.4%</td>
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
<td align="right">52,596,780</td>
<td align="right">88.4%</td>
<td align="right">0.7%</td>
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
<td align="right">146,600</td>
<td align="right">100.0%</td>
<td align="right">-0.7%</td>
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
<td align="right">681,860</td>
<td align="right">4.3%</td>
<td align="right">-10.0%</td>
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
<td align="right">95.6%</td>
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
<td align="right">3,900</td>
<td align="right">80.9%</td>
<td align="right">95.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">920</td>
<td align="right">31.5%</td>
<td align="right">920</td>
<td align="right">19.1%</td>
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
<td align="right">2,340</td>
<td align="right">60.0%</td>
<td align="right">408.7%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">120</td>
<td align="right">6.0%</td>
<td align="right">140</td>
<td align="right">3.6%</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">920</td>
<td align="right">46.0%</td>
<td align="right">920</td>
<td align="right">23.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">220</td>
<td align="right">11.0%</td>
<td align="right">220</td>
<td align="right">5.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">120</td>
<td align="right">6.0%</td>
<td align="right">120</td>
<td align="right">3.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">80</td>
<td align="right">4.0%</td>
<td align="right">80</td>
<td align="right">2.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">40</td>
<td align="right">2.0%</td>
<td align="right">40</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">40</td>
<td align="right">2.0%</td>
<td align="right">40</td>
<td align="right">1.0%</td>
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
<td align="right">2,277,492</td>
<td align="right">38.3%</td>
<td align="right">1,685,537</td>
<td align="right">31.5%</td>
<td align="right">-26.0%</td>
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
<td align="right">67.9%</td>
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
<td align="right">0.5%</td>
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
<td align="right">6,300</td>
<td align="right">86.5%</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">980</td>
<td align="right">15.5%</td>
<td align="right">980</td>
<td align="right">13.5%</td>
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
<td align="right">2,860</td>
<td align="right">53.6%</td>
<td align="right">3,640</td>
<td align="right">57.8%</td>
<td align="right">27.3%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">1,000</td>
<td align="right">18.7%</td>
<td align="right">1,160</td>
<td align="right">18.4%</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">400</td>
<td align="right">7.5%</td>
<td align="right">420</td>
<td align="right">6.7%</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">1,080</td>
<td align="right">20.2%</td>
<td align="right">1,080</td>
<td align="right">17.1%</td>
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
<td align="right">2,405,120</td>
<td align="right">9.9%</td>
<td align="right">-44.8%</td>
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
<td align="right">145,420</td>
<td align="right">0.6%</td>
<td align="right">-31.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">24,718,052</td>
<td align="right">84.4%</td>
<td align="right">21,663,077</td>
<td align="right">89.4%</td>
<td align="right">-12.4%</td>
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
<td align="right">7,600</td>
<td align="right">62.7%</td>
<td align="right">17,360</td>
<td align="right">84.0%</td>
<td align="right">128.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">4,520</td>
<td align="right">37.3%</td>
<td align="right">3,300</td>
<td align="right">16.0%</td>
<td align="right">-27.0%</td>
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
<td align="right">12,660</td>
<td align="right">72.9%</td>
<td align="right">1,094.3%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">3,880</td>
<td align="right">51.1%</td>
<td align="right">1,980</td>
<td align="right">11.4%</td>
<td align="right">-49.0%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">200</td>
<td align="right">2.6%</td>
<td align="right">240</td>
<td align="right">1.4%</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">140</td>
<td align="right">1.8%</td>
<td align="right">160</td>
<td align="right">0.9%</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">1,180</td>
<td align="right">15.5%</td>
<td align="right">1,180</td>
<td align="right">6.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">500</td>
<td align="right">6.6%</td>
<td align="right">500</td>
<td align="right">2.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">260</td>
<td align="right">3.4%</td>
<td align="right">260</td>
<td align="right">1.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">220</td>
<td align="right">2.9%</td>
<td align="right">220</td>
<td align="right">1.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">120</td>
<td align="right">1.6%</td>
<td align="right">120</td>
<td align="right">0.7%</td>
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
<td align="right">200,160</td>
<td align="right">0.2%</td>
<td align="right">11.2%</td>
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
<td align="right">11,300,100</td>
<td align="right">10.4%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">29,680,206</td>
<td align="right">26.8%</td>
<td align="right">29,252,960</td>
<td align="right">26.8%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">68,610,458</td>
<td align="right">62.0%</td>
<td align="right">68,480,114</td>
<td align="right">62.7%</td>
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
<td align="left">Failure</td>
<td align="right">64,320</td>
<td align="right">10.1%</td>
<td align="right">83,320</td>
<td align="right">12.5%</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">572,560</td>
<td align="right">89.9%</td>
<td align="right">582,940</td>
<td align="right">87.5%</td>
<td align="right">1.8%</td>
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
<td align="right">4,380</td>
<td align="right">5.3%</td>
<td align="right">742.3%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">3,040</td>
<td align="right">4.7%</td>
<td align="right">7,540</td>
<td align="right">9.0%</td>
<td align="right">148.0%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">2,800</td>
<td align="right">4.4%</td>
<td align="right">4,400</td>
<td align="right">5.3%</td>
<td align="right">57.1%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">680</td>
<td align="right">1.1%</td>
<td align="right">820</td>
<td align="right">1.0%</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">180</td>
<td align="right">0.3%</td>
<td align="right">200</td>
<td align="right">0.2%</td>
<td align="right">11.1%</td>
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
<td align="right">1,400</td>
<td align="right">1.7%</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">740</td>
<td align="right">1.2%</td>
<td align="right">740</td>
<td align="right">0.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">480</td>
<td align="right">0.7%</td>
<td align="right">480</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">200</td>
<td align="right">0.3%</td>
<td align="right">200</td>
<td align="right">0.2%</td>
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
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">40</td>
<td align="right">0.0%</td>
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
<td align="right">46,651,160</td>
<td align="right">100.0%</td>
<td align="right">-6.3%</td>
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
<td align="left">Success</td>
<td align="right">60</td>
<td align="right">2.4%</td>
<td align="right">60</td>
<td align="right">2.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">2,400</td>
<td align="right">97.6%</td>
<td align="right">2,400</td>
<td align="right">97.6%</td>
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
<td align="right">660</td>
<td align="right">27.5%</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">1,720</td>
<td align="right">71.7%</td>
<td align="right">1,700</td>
<td align="right">70.8%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">40</td>
<td align="right">1.7%</td>
<td align="right">40</td>
<td align="right">1.7%</td>
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
<td align="right">1,184,180</td>
<td align="right">10.3%</td>
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
<td align="right">9,263,720</td>
<td align="right">80.5%</td>
<td align="right">9,263,720</td>
<td align="right">80.5%</td>
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
<td align="left">Success</td>
<td align="right">23,480</td>
<td align="right">91.1%</td>
<td align="right">23,480</td>
<td align="right">91.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">2,280</td>
<td align="right">8.9%</td>
<td align="right">2,280</td>
<td align="right">8.9%</td>
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
<td align="right">61,560</td>
<td align="right">2,700.0%</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1,020</td>
<td align="right">44.7%</td>
<td align="right">1,020</td>
<td align="right">44.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">480</td>
<td align="right">21.1%</td>
<td align="right">480</td>
<td align="right">21.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">380</td>
<td align="right">16.7%</td>
<td align="right">380</td>
<td align="right">16.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">200</td>
<td align="right">8.8%</td>
<td align="right">200</td>
<td align="right">8.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">120</td>
<td align="right">5.3%</td>
<td align="right">120</td>
<td align="right">5.3%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">555,080</td>
<td align="right">1.5%</td>
<td align="right">514,580</td>
<td align="right">1.4%</td>
<td align="right">-7.3%</td>
</tr>
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
<td align="right">2,688,200</td>
<td align="right">7.1%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">34,813,612</td>
<td align="right">91.3%</td>
<td align="right">34,492,517</td>
<td align="right">91.5%</td>
<td align="right">-0.9%</td>
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
<td align="right">320</td>
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
<td align="right">5,720</td>
<td align="right">9.2%</td>
<td align="right">6,500</td>
<td align="right">10.4%</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">56,560</td>
<td align="right">90.8%</td>
<td align="right">55,940</td>
<td align="right">89.6%</td>
<td align="right">-1.1%</td>
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
<td align="right">4,200</td>
<td align="right">64.6%</td>
<td align="right">22.8%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">780</td>
<td align="right">13.6%</td>
<td align="right">780</td>
<td align="right">12.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">600</td>
<td align="right">10.5%</td>
<td align="right">600</td>
<td align="right">9.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">520</td>
<td align="right">9.1%</td>
<td align="right">520</td>
<td align="right">8.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">260</td>
<td align="right">4.5%</td>
<td align="right">260</td>
<td align="right">4.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">80</td>
<td align="right">1.4%</td>
<td align="right">80</td>
<td align="right">1.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">40</td>
<td align="right">0.7%</td>
<td align="right">40</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">20</td>
<td align="right">0.3%</td>
<td align="right">20</td>
<td align="right">0.3%</td>
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
<td align="right">795,600</td>
<td align="right">10.9%</td>
<td align="right">58,680</td>
<td align="right">0.9%</td>
<td align="right">-92.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,497,892</td>
<td align="right">89.1%</td>
<td align="right">6,496,497</td>
<td align="right">99.1%</td>
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
<td align="left">Success</td>
<td align="right">580</td>
<td align="right">74.4%</td>
<td align="right">580</td>
<td align="right">74.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">200</td>
<td align="right">25.6%</td>
<td align="right">200</td>
<td align="right">25.6%</td>
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
<td align="right">180</td>
<td align="right">90.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">20</td>
<td align="right">10.0%</td>
<td align="right">20</td>
<td align="right">10.0%</td>
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
<td align="right">352,168,358</td>
<td align="right">34.8%</td>
<td align="right">306,895,919</td>
<td align="right">33.3%</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">42,639,332</td>
<td align="right">4.2%</td>
<td align="right">37,174,897</td>
<td align="right">4.0%</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">576,735,432</td>
<td align="right">56.9%</td>
<td align="right">536,192,022</td>
<td align="right">58.2%</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">41,367,506</td>
<td align="right">4.1%</td>
<td align="right">40,621,780</td>
<td align="right">4.4%</td>
<td align="right">-1.8%</td>
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
<td align="right">2,405,120</td>
<td align="right">7.2%</td>
<td align="right">-44.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,403,500</td>
<td align="right">6.2%</td>
<td align="right">1,653,060</td>
<td align="right">5.0%</td>
<td align="right">-31.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">2,277,492</td>
<td align="right">5.9%</td>
<td align="right">1,685,537</td>
<td align="right">5.0%</td>
<td align="right">-26.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">757,760</td>
<td align="right">2.0%</td>
<td align="right">681,860</td>
<td align="right">2.0%</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">12,314,580</td>
<td align="right">31.8%</td>
<td align="right">11,300,100</td>
<td align="right">33.8%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">555,080</td>
<td align="right">1.4%</td>
<td align="right">514,580</td>
<td align="right">1.5%</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">6,919,160</td>
<td align="right">17.8%</td>
<td align="right">6,753,940</td>
<td align="right">20.2%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">6,066,240</td>
<td align="right">15.6%</td>
<td align="right">6,066,240</td>
<td align="right">18.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">1,184,180</td>
<td align="right">3.1%</td>
<td align="right">1,184,180</td>
<td align="right">3.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">795,600</td>
<td align="right">2.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">531,920</td>
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
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">1,300,300</td>
<td align="right">3.1%</td>
<td align="right">1,031,640</td>
<td align="right">2.5%</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">819,080</td>
<td align="right">2.0%</td>
<td align="right">749,520</td>
<td align="right">1.8%</td>
<td align="right">-8.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">2,916,280</td>
<td align="right">7.0%</td>
<td align="right">2,754,280</td>
<td align="right">6.8%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">2,387,980</td>
<td align="right">5.8%</td>
<td align="right">2,331,740</td>
<td align="right">5.7%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">5,033,640</td>
<td align="right">12.2%</td>
<td align="right">5,140,860</td>
<td align="right">12.7%</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">14,961,220</td>
<td align="right">36.2%</td>
<td align="right">14,739,120</td>
<td align="right">36.3%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">5,982,920</td>
<td align="right">14.5%</td>
<td align="right">6,034,620</td>
<td align="right">14.9%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,944,380</td>
<td align="right">12.0%</td>
<td align="right">4,919,160</td>
<td align="right">12.1%</td>
<td align="right">-0.5%</td>
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
<td align="right">1,825,000</td>
<td align="right">3.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">6,690,180</td>
<td align="right">10.8%</td>
<td align="right">6,690,340</td>
<td align="right">10.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">6,690,180</td>
<td align="right">10.8%</td>
<td align="right">6,690,340</td>
<td align="right">10.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">55,110,000</td>
<td align="right">89.2%</td>
<td align="right">55,109,840</td>
<td align="right">89.2%</td>
<td align="right">-0.0%</td>
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
<td align="right">222,619</td>
<td align="right"></td>
<td align="right">199,130</td>
<td align="right"></td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">223,650,942</td>
<td align="right">33.7%</td>
<td align="right">206,103,848</td>
<td align="right">31.2%</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">1,561,665</td>
<td align="right"></td>
<td align="right">1,447,365</td>
<td align="right"></td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">249,715,997</td>
<td align="right">37.7%</td>
<td align="right">266,654,339</td>
<td align="right">40.4%</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">1,339,647</td>
<td align="right"></td>
<td align="right">1,248,852</td>
<td align="right"></td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">230,872,096</td>
<td align="right">33.9%</td>
<td align="right">245,955,688</td>
<td align="right">36.2%</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">307,598,508</td>
<td align="right">45.2%</td>
<td align="right">291,905,728</td>
<td align="right">43.0%</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">27,260</td>
<td align="right">0.0%</td>
<td align="right">28,160</td>
<td align="right">0.0%</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">35,761,340</td>
<td align="right">5.4%</td>
<td align="right">34,988,140</td>
<td align="right">5.3%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">48,609,385</td>
<td align="right"></td>
<td align="right">47,738,028</td>
<td align="right"></td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">24,584,100</td>
<td align="right">3.6%</td>
<td align="right">24,282,900</td>
<td align="right">3.6%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">117,420,763</td>
<td align="right">17.3%</td>
<td align="right">116,613,233</td>
<td align="right">17.2%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">286,380</td>
<td align="right">0.4%</td>
<td align="right">288,080</td>
<td align="right">0.4%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">153,652,913</td>
<td align="right">23.2%</td>
<td align="right">152,955,167</td>
<td align="right">23.2%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">25,960,221</td>
<td align="right"></td>
<td align="right">25,979,310</td>
<td align="right"></td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">39,419,575</td>
<td align="right"></td>
<td align="right">39,416,935</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">39,439,560</td>
<td align="right">52.6%</td>
<td align="right">39,438,196</td>
<td align="right">52.6%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">39,753,200</td>
<td align="right">53.0%</td>
<td align="right">39,754,436</td>
<td align="right">53.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">35,259,680</td>
<td align="right">47.0%</td>
<td align="right">35,259,160</td>
<td align="right">47.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">35,282,540</td>
<td align="right"></td>
<td align="right">35,282,020</td>
<td align="right"></td>
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
<td align="right">60,919,472</td>
<td align="right">8,948,987</td>
<td align="right">1,842,793</td>
<td align="right">1,060</td>
<td align="right">19,460</td>
<td align="right">60,986,516</td>
<td align="right">8,951,731</td>
<td align="right">1,840,829</td>
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
<td align="right">155,380</td>
<td align="right"></td>
<td align="right">3,480.2%</td>
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
<td align="right">660</td>
<td align="right">0.4%</td>
<td align="right">1,550.0%</td>
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
<td align="right">4,280</td>
<td align="right">2.8%</td>
<td align="right">282.1%</td>
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
<td align="right">565,173,580</td>
<td align="right">1,729.9%</td>
<td align="right">115.7%</td>
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
<td align="right">32,671,060</td>
<td align="right"></td>
<td align="right">113.6%</td>
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
<td align="right">540</td>
<td align="right">0.3%</td>
<td align="right">540 / 0 !!</td>
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
<td align="right">4,280</td>
<td align="right"></td>
<td align="right">282.1%</td>
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
<td align="right">3,740</td>
<td align="right">87.4%</td>
<td align="right">233.9%</td>
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
<td align="right">48,079,680</td>
<td align="right">85.1%</td>
<td align="right">595.0%</td>
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
<td align="right">56,524,800</td>
<td align="right"></td>
<td align="right">516.1%</td>
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
<td align="right">978,240</td>
<td align="right">1.7%</td>
<td align="right">467.7%</td>
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
<td align="right">7,463,140</td>
<td align="right">13.2%</td>
<td align="right">258.1%</td>
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
<td align="left">1,540</td>
<td align="right">41.2%</td>
<td align="right">250.0%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">420</td>
<td align="right">37.5%</td>
<td align="left">700</td>
<td align="right">18.7%</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">220</td>
<td align="right">19.6%</td>
<td align="left">740</td>
<td align="right">19.8%</td>
<td align="right">236.4%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">40</td>
<td align="right">3.6%</td>
<td align="left">340</td>
<td align="right">9.1%</td>
<td align="right">750.0%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">300</td>
<td align="right">8.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">120</td>
<td align="right">3.2%</td>
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
<td align="right">860</td>
<td align="right">20.1%</td>
<td align="right">4,200.0%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">560</td>
<td align="right">50.0%</td>
<td align="right">880</td>
<td align="right">20.6%</td>
<td align="right">57.1%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">340</td>
<td align="right">30.4%</td>
<td align="right">680</td>
<td align="right">15.9%</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">200</td>
<td align="right">17.9%</td>
<td align="right">600</td>
<td align="right">14.0%</td>
<td align="right">200.0%</td>
</tr>
<tr>
<td align="left"><= 4</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">20</td>
<td align="right">0.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">440</td>
<td align="right">10.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">140</td>
<td align="right">3.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">120</td>
<td align="right">2.8%</td>
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
<td align="right">7,658,320</td>
<td align="right">96,110.1%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">7,960</td>
<td align="right">1,568,380</td>
<td align="right">19,603.3%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">7,960</td>
<td align="right">1,458,320</td>
<td align="right">18,220.6%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">7,960</td>
<td align="right">894,140</td>
<td align="right">11,132.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">7,960</td>
<td align="right">858,580</td>
<td align="right">10,686.2%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">7,960</td>
<td align="right">774,840</td>
<td align="right">9,634.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">10,800</td>
<td align="right">541,860</td>
<td align="right">4,917.2%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">41,360</td>
<td align="right">1,886,660</td>
<td align="right">4,461.6%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">51,080</td>
<td align="right">1,430,360</td>
<td align="right">2,700.2%</td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right">11,600</td>
<td align="right">274,880</td>
<td align="right">2,269.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">5,800</td>
<td align="right">116,140</td>
<td align="right">1,902.4%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">15,640</td>
<td align="right">288,660</td>
<td align="right">1,745.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">20,720</td>
<td align="right">218,300</td>
<td align="right">953.6%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">2,580</td>
<td align="right">26,700</td>
<td align="right">934.9%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">2,580</td>
<td align="right">26,700</td>
<td align="right">934.9%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">2,580</td>
<td align="right">26,580</td>
<td align="right">930.2%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">473,100</td>
<td align="right">3,922,520</td>
<td align="right">729.1%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">25,480</td>
<td align="right">182,520</td>
<td align="right">616.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">5,800</td>
<td align="right">31,180</td>
<td align="right">437.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">171,900</td>
<td align="right">887,020</td>
<td align="right">416.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right">60,040</td>
<td align="right">306,500</td>
<td align="right">410.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">465,660</td>
<td align="right">2,317,780</td>
<td align="right">397.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">190,900</td>
<td align="right">928,020</td>
<td align="right">386.1%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">214,340</td>
<td align="right">1,004,520</td>
<td align="right">368.7%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">9,840</td>
<td align="right">41,880</td>
<td align="right">325.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_ANY_SET</td>
<td align="right">43,940</td>
<td align="right">184,740</td>
<td align="right">320.4%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">1,210,020</td>
<td align="right">4,910,720</td>
<td align="right">305.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">157,940</td>
<td align="right">621,980</td>
<td align="right">293.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">584,680</td>
<td align="right">2,081,360</td>
<td align="right">256.0%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">17,000</td>
<td align="right">58,160</td>
<td align="right">242.1%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">29,700</td>
<td align="right">100,240</td>
<td align="right">237.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">149,160</td>
<td align="right">498,600</td>
<td align="right">234.3%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">482,140</td>
<td align="right">1,475,940</td>
<td align="right">206.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">482,140</td>
<td align="right">1,475,340</td>
<td align="right">206.0%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">364,500</td>
<td align="right">1,101,420</td>
<td align="right">202.2%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">2,878,480</td>
<td align="right">8,654,020</td>
<td align="right">200.6%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">1,036,620</td>
<td align="right">3,060,620</td>
<td align="right">195.2%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">7,012,800</td>
<td align="right">20,565,220</td>
<td align="right">193.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">592,740</td>
<td align="right">1,711,440</td>
<td align="right">188.7%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">3,297,280</td>
<td align="right">9,427,260</td>
<td align="right">185.9%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">195,200</td>
<td align="right">553,180</td>
<td align="right">183.4%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">32,140</td>
<td align="right">90,040</td>
<td align="right">180.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_OVERFLOWED</td>
<td align="right">190,540</td>
<td align="right">532,040</td>
<td align="right">179.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">17,460</td>
<td align="right">46,740</td>
<td align="right">167.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_SLICE</td>
<td align="right">17,460</td>
<td align="right">46,740</td>
<td align="right">167.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">29,460</td>
<td align="right">76,840</td>
<td align="right">160.8%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">49,660</td>
<td align="right">128,820</td>
<td align="right">159.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">777,240</td>
<td align="right">1,892,560</td>
<td align="right">143.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">1,733,740</td>
<td align="right">4,149,740</td>
<td align="right">139.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">5,494,640</td>
<td align="right">13,027,440</td>
<td align="right">137.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">122,660</td>
<td align="right">284,880</td>
<td align="right">132.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">1,618,880</td>
<td align="right">3,742,140</td>
<td align="right">131.2%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">778,260</td>
<td align="right">1,784,740</td>
<td align="right">129.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right">660,460</td>
<td align="right">1,501,600</td>
<td align="right">127.4%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">64,480</td>
<td align="right">146,140</td>
<td align="right">126.6%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">60,040</td>
<td align="right">136,060</td>
<td align="right">126.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">60,340</td>
<td align="right">136,340</td>
<td align="right">126.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">1,118,580</td>
<td align="right">2,512,640</td>
<td align="right">124.6%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">36,640,700</td>
<td align="right">81,602,440</td>
<td align="right">122.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">623,340</td>
<td align="right">1,383,700</td>
<td align="right">122.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">73,760</td>
<td align="right">162,540</td>
<td align="right">120.4%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">48,886,920</td>
<td align="right">105,605,980</td>
<td align="right">116.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">963,360</td>
<td align="right">2,060,360</td>
<td align="right">113.9%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_LIST</td>
<td align="right">41,380</td>
<td align="right">84,640</td>
<td align="right">104.5%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">41,380</td>
<td align="right">84,640</td>
<td align="right">104.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_TUPLE</td>
<td align="right">240,720</td>
<td align="right">486,480</td>
<td align="right">102.1%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">2,143,900</td>
<td align="right">4,280,960</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">1,644,320</td>
<td align="right">3,245,080</td>
<td align="right">97.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">1,871,860</td>
<td align="right">3,634,260</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">12,415,560</td>
<td align="right">24,017,040</td>
<td align="right">93.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">350,820</td>
<td align="right">664,200</td>
<td align="right">89.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">2,548,100</td>
<td align="right">4,819,600</td>
<td align="right">89.1%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">2,371,660</td>
<td align="right">4,474,860</td>
<td align="right">88.7%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">628,220</td>
<td align="right">1,177,800</td>
<td align="right">87.5%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">117,260</td>
<td align="right">219,240</td>
<td align="right">87.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">1,044,520</td>
<td align="right">1,948,240</td>
<td align="right">86.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">4,718,020</td>
<td align="right">8,692,960</td>
<td align="right">84.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right">809,420</td>
<td align="right">1,436,920</td>
<td align="right">77.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">887,340</td>
<td align="right">1,570,820</td>
<td align="right">77.0%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">16,209,060</td>
<td align="right">28,340,740</td>
<td align="right">74.8%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">381,760</td>
<td align="right">667,340</td>
<td align="right">74.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">4,751,660</td>
<td align="right">8,251,900</td>
<td align="right">73.7%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">285,460</td>
<td align="right">492,520</td>
<td align="right">72.5%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">838,500</td>
<td align="right">1,429,060</td>
<td align="right">70.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">1,851,000</td>
<td align="right">3,112,240</td>
<td align="right">68.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">1,485,940</td>
<td align="right">2,454,200</td>
<td align="right">65.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">1,447,420</td>
<td align="right">2,385,560</td>
<td align="right">64.8%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">406,420</td>
<td align="right">661,000</td>
<td align="right">62.6%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">4,412,700</td>
<td align="right">7,170,380</td>
<td align="right">62.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">4,412,700</td>
<td align="right">7,162,500</td>
<td align="right">62.3%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">4,769,360</td>
<td align="right">7,637,420</td>
<td align="right">60.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">2,960,000</td>
<td align="right">4,615,380</td>
<td align="right">55.9%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">287,100</td>
<td align="right">447,180</td>
<td align="right">55.8%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">2,062,160</td>
<td align="right">3,207,140</td>
<td align="right">55.5%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">12,365,900</td>
<td align="right">19,207,480</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">203,420</td>
<td align="right">91,060</td>
<td align="right">-55.2%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">3,998,840</td>
<td align="right">6,170,500</td>
<td align="right">54.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,133,080</td>
<td align="right">1,726,220</td>
<td align="right">52.3%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">661,740</td>
<td align="right">1,007,920</td>
<td align="right">52.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">2,960,880</td>
<td align="right">4,492,800</td>
<td align="right">51.7%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">2,960,880</td>
<td align="right">4,491,640</td>
<td align="right">51.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">2,565,040</td>
<td align="right">3,856,140</td>
<td align="right">50.3%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">596,560</td>
<td align="right">893,840</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">594,420</td>
<td align="right">301,760</td>
<td align="right">-49.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">1,122,780</td>
<td align="right">1,649,420</td>
<td align="right">46.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">5,258,140</td>
<td align="right">7,632,880</td>
<td align="right">45.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">1,092,380</td>
<td align="right">1,568,800</td>
<td align="right">43.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">1,619,580</td>
<td align="right">2,314,120</td>
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">536,520</td>
<td align="right">757,780</td>
<td align="right">41.2%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">2,177,580</td>
<td align="right">2,925,840</td>
<td align="right">34.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">2,756,400</td>
<td align="right">3,688,200</td>
<td align="right">33.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">1,715,600</td>
<td align="right">2,169,900</td>
<td align="right">26.5%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">2,466,980</td>
<td align="right">2,873,940</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">3,793,500</td>
<td align="right">4,323,740</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">473,200</td>
<td align="right">523,140</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">9,055,180</td>
<td align="right">9,722,940</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">3,038,160</td>
<td align="right">3,205,380</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">1,960</td>
<td align="right">1,940</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">14,860</td>
<td align="right">14,840</td>
<td align="right">-0.1%</td>
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
<td align="right">11,119,880</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">5,938,920</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">4,669,420</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right"></td>
<td align="right">1,900,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">1,449,440</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right"></td>
<td align="right">976,080</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right"></td>
<td align="right">673,220</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right"></td>
<td align="right">635,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right"></td>
<td align="right">611,300</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right"></td>
<td align="right">605,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right"></td>
<td align="right">428,340</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right"></td>
<td align="right">395,980</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LEN</td>
<td align="right"></td>
<td align="right">393,620</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right">380,840</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right"></td>
<td align="right">317,760</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right"></td>
<td align="right">288,620</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right"></td>
<td align="right">247,680</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right"></td>
<td align="right">246,140</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">234,580</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right"></td>
<td align="right">233,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION_AND_LOCK</td>
<td align="right"></td>
<td align="right">233,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">233,520</td>
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
<td align="left">_POP_ITER</td>
<td align="right"></td>
<td align="right">209,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right"></td>
<td align="right">190,640</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right"></td>
<td align="right">173,500</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right"></td>
<td align="right">147,180</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right"></td>
<td align="right">146,240</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_1</td>
<td align="right"></td>
<td align="right">139,300</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right"></td>
<td align="right">111,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_PROPERTY_FRAME</td>
<td align="right"></td>
<td align="right">110,060</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right"></td>
<td align="right">97,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_INIT_CHECK</td>
<td align="right"></td>
<td align="right">90,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_AND_ALLOCATE_OBJECT</td>
<td align="right"></td>
<td align="right">90,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CREATE_INIT_FRAME</td>
<td align="right"></td>
<td align="right">90,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SWAP_3</td>
<td align="right"></td>
<td align="right">87,220</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right"></td>
<td align="right">85,200</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PY_FRAME_GENERAL</td>
<td align="right"></td>
<td align="right">84,660</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">79,580</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right"></td>
<td align="right">79,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right"></td>
<td align="right">65,620</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right"></td>
<td align="right">65,620</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_0</td>
<td align="right"></td>
<td align="right">64,600</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SEND_GEN_FRAME</td>
<td align="right"></td>
<td align="right">62,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">54,040</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right"></td>
<td align="right">39,700</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right"></td>
<td align="right">39,160</td>
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
<td align="right">35,880</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_FOR</td>
<td align="right"></td>
<td align="right">32,680</td>
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
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right"></td>
<td align="right">26,760</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">26,100</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">19,420</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right"></td>
<td align="right">17,940</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">12,440</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right"></td>
<td align="right">11,980</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right"></td>
<td align="right">11,980</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right"></td>
<td align="right">10,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right"></td>
<td align="right">9,980</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right"></td>
<td align="right">9,980</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right"></td>
<td align="right">9,980</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right"></td>
<td align="right">9,500</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right"></td>
<td align="right">7,640</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right"></td>
<td align="right">7,200</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_KW_NON_PY</td>
<td align="right"></td>
<td align="right">6,840</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE_KW</td>
<td align="right"></td>
<td align="right">6,840</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE</td>
<td align="right"></td>
<td align="right">6,360</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">6,300</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right"></td>
<td align="right">6,120</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_KW</td>
<td align="right"></td>
<td align="right">4,700</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PY_FRAME_KW</td>
<td align="right"></td>
<td align="right">4,700</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right"></td>
<td align="right">3,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_COMMON_CONSTANT</td>
<td align="right"></td>
<td align="right">3,240</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right"></td>
<td align="right">2,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right"></td>
<td align="right">1,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right"></td>
<td align="right">780</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right"></td>
<td align="right">780</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right"></td>
<td align="right">580</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right"></td>
<td align="right">80</td>
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
Stats gathered on: 2025-10-23
