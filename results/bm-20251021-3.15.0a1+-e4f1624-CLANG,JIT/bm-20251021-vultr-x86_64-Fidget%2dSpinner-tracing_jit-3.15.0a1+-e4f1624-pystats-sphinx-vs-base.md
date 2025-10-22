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
<td align="right">9,120,527</td>
<td align="right">50,913,552</td>
<td align="right">458.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">2,653,741</td>
<td align="right">10,229,930</td>
<td align="right">285.5%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">155,774</td>
<td align="right">554,235</td>
<td align="right">255.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">551,220</td>
<td align="right">1,878,534</td>
<td align="right">240.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">239,955</td>
<td align="right">655,299</td>
<td align="right">173.1%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">1,606,786</td>
<td align="right">3,563,455</td>
<td align="right">121.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">1,044,938</td>
<td align="right">2,148,629</td>
<td align="right">105.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">759,900</td>
<td align="right">1,452,802</td>
<td align="right">91.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">61,068,659</td>
<td align="right">7,884,564</td>
<td align="right">-87.1%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">39,529,039</td>
<td align="right">6,174,049</td>
<td align="right">-84.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">1,316,514</td>
<td align="right">2,348,052</td>
<td align="right">78.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">64,012,586</td>
<td align="right">14,736,683</td>
<td align="right">-77.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,696,353</td>
<td align="right">2,938,551</td>
<td align="right">73.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">2,987,262</td>
<td align="right">5,026,677</td>
<td align="right">68.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">75,094,954</td>
<td align="right">24,141,702</td>
<td align="right">-67.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">88,145,834</td>
<td align="right">37,352,191</td>
<td align="right">-57.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,902,808</td>
<td align="right">2,966,291</td>
<td align="right">55.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">7,025,649</td>
<td align="right">10,918,469</td>
<td align="right">55.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">38,050,643</td>
<td align="right">18,879,670</td>
<td align="right">-50.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">5,603,933</td>
<td align="right">8,407,499</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">5,328,538</td>
<td align="right">7,914,752</td>
<td align="right">48.5%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">3,478,869</td>
<td align="right">1,891,557</td>
<td align="right">-45.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">78,137,477</td>
<td align="right">42,753,141</td>
<td align="right">-45.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">101,515,058</td>
<td align="right">55,742,697</td>
<td align="right">-45.1%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">38,888,516</td>
<td align="right">21,597,078</td>
<td align="right">-44.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">84,082,542</td>
<td align="right">49,033,262</td>
<td align="right">-41.7%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">83,884,215</td>
<td align="right">49,200,066</td>
<td align="right">-41.3%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">86,457,020</td>
<td align="right">52,299,724</td>
<td align="right">-39.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">2,672,818</td>
<td align="right">1,699,880</td>
<td align="right">-36.4%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">22,681,604</td>
<td align="right">15,133,392</td>
<td align="right">-33.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">137,432,698</td>
<td align="right">98,790,277</td>
<td align="right">-28.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">133,263,531</td>
<td align="right">97,432,506</td>
<td align="right">-26.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">179,625,572</td>
<td align="right">131,330,563</td>
<td align="right">-26.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">1,721,569</td>
<td align="right">2,167,006</td>
<td align="right">25.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">107,801,599</td>
<td align="right">81,253,955</td>
<td align="right">-24.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">145,931,709</td>
<td align="right">112,278,953</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">157,501,828</td>
<td align="right">122,714,132</td>
<td align="right">-22.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">620,255,985</td>
<td align="right">504,778,526</td>
<td align="right">-18.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,288,460</td>
<td align="right">1,516,729</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">11,414,232</td>
<td align="right">9,429,582</td>
<td align="right">-17.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">2,223,876</td>
<td align="right">2,602,175</td>
<td align="right">17.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">29,692,174</td>
<td align="right">34,734,350</td>
<td align="right">17.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">3,798,333</td>
<td align="right">4,435,028</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">680,996</td>
<td align="right">773,029</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">155,130,823</td>
<td align="right">134,996,556</td>
<td align="right">-13.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">172,140,230</td>
<td align="right">150,966,363</td>
<td align="right">-12.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">4,448,215</td>
<td align="right">4,950,812</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">4,644,831</td>
<td align="right">4,137,364</td>
<td align="right">-10.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">46,226,263</td>
<td align="right">51,271,051</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">15,146,327</td>
<td align="right">16,729,037</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">8,712,632</td>
<td align="right">9,597,704</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">11,035,480</td>
<td align="right">12,106,217</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">24,859,209</td>
<td align="right">27,259,306</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">4,977,858</td>
<td align="right">4,542,999</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">15,344,262</td>
<td align="right">14,090,696</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">17,331,982</td>
<td align="right">16,008,847</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">3,142,274</td>
<td align="right">3,381,023</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">56,362,472</td>
<td align="right">52,321,526</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">4,053,446</td>
<td align="right">4,322,069</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">5,021,626</td>
<td align="right">5,353,762</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,534,085</td>
<td align="right">3,765,306</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">8,319,650</td>
<td align="right">8,831,260</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">9,940,747</td>
<td align="right">9,358,056</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">16,013,896</td>
<td align="right">16,909,621</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">1,317,405</td>
<td align="right">1,390,429</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">113,765,537</td>
<td align="right">108,027,779</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">6,089,959</td>
<td align="right">6,393,827</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">12,931,792</td>
<td align="right">12,364,935</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">16,494,260</td>
<td align="right">15,790,358</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">9,455,414</td>
<td align="right">9,850,104</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">50,211,491</td>
<td align="right">48,123,163</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">19,224,930</td>
<td align="right">20,006,136</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">501,870</td>
<td align="right">481,710</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">2,480,797</td>
<td align="right">2,382,442</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">2,025,963</td>
<td align="right">1,951,941</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">1,103,892</td>
<td align="right">1,064,514</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">6,425,342</td>
<td align="right">6,240,410</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">693,680</td>
<td align="right">712,552</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">1,249,788</td>
<td align="right">1,216,458</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">3,052,028</td>
<td align="right">2,974,151</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">1,117,701</td>
<td align="right">1,089,264</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,518,894</td>
<td align="right">1,481,206</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">5,682,861</td>
<td align="right">5,542,176</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">575,269</td>
<td align="right">561,032</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">2,941,157</td>
<td align="right">2,870,689</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">17,938,507</td>
<td align="right">17,510,102</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">5,948,321</td>
<td align="right">5,807,090</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">18,959,442</td>
<td align="right">19,387,364</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">4,586,725</td>
<td align="right">4,490,533</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">4,476,910</td>
<td align="right">4,393,625</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">16,971,335</td>
<td align="right">16,678,932</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">9,387,058</td>
<td align="right">9,232,448</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">750,411</td>
<td align="right">738,545</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">10,309,636</td>
<td align="right">10,146,641</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">72,335,623</td>
<td align="right">71,357,912</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">21,497,949</td>
<td align="right">21,207,379</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">22,300,083</td>
<td align="right">22,527,930</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">85,417</td>
<td align="right">84,640</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">16,978,276</td>
<td align="right">17,123,808</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">1,091,768</td>
<td align="right">1,084,730</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">10,050,309</td>
<td align="right">10,105,021</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">5,568,621</td>
<td align="right">5,538,485</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">4,323,540</td>
<td align="right">4,306,988</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">7,308,806</td>
<td align="right">7,281,929</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">1,337,428</td>
<td align="right">1,333,119</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">84,798</td>
<td align="right">84,525</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">893,183</td>
<td align="right">890,851</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">38,017,740</td>
<td align="right">37,926,343</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">16,962,832</td>
<td align="right">16,993,120</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">1,795,639</td>
<td align="right">1,792,846</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">1,490,325</td>
<td align="right">1,488,082</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">554,759</td>
<td align="right">555,279</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">4,521,001</td>
<td align="right">4,516,769</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">645,139</td>
<td align="right">644,797</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,268,317</td>
<td align="right">1,268,464</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">1,277,184</td>
<td align="right">1,277,331</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">21,686</td>
<td align="right">21,687</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">462,021</td>
<td align="right">462,042</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">39,019</td>
<td align="right">39,020</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">1,248,121</td>
<td align="right">1,248,142</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">2,973,599</td>
<td align="right">2,973,599</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">2,718,635</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">2,687,033</td>
<td align="right">2,687,033</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">1,684,019</td>
<td align="right">1,684,019</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">1,684,019</td>
<td align="right">1,684,019</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">1,638,816</td>
<td align="right">1,638,816</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">1,341,773</td>
<td align="right">1,341,773</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">833,724</td>
<td align="right">833,724</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">346,538</td>
<td align="right">346,538</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">296,748</td>
<td align="right">296,748</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">266,667</td>
<td align="right">266,667</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">260,457</td>
<td align="right">260,457</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">247,491</td>
<td align="right">247,491</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">196,241</td>
<td align="right">196,241</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">192,022</td>
<td align="right">192,022</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">176,748</td>
<td align="right">176,748</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">158,435</td>
<td align="right">158,435</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">155,526</td>
<td align="right">155,526</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">149,630</td>
<td align="right">149,630</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">146,480</td>
<td align="right">146,480</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">135,494</td>
<td align="right">135,494</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">119,027</td>
<td align="right">119,027</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">79,885</td>
<td align="right">79,885</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">77,001</td>
<td align="right">77,001</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">64,722</td>
<td align="right">64,722</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">36,237</td>
<td align="right">36,237</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">35,212</td>
<td align="right">35,212</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">28,987</td>
<td align="right">28,987</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">28,010</td>
<td align="right">28,010</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">25,320</td>
<td align="right">25,320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">25,183</td>
<td align="right">25,183</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">23,696</td>
<td align="right">23,696</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">23,535</td>
<td align="right">23,535</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">21,472</td>
<td align="right">21,472</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">16,387</td>
<td align="right">16,387</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">11,469</td>
<td align="right">11,469</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">10,810</td>
<td align="right">10,810</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">10,441</td>
<td align="right">10,441</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">9,256</td>
<td align="right">9,256</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">8,706</td>
<td align="right">8,706</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">8,706</td>
<td align="right">8,706</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">4,541</td>
<td align="right">4,541</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">3,056</td>
<td align="right">3,056</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">2,560</td>
<td align="right">2,560</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">2,240</td>
<td align="right">2,240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">2,075</td>
<td align="right">2,075</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">1,335</td>
<td align="right">1,335</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">501</td>
<td align="right">501</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">348</td>
<td align="right">348</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">298</td>
<td align="right">298</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">259</td>
<td align="right">259</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">175</td>
<td align="right">175</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">129</td>
<td align="right">129</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SETUP_ANNOTATIONS</td>
<td align="right">117</td>
<td align="right">117</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">98</td>
<td align="right">98</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">74</td>
<td align="right">74</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">63</td>
<td align="right">63</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">16</td>
<td align="right">16</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">14</td>
<td align="right">14</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">9</td>
<td align="right">9</td>
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
<td align="right">9,348,292</td>
<td align="right">14.2%</td>
<td align="right">9,192,924</td>
<td align="right">14.0%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">3,100,870</td>
<td align="right">4.7%</td>
<td align="right">3,106,103</td>
<td align="right">4.7%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">53,452,666</td>
<td align="right">81.1%</td>
<td align="right">53,503,949</td>
<td align="right">81.3%</td>
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
<td align="right"></td>
<td align="right"></td>
<td align="right">49</td>
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
<td align="right">36,775</td>
<td align="right">37.9%</td>
<td align="right">37,519</td>
<td align="right">38.3%</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">60,348</td>
<td align="right">62.1%</td>
<td align="right">60,469</td>
<td align="right">61.7%</td>
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
<td align="left">remainder</td>
<td align="right">3,402</td>
<td align="right">9.3%</td>
<td align="right">4,581</td>
<td align="right">12.2%</td>
<td align="right">34.7%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">2,633</td>
<td align="right">7.2%</td>
<td align="right">2,763</td>
<td align="right">7.4%</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">23,921</td>
<td align="right">65.0%</td>
<td align="right">23,356</td>
<td align="right">62.3%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">2,349</td>
<td align="right">6.4%</td>
<td align="right">2,349</td>
<td align="right">6.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">1,522</td>
<td align="right">4.1%</td>
<td align="right">1,522</td>
<td align="right">4.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">742</td>
<td align="right">2.0%</td>
<td align="right">742</td>
<td align="right">2.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">535</td>
<td align="right">1.5%</td>
<td align="right">535</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">254</td>
<td align="right">0.7%</td>
<td align="right">254</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">251</td>
<td align="right">0.7%</td>
<td align="right">251</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">229</td>
<td align="right">0.6%</td>
<td align="right">229</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">196</td>
<td align="right">0.5%</td>
<td align="right">196</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">167</td>
<td align="right">0.5%</td>
<td align="right">167</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">124</td>
<td align="right">0.3%</td>
<td align="right">124</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">or different types</td>
<td align="right">116</td>
<td align="right">0.3%</td>
<td align="right">116</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr other slice</td>
<td align="right">110</td>
<td align="right">0.3%</td>
<td align="right">110</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr counter</td>
<td align="right">92</td>
<td align="right">0.3%</td>
<td align="right">92</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">66</td>
<td align="right">0.2%</td>
<td align="right">66</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">46</td>
<td align="right">0.1%</td>
<td align="right">46</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">6</td>
<td align="right">0.0%</td>
<td align="right">6</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">4</td>
<td align="right">0.0%</td>
<td align="right">4</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr bytes</td>
<td align="right">4</td>
<td align="right">0.0%</td>
<td align="right">4</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">2</td>
<td align="right">0.0%</td>
<td align="right">2</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr range</td>
<td align="right">2</td>
<td align="right">0.0%</td>
<td align="right">2</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">1</td>
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
<td align="right">3,142,274</td>
<td align="right">100.0%</td>
<td align="right">3,381,023</td>
<td align="right">100.0%</td>
<td align="right">7.6%</td>
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
<td align="right">1,919,290</td>
<td align="right">0.8%</td>
<td align="right">1,921,699</td>
<td align="right">0.8%</td>
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
<td align="right">1,898,085</td>
<td align="right">0.8%</td>
<td align="right">1,898,941</td>
<td align="right">0.8%</td>
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
<td align="right">239,666,788</td>
<td align="right">99.2%</td>
<td align="right">239,623,865</td>
<td align="right">99.2%</td>
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
<td align="right">2,524</td>
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
<td align="right">60,224</td>
<td align="right">100.0%</td>
<td align="right">61,778</td>
<td align="right">100.0%</td>
<td align="right">2.6%</td>
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
<td align="right">424</td>
<td align="right">424 / 0 !!</td>
<td align="right">424</td>
<td align="right">424 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">24</td>
<td align="right">24 / 0 !!</td>
<td align="right">24</td>
<td align="right">24 / 0 !!</td>
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
<td align="right">386</td>
<td align="right">18.0%</td>
<td align="right">386</td>
<td align="right">18.0%</td>
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
<td align="right">64</td>
<td align="right">3.0%</td>
<td align="right">64</td>
<td align="right">3.0%</td>
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
<td align="right">1,753</td>
<td align="right">100.0%</td>
<td align="right">1,753</td>
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
<td align="right">641,245</td>
<td align="right">5.5%</td>
<td align="right">640,727</td>
<td align="right">5.5%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">10,933,579</td>
<td align="right">94.4%</td>
<td align="right">10,933,579</td>
<td align="right">94.4%</td>
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
<td align="right">8,087</td>
<td align="right">0.1%</td>
<td align="right">8,087</td>
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
<td align="right">2,679</td>
<td align="right">66.6%</td>
<td align="right">2,855</td>
<td align="right">68.0%</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,345</td>
<td align="right">33.4%</td>
<td align="right">1,345</td>
<td align="right">32.0%</td>
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
<td align="left">different types</td>
<td align="right">1,820</td>
<td align="right">67.9%</td>
<td align="right">1,997</td>
<td align="right">69.9%</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">101</td>
<td align="right">3.8%</td>
<td align="right">100</td>
<td align="right">3.5%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">259</td>
<td align="right">9.7%</td>
<td align="right">259</td>
<td align="right">9.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">251</td>
<td align="right">9.4%</td>
<td align="right">251</td>
<td align="right">8.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">156</td>
<td align="right">5.8%</td>
<td align="right">156</td>
<td align="right">5.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">43</td>
<td align="right">1.6%</td>
<td align="right">43</td>
<td align="right">1.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">27</td>
<td align="right">1.0%</td>
<td align="right">27</td>
<td align="right">0.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">21</td>
<td align="right">0.8%</td>
<td align="right">21</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">1</td>
<td align="right">0.0%</td>
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
<td align="right">4,047,940</td>
<td align="right">25.6%</td>
<td align="right">4,316,201</td>
<td align="right">26.9%</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">11,735,426</td>
<td align="right">74.3%</td>
<td align="right">11,735,426</td>
<td align="right">73.1%</td>
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
<td align="right">4,976</td>
<td align="right">90.4%</td>
<td align="right">5,338</td>
<td align="right">91.0%</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">530</td>
<td align="right">9.6%</td>
<td align="right">530</td>
<td align="right">9.0%</td>
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
<td align="right">1,421</td>
<td align="right">28.6%</td>
<td align="right">1,590</td>
<td align="right">29.8%</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">2,198</td>
<td align="right">44.2%</td>
<td align="right">2,391</td>
<td align="right">44.8%</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">731</td>
<td align="right">14.7%</td>
<td align="right">731</td>
<td align="right">13.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">626</td>
<td align="right">12.6%</td>
<td align="right">626</td>
<td align="right">11.7%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">27,099,755</td>
<td align="right">16.9%</td>
<td align="right">2,523,843</td>
<td align="right">2.2%</td>
<td align="right">-90.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">123,600,599</td>
<td align="right">76.9%</td>
<td align="right">101,993,607</td>
<td align="right">89.6%</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">9,934,525</td>
<td align="right">6.2%</td>
<td align="right">9,310,655</td>
<td align="right">8.2%</td>
<td align="right">-6.3%</td>
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
<td align="right">61,671</td>
<td align="right">0.1%</td>
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
<td align="right">5,567</td>
<td align="right">1.1%</td>
<td align="right">46,746</td>
<td align="right">30.5%</td>
<td align="right">739.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">511,955</td>
<td align="right">98.9%</td>
<td align="right">106,360</td>
<td align="right">69.5%</td>
<td align="right">-79.2%</td>
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
<td align="left">dict items</td>
<td align="right">1,251</td>
<td align="right">22.5%</td>
<td align="right">22,881</td>
<td align="right">48.9%</td>
<td align="right">1,729.0%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">1,789</td>
<td align="right">32.1%</td>
<td align="right">19,321</td>
<td align="right">41.3%</td>
<td align="right">980.0%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">108</td>
<td align="right">1.9%</td>
<td align="right">640</td>
<td align="right">1.4%</td>
<td align="right">492.6%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">276</td>
<td align="right">5.0%</td>
<td align="right">851</td>
<td align="right">1.8%</td>
<td align="right">208.3%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">352</td>
<td align="right">6.3%</td>
<td align="right">668</td>
<td align="right">1.4%</td>
<td align="right">89.8%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">794</td>
<td align="right">14.3%</td>
<td align="right">1,179</td>
<td align="right">2.5%</td>
<td align="right">48.5%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">469</td>
<td align="right">8.4%</td>
<td align="right">678</td>
<td align="right">1.5%</td>
<td align="right">44.6%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">272</td>
<td align="right">4.9%</td>
<td align="right">272</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">96</td>
<td align="right">1.7%</td>
<td align="right">96</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">60</td>
<td align="right">1.1%</td>
<td align="right">60</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">51</td>
<td align="right">0.9%</td>
<td align="right">51</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">49</td>
<td align="right">0.9%</td>
<td align="right">49</td>
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
<td align="right">39,247,173</td>
<td align="right">39,247,173 / 0 !!</td>
<td align="right">39,247,173</td>
<td align="right">39,247,173 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">24,403,908</td>
<td align="right">24,403,908 / 0 !!</td>
<td align="right">24,403,908</td>
<td align="right">24,403,908 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">21,180,612</td>
<td align="right">21,180,612 / 0 !!</td>
<td align="right">21,180,612</td>
<td align="right">21,180,612 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">3,653,809</td>
<td align="right">3,653,809 / 0 !!</td>
<td align="right">3,653,809</td>
<td align="right">3,653,809 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">218,045</td>
<td align="right">218,045 / 0 !!</td>
<td align="right">218,045</td>
<td align="right">218,045 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">149,326</td>
<td align="right">149,326 / 0 !!</td>
<td align="right">149,326</td>
<td align="right">149,326 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">52,709</td>
<td align="right">52,709 / 0 !!</td>
<td align="right">52,709</td>
<td align="right">52,709 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">33,626</td>
<td align="right">33,626 / 0 !!</td>
<td align="right">33,626</td>
<td align="right">33,626 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">1,730</td>
<td align="right">1,730 / 0 !!</td>
<td align="right">1,730</td>
<td align="right">1,730 / 0 !!</td>
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
<td align="right">64,390</td>
<td align="right">0.0%</td>
<td align="right">388,585</td>
<td align="right">0.1%</td>
<td align="right">503.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">133,978,697</td>
<td align="right">33.8%</td>
<td align="right">91,392,436</td>
<td align="right">25.7%</td>
<td align="right">-31.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">55,772,995</td>
<td align="right">14.1%</td>
<td align="right">52,121,413</td>
<td align="right">14.7%</td>
<td align="right">-6.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">206,478,183</td>
<td align="right">52.0%</td>
<td align="right">211,773,569</td>
<td align="right">59.6%</td>
<td align="right">2.6%</td>
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
<td align="right">186,100</td>
<td align="right">6.9%</td>
<td align="right">69,509</td>
<td align="right">3.5%</td>
<td align="right">-62.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,530,611</td>
<td align="right">93.1%</td>
<td align="right">1,934,176</td>
<td align="right">96.5%</td>
<td align="right">-23.6%</td>
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
<td align="left">overridden</td>
<td align="right">646</td>
<td align="right">0.3%</td>
<td align="right">1,762</td>
<td align="right">2.5%</td>
<td align="right">172.8%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">2,861</td>
<td align="right">1.5%</td>
<td align="right">6,898</td>
<td align="right">9.9%</td>
<td align="right">141.1%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">323</td>
<td align="right">0.2%</td>
<td align="right">561</td>
<td align="right">0.8%</td>
<td align="right">73.7%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">1,314</td>
<td align="right">0.7%</td>
<td align="right">2,005</td>
<td align="right">2.9%</td>
<td align="right">52.6%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">3,081</td>
<td align="right">1.7%</td>
<td align="right">4,559</td>
<td align="right">6.6%</td>
<td align="right">48.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">764</td>
<td align="right">0.4%</td>
<td align="right">741</td>
<td align="right">1.1%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">4,561</td>
<td align="right">2.5%</td>
<td align="right">4,664</td>
<td align="right">6.7%</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">996</td>
<td align="right">0.5%</td>
<td align="right">996</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">70</td>
<td align="right">0.0%</td>
<td align="right">70</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">65</td>
<td align="right">0.0%</td>
<td align="right">65</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">7</td>
<td align="right">0.0%</td>
<td align="right">7</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">2</td>
<td align="right">0.0%</td>
<td align="right">2</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">2</td>
<td align="right">0.0%</td>
<td align="right">2</td>
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
<td align="right">205,585,104</td>
<td align="right">100.0%</td>
<td align="right">207,330,603</td>
<td align="right">100.0%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,812</td>
<td align="right">0.0%</td>
<td align="right">2,812</td>
<td align="right">0.0%</td>
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
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">1</td>
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
<td align="right">14,050</td>
<td align="right">0.0%</td>
<td align="right">14,050</td>
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
<td align="right">19,343</td>
<td align="right">100.0%</td>
<td align="right">19,344</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">50</td>
<td align="right">0.0%</td>
<td align="right">50</td>
<td align="right">0.0%</td>
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
<td align="right">425,102</td>
<td align="right">99.9%</td>
<td align="right">425,102</td>
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
<td align="right">209</td>
<td align="right">100.0%</td>
<td align="right">209</td>
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
<td align="right">4,490</td>
<td align="right">29.2%</td>
<td align="right">4,490</td>
<td align="right">29.2%</td>
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
<td align="right">10,810</td>
<td align="right">70.4%</td>
<td align="right">10,810</td>
<td align="right">70.4%</td>
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
<td align="right">4</td>
<td align="right">7.8%</td>
<td align="right">4</td>
<td align="right">7.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">47</td>
<td align="right">92.2%</td>
<td align="right">47</td>
<td align="right">92.2%</td>
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
<td align="right">47</td>
<td align="right">100.0%</td>
<td align="right">47</td>
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
<td align="right">9,609,951</td>
<td align="right">28.5%</td>
<td align="right">9,481,229</td>
<td align="right">28.1%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">14,063,495</td>
<td align="right">41.7%</td>
<td align="right">14,191,252</td>
<td align="right">42.0%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">10,035,354</td>
<td align="right">29.8%</td>
<td align="right">10,002,479</td>
<td align="right">29.6%</td>
<td align="right">-0.3%</td>
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
<td align="right">2,729</td>
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
<td align="right">9,808</td>
<td align="right">5.0%</td>
<td align="right">97,395</td>
<td align="right">34.5%</td>
<td align="right">893.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">185,984</td>
<td align="right">95.0%</td>
<td align="right">185,019</td>
<td align="right">65.5%</td>
<td align="right">-0.5%</td>
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
<td align="right">5,037</td>
<td align="right">51.4%</td>
<td align="right">92,518</td>
<td align="right">95.0%</td>
<td align="right">1,736.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">170,832</td>
<td align="right">1,741.8%</td>
<td align="right">46,601</td>
<td align="right">47.8%</td>
<td align="right">-72.7%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">643</td>
<td align="right">6.6%</td>
<td align="right">749</td>
<td align="right">0.8%</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">2,626</td>
<td align="right">26.8%</td>
<td align="right">2,626</td>
<td align="right">2.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">311</td>
<td align="right">3.2%</td>
<td align="right">311</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">290</td>
<td align="right">3.0%</td>
<td align="right">290</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">119</td>
<td align="right">1.2%</td>
<td align="right">119</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">94</td>
<td align="right">1.0%</td>
<td align="right">94</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">5</td>
<td align="right">0.1%</td>
<td align="right">5</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">1</td>
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
<td align="right">196,241</td>
<td align="right">100.0%</td>
<td align="right">196,241</td>
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
<td align="right">1,486,372</td>
<td align="right">14.0%</td>
<td align="right">1,484,019</td>
<td align="right">13.9%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">9,156,647</td>
<td align="right">86.0%</td>
<td align="right">9,156,647</td>
<td align="right">86.0%</td>
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
<td align="right">3,478</td>
<td align="right">88.0%</td>
<td align="right">3,588</td>
<td align="right">88.3%</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">475</td>
<td align="right">12.0%</td>
<td align="right">475</td>
<td align="right">11.7%</td>
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
<td align="left">bytearray int</td>
<td align="right">16</td>
<td align="right">0.5%</td>
<td align="right">20</td>
<td align="right">0.6%</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">2,962</td>
<td align="right">85.2%</td>
<td align="right">3,068</td>
<td align="right">85.5%</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">341</td>
<td align="right">9.8%</td>
<td align="right">341</td>
<td align="right">9.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">113</td>
<td align="right">3.2%</td>
<td align="right">113</td>
<td align="right">3.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">46</td>
<td align="right">1.3%</td>
<td align="right">46</td>
<td align="right">1.3%</td>
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
<td align="right">15,192,688</td>
<td align="right">8.2%</td>
<td align="right">13,942,374</td>
<td align="right">7.5%</td>
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
<td align="right">5,285,981</td>
<td align="right">2.8%</td>
<td align="right">5,254,260</td>
<td align="right">2.8%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">165,576,589</td>
<td align="right">88.9%</td>
<td align="right">165,683,641</td>
<td align="right">89.5%</td>
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
<td align="right"></td>
<td align="right"></td>
<td align="right">1,648</td>
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
<td align="right">147,607</td>
<td align="right">58.8%</td>
<td align="right">144,355</td>
<td align="right">58.1%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">103,628</td>
<td align="right">41.2%</td>
<td align="right">104,188</td>
<td align="right">41.9%</td>
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
<td align="left">other</td>
<td align="right">243</td>
<td align="right">0.2%</td>
<td align="right">264</td>
<td align="right">0.2%</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">134,241</td>
<td align="right">90.9%</td>
<td align="right">131,045</td>
<td align="right">90.8%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">9,937</td>
<td align="right">6.7%</td>
<td align="right">9,860</td>
<td align="right">6.8%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">2,081</td>
<td align="right">1.4%</td>
<td align="right">2,081</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">880</td>
<td align="right">0.6%</td>
<td align="right">880</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">118</td>
<td align="right">0.1%</td>
<td align="right">118</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">107</td>
<td align="right">0.1%</td>
<td align="right">107</td>
<td align="right">0.1%</td>
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
<td align="right">296,268</td>
<td align="right">2.0%</td>
<td align="right">296,268</td>
<td align="right">2.0%</td>
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
<td align="right">14,610,131</td>
<td align="right">98.0%</td>
<td align="right">14,610,131</td>
<td align="right">98.0%</td>
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
<td align="right">383</td>
<td align="right">79.8%</td>
<td align="right">383</td>
<td align="right">79.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">97</td>
<td align="right">20.2%</td>
<td align="right">97</td>
<td align="right">20.2%</td>
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
<td align="right">74</td>
<td align="right">76.3%</td>
<td align="right">74</td>
<td align="right">76.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">23</td>
<td align="right">23.7%</td>
<td align="right">23</td>
<td align="right">23.7%</td>
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
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">181,018,930</td>
<td align="right">5.0%</td>
<td align="right">113,703,567</td>
<td align="right">4.0%</td>
<td align="right">-37.2%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">199,122,435</td>
<td align="right">5.5%</td>
<td align="right">142,856,480</td>
<td align="right">5.0%</td>
<td align="right">-28.3%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">1,275,140,872</td>
<td align="right">35.1%</td>
<td align="right">966,375,073</td>
<td align="right">33.9%</td>
<td align="right">-24.2%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">1,972,750,389</td>
<td align="right">54.4%</td>
<td align="right">1,628,952,874</td>
<td align="right">57.1%</td>
<td align="right">-17.4%</td>
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
<td align="left">TO_BOOL</td>
<td align="right">15,192,688</td>
<td align="right">13.6%</td>
<td align="right">13,942,374</td>
<td align="right">13.1%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">3,142,274</td>
<td align="right">2.8%</td>
<td align="right">3,381,023</td>
<td align="right">3.2%</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">4,047,940</td>
<td align="right">3.6%</td>
<td align="right">4,316,201</td>
<td align="right">4.0%</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">55,772,995</td>
<td align="right">49.8%</td>
<td align="right">52,121,413</td>
<td align="right">48.8%</td>
<td align="right">-6.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">9,934,525</td>
<td align="right">8.9%</td>
<td align="right">9,310,655</td>
<td align="right">8.7%</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">9,348,292</td>
<td align="right">8.3%</td>
<td align="right">9,192,924</td>
<td align="right">8.6%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">10,035,354</td>
<td align="right">9.0%</td>
<td align="right">10,002,479</td>
<td align="right">9.4%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">1,486,372</td>
<td align="right">1.3%</td>
<td align="right">1,484,019</td>
<td align="right">1.4%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">641,245</td>
<td align="right">0.6%</td>
<td align="right">640,727</td>
<td align="right">0.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,898,085</td>
<td align="right">1.7%</td>
<td align="right">1,898,941</td>
<td align="right">1.8%</td>
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
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">13,549,279</td>
<td align="right">7.5%</td>
<td align="right">1,239,830</td>
<td align="right">1.1%</td>
<td align="right">-90.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">13,550,476</td>
<td align="right">7.5%</td>
<td align="right">1,284,013</td>
<td align="right">1.1%</td>
<td align="right">-90.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">41,882,177</td>
<td align="right">23.1%</td>
<td align="right">17,032,615</td>
<td align="right">15.0%</td>
<td align="right">-59.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">23,418,650</td>
<td align="right">12.9%</td>
<td align="right">13,433,167</td>
<td align="right">11.8%</td>
<td align="right">-42.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">49,101,018</td>
<td align="right">27.1%</td>
<td align="right">42,582,000</td>
<td align="right">37.4%</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">7,690,738</td>
<td align="right">4.2%</td>
<td align="right">7,305,612</td>
<td align="right">6.4%</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">9,554,980</td>
<td align="right">5.3%</td>
<td align="right">9,426,258</td>
<td align="right">8.3%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">4,346,614</td>
<td align="right">2.4%</td>
<td align="right">4,327,690</td>
<td align="right">3.8%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">10,348,805</td>
<td align="right">5.7%</td>
<td align="right">10,350,920</td>
<td align="right">9.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">2,342,077</td>
<td align="right">1.3%</td>
<td align="right">2,342,010</td>
<td align="right">2.1%</td>
<td align="right">-0.0%</td>
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
<td align="right">18,548,610</td>
<td align="right">8.5%</td>
<td align="right">18,459,189</td>
<td align="right">8.4%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">39,596,863</td>
<td align="right">18.1%</td>
<td align="right">39,505,466</td>
<td align="right">18.0%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">39,598,585</td>
<td align="right">18.1%</td>
<td align="right">39,507,188</td>
<td align="right">18.0%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">40,141,976</td>
<td align="right">18.3%</td>
<td align="right">40,050,579</td>
<td align="right">18.3%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">40,141,976</td>
<td align="right">18.3%</td>
<td align="right">40,050,579</td>
<td align="right">18.3%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">179,017,035</td>
<td align="right">81.7%</td>
<td align="right">179,108,432</td>
<td align="right">81.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">158,090,941</td>
<td align="right">72.1%</td>
<td align="right">158,092,917</td>
<td align="right">72.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">543,391</td>
<td align="right">0.2%</td>
<td align="right">543,391</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">387</td>
<td align="right">0.0%</td>
<td align="right">387</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">1,335</td>
<td align="right">0.0%</td>
<td align="right">1,335</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">10,469,903</td>
<td align="right">4.8%</td>
<td align="right">10,469,903</td>
<td align="right">4.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">502,516</td>
<td align="right">0.2%</td>
<td align="right">502,516</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">256</td>
<td align="right">0.0%</td>
<td align="right">256</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">6,772,045</td>
<td align="right">3.1%</td>
<td align="right">6,772,045</td>
<td align="right">3.1%</td>
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
<td align="right">775,135,623</td>
<td align="right">31.7%</td>
<td align="right">611,193,886</td>
<td align="right">25.2%</td>
<td align="right">-21.2%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">922,946,074</td>
<td align="right">37.8%</td>
<td align="right">1,092,521,022</td>
<td align="right">45.0%</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">2,740,363</td>
<td align="right"></td>
<td align="right">2,363,475</td>
<td align="right"></td>
<td align="right">-13.8%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">811,035,452</td>
<td align="right">32.4%</td>
<td align="right">912,372,916</td>
<td align="right">36.6%</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">62,106</td>
<td align="right">0.0%</td>
<td align="right">67,676</td>
<td align="right">0.0%</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">1,092,283,736</td>
<td align="right">43.6%</td>
<td align="right">996,796,697</td>
<td align="right">40.0%</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">12,582,903</td>
<td align="right"></td>
<td align="right">11,618,815</td>
<td align="right"></td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">9,844,103</td>
<td align="right"></td>
<td align="right">9,256,872</td>
<td align="right"></td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">622,787,270</td>
<td align="right">25.5%</td>
<td align="right">596,949,767</td>
<td align="right">24.6%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">121,703,315</td>
<td align="right">5.0%</td>
<td align="right">125,406,055</td>
<td align="right">5.2%</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">516,863,656</td>
<td align="right">20.6%</td>
<td align="right">502,154,547</td>
<td align="right">20.1%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">203,014,753</td>
<td align="right"></td>
<td align="right">197,858,700</td>
<td align="right"></td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">1,423,513</td>
<td align="right">0.6%</td>
<td align="right">1,430,495</td>
<td align="right">0.6%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">83,332,013</td>
<td align="right">3.3%</td>
<td align="right">83,232,370</td>
<td align="right">3.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">141,783,678</td>
<td align="right"></td>
<td align="right">141,909,307</td>
<td align="right"></td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">107,348,106</td>
<td align="right"></td>
<td align="right">107,368,219</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">107,367,320</td>
<td align="right">45.0%</td>
<td align="right">107,387,370</td>
<td align="right">45.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">155,002,051</td>
<td align="right"></td>
<td align="right">154,987,729</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">131,355,591</td>
<td align="right">55.0%</td>
<td align="right">131,362,485</td>
<td align="right">55.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">129,869,972</td>
<td align="right">54.4%</td>
<td align="right">129,864,314</td>
<td align="right">54.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">3,080,797</td>
<td align="right"></td>
<td align="right">3,080,797</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">997,135</td>
<td align="right">32.4%</td>
<td align="right">997,135</td>
<td align="right">32.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">98,881</td>
<td align="right">3.2%</td>
<td align="right">98,881</td>
<td align="right">3.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">1,344</td>
<td align="right">0.0%</td>
<td align="right">1,344</td>
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
<td align="right">6,260</td>
<td align="right">12,777,902</td>
<td align="right">257,939,739</td>
<td align="right">16,407,949</td>
<td align="right">23,230,644</td>
<td align="right">6,240</td>
<td align="right">12,889,970</td>
<td align="right">261,228,491</td>
<td align="right">16,127,085</td>
<td align="right">23,497,676</td>
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
<td align="right">19,982</td>
<td align="right"></td>
<td align="right">1,122,046</td>
<td align="right"></td>
<td align="right">5,515.3%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">960</td>
<td align="right">4.8%</td>
<td align="right">13,537</td>
<td align="right">1.2%</td>
<td align="right">1,310.1%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">42,141,481</td>
<td align="right"></td>
<td align="right">218,893,413</td>
<td align="right"></td>
<td align="right">419.4%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">826,961,812</td>
<td align="right">1,962.3%</td>
<td align="right">3,817,678,724</td>
<td align="right">1,744.1%</td>
<td align="right">361.7%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">1,270</td>
<td align="right">6.4%</td>
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
<td align="right">148</td>
<td align="right">0.7%</td>
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
<td align="right">22</td>
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
<td align="right">17,604</td>
<td align="right">88.1%</td>
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
<td align="right">656</td>
<td align="right">0.1%</td>
<td align="right">656 / 0 !!</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
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
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">87</td>
<td align="right">0.6%</td>
<td align="right">87 / 0 !!</td>
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
<td align="right">875</td>
<td align="right">91.1%</td>
<td align="right">13,432</td>
<td align="right">99.2%</td>
<td align="right">1,435.1%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">960</td>
<td align="right"></td>
<td align="right">13,537</td>
<td align="right"></td>
<td align="right">1,310.1%</td>
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
<td align="right">4,193,898</td>
<td align="right">67.1%</td>
<td align="right">223,825,695</td>
<td align="right">86.9%</td>
<td align="right">5,236.9%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">6,246,400</td>
<td align="right"></td>
<td align="right">257,658,880</td>
<td align="right"></td>
<td align="right">4,024.9%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">118,720</td>
<td align="right">1.9%</td>
<td align="right">3,871,680</td>
<td align="right">1.5%</td>
<td align="right">3,161.2%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">1,932,906</td>
<td align="right">30.9%</td>
<td align="right">29,948,073</td>
<td align="right">11.6%</td>
<td align="right">1,449.4%</td>
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
<td align="right">4,096</td>
<td align="right">0.0%</td>
<td align="right">4,096 / 0 !!</td>
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
<td align="left">335</td>
<td align="right">38.2%</td>
<td align="left">3,361</td>
<td align="right">25.0%</td>
<td align="right">903.3%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">454</td>
<td align="right">51.8%</td>
<td align="left">4,006</td>
<td align="right">29.8%</td>
<td align="right">782.4%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">87</td>
<td align="right">9.9%</td>
<td align="left">1,739</td>
<td align="right">12.9%</td>
<td align="right">1,898.9%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">2,673</td>
<td align="right">19.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">640</td>
<td align="right">4.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">1,013</td>
<td align="right">7.5%</td>
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
<td align="right">25</td>
<td align="right">2.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">220</td>
<td align="right">22.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">543</td>
<td align="right">56.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">172</td>
<td align="right">17.9%</td>
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
<td align="left"><= 8</td>
<td align="right">21</td>
<td align="right">2.2%</td>
<td align="right">21</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">47</td>
<td align="right">4.9%</td>
<td align="right">1,734</td>
<td align="right">12.8%</td>
<td align="right">3,589.4%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">439</td>
<td align="right">45.7%</td>
<td align="right">3,153</td>
<td align="right">23.3%</td>
<td align="right">618.2%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">347</td>
<td align="right">36.1%</td>
<td align="right">2,844</td>
<td align="right">21.0%</td>
<td align="right">719.6%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">21</td>
<td align="right">2.2%</td>
<td align="right">2,202</td>
<td align="right">16.3%</td>
<td align="right">10,385.7%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">2,190</td>
<td align="right">16.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">548</td>
<td align="right">4.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">740</td>
<td align="right">5.5%</td>
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
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right">4,620</td>
<td align="right">1,322,733</td>
<td align="right">28,530.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">298,892</td>
<td align="right">39,110,508</td>
<td align="right">12,985.2%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">3,644</td>
<td align="right">438,503</td>
<td align="right">11,933.6%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">295,542</td>
<td align="right">20,912,071</td>
<td align="right">6,975.8%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">295,542</td>
<td align="right">20,864,761</td>
<td align="right">6,959.8%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">795,104</td>
<td align="right">51,588,747</td>
<td align="right">6,388.3%</td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right">714,592</td>
<td align="right">34,871,888</td>
<td align="right">4,780.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">2,131,043</td>
<td align="right">77,324,420</td>
<td align="right">3,528.5%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">19,509</td>
<td align="right">586,366</td>
<td align="right">2,905.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">3,499</td>
<td align="right">102,391</td>
<td align="right">2,826.3%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">108,927</td>
<td align="right">3,007,096</td>
<td align="right">2,660.7%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">1,808,129</td>
<td align="right">46,513,433</td>
<td align="right">2,472.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">2,017,548</td>
<td align="right">34,616,148</td>
<td align="right">1,615.8%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">3,160,277</td>
<td align="right">37,842,956</td>
<td align="right">1,097.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">5,021,978</td>
<td align="right">45,556,246</td>
<td align="right">807.1%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">5,517,719</td>
<td align="right">40,816,158</td>
<td align="right">639.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">13,528,749</td>
<td align="right">86,541,390</td>
<td align="right">539.7%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">10,059,731</td>
<td align="right">59,827,763</td>
<td align="right">494.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">10,059,731</td>
<td align="right">59,175,801</td>
<td align="right">488.2%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">33,129,827</td>
<td align="right">182,329,731</td>
<td align="right">450.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">367,778</td>
<td align="right">1,966,999</td>
<td align="right">434.8%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">33,020,421</td>
<td align="right">167,980,297</td>
<td align="right">408.7%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">8,453,714</td>
<td align="right">39,201,940</td>
<td align="right">363.7%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">155,273,868</td>
<td align="right">687,856,414</td>
<td align="right">343.0%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">12,483,824</td>
<td align="right">54,994,786</td>
<td align="right">340.5%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">45,102,890</td>
<td align="right">192,508,089</td>
<td align="right">326.8%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">9,011,654</td>
<td align="right">36,563,682</td>
<td align="right">305.7%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">126,993,646</td>
<td align="right">512,210,495</td>
<td align="right">303.3%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">6,451,905</td>
<td align="right">24,713,270</td>
<td align="right">283.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">34,680,651</td>
<td align="right">127,251,612</td>
<td align="right">266.9%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">1,807,073</td>
<td align="right">6,520,632</td>
<td align="right">260.8%</td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right">340</td>
<td align="right">1,160</td>
<td align="right">241.2%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">25,893,745</td>
<td align="right">86,932,811</td>
<td align="right">235.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">37,635</td>
<td align="right">125,365</td>
<td align="right">233.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">12,368,397</td>
<td align="right">40,752,534</td>
<td align="right">229.5%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">14,572,008</td>
<td align="right">40,445,112</td>
<td align="right">177.6%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">138,223</td>
<td align="right">321,058</td>
<td align="right">132.3%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">138,223</td>
<td align="right">321,058</td>
<td align="right">132.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">138,223</td>
<td align="right">318,988</td>
<td align="right">130.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">617,130</td>
<td align="right">1,379,763</td>
<td align="right">123.6%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">96,537</td>
<td align="right">4,437</td>
<td align="right">-95.4%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,139,986</td>
<td align="right">76,503</td>
<td align="right">-93.3%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">8,378,000</td>
<td align="right">801,811</td>
<td align="right">-90.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right">8,378,000</td>
<td align="right">801,811</td>
<td align="right">-90.4%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">443,192</td>
<td align="right">44,731</td>
<td align="right">-89.9%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">463,730</td>
<td align="right">48,386</td>
<td align="right">-89.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">443,192</td>
<td align="right">55,928</td>
<td align="right">-87.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_SLICE</td>
<td align="right">443,192</td>
<td align="right">55,928</td>
<td align="right">-87.4%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">7,489,227</td>
<td align="right">13,889,973</td>
<td align="right">85.5%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">120,897</td>
<td align="right">18,448</td>
<td align="right">-84.7%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">3,099,324</td>
<td align="right">513,110</td>
<td align="right">-83.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_OVERFLOWED</td>
<td align="right">290,312</td>
<td align="right">58,471</td>
<td align="right">-79.9%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">286,587</td>
<td align="right">58,318</td>
<td align="right">-79.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right">4,917,500</td>
<td align="right">1,045,284</td>
<td align="right">-78.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">7,489,227</td>
<td align="right">13,354,132</td>
<td align="right">78.3%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">2,509,165</td>
<td align="right">552,496</td>
<td align="right">-78.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_OVERFLOWED</td>
<td align="right">372,581</td>
<td align="right">84,780</td>
<td align="right">-77.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">2,155,905</td>
<td align="right">577,594</td>
<td align="right">-73.2%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">1,958,767</td>
<td align="right">631,453</td>
<td align="right">-67.8%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,837,412</td>
<td align="right">595,214</td>
<td align="right">-67.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">1,170,749</td>
<td align="right">402,329</td>
<td align="right">-65.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_DICT</td>
<td align="right">2,430,932</td>
<td align="right">848,222</td>
<td align="right">-65.1%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">366,968</td>
<td align="right">128,219</td>
<td align="right">-65.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">981,316</td>
<td align="right">348,207</td>
<td align="right">-64.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">1,075,591</td>
<td align="right">382,689</td>
<td align="right">-64.4%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">1,075,591</td>
<td align="right">382,689</td>
<td align="right">-64.4%</td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">139</td>
<td align="right">50</td>
<td align="right">-64.0%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">433,765</td>
<td align="right">165,504</td>
<td align="right">-61.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">2,786,626</td>
<td align="right">1,078,867</td>
<td align="right">-61.3%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">977,939</td>
<td align="right">379,843</td>
<td align="right">-61.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">637,283</td>
<td align="right">252,155</td>
<td align="right">-60.4%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">1,377,839</td>
<td align="right">2,187,066</td>
<td align="right">58.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,932,516</td>
<td align="right">3,060,424</td>
<td align="right">58.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right">1,060,066</td>
<td align="right">446,593</td>
<td align="right">-57.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">707,019</td>
<td align="right">302,721</td>
<td align="right">-57.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">7,225,047</td>
<td align="right">3,174,767</td>
<td align="right">-56.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">3,338,630</td>
<td align="right">1,471,521</td>
<td align="right">-55.9%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">35,105</td>
<td align="right">16,233</td>
<td align="right">-53.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">1,332,846</td>
<td align="right">629,594</td>
<td align="right">-52.8%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">5,387,635</td>
<td align="right">2,584,069</td>
<td align="right">-52.0%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">658,308</td>
<td align="right">321,107</td>
<td align="right">-51.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">2,041,107</td>
<td align="right">1,008,357</td>
<td align="right">-50.6%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">1,797,020</td>
<td align="right">901,951</td>
<td align="right">-49.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">8,921,226</td>
<td align="right">4,514,879</td>
<td align="right">-49.4%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">682,505</td>
<td align="right">350,369</td>
<td align="right">-48.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">1,253,803</td>
<td align="right">645,374</td>
<td align="right">-48.5%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">1,797,020</td>
<td align="right">941,040</td>
<td align="right">-47.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">1,890,472</td>
<td align="right">1,030,921</td>
<td align="right">-45.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">4,711,031</td>
<td align="right">2,671,679</td>
<td align="right">-43.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">1,230,523</td>
<td align="right">699,283</td>
<td align="right">-43.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">9,480,783</td>
<td align="right">5,539,364</td>
<td align="right">-41.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">6,264,233</td>
<td align="right">3,765,891</td>
<td align="right">-39.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">8,677,791</td>
<td align="right">5,276,880</td>
<td align="right">-39.2%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">2,363,026</td>
<td align="right">1,477,954</td>
<td align="right">-37.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">1,054,038</td>
<td align="right">675,739</td>
<td align="right">-35.9%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,429,610</td>
<td align="right">918,000</td>
<td align="right">-35.8%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">731,232</td>
<td align="right">500,011</td>
<td align="right">-31.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right">1,692,028</td>
<td align="right">1,191,373</td>
<td align="right">-29.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">8,415,787</td>
<td align="right">10,894,689</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">258,090</td>
<td align="right">185,066</td>
<td align="right">-28.3%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">8,826,236</td>
<td align="right">6,400,993</td>
<td align="right">-27.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">6,667,852</td>
<td align="right">4,872,283</td>
<td align="right">-26.9%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">1,411,421</td>
<td align="right">1,032,573</td>
<td align="right">-26.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">4,926,200</td>
<td align="right">3,605,886</td>
<td align="right">-26.8%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">11,092,579</td>
<td align="right">8,427,747</td>
<td align="right">-24.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">11,047,745</td>
<td align="right">8,401,886</td>
<td align="right">-23.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">4,004,012</td>
<td align="right">3,067,664</td>
<td align="right">-23.4%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">19,236</td>
<td align="right">23,468</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">4,890,708</td>
<td align="right">3,847,780</td>
<td align="right">-21.3%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">799,755</td>
<td align="right">654,223</td>
<td align="right">-18.2%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">3,692,052</td>
<td align="right">4,315,922</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">771,316</td>
<td align="right">650,330</td>
<td align="right">-15.7%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">11,973,063</td>
<td align="right">10,178,401</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">19,929</td>
<td align="right">21,917</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_LIST</td>
<td align="right">19,929</td>
<td align="right">21,559</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">6,481,972</td>
<td align="right">5,952,679</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">7,406,646</td>
<td align="right">6,813,698</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE</td>
<td align="right">295,542</td>
<td align="right">276,559</td>
<td align="right">-6.4%</td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">3,381</td>
<td align="right">3,234</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">3,381</td>
<td align="right">3,234</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">767,515</td>
<td align="right">784,067</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">180,103</td>
<td align="right">182,456</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">84,992</td>
<td align="right">84,736</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">19,236</td>
<td align="right">19,215</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_CALL_KW_NON_PY</td>
<td align="right">19,236</td>
<td align="right">19,215</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE_KW</td>
<td align="right">19,236</td>
<td align="right">19,215</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">12,996,620</td>
<td align="right">13,008,287</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">150,702,599</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right"></td>
<td align="right">89,663,154</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">53,184,095</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right"></td>
<td align="right">40,374,756</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">36,534,776</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right"></td>
<td align="right">36,402,600</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right"></td>
<td align="right">36,341,352</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right"></td>
<td align="right">35,092,569</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right"></td>
<td align="right">35,092,569</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right"></td>
<td align="right">34,908,597</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">34,371,085</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right"></td>
<td align="right">34,087,514</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right"></td>
<td align="right">33,828,302</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right"></td>
<td align="right">33,354,990</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right"></td>
<td align="right">20,136,243</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_FOR</td>
<td align="right"></td>
<td align="right">17,291,438</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right"></td>
<td align="right">16,016,095</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">11,341,128</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">7,548,212</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right"></td>
<td align="right">3,479,741</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right">2,019,459</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right"></td>
<td align="right">1,884,918</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right"></td>
<td align="right">1,322,757</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right"></td>
<td align="right">1,202,791</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right"></td>
<td align="right">953,527</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right"></td>
<td align="right">708,305</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PY_FRAME_GENERAL</td>
<td align="right"></td>
<td align="right">702,931</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">672,528</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_KW</td>
<td align="right"></td>
<td align="right">507,467</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PY_FRAME_KW</td>
<td align="right"></td>
<td align="right">507,467</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION_AND_LOCK</td>
<td align="right"></td>
<td align="right">299,496</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">297,592</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right"></td>
<td align="right">292,403</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right"></td>
<td align="right">289,605</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">289,605</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NULL</td>
<td align="right"></td>
<td align="right">274,523</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right"></td>
<td align="right">253,851</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LEN</td>
<td align="right"></td>
<td align="right">219,209</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right"></td>
<td align="right">204,337</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right"></td>
<td align="right">142,327</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right"></td>
<td align="right">141,231</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right"></td>
<td align="right">140,685</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">105,442</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right"></td>
<td align="right">96,192</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right"></td>
<td align="right">82,017</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_CHECK_FUNC</td>
<td align="right"></td>
<td align="right">74,022</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_INIT_CALL</td>
<td align="right"></td>
<td align="right">74,022</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">71,336</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">71,336</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right"></td>
<td align="right">70,468</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_PROPERTY_FRAME</td>
<td align="right"></td>
<td align="right">61,248</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_EXTEND</td>
<td align="right"></td>
<td align="right">39,377</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_BINARY_OP_EXTEND</td>
<td align="right"></td>
<td align="right">39,377</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right"></td>
<td align="right">37,688</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_CALL_LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">33,333</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right"></td>
<td align="right">32,875</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">28,807</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right"></td>
<td align="right">28,437</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_STR_1</td>
<td align="right"></td>
<td align="right">28,437</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right"></td>
<td align="right">26,877</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_TYPE_1</td>
<td align="right"></td>
<td align="right">26,877</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right"></td>
<td align="right">20,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_AND_ALLOCATE_OBJECT</td>
<td align="right"></td>
<td align="right">19,857</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right"></td>
<td align="right">16,185</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right"></td>
<td align="right">14,700</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right"></td>
<td align="right">14,510</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right"></td>
<td align="right">11,866</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right"></td>
<td align="right">10,656</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right"></td>
<td align="right">7,557</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right"></td>
<td align="right">7,038</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS</td>
<td align="right"></td>
<td align="right">5,225</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_ANY_SET</td>
<td align="right"></td>
<td align="right">4,130</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_1</td>
<td align="right"></td>
<td align="right">3,843</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right"></td>
<td align="right">2,793</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CREATE_INIT_FRAME</td>
<td align="right"></td>
<td align="right">2,437</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_TUPLE</td>
<td align="right"></td>
<td align="right">1,646</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_INIT_CHECK</td>
<td align="right"></td>
<td align="right">1,456</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SWAP_3</td>
<td align="right"></td>
<td align="right">1,268</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right"></td>
<td align="right">777</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right"></td>
<td align="right">451</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right"></td>
<td align="right">273</td>
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
<td align="right">192</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">21</td>
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
<td align="right">227</td>
<td align="right">227</td>
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
<td align="right">126</td>
<td align="right">126 / 0 !!</td>
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
<td align="right">126</td>
<td align="right">126 / 0 !!</td>
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
<td align="right">21</td>
<td align="right">21</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-10-22
