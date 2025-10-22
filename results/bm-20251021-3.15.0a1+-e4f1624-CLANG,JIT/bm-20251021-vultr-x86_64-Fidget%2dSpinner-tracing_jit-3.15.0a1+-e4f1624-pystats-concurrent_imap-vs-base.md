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
<td align="right">914,440</td>
<td align="right">2,689,248</td>
<td align="right">194.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">9,731,758</td>
<td align="right">81,150</td>
<td align="right">-99.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">9,815,287</td>
<td align="right">235,755</td>
<td align="right">-97.6%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">22,666,824</td>
<td align="right">934,632</td>
<td align="right">-95.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">10,141,960</td>
<td align="right">601,999</td>
<td align="right">-94.1%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">892,975</td>
<td align="right">65,171</td>
<td align="right">-92.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">10,598,776</td>
<td align="right">1,019,204</td>
<td align="right">-90.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,891,881</td>
<td align="right">236,016</td>
<td align="right">-87.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,924,937</td>
<td align="right">256,715</td>
<td align="right">-86.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">982,136</td>
<td align="right">134,806</td>
<td align="right">-86.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,127,961</td>
<td align="right">279,351</td>
<td align="right">-75.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,148,581</td>
<td align="right">298,070</td>
<td align="right">-74.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">1,063,805</td>
<td align="right">294,537</td>
<td align="right">-72.3%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">1,174,560</td>
<td align="right">383,382</td>
<td align="right">-67.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">32,464</td>
<td align="right">53,714</td>
<td align="right">65.5%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">1,209,593</td>
<td align="right">460,278</td>
<td align="right">-61.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,229,738</td>
<td align="right">488,293</td>
<td align="right">-60.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">9,540,693</td>
<td align="right">4,091,305</td>
<td align="right">-57.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">2,969,995</td>
<td align="right">1,357,839</td>
<td align="right">-54.3%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">7,606,069</td>
<td align="right">3,625,292</td>
<td align="right">-52.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">21,738,983</td>
<td align="right">10,706,957</td>
<td align="right">-50.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">24,160,600</td>
<td align="right">12,522,057</td>
<td align="right">-48.2%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">31,831</td>
<td align="right">46,129</td>
<td align="right">44.9%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">1,880,107</td>
<td align="right">1,074,772</td>
<td align="right">-42.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">1,982,151</td>
<td align="right">1,134,388</td>
<td align="right">-42.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">17,805,690</td>
<td align="right">10,366,475</td>
<td align="right">-41.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">107,445</td>
<td align="right">149,843</td>
<td align="right">39.5%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">10,516,423</td>
<td align="right">6,427,689</td>
<td align="right">-38.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">8,078,453</td>
<td align="right">5,008,954</td>
<td align="right">-38.0%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">4,352,860</td>
<td align="right">2,714,880</td>
<td align="right">-37.6%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">31,219,708</td>
<td align="right">19,569,170</td>
<td align="right">-37.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">1,964,444</td>
<td align="right">1,231,724</td>
<td align="right">-37.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">4,517,525</td>
<td align="right">2,864,916</td>
<td align="right">-36.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,159,859</td>
<td align="right">1,379,332</td>
<td align="right">-36.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">635,729</td>
<td align="right">862,399</td>
<td align="right">35.7%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">4,123,549</td>
<td align="right">2,657,097</td>
<td align="right">-35.6%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">4,678,167</td>
<td align="right">3,096,000</td>
<td align="right">-33.8%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">4,890,100</td>
<td align="right">3,323,611</td>
<td align="right">-32.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">490,274</td>
<td align="right">647,276</td>
<td align="right">32.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">192,446</td>
<td align="right">251,167</td>
<td align="right">30.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">2,449,544</td>
<td align="right">1,708,119</td>
<td align="right">-30.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">48,462</td>
<td align="right">62,760</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">243,869</td>
<td align="right">314,800</td>
<td align="right">29.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">2,918,103</td>
<td align="right">2,130,865</td>
<td align="right">-27.0%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">170,499</td>
<td align="right">215,064</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">8,125,102</td>
<td align="right">6,024,676</td>
<td align="right">-25.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">231,619</td>
<td align="right">286,837</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">3,482,540</td>
<td align="right">2,660,424</td>
<td align="right">-23.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">5,899,000</td>
<td align="right">4,522,846</td>
<td align="right">-23.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">55,749,711</td>
<td align="right">43,175,423</td>
<td align="right">-22.6%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">144,005</td>
<td align="right">174,382</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">292,120</td>
<td align="right">350,841</td>
<td align="right">20.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">358,914</td>
<td align="right">428,964</td>
<td align="right">19.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">115,211</td>
<td align="right">136,548</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">3,530,917</td>
<td align="right">2,889,440</td>
<td align="right">-18.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">4,473,697</td>
<td align="right">3,666,278</td>
<td align="right">-18.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">39,678</td>
<td align="right">46,749</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">127,349</td>
<td align="right">148,801</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">369,617</td>
<td align="right">428,338</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">135,089</td>
<td align="right">156,519</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">181,122</td>
<td align="right">209,566</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">3,797,606</td>
<td align="right">3,209,810</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">4,583,778</td>
<td align="right">3,933,964</td>
<td align="right">-14.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">15,676,675</td>
<td align="right">13,475,471</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">106,192</td>
<td align="right">120,246</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">108,304</td>
<td align="right">122,358</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">168,176</td>
<td align="right">189,731</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">718,507</td>
<td align="right">807,321</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">61,795</td>
<td align="right">68,889</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">64,901</td>
<td align="right">71,994</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">82,454</td>
<td align="right">89,603</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">8,710,578</td>
<td align="right">7,959,766</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">448,190</td>
<td align="right">485,575</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">12,357</td>
<td align="right">11,352</td>
<td align="right">-8.1%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">162,805</td>
<td align="right">175,909</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">395,224</td>
<td align="right">366,929</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">482,169</td>
<td align="right">449,546</td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">128,507</td>
<td align="right">135,596</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">549,446</td>
<td align="right">519,401</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">2,512,004</td>
<td align="right">2,625,794</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">3,417</td>
<td align="right">3,269</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">2,443,775</td>
<td align="right">2,545,547</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">1,020,358</td>
<td align="right">1,058,656</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">786,034</td>
<td align="right">813,972</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">954,948</td>
<td align="right">927,018</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">901,820</td>
<td align="right">922,955</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">939,067</td>
<td align="right">960,257</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,768,690</td>
<td align="right">2,824,123</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">20,742,569</td>
<td align="right">20,352,167</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">70,990</td>
<td align="right">69,985</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">520,794</td>
<td align="right">527,828</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">79,821</td>
<td align="right">78,816</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">79,821</td>
<td align="right">78,816</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">83</td>
<td align="right">84</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">11,153,088</td>
<td align="right">11,273,863</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">2,543</td>
<td align="right">2,562</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">1,695</td>
<td align="right">1,689</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">337,456</td>
<td align="right">336,341</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">71,735</td>
<td align="right">71,587</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">80,660</td>
<td align="right">80,702</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">80,660</td>
<td align="right">80,702</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">406,493</td>
<td align="right">406,349</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">122,143</td>
<td align="right">122,185</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">45,451</td>
<td align="right">45,459</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">132,462</td>
<td align="right">132,468</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">214,104</td>
<td align="right">214,112</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">141,314</td>
<td align="right">141,318</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">3,766,159</td>
<td align="right">3,766,099</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">119,914</td>
<td align="right">119,915</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">155,370</td>
<td align="right">155,371</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">215,864</td>
<td align="right">215,864</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">215,834</td>
<td align="right">215,834</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">200,831</td>
<td align="right">200,831</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">177,776</td>
<td align="right">177,776</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">169,708</td>
<td align="right">169,708</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">122,039</td>
<td align="right">122,039</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">122,035</td>
<td align="right">122,035</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">102,271</td>
<td align="right">102,271</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">100,846</td>
<td align="right">100,846</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">90,616</td>
<td align="right">90,616</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">89,895</td>
<td align="right">89,895</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">83,060</td>
<td align="right">83,060</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">73,364</td>
<td align="right">73,364</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">60,027</td>
<td align="right">60,027</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">47,636</td>
<td align="right">47,636</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">43,132</td>
<td align="right">43,132</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">39,420</td>
<td align="right">39,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">38,933</td>
<td align="right">38,933</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">37,819</td>
<td align="right">37,819</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">33,036</td>
<td align="right">33,036</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">27,557</td>
<td align="right">27,557</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">26,496</td>
<td align="right">26,496</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">17,704</td>
<td align="right">17,704</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">17,662</td>
<td align="right">17,662</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">16,557</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">8,835</td>
<td align="right">8,835</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">8,831</td>
<td align="right">8,831</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">2,283</td>
<td align="right">2,283</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">2,175</td>
<td align="right">2,175</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">2,110</td>
<td align="right">2,110</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">1,049</td>
<td align="right">1,049</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">1,025</td>
<td align="right">1,025</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">1,024</td>
<td align="right">1,024</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">795</td>
<td align="right">795</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">504</td>
<td align="right">504</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">439</td>
<td align="right">439</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">207</td>
<td align="right">207</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">107</td>
<td align="right">107</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">81</td>
<td align="right">81</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">42</td>
<td align="right">42</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">38</td>
<td align="right">38</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">28</td>
<td align="right">28</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">27</td>
<td align="right">27</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">15</td>
<td align="right">15</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">12</td>
<td align="right">12</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">6</td>
<td align="right">6</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">4</td>
<td align="right">4</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">3</td>
<td align="right">3</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">1</td>
<td align="right">1</td>
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
<td align="right">11,489</td>
<td align="right">0.2%</td>
<td align="right">21,034</td>
<td align="right">0.5%</td>
<td align="right">83.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,126,712</td>
<td align="right">24.1%</td>
<td align="right">278,289</td>
<td align="right">6.7%</td>
<td align="right">-75.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,538,766</td>
<td align="right">75.6%</td>
<td align="right">3,876,770</td>
<td align="right">92.8%</td>
<td align="right">9.6%</td>
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
<td align="right">376</td>
<td align="right">25.6%</td>
<td align="right">558</td>
<td align="right">38.3%</td>
<td align="right">48.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,091</td>
<td align="right">74.4%</td>
<td align="right">900</td>
<td align="right">61.7%</td>
<td align="right">-17.5%</td>
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
<td align="right">255</td>
<td align="right">23.4%</td>
<td align="right">62</td>
<td align="right">6.9%</td>
<td align="right">-75.7%</td>
</tr>
<tr>
<td align="left">subscr deque</td>
<td align="right">96</td>
<td align="right">8.8%</td>
<td align="right">94</td>
<td align="right">10.4%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">402</td>
<td align="right">36.8%</td>
<td align="right">406</td>
<td align="right">45.1%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">194</td>
<td align="right">17.8%</td>
<td align="right">194</td>
<td align="right">21.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">135</td>
<td align="right">12.4%</td>
<td align="right">135</td>
<td align="right">15.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">4</td>
<td align="right">0.4%</td>
<td align="right">4</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr bytes</td>
<td align="right">4</td>
<td align="right">0.4%</td>
<td align="right">4</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr other slice</td>
<td align="right">1</td>
<td align="right">0.1%</td>
<td align="right">1</td>
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
<td align="right">37,819</td>
<td align="right">100.0%</td>
<td align="right">37,819</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">18,562,461</td>
<td align="right">100.0%</td>
<td align="right">19,200,799</td>
<td align="right">100.0%</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">7,405</td>
<td align="right">0.0%</td>
<td align="right">7,418</td>
<td align="right">0.0%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">6,450</td>
<td align="right">0.0%</td>
<td align="right">6,450</td>
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
<td align="right">1,588</td>
<td align="right">100.0%</td>
<td align="right">1,594</td>
<td align="right">100.0%</td>
<td align="right">0.4%</td>
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
<td align="right">42</td>
<td align="right">51.9%</td>
<td align="right">42</td>
<td align="right">51.9%</td>
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
<td align="right">39</td>
<td align="right">100.0%</td>
<td align="right">39</td>
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
<td align="right">17,435</td>
<td align="right">0.3%</td>
<td align="right">24,549</td>
<td align="right">0.5%</td>
<td align="right">40.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">167,203</td>
<td align="right">3.3%</td>
<td align="right">188,611</td>
<td align="right">3.6%</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,939,150</td>
<td align="right">96.4%</td>
<td align="right">5,021,655</td>
<td align="right">95.9%</td>
<td align="right">1.7%</td>
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
<td align="right">463</td>
<td align="right">36.0%</td>
<td align="right">596</td>
<td align="right">38.0%</td>
<td align="right">28.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">822</td>
<td align="right">64.0%</td>
<td align="right">973</td>
<td align="right">62.0%</td>
<td align="right">18.4%</td>
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
<td align="left">float long</td>
<td align="right">357</td>
<td align="right">43.4%</td>
<td align="right">504</td>
<td align="right">51.8%</td>
<td align="right">41.2%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">274</td>
<td align="right">33.3%</td>
<td align="right">278</td>
<td align="right">28.6%</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">100</td>
<td align="right">12.2%</td>
<td align="right">100</td>
<td align="right">10.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">91</td>
<td align="right">11.1%</td>
<td align="right">91</td>
<td align="right">9.4%</td>
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
<td align="right">978,869</td>
<td align="right">99.8%</td>
<td align="right">1,028,654</td>
<td align="right">99.8%</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,057</td>
<td align="right">0.2%</td>
<td align="right">2,057</td>
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
<td align="left">Success</td>
<td align="right">7</td>
<td align="right">13.2%</td>
<td align="right">7</td>
<td align="right">13.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">46</td>
<td align="right">86.8%</td>
<td align="right">46</td>
<td align="right">86.8%</td>
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
<td align="right">46</td>
<td align="right">100.0%</td>
<td align="right">46</td>
<td align="right">100.0%</td>
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
<td align="right">1,891,147</td>
<td align="right">8.6%</td>
<td align="right">235,604</td>
<td align="right">2.2%</td>
<td align="right">-87.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">20,040,000</td>
<td align="right">91.4%</td>
<td align="right">10,521,491</td>
<td align="right">97.8%</td>
<td align="right">-47.5%</td>
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
<td align="right">696</td>
<td align="right">94.8%</td>
<td align="right">374</td>
<td align="right">90.8%</td>
<td align="right">-46.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">38</td>
<td align="right">5.2%</td>
<td align="right">38</td>
<td align="right">9.2%</td>
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
<td align="left">itertools</td>
<td align="right">80</td>
<td align="right">11.5%</td>
<td align="right">143</td>
<td align="right">38.2%</td>
<td align="right">78.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">255</td>
<td align="right">36.6%</td>
<td align="right">62</td>
<td align="right">16.6%</td>
<td align="right">-75.7%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">255</td>
<td align="right">36.6%</td>
<td align="right">63</td>
<td align="right">16.8%</td>
<td align="right">-75.3%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">94</td>
<td align="right">13.5%</td>
<td align="right">94</td>
<td align="right">25.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">5</td>
<td align="right">0.7%</td>
<td align="right">5</td>
<td align="right">1.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">4</td>
<td align="right">0.6%</td>
<td align="right">4</td>
<td align="right">1.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">2</td>
<td align="right">0.3%</td>
<td align="right">2</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">1</td>
<td align="right">0.1%</td>
<td align="right">1</td>
<td align="right">0.3%</td>
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
<td align="left">self</td>
<td align="right">43,935</td>
<td align="right">43,935 / 0 !!</td>
<td align="right">51,084</td>
<td align="right">51,084 / 0 !!</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">1,094,066</td>
<td align="right">1,094,066 / 0 !!</td>
<td align="right">1,164,997</td>
<td align="right">1,164,997 / 0 !!</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">46,346</td>
<td align="right">46,346 / 0 !!</td>
<td align="right">46,346</td>
<td align="right">46,346 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">18,863</td>
<td align="right">18,863 / 0 !!</td>
<td align="right">18,863</td>
<td align="right">18,863 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">17,662</td>
<td align="right">17,662 / 0 !!</td>
<td align="right">17,662</td>
<td align="right">17,662 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">8,831</td>
<td align="right">8,831 / 0 !!</td>
<td align="right">8,831</td>
<td align="right">8,831 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">31</td>
<td align="right">31 / 0 !!</td>
<td align="right">31</td>
<td align="right">31 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">4</td>
<td align="right">4 / 0 !!</td>
<td align="right">4</td>
<td align="right">4 / 0 !!</td>
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
<td align="right">6</td>
<td align="right">0.0%</td>
<td align="right">27</td>
<td align="right">0.0%</td>
<td align="right">350.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">3,789,061</td>
<td align="right">9.8%</td>
<td align="right">3,201,497</td>
<td align="right">8.6%</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">857,275</td>
<td align="right">2.2%</td>
<td align="right">825,015</td>
<td align="right">2.2%</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">34,018,811</td>
<td align="right">88.0%</td>
<td align="right">33,237,880</td>
<td align="right">89.2%</td>
<td align="right">-2.3%</td>
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
<td align="right">7,034</td>
<td align="right">28.2%</td>
<td align="right">6,798</td>
<td align="right">28.2%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">17,897</td>
<td align="right">71.8%</td>
<td align="right">17,325</td>
<td align="right">71.8%</td>
<td align="right">-3.2%</td>
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
<td align="right">2,016</td>
<td align="right">28.7%</td>
<td align="right">1,815</td>
<td align="right">26.7%</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">879</td>
<td align="right">12.5%</td>
<td align="right">843</td>
<td align="right">12.4%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">938</td>
<td align="right">13.3%</td>
<td align="right">963</td>
<td align="right">14.2%</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">755</td>
<td align="right">10.7%</td>
<td align="right">755</td>
<td align="right">11.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">568</td>
<td align="right">8.1%</td>
<td align="right">568</td>
<td align="right">8.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">95</td>
<td align="right">1.4%</td>
<td align="right">95</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">92</td>
<td align="right">1.3%</td>
<td align="right">92</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">91</td>
<td align="right">1.3%</td>
<td align="right">91</td>
<td align="right">1.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">46</td>
<td align="right">0.7%</td>
<td align="right">46</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
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
<td align="right">12,708,659</td>
<td align="right">100.0%</td>
<td align="right">10,834,062</td>
<td align="right">100.0%</td>
<td align="right">-14.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">776</td>
<td align="right">0.0%</td>
<td align="right">781</td>
<td align="right">0.0%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4</td>
<td align="right">0.0%</td>
<td align="right">4</td>
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
<td align="right">221</td>
<td align="right">0.0%</td>
<td align="right">221</td>
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
<td align="right">926</td>
<td align="right">100.0%</td>
<td align="right">915</td>
<td align="right">100.0%</td>
<td align="right">-1.2%</td>
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
<td align="right">286,063</td>
<td align="right">100.0%</td>
<td align="right">364,192</td>
<td align="right">100.0%</td>
<td align="right">27.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">13</td>
<td align="right">0.0%</td>
<td align="right">13</td>
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
<td align="right">15</td>
<td align="right">100.0%</td>
<td align="right">15</td>
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
<td align="right">3,030,149</td>
<td align="right">85.0%</td>
<td align="right">3,171,865</td>
<td align="right">85.6%</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">212,931</td>
<td align="right">6.0%</td>
<td align="right">212,935</td>
<td align="right">5.7%</td>
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
<td align="right">319,503</td>
<td align="right">9.0%</td>
<td align="right">319,503</td>
<td align="right">8.6%</td>
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
<td align="right">6,437</td>
<td align="right">87.2%</td>
<td align="right">6,441</td>
<td align="right">87.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">949</td>
<td align="right">12.8%</td>
<td align="right">949</td>
<td align="right">12.8%</td>
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
<td align="right">849</td>
<td align="right">89.5%</td>
<td align="right">832</td>
<td align="right">87.7%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">464</td>
<td align="right">48.9%</td>
<td align="right">464</td>
<td align="right">48.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">236</td>
<td align="right">24.9%</td>
<td align="right">236</td>
<td align="right">24.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">90</td>
<td align="right">9.5%</td>
<td align="right">90</td>
<td align="right">9.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">11</td>
<td align="right">1.2%</td>
<td align="right">11</td>
<td align="right">1.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">2</td>
<td align="right">0.2%</td>
<td align="right">2</td>
<td align="right">0.2%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,064,804</td>
<td align="right">95.9%</td>
<td align="right">1,115,537</td>
<td align="right">96.1%</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">45,201</td>
<td align="right">4.1%</td>
<td align="right">45,205</td>
<td align="right">3.9%</td>
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
<td align="right">14</td>
<td align="right">5.6%</td>
<td align="right">18</td>
<td align="right">7.1%</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">236</td>
<td align="right">94.4%</td>
<td align="right">236</td>
<td align="right">92.9%</td>
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
<td align="right">144</td>
<td align="right">61.0%</td>
<td align="right">144</td>
<td align="right">61.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">92</td>
<td align="right">39.0%</td>
<td align="right">92</td>
<td align="right">39.0%</td>
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
<td align="right">1,147,258</td>
<td align="right">23.1%</td>
<td align="right">296,940</td>
<td align="right">6.6%</td>
<td align="right">-74.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,828,510</td>
<td align="right">76.9%</td>
<td align="right">4,194,827</td>
<td align="right">93.4%</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">28</td>
<td align="right">0.0%</td>
<td align="right">28</td>
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
<td align="right">1,099</td>
<td align="right">83.1%</td>
<td align="right">900</td>
<td align="right">79.6%</td>
<td align="right">-18.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">224</td>
<td align="right">16.9%</td>
<td align="right">230</td>
<td align="right">20.4%</td>
<td align="right">2.7%</td>
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
<td align="right">347</td>
<td align="right">31.6%</td>
<td align="right">154</td>
<td align="right">17.1%</td>
<td align="right">-55.6%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">378</td>
<td align="right">34.4%</td>
<td align="right">371</td>
<td align="right">41.2%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">144</td>
<td align="right">13.1%</td>
<td align="right">145</td>
<td align="right">16.1%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">138</td>
<td align="right">12.6%</td>
<td align="right">138</td>
<td align="right">15.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">memory view</td>
<td align="right">47</td>
<td align="right">4.3%</td>
<td align="right">47</td>
<td align="right">5.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">45</td>
<td align="right">4.1%</td>
<td align="right">45</td>
<td align="right">5.0%</td>
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
<td align="right">3,673,490</td>
<td align="right">100.0%</td>
<td align="right">3,687,623</td>
<td align="right">100.0%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">37</td>
<td align="right">0.0%</td>
<td align="right">37</td>
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
<td align="right">70</td>
<td align="right">100.0%</td>
<td align="right">70</td>
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
<td align="right">156,956,499</td>
<td align="right">37.3%</td>
<td align="right">81,072,091</td>
<td align="right">31.4%</td>
<td align="right">-48.3%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">9,667,881</td>
<td align="right">2.3%</td>
<td align="right">5,005,238</td>
<td align="right">1.9%</td>
<td align="right">-48.2%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">252,553,025</td>
<td align="right">60.1%</td>
<td align="right">171,202,376</td>
<td align="right">66.2%</td>
<td align="right">-32.2%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,212,401</td>
<td align="right">0.3%</td>
<td align="right">1,196,800</td>
<td align="right">0.5%</td>
<td align="right">-1.3%</td>
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
<td align="right">1,891,147</td>
<td align="right">22.4%</td>
<td align="right">235,604</td>
<td align="right">5.2%</td>
<td align="right">-87.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,126,712</td>
<td align="right">13.4%</td>
<td align="right">278,289</td>
<td align="right">6.2%</td>
<td align="right">-75.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,147,258</td>
<td align="right">13.6%</td>
<td align="right">296,940</td>
<td align="right">6.6%</td>
<td align="right">-74.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">3,789,061</td>
<td align="right">45.0%</td>
<td align="right">3,201,497</td>
<td align="right">71.0%</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">167,203</td>
<td align="right">2.0%</td>
<td align="right">188,611</td>
<td align="right">4.2%</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">7,405</td>
<td align="right">0.1%</td>
<td align="right">7,418</td>
<td align="right">0.2%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">45,201</td>
<td align="right">0.5%</td>
<td align="right">45,205</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">212,931</td>
<td align="right">2.5%</td>
<td align="right">212,935</td>
<td align="right">4.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">37,819</td>
<td align="right">0.4%</td>
<td align="right">37,819</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">2,057</td>
<td align="right">0.0%</td>
<td align="right">2,057</td>
<td align="right">0.0%</td>
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
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">5,712</td>
<td align="right">0.5%</td>
<td align="right">10,563</td>
<td align="right">0.9%</td>
<td align="right">84.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">5,777</td>
<td align="right">0.5%</td>
<td align="right">10,471</td>
<td align="right">0.9%</td>
<td align="right">81.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">17,434</td>
<td align="right">1.4%</td>
<td align="right">24,548</td>
<td align="right">2.1%</td>
<td align="right">40.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">736,096</td>
<td align="right">60.7%</td>
<td align="right">703,881</td>
<td align="right">58.8%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">100,883</td>
<td align="right">8.3%</td>
<td align="right">100,838</td>
<td align="right">8.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">319,503</td>
<td align="right">26.4%</td>
<td align="right">319,503</td>
<td align="right">26.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">20,147</td>
<td align="right">1.7%</td>
<td align="right">20,147</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">3,148</td>
<td align="right">0.3%</td>
<td align="right">3,148</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">2,109</td>
<td align="right">0.2%</td>
<td align="right">2,109</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,048</td>
<td align="right">0.1%</td>
<td align="right">1,048</td>
<td align="right">0.1%</td>
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
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">324,188</td>
<td align="right">1.0%</td>
<td align="right">338,486</td>
<td align="right">1.1%</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">20,755,410</td>
<td align="right">66.4%</td>
<td align="right">21,430,452</td>
<td align="right">67.1%</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">20,097,648</td>
<td align="right">64.3%</td>
<td align="right">20,651,919</td>
<td align="right">64.7%</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">79,835</td>
<td align="right">0.3%</td>
<td align="right">78,830</td>
<td align="right">0.2%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">10,267,427</td>
<td align="right">32.8%</td>
<td align="right">10,388,198</td>
<td align="right">32.5%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">10,267,485</td>
<td align="right">32.8%</td>
<td align="right">10,388,256</td>
<td align="right">32.5%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">11,162,060</td>
<td align="right">35.7%</td>
<td align="right">11,282,831</td>
<td align="right">35.3%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">11,162,060</td>
<td align="right">35.7%</td>
<td align="right">11,282,831</td>
<td align="right">35.3%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">894,575</td>
<td align="right">2.9%</td>
<td align="right">894,575</td>
<td align="right">2.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">16</td>
<td align="right">0.0%</td>
<td align="right">16</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">42</td>
<td align="right">0.0%</td>
<td align="right">42</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">956,823</td>
<td align="right">3.1%</td>
<td align="right">956,823</td>
<td align="right">3.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">886,948</td>
<td align="right">2.8%</td>
<td align="right">886,948</td>
<td align="right">2.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">3</td>
<td align="right">0.0%</td>
<td align="right">3</td>
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
<td align="right">38,040</td>
<td align="right"></td>
<td align="right">25,900</td>
<td align="right"></td>
<td align="right">-31.9%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">103,197</td>
<td align="right"></td>
<td align="right">75,260</td>
<td align="right"></td>
<td align="right">-27.1%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">54,776,711</td>
<td align="right">29.6%</td>
<td align="right">68,615,901</td>
<td align="right">35.8%</td>
<td align="right">25.3%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">65,381</td>
<td align="right"></td>
<td align="right">49,575</td>
<td align="right"></td>
<td align="right">-24.2%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">56,262,477</td>
<td align="right">25.8%</td>
<td align="right">68,158,404</td>
<td align="right">30.2%</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">76,091,593</td>
<td align="right">41.1%</td>
<td align="right">67,214,745</td>
<td align="right">35.1%</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">493,982</td>
<td align="right"></td>
<td align="right">550,670</td>
<td align="right"></td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">5,078,614</td>
<td align="right"></td>
<td align="right">5,465,855</td>
<td align="right"></td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">11,107,589</td>
<td align="right">6.0%</td>
<td align="right">10,424,100</td>
<td align="right">5.4%</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">101,916,523</td>
<td align="right">46.7%</td>
<td align="right">95,671,861</td>
<td align="right">42.4%</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">43,223,625</td>
<td align="right">23.3%</td>
<td align="right">45,371,789</td>
<td align="right">23.7%</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">9,605,817</td>
<td align="right"></td>
<td align="right">9,886,837</td>
<td align="right"></td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">19,752,102</td>
<td align="right">63.5%</td>
<td align="right">20,311,290</td>
<td align="right">63.7%</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">19,752,683</td>
<td align="right"></td>
<td align="right">20,311,885</td>
<td align="right"></td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">59,659,622</td>
<td align="right">27.3%</td>
<td align="right">61,112,859</td>
<td align="right">27.1%</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">11,765,283</td>
<td align="right"></td>
<td align="right">12,036,331</td>
<td align="right"></td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">10,959,818</td>
<td align="right">35.2%</td>
<td align="right">11,181,185</td>
<td align="right">35.0%</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">11,375,754</td>
<td align="right">36.5%</td>
<td align="right">11,597,170</td>
<td align="right">36.3%</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">563,731</td>
<td align="right">0.3%</td>
<td align="right">564,186</td>
<td align="right">0.3%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">172,994</td>
<td align="right">0.6%</td>
<td align="right">173,034</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">242,942</td>
<td align="right">0.8%</td>
<td align="right">242,951</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">5,120</td>
<td align="right">1.0%</td>
<td align="right">5,120</td>
<td align="right">0.9%</td>
<td align="right">0.0%</td>
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
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">100,665,987</td>
<td align="right">5,503.9%</td>
<td align="right">653,619,238</td>
<td align="right">8,396.4%</td>
<td align="right">549.3%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">1,828,981</td>
<td align="right"></td>
<td align="right">7,784,507</td>
<td align="right"></td>
<td align="right">325.6%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">2,748</td>
<td align="right">49.5%</td>
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
<td align="right">194</td>
<td align="right">3.5%</td>
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
<td align="right">2,553</td>
<td align="right">46.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">5,546</td>
<td align="right"></td>
<td align="right">709</td>
<td align="right"></td>
<td align="right">-87.2%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">51</td>
<td align="right">0.9%</td>
<td align="right">71</td>
<td align="right">10.0%</td>
<td align="right">39.2%</td>
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
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
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
<td align="right">51</td>
<td align="right"></td>
<td align="right">71</td>
<td align="right"></td>
<td align="right">39.2%</td>
</tr>
<tr>
<td align="left">
Optimizer successes
<details>
<summary>ⓘ</summary>

