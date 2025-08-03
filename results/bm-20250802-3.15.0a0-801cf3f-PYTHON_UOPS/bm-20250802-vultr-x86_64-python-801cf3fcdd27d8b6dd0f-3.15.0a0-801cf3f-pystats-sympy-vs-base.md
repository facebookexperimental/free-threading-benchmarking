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
<td align="right">151,246,067</td>
<td align="right">2,418,307</td>
<td align="right">-98.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">16,585,949</td>
<td align="right">2,618,018</td>
<td align="right">-84.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">26,055,421</td>
<td align="right">5,489,307</td>
<td align="right">-78.9%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">4,261,669</td>
<td align="right">1,585,455</td>
<td align="right">-62.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">54,679,191</td>
<td align="right">22,362,925</td>
<td align="right">-59.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">3,641,811</td>
<td align="right">1,555,262</td>
<td align="right">-57.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">38,139,343</td>
<td align="right">17,486,739</td>
<td align="right">-54.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">22,926,251</td>
<td align="right">10,848,369</td>
<td align="right">-52.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">515</td>
<td align="right">255</td>
<td align="right">-50.5%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">28,929</td>
<td align="right">14,629</td>
<td align="right">-49.4%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">1,448,694</td>
<td align="right">746,319</td>
<td align="right">-48.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">29,045,263</td>
<td align="right">15,047,489</td>
<td align="right">-48.2%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">77,269</td>
<td align="right">41,119</td>
<td align="right">-46.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">84,682,501</td>
<td align="right">45,660,705</td>
<td align="right">-46.1%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">2,979</td>
<td align="right">1,679</td>
<td align="right">-43.6%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">1,291,782</td>
<td align="right">745,949</td>
<td align="right">-42.3%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">6,260,963</td>
<td align="right">3,725,200</td>
<td align="right">-40.5%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">638,727</td>
<td align="right">389,902</td>
<td align="right">-39.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">33,678</td>
<td align="right">20,680</td>
<td align="right">-38.6%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">605,310</td>
<td align="right">372,870</td>
<td align="right">-38.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">707</td>
<td align="right">447</td>
<td align="right">-36.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">22,003,735</td>
<td align="right">13,934,567</td>
<td align="right">-36.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">24,602,522</td>
<td align="right">15,915,616</td>
<td align="right">-35.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">84,749,269</td>
<td align="right">55,242,449</td>
<td align="right">-34.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">86,374,345</td>
<td align="right">56,752,923</td>
<td align="right">-34.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">13,564,390</td>
<td align="right">8,932,432</td>
<td align="right">-34.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">3,024,708</td>
<td align="right">2,007,738</td>
<td align="right">-33.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">86,125,220</td>
<td align="right">57,848,647</td>
<td align="right">-32.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">14,394,911</td>
<td align="right">9,917,798</td>
<td align="right">-31.1%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">851</td>
<td align="right">591</td>
<td align="right">-30.6%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">18,872,039</td>
<td align="right">13,252,477</td>
<td align="right">-29.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">32,460,243</td>
<td align="right">23,263,483</td>
<td align="right">-28.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">118,457,022</td>
<td align="right">86,032,328</td>
<td align="right">-27.4%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">53,236,580</td>
<td align="right">39,249,120</td>
<td align="right">-26.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">1,639,203</td>
<td align="right">1,221,422</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">229,507,798</td>
<td align="right">171,710,368</td>
<td align="right">-25.2%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">15,937</td>
<td align="right">12,037</td>
<td align="right">-24.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">27,768,657</td>
<td align="right">20,998,663</td>
<td align="right">-24.4%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">866,253</td>
<td align="right">655,181</td>
<td align="right">-24.4%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">866,253</td>
<td align="right">655,181</td>
<td align="right">-24.4%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">866,253</td>
<td align="right">655,181</td>
<td align="right">-24.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">44,493,883</td>
<td align="right">34,204,707</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">308,480,285</td>
<td align="right">239,351,567</td>
<td align="right">-22.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">47,517,845</td>
<td align="right">37,035,091</td>
<td align="right">-22.1%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">27,479,688</td>
<td align="right">21,663,167</td>
<td align="right">-21.2%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">40,526,155</td>
<td align="right">32,102,529</td>
<td align="right">-20.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">11,294</td>
<td align="right">8,950</td>
<td align="right">-20.8%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">23,511,603</td>
<td align="right">18,635,463</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">8,933</td>
<td align="right">7,111</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">12,148,531</td>
<td align="right">9,673,463</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">11,848,090</td>
<td align="right">9,584,406</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">73,184,901</td>
<td align="right">59,919,111</td>
<td align="right">-18.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">13,464,581</td>
<td align="right">11,032,516</td>
<td align="right">-18.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">75,775,233</td>
<td align="right">62,230,773</td>
<td align="right">-17.9%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">100,778</td>
<td align="right">83,096</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">7,283,470</td>
<td align="right">6,025,885</td>
<td align="right">-17.3%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">46,352,340</td>
<td align="right">38,721,162</td>
<td align="right">-16.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">3,165</td>
<td align="right">2,645</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">741,992,675</td>
<td align="right">624,176,348</td>
<td align="right">-15.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">8,076,080</td>
<td align="right">6,812,939</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">206,696</td>
<td align="right">175,279</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">3,038,973</td>
<td align="right">2,585,203</td>
<td align="right">-14.9%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">13,242,878</td>
<td align="right">11,270,829</td>
<td align="right">-14.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">3,040,457</td>
<td align="right">2,588,471</td>
<td align="right">-14.9%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">17,616,782</td>
<td align="right">15,116,390</td>
<td align="right">-14.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">164,279</td>
<td align="right">141,390</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">78,108,003</td>
<td align="right">67,333,898</td>
<td align="right">-13.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">254,610,844</td>
<td align="right">220,376,683</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">28,524,208</td>
<td align="right">24,805,526</td>
<td align="right">-13.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">486,947</td>
<td align="right">427,534</td>
<td align="right">-12.2%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">18,076,732</td>
<td align="right">15,884,930</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">47,299,256</td>
<td align="right">41,597,697</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">55,773,566</td>
<td align="right">49,127,410</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">54,125,734</td>
<td align="right">48,111,306</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">19,636,956</td>
<td align="right">17,535,735</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">10,530,043</td>
<td align="right">9,409,288</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">508,647</td>
<td align="right">456,464</td>
<td align="right">-10.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">191,536</td>
<td align="right">172,003</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">66,015,891</td>
<td align="right">59,364,339</td>
<td align="right">-10.1%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">49,809,049</td>
<td align="right">44,884,738</td>
<td align="right">-9.9%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">47,777,811</td>
<td align="right">43,237,445</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">56,775,797</td>
<td align="right">51,396,040</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">87,849</td>
<td align="right">79,529</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">23,817,634</td>
<td align="right">21,702,685</td>
<td align="right">-8.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">7,395,065</td>
<td align="right">6,744,256</td>
<td align="right">-8.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">156,618,389</td>
<td align="right">144,132,599</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">2,180,790</td>
<td align="right">2,008,508</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">4,878,632</td>
<td align="right">4,497,247</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">26,833,233</td>
<td align="right">24,754,268</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">48,330,345</td>
<td align="right">44,609,459</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">215,559,865</td>
<td align="right">199,018,263</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">19,262,977</td>
<td align="right">17,804,458</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">707,770</td>
<td align="right">654,465</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">707,752</td>
<td align="right">654,449</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">3,238,793</td>
<td align="right">2,995,200</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">160,024,621</td>
<td align="right">147,995,142</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">20,465,476</td>
<td align="right">18,937,335</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">186,919,691</td>
<td align="right">173,111,490</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">196,230,100</td>
<td align="right">181,818,051</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">19,443,659</td>
<td align="right">18,020,402</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">7,109,079</td>
<td align="right">6,589,591</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">12,398,730</td>
<td align="right">11,495,424</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">8,557,269</td>
<td align="right">7,935,346</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">57,170,011</td>
<td align="right">53,070,831</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">2,456,748</td>
<td align="right">2,281,462</td>
<td align="right">-7.1%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">8,711,110</td>
<td align="right">8,099,080</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">6,181,186</td>
<td align="right">5,753,055</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">4,298,686</td>
<td align="right">4,001,680</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">48,053,153</td>
<td align="right">44,992,583</td>
<td align="right">-6.4%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">286,304</td>
<td align="right">270,096</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">7,982,757</td>
<td align="right">7,541,347</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">13,150,825</td>
<td align="right">12,439,594</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">6,998,558</td>
<td align="right">6,622,699</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">19,171,415</td>
<td align="right">18,146,346</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">1,466,790</td>
<td align="right">1,389,722</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">34,957,745</td>
<td align="right">33,137,792</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">83,039,498</td>
<td align="right">78,735,167</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,854,410</td>
<td align="right">1,758,985</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">630,515</td>
<td align="right">598,528</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">79,310,761</td>
<td align="right">75,301,040</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">1,391,177</td>
<td align="right">1,323,308</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">173,809</td>
<td align="right">165,659</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">407,807</td>
<td align="right">388,827</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,078,257</td>
<td align="right">1,029,875</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">1,076,326</td>
<td align="right">1,028,984</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">777,250</td>
<td align="right">744,767</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,337,317</td>
<td align="right">1,288,068</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">7,041,177</td>
<td align="right">6,785,838</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">31,537,090</td>
<td align="right">30,402,876</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">10,139,090</td>
<td align="right">9,777,834</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">513,084</td>
<td align="right">495,186</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">22,737,892</td>
<td align="right">21,976,987</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">974,612</td>
<td align="right">942,610</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">22,680,330</td>
<td align="right">21,991,491</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">1,068,283</td>
<td align="right">1,036,043</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">4,720,473</td>
<td align="right">4,583,030</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">11,184,334</td>
<td align="right">10,870,983</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">6,141,785</td>
<td align="right">5,972,226</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">1,801,849</td>
<td align="right">1,754,523</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">11,194,664</td>
<td align="right">10,927,245</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">2,252,586</td>
<td align="right">2,200,023</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">15,928,238</td>
<td align="right">15,580,031</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">4,268,298</td>
<td align="right">4,179,003</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">136,324</td>
<td align="right">133,724</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">347,960</td>
<td align="right">341,720</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">1,265,585</td>
<td align="right">1,244,523</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">90,309</td>
<td align="right">89,009</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">181,132</td>
<td align="right">178,532</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">181,134</td>
<td align="right">178,534</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">4,530,256</td>
<td align="right">4,466,524</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">2,971</td>
<td align="right">2,960</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">996</td>
<td align="right">998</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">18,093</td>
<td align="right">18,062</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">1,444</td>
<td align="right">1,445</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">23,811</td>
<td align="right">23,796</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">9,212</td>
<td align="right">9,212</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">8,941</td>
<td align="right">8,941</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">5,550</td>
<td align="right">5,550</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">4,150</td>
<td align="right">4,150</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">1,055</td>
<td align="right">1,055</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">394</td>
<td align="right">394</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">200</td>
<td align="right">200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">133</td>
<td align="right">133</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">127</td>
<td align="right">127</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">102</td>
<td align="right">102</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">92</td>
<td align="right">92</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">6</td>
<td align="right">6</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">3</td>
<td align="right">3</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">1</td>
<td align="right">1</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">1</td>
<td align="right">1</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right"></td>
<td align="right">57,352,317</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right"></td>
<td align="right">28,421,694</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right"></td>
<td align="right">223,546</td>
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
<td align="right">94,681,331</td>
<td align="right">66.0%</td>
<td align="right">70,502,493</td>
<td align="right">61.0%</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">48,298,401</td>
<td align="right">33.7%</td>
<td align="right">44,578,493</td>
<td align="right">38.6%</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">444,083</td>
<td align="right">0.3%</td>
<td align="right">437,077</td>
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
<td align="right">29,819</td>
<td align="right">74.0%</td>
<td align="right">28,840</td>
<td align="right">73.6%</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">10,481</td>
<td align="right">26.0%</td>
<td align="right">10,346</td>
<td align="right">26.4%</td>
<td align="right">-1.3%</td>
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
<td align="left">multiply different types</td>
<td align="right">2,376</td>
<td align="right">8.0%</td>
<td align="right">2,142</td>
<td align="right">7.4%</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">466</td>
<td align="right">1.6%</td>
<td align="right">422</td>
<td align="right">1.5%</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">4,979</td>
<td align="right">16.7%</td>
<td align="right">4,545</td>
<td align="right">15.8%</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">1,891</td>
<td align="right">6.3%</td>
<td align="right">1,765</td>
<td align="right">6.1%</td>
<td align="right">-6.7%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">741</td>
<td align="right">2.5%</td>
<td align="right">716</td>
<td align="right">2.5%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">1,012</td>
<td align="right">3.4%</td>
<td align="right">982</td>
<td align="right">3.4%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">93</td>
<td align="right">0.3%</td>
<td align="right">91</td>
<td align="right">0.3%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">986</td>
<td align="right">3.3%</td>
<td align="right">1,003</td>
<td align="right">3.5%</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">212</td>
<td align="right">0.7%</td>
<td align="right">209</td>
<td align="right">0.7%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">1,230</td>
<td align="right">4.1%</td>
<td align="right">1,214</td>
<td align="right">4.2%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">2,934</td>
<td align="right">9.8%</td>
<td align="right">2,901</td>
<td align="right">10.1%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">715</td>
<td align="right">2.4%</td>
<td align="right">708</td>
<td align="right">2.5%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">571</td>
<td align="right">1.9%</td>
<td align="right">566</td>
<td align="right">2.0%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">1,094</td>
<td align="right">3.7%</td>
<td align="right">1,086</td>
<td align="right">3.8%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">156</td>
<td align="right">0.5%</td>
<td align="right">155</td>
<td align="right">0.5%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">365</td>
<td align="right">1.2%</td>
<td align="right">363</td>
<td align="right">1.3%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">3,914</td>
<td align="right">13.1%</td>
<td align="right">3,901</td>
<td align="right">13.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">3,231</td>
<td align="right">10.8%</td>
<td align="right">3,221</td>
<td align="right">11.2%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">2,228</td>
<td align="right">7.5%</td>
<td align="right">2,225</td>
<td align="right">7.7%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">624</td>
<td align="right">2.1%</td>
<td align="right">624</td>
<td align="right">2.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr array</td>
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
<td align="right">15,937</td>
<td align="right">100.0%</td>
<td align="right">12,037</td>
<td align="right">100.0%</td>
<td align="right">-24.5%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">44,841,081</td>
<td align="right">12.9%</td>
<td align="right">36,359,159</td>
<td align="right">12.1%</td>
<td align="right">-18.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">44,003,600</td>
<td align="right">12.7%</td>
<td align="right">35,681,652</td>
<td align="right">11.8%</td>
<td align="right">-18.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">301,903,261</td>
<td align="right">87.1%</td>
<td align="right">265,180,550</td>
<td align="right">87.9%</td>
<td align="right">-12.2%</td>
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
<td align="right">861,292</td>
<td align="right">100.0%</td>
<td align="right">701,303</td>
<td align="right">100.0%</td>
<td align="right">-18.6%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">3,022</td>
<td align="right">67.7%</td>
<td align="right">2,805</td>
<td align="right">66.0%</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">3,399</td>
<td align="right">76.1%</td>
<td align="right">3,183</td>
<td align="right">74.9%</td>
<td align="right">-6.4%</td>
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
<td align="right">1,067</td>
<td align="right">100.0%</td>
<td align="right">1,067</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">58,794,408</td>
<td align="right">64.8%</td>
<td align="right">47,986,364</td>
<td align="right">60.9%</td>
<td align="right">-18.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">31,498,572</td>
<td align="right">34.7%</td>
<td align="right">30,364,764</td>
<td align="right">38.5%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">405,048</td>
<td align="right">0.4%</td>
<td align="right">403,506</td>
<td align="right">0.5%</td>
<td align="right">-0.4%</td>
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
<td align="right">37,353</td>
<td align="right">81.0%</td>
<td align="right">36,950</td>
<td align="right">80.9%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">8,786</td>
<td align="right">19.0%</td>
<td align="right">8,719</td>
<td align="right">19.1%</td>
<td align="right">-0.8%</td>
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
<td align="right">112</td>
<td align="right">0.3%</td>
<td align="right">91</td>
<td align="right">0.2%</td>
<td align="right">-18.8%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">1,551</td>
<td align="right">4.2%</td>
<td align="right">1,440</td>
<td align="right">3.9%</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">4,375</td>
<td align="right">11.7%</td>
<td align="right">4,256</td>
<td align="right">11.5%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">7,278</td>
<td align="right">19.5%</td>
<td align="right">7,108</td>
<td align="right">19.2%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">115</td>
<td align="right">0.3%</td>
<td align="right">116</td>
<td align="right">0.3%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">139</td>
<td align="right">0.4%</td>
<td align="right">138</td>
<td align="right">0.4%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">6,477</td>
<td align="right">17.3%</td>
<td align="right">6,460</td>
<td align="right">17.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">13,975</td>
<td align="right">37.4%</td>
<td align="right">14,008</td>
<td align="right">37.9%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">3,151</td>
<td align="right">8.4%</td>
<td align="right">3,153</td>
<td align="right">8.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">136</td>
<td align="right">0.4%</td>
<td align="right">136</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">44</td>
<td align="right">0.1%</td>
<td align="right">44</td>
<td align="right">0.1%</td>
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
<td align="right">26,142,250</td>
<td align="right">53.3%</td>
<td align="right">5,567,816</td>
<td align="right">33.9%</td>
<td align="right">-78.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">22,917,750</td>
<td align="right">46.7%</td>
<td align="right">10,842,854</td>
<td align="right">66.0%</td>
<td align="right">-52.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,020</td>
<td align="right">0.0%</td>
<td align="right">1,020</td>
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
<td align="right">8,376</td>
<td align="right">98.5%</td>
<td align="right">5,390</td>
<td align="right">97.7%</td>
<td align="right">-35.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">125</td>
<td align="right">1.5%</td>
<td align="right">125</td>
<td align="right">2.3%</td>
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
<td align="right">6,373</td>
<td align="right">76.1%</td>
<td align="right">3,435</td>
<td align="right">63.7%</td>
<td align="right">-46.1%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">222</td>
<td align="right">2.7%</td>
<td align="right">182</td>
<td align="right">3.4%</td>
<td align="right">-18.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">301</td>
<td align="right">3.6%</td>
<td align="right">299</td>
<td align="right">5.5%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">1,480</td>
<td align="right">17.7%</td>
<td align="right">1,474</td>
<td align="right">27.3%</td>
<td align="right">-0.4%</td>
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
<td align="right">84,615,755</td>
<td align="right">41.8%</td>
<td align="right">45,607,906</td>
<td align="right">41.1%</td>
<td align="right">-46.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">116,381,247</td>
<td align="right">57.5%</td>
<td align="right">64,031,140</td>
<td align="right">57.7%</td>
<td align="right">-45.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,373,073</td>
<td align="right">0.7%</td>
<td align="right">1,249,041</td>
<td align="right">1.1%</td>
<td align="right">-9.0%</td>
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
<td align="right">65,955</td>
<td align="right">71.2%</td>
<td align="right">52,010</td>
<td align="right">68.2%</td>
<td align="right">-21.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">26,638</td>
<td align="right">28.8%</td>
<td align="right">24,270</td>
<td align="right">31.8%</td>
<td align="right">-8.9%</td>
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
<td align="left">ascii string</td>
<td align="right">45</td>
<td align="right">0.1%</td>
<td align="right">24</td>
<td align="right">0.0%</td>
<td align="right">-46.7%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">4,225</td>
<td align="right">6.4%</td>
<td align="right">2,697</td>
<td align="right">5.2%</td>
<td align="right">-36.2%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">50,955</td>
<td align="right">77.3%</td>
<td align="right">39,402</td>
<td align="right">75.8%</td>
<td align="right">-22.7%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">286</td>
<td align="right">0.4%</td>
<td align="right">243</td>
<td align="right">0.5%</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">7,044</td>
<td align="right">10.7%</td>
<td align="right">6,301</td>
<td align="right">12.1%</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">607</td>
<td align="right">0.9%</td>
<td align="right">557</td>
<td align="right">1.1%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">195</td>
<td align="right">0.3%</td>
<td align="right">194</td>
<td align="right">0.4%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">760</td>
<td align="right">1.2%</td>
<td align="right">758</td>
<td align="right">1.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">383</td>
<td align="right">0.6%</td>
<td align="right">382</td>
<td align="right">0.7%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">1,362</td>
<td align="right">2.1%</td>
<td align="right">1,359</td>
<td align="right">2.6%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">64</td>
<td align="right">0.1%</td>
<td align="right">64</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">29</td>
<td align="right">0.0%</td>
<td align="right">29</td>
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
<td align="left">generator</td>
<td align="right">112,867</td>
<td align="right">112,867 / 0 !!</td>
<td align="right">70,479</td>
<td align="right">70,479 / 0 !!</td>
<td align="right">-37.6%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">703</td>
<td align="right">703 / 0 !!</td>
<td align="right">443</td>
<td align="right">443 / 0 !!</td>
<td align="right">-37.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">9,603,642</td>
<td align="right">9,603,642 / 0 !!</td>
<td align="right">8,715,581</td>
<td align="right">8,715,581 / 0 !!</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">170,135</td>
<td align="right">170,135 / 0 !!</td>
<td align="right">157,913</td>
<td align="right">157,913 / 0 !!</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">7,721,127</td>
<td align="right">7,721,127 / 0 !!</td>
<td align="right">7,192,141</td>
<td align="right">7,192,141 / 0 !!</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">10,065,523</td>
<td align="right">10,065,523 / 0 !!</td>
<td align="right">9,440,391</td>
<td align="right">9,440,391 / 0 !!</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">9,612,265</td>
<td align="right">9,612,265 / 0 !!</td>
<td align="right">9,237,119</td>
<td align="right">9,237,119 / 0 !!</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">12,516,759</td>
<td align="right">12,516,759 / 0 !!</td>
<td align="right">12,233,587</td>
<td align="right">12,233,587 / 0 !!</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">6,028</td>
<td align="right">6,028 / 0 !!</td>
<td align="right">6,028</td>
<td align="right">6,028 / 0 !!</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">73,120,639</td>
<td align="right">19.5%</td>
<td align="right">59,858,875</td>
<td align="right">19.0%</td>
<td align="right">-18.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">243,355,606</td>
<td align="right">65.0%</td>
<td align="right">202,563,824</td>
<td align="right">64.3%</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">57,916,416</td>
<td align="right">15.5%</td>
<td align="right">52,721,414</td>
<td align="right">16.7%</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">1</td>
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
<td align="right">1,103,830</td>
<td align="right">95.8%</td>
<td align="right">1,005,549</td>
<td align="right">95.7%</td>
<td align="right">-8.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">48,563</td>
<td align="right">4.2%</td>
<td align="right">45,055</td>
<td align="right">4.3%</td>
<td align="right">-7.2%</td>
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
<td align="left">builtin class method</td>
<td align="right">567</td>
<td align="right">1.2%</td>
<td align="right">206</td>
<td align="right">0.5%</td>
<td align="right">-63.7%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">4,397</td>
<td align="right">9.1%</td>
<td align="right">3,115</td>
<td align="right">6.9%</td>
<td align="right">-29.2%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">2,687</td>
<td align="right">5.5%</td>
<td align="right">2,324</td>
<td align="right">5.2%</td>
<td align="right">-13.5%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">22,432</td>
<td align="right">46.2%</td>
<td align="right">21,418</td>
<td align="right">47.5%</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">7,115</td>
<td align="right">14.7%</td>
<td align="right">6,815</td>
<td align="right">15.1%</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">2,817</td>
<td align="right">5.8%</td>
<td align="right">2,743</td>
<td align="right">6.1%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">47</td>
<td align="right">0.1%</td>
<td align="right">46</td>
<td align="right">0.1%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">4,137</td>
<td align="right">8.5%</td>
<td align="right">4,058</td>
<td align="right">9.0%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">3,124</td>
<td align="right">6.4%</td>
<td align="right">3,099</td>
<td align="right">6.9%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">148</td>
<td align="right">0.3%</td>
<td align="right">148</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">7</td>
<td align="right">0.0%</td>
<td align="right">7</td>
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
<td align="right">305,375,411</td>
<td align="right">100.0%</td>
<td align="right">259,142,516</td>
<td align="right">100.0%</td>
<td align="right">-15.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">4,554</td>
<td align="right">0.0%</td>
<td align="right">4,529</td>
<td align="right">0.0%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,302</td>
<td align="right">0.0%</td>
<td align="right">1,302</td>
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
<td align="right">13,587</td>
<td align="right">100.0%</td>
<td align="right">13,581</td>
<td align="right">100.0%</td>
<td align="right">-0.0%</td>
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
<td align="right">2,365,789</td>
<td align="right">100.0%</td>
<td align="right">2,265,918</td>
<td align="right">100.0%</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">30</td>
<td align="right">0.0%</td>
<td align="right">30</td>
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
<td align="right">30</td>
<td align="right">100.0%</td>
<td align="right">30</td>
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
<td align="right">1,421,094</td>
<td align="right">81.9%</td>
<td align="right">731,608</td>
<td align="right">72.0%</td>
<td align="right">-48.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">27,600</td>
<td align="right">1.6%</td>
<td align="right">14,711</td>
<td align="right">1.4%</td>
<td align="right">-46.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">283,952</td>
<td align="right">16.4%</td>
<td align="right">268,986</td>
<td align="right">26.5%</td>
<td align="right">-5.3%</td>
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
<td align="right">2,370</td>
<td align="right">82.3%</td>
<td align="right">1,108</td>
<td align="right">80.2%</td>
<td align="right">-53.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">510</td>
<td align="right">17.7%</td>
<td align="right">274</td>
<td align="right">19.8%</td>
<td align="right">-46.3%</td>
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
<td align="right">2,370</td>
<td align="right">100.0%</td>
<td align="right">1,108</td>
<td align="right">100.0%</td>
<td align="right">-53.2%</td>
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
<td align="right">205,428</td>
<td align="right">2.1%</td>
<td align="right">173,967</td>
<td align="right">1.9%</td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,803,936</td>
<td align="right">18.7%</td>
<td align="right">1,574,794</td>
<td align="right">17.3%</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">7,651,370</td>
<td align="right">79.2%</td>
<td align="right">7,329,367</td>
<td align="right">80.7%</td>
<td align="right">-4.2%</td>
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
<td align="right">34,282</td>
<td align="right">97.4%</td>
<td align="right">29,953</td>
<td align="right">96.8%</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">932</td>
<td align="right">2.6%</td>
<td align="right">976</td>
<td align="right">3.2%</td>
<td align="right">4.7%</td>
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
<td align="right">254</td>
<td align="right">27.3%</td>
<td align="right">298</td>
<td align="right">30.5%</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">103</td>
<td align="right">11.1%</td>
<td align="right">102</td>
<td align="right">10.5%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">518</td>
<td align="right">55.6%</td>
<td align="right">518</td>
<td align="right">53.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">3</td>
<td align="right">0.3%</td>
<td align="right">3</td>
<td align="right">0.3%</td>
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
<td align="right">851</td>
<td align="right">100.0%</td>
<td align="right">591</td>
<td align="right">100.0%</td>
<td align="right">-30.6%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">26,404,371</td>
<td align="right">89.7%</td>
<td align="right">17,670,139</td>
<td align="right">87.2%</td>
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
<td align="right">3,036,699</td>
<td align="right">10.3%</td>
<td align="right">2,583,084</td>
<td align="right">12.8%</td>
<td align="right">-14.9%</td>
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
<td align="right">1,698</td>
<td align="right">74.7%</td>
<td align="right">1,543</td>
<td align="right">72.8%</td>
<td align="right">-9.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">576</td>
<td align="right">25.3%</td>
<td align="right">576</td>
<td align="right">27.2%</td>
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
<td align="right">1,698</td>
<td align="right">100.0%</td>
<td align="right">1,543</td>
<td align="right">100.0%</td>
<td align="right">-9.1%</td>
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
<td align="right">784,654</td>
<td align="right">0.4%</td>
<td align="right">623,259</td>
<td align="right">0.4%</td>
<td align="right">-20.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">177,388,021</td>
<td align="right">94.2%</td>
<td align="right">163,508,460</td>
<td align="right">94.0%</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">10,116,283</td>
<td align="right">5.4%</td>
<td align="right">9,755,796</td>
<td align="right">5.6%</td>
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
<td align="left">Success</td>
<td align="right">21,954</td>
<td align="right">59.3%</td>
<td align="right">18,965</td>
<td align="right">57.1%</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">15,054</td>
<td align="right">40.7%</td>
<td align="right">14,271</td>
<td align="right">42.9%</td>
<td align="right">-5.2%</td>
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
<td align="right">2,843</td>
<td align="right">18.9%</td>
<td align="right">2,596</td>
<td align="right">18.2%</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">8,538</td>
<td align="right">56.7%</td>
<td align="right">8,007</td>
<td align="right">56.1%</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">845</td>
<td align="right">5.6%</td>
<td align="right">883</td>
<td align="right">6.2%</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">1,287</td>
<td align="right">8.5%</td>
<td align="right">1,258</td>
<td align="right">8.8%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">725</td>
<td align="right">4.8%</td>
<td align="right">716</td>
<td align="right">5.0%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">730</td>
<td align="right">4.8%</td>
<td align="right">725</td>
<td align="right">5.1%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">84</td>
<td align="right">0.6%</td>
<td align="right">84</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">2</td>
<td align="right">0.0%</td>
<td align="right">2</td>
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
<td align="right">86,250,865</td>
<td align="right">100.0%</td>
<td align="right">56,671,907</td>
<td align="right">100.0%</td>
<td align="right">-34.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">8,605</td>
<td align="right">0.0%</td>
<td align="right">6,264</td>
<td align="right">0.0%</td>
<td align="right">-27.2%</td>
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
<td align="right">298</td>
<td align="right">11.1%</td>
<td align="right">295</td>
<td align="right">11.0%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,391</td>
<td align="right">88.9%</td>
<td align="right">2,391</td>
<td align="right">89.0%</td>
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
<td align="right">255</td>
<td align="right">85.6%</td>
<td align="right">252</td>
<td align="right">85.4%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">43</td>
<td align="right">14.4%</td>
<td align="right">43</td>
<td align="right">14.6%</td>
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
<td align="right">324,212,690</td>
<td align="right">6.2%</td>
<td align="right">249,198,611</td>
<td align="right">5.8%</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">1,790,093,751</td>
<td align="right">34.2%</td>
<td align="right">1,408,228,400</td>
<td align="right">32.9%</td>
<td align="right">-21.3%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">3,010,686,108</td>
<td align="right">57.5%</td>
<td align="right">2,533,695,255</td>
<td align="right">59.1%</td>
<td align="right">-15.8%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">107,601,235</td>
<td align="right">2.1%</td>
<td align="right">93,388,090</td>
<td align="right">2.2%</td>
<td align="right">-13.2%</td>
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
<td align="left">CONTAINS_OP</td>
<td align="right">22,917,750</td>
<td align="right">7.2%</td>
<td align="right">10,842,854</td>
<td align="right">4.5%</td>
<td align="right">-52.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">84,615,755</td>
<td align="right">26.6%</td>
<td align="right">45,607,906</td>
<td align="right">19.0%</td>
<td align="right">-46.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">44,003,600</td>
<td align="right">13.8%</td>
<td align="right">35,681,652</td>
<td align="right">14.9%</td>
<td align="right">-18.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">73,120,639</td>
<td align="right">23.0%</td>
<td align="right">59,858,875</td>
<td align="right">25.0%</td>
<td align="right">-18.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">205,428</td>
<td align="right">0.1%</td>
<td align="right">173,967</td>
<td align="right">0.1%</td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">3,036,699</td>
<td align="right">1.0%</td>
<td align="right">2,583,084</td>
<td align="right">1.1%</td>
<td align="right">-14.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">48,298,401</td>
<td align="right">15.2%</td>
<td align="right">44,578,493</td>
<td align="right">18.6%</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">283,952</td>
<td align="right">0.1%</td>
<td align="right">268,986</td>
<td align="right">0.1%</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">31,498,572</td>
<td align="right">9.9%</td>
<td align="right">30,364,764</td>
<td align="right">12.7%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">10,116,283</td>
<td align="right">3.2%</td>
<td align="right">9,755,796</td>
<td align="right">4.1%</td>
<td align="right">-3.6%</td>
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
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">18,527,360</td>
<td align="right">17.2%</td>
<td align="right">11,699,535</td>
<td align="right">12.5%</td>
<td align="right">-36.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">4,113,613</td>
<td align="right">3.8%</td>
<td align="right">3,208,209</td>
<td align="right">3.4%</td>
<td align="right">-22.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,802,357</td>
<td align="right">1.7%</td>
<td align="right">1,574,015</td>
<td align="right">1.7%</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">14,235,821</td>
<td align="right">13.2%</td>
<td align="right">12,839,111</td>
<td align="right">13.7%</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">12,242,343</td>
<td align="right">11.4%</td>
<td align="right">11,182,536</td>
<td align="right">12.0%</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">31,277,057</td>
<td align="right">29.1%</td>
<td align="right">28,926,623</td>
<td align="right">31.0%</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">6,579,059</td>
<td align="right">6.1%</td>
<td align="right">6,164,396</td>
<td align="right">6.6%</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">7,560,395</td>
<td align="right">7.0%</td>
<td align="right">7,331,090</td>
<td align="right">7.9%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">2,161,618</td>
<td align="right">2.0%</td>
<td align="right">2,103,568</td>
<td align="right">2.3%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">5,178,009</td>
<td align="right">4.8%</td>
<td align="right">5,099,555</td>
<td align="right">5.5%</td>
<td align="right">-1.5%</td>
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
<td align="left">Frame objects created</td>
<td align="right">1,236,196</td>
<td align="right">0.5%</td>
<td align="right">950,246</td>
<td align="right">0.5%</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">3,938,031</td>
<td align="right">1.7%</td>
<td align="right">3,468,700</td>
<td align="right">1.7%</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">144,472,473</td>
<td align="right">63.4%</td>
<td align="right">131,242,992</td>
<td align="right">62.5%</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">202,581,446</td>
<td align="right">89.0%</td>
<td align="right">187,641,025</td>
<td align="right">89.3%</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">43,616,340</td>
<td align="right">19.2%</td>
<td align="right">41,131,227</td>
<td align="right">19.6%</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">83,238,894</td>
<td align="right">36.6%</td>
<td align="right">78,889,580</td>
<td align="right">37.5%</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">83,238,894</td>
<td align="right">36.6%</td>
<td align="right">78,889,580</td>
<td align="right">37.5%</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">79,300,078</td>
<td align="right">34.8%</td>
<td align="right">75,420,095</td>
<td align="right">35.9%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">79,300,863</td>
<td align="right">34.8%</td>
<td align="right">75,420,880</td>
<td align="right">35.9%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">19,324,214</td>
<td align="right">8.5%</td>
<td align="right">18,496,772</td>
<td align="right">8.8%</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">9,507,221</td>
<td align="right">4.2%</td>
<td align="right">9,331,964</td>
<td align="right">4.4%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">652</td>
<td align="right">0.0%</td>
<td align="right">652</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">133</td>
<td align="right">0.0%</td>
<td align="right">133</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">416</td>
<td align="right">0.0%</td>
<td align="right">416</td>
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
<td align="right">975,986</td>
<td align="right"></td>
<td align="right">1,100,482</td>
<td align="right"></td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">3,502,696</td>
<td align="right"></td>
<td align="right">3,873,232</td>
<td align="right"></td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">960,383</td>
<td align="right"></td>
<td align="right">866,250</td>
<td align="right"></td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">2,529,341</td>
<td align="right"></td>
<td align="right">2,774,242</td>
<td align="right"></td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">1,382,212,331</td>
<td align="right">38.0%</td>
<td align="right">1,270,809,827</td>
<td align="right">37.2%</td>
<td align="right">-8.1%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">1,715,289,216</td>
<td align="right">43.8%</td>
<td align="right">1,588,272,986</td>
<td align="right">43.1%</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">54,955,899</td>
<td align="right">1.4%</td>
<td align="right">51,393,621</td>
<td align="right">1.4%</td>
<td align="right">-6.5%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">159,727,453</td>
<td align="right"></td>
<td align="right">149,507,641</td>
<td align="right"></td>
<td align="right">-6.4%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">813,671</td>
<td align="right">0.2%</td>
<td align="right">764,700</td>
<td align="right">0.2%</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">263,912,345</td>
<td align="right"></td>
<td align="right">249,118,485</td>
<td align="right"></td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">9,451</td>
<td align="right">0.0%</td>
<td align="right">8,976</td>
<td align="right">0.0%</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">1,158,086,196</td>
<td align="right">31.9%</td>
<td align="right">1,100,169,478</td>
<td align="right">32.2%</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">83,226,281</td>
<td align="right">2.3%</td>
<td align="right">79,112,783</td>
<td align="right">2.3%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">135,718,892</td>
<td align="right">27.1%</td>
<td align="right">129,110,033</td>
<td align="right">26.8%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">134,895,770</td>
<td align="right">27.0%</td>
<td align="right">128,336,357</td>
<td align="right">26.6%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">148,922,277</td>
<td align="right"></td>
<td align="right">141,762,606</td>
<td align="right"></td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">1,263,373,186</td>
<td align="right">32.3%</td>
<td align="right">1,204,207,573</td>
<td align="right">32.7%</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">880,749,799</td>
<td align="right">22.5%</td>
<td align="right">842,859,426</td>
<td align="right">22.9%</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">1,009,522,395</td>
<td align="right">27.8%</td>
<td align="right">969,489,941</td>
<td align="right">28.4%</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">364,393,470</td>
<td align="right">72.9%</td>
<td align="right">352,517,857</td>
<td align="right">73.2%</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">364,428,682</td>
<td align="right"></td>
<td align="right">352,553,064</td>
<td align="right"></td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
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
<td align="right">84</td>
<td align="right">84</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-08-03
