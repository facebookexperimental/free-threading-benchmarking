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
<td align="right">5,923,081,419</td>
<td align="right">7,699,809</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">112,725,129</td>
<td align="right">1,085,625</td>
<td align="right">-99.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">441,386,435</td>
<td align="right">9,875,293</td>
<td align="right">-97.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">62,380,388</td>
<td align="right">2,297,114</td>
<td align="right">-96.3%</td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">100,136,760</td>
<td align="right">6,000,000</td>
<td align="right">-94.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,508,236,620</td>
<td align="right">204,515,528</td>
<td align="right">-86.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,588,072,216</td>
<td align="right">228,071,425</td>
<td align="right">-85.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">693,121,212</td>
<td align="right">101,354,748</td>
<td align="right">-85.4%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,388,639,513</td>
<td align="right">203,896,731</td>
<td align="right">-85.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,753,883,266</td>
<td align="right">277,202,100</td>
<td align="right">-84.2%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,220,554,945</td>
<td align="right">194,709,005</td>
<td align="right">-84.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">2,716,376,461</td>
<td align="right">442,185,150</td>
<td align="right">-83.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">577,800,925</td>
<td align="right">95,465,722</td>
<td align="right">-83.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">403,049,840</td>
<td align="right">68,653,741</td>
<td align="right">-83.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">2,097,546,836</td>
<td align="right">368,514,695</td>
<td align="right">-82.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,441,643,212</td>
<td align="right">606,629,385</td>
<td align="right">-82.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,240,440,917</td>
<td align="right">406,655,579</td>
<td align="right">-81.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">507,441,136</td>
<td align="right">94,164,859</td>
<td align="right">-81.4%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">89,055,829</td>
<td align="right">17,467,135</td>
<td align="right">-80.4%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">116,434,977</td>
<td align="right">23,649,217</td>
<td align="right">-79.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">1,251,912,100</td>
<td align="right">265,631,939</td>
<td align="right">-78.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">884,161,508</td>
<td align="right">190,784,856</td>
<td align="right">-78.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">353,327,957</td>
<td align="right">76,417,521</td>
<td align="right">-78.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">158,449,394</td>
<td align="right">34,420,892</td>
<td align="right">-78.3%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">654,944,799</td>
<td align="right">151,871,168</td>
<td align="right">-76.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">729,321,792</td>
<td align="right">173,790,390</td>
<td align="right">-76.2%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">123,914,279</td>
<td align="right">30,360,735</td>
<td align="right">-75.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">448,177,000</td>
<td align="right">111,983,572</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">62,995,725</td>
<td align="right">15,872,571</td>
<td align="right">-74.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">942,910,650</td>
<td align="right">239,358,250</td>
<td align="right">-74.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">562,992,638</td>
<td align="right">146,023,573</td>
<td align="right">-74.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,623,421,861</td>
<td align="right">424,438,388</td>
<td align="right">-73.9%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">7,316,207,889</td>
<td align="right">1,989,214,477</td>
<td align="right">-72.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">199,618,963</td>
<td align="right">56,544,949</td>
<td align="right">-71.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,466,863,364</td>
<td align="right">1,006,511,035</td>
<td align="right">-71.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">541,617,267</td>
<td align="right">160,435,889</td>
<td align="right">-70.4%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">57,250,825</td>
<td align="right">17,097,302</td>
<td align="right">-70.1%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">704,858,617</td>
<td align="right">212,882,815</td>
<td align="right">-69.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">2,160,569,461</td>
<td align="right">652,657,465</td>
<td align="right">-69.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,258,235,244</td>
<td align="right">383,668,758</td>
<td align="right">-69.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,167,227,031</td>
<td align="right">670,044,296</td>
<td align="right">-69.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">262,266,375</td>
<td align="right">81,567,003</td>
<td align="right">-68.9%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">375,497,965</td>
<td align="right">117,454,434</td>
<td align="right">-68.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,506,238,380</td>
<td align="right">784,363,567</td>
<td align="right">-68.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">2,846,620,336</td>
<td align="right">905,742,334</td>
<td align="right">-68.2%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,506,623,144</td>
<td align="right">807,217,490</td>
<td align="right">-67.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,884,551,894</td>
<td align="right">1,933,983,732</td>
<td align="right">-67.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">13,745,845,117</td>
<td align="right">4,587,232,792</td>
<td align="right">-66.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">10,392,456,447</td>
<td align="right">3,473,032,514</td>
<td align="right">-66.6%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">158,352,249</td>
<td align="right">54,067,802</td>
<td align="right">-65.9%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">525,661,645</td>
<td align="right">180,259,454</td>
<td align="right">-65.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">357,274,885</td>
<td align="right">124,902,642</td>
<td align="right">-65.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">77,914,811</td>
<td align="right">27,776,340</td>
<td align="right">-64.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">10,903,301,068</td>
<td align="right">3,921,645,313</td>
<td align="right">-64.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">1,042,250,209</td>
<td align="right">378,568,822</td>
<td align="right">-63.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">23,171,193</td>
<td align="right">8,733,357</td>
<td align="right">-62.3%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">67,399,944</td>
<td align="right">26,552,502</td>
<td align="right">-60.6%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">263,793,853</td>
<td align="right">103,961,442</td>
<td align="right">-60.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">102,941,963</td>
<td align="right">40,728,032</td>
<td align="right">-60.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,518,520,811</td>
<td align="right">999,413,096</td>
<td align="right">-60.3%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,203,806,289</td>
<td align="right">487,989,411</td>
<td align="right">-59.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">443,496,497</td>
<td align="right">183,443,914</td>
<td align="right">-58.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,131,502,741</td>
<td align="right">468,512,477</td>
<td align="right">-58.6%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,156,329</td>
<td align="right">2,600,969</td>
<td align="right">-57.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">8,700,068,189</td>
<td align="right">3,748,520,598</td>
<td align="right">-56.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">805,191,421</td>
<td align="right">354,273,815</td>
<td align="right">-56.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">34,383,359,824</td>
<td align="right">15,418,565,729</td>
<td align="right">-55.2%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">787,803,045</td>
<td align="right">356,213,565</td>
<td align="right">-54.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">92,363,064</td>
<td align="right">42,030,240</td>
<td align="right">-54.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">77,196,926</td>
<td align="right">35,415,427</td>
<td align="right">-54.1%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,094,740,678</td>
<td align="right">507,158,864</td>
<td align="right">-53.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">275,909,160</td>
<td align="right">129,204,548</td>
<td align="right">-53.2%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">1,055,447,451</td>
<td align="right">496,862,546</td>
<td align="right">-52.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">7,879,405</td>
<td align="right">3,714,396</td>
<td align="right">-52.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,984,107,304</td>
<td align="right">1,887,023,312</td>
<td align="right">-52.6%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">131,427,667</td>
<td align="right">62,800,184</td>
<td align="right">-52.2%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,582,195,012</td>
<td align="right">758,254,261</td>
<td align="right">-52.1%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">553,400,781</td>
<td align="right">274,068,032</td>
<td align="right">-50.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">205,945,641</td>
<td align="right">103,794,929</td>
<td align="right">-49.6%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">100,403,840</td>
<td align="right">51,504,789</td>
<td align="right">-48.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">257,273,166</td>
<td align="right">132,730,946</td>
<td align="right">-48.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">92,219,519</td>
<td align="right">48,295,698</td>
<td align="right">-47.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">334,446,132</td>
<td align="right">175,915,827</td>
<td align="right">-47.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,604,014,869</td>
<td align="right">1,394,798,183</td>
<td align="right">-46.4%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">13,167,711</td>
<td align="right">7,168,447</td>
<td align="right">-45.6%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">94,136,760</td>
<td align="right">136,976,966</td>
<td align="right">45.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">283,860,783</td>
<td align="right">154,804,332</td>
<td align="right">-45.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">374,892,151</td>
<td align="right">210,508,377</td>
<td align="right">-43.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,546,640,998</td>
<td align="right">878,950,904</td>
<td align="right">-43.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">291,564,794</td>
<td align="right">165,705,430</td>
<td align="right">-43.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">374,490,936</td>
<td align="right">213,379,449</td>
<td align="right">-43.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">3,355,557,487</td>
<td align="right">1,918,927,237</td>
<td align="right">-42.8%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">118,583,102</td>
<td align="right">67,968,447</td>
<td align="right">-42.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">781,278,563</td>
<td align="right">447,986,396</td>
<td align="right">-42.7%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">61,351,379</td>
<td align="right">35,537,597</td>
<td align="right">-42.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">195,093,484</td>
<td align="right">114,764,835</td>
<td align="right">-41.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">216,661,437</td>
<td align="right">128,212,479</td>
<td align="right">-40.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">266,892,131</td>
<td align="right">162,624,478</td>
<td align="right">-39.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">825,717,187</td>
<td align="right">503,856,357</td>
<td align="right">-39.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">5,197,803,766</td>
<td align="right">3,173,143,031</td>
<td align="right">-39.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">184,463,026</td>
<td align="right">112,909,352</td>
<td align="right">-38.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,373,403,477</td>
<td align="right">844,237,304</td>
<td align="right">-38.5%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">190,528,661</td>
<td align="right">118,942,093</td>
<td align="right">-37.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">8,975,993</td>
<td align="right">5,693,673</td>
<td align="right">-36.6%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">193,912,356</td>
<td align="right">125,549,993</td>
<td align="right">-35.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">74,132,229</td>
<td align="right">49,247,586</td>
<td align="right">-33.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">490,666,682</td>
<td align="right">329,006,287</td>
<td align="right">-32.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,538,009,335</td>
<td align="right">2,398,462,054</td>
<td align="right">-32.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">66,859,864</td>
<td align="right">45,577,927</td>
<td align="right">-31.8%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">255,422,744</td>
<td align="right">175,943,833</td>
<td align="right">-31.1%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">253,369,856</td>
<td align="right">174,595,065</td>
<td align="right">-31.1%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">402,783,187</td>
<td align="right">283,542,508</td>
<td align="right">-29.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">78,593,858</td>
<td align="right">55,723,606</td>
<td align="right">-29.1%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">852,238,399</td>
<td align="right">616,425,271</td>
<td align="right">-27.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,377,454,340</td>
<td align="right">2,456,711,491</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,630,037,179</td>
<td align="right">4,122,746,609</td>
<td align="right">-26.8%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,541,926,657</td>
<td align="right">4,820,452,553</td>
<td align="right">-26.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">349,240,536</td>
<td align="right">259,293,005</td>
<td align="right">-25.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">689,011,749</td>
<td align="right">518,925,366</td>
<td align="right">-24.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">473,193,108</td>
<td align="right">358,686,717</td>
<td align="right">-24.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">67,712,282</td>
<td align="right">51,996,426</td>
<td align="right">-23.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">1,581,878</td>
<td align="right">1,214,890</td>
<td align="right">-23.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">942,944,248</td>
<td align="right">734,783,927</td>
<td align="right">-22.1%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">83,221,629</td>
<td align="right">66,834,832</td>
<td align="right">-19.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,100,495,554</td>
<td align="right">890,750,037</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">276,317,460</td>
<td align="right">224,928,312</td>
<td align="right">-18.6%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">346,772,006</td>
<td align="right">285,214,690</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">70,162,343</td>
<td align="right">57,998,281</td>
<td align="right">-17.3%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,760,056</td>
<td align="right">3,124,716</td>
<td align="right">-16.9%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">87,672</td>
<td align="right">73,592</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">418,046,026</td>
<td align="right">350,927,157</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">21,349,250</td>
<td align="right">18,019,393</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">21,349,251</td>
<td align="right">18,019,394</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">21,007,004</td>
<td align="right">17,846,527</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">115,236,757</td>
<td align="right">98,457,566</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">9,180</td>
<td align="right">10,380</td>
<td align="right">13.1%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">78,021,677</td>
<td align="right">70,204,680</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">72,351,579</td>
<td align="right">65,541,768</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,177,644</td>
<td align="right">5,641,766</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">63,731,985</td>
<td align="right">58,350,615</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">LOAD_FROM_DICT_OR_DEREF</td>
<td align="right">1,460</td>
<td align="right">1,340</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">1,630,974,264</td>
<td align="right">1,498,738,770</td>
<td align="right">-8.1%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">152,429,824</td>
<td align="right">140,533,712</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">473,004</td>
<td align="right">437,321</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">31,003</td>
<td align="right">28,839</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">346,922,504</td>
<td align="right">324,691,207</td>
<td align="right">-6.4%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">10,294,872</td>
<td align="right">9,679,630</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">6,362,441</td>
<td align="right">5,997,953</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">3,349</td>
<td align="right">3,189</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">74,348,140</td>
<td align="right">70,884,278</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">163,034,562</td>
<td align="right">155,672,169</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">11,999,581</td>
<td align="right">11,474,194</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">14,697,034</td>
<td align="right">14,181,337</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">127,613,814</td>
<td align="right">123,751,884</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">3,956,570</td>
<td align="right">3,845,041</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">196,104,123</td>
<td align="right">190,596,148</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">29,061,522</td>
<td align="right">28,462,848</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">66,057,413</td>
<td align="right">65,232,899</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">3,372</td>
<td align="right">3,332</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">47,846</td>
<td align="right">47,366</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">35,680,972</td>
<td align="right">35,428,173</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">4,558,456</td>
<td align="right">4,526,914</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">324,882</td>
<td align="right">322,688</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,152,992,098</td>
<td align="right">1,146,663,337</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">11,724</td>
<td align="right">11,768</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">91,596</td>
<td align="right">91,336</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">420,296,222</td>
<td align="right">419,682,429</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">223,900</td>
<td align="right">224,220</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">593,922,213</td>
<td align="right">593,230,411</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">14,640,076</td>
<td align="right">14,627,518</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">2,369</td>
<td align="right">2,371</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">302,369,291</td>
<td align="right">302,133,017</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">41,995,026</td>
<td align="right">41,964,122</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">6,507</td>
<td align="right">6,509</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,456,529</td>
<td align="right">128,425,585</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">14,737,894</td>
<td align="right">14,738,372</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">9,738,685</td>
<td align="right">9,738,485</td>
<td align="right">-0.0%</td>
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
<td align="left">END_ASYNC_FOR</td>
<td align="right">6,000,000</td>
<td align="right">6,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">1,714,272</td>
<td align="right">1,714,272</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">235,809</td>
<td align="right">235,809</td>
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
<td align="left">DICT_UPDATE</td>
<td align="right">14,747</td>
<td align="right">14,747</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">2,740</td>
<td align="right">2,740</td>
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
<td align="right">1,041,024,332</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right"></td>
<td align="right">755,233,216</td>
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
<td align="right">16,313,954,546</td>
<td align="right">86.3%</td>
<td align="right">3,869,427,306</td>
<td align="right">78.6%</td>
<td align="right">-76.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,517,549,274</td>
<td align="right">13.3%</td>
<td align="right">998,994,870</td>
<td align="right">20.3%</td>
<td align="right">-60.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">62,394,875</td>
<td align="right">0.3%</td>
<td align="right">52,182,047</td>
<td align="right">1.1%</td>
<td align="right">-16.4%</td>
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
<td align="right">954,906</td>
<td align="right">44.4%</td>
<td align="right">401,655</td>
<td align="right">28.6%</td>
<td align="right">-57.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,193,660</td>
<td align="right">55.6%</td>
<td align="right">1,000,873</td>
<td align="right">71.4%</td>
<td align="right">-16.2%</td>
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
<td align="left">and different types</td>
<td align="right">41</td>
<td align="right">0.0%</td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right">-92.7%</td>
</tr>
<tr>
<td align="left">subscr bytes</td>
<td align="right">22,288</td>
<td align="right">2.3%</td>
<td align="right">1,808</td>
<td align="right">0.5%</td>
<td align="right">-91.9%</td>
</tr>
<tr>
<td align="left">subscr array</td>
<td align="right">166,377</td>
<td align="right">17.4%</td>
<td align="right">25,838</td>
<td align="right">6.4%</td>
<td align="right">-84.5%</td>
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
<td align="right">9.0%</td>
<td align="right">16,340</td>
<td align="right">4.1%</td>
<td align="right">-80.9%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">11,587</td>
<td align="right">1.2%</td>
<td align="right">2,768</td>
<td align="right">0.7%</td>
<td align="right">-76.1%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">74,202</td>
<td align="right">7.8%</td>
<td align="right">18,488</td>
<td align="right">4.6%</td>
<td align="right">-75.1%</td>
</tr>
<tr>
<td align="left">subscr counter</td>
<td align="right">107,772</td>
<td align="right">11.3%</td>
<td align="right">26,892</td>
<td align="right">6.7%</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">8,232</td>
<td align="right">0.9%</td>
<td align="right">2,349</td>
<td align="right">0.6%</td>
<td align="right">-71.5%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">1,082</td>
<td align="right">0.1%</td>
<td align="right">316</td>
<td align="right">0.1%</td>
<td align="right">-70.8%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">2,681</td>
<td align="right">0.3%</td>
<td align="right">836</td>
<td align="right">0.2%</td>
<td align="right">-68.8%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">23,525</td>
<td align="right">2.5%</td>
<td align="right">8,299</td>
<td align="right">2.1%</td>
<td align="right">-64.7%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">43,287</td>
<td align="right">4.5%</td>
<td align="right">18,123</td>
<td align="right">4.5%</td>
<td align="right">-58.1%</td>
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
<td align="right">43,769</td>
<td align="right">4.6%</td>
<td align="right">19,520</td>
<td align="right">4.9%</td>
<td align="right">-55.4%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">33,949</td>
<td align="right">3.6%</td>
<td align="right">19,821</td>
<td align="right">4.9%</td>
<td align="right">-41.6%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">37,894</td>
<td align="right">4.0%</td>
<td align="right">22,356</td>
<td align="right">5.6%</td>
<td align="right">-41.0%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">19,440</td>
<td align="right">2.0%</td>
<td align="right">11,545</td>
<td align="right">2.9%</td>
<td align="right">-40.6%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">109,556</td>
<td align="right">11.5%</td>
<td align="right">73,796</td>
<td align="right">18.4%</td>
<td align="right">-32.6%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">8,519</td>
<td align="right">0.9%</td>
<td align="right">6,189</td>
<td align="right">1.5%</td>
<td align="right">-27.4%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">7,717</td>
<td align="right">0.8%</td>
<td align="right">6,006</td>
<td align="right">1.5%</td>
<td align="right">-22.2%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">78,817</td>
<td align="right">8.3%</td>
<td align="right">62,836</td>
<td align="right">15.6%</td>
<td align="right">-20.3%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">46,907</td>
<td align="right">4.9%</td>
<td align="right">37,587</td>
<td align="right">9.4%</td>
<td align="right">-19.9%</td>
</tr>
<tr>
<td align="left">subscr other slice</td>
<td align="right">311</td>
<td align="right">0.0%</td>
<td align="right">273</td>
<td align="right">0.1%</td>
<td align="right">-12.2%</td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">2,216</td>
<td align="right">0.2%</td>
<td align="right">2,001</td>
<td align="right">0.5%</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">7,644</td>
<td align="right">0.8%</td>
<td align="right">6,959</td>
<td align="right">1.7%</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">subscr range</td>
<td align="right">3,163</td>
<td align="right">0.3%</td>
<td align="right">2,935</td>
<td align="right">0.7%</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">subscr deque</td>
<td align="right">98</td>
<td align="right">0.0%</td>
<td align="right">102</td>
<td align="right">0.0%</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">2,009</td>
<td align="right">0.2%</td>
<td align="right">1,961</td>
<td align="right">0.5%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">1,394</td>
<td align="right">0.1%</td>
<td align="right">1,363</td>
<td align="right">0.3%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">630</td>
<td align="right">0.1%</td>
<td align="right">628</td>
<td align="right">0.2%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">3,102</td>
<td align="right">0.3%</td>
<td align="right">3,100</td>
<td align="right">0.8%</td>
<td align="right">-0.1%</td>
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
<td align="right">525,661,645</td>
<td align="right">100.0%</td>
<td align="right">180,259,454</td>
<td align="right">100.0%</td>
<td align="right">-65.7%</td>
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
<td align="right">11,395,774,988</td>
<td align="right">98.3%</td>
<td align="right">4,721,346,174</td>
<td align="right">96.8%</td>
<td align="right">-58.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">199,890,030</td>
<td align="right">1.7%</td>
<td align="right">156,229,308</td>
<td align="right">3.2%</td>
<td align="right">-21.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">196,180,872</td>
<td align="right">1.7%</td>
<td align="right">153,344,163</td>
<td align="right">3.1%</td>
<td align="right">-21.8%</td>
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
<td align="right">3,932,912</td>
<td align="right">100.0%</td>
<td align="right">3,109,219</td>
<td align="right">100.0%</td>
<td align="right">-20.9%</td>
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
<td align="right">536,930</td>
<td align="right">96.6%</td>
<td align="right">536,740</td>
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
<td align="right">544,041</td>
<td align="right">97.9%</td>
<td align="right">543,849</td>
<td align="right">97.9%</td>
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
<td align="right">18,835</td>
<td align="right">100.0%</td>
<td align="right">18,877</td>
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
<td align="right">507,205,159</td>
<td align="right">9.9%</td>
<td align="right">94,035,137</td>
<td align="right">7.0%</td>
<td align="right">-81.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,628,342,599</td>
<td align="right">90.1%</td>
<td align="right">1,247,262,148</td>
<td align="right">92.9%</td>
<td align="right">-73.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,443,437</td>
<td align="right">0.0%</td>
<td align="right">1,316,446</td>
<td align="right">0.1%</td>
<td align="right">-8.8%</td>
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
<td align="right">214,229</td>
<td align="right">81.4%</td>
<td align="right">107,964</td>
<td align="right">69.9%</td>
<td align="right">-49.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">48,843</td>
<td align="right">18.6%</td>
<td align="right">46,416</td>
<td align="right">30.1%</td>
<td align="right">-5.0%</td>
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
<td align="right">84,968</td>
<td align="right">39.7%</td>
<td align="right">4,064</td>
<td align="right">3.8%</td>
<td align="right">-95.2%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">6,822</td>
<td align="right">3.2%</td>
<td align="right">361</td>
<td align="right">0.3%</td>
<td align="right">-94.7%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">10,899</td>
<td align="right">5.1%</td>
<td align="right">6,142</td>
<td align="right">5.7%</td>
<td align="right">-43.6%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">14,818</td>
<td align="right">6.9%</td>
<td align="right">8,941</td>
<td align="right">8.3%</td>
<td align="right">-39.7%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">932</td>
<td align="right">0.4%</td>
<td align="right">755</td>
<td align="right">0.7%</td>
<td align="right">-19.0%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">46,048</td>
<td align="right">21.5%</td>
<td align="right">38,697</td>
<td align="right">35.8%</td>
<td align="right">-16.0%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">184</td>
<td align="right">0.1%</td>
<td align="right">164</td>
<td align="right">0.2%</td>
<td align="right">-10.9%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">1,940</td>
<td align="right">0.9%</td>
<td align="right">1,863</td>
<td align="right">1.7%</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">7,807</td>
<td align="right">3.6%</td>
<td align="right">7,641</td>
<td align="right">7.1%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">30,689</td>
<td align="right">14.3%</td>
<td align="right">30,307</td>
<td align="right">28.1%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">7,773</td>
<td align="right">3.6%</td>
<td align="right">7,681</td>
<td align="right">7.1%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">1,349</td>
<td align="right">0.6%</td>
<td align="right">1,348</td>
<td align="right">1.2%</td>
<td align="right">-0.1%</td>
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
<td align="right">2,195,977,625</td>
<td align="right">91.4%</td>
<td align="right">459,243,876</td>
<td align="right">81.4%</td>
<td align="right">-79.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">205,873,599</td>
<td align="right">8.6%</td>
<td align="right">103,748,743</td>
<td align="right">18.4%</td>
<td align="right">-49.6%</td>
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
<td align="right">70,177</td>
<td align="right">71.3%</td>
<td align="right">44,321</td>
<td align="right">61.0%</td>
<td align="right">-36.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">28,317</td>
<td align="right">28.7%</td>
<td align="right">28,317</td>
<td align="right">39.0%</td>
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
<td align="right">24,184</td>
<td align="right">34.5%</td>
<td align="right">7,850</td>
<td align="right">17.7%</td>
<td align="right">-67.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">12,189</td>
<td align="right">17.4%</td>
<td align="right">8,946</td>
<td align="right">20.2%</td>
<td align="right">-26.6%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">23,213</td>
<td align="right">33.1%</td>
<td align="right">17,765</td>
<td align="right">40.1%</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">10,591</td>
<td align="right">15.1%</td>
<td align="right">9,760</td>
<td align="right">22.0%</td>
<td align="right">-7.8%</td>
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
<td align="right">1,507,794,927</td>
<td align="right">28.5%</td>
<td align="right">204,405,180</td>
<td align="right">13.5%</td>
<td align="right">-86.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">164,097,287</td>
<td align="right">3.1%</td>
<td align="right">44,203,914</td>
<td align="right">2.9%</td>
<td align="right">-73.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,614,333,737</td>
<td align="right">68.4%</td>
<td align="right">1,267,371,037</td>
<td align="right">83.6%</td>
<td align="right">-64.9%</td>
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
<td align="right">435,935</td>
<td align="right">12.3%</td>
<td align="right">104,581</td>
<td align="right">11.1%</td>
<td align="right">-76.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,101,767</td>
<td align="right">87.7%</td>
<td align="right">839,672</td>
<td align="right">88.9%</td>
<td align="right">-72.9%</td>
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
<td align="left">zip</td>
<td align="right">161,257</td>
<td align="right">37.0%</td>
<td align="right">4,094</td>
<td align="right">3.9%</td>
<td align="right">-97.5%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">83,646</td>
<td align="right">19.2%</td>
<td align="right">10,842</td>
<td align="right">10.4%</td>
<td align="right">-87.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">34,752</td>
<td align="right">8.0%</td>
<td align="right">5,486</td>
<td align="right">5.2%</td>
<td align="right">-84.2%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">16,123</td>
<td align="right">3.7%</td>
<td align="right">3,003</td>
<td align="right">2.9%</td>
<td align="right">-81.4%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">18,158</td>
<td align="right">4.2%</td>
<td align="right">4,077</td>
<td align="right">3.9%</td>
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
<td align="left">ascii string</td>
<td align="right">3,417</td>
<td align="right">0.8%</td>
<td align="right">1,215</td>
<td align="right">1.2%</td>
<td align="right">-64.4%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">11,768</td>
<td align="right">2.7%</td>
<td align="right">4,246</td>
<td align="right">4.1%</td>
<td align="right">-63.9%</td>
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
<td align="right">3,094</td>
<td align="right">0.7%</td>
<td align="right">1,911</td>
<td align="right">1.8%</td>
<td align="right">-38.2%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">72,953</td>
<td align="right">16.7%</td>
<td align="right">48,371</td>
<td align="right">46.3%</td>
<td align="right">-33.7%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">18,349</td>
<td align="right">4.2%</td>
<td align="right">12,351</td>
<td align="right">11.8%</td>
<td align="right">-32.7%</td>
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
<td align="left">dict values</td>
<td align="right">6,038</td>
<td align="right">1.4%</td>
<td align="right">4,720</td>
<td align="right">4.5%</td>
<td align="right">-21.8%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">4,325</td>
<td align="right">1.0%</td>
<td align="right">3,430</td>
<td align="right">3.3%</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">251</td>
<td align="right">0.1%</td>
<td align="right">212</td>
<td align="right">0.2%</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="left">tuple</td>
<td align="right">174,006,042</td>
<td align="right">174,006,042 / 0 !!</td>
<td align="right">122,517,831</td>
<td align="right">122,517,831 / 0 !!</td>
<td align="right">-29.6%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">5,473,118</td>
<td align="right">5,473,118 / 0 !!</td>
<td align="right">4,078,179</td>
<td align="right">4,078,179 / 0 !!</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">311,864,596</td>
<td align="right">311,864,596 / 0 !!</td>
<td align="right">255,217,032</td>
<td align="right">255,217,032 / 0 !!</td>
<td align="right">-18.2%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">101,651,085</td>
<td align="right">101,651,085 / 0 !!</td>
<td align="right">85,054,675</td>
<td align="right">85,054,675 / 0 !!</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">127,997,368</td>
<td align="right">127,997,368 / 0 !!</td>
<td align="right">119,987,101</td>
<td align="right">119,987,101 / 0 !!</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">12,580,898</td>
<td align="right">12,580,898 / 0 !!</td>
<td align="right">12,002,639</td>
<td align="right">12,002,639 / 0 !!</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">2,823,677</td>
<td align="right">2,823,677 / 0 !!</td>
<td align="right">2,734,441</td>
<td align="right">2,734,441 / 0 !!</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">34,932,334</td>
<td align="right">34,932,334 / 0 !!</td>
<td align="right">34,770,305</td>
<td align="right">34,770,305 / 0 !!</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">322,636,120</td>
<td align="right">322,636,120 / 0 !!</td>
<td align="right">322,207,480</td>
<td align="right">322,207,480 / 0 !!</td>
<td align="right">-0.1%</td>
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
<td align="right">12,719,258,987</td>
<td align="right">88.2%</td>
<td align="right">6,745,734,662</td>
<td align="right">87.0%</td>
<td align="right">-47.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">871,749,894</td>
<td align="right">6.0%</td>
<td align="right">502,655,251</td>
<td align="right">6.5%</td>
<td align="right">-42.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">823,954,809</td>
<td align="right">5.7%</td>
<td align="right">502,476,378</td>
<td align="right">6.5%</td>
<td align="right">-39.0%</td>
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
<td align="right">16,524,451</td>
<td align="right">97.0%</td>
<td align="right">9,590,028</td>
<td align="right">95.7%</td>
<td align="right">-42.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">506,648</td>
<td align="right">3.0%</td>
<td align="right">426,273</td>
<td align="right">4.3%</td>
<td align="right">-15.9%</td>
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
<td align="right">75,077</td>
<td align="right">14.8%</td>
<td align="right">36,375</td>
<td align="right">8.5%</td>
<td align="right">-51.5%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">1,060</td>
<td align="right">0.2%</td>
<td align="right">662</td>
<td align="right">0.2%</td>
<td align="right">-37.5%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">400</td>
<td align="right">0.1%</td>
<td align="right">260</td>
<td align="right">0.1%</td>
<td align="right">-35.0%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">57,976</td>
<td align="right">11.4%</td>
<td align="right">39,901</td>
<td align="right">9.4%</td>
<td align="right">-31.2%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">8,815</td>
<td align="right">1.7%</td>
<td align="right">6,343</td>
<td align="right">1.5%</td>
<td align="right">-28.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">6,006</td>
<td align="right">1.2%</td>
<td align="right">4,706</td>
<td align="right">1.1%</td>
<td align="right">-21.6%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">24,275</td>
<td align="right">4.8%</td>
<td align="right">19,301</td>
<td align="right">4.5%</td>
<td align="right">-20.5%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">823</td>
<td align="right">0.2%</td>
<td align="right">671</td>
<td align="right">0.2%</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">2,736</td>
<td align="right">0.5%</td>
<td align="right">2,374</td>
<td align="right">0.6%</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">53,113</td>
<td align="right">10.5%</td>
<td align="right">47,742</td>
<td align="right">11.2%</td>
<td align="right">-10.1%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">643</td>
<td align="right">0.1%</td>
<td align="right">603</td>
<td align="right">0.1%</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">17,124</td>
<td align="right">3.4%</td>
<td align="right">16,221</td>
<td align="right">3.8%</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1,713</td>
<td align="right">0.3%</td>
<td align="right">1,642</td>
<td align="right">0.4%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">47</td>
<td align="right">0.0%</td>
<td align="right">46</td>
<td align="right">0.0%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">4,411</td>
<td align="right">0.9%</td>
<td align="right">4,411</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
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
<td align="left">wrong number arguments</td>
<td align="right">200</td>
<td align="right">0.0%</td>
<td align="right">200</td>
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
<td align="right">9,422,519,032</td>
<td align="right">99.8%</td>
<td align="right">4,332,404,211</td>
<td align="right">99.7%</td>
<td align="right">-54.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">42,197</td>
<td align="right">0.0%</td>
<td align="right">41,575</td>
<td align="right">0.0%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">14,612,304</td>
<td align="right">0.2%</td>
<td align="right">14,612,537</td>
<td align="right">0.3%</td>
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
<td align="right">126,316</td>
<td align="right">100.0%</td>
<td align="right">126,561</td>
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
<td align="right">68,290,441</td>
<td align="right">100.0%</td>
<td align="right">62,877,529</td>
<td align="right">100.0%</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">110</td>
<td align="right">0.0%</td>
<td align="right">112</td>
<td align="right">0.0%</td>
<td align="right">1.8%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">27,457</td>
<td align="right">0.0%</td>
<td align="right">14,711</td>
<td align="right">0.0%</td>
<td align="right">-46.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">593,894,756</td>
<td align="right">82.2%</td>
<td align="right">593,215,700</td>
<td align="right">82.2%</td>
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
<td align="right">128,421,006</td>
<td align="right">17.8%</td>
<td align="right">128,391,290</td>
<td align="right">17.8%</td>
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
<td align="right">849</td>
<td align="right">2.4%</td>
<td align="right">616</td>
<td align="right">1.8%</td>
<td align="right">-27.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">35,199</td>
<td align="right">97.6%</td>
<td align="right">33,951</td>
<td align="right">98.2%</td>
<td align="right">-3.5%</td>
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
<td align="right">4,171</td>
<td align="right">11.8%</td>
<td align="right">2,923</td>
<td align="right">8.6%</td>
<td align="right">-29.9%</td>
</tr>
<tr>
<td align="left">async generator send</td>
<td align="right">24,440</td>
<td align="right">69.4%</td>
<td align="right">24,440</td>
<td align="right">72.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">5,948</td>
<td align="right">16.9%</td>
<td align="right">5,948</td>
<td align="right">17.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">640</td>
<td align="right">1.8%</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">115,527,763</td>
<td align="right">5.4%</td>
<td align="right">85,599,559</td>
<td align="right">5.1%</td>
<td align="right">-25.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">67,626,856</td>
<td align="right">3.2%</td>
<td align="right">51,916,680</td>
<td align="right">3.1%</td>
<td align="right">-23.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,936,888,032</td>
<td align="right">91.4%</td>
<td align="right">1,545,628,078</td>
<td align="right">91.8%</td>
<td align="right">-20.2%</td>
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
<td align="right">2,218,999</td>
<td align="right">98.0%</td>
<td align="right">1,654,478</td>
<td align="right">97.6%</td>
<td align="right">-25.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">45,755</td>
<td align="right">2.0%</td>
<td align="right">39,920</td>
<td align="right">2.4%</td>
<td align="right">-12.8%</td>
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
<td align="right">13.3%</td>
<td align="right">4,651</td>
<td align="right">11.7%</td>
<td align="right">-23.6%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">20,316</td>
<td align="right">44.4%</td>
<td align="right">16,035</td>
<td align="right">40.2%</td>
<td align="right">-21.1%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">749</td>
<td align="right">1.6%</td>
<td align="right">669</td>
<td align="right">1.7%</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">1,614</td>
<td align="right">3.5%</td>
<td align="right">1,514</td>
<td align="right">3.8%</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">2,962</td>
<td align="right">6.5%</td>
<td align="right">3,081</td>
<td align="right">7.7%</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">242,307</td>
<td align="right">529.6%</td>
<td align="right">235,600</td>
<td align="right">590.2%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">7,206</td>
<td align="right">15.7%</td>
<td align="right">7,166</td>
<td align="right">18.0%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">3,673</td>
<td align="right">8.0%</td>
<td align="right">3,673</td>
<td align="right">9.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">421</td>
<td align="right">0.9%</td>
<td align="right">421</td>
<td align="right">1.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">313</td>
<td align="right">0.7%</td>
<td align="right">313</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">101</td>
<td align="right">0.2%</td>
<td align="right">101</td>
<td align="right">0.3%</td>
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
<td align="right">112,725,129</td>
<td align="right">100.0%</td>
<td align="right">1,085,625</td>
<td align="right">100.0%</td>
<td align="right">-99.0%</td>
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
<td align="right">692,938,148</td>
<td align="right">42.6%</td>
<td align="right">101,317,058</td>
<td align="right">31.5%</td>
<td align="right">-85.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">935,073,590</td>
<td align="right">57.4%</td>
<td align="right">220,367,424</td>
<td align="right">68.5%</td>
<td align="right">-76.4%</td>
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
<td align="right">940</td>
<td align="right">0.0%</td>
<td align="right">-57.7%</td>
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
<td align="right">180,142</td>
<td align="right">98.4%</td>
<td align="right">34,792</td>
<td align="right">92.3%</td>
<td align="right">-80.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,962</td>
<td align="right">1.6%</td>
<td align="right">2,918</td>
<td align="right">7.7%</td>
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
<td align="left">other</td>
<td align="right">81,221</td>
<td align="right">45.1%</td>
<td align="right">320</td>
<td align="right">0.9%</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">5,259</td>
<td align="right">2.9%</td>
<td align="right">21</td>
<td align="right">0.1%</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">19,296</td>
<td align="right">10.7%</td>
<td align="right">3,283</td>
<td align="right">9.4%</td>
<td align="right">-83.0%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">52,368</td>
<td align="right">29.1%</td>
<td align="right">10,484</td>
<td align="right">30.1%</td>
<td align="right">-80.0%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">2,978</td>
<td align="right">1.7%</td>
<td align="right">2,499</td>
<td align="right">7.2%</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">1,673</td>
<td align="right">0.9%</td>
<td align="right">1,555</td>
<td align="right">4.5%</td>
<td align="right">-7.1%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">17,279</td>
<td align="right">9.6%</td>
<td align="right">16,562</td>
<td align="right">47.6%</td>
<td align="right">-4.1%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,844,897,394</td>
<td align="right">92.9%</td>
<td align="right">2,345,601,197</td>
<td align="right">92.3%</td>
<td align="right">-51.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">256,623,969</td>
<td align="right">4.9%</td>
<td align="right">132,247,032</td>
<td align="right">5.2%</td>
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
<td align="right">110,626,638</td>
<td align="right">2.1%</td>
<td align="right">62,661,568</td>
<td align="right">2.5%</td>
<td align="right">-43.4%</td>
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
<td align="right">2,135,431</td>
<td align="right">78.1%</td>
<td align="right">1,230,679</td>
<td align="right">73.9%</td>
<td align="right">-42.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">599,547</td>
<td align="right">21.9%</td>
<td align="right">434,135</td>
<td align="right">26.1%</td>
<td align="right">-27.6%</td>
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
<td align="right">2.7%</td>
<td align="right">1,818</td>
<td align="right">0.4%</td>
<td align="right">-88.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">126,941</td>
<td align="right">21.2%</td>
<td align="right">67,399</td>
<td align="right">15.5%</td>
<td align="right">-46.9%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">16,272</td>
<td align="right">2.7%</td>
<td align="right">10,498</td>
<td align="right">2.4%</td>
<td align="right">-35.5%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">85,804</td>
<td align="right">14.3%</td>
<td align="right">55,735</td>
<td align="right">12.8%</td>
<td align="right">-35.0%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">263,052</td>
<td align="right">43.9%</td>
<td align="right">208,600</td>
<td align="right">48.0%</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">9,778</td>
<td align="right">1.6%</td>
<td align="right">9,489</td>
<td align="right">2.2%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">71,756</td>
<td align="right">12.0%</td>
<td align="right">70,678</td>
<td align="right">16.3%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">9,460</td>
<td align="right">1.6%</td>
<td align="right">9,452</td>
<td align="right">2.2%</td>
<td align="right">-0.1%</td>
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
<td align="right">1,246,705,091</td>
<td align="right">99.9%</td>
<td align="right">518,935,211</td>
<td align="right">99.8%</td>
<td align="right">-58.4%</td>
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
<td align="right">2,040</td>
<td align="right">0.0%</td>
<td align="right">-44.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,571,300</td>
<td align="right">0.1%</td>
<td align="right">1,204,442</td>
<td align="right">0.2%</td>
<td align="right">-23.3%</td>
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
<td align="right">864</td>
<td align="right">8.1%</td>
<td align="right">741</td>
<td align="right">7.1%</td>
<td align="right">-14.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">9,794</td>
<td align="right">91.9%</td>
<td align="right">9,747</td>
<td align="right">92.9%</td>
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
<td align="left">sequence</td>
<td align="right">633</td>
<td align="right">73.3%</td>
<td align="right">510</td>
<td align="right">68.8%</td>
<td align="right">-19.4%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">132</td>
<td align="right">15.3%</td>
<td align="right">132</td>
<td align="right">17.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">99</td>
<td align="right">11.5%</td>
<td align="right">99</td>
<td align="right">13.4%</td>
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
<td align="right">8,462,109,801</td>
<td align="right">3.9%</td>
<td align="right">3,024,948,038</td>
<td align="right">3.3%</td>
<td align="right">-64.3%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">80,863,207,379</td>
<td align="right">37.5%</td>
<td align="right">34,024,461,206</td>
<td align="right">36.7%</td>
<td align="right">-57.9%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">124,858,819,844</td>
<td align="right">57.9%</td>
<td align="right">54,763,349,983</td>
<td align="right">59.1%</td>
<td align="right">-56.1%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,527,911,610</td>
<td align="right">0.7%</td>
<td align="right">907,012,538</td>
<td align="right">1.0%</td>
<td align="right">-40.6%</td>
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
<td align="right">1,507,794,927</td>
<td align="right">19.9%</td>
<td align="right">204,405,180</td>
<td align="right">7.7%</td>
<td align="right">-86.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">692,938,148</td>
<td align="right">9.2%</td>
<td align="right">101,317,058</td>
<td align="right">3.8%</td>
<td align="right">-85.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">507,205,159</td>
<td align="right">6.7%</td>
<td align="right">94,035,137</td>
<td align="right">3.5%</td>
<td align="right">-81.5%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">525,661,645</td>
<td align="right">7.0%</td>
<td align="right">180,259,454</td>
<td align="right">6.8%</td>
<td align="right">-65.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,517,549,274</td>
<td align="right">33.3%</td>
<td align="right">998,994,870</td>
<td align="right">37.4%</td>
<td align="right">-60.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">205,873,599</td>
<td align="right">2.7%</td>
<td align="right">103,748,743</td>
<td align="right">3.9%</td>
<td align="right">-49.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">256,623,969</td>
<td align="right">3.4%</td>
<td align="right">132,247,032</td>
<td align="right">5.0%</td>
<td align="right">-48.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">823,954,809</td>
<td align="right">10.9%</td>
<td align="right">502,476,378</td>
<td align="right">18.8%</td>
<td align="right">-39.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">196,180,872</td>
<td align="right">2.6%</td>
<td align="right">153,344,163</td>
<td align="right">5.7%</td>
<td align="right">-21.8%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,421,006</td>
<td align="right">1.7%</td>
<td align="right">128,391,290</td>
<td align="right">4.8%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">369,060,247</td>
<td align="right">24.2%</td>
<td align="right">180,347,218</td>
<td align="right">19.9%</td>
<td align="right">-51.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">268,697,696</td>
<td align="right">17.6%</td>
<td align="right">140,186,685</td>
<td align="right">15.5%</td>
<td align="right">-47.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">54,659,346</td>
<td align="right">3.6%</td>
<td align="right">29,847,068</td>
<td align="right">3.3%</td>
<td align="right">-45.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">49,067,226</td>
<td align="right">3.2%</td>
<td align="right">26,955,038</td>
<td align="right">3.0%</td>
<td align="right">-45.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">84,992,108</td>
<td align="right">5.6%</td>
<td align="right">53,620,198</td>
<td align="right">5.9%</td>
<td align="right">-36.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">95,065,930</td>
<td align="right">6.2%</td>
<td align="right">65,804,377</td>
<td align="right">7.3%</td>
<td align="right">-30.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">82,722,493</td>
<td align="right">5.4%</td>
<td align="right">59,861,341</td>
<td align="right">6.6%</td>
<td align="right">-27.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">92,068,542</td>
<td align="right">6.0%</td>
<td align="right">72,565,683</td>
<td align="right">8.0%</td>
<td align="right">-21.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">82,057,660</td>
<td align="right">5.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">81,912,853</td>
<td align="right">5.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">24,850,030</td>
<td align="right">2.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">22,172,033</td>
<td align="right">2.4%</td>
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
<td align="left">Frames pushed</td>
<td align="right">5,687,493,681</td>
<td align="right">81.4%</td>
<td align="right">4,715,085,664</td>
<td align="right">77.7%</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">273,093,673</td>
<td align="right">3.9%</td>
<td align="right">228,600,720</td>
<td align="right">3.8%</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">5,353,795,811</td>
<td align="right">76.6%</td>
<td align="right">4,570,275,958</td>
<td align="right">75.3%</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,016,856,670</td>
<td align="right">14.5%</td>
<td align="right">883,830,923</td>
<td align="right">14.6%</td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,021,133,337</td>
<td align="right">14.6%</td>
<td align="right">888,105,270</td>
<td align="right">14.6%</td>
<td align="right">-13.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">261,178,202</td>
<td align="right">3.7%</td>
<td align="right">229,639,380</td>
<td align="right">3.8%</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">71,263,033</td>
<td align="right">1.0%</td>
<td align="right">64,558,919</td>
<td align="right">1.1%</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">1,635,494,095</td>
<td align="right">23.4%</td>
<td align="right">1,501,847,044</td>
<td align="right">24.7%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">1,635,494,095</td>
<td align="right">23.4%</td>
<td align="right">1,501,847,044</td>
<td align="right">24.7%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">141,112,765</td>
<td align="right">2.0%</td>
<td align="right">132,513,832</td>
<td align="right">2.2%</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">24,608,223</td>
<td align="right">0.4%</td>
<td align="right">23,644,624</td>
<td align="right">0.4%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">3,372</td>
<td align="right">0.0%</td>
<td align="right">3,332</td>
<td align="right">0.0%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">614,360,758</td>
<td align="right">8.8%</td>
<td align="right">613,741,774</td>
<td align="right">10.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">4,273,295</td>
<td align="right">0.1%</td>
<td align="right">4,271,015</td>
<td align="right">0.1%</td>
<td align="right">-0.1%</td>
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
<td align="left">Method cache misses</td>
<td align="right">56,920,771</td>
<td align="right"></td>
<td align="right">40,477,893</td>
<td align="right"></td>
<td align="right">-28.9%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">63,251,468</td>
<td align="right"></td>
<td align="right">45,443,091</td>
<td align="right"></td>
<td align="right">-28.2%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">2,451,257,254</td>
<td align="right"></td>
<td align="right">1,779,488,623</td>
<td align="right"></td>
<td align="right">-27.4%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">7,136,121</td>
<td align="right"></td>
<td align="right">5,226,145</td>
<td align="right"></td>
<td align="right">-26.8%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">2,444,217,294</td>
<td align="right"></td>
<td align="right">1,843,185,665</td>
<td align="right"></td>
<td align="right">-24.6%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">6,192,706,158</td>
<td align="right"></td>
<td align="right">5,241,180,722</td>
<td align="right"></td>
<td align="right">-15.4%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">306,669</td>
<td align="right">0.2%</td>
<td align="right">259,969</td>
<td align="right">0.1%</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">5,531,774,181</td>
<td align="right">28.5%</td>
<td align="right">4,695,543,558</td>
<td align="right">27.0%</td>
<td align="right">-15.1%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">5,610,000,032</td>
<td align="right">28.9%</td>
<td align="right">4,773,388,202</td>
<td align="right">27.4%</td>
<td align="right">-14.9%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">25,087,147,989</td>
<td align="right">26.9%</td>
<td align="right">21,837,624,032</td>
<td align="right">26.5%</td>
<td align="right">-13.0%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">31,869,752,528</td>
<td align="right">28.9%</td>
<td align="right">28,135,263,089</td>
<td align="right">28.6%</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">51,477,353,718</td>
<td align="right">46.7%</td>
<td align="right">45,537,408,531</td>
<td align="right">46.2%</td>
<td align="right">-11.5%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">23,138,562,305</td>
<td align="right">24.8%</td>
<td align="right">20,511,065,663</td>
<td align="right">24.9%</td>
<td align="right">-11.4%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">40,166,107,153</td>
<td align="right">43.1%</td>
<td align="right">35,705,956,982</td>
<td align="right">43.3%</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">13,807,853,667</td>
<td align="right">71.1%</td>
<td align="right">12,636,787,775</td>
<td align="right">72.6%</td>
<td align="right">-8.5%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">13,808,046,273</td>
<td align="right"></td>
<td align="right">12,636,975,507</td>
<td align="right"></td>
<td align="right">-8.5%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">25,041,960,831</td>
<td align="right">22.7%</td>
<td align="right">22,951,008,220</td>
<td align="right">23.3%</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">4,758,231,006</td>
<td align="right">5.1%</td>
<td align="right">4,387,768,039</td>
<td align="right">5.3%</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">1,945,510,066</td>
<td align="right">1.8%</td>
<td align="right">1,846,002,758</td>
<td align="right">1.9%</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">190,879,833</td>
<td align="right"></td>
<td align="right">184,360,638</td>
<td align="right"></td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">6,700,904</td>
<td align="right">0.0%</td>
<td align="right">6,552,558</td>
<td align="right">0.0%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">71,524,947</td>
<td align="right">0.4%</td>
<td align="right">71,292,086</td>
<td align="right">0.4%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">3,386,403</td>
<td align="right">1.8%</td>
<td align="right">3,386,403</td>
<td align="right">1.8%</td>
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
<td align="right">359,169</td>
<td align="right">104,364,419</td>
<td align="right">9,626,275,968</td>
<td align="right">782,383,440</td>
<td align="right">756,389,122</td>
<td align="right">347,366</td>
<td align="right">73,360,954</td>
<td align="right">9,147,649,264</td>
<td align="right">772,819,793</td>
<td align="right">709,844,856</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">15,998</td>
<td align="right">8,734,500</td>
<td align="right">11,359,129,076</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">15,998</td>
<td align="right">8,734,500</td>
<td align="right">11,359,600,308</td>
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
<td align="right">2,416</td>
<td align="right">-0.8%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-06-02