The number of traces that were successfully optimized.
</details>
</td>
<td align="right">51</td>
<td align="right">100.0%</td>
<td align="right">71</td>
<td align="right">100.0%</td>
<td align="right">39.2%</td>
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
<td align="right">600,912</td>
<td align="right">75.2%</td>
<td align="right">2,020,141</td>
<td align="right">92.7%</td>
<td align="right">236.2%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">798,720</td>
<td align="right"></td>
<td align="right">2,179,072</td>
<td align="right"></td>
<td align="right">172.8%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">13,888</td>
<td align="right">1.7%</td>
<td align="right">32,480</td>
<td align="right">1.5%</td>
<td align="right">133.9%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">183,847</td>
<td align="right">23.0%</td>
<td align="right">126,378</td>
<td align="right">5.8%</td>
<td align="right">-31.3%</td>
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
<td align="left">22</td>
<td align="right">30.1%</td>
<td align="left">3</td>
<td align="right">4.1%</td>
<td align="right">-86.4%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">22</td>
<td align="right">30.1%</td>
<td align="left">26</td>
<td align="right">35.6%</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">22</td>
<td align="right">30.1%</td>
<td align="left">2</td>
<td align="right">2.7%</td>
<td align="right">-90.9%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">0</td>
<td align="right">0.0%</td>
<td align="left">1</td>
<td align="right">1.4%</td>
<td align="right">1 / 0 !!</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left">7</td>
<td align="right">9.6%</td>
<td align="left">41</td>
<td align="right">56.2%</td>
<td align="right">485.7%</td>
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
<td align="left"><= 64</td>
<td align="right">21</td>
<td align="right">41.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">23</td>
<td align="right">45.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">7</td>
<td align="right">13.7%</td>
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
<td align="left"><= 64</td>
<td align="right">22</td>
<td align="right">43.1%</td>
<td align="right">24</td>
<td align="right">33.8%</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">22</td>
<td align="right">43.1%</td>
<td align="right">2</td>
<td align="right">2.8%</td>
<td align="right">-90.9%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">7</td>
<td align="right">13.7%</td>
<td align="right">15</td>
<td align="right">21.1%</td>
<td align="right">114.3%</td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">1</td>
<td align="right">1.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">2</td>
<td align="right">2.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">27</td>
<td align="right">38.0%</td>
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
<td align="left">_STORE_FAST_4</td>
<td align="right">1,998</td>
<td align="right">10,454,929</td>
<td align="right">523,169.7%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">3,001</td>
<td align="right">8,782,458</td>
<td align="right">292,551.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">999</td>
<td align="right">1,676,553</td>
<td align="right">167,723.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">7,753</td>
<td align="right">9,696,916</td>
<td align="right">124,973.1%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">7,753</td>
<td align="right">9,696,916</td>
<td align="right">124,973.1%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">12,004</td>
<td align="right">12,337,584</td>
<td align="right">102,678.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">999</td>
<td align="right">857,354</td>
<td align="right">85,721.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right">999</td>
<td align="right">821,000</td>
<td align="right">82,082.2%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">999</td>
<td align="right">821,000</td>
<td align="right">82,082.2%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">3,001</td>
<td align="right">1,791,068</td>
<td align="right">59,582.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">5,998</td>
<td align="right">3,535,610</td>
<td align="right">58,846.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">14,002</td>
<td align="right">5,928,725</td>
<td align="right">42,242.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">7,001</td>
<td align="right">2,618,348</td>
<td align="right">37,299.6%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">3,001</td>
<td align="right">925,087</td>
<td align="right">30,726.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">2,997</td>
<td align="right">923,318</td>
<td align="right">30,708.1%</td>
</tr>
<tr>
<td align="left">_PY_FRAME_GENERAL</td>
<td align="right">3,001</td>
<td align="right">888,390</td>
<td align="right">29,503.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">3,001</td>
<td align="right">850,213</td>
<td align="right">28,231.0%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">3,001</td>
<td align="right">841,934</td>
<td align="right">27,955.1%</td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right">3,996</td>
<td align="right">1,069,448</td>
<td align="right">26,663.0%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">12,004</td>
<td align="right">2,686,976</td>
<td align="right">22,284.0%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">12,004</td>
<td align="right">2,686,976</td>
<td align="right">22,284.0%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">7,001</td>
<td align="right">938,655</td>
<td align="right">13,307.4%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">7,001</td>
<td align="right">938,655</td>
<td align="right">13,307.4%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">15,005</td>
<td align="right">1,767,653</td>
<td align="right">11,680.4%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right">9,003</td>
<td align="right">895,908</td>
<td align="right">9,851.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">9,003</td>
<td align="right">895,031</td>
<td align="right">9,841.5%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">61,626</td>
<td align="right">1,756,251</td>
<td align="right">2,749.9%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">77,042</td>
<td align="right">1,790,551</td>
<td align="right">2,224.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right">77,042</td>
<td align="right">1,752,372</td>
<td align="right">2,174.6%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">88,069</td>
<td align="right">1,743,612</td>
<td align="right">1,879.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">138,668</td>
<td align="right">2,633,674</td>
<td align="right">1,799.3%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">1,797,144</td>
<td align="right">33,278,984</td>
<td align="right">1,751.8%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">806,610</td>
<td align="right">12,196,830</td>
<td align="right">1,412.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">77,042</td>
<td align="right">924,276</td>
<td align="right">1,099.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">804,612</td>
<td align="right">9,592,586</td>
<td align="right">1,092.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">77,042</td>
<td align="right">896,525</td>
<td align="right">1,063.7%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">882,653</td>
<td align="right">9,650,199</td>
<td align="right">993.3%</td>
</tr>
<tr>
<td align="left">_POP_TOP_INT</td>
<td align="right">999</td>
<td align="right">9,754</td>
<td align="right">876.4%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">999</td>
<td align="right">9,754</td>
<td align="right">876.4%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">1,797,144</td>
<td align="right">14,805,572</td>
<td align="right">723.8%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_EXTEND</td>
<td align="right">8,999</td>
<td align="right">74,080</td>
<td align="right">723.2%</td>
</tr>
<tr>
<td align="left">_GUARD_BINARY_OP_EXTEND</td>
<td align="right">8,999</td>
<td align="right">74,080</td>
<td align="right">723.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">8,000</td>
<td align="right">64,326</td>
<td align="right">704.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">6,002</td>
<td align="right">44,818</td>
<td align="right">646.7%</td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">3,001</td>
<td align="right">22,409</td>
<td align="right">646.7%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">3,001</td>
<td align="right">22,409</td>
<td align="right">646.7%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">3,001</td>
<td align="right">22,409</td>
<td align="right">646.7%</td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right">3,001</td>
<td align="right">22,409</td>
<td align="right">646.7%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">3,001</td>
<td align="right">22,409</td>
<td align="right">646.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">3,001</td>
<td align="right">22,409</td>
<td align="right">646.7%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">2,593,110</td>
<td align="right">19,214,911</td>
<td align="right">641.0%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">19,297,194</td>
<td align="right">142,406,007</td>
<td align="right">638.0%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">18,450,243</td>
<td align="right">118,738,924</td>
<td align="right">543.6%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">914,491</td>
<td align="right">5,155,373</td>
<td align="right">463.7%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">914,490</td>
<td align="right">5,095,257</td>
<td align="right">457.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">819,613</td>
<td align="right">4,284,936</td>
<td align="right">422.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">999</td>
<td align="right">5,176</td>
<td align="right">418.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">833,799</td>
<td align="right">3,400,667</td>
<td align="right">307.9%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">1,802,139</td>
<td align="right">6,844,450</td>
<td align="right">279.8%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">1,694,488</td>
<td align="right">5,916,539</td>
<td align="right">249.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">2,430,114</td>
<td align="right">7,962,216</td>
<td align="right">227.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">811,247</td>
<td align="right">2,478,045</td>
<td align="right">205.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">866,238</td>
<td align="right">2,588,789</td>
<td align="right">198.9%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">914,490</td>
<td align="right">2,629,134</td>
<td align="right">187.5%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">905,846</td>
<td align="right">2,598,241</td>
<td align="right">186.8%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">905,846</td>
<td align="right">2,598,241</td>
<td align="right">186.8%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">4,847,225</td>
<td align="right">12,621,873</td>
<td align="right">160.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,847,225</td>
<td align="right">12,621,873</td>
<td align="right">160.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">4,857,227</td>
<td align="right">11,879,814</td>
<td align="right">144.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">804,612</td>
<td align="right">1,707,465</td>
<td align="right">112.2%</td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right">806,610</td>
<td align="right">1,699,322</td>
<td align="right">110.7%</td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right">804,612</td>
<td align="right">1,679,814</td>
<td align="right">108.8%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">811,613</td>
<td align="right">1,688,139</td>
<td align="right">108.0%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">811,247</td>
<td align="right">1,658,522</td>
<td align="right">104.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">827,804</td>
<td align="right">1,679,923</td>
<td align="right">102.9%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">811,247</td>
<td align="right">1,630,769</td>
<td align="right">101.0%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">880,518</td>
<td align="right">1,744,075</td>
<td align="right">98.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">904,847</td>
<td align="right">1,752,080</td>
<td align="right">93.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">4,072,792</td>
<td align="right">4,892,312</td>
<td align="right">20.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">4,961,081</td>
<td align="right">5,780,558</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">813,889</td>
<td align="right">850,570</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right">813,889</td>
<td align="right">850,570</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">804,612</td>
<td align="right">832,538</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">804,612</td>
<td align="right">832,538</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">804,612</td>
<td align="right">832,538</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION_AND_LOCK</td>
<td align="right">804,612</td>
<td align="right">832,538</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">804,612</td>
<td align="right">832,538</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">805,611</td>
<td align="right">814,640</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">77,042</td>
<td align="right">77,000</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">77,042</td>
<td align="right">77,000</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">77,042</td>
<td align="right">77,000</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">77,042</td>
<td align="right">77,000</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_FLOAT</td>
<td align="right">77,042</td>
<td align="right">77,000</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_FLOAT</td>
<td align="right">77,042</td>
<td align="right">77,000</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">811,247</td>
<td align="right">811,246</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">827,805</td>
<td align="right">827,804</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">12,004</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">22,986,604</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">9,650,608</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">9,579,572</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right"></td>
<td align="right">8,760,049</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right"></td>
<td align="right">2,081,863</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INSERT_NULL</td>
<td align="right"></td>
<td align="right">1,694,552</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SPECIAL</td>
<td align="right"></td>
<td align="right">1,694,552</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right"></td>
<td align="right">1,675,372</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right"></td>
<td align="right">1,639,046</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right"></td>
<td align="right">884,083</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right">875,643</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right"></td>
<td align="right">855,455</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">847,598</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right"></td>
<td align="right">847,568</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right"></td>
<td align="right">847,276</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right"></td>
<td align="right">847,276</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right"></td>
<td align="right">847,276</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right"></td>
<td align="right">847,276</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right"></td>
<td align="right">847,276</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SWAP_3</td>
<td align="right"></td>
<td align="right">847,276</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right"></td>
<td align="right">827,804</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right"></td>
<td align="right">827,395</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right"></td>
<td align="right">819,525</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right"></td>
<td align="right">819,523</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right"></td>
<td align="right">163,931</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right"></td>
<td align="right">137,888</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right"></td>
<td align="right">83,153</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">60,117</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">55,402</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right"></td>
<td align="right">55,302</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right"></td>
<td align="right">28,075</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right"></td>
<td align="right">28,075</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_1</td>
<td align="right"></td>
<td align="right">27,652</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">27,651</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right"></td>
<td align="right">4,578</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right"></td>
<td align="right">4,578</td>
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
<td align="right">195</td>
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
<td align="right">42</td>
<td align="right">42</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-10-22
