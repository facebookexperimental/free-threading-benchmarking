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
<td align="right">5,865,290,284</td>
<td align="right">6,782,341</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">112,724,874</td>
<td align="right">1,232,454</td>
<td align="right">-98.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">441,384,653</td>
<td align="right">13,359,844</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">62,357,839</td>
<td align="right">2,270,991</td>
<td align="right">-96.4%</td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">100,136,760</td>
<td align="right">6,000,000</td>
<td align="right">-94.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,505,447,733</td>
<td align="right">214,677,448</td>
<td align="right">-85.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">691,583,324</td>
<td align="right">103,565,545</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,753,875,536</td>
<td align="right">272,631,273</td>
<td align="right">-84.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">569,317,851</td>
<td align="right">97,095,353</td>
<td align="right">-82.9%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,220,193,573</td>
<td align="right">210,644,700</td>
<td align="right">-82.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">2,714,118,481</td>
<td align="right">469,574,467</td>
<td align="right">-82.7%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">2,123,312,040</td>
<td align="right">403,337,960</td>
<td align="right">-81.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">353,326,715</td>
<td align="right">76,416,367</td>
<td align="right">-78.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">1,256,721,687</td>
<td align="right">279,455,973</td>
<td align="right">-77.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">528,751,149</td>
<td align="right">122,583,227</td>
<td align="right">-76.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">158,452,009</td>
<td align="right">37,396,753</td>
<td align="right">-76.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,723,984,128</td>
<td align="right">903,794,839</td>
<td align="right">-75.7%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,545,805,436</td>
<td align="right">385,951,206</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,831,599,027</td>
<td align="right">481,563,902</td>
<td align="right">-73.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,458,368,468</td>
<td align="right">669,665,021</td>
<td align="right">-72.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">942,782,215</td>
<td align="right">258,414,093</td>
<td align="right">-72.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">678,193,389</td>
<td align="right">186,289,481</td>
<td align="right">-72.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">510,992,075</td>
<td align="right">146,023,177</td>
<td align="right">-71.4%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">684,887,901</td>
<td align="right">197,613,173</td>
<td align="right">-71.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">199,310,971</td>
<td align="right">59,069,217</td>
<td align="right">-70.4%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">375,081,102</td>
<td align="right">111,456,045</td>
<td align="right">-70.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">540,273,115</td>
<td align="right">172,325,614</td>
<td align="right">-68.1%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">57,164,879</td>
<td align="right">18,639,632</td>
<td align="right">-67.4%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">7,782,544,105</td>
<td align="right">2,544,343,242</td>
<td align="right">-67.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">2,157,256,116</td>
<td align="right">721,000,446</td>
<td align="right">-66.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,504,727,861</td>
<td align="right">1,174,703,103</td>
<td align="right">-66.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,129,481,385</td>
<td align="right">379,226,124</td>
<td align="right">-66.4%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">158,352,273</td>
<td align="right">55,173,450</td>
<td align="right">-65.2%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">94,136,760</td>
<td align="right">154,923,361</td>
<td align="right">64.6%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">543,088,951</td>
<td align="right">199,228,538</td>
<td align="right">-63.3%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">112,878,660</td>
<td align="right">42,462,349</td>
<td align="right">-62.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,674,647,467</td>
<td align="right">1,007,747,450</td>
<td align="right">-62.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,937,038,191</td>
<td align="right">744,879,761</td>
<td align="right">-61.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">381,096,473</td>
<td align="right">149,726,456</td>
<td align="right">-60.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">10,611,601,161</td>
<td align="right">4,178,650,998</td>
<td align="right">-60.6%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">67,374,396</td>
<td align="right">26,549,528</td>
<td align="right">-60.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">1,153,536,302</td>
<td align="right">455,068,026</td>
<td align="right">-60.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">440,902,328</td>
<td align="right">175,836,742</td>
<td align="right">-60.1%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">263,839,451</td>
<td align="right">105,505,548</td>
<td align="right">-60.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">22,610,651</td>
<td align="right">9,211,734</td>
<td align="right">-59.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,737,905,267</td>
<td align="right">1,129,061,771</td>
<td align="right">-58.8%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">751,919,257</td>
<td align="right">311,077,255</td>
<td align="right">-58.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">14,488,508,457</td>
<td align="right">6,021,652,989</td>
<td align="right">-58.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">539,548,642</td>
<td align="right">226,155,645</td>
<td align="right">-58.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">3,293,443,751</td>
<td align="right">1,385,645,085</td>
<td align="right">-57.9%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,156,329</td>
<td align="right">2,600,969</td>
<td align="right">-57.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">888,655,604</td>
<td align="right">381,201,816</td>
<td align="right">-57.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,079,502,741</td>
<td align="right">468,512,477</td>
<td align="right">-56.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">12,141,427,471</td>
<td align="right">5,318,683,375</td>
<td align="right">-56.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">6,842,524,224</td>
<td align="right">3,080,312,289</td>
<td align="right">-55.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">7,879,440</td>
<td align="right">3,593,514</td>
<td align="right">-54.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">93,694,036</td>
<td align="right">44,743,813</td>
<td align="right">-52.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">831,876,317</td>
<td align="right">398,625,516</td>
<td align="right">-52.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,416,066,927</td>
<td align="right">1,166,088,286</td>
<td align="right">-51.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">321,870,716</td>
<td align="right">156,187,033</td>
<td align="right">-51.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">92,047,363</td>
<td align="right">45,328,385</td>
<td align="right">-50.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">403,666,081</td>
<td align="right">203,561,244</td>
<td align="right">-49.6%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,093,196,590</td>
<td align="right">555,354,358</td>
<td align="right">-49.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">9,292,252,329</td>
<td align="right">4,783,481,545</td>
<td align="right">-48.5%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">99,846,008</td>
<td align="right">51,449,674</td>
<td align="right">-48.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">330,547,578</td>
<td align="right">173,406,963</td>
<td align="right">-47.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">303,471,870</td>
<td align="right">161,458,270</td>
<td align="right">-46.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,621,031,190</td>
<td align="right">1,397,397,136</td>
<td align="right">-46.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">13,158,809</td>
<td align="right">7,148,338</td>
<td align="right">-45.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">89,810,539</td>
<td align="right">49,688,965</td>
<td align="right">-44.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">39,572,678,675</td>
<td align="right">21,902,325,444</td>
<td align="right">-44.7%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">975,101,954</td>
<td align="right">550,297,153</td>
<td align="right">-43.6%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,232,183,250</td>
<td align="right">697,404,499</td>
<td align="right">-43.4%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">594,020,788</td>
<td align="right">339,334,184</td>
<td align="right">-42.9%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">117,814,436</td>
<td align="right">67,835,312</td>
<td align="right">-42.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,870,502,570</td>
<td align="right">1,660,509,204</td>
<td align="right">-42.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">148,285,828</td>
<td align="right">85,981,576</td>
<td align="right">-42.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">195,700,515</td>
<td align="right">114,764,832</td>
<td align="right">-41.4%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">1,053,839,616</td>
<td align="right">618,660,675</td>
<td align="right">-41.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">219,397,637</td>
<td align="right">129,531,973</td>
<td align="right">-41.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">297,151,762</td>
<td align="right">176,800,253</td>
<td align="right">-40.5%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,667,253,908</td>
<td align="right">1,005,357,475</td>
<td align="right">-39.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">806,746,670</td>
<td align="right">490,640,416</td>
<td align="right">-39.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">230,299,197</td>
<td align="right">140,676,757</td>
<td align="right">-38.9%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,369,669,750</td>
<td align="right">842,464,626</td>
<td align="right">-38.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">3,769,070,477</td>
<td align="right">2,366,520,494</td>
<td align="right">-37.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">4,861,987,501</td>
<td align="right">3,098,083,857</td>
<td align="right">-36.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">440,424,881</td>
<td align="right">284,653,678</td>
<td align="right">-35.4%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">116,432,417</td>
<td align="right">75,260,205</td>
<td align="right">-35.4%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">123,911,725</td>
<td align="right">81,942,609</td>
<td align="right">-33.9%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">62,994,451</td>
<td align="right">41,704,231</td>
<td align="right">-33.8%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">61,319,876</td>
<td align="right">40,796,667</td>
<td align="right">-33.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">5,843,150,450</td>
<td align="right">3,895,157,283</td>
<td align="right">-33.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">851,208,287</td>
<td align="right">569,318,138</td>
<td align="right">-33.1%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">144,891,111</td>
<td align="right">97,156,060</td>
<td align="right">-32.9%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">214,351,148</td>
<td align="right">143,958,819</td>
<td align="right">-32.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">251,068,663</td>
<td align="right">172,298,762</td>
<td align="right">-31.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">66,660,073</td>
<td align="right">46,306,328</td>
<td align="right">-30.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">509,895,927</td>
<td align="right">356,595,052</td>
<td align="right">-30.1%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">437,760,792</td>
<td align="right">312,725,368</td>
<td align="right">-28.6%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">189,121,440</td>
<td align="right">136,167,486</td>
<td align="right">-28.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">446,351,990</td>
<td align="right">324,466,600</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">350,534,808</td>
<td align="right">262,820,076</td>
<td align="right">-25.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">4,135,593,944</td>
<td align="right">3,167,217,338</td>
<td align="right">-23.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">1,579,459</td>
<td align="right">1,214,931</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">368,273,894</td>
<td align="right">291,904,401</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">7,480,479,393</td>
<td align="right">5,978,862,704</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">441,115,279</td>
<td align="right">355,331,680</td>
<td align="right">-19.4%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,656,062,609</td>
<td align="right">2,960,962,705</td>
<td align="right">-19.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">353,963,576</td>
<td align="right">288,362,492</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">3,454,135,070</td>
<td align="right">2,845,404,574</td>
<td align="right">-17.6%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">344,764,768</td>
<td align="right">284,755,696</td>
<td align="right">-17.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">612,546,066</td>
<td align="right">508,201,005</td>
<td align="right">-17.0%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">1,175,392,946</td>
<td align="right">979,734,652</td>
<td align="right">-16.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,114,961,258</td>
<td align="right">942,351,700</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">17,299,586</td>
<td align="right">14,624,910</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">291,589,640</td>
<td align="right">247,722,616</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">589,124,126</td>
<td align="right">506,029,571</td>
<td align="right">-14.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">6,641,724,384</td>
<td align="right">5,719,766,853</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">116,347,081</td>
<td align="right">101,074,140</td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">80,501,462</td>
<td align="right">69,964,442</td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">125,503,470</td>
<td align="right">109,898,349</td>
<td align="right">-12.4%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">417,069,497</td>
<td align="right">367,563,959</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">64,702,460</td>
<td align="right">58,740,144</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">78,137,493</td>
<td align="right">71,299,417</td>
<td align="right">-8.8%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">63,661,393</td>
<td align="right">58,148,262</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,758,776</td>
<td align="right">3,446,516</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,600,029,689</td>
<td align="right">1,468,954,583</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">152,374,025</td>
<td align="right">142,206,505</td>
<td align="right">-6.7%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,160,178</td>
<td align="right">5,794,148</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">10,291,678</td>
<td align="right">9,686,362</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">74,097,285</td>
<td align="right">70,446,660</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">20,799,950</td>
<td align="right">19,831,440</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">21,142,196</td>
<td align="right">20,173,686</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">21,142,197</td>
<td align="right">20,173,687</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">11,575,514</td>
<td align="right">11,157,755</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">14,182,382</td>
<td align="right">13,675,967</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">74,138,522</td>
<td align="right">71,539,702</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">140,539,805</td>
<td align="right">136,830,973</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">1,713,092</td>
<td align="right">1,683,972</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">4,526,868</td>
<td align="right">4,460,421</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">65,680,429</td>
<td align="right">64,758,972</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">70,920,316</td>
<td align="right">70,259,587</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">345,348,217</td>
<td align="right">343,320,400</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">1,894,123,552</td>
<td align="right">1,883,633,357</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">6,250,377</td>
<td align="right">6,223,554</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">220,000,526</td>
<td align="right">219,062,359</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">91,596</td>
<td align="right">91,336</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">11,732</td>
<td align="right">11,763</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">324,888</td>
<td align="right">324,111</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">163,021,811</td>
<td align="right">162,655,739</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,150,853,633</td>
<td align="right">1,148,822,616</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">3,935,130</td>
<td align="right">3,930,619</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">28,494,119</td>
<td align="right">28,466,013</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">6,503</td>
<td align="right">6,497</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">2,371</td>
<td align="right">2,369</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">419,759,873</td>
<td align="right">419,528,389</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">223,666</td>
<td align="right">223,787</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">31,016</td>
<td align="right">31,000</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">131,427,680</td>
<td align="right">131,373,393</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">437,244</td>
<td align="right">437,407</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">324,285,298</td>
<td align="right">324,189,897</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">326,338,186</td>
<td align="right">326,242,785</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">35,435,783</td>
<td align="right">35,428,137</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,440,667</td>
<td align="right">128,425,585</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">114,996,130</td>
<td align="right">114,987,232</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">302,140,427</td>
<td align="right">302,133,017</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">14,737,868</td>
<td align="right">14,737,963</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">593,230,351</td>
<td align="right">593,230,375</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">172,683,388</td>
<td align="right">172,683,388</td>
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
<td align="left">LOAD_NAME</td>
<td align="right">9,738,715</td>
<td align="right">9,738,715</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">8,975,993</td>
<td align="right">8,975,993</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AITER</td>
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
<td align="left">UNPACK_EX</td>
<td align="right">235,809</td>
<td align="right">235,809</td>
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
<td align="right">47,857</td>
<td align="right">47,857</td>
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
<td align="right">9,180</td>
<td align="right">9,180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">3,372</td>
<td align="right">3,372</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">3,349</td>
<td align="right">3,349</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">2,740</td>
<td align="right">2,740</td>
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
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right"></td>
<td align="right">1,113,687,065</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right"></td>
<td align="right">875,485,764</td>
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
<td align="right">16,995,514,659</td>
<td align="right">87.2%</td>
<td align="right">4,818,633,234</td>
<td align="right">79.7%</td>
<td align="right">-71.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,415,120,426</td>
<td align="right">12.4%</td>
<td align="right">1,165,587,611</td>
<td align="right">19.3%</td>
<td align="right">-51.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">72,187,503</td>
<td align="right">0.4%</td>
<td align="right">64,610,500</td>
<td align="right">1.1%</td>
<td align="right">-10.5%</td>
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
<td align="right">929,818</td>
<td align="right">40.3%</td>
<td align="right">484,023</td>
<td align="right">28.1%</td>
<td align="right">-47.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,378,477</td>
<td align="right">59.7%</td>
<td align="right">1,235,495</td>
<td align="right">71.9%</td>
<td align="right">-10.4%</td>
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
<td align="left">subscr bytes</td>
<td align="right">22,292</td>
<td align="right">2.4%</td>
<td align="right">1,812</td>
<td align="right">0.4%</td>
<td align="right">-91.9%</td>
</tr>
<tr>
<td align="left">subscr mappingproxy</td>
<td align="right">440</td>
<td align="right">0.0%</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">-81.8%</td>
</tr>
<tr>
<td align="left">xor int</td>
<td align="right">85,540</td>
<td align="right">9.2%</td>
<td align="right">16,340</td>
<td align="right">3.4%</td>
<td align="right">-80.9%</td>
</tr>
<tr>
<td align="left">subscr array</td>
<td align="right">127,767</td>
<td align="right">13.7%</td>
<td align="right">25,838</td>
<td align="right">5.3%</td>
<td align="right">-79.8%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">11,588</td>
<td align="right">1.2%</td>
<td align="right">2,767</td>
<td align="right">0.6%</td>
<td align="right">-76.1%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">74,182</td>
<td align="right">8.0%</td>
<td align="right">18,497</td>
<td align="right">3.8%</td>
<td align="right">-75.1%</td>
</tr>
<tr>
<td align="left">subscr counter</td>
<td align="right">107,772</td>
<td align="right">11.6%</td>
<td align="right">26,892</td>
<td align="right">5.6%</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">1,074</td>
<td align="right">0.1%</td>
<td align="right">315</td>
<td align="right">0.1%</td>
<td align="right">-70.7%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">23,511</td>
<td align="right">2.5%</td>
<td align="right">8,293</td>
<td align="right">1.7%</td>
<td align="right">-64.7%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">320</td>
<td align="right">0.0%</td>
<td align="right">140</td>
<td align="right">0.0%</td>
<td align="right">-56.2%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">43,781</td>
<td align="right">4.7%</td>
<td align="right">20,489</td>
<td align="right">4.2%</td>
<td align="right">-53.2%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">34,139</td>
<td align="right">3.7%</td>
<td align="right">20,065</td>
<td align="right">4.1%</td>
<td align="right">-41.2%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">19,441</td>
<td align="right">2.1%</td>
<td align="right">11,542</td>
<td align="right">2.4%</td>
<td align="right">-40.6%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">14,988</td>
<td align="right">1.6%</td>
<td align="right">9,122</td>
<td align="right">1.9%</td>
<td align="right">-39.1%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">8,509</td>
<td align="right">0.9%</td>
<td align="right">6,189</td>
<td align="right">1.3%</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">37,865</td>
<td align="right">4.1%</td>
<td align="right">28,447</td>
<td align="right">5.9%</td>
<td align="right">-24.9%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">78,708</td>
<td align="right">8.5%</td>
<td align="right">62,851</td>
<td align="right">13.0%</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">43,592</td>
<td align="right">4.7%</td>
<td align="right">36,473</td>
<td align="right">7.5%</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">46,864</td>
<td align="right">5.0%</td>
<td align="right">41,346</td>
<td align="right">8.5%</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">2,154</td>
<td align="right">0.2%</td>
<td align="right">1,961</td>
<td align="right">0.4%</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">7,399</td>
<td align="right">0.8%</td>
<td align="right">7,036</td>
<td align="right">1.5%</td>
<td align="right">-4.9%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">2,678</td>
<td align="right">0.3%</td>
<td align="right">2,616</td>
<td align="right">0.5%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">14,314</td>
<td align="right">1.5%</td>
<td align="right">14,020</td>
<td align="right">2.9%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">subscr deque</td>
<td align="right">104</td>
<td align="right">0.0%</td>
<td align="right">103</td>
<td align="right">0.0%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">1,387</td>
<td align="right">0.1%</td>
<td align="right">1,383</td>
<td align="right">0.3%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">628</td>
<td align="right">0.1%</td>
<td align="right">627</td>
<td align="right">0.1%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">2,216</td>
<td align="right">0.2%</td>
<td align="right">2,213</td>
<td align="right">0.5%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">109,553</td>
<td align="right">11.8%</td>
<td align="right">109,554</td>
<td align="right">22.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr range</td>
<td align="right">3,162</td>
<td align="right">0.3%</td>
<td align="right">3,162</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">3,100</td>
<td align="right">0.3%</td>
<td align="right">3,100</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr other slice</td>
<td align="right">312</td>
<td align="right">0.0%</td>
<td align="right">312</td>
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
<td align="left">or int</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr ordereddict</td>
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
<td align="right">543,088,951</td>
<td align="right">100.0%</td>
<td align="right">199,228,538</td>
<td align="right">100.0%</td>
<td align="right">-63.3%</td>
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
<td align="right">12,564,931,053</td>
<td align="right">98.4%</td>
<td align="right">6,512,091,812</td>
<td align="right">97.5%</td>
<td align="right">-48.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">197,968,697</td>
<td align="right">1.6%</td>
<td align="right">169,062,373</td>
<td align="right">2.5%</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">194,295,803</td>
<td align="right">1.5%</td>
<td align="right">165,934,870</td>
<td align="right">2.5%</td>
<td align="right">-14.6%</td>
</tr>
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
<td align="right">8,000</td>
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
<td align="right">3,896,414</td>
<td align="right">100.0%</td>
<td align="right">3,351,144</td>
<td align="right">100.0%</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">146</td>
<td align="right">0.0%</td>
<td align="right">146</td>
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
<td align="left">init not simple</td>
<td align="right">731</td>
<td align="right">500.7%</td>
<td align="right">731</td>
<td align="right">500.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">266</td>
<td align="right">182.2%</td>
<td align="right">266</td>
<td align="right">182.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">146</td>
<td align="right">100.0%</td>
<td align="right">146</td>
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
<td align="right">535,220</td>
<td align="right">96.6%</td>
<td align="right">535,218</td>
<td align="right">96.6%</td>
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
<td align="right">542,289</td>
<td align="right">97.9%</td>
<td align="right">542,289</td>
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
<td align="right">18,801</td>
<td align="right">100.0%</td>
<td align="right">18,834</td>
<td align="right">100.0%</td>
<td align="right">0.2%</td>
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
<td align="right">528,510,507</td>
<td align="right">9.0%</td>
<td align="right">122,451,096</td>
<td align="right">5.8%</td>
<td align="right">-76.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,319,309,645</td>
<td align="right">90.9%</td>
<td align="right">1,980,728,219</td>
<td align="right">94.1%</td>
<td align="right">-62.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,433,648</td>
<td align="right">0.0%</td>
<td align="right">1,245,600</td>
<td align="right">0.1%</td>
<td align="right">-13.1%</td>
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
<td align="right">218,870</td>
<td align="right">81.8%</td>
<td align="right">110,372</td>
<td align="right">71.0%</td>
<td align="right">-49.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">48,642</td>
<td align="right">18.2%</td>
<td align="right">45,191</td>
<td align="right">29.0%</td>
<td align="right">-7.1%</td>
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
<td align="right">84,964</td>
<td align="right">38.8%</td>
<td align="right">4,094</td>
<td align="right">3.7%</td>
<td align="right">-95.2%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">6,823</td>
<td align="right">3.1%</td>
<td align="right">361</td>
<td align="right">0.3%</td>
<td align="right">-94.7%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">10,899</td>
<td align="right">5.0%</td>
<td align="right">6,163</td>
<td align="right">5.6%</td>
<td align="right">-43.5%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">14,803</td>
<td align="right">6.8%</td>
<td align="right">8,945</td>
<td align="right">8.1%</td>
<td align="right">-39.6%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">45,981</td>
<td align="right">21.0%</td>
<td align="right">35,843</td>
<td align="right">32.5%</td>
<td align="right">-22.0%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">1,920</td>
<td align="right">0.9%</td>
<td align="right">1,868</td>
<td align="right">1.7%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">30,613</td>
<td align="right">14.0%</td>
<td align="right">30,223</td>
<td align="right">27.4%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">10,652</td>
<td align="right">4.9%</td>
<td align="right">10,661</td>
<td align="right">9.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">1,350</td>
<td align="right">0.6%</td>
<td align="right">1,349</td>
<td align="right">1.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">9,729</td>
<td align="right">4.4%</td>
<td align="right">9,729</td>
<td align="right">8.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">952</td>
<td align="right">0.4%</td>
<td align="right">952</td>
<td align="right">0.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">184</td>
<td align="right">0.1%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,193,375,726</td>
<td align="right">90.4%</td>
<td align="right">447,065,877</td>
<td align="right">75.9%</td>
<td align="right">-79.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">230,221,191</td>
<td align="right">9.5%</td>
<td align="right">140,620,541</td>
<td align="right">23.9%</td>
<td align="right">-38.9%</td>
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
<td align="right">1,402,138</td>
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
<td align="right">76,141</td>
<td align="right">72.9%</td>
<td align="right">54,351</td>
<td align="right">65.7%</td>
<td align="right">-28.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">28,317</td>
<td align="right">27.1%</td>
<td align="right">28,317</td>
<td align="right">34.3%</td>
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
<td align="right">25,502</td>
<td align="right">33.5%</td>
<td align="right">10,876</td>
<td align="right">20.0%</td>
<td align="right">-57.4%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">10,973</td>
<td align="right">14.4%</td>
<td align="right">9,156</td>
<td align="right">16.8%</td>
<td align="right">-16.6%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">29,051</td>
<td align="right">38.2%</td>
<td align="right">24,262</td>
<td align="right">44.6%</td>
<td align="right">-16.5%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">10,615</td>
<td align="right">13.9%</td>
<td align="right">10,057</td>
<td align="right">18.5%</td>
<td align="right">-5.3%</td>
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
<td align="right">1,505,006,507</td>
<td align="right">28.8%</td>
<td align="right">214,561,100</td>
<td align="right">13.1%</td>
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
<td align="right">164,062,670</td>
<td align="right">3.1%</td>
<td align="right">62,087,034</td>
<td align="right">3.8%</td>
<td align="right">-62.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,557,008,167</td>
<td align="right">68.1%</td>
<td align="right">1,360,848,907</td>
<td align="right">83.1%</td>
<td align="right">-61.7%</td>
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
<td align="right">435,465</td>
<td align="right">12.3%</td>
<td align="right">110,605</td>
<td align="right">8.6%</td>
<td align="right">-74.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,101,100</td>
<td align="right">87.7%</td>
<td align="right">1,177,037</td>
<td align="right">91.4%</td>
<td align="right">-62.0%</td>
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
<td align="right">161,274</td>
<td align="right">37.0%</td>
<td align="right">4,136</td>
<td align="right">3.7%</td>
<td align="right">-97.4%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">83,665</td>
<td align="right">19.2%</td>
<td align="right">10,958</td>
<td align="right">9.9%</td>
<td align="right">-86.9%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">34,739</td>
<td align="right">8.0%</td>
<td align="right">6,164</td>
<td align="right">5.6%</td>
<td align="right">-82.3%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">18,157</td>
<td align="right">4.2%</td>
<td align="right">4,077</td>
<td align="right">3.7%</td>
<td align="right">-77.5%</td>
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
<td align="left">seq iter</td>
<td align="right">19,424</td>
<td align="right">4.5%</td>
<td align="right">6,473</td>
<td align="right">5.9%</td>
<td align="right">-66.7%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">3,396</td>
<td align="right">0.8%</td>
<td align="right">1,169</td>
<td align="right">1.1%</td>
<td align="right">-65.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">11,721</td>
<td align="right">2.7%</td>
<td align="right">4,246</td>
<td align="right">3.8%</td>
<td align="right">-63.8%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">533</td>
<td align="right">0.1%</td>
<td align="right">232</td>
<td align="right">0.2%</td>
<td align="right">-56.5%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">3,051</td>
<td align="right">0.7%</td>
<td align="right">1,931</td>
<td align="right">1.7%</td>
<td align="right">-36.7%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">131</td>
<td align="right">0.0%</td>
<td align="right">91</td>
<td align="right">0.1%</td>
<td align="right">-30.5%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">69,885</td>
<td align="right">16.0%</td>
<td align="right">49,044</td>
<td align="right">44.3%</td>
<td align="right">-29.8%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">17,736</td>
<td align="right">4.1%</td>
<td align="right">12,485</td>
<td align="right">11.3%</td>
<td align="right">-29.6%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">4,324</td>
<td align="right">1.0%</td>
<td align="right">3,430</td>
<td align="right">3.1%</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">6,038</td>
<td align="right">1.4%</td>
<td align="right">5,598</td>
<td align="right">5.1%</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">251</td>
<td align="right">0.1%</td>
<td align="right">251</td>
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
<td align="left">string</td>
<td align="right">2,823,421</td>
<td align="right">2,823,421 / 0 !!</td>
<td align="right">2,769,341</td>
<td align="right">2,769,341 / 0 !!</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">313,242,088</td>
<td align="right">313,242,088 / 0 !!</td>
<td align="right">307,722,332</td>
<td align="right">307,722,332 / 0 !!</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">126,672,941</td>
<td align="right">126,672,941 / 0 !!</td>
<td align="right">124,467,392</td>
<td align="right">124,467,392 / 0 !!</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">5,461,170</td>
<td align="right">5,461,170 / 0 !!</td>
<td align="right">5,390,529</td>
<td align="right">5,390,529 / 0 !!</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">12,144,850</td>
<td align="right">12,144,850 / 0 !!</td>
<td align="right">12,092,821</td>
<td align="right">12,092,821 / 0 !!</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">34,932,458</td>
<td align="right">34,932,458 / 0 !!</td>
<td align="right">34,820,138</td>
<td align="right">34,820,138 / 0 !!</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">173,265,149</td>
<td align="right">173,265,149 / 0 !!</td>
<td align="right">172,849,551</td>
<td align="right">172,849,551 / 0 !!</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">322,269,557</td>
<td align="right">322,269,557 / 0 !!</td>
<td align="right">322,192,746</td>
<td align="right">322,192,746 / 0 !!</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">101,609,516</td>
<td align="right">101,609,516 / 0 !!</td>
<td align="right">101,600,706</td>
<td align="right">101,600,706 / 0 !!</td>
<td align="right">-0.0%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">15,759,517,651</td>
<td align="right">90.2%</td>
<td align="right">10,082,911,735</td>
<td align="right">89.5%</td>
<td align="right">-36.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">849,440,475</td>
<td align="right">4.9%</td>
<td align="right">567,644,364</td>
<td align="right">5.0%</td>
<td align="right">-33.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">867,831,704</td>
<td align="right">5.0%</td>
<td align="right">617,473,933</td>
<td align="right">5.5%</td>
<td align="right">-28.8%</td>
</tr>
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
<td align="right">1,422,762</td>
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
<td align="right">16,450,031</td>
<td align="right">97.0%</td>
<td align="right">11,726,524</td>
<td align="right">96.4%</td>
<td align="right">-28.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">513,226</td>
<td align="right">3.0%</td>
<td align="right">439,960</td>
<td align="right">3.6%</td>
<td align="right">-14.3%</td>
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
<td align="right">80,970</td>
<td align="right">15.8%</td>
<td align="right">43,398</td>
<td align="right">9.9%</td>
<td align="right">-46.4%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">1,078</td>
<td align="right">0.2%</td>
<td align="right">718</td>
<td align="right">0.2%</td>
<td align="right">-33.4%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">59,367</td>
<td align="right">11.6%</td>
<td align="right">40,107</td>
<td align="right">9.1%</td>
<td align="right">-32.4%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">5,962</td>
<td align="right">1.2%</td>
<td align="right">4,726</td>
<td align="right">1.1%</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">2,734</td>
<td align="right">0.5%</td>
<td align="right">2,374</td>
<td align="right">0.5%</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">52,598</td>
<td align="right">10.2%</td>
<td align="right">47,877</td>
<td align="right">10.9%</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">24,277</td>
<td align="right">4.7%</td>
<td align="right">23,253</td>
<td align="right">5.3%</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">17,019</td>
<td align="right">3.3%</td>
<td align="right">16,352</td>
<td align="right">3.7%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1,710</td>
<td align="right">0.3%</td>
<td align="right">1,709</td>
<td align="right">0.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">7,603</td>
<td align="right">1.5%</td>
<td align="right">7,607</td>
<td align="right">1.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">4,411</td>
<td align="right">0.9%</td>
<td align="right">4,410</td>
<td align="right">1.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">1,035</td>
<td align="right">0.2%</td>
<td align="right">1,035</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">861</td>
<td align="right">0.2%</td>
<td align="right">861</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">643</td>
<td align="right">0.1%</td>
<td align="right">643</td>
<td align="right">0.1%</td>
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
<td align="right">10,978,074,259</td>
<td align="right">99.9%</td>
<td align="right">6,247,485,720</td>
<td align="right">99.8%</td>
<td align="right">-43.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">43,909</td>
<td align="right">0.0%</td>
<td align="right">43,907</td>
<td align="right">0.0%</td>
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
<td align="right">14,612,364</td>
<td align="right">0.1%</td>
<td align="right">14,612,308</td>
<td align="right">0.2%</td>
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
<td align="right">1,325</td>
<td align="right">0.0%</td>
<td align="right">1,325</td>
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
<td align="right">126,230</td>
<td align="right">100.0%</td>
<td align="right">126,381</td>
<td align="right">100.0%</td>
<td align="right">0.1%</td>
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
<td align="right">68,188,261</td>
<td align="right">100.0%</td>
<td align="right">62,608,683</td>
<td align="right">100.0%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">112</td>
<td align="right">0.0%</td>
<td align="right">110</td>
<td align="right">0.0%</td>
<td align="right">-1.8%</td>
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
<td align="right">2,259</td>
<td align="right">100.0%</td>
<td align="right">2,259</td>
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
<td align="right">128,391,290</td>
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
<td align="right">593,215,640</td>
<td align="right">82.2%</td>
<td align="right">593,215,664</td>
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
<td align="right">33,951</td>
<td align="right">98.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">616</td>
<td align="right">1.8%</td>
<td align="right">616</td>
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
<td align="right">640</td>
<td align="right">1.9%</td>
<td align="right">640</td>
<td align="right">1.9%</td>
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
<td align="right">2,608,662,515</td>
<td align="right">93.5%</td>
<td align="right">2,311,683,028</td>
<td align="right">93.2%</td>
<td align="right">-11.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">64,617,781</td>
<td align="right">2.3%</td>
<td align="right">58,656,793</td>
<td align="right">2.4%</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">115,304,425</td>
<td align="right">4.1%</td>
<td align="right">108,599,248</td>
<td align="right">4.4%</td>
<td align="right">-5.8%</td>
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
<td align="right">2,214,793</td>
<td align="right">98.0%</td>
<td align="right">2,088,515</td>
<td align="right">98.0%</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">45,009</td>
<td align="right">2.0%</td>
<td align="right">43,520</td>
<td align="right">2.0%</td>
<td align="right">-3.3%</td>
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
<td align="right">6,084</td>
<td align="right">13.5%</td>
<td align="right">4,651</td>
<td align="right">10.7%</td>
<td align="right">-23.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">243,426</td>
<td align="right">540.8%</td>
<td align="right">236,043</td>
<td align="right">542.4%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">3,004</td>
<td align="right">6.7%</td>
<td align="right">2,975</td>
<td align="right">6.8%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">20,316</td>
<td align="right">45.1%</td>
<td align="right">20,295</td>
<td align="right">46.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">7,206</td>
<td align="right">16.0%</td>
<td align="right">7,206</td>
<td align="right">16.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">3,673</td>
<td align="right">8.2%</td>
<td align="right">3,673</td>
<td align="right">8.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">1,614</td>
<td align="right">3.6%</td>
<td align="right">1,614</td>
<td align="right">3.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">749</td>
<td align="right">1.7%</td>
<td align="right">749</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">421</td>
<td align="right">0.9%</td>
<td align="right">421</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">313</td>
<td align="right">0.7%</td>
<td align="right">313</td>
<td align="right">0.7%</td>
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
<tr>
<td align="left">mutable class</td>
<td align="right">89</td>
<td align="right">0.2%</td>
<td align="right">89</td>
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
<td align="right">112,724,874</td>
<td align="right">100.0%</td>
<td align="right">1,232,454</td>
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
<td align="right">691,400,686</td>
<td align="right">42.1%</td>
<td align="right">103,526,403</td>
<td align="right">29.5%</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">950,412,104</td>
<td align="right">57.9%</td>
<td align="right">246,819,589</td>
<td align="right">70.4%</td>
<td align="right">-74.0%</td>
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
<td align="right">179,717</td>
<td align="right">98.4%</td>
<td align="right">36,220</td>
<td align="right">92.4%</td>
<td align="right">-79.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,961</td>
<td align="right">1.6%</td>
<td align="right">2,962</td>
<td align="right">7.6%</td>
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
<td align="right">81,221</td>
<td align="right">45.2%</td>
<td align="right">320</td>
<td align="right">0.9%</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">5,259</td>
<td align="right">2.9%</td>
<td align="right">136</td>
<td align="right">0.4%</td>
<td align="right">-97.4%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">19,143</td>
<td align="right">10.7%</td>
<td align="right">3,283</td>
<td align="right">9.1%</td>
<td align="right">-82.9%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">52,096</td>
<td align="right">29.0%</td>
<td align="right">10,484</td>
<td align="right">28.9%</td>
<td align="right">-79.9%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">2,978</td>
<td align="right">1.7%</td>
<td align="right">2,977</td>
<td align="right">8.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">17,279</td>
<td align="right">9.6%</td>
<td align="right">17,279</td>
<td align="right">47.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">1,673</td>
<td align="right">0.9%</td>
<td align="right">1,673</td>
<td align="right">4.6%</td>
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
<td align="right">111,275,212</td>
<td align="right">1.7%</td>
<td align="right">65,091,063</td>
<td align="right">1.6%</td>
<td align="right">-41.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,813,813,201</td>
<td align="right">91.2%</td>
<td align="right">3,667,974,239</td>
<td align="right">90.4%</td>
<td align="right">-36.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">445,660,417</td>
<td align="right">7.0%</td>
<td align="right">323,862,680</td>
<td align="right">8.0%</td>
<td align="right">-27.3%</td>
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
<td align="right">2,147,635</td>
<td align="right">77.0%</td>
<td align="right">1,276,211</td>
<td align="right">69.7%</td>
<td align="right">-40.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">642,063</td>
<td align="right">23.0%</td>
<td align="right">554,456</td>
<td align="right">30.3%</td>
<td align="right">-13.6%</td>
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
<td align="right">16,018</td>
<td align="right">2.5%</td>
<td align="right">1,818</td>
<td align="right">0.3%</td>
<td align="right">-88.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">126,752</td>
<td align="right">19.7%</td>
<td align="right">68,542</td>
<td align="right">12.4%</td>
<td align="right">-45.9%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">16,260</td>
<td align="right">2.5%</td>
<td align="right">10,914</td>
<td align="right">2.0%</td>
<td align="right">-32.9%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">85,534</td>
<td align="right">13.3%</td>
<td align="right">75,987</td>
<td align="right">13.7%</td>
<td align="right">-11.2%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">9,787</td>
<td align="right">1.5%</td>
<td align="right">9,502</td>
<td align="right">1.7%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">6,474</td>
<td align="right">1.0%</td>
<td align="right">6,481</td>
<td align="right">1.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">71,794</td>
<td align="right">11.2%</td>
<td align="right">71,768</td>
<td align="right">12.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">308,978</td>
<td align="right">48.1%</td>
<td align="right">308,978</td>
<td align="right">55.7%</td>
<td align="right">0.0%</td>
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
<td align="right">1,272,766,890</td>
<td align="right">99.9%</td>
<td align="right">696,468,951</td>
<td align="right">99.8%</td>
<td align="right">-45.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,568,865</td>
<td align="right">0.1%</td>
<td align="right">1,204,465</td>
<td align="right">0.2%</td>
<td align="right">-23.2%</td>
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
<td align="right">868</td>
<td align="right">8.1%</td>
<td align="right">752</td>
<td align="right">7.1%</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">9,806</td>
<td align="right">91.9%</td>
<td align="right">9,794</td>
<td align="right">92.9%</td>
<td align="right">-0.1%</td>
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
<td align="right">637</td>
<td align="right">73.4%</td>
<td align="right">521</td>
<td align="right">69.3%</td>
<td align="right">-18.2%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">132</td>
<td align="right">15.2%</td>
<td align="right">132</td>
<td align="right">17.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">99</td>
<td align="right">11.4%</td>
<td align="right">99</td>
<td align="right">13.2%</td>
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
<td align="right">8,628,417,245</td>
<td align="right">3.6%</td>
<td align="right">3,600,547,893</td>
<td align="right">2.9%</td>
<td align="right">-58.3%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">90,897,384,631</td>
<td align="right">38.3%</td>
<td align="right">46,682,891,968</td>
<td align="right">37.9%</td>
<td align="right">-48.6%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">136,338,266,205</td>
<td align="right">57.4%</td>
<td align="right">71,912,540,221</td>
<td align="right">58.3%</td>
<td align="right">-47.3%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,532,233,172</td>
<td align="right">0.6%</td>
<td align="right">1,090,340,678</td>
<td align="right">0.9%</td>
<td align="right">-28.8%</td>
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
<td align="right">1,505,006,507</td>
<td align="right">19.5%</td>
<td align="right">214,561,100</td>
<td align="right">6.7%</td>
<td align="right">-85.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">691,400,686</td>
<td align="right">8.9%</td>
<td align="right">103,526,403</td>
<td align="right">3.2%</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">528,510,507</td>
<td align="right">6.8%</td>
<td align="right">122,451,096</td>
<td align="right">3.8%</td>
<td align="right">-76.8%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">543,088,951</td>
<td align="right">7.0%</td>
<td align="right">199,228,538</td>
<td align="right">6.2%</td>
<td align="right">-63.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,415,120,426</td>
<td align="right">31.3%</td>
<td align="right">1,165,587,611</td>
<td align="right">36.3%</td>
<td align="right">-51.7%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">230,221,191</td>
<td align="right">3.0%</td>
<td align="right">140,620,541</td>
<td align="right">4.4%</td>
<td align="right">-38.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">849,440,475</td>
<td align="right">11.0%</td>
<td align="right">567,644,364</td>
<td align="right">17.7%</td>
<td align="right">-33.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">445,660,417</td>
<td align="right">5.8%</td>
<td align="right">323,862,680</td>
<td align="right">10.1%</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">194,295,803</td>
<td align="right">2.5%</td>
<td align="right">165,934,870</td>
<td align="right">5.2%</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,406,370</td>
<td align="right">1.7%</td>
<td align="right">128,391,290</td>
<td align="right">4.0%</td>
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
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">81,894,134</td>
<td align="right">5.3%</td>
<td align="right">30,945,823</td>
<td align="right">2.8%</td>
<td align="right">-62.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">82,041,762</td>
<td align="right">5.4%</td>
<td align="right">31,014,697</td>
<td align="right">2.8%</td>
<td align="right">-62.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">49,476,367</td>
<td align="right">3.2%</td>
<td align="right">27,182,010</td>
<td align="right">2.5%</td>
<td align="right">-45.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">54,987,827</td>
<td align="right">3.6%</td>
<td align="right">31,239,018</td>
<td align="right">2.9%</td>
<td align="right">-43.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">369,735,073</td>
<td align="right">24.1%</td>
<td align="right">220,120,975</td>
<td align="right">20.2%</td>
<td align="right">-40.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">268,643,907</td>
<td align="right">17.5%</td>
<td align="right">179,178,255</td>
<td align="right">16.4%</td>
<td align="right">-33.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">90,396,587</td>
<td align="right">5.9%</td>
<td align="right">63,293,238</td>
<td align="right">5.8%</td>
<td align="right">-30.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">95,065,142</td>
<td align="right">6.2%</td>
<td align="right">88,803,017</td>
<td align="right">8.1%</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">89,821,230</td>
<td align="right">5.9%</td>
<td align="right">84,909,134</td>
<td align="right">7.8%</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">82,487,137</td>
<td align="right">5.4%</td>
<td align="right">79,121,103</td>
<td align="right">7.3%</td>
<td align="right">-4.1%</td>
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
<td align="right">141,112,765</td>
<td align="right">1.8%</td>
<td align="right">132,513,832</td>
<td align="right">1.7%</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">72,979,235</td>
<td align="right">0.9%</td>
<td align="right">70,108,951</td>
<td align="right">0.9%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,028,267,074</td>
<td align="right">76.0%</td>
<td align="right">5,885,987,662</td>
<td align="right">75.7%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,698,706,144</td>
<td align="right">84.5%</td>
<td align="right">6,547,888,214</td>
<td align="right">84.2%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,280,424,424</td>
<td align="right">16.2%</td>
<td align="right">1,269,953,774</td>
<td align="right">16.3%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,284,701,091</td>
<td align="right">16.2%</td>
<td align="right">1,274,230,441</td>
<td align="right">16.4%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">1,898,599,112</td>
<td align="right">24.0%</td>
<td align="right">1,888,108,642</td>
<td align="right">24.3%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">1,898,599,112</td>
<td align="right">24.0%</td>
<td align="right">1,888,108,642</td>
<td align="right">24.3%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">613,898,021</td>
<td align="right">7.7%</td>
<td align="right">613,878,201</td>
<td align="right">7.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">458,227,598</td>
<td align="right">5.8%</td>
<td align="right">458,214,715</td>
<td align="right">5.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">24,435,363</td>
<td align="right">0.3%</td>
<td align="right">24,434,845</td>
<td align="right">0.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">308,343,108</td>
<td align="right">3.9%</td>
<td align="right">308,343,863</td>
<td align="right">4.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">4,273,295</td>
<td align="right">0.1%</td>
<td align="right">4,273,295</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">3,372</td>
<td align="right">0.0%</td>
<td align="right">3,372</td>
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
<td align="right">8,764,968</td>
<td align="right"></td>
<td align="right">29,710,114</td>
<td align="right"></td>
<td align="right">239.0%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">67,188,348</td>
<td align="right"></td>
<td align="right">89,026,043</td>
<td align="right"></td>
<td align="right">32.5%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">4,052,003</td>
<td align="right">2.1%</td>
<td align="right">3,386,403</td>
<td align="right">1.8%</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">306,669</td>
<td align="right">0.2%</td>
<td align="right">265,069</td>
<td align="right">0.1%</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">2,312,212,803</td>
<td align="right"></td>
<td align="right">2,089,077,650</td>
<td align="right"></td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">2,032,275,236</td>
<td align="right">1.8%</td>
<td align="right">1,986,777,743</td>
<td align="right">1.7%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">23,565,205,620</td>
<td align="right">23.7%</td>
<td align="right">23,139,994,008</td>
<td align="right">23.4%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">59,223,214</td>
<td align="right"></td>
<td align="right">60,118,076</td>
<td align="right"></td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">2,902,329,817</td>
<td align="right"></td>
<td align="right">2,863,801,617</td>
<td align="right"></td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">23,145,989,425</td>
<td align="right">20.3%</td>
<td align="right">22,858,754,799</td>
<td align="right">20.1%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">14,214,720,111</td>
<td align="right">70.5%</td>
<td align="right">14,041,553,332</td>
<td align="right">70.4%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">14,214,877,135</td>
<td align="right"></td>
<td align="right">14,041,723,244</td>
<td align="right"></td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">25,820,218,010</td>
<td align="right">26.0%</td>
<td align="right">25,541,343,248</td>
<td align="right">25.9%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">5,507,614,502</td>
<td align="right">5.5%</td>
<td align="right">5,448,309,618</td>
<td align="right">5.5%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">5,858,200,177</td>
<td align="right">29.1%</td>
<td align="right">5,815,851,381</td>
<td align="right">29.2%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">32,565,953,905</td>
<td align="right">28.5%</td>
<td align="right">32,332,046,947</td>
<td align="right">28.5%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">5,936,391,112</td>
<td align="right">29.5%</td>
<td align="right">5,893,979,142</td>
<td align="right">29.6%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">6,534,908,544</td>
<td align="right"></td>
<td align="right">6,489,881,154</td>
<td align="right"></td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">191,449,712</td>
<td align="right"></td>
<td align="right">190,425,664</td>
<td align="right"></td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">44,444,210,503</td>
<td align="right">44.7%</td>
<td align="right">44,573,675,577</td>
<td align="right">45.2%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">56,488,793,683</td>
<td align="right">49.5%</td>
<td align="right">56,363,353,347</td>
<td align="right">49.6%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">71,490,543</td>
<td align="right">0.4%</td>
<td align="right">71,432,463</td>
<td align="right">0.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">6,700,392</td>
<td align="right">0.0%</td>
<td align="right">6,695,298</td>
<td align="right">0.0%</td>
<td align="right">-0.1%</td>
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
<td align="right">359,237</td>
<td align="right">105,205,929</td>
<td align="right">9,709,803,545</td>
<td align="right">793,107,366</td>
<td align="right">757,127,444</td>
<td align="right">357,907</td>
<td align="right">103,561,289</td>
<td align="right">9,615,853,270</td>
<td align="right">785,158,206</td>
<td align="right">751,025,320</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">15,998</td>
<td align="right">8,734,505</td>
<td align="right">11,444,022,222</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">15,998</td>
<td align="right">8,734,505</td>
<td align="right">11,444,556,678</td>
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
<td align="right">120</td>
<td align="right">120 / 0 !!</td>
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
<td align="right">120</td>
<td align="right">120 / 0 !!</td>
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
<td align="right">2,435</td>
<td align="right">2,435</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-07-13
