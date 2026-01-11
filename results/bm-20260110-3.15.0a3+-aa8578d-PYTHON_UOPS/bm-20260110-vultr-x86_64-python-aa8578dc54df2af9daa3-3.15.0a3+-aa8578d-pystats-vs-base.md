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
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,604,169,952</td>
<td align="right">10</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">158,327,123</td>
<td align="right">1</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">417,869,997</td>
<td align="right">3</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">569,319,729</td>
<td align="right">5</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">195,690,042</td>
<td align="right">2</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">131,335,896</td>
<td align="right">2</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,754,427,326</td>
<td align="right">42</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">308,729,599</td>
<td align="right">19</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">116,416,454</td>
<td align="right">8</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">57,484,640</td>
<td align="right">4</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">444,852,794</td>
<td align="right">39</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">265,402,206</td>
<td align="right">26</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">189,463,675</td>
<td align="right">22</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">41,963,287</td>
<td align="right">5</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">195,581,480</td>
<td align="right">29</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">33,573,506</td>
<td align="right">5</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">120,080,873</td>
<td align="right">18</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">386,695,578</td>
<td align="right">59</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">125,175,217</td>
<td align="right">20</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,156,329</td>
<td align="right">1</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">64,266,129</td>
<td align="right">11</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">5,829,879</td>
<td align="right">1</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">161,939,095</td>
<td align="right">29</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">72,218,032</td>
<td align="right">14</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">65,911,089</td>
<td align="right">14</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">67,374,533</td>
<td align="right">19</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">59,268,245</td>
<td align="right">19</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">68,460,576</td>
<td align="right">28</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">9,740,382</td>
<td align="right">5</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">219,363,920</td>
<td align="right">477</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">5,073,159</td>
<td align="right">13</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">2,714,780,498</td>
<td align="right">8,450</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">691,475,902</td>
<td align="right">2,159</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">140,684,617</td>
<td align="right">462</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">125,523,387</td>
<td align="right">507</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,505,133,469</td>
<td align="right">7,422</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">232,195,573</td>
<td align="right">1,187</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,433,107,694</td>
<td align="right">16,304</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,145,036,111</td>
<td align="right">8,100</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">157,765,596</td>
<td align="right">1,134</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">2,662,618</td>
<td align="right">24</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">4,545,218</td>
<td align="right">68</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">889,529,139</td>
<td align="right">13,758</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">543,798,051</td>
<td align="right">8,574</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">436,368,313</td>
<td align="right">7,060</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">403,591,303</td>
<td align="right">7,574</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">2,164,616,457</td>
<td align="right">42,742</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">22,610,964</td>
<td align="right">481</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,463,156,103</td>
<td align="right">61,294</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">592,759,242</td>
<td align="right">17,076</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">511,327,826</td>
<td align="right">15,360</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">291,799,003</td>
<td align="right">8,843</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">2,129,961,729</td>
<td align="right">70,281</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">214,351,839</td>
<td align="right">7,829</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">383,690,351</td>
<td align="right">14,613</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">354,364,207</td>
<td align="right">15,600</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,371,949,490</td>
<td align="right">61,715</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">298,871,939</td>
<td align="right">13,720</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,212,258,842</td>
<td align="right">59,909</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">7,871,459</td>
<td align="right">460</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">349,394,283</td>
<td align="right">23,692</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">113,565,659</td>
<td align="right">7,829</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">96,843,293</td>
<td align="right">7,069</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">530,790,353</td>
<td align="right">39,378</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">858,342,075</td>
<td align="right">88,006</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">497,168,302</td>
<td align="right">68,357</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">115,929,200</td>
<td align="right">16,484</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">752,314,515</td>
<td align="right">116,070</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">99,230,492</td>
<td align="right">16,446</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">89,969,789</td>
<td align="right">15,686</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">74,258,049</td>
<td align="right">16,445</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">146,776,008</td>
<td align="right">37,227</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">1,110,848,241</td>
<td align="right">354,090</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">5,899,206,925</td>
<td align="right">3,072,495</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,547,522,324</td>
<td align="right">930,882</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">65,151,714</td>
<td align="right">39,197</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">48,169</td>
<td align="right">36</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">64,693,805</td>
<td align="right">50,306</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">5,023</td>
<td align="right">4</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">3,381</td>
<td align="right">3</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">3,358</td>
<td align="right">3</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">3,452,100,002</td>
<td align="right">3,086,683</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">CALL_EX_PY</td>
<td align="right">23,993,613</td>
<td align="right">21,863</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,230,125,225</td>
<td align="right">1,762,055</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,621,603,026</td>
<td align="right">4,163,652</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,635,952,104</td>
<td align="right">4,420,098</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,831,515,174</td>
<td align="right">3,093,812</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">374,079,113</td>
<td align="right">707,330</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">14,517,650,880</td>
<td align="right">29,883,188</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">459,649,281</td>
<td align="right">993,551</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">4,778,543,069</td>
<td align="right">10,412,894</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">831,540,333</td>
<td align="right">1,928,999</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">675,584,652</td>
<td align="right">1,590,321</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">807,357,347</td>
<td align="right">1,925,800</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">6,839,489,284</td>
<td align="right">18,551,741</td>
<td align="right">-99.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,131,605,082</td>
<td align="right">3,160,339</td>
<td align="right">-99.7%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,098,645,449</td>
<td align="right">3,135,910</td>
<td align="right">-99.7%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">1,063,741,335</td>
<td align="right">3,136,668</td>
<td align="right">-99.7%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">18,019,112</td>
<td align="right">60,700</td>
<td align="right">-99.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">1,579,142</td>
<td align="right">6,084</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,803,414,797</td>
<td align="right">11,173,809</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">378,031,544</td>
<td align="right">1,545,801</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">11,546,416,368</td>
<td align="right">49,538,789</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">14,738,423</td>
<td align="right">65,284</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">5,775,116,584</td>
<td align="right">25,715,361</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">334,932,652</td>
<td align="right">1,551,989</td>
<td align="right">-99.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,744,656,566</td>
<td align="right">12,785,856</td>
<td align="right">-99.5%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">1,176,131,675</td>
<td align="right">6,273,776</td>
<td align="right">-99.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">885,174,986</td>
<td align="right">5,252,849</td>
<td align="right">-99.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">369,243,878</td>
<td align="right">2,249,875</td>
<td align="right">-99.4%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">447,318,623</td>
<td align="right">2,857,242</td>
<td align="right">-99.4%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">690,054,182</td>
<td align="right">4,640,140</td>
<td align="right">-99.3%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">116,031,409</td>
<td align="right">956,512</td>
<td align="right">-99.2%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">1,844,109,779</td>
<td align="right">15,433,009</td>
<td align="right">-99.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">346,021,085</td>
<td align="right">3,087,986</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">973,113,584</td>
<td align="right">9,350,893</td>
<td align="right">-99.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">620,302,508</td>
<td align="right">6,070,401</td>
<td align="right">-99.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">330,950,767</td>
<td align="right">3,426,659</td>
<td align="right">-99.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">42,063,847,703</td>
<td align="right">445,051,820</td>
<td align="right">-98.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">12,080,129,084</td>
<td align="right">131,921,478</td>
<td align="right">-98.9%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">2,387</td>
<td align="right">27</td>
<td align="right">-98.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">539,441,098</td>
<td align="right">6,158,585</td>
<td align="right">-98.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">539,770,801</td>
<td align="right">6,299,287</td>
<td align="right">-98.8%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,668,704,893</td>
<td align="right">20,193,563</td>
<td align="right">-98.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,719,514,248</td>
<td align="right">58,276,246</td>
<td align="right">-98.4%</td>
</tr>
<tr>
<td align="left">CALL_EX_NON_PY_GENERAL</td>
<td align="right">194,600,363</td>
<td align="right">3,094,044</td>
<td align="right">-98.4%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">18,349,935</td>
<td align="right">361,358</td>
<td align="right">-98.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">18,349,957</td>
<td align="right">361,360</td>
<td align="right">-98.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">18,011,870</td>
<td align="right">361,359</td>
<td align="right">-98.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">9,269,448,825</td>
<td align="right">188,650,666</td>
<td align="right">-98.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">16,541,290</td>
<td align="right">352,818</td>
<td align="right">-97.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">7,407,967,214</td>
<td align="right">163,305,760</td>
<td align="right">-97.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">248,710,163</td>
<td align="right">6,144,000</td>
<td align="right">-97.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">359,817,186</td>
<td align="right">9,320,423</td>
<td align="right">-97.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">6,575,435,391</td>
<td align="right">174,066,085</td>
<td align="right">-97.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">450,419,146</td>
<td align="right">12,360,074</td>
<td align="right">-97.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">4,836,519,968</td>
<td align="right">136,873,558</td>
<td align="right">-97.2%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">153,384,972</td>
<td align="right">4,654,011</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">7,784,456,600</td>
<td align="right">237,195,035</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">93,615,220</td>
<td align="right">3,072,931</td>
<td align="right">-96.7%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">325,656,862</td>
<td align="right">10,752,069</td>
<td align="right">-96.7%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">323,603,916</td>
<td align="right">10,752,069</td>
<td align="right">-96.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">3,776,689,199</td>
<td align="right">133,898,517</td>
<td align="right">-96.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">3,297,024,867</td>
<td align="right">117,693,189</td>
<td align="right">-96.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">4,109,591,037</td>
<td align="right">152,811,759</td>
<td align="right">-96.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">599,436,259</td>
<td align="right">22,643,099</td>
<td align="right">-96.2%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">78,206,409</td>
<td align="right">3,109,922</td>
<td align="right">-96.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">60,896,007</td>
<td align="right">3,072,929</td>
<td align="right">-95.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,111,558,969</td>
<td align="right">64,686,490</td>
<td align="right">-94.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,933,182,445</td>
<td align="right">116,542,922</td>
<td align="right">-94.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">262,434</td>
<td align="right">24,123</td>
<td align="right">-90.8%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">593,206,220</td>
<td align="right">116,536,320</td>
<td align="right">-80.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">224,139</td>
<td align="right">61,480</td>
<td align="right">-72.6%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">11,074,051</td>
<td align="right">3,072,003</td>
<td align="right">-72.3%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">416,122,862</td>
<td align="right">116,544,869</td>
<td align="right">-72.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">10,352,037</td>
<td align="right">3,072,005</td>
<td align="right">-70.3%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">11,798</td>
<td align="right">4,268</td>
<td align="right">-63.8%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">302,140,431</td>
<td align="right">116,536,320</td>
<td align="right">-61.4%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">31,218</td>
<td align="right">16,390</td>
<td align="right">-47.5%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">11,801</td>
<td align="right">6,229</td>
<td align="right">-47.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">6,534</td>
<td align="right">4,213</td>
<td align="right">-35.5%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">172,683,388</td>
<td align="right">116,536,320</td>
<td align="right">-32.5%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">4,511,091</td>
<td align="right">3,072,004</td>
<td align="right">-31.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_USTR_INT</td>
<td align="right">1,198,905,470</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,079,436,181</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">140,557,579</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,447,198</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">112,724,877</td>
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
<td align="left">NOT_TAKEN</td>
<td align="right">94,136,760</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">80,499,959</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">73,210,458</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">62,751,089</td>
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
<td align="left">SET_ADD</td>
<td align="right">40,815,984</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">35,435,823</td>
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
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">13,481,155</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">13,369,610</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">8,976,233</td>
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
<td align="right">5,529,560</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">1,714,200</td>
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
<td align="left">CLEANUP_THROW</td>
<td align="right">91,596</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">68,063</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">49,580</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">14,745</td>
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
<td align="left">INSTRUMENTED_JUMP_BACKWARD</td>
<td align="right">120</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SETUP_ANNOTATIONS</td>
<td align="right">117</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">17</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right"></td>
<td align="right">1,743,262</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TRACE_RECORD</td>
<td align="right"></td>
<td align="right">54,600</td>
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
<td align="right">59,195,282</td>
<td align="right">0.3%</td>
<td align="right">62</td>
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
<td align="right">2,432,680,954</td>
<td align="right">12.5%</td>
<td align="right">12,687</td>
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
<td align="right">16,962,659,406</td>
<td align="right">87.2%</td>
<td align="right">175,251,713</td>
<td align="right">100.0%</td>
<td align="right">-99.0%</td>
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
<td align="right">410,127</td>
<td align="right">26.6%</td>
<td align="right">694</td>
<td align="right">19.2%</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,133,278</td>
<td align="right">73.4%</td>
<td align="right">2,923</td>
<td align="right">80.8%</td>
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
<td align="right">29,916</td>
<td align="right">7.3%</td>
<td align="right">1</td>
<td align="right">0.1%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">45,385</td>
<td align="right">11.1%</td>
<td align="right">2</td>
<td align="right">0.3%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">16,461</td>
<td align="right">4.0%</td>
<td align="right">2</td>
<td align="right">0.3%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">1,230</td>
<td align="right">0.3%</td>
<td align="right">3</td>
<td align="right">0.4%</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">23,657</td>
<td align="right">5.8%</td>
<td align="right">204</td>
<td align="right">29.4%</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">7,487</td>
<td align="right">1.8%</td>
<td align="right">480</td>
<td align="right">69.2%</td>
<td align="right">-93.6%</td>
</tr>
<tr>
<td align="left">subscr ordereddict</td>
<td align="right">22</td>
<td align="right">0.0%</td>
<td align="right">2</td>
<td align="right">0.3%</td>
<td align="right">-90.9%</td>
</tr>
<tr>
<td align="left">subscr array</td>
<td align="right">63,958</td>
<td align="right">15.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr counter</td>
<td align="right">53,846</td>
<td align="right">13.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">39,448</td>
<td align="right">9.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">21,977</td>
<td align="right">5.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">17,159</td>
<td align="right">4.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">11,629</td>
<td align="right">2.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">11,251</td>
<td align="right">2.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr bytes</td>
<td align="right">11,160</td>
<td align="right">2.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">9,585</td>
<td align="right">2.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">xor int</td>
<td align="right">9,100</td>
<td align="right">2.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">7,956</td>
<td align="right">1.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">7,613</td>
<td align="right">1.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">5,836</td>
<td align="right">1.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">4,630</td>
<td align="right">1.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">3,628</td>
<td align="right">0.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr range</td>
<td align="right">1,602</td>
<td align="right">0.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">1,558</td>
<td align="right">0.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">1,286</td>
<td align="right">0.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">821</td>
<td align="right">0.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">598</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">402</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr mappingproxy</td>
<td align="right">220</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr other slice</td>
<td align="right">186</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">140</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr structtime</td>
<td align="right">140</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">or different types</td>
<td align="right">70</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">subscr deque</td>
<td align="right">68</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">code complex parameters</td>
<td align="right">60</td>
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
<td align="right">543,798,051</td>
<td align="right">100.0%</td>
<td align="right">8,574</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">198,111,730</td>
<td align="right">1.6%</td>
<td align="right">14</td>
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
<td align="right">194,436,575</td>
<td align="right">1.5%</td>
<td align="right">31,829</td>
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
<td align="right">12,581,655,861</td>
<td align="right">98.4%</td>
<td align="right">171,316,990</td>
<td align="right">100.0%</td>
<td align="right">-98.6%</td>
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
<td align="right">147</td>
<td align="right">0.0%</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">-99.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,899,147</td>
<td align="right">100.0%</td>
<td align="right">29,664</td>
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
<td align="left">out of versions</td>
<td align="right">147</td>
<td align="right">100.0%</td>
<td align="right">1</td>
<td align="right">100.0%</td>
<td align="right">-99.3%</td>
</tr>
<tr>
<td align="left">init not simple</td>
<td align="right">731</td>
<td align="right">497.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">266</td>
<td align="right">181.0%</td>
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
<td align="right">20,142</td>
<td align="right">63.1%</td>
<td align="right">900</td>
<td align="right">12.6%</td>
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
<td align="right">23,451</td>
<td align="right">73.4%</td>
<td align="right">4,042</td>
<td align="right">56.7%</td>
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
<td align="right">8,492</td>
<td align="right">100.0%</td>
<td align="right">3,087</td>
<td align="right">100.0%</td>
<td align="right">-63.6%</td>
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
<td align="right">537,932</td>
<td align="right">96.6%</td>
<td align="right">2,123</td>
<td align="right">49.7%</td>
<td align="right">-99.6%</td>
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
<td align="right">18,875</td>
<td align="right">100.0%</td>
<td align="right">2,145</td>
<td align="right">100.0%</td>
<td align="right">-88.6%</td>
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
<td align="right">1,596,547</td>
<td align="right">0.0%</td>
<td align="right">1</td>
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
<td align="right">530,635,520</td>
<td align="right">9.1%</td>
<td align="right">23,326</td>
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
<td align="right">5,322,633,536</td>
<td align="right">90.9%</td>
<td align="right">120,787,002</td>
<td align="right">100.0%</td>
<td align="right">-97.7%</td>
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
<td align="right">133,097</td>
<td align="right">72.0%</td>
<td align="right">1,005</td>
<td align="right">6.3%</td>
<td align="right">-99.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">51,705</td>
<td align="right">28.0%</td>
<td align="right">15,047</td>
<td align="right">93.7%</td>
<td align="right">-70.9%</td>
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
<td align="right">42,668</td>
<td align="right">32.1%</td>
<td align="right">20</td>
<td align="right">2.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">1,055</td>
<td align="right">0.8%</td>
<td align="right">1</td>
<td align="right">0.1%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">629</td>
<td align="right">0.5%</td>
<td align="right">2</td>
<td align="right">0.2%</td>
<td align="right">-99.7%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">28,238</td>
<td align="right">21.2%</td>
<td align="right">982</td>
<td align="right">97.7%</td>
<td align="right">-96.5%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">25,861</td>
<td align="right">19.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">14,387</td>
<td align="right">10.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">5,817</td>
<td align="right">4.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">5,535</td>
<td align="right">4.2%</td>
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
<td align="right">2.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">554</td>
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
<td align="right">2,197,880,930</td>
<td align="right">90.4%</td>
<td align="right">81</td>
<td align="right">6.4%</td>
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
<td align="right">232,154,230</td>
<td align="right">9.5%</td>
<td align="right">1,166</td>
<td align="right">92.0%</td>
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
<td align="right">1,399,190</td>
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
<td align="right">28,280</td>
<td align="right">41.7%</td>
<td align="right">4</td>
<td align="right">19.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">39,475</td>
<td align="right">58.3%</td>
<td align="right">17</td>
<td align="right">81.0%</td>
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
<td align="left">list</td>
<td align="right">14,657</td>
<td align="right">37.1%</td>
<td align="right">1</td>
<td align="right">5.9%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">5,520</td>
<td align="right">14.0%</td>
<td align="right">1</td>
<td align="right">5.9%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">6,099</td>
<td align="right">15.5%</td>
<td align="right">2</td>
<td align="right">11.8%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">13,199</td>
<td align="right">33.4%</td>
<td align="right">13</td>
<td align="right">76.5%</td>
<td align="right">-99.9%</td>
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
<td align="right">163,563,728</td>
<td align="right">3.1%</td>
<td align="right">7</td>
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
<td align="right">1,504,901,085</td>
<td align="right">28.5%</td>
<td align="right">4,099</td>
<td align="right">0.1%</td>
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
<td align="right">3,603,103,760</td>
<td align="right">68.3%</td>
<td align="right">7,932,402</td>
<td align="right">99.9%</td>
<td align="right">-99.8%</td>
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
<td align="right">3,091,715</td>
<td align="right">93.2%</td>
<td align="right">2,620</td>
<td align="right">78.8%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">226,623</td>
<td align="right">6.8%</td>
<td align="right">703</td>
<td align="right">21.2%</td>
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
<td align="left">dict items</td>
<td align="right">45,982</td>
<td align="right">20.3%</td>
<td align="right">1</td>
<td align="right">0.1%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">41,828</td>
<td align="right">18.5%</td>
<td align="right">3</td>
<td align="right">0.4%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">7,652</td>
<td align="right">3.4%</td>
<td align="right">1</td>
<td align="right">0.1%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">17,503</td>
<td align="right">7.7%</td>
<td align="right">5</td>
<td align="right">0.7%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">5,783</td>
<td align="right">2.6%</td>
<td align="right">5</td>
<td align="right">0.7%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">1,594</td>
<td align="right">0.7%</td>
<td align="right">5</td>
<td align="right">0.7%</td>
<td align="right">-99.7%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">5,303</td>
<td align="right">2.3%</td>
<td align="right">683</td>
<td align="right">97.2%</td>
<td align="right">-87.1%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">80,759</td>
<td align="right">35.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">9,093</td>
<td align="right">4.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">6,285</td>
<td align="right">2.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">2,235</td>
<td align="right">1.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">1,543</td>
<td align="right">0.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">580</td>
<td align="right">0.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">309</td>
<td align="right">0.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">108</td>
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
<td align="right">101,601,595</td>
<td align="right">101,601,595 / 0 !!</td>
<td align="right">1</td>
<td align="right">1 / 0 !!</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">34,933,519</td>
<td align="right">34,933,519 / 0 !!</td>
<td align="right">7</td>
<td align="right">7 / 0 !!</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">5,457,822</td>
<td align="right">5,457,822 / 0 !!</td>
<td align="right">11</td>
<td align="right">11 / 0 !!</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">2,710,286</td>
<td align="right">2,710,286 / 0 !!</td>
<td align="right">17</td>
<td align="right">17 / 0 !!</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">318,437,243</td>
<td align="right">318,437,243 / 0 !!</td>
<td align="right">7,888</td>
<td align="right">7,888 / 0 !!</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">126,656,029</td>
<td align="right">126,656,029 / 0 !!</td>
<td align="right">16,232</td>
<td align="right">16,232 / 0 !!</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">173,352,588</td>
<td align="right">173,352,588 / 0 !!</td>
<td align="right">3,111,754</td>
<td align="right">3,111,754 / 0 !!</td>
<td align="right">-98.2%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">322,600,903</td>
<td align="right">322,600,903 / 0 !!</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">12,120,024</td>
<td align="right">12,120,024 / 0 !!</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">775,440</td>
<td align="right">775,440 / 0 !!</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
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
<td align="right">862,905,356</td>
<td align="right">5.0%</td>
<td align="right">62</td>
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
<td align="right">856,838,274</td>
<td align="right">4.9%</td>
<td align="right">49,189</td>
<td align="right">0.1%</td>
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
<td align="right">15,642,174,326</td>
<td align="right">90.1%</td>
<td align="right">90,780,757</td>
<td align="right">99.9%</td>
<td align="right">-99.4%</td>
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
<td align="right">16,359,486</td>
<td align="right">98.4%</td>
<td align="right">37,583</td>
<td align="right">96.9%</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">259,760</td>
<td align="right">1.6%</td>
<td align="right">1,194</td>
<td align="right">3.1%</td>
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
<td align="left">overriding descriptor</td>
<td align="right">30,515</td>
<td align="right">11.7%</td>
<td align="right">4</td>
<td align="right">0.3%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">42,450</td>
<td align="right">16.3%</td>
<td align="right">7</td>
<td align="right">0.6%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">28,848</td>
<td align="right">11.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">12,448</td>
<td align="right">4.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">8,812</td>
<td align="right">3.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">3,878</td>
<td align="right">1.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">3,196</td>
<td align="right">1.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">1,424</td>
<td align="right">0.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">877</td>
<td align="right">0.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">623</td>
<td align="right">0.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">502</td>
<td align="right">0.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">487</td>
<td align="right">0.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">472</td>
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
<td align="left">wrong number arguments</td>
<td align="right">120</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">63</td>
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
<td align="right">14,612,749</td>
<td align="right">0.1%</td>
<td align="right">33,284</td>
<td align="right">0.0%</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,980</td>
<td align="right">0.0%</td>
<td align="right">14</td>
<td align="right">0.0%</td>
<td align="right">-99.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">10,949,027,767</td>
<td align="right">99.9%</td>
<td align="right">171,355,186</td>
<td align="right">100.0%</td>
<td align="right">-98.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">52,554</td>
<td align="right">0.0%</td>
<td align="right">8,314</td>
<td align="right">0.0%</td>
<td align="right">-84.2%</td>
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
<td align="right">126,558</td>
<td align="right">100.0%</td>
<td align="right">32,002</td>
<td align="right">100.0%</td>
<td align="right">-74.7%</td>
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
<td align="right">70,422,180</td>
<td align="right">100.0%</td>
<td align="right">3,072,018</td>
<td align="right">100.0%</td>
<td align="right">-95.6%</td>
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
<td align="right">17</td>
<td align="right">0.0%</td>
<td align="right">-86.1%</td>
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
<td align="right">2,265</td>
<td align="right">100.0%</td>
<td align="right">10</td>
<td align="right">100.0%</td>
<td align="right">-99.6%</td>
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
<td align="right">593,204,684</td>
<td align="right">82.2%</td>
<td align="right">116,536,320</td>
<td align="right">100.0%</td>
<td align="right">-80.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">128,430,319</td>
<td align="right">17.8%</td>
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
<td align="right">1,536</td>
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
<td align="right">362</td>
<td align="right">2.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">16,557</td>
<td align="right">97.9%</td>
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
<td align="left">async generator send</td>
<td align="right">12,220</td>
<td align="right">73.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">3,034</td>
<td align="right">18.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">1,043</td>
<td align="right">6.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">260</td>
<td align="right">1.6%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">115,130,193</td>
<td align="right">4.1%</td>
<td align="right">1</td>
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
<td align="right">64,627,245</td>
<td align="right">2.3%</td>
<td align="right">35,368</td>
<td align="right">0.1%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,609,574,961</td>
<td align="right">93.6%</td>
<td align="right">64,686,499</td>
<td align="right">99.9%</td>
<td align="right">-97.5%</td>
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
<td align="right">2,211,384</td>
<td align="right">98.8%</td>
<td align="right">12,037</td>
<td align="right">80.6%</td>
<td align="right">-99.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">26,724</td>
<td align="right">1.2%</td>
<td align="right">2,901</td>
<td align="right">19.4%</td>
<td align="right">-89.1%</td>
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
<td align="right">11,089</td>
<td align="right">41.5%</td>
<td align="right">1,921</td>
<td align="right">66.2%</td>
<td align="right">-82.7%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1,870</td>
<td align="right">7.0%</td>
<td align="right">980</td>
<td align="right">33.8%</td>
<td align="right">-47.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">118,304</td>
<td align="right">442.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">5,172</td>
<td align="right">19.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">3,376</td>
<td align="right">12.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">2,139</td>
<td align="right">8.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">974</td>
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
<td align="right">379</td>
<td align="right">1.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">222</td>
<td align="right">0.8%</td>
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
<td align="right">112,724,877</td>
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
<td align="right">691,382,501</td>
<td align="right">42.0%</td>
<td align="right">1,089</td>
<td align="right">6.5%</td>
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
<td align="right">953,007,860</td>
<td align="right">58.0%</td>
<td align="right">14,618</td>
<td align="right">87.1%</td>
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
<td align="right">2,220</td>
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
<td align="right">90,483</td>
<td align="right">96.8%</td>
<td align="right">7</td>
<td align="right">0.7%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,958</td>
<td align="right">3.2%</td>
<td align="right">1,063</td>
<td align="right">99.3%</td>
<td align="right">-64.1%</td>
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
<td align="right">40,613</td>
<td align="right">44.9%</td>
<td align="right">3</td>
<td align="right">42.9%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">9,012</td>
<td align="right">10.0%</td>
<td align="right">4</td>
<td align="right">57.1%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">26,138</td>
<td align="right">28.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">9,605</td>
<td align="right">10.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">2,670</td>
<td align="right">3.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">1,511</td>
<td align="right">1.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">889</td>
<td align="right">1.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">array slice</td>
<td align="right">45</td>
<td align="right">0.0%</td>
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
<td align="right">104,848,206</td>
<td align="right">1.7%</td>
<td align="right">12</td>
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
<td align="right">459,333,585</td>
<td align="right">7.3%</td>
<td align="right">972,867</td>
<td align="right">6.5%</td>
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
<td align="right">5,738,110,598</td>
<td align="right">91.0%</td>
<td align="right">13,930,656</td>
<td align="right">93.3%</td>
<td align="right">-99.8%</td>
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
<td align="right">2,026,506</td>
<td align="right">88.4%</td>
<td align="right">17,501</td>
<td align="right">84.6%</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">266,065</td>
<td align="right">11.6%</td>
<td align="right">3,183</td>
<td align="right">15.4%</td>
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
<td align="left">other</td>
<td align="right">28,121</td>
<td align="right">10.6%</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">9,490</td>
<td align="right">3.6%</td>
<td align="right">220</td>
<td align="right">6.9%</td>
<td align="right">-97.7%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">66,567</td>
<td align="right">25.0%</td>
<td align="right">1,960</td>
<td align="right">61.6%</td>
<td align="right">-97.1%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">4,030</td>
<td align="right">1.5%</td>
<td align="right">1,002</td>
<td align="right">31.5%</td>
<td align="right">-75.1%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">140,894</td>
<td align="right">53.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">8,072</td>
<td align="right">3.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">4,729</td>
<td align="right">1.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">3,919</td>
<td align="right">1.5%</td>
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
<td align="right">1,273,697,099</td>
<td align="right">99.9%</td>
<td align="right">1,933,374</td>
<td align="right">99.7%</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,568,947</td>
<td align="right">0.1%</td>
<td align="right">3,158</td>
<td align="right">0.2%</td>
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
<td align="right">451</td>
<td align="right">4.4%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">9,804</td>
<td align="right">95.6%</td>
<td align="right">2,926</td>
<td align="right">100.0%</td>
<td align="right">-70.2%</td>
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
<td align="right">312</td>
<td align="right">69.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">88</td>
<td align="right">19.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">51</td>
<td align="right">11.3%</td>
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
<td align="right">1,507,556,865</td>
<td align="right">0.6%</td>
<td align="right">9,373</td>
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
<td align="right">8,675,571,417</td>
<td align="right">3.6%</td>
<td align="right">4,486,169</td>
<td align="right">0.2%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">90,824,411,482</td>
<td align="right">38.2%</td>
<td align="right">1,124,456,351</td>
<td align="right">37.7%</td>
<td align="right">-98.8%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">137,063,660,560</td>
<td align="right">57.6%</td>
<td align="right">1,851,761,246</td>
<td align="right">62.1%</td>
<td align="right">-98.6%</td>
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
<td align="right">1,504,901,085</td>
<td align="right">19.4%</td>
<td align="right">4,099</td>
<td align="right">0.3%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,432,680,954</td>
<td align="right">31.3%</td>
<td align="right">12,687</td>
<td align="right">1.1%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">543,798,051</td>
<td align="right">7.0%</td>
<td align="right">8,574</td>
<td align="right">0.7%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">530,635,520</td>
<td align="right">6.8%</td>
<td align="right">23,326</td>
<td align="right">2.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">856,838,274</td>
<td align="right">11.0%</td>
<td align="right">49,189</td>
<td align="right">4.2%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">194,436,575</td>
<td align="right">2.5%</td>
<td align="right">31,829</td>
<td align="right">2.7%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">459,333,585</td>
<td align="right">5.9%</td>
<td align="right">972,867</td>
<td align="right">82.2%</td>
<td align="right">-99.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">691,382,501</td>
<td align="right">8.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">232,154,230</td>
<td align="right">3.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,430,319</td>
<td align="right">1.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">35,368</td>
<td align="right">3.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">33,284</td>
<td align="right">2.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">4,042</td>
<td align="right">0.3%</td>
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
<td align="left">FOR_ITER_LIST</td>
<td align="right">81,897,720</td>
<td align="right">5.4%</td>
<td align="right">5</td>
<td align="right">0.1%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">368,474,276</td>
<td align="right">24.4%</td>
<td align="right">39</td>
<td align="right">0.4%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">268,547,734</td>
<td align="right">17.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">94,889,423</td>
<td align="right">6.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">90,449,880</td>
<td align="right">6.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">89,786,932</td>
<td align="right">6.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">81,539,232</td>
<td align="right">5.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">79,646,138</td>
<td align="right">5.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">49,483,584</td>
<td align="right">3.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">49,222,298</td>
<td align="right">3.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">8,276</td>
<td align="right">88.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_EX_NON_PY_GENERAL</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">460</td>
<td align="right">4.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_EX_PY</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">440</td>
<td align="right">4.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">60</td>
<td align="right">0.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">38</td>
<td align="right">0.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">20</td>
<td align="right">0.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">6</td>
<td align="right">0.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">4</td>
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
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">141,112,775</td>
<td align="right">1.8%</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">305,354,966</td>
<td align="right">3.9%</td>
<td align="right">29</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">4,273,304</td>
<td align="right">0.1%</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">565,799,272</td>
<td align="right">7.2%</td>
<td align="right">16,592</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">3,381</td>
<td align="right">0.0%</td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">71,351,413</td>
<td align="right">0.9%</td>
<td align="right">360,957</td>
<td align="right">0.1%</td>
<td align="right">-99.5%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">1,848,581,448</td>
<td align="right">23.5%</td>
<td align="right">15,434,299</td>
<td align="right">5.5%</td>
<td align="right">-99.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">1,848,581,448</td>
<td align="right">23.5%</td>
<td align="right">15,434,299</td>
<td align="right">5.5%</td>
<td align="right">-99.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">458,817,197</td>
<td align="right">5.8%</td>
<td align="right">4,616,082</td>
<td align="right">1.6%</td>
<td align="right">-99.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,282,782,176</td>
<td align="right">16.3%</td>
<td align="right">15,417,707</td>
<td align="right">5.5%</td>
<td align="right">-98.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,278,505,491</td>
<td align="right">16.3%</td>
<td align="right">15,417,703</td>
<td align="right">5.5%</td>
<td align="right">-98.8%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,631,317,504</td>
<td align="right">84.4%</td>
<td align="right">174,066,119</td>
<td align="right">62.2%</td>
<td align="right">-97.4%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,004,826,126</td>
<td align="right">76.5%</td>
<td align="right">264,432,720</td>
<td align="right">94.5%</td>
<td align="right">-95.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">11,309</td>
<td align="right">0.0%</td>
<td align="right">2,024</td>
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
<td align="right">4,041,763</td>
<td align="right">2.1%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">307,309</td>
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
<td align="left">Method cache collisions</td>
<td align="right">62,266,108</td>
<td align="right"></td>
<td align="right">33,614</td>
<td align="right"></td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">6,652,270</td>
<td align="right">0.0%</td>
<td align="right">3,682</td>
<td align="right">0.0%</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">57,089,905</td>
<td align="right"></td>
<td align="right">37,815</td>
<td align="right"></td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">5,981,265</td>
<td align="right"></td>
<td align="right">7,790</td>
<td align="right"></td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">2,906,980,701</td>
<td align="right"></td>
<td align="right">14,686,109</td>
<td align="right"></td>
<td align="right">-99.5%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">13,812,454,147</td>
<td align="right">70.2%</td>
<td align="right">99,731,179</td>
<td align="right">26.5%</td>
<td align="right">-99.3%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">13,812,628,521</td>
<td align="right"></td>
<td align="right">99,738,598</td>
<td align="right"></td>
<td align="right">-99.3%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">23,371,912,545</td>
<td align="right">21.0%</td>
<td align="right">239,405,132</td>
<td align="right">13.5%</td>
<td align="right">-99.0%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">55,877,429,724</td>
<td align="right">50.1%</td>
<td align="right">760,488,112</td>
<td align="right">42.9%</td>
<td align="right">-98.6%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">2,315,620,882</td>
<td align="right"></td>
<td align="right">32,432,605</td>
<td align="right"></td>
<td align="right">-98.6%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">25,587,849,480</td>
<td align="right">26.4%</td>
<td align="right">362,718,382</td>
<td align="right">21.1%</td>
<td align="right">-98.6%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">42,132,892,512</td>
<td align="right">43.5%</td>
<td align="right">626,286,721</td>
<td align="right">36.4%</td>
<td align="right">-98.5%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">30,137,671,595</td>
<td align="right">27.0%</td>
<td align="right">521,301,345</td>
<td align="right">29.4%</td>
<td align="right">-98.3%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">23,647,497,325</td>
<td align="right">24.4%</td>
<td align="right">449,796,041</td>
<td align="right">26.2%</td>
<td align="right">-98.1%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">71,682,146</td>
<td align="right">0.4%</td>
<td align="right">1,864,180</td>
<td align="right">0.5%</td>
<td align="right">-97.4%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">6,466,381,917</td>
<td align="right"></td>
<td align="right">280,979,943</td>
<td align="right"></td>
<td align="right">-95.7%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">5,866,474,577</td>
<td align="right">29.8%</td>
<td align="right">276,542,134</td>
<td align="right">73.5%</td>
<td align="right">-95.3%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">5,788,140,161</td>
<td align="right">29.4%</td>
<td align="right">274,674,272</td>
<td align="right">73.0%</td>
<td align="right">-95.3%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">5,572,629,584</td>
<td align="right">5.7%</td>
<td align="right">280,926,779</td>
<td align="right">16.3%</td>
<td align="right">-95.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">193,069,542</td>
<td align="right"></td>
<td align="right">18,455,779</td>
<td align="right"></td>
<td align="right">-90.4%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">2,046,695,006</td>
<td align="right">1.8%</td>
<td align="right">250,048,697</td>
<td align="right">14.1%</td>
<td align="right">-87.8%</td>
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
<td align="right">415,676</td>
<td align="right">103,603,608</td>
<td align="right">6,627,366,174</td>
<td align="right">717,286,249</td>
<td align="right">375,535,561</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">0</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">15,998</td>
<td align="right">8,734,228</td>
<td align="right">11,466,222,924</td>
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
<td align="right">2,436</td>
<td align="right">682</td>
<td align="right">-72.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2026-01-11
