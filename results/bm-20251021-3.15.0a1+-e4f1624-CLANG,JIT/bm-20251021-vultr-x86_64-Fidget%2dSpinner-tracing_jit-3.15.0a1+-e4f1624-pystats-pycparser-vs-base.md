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
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">1,195,920</td>
<td align="right">1,299</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,962,600</td>
<td align="right">12,600</td>
<td align="right">-99.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">4,138,460</td>
<td align="right">90,980</td>
<td align="right">-97.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">11,276,680</td>
<td align="right">295,674</td>
<td align="right">-97.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">37,932,880</td>
<td align="right">2,018,917</td>
<td align="right">-94.7%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">26,601,120</td>
<td align="right">1,417,797</td>
<td align="right">-94.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">26,174,520</td>
<td align="right">1,395,630</td>
<td align="right">-94.7%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">57,997,900</td>
<td align="right">4,575,932</td>
<td align="right">-92.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">31,292,180</td>
<td align="right">2,997,617</td>
<td align="right">-90.4%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">18,382,400</td>
<td align="right">1,897,966</td>
<td align="right">-89.7%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">38,640,980</td>
<td align="right">4,217,308</td>
<td align="right">-89.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">11,699,120</td>
<td align="right">1,520,884</td>
<td align="right">-87.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">19,697,720</td>
<td align="right">2,602,392</td>
<td align="right">-86.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,898,940</td>
<td align="right">258,481</td>
<td align="right">-86.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,765,160</td>
<td align="right">250,300</td>
<td align="right">-85.8%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">10,952,100</td>
<td align="right">1,798,298</td>
<td align="right">-83.6%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">27,454,460</td>
<td align="right">4,544,710</td>
<td align="right">-83.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">30,116,640</td>
<td align="right">5,046,430</td>
<td align="right">-83.2%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">2,240,280</td>
<td align="right">384,318</td>
<td align="right">-82.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">28,587,940</td>
<td align="right">5,168,487</td>
<td align="right">-81.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">36,950,160</td>
<td align="right">7,712,553</td>
<td align="right">-79.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">1,495,260</td>
<td align="right">313,979</td>
<td align="right">-79.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">5,903,480</td>
<td align="right">1,331,029</td>
<td align="right">-77.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">176,471,000</td>
<td align="right">39,944,434</td>
<td align="right">-77.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">263,898,800</td>
<td align="right">61,164,818</td>
<td align="right">-76.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">44,049,700</td>
<td align="right">10,696,365</td>
<td align="right">-75.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">8,032,220</td>
<td align="right">1,978,440</td>
<td align="right">-75.4%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">105,292,140</td>
<td align="right">26,325,640</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">6,225,720</td>
<td align="right">1,562,845</td>
<td align="right">-74.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">7,137,220</td>
<td align="right">1,803,246</td>
<td align="right">-74.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">47,252,760</td>
<td align="right">15,730,155</td>
<td align="right">-66.7%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">1,396,240</td>
<td align="right">511,384</td>
<td align="right">-63.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">3,111,320</td>
<td align="right">1,238,803</td>
<td align="right">-60.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,461,150,420</td>
<td align="right">596,737,587</td>
<td align="right">-59.2%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">52,349,040</td>
<td align="right">23,350,212</td>
<td align="right">-55.4%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">52,349,040</td>
<td align="right">23,350,212</td>
<td align="right">-55.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">185,323,260</td>
<td align="right">84,755,318</td>
<td align="right">-54.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">94,649,180</td>
<td align="right">46,166,803</td>
<td align="right">-51.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">1,091,700</td>
<td align="right">534,601</td>
<td align="right">-51.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,091,760</td>
<td align="right">534,775</td>
<td align="right">-51.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">251,739,960</td>
<td align="right">125,775,079</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">35,967,840</td>
<td align="right">18,431,425</td>
<td align="right">-48.8%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,609,400</td>
<td align="right">1,364,999</td>
<td align="right">-47.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">969,720</td>
<td align="right">1,431,108</td>
<td align="right">47.6%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">234,295,760</td>
<td align="right">122,903,681</td>
<td align="right">-47.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,036,080</td>
<td align="right">3,755,569</td>
<td align="right">-46.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">107,327,920</td>
<td align="right">58,364,749</td>
<td align="right">-45.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">10,952,240</td>
<td align="right">6,082,766</td>
<td align="right">-44.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">52,433,280</td>
<td align="right">30,079,270</td>
<td align="right">-42.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">253,782,500</td>
<td align="right">149,660,303</td>
<td align="right">-41.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">78,254,500</td>
<td align="right">51,617,325</td>
<td align="right">-34.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">109,965,020</td>
<td align="right">72,704,587</td>
<td align="right">-33.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">88,219,480</td>
<td align="right">66,976,134</td>
<td align="right">-24.1%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">63,978,340</td>
<td align="right">48,939,097</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">25,093,700</td>
<td align="right">30,800,152</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">419,800</td>
<td align="right">329,376</td>
<td align="right">-21.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">46,868,280</td>
<td align="right">37,720,630</td>
<td align="right">-19.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">162,577,500</td>
<td align="right">131,657,719</td>
<td align="right">-19.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">6,336,120</td>
<td align="right">5,198,774</td>
<td align="right">-18.0%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,054,520</td>
<td align="right">869,311</td>
<td align="right">-17.6%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">2,410,980</td>
<td align="right">2,000,280</td>
<td align="right">-17.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">26,781,000</td>
<td align="right">22,406,362</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">7,879,820</td>
<td align="right">6,620,927</td>
<td align="right">-16.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">35,514,600</td>
<td align="right">30,116,121</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">28,863,200</td>
<td align="right">24,488,526</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">38,713,100</td>
<td align="right">32,917,300</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">10,574,580</td>
<td align="right">9,104,052</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">139,498,760</td>
<td align="right">120,950,204</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">106,276,480</td>
<td align="right">92,317,409</td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">855,060</td>
<td align="right">747,348</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">38,660,500</td>
<td align="right">41,988,987</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">20,526,900</td>
<td align="right">18,899,030</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">12,358,920</td>
<td align="right">11,399,325</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">6,266,820</td>
<td align="right">5,955,527</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">16,603,860</td>
<td align="right">15,987,680</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">34,938,680</td>
<td align="right">34,195,314</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">4,013,520</td>
<td align="right">3,982,310</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">4,013,340</td>
<td align="right">3,982,134</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">378,060</td>
<td align="right">377,391</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">88,680</td>
<td align="right">88,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">41,912,040</td>
<td align="right">41,912,040</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">1,852,280</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">835,200</td>
<td align="right">835,200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">669,540</td>
<td align="right">669,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">406,300</td>
<td align="right">406,300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">379,680</td>
<td align="right">379,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">216,960</td>
<td align="right">216,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">180,960</td>
<td align="right">180,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">94,920</td>
<td align="right">94,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">84,420</td>
<td align="right">84,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">65,880</td>
<td align="right">65,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">65,880</td>
<td align="right">65,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">56,100</td>
<td align="right">56,100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">32,940</td>
<td align="right">32,940</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">30,600</td>
<td align="right">30,600</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">30,420</td>
<td align="right">30,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">30,420</td>
<td align="right">30,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">13,860</td>
<td align="right">13,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">13,860</td>
<td align="right">13,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">13,860</td>
<td align="right">13,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">3,840</td>
<td align="right">3,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">1,980</td>
<td align="right">1,980</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">1,620</td>
<td align="right">1,620</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">1,440</td>
<td align="right">1,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">960</td>
<td align="right">960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">720</td>
<td align="right">720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">720</td>
<td align="right">720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">480</td>
<td align="right">480</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">360</td>
<td align="right">360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">360</td>
<td align="right">360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">360</td>
<td align="right">360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">360</td>
<td align="right">360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">280</td>
<td align="right">280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">240</td>
<td align="right">240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">120</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">40</td>
<td align="right">40</td>
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
<td align="right">28,855,380</td>
<td align="right">6.5%</td>
<td align="right">24,481,436</td>
<td align="right">5.6%</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">415,632,600</td>
<td align="right">93.5%</td>
<td align="right">415,632,600</td>
<td align="right">94.4%</td>
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
<td align="right">7,760</td>
<td align="right">99.2%</td>
<td align="right">7,030</td>
<td align="right">99.2%</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">60</td>
<td align="right">0.8%</td>
<td align="right">60</td>
<td align="right">0.8%</td>
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
<td align="left">out of range</td>
<td align="right">7,060</td>
<td align="right">91.0%</td>
<td align="right">6,330</td>
<td align="right">90.0%</td>
<td align="right">-10.3%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">200</td>
<td align="right">2.6%</td>
<td align="right">200</td>
<td align="right">2.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">200</td>
<td align="right">2.6%</td>
<td align="right">200</td>
<td align="right">2.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">120</td>
<td align="right">1.5%</td>
<td align="right">120</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">120</td>
<td align="right">1.5%</td>
<td align="right">120</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">40</td>
<td align="right">0.5%</td>
<td align="right">40</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">20</td>
<td align="right">0.3%</td>
<td align="right">20</td>
<td align="right">0.3%</td>
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
<td align="right">26,601,120</td>
<td align="right">100.0%</td>
<td align="right">1,417,797</td>
<td align="right">100.0%</td>
<td align="right">-94.7%</td>
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
<td align="right">28,029,800</td>
<td align="right">9.0%</td>
<td align="right">20,378,304</td>
<td align="right">6.3%</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">28,568,820</td>
<td align="right">9.2%</td>
<td align="right">20,772,812</td>
<td align="right">6.4%</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">282,821,200</td>
<td align="right">90.8%</td>
<td align="right">302,857,742</td>
<td align="right">93.6%</td>
<td align="right">7.1%</td>
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
<td align="right">4,821</td>
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
<td align="right">539,500</td>
<td align="right">100.0%</td>
<td align="right">394,988</td>
<td align="right">100.0%</td>
<td align="right">-26.8%</td>
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
<td align="right">406,200</td>
<td align="right">0.3%</td>
<td align="right">406,200</td>
<td align="right">0.3%</td>
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
<td align="right">130,939,800</td>
<td align="right">99.7%</td>
<td align="right">130,939,800</td>
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
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">100</td>
<td align="right">100.0%</td>
<td align="right">100</td>
<td align="right">100.0%</td>
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
<td align="right">100</td>
<td align="right">100.0%</td>
<td align="right">100</td>
<td align="right">100.0%</td>
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
<td align="right">1,395,660</td>
<td align="right">3.9%</td>
<td align="right">511,002</td>
<td align="right">1.5%</td>
<td align="right">-63.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">34,664,280</td>
<td align="right">96.1%</td>
<td align="right">34,664,280</td>
<td align="right">98.5%</td>
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
<td align="right">580</td>
<td align="right">100.0%</td>
<td align="right">382</td>
<td align="right">100.0%</td>
<td align="right">-34.1%</td>
</tr>
<tr>
<td align="left">Success</td>
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
<td align="left">tuple</td>
<td align="right">300</td>
<td align="right">51.7%</td>
<td align="right">122</td>
<td align="right">31.9%</td>
<td align="right">-59.3%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">200</td>
<td align="right">34.5%</td>
<td align="right">180</td>
<td align="right">47.1%</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">80</td>
<td align="right">13.8%</td>
<td align="right">80</td>
<td align="right">20.9%</td>
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
<td align="right">1,764,480</td>
<td align="right">63.8%</td>
<td align="right">249,940</td>
<td align="right">14.6%</td>
<td align="right">-85.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,000,440</td>
<td align="right">36.2%</td>
<td align="right">1,461,828</td>
<td align="right">85.4%</td>
<td align="right">46.1%</td>
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
<td align="right">680</td>
<td align="right">100.0%</td>
<td align="right">360</td>
<td align="right">100.0%</td>
<td align="right">-47.1%</td>
</tr>
<tr>
<td align="left">Success</td>
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
<td align="left">ascii string</td>
<td align="right">100</td>
<td align="right">14.7%</td>
<td align="right">20</td>
<td align="right">5.6%</td>
<td align="right">-80.0%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">160</td>
<td align="right">23.5%</td>
<td align="right">200</td>
<td align="right">55.6%</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">280</td>
<td align="right">41.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">60</td>
<td align="right">8.8%</td>
<td align="right">60</td>
<td align="right">16.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">40</td>
<td align="right">5.9%</td>
<td align="right">40</td>
<td align="right">11.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">40</td>
<td align="right">5.9%</td>
<td align="right">40</td>
<td align="right">11.1%</td>
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
<td align="left">list</td>
<td align="right">11,586,960</td>
<td align="right">11,586,960 / 0 !!</td>
<td align="right">11,586,960</td>
<td align="right">11,586,960 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">2,209,860</td>
<td align="right">2,209,860 / 0 !!</td>
<td align="right">2,209,860</td>
<td align="right">2,209,860 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">405,480</td>
<td align="right">405,480 / 0 !!</td>
<td align="right">405,480</td>
<td align="right">405,480 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">14,400</td>
<td align="right">14,400 / 0 !!</td>
<td align="right">14,400</td>
<td align="right">14,400 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">13,860</td>
<td align="right">13,860 / 0 !!</td>
<td align="right">13,860</td>
<td align="right">13,860 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">1,320</td>
<td align="right">1,320 / 0 !!</td>
<td align="right">1,320</td>
<td align="right">1,320 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">360</td>
<td align="right">360 / 0 !!</td>
<td align="right">360</td>
<td align="right">360 / 0 !!</td>
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
<td align="right">35,956,720</td>
<td align="right">6.5%</td>
<td align="right">18,424,146</td>
<td align="right">3.4%</td>
<td align="right">-48.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">10,247,560</td>
<td align="right">1.8%</td>
<td align="right">8,404,826</td>
<td align="right">1.6%</td>
<td align="right">-18.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">510,710,260</td>
<td align="right">91.7%</td>
<td align="right">509,906,755</td>
<td align="right">95.0%</td>
<td align="right">-0.2%</td>
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
<td align="right">306</td>
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
<td align="right">10,760</td>
<td align="right">5.3%</td>
<td align="right">6,919</td>
<td align="right">4.2%</td>
<td align="right">-35.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">193,620</td>
<td align="right">94.7%</td>
<td align="right">159,040</td>
<td align="right">95.8%</td>
<td align="right">-17.9%</td>
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
<td align="right">1,460</td>
<td align="right">13.6%</td>
<td align="right">521</td>
<td align="right">7.5%</td>
<td align="right">-64.3%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">120</td>
<td align="right">1.1%</td>
<td align="right">120</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">120</td>
<td align="right">1.1%</td>
<td align="right">120</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">100</td>
<td align="right">0.9%</td>
<td align="right">100</td>
<td align="right">1.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">60</td>
<td align="right">0.6%</td>
<td align="right">60</td>
<td align="right">0.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">40</td>
<td align="right">0.4%</td>
<td align="right">40</td>
<td align="right">0.6%</td>
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
<td align="right">156,887,080</td>
<td align="right">100.0%</td>
<td align="right">144,370,196</td>
<td align="right">100.0%</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,060</td>
<td align="right">0.0%</td>
<td align="right">4,060</td>
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
<td align="right">340</td>
<td align="right">100.0%</td>
<td align="right">340</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">8,029,800</td>
<td align="right">3.3%</td>
<td align="right">1,977,460</td>
<td align="right">0.8%</td>
<td align="right">-75.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">187,920</td>
<td align="right">0.1%</td>
<td align="right">185,480</td>
<td align="right">0.1%</td>
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
<td align="right">231,820,800</td>
<td align="right">96.6%</td>
<td align="right">231,823,200</td>
<td align="right">99.1%</td>
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
<td align="right">2,420</td>
<td align="right">40.6%</td>
<td align="right">980</td>
<td align="right">21.9%</td>
<td align="right">-59.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,540</td>
<td align="right">59.4%</td>
<td align="right">3,500</td>
<td align="right">78.1%</td>
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
<td align="left">split dict</td>
<td align="right">2,380</td>
<td align="right">98.3%</td>
<td align="right">940</td>
<td align="right">95.9%</td>
<td align="right">-60.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">8,840</td>
<td align="right">365.3%</td>
<td align="right">5,938</td>
<td align="right">605.9%</td>
<td align="right">-32.8%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">40</td>
<td align="right">1.7%</td>
<td align="right">40</td>
<td align="right">4.1%</td>
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
<td align="right">26,772,000</td>
<td align="right">50.2%</td>
<td align="right">22,398,056</td>
<td align="right">45.7%</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">26,554,200</td>
<td align="right">49.8%</td>
<td align="right">26,554,200</td>
<td align="right">54.2%</td>
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
<td align="right">9,000</td>
<td align="right">100.0%</td>
<td align="right">8,306</td>
<td align="right">100.0%</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">Success</td>
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
<td align="left">py simple</td>
<td align="right">9,000</td>
<td align="right">100.0%</td>
<td align="right">8,306</td>
<td align="right">100.0%</td>
<td align="right">-7.7%</td>
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
<td align="right">1,880,340</td>
<td align="right">1.4%</td>
<td align="right">8,940</td>
<td align="right">0.0%</td>
<td align="right">-99.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,573,400</td>
<td align="right">3.5%</td>
<td align="right">612,505</td>
<td align="right">0.5%</td>
<td align="right">-86.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">124,149,800</td>
<td align="right">95.0%</td>
<td align="right">121,792,940</td>
<td align="right">99.5%</td>
<td align="right">-1.9%</td>
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
<td align="right">62</td>
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
<td align="right">82,240</td>
<td align="right">48.8%</td>
<td align="right">3,640</td>
<td align="right">23.9%</td>
<td align="right">-95.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">86,320</td>
<td align="right">51.2%</td>
<td align="right">11,620</td>
<td align="right">76.1%</td>
<td align="right">-86.5%</td>
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
<td align="left">dict</td>
<td align="right">2,660</td>
<td align="right">3.2%</td>
<td align="right">2,620</td>
<td align="right">72.0%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">78,560</td>
<td align="right">95.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">1,000</td>
<td align="right">1.2%</td>
<td align="right">1,000</td>
<td align="right">27.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">20</td>
<td align="right">0.5%</td>
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
<td align="right">36,819,480</td>
<td align="right">100.0%</td>
<td align="right">36,819,480</td>
<td align="right">100.0%</td>
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
<td align="right">40</td>
<td align="right">100.0%</td>
<td align="right">40</td>
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
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">3,224,997,120</td>
<td align="right">63.6%</td>
<td align="right">1,444,310,550</td>
<td align="right">58.4%</td>
<td align="right">-55.2%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">134,016,760</td>
<td align="right">2.6%</td>
<td align="right">70,288,252</td>
<td align="right">2.8%</td>
<td align="right">-47.6%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">1,664,730,840</td>
<td align="right">32.9%</td>
<td align="right">929,994,538</td>
<td align="right">37.6%</td>
<td align="right">-44.1%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">43,583,840</td>
<td align="right">0.9%</td>
<td align="right">29,981,920</td>
<td align="right">1.2%</td>
<td align="right">-31.2%</td>
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
<td align="right">1,880,340</td>
<td align="right">1.2%</td>
<td align="right">8,940</td>
<td align="right">0.0%</td>
<td align="right">-99.5%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">26,601,120</td>
<td align="right">16.7%</td>
<td align="right">1,417,797</td>
<td align="right">1.6%</td>
<td align="right">-94.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,764,480</td>
<td align="right">1.1%</td>
<td align="right">249,940</td>
<td align="right">0.3%</td>
<td align="right">-85.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">8,029,800</td>
<td align="right">5.0%</td>
<td align="right">1,977,460</td>
<td align="right">2.2%</td>
<td align="right">-75.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">1,395,660</td>
<td align="right">0.9%</td>
<td align="right">511,002</td>
<td align="right">0.6%</td>
<td align="right">-63.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">35,956,720</td>
<td align="right">22.5%</td>
<td align="right">18,424,146</td>
<td align="right">20.4%</td>
<td align="right">-48.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">28,029,800</td>
<td align="right">17.6%</td>
<td align="right">20,378,304</td>
<td align="right">22.6%</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">26,772,000</td>
<td align="right">16.8%</td>
<td align="right">22,398,056</td>
<td align="right">24.8%</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">28,855,380</td>
<td align="right">18.1%</td>
<td align="right">24,481,436</td>
<td align="right">27.1%</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">406,200</td>
<td align="right">0.3%</td>
<td align="right">406,200</td>
<td align="right">0.5%</td>
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
<td align="right">13,887,460</td>
<td align="right">31.9%</td>
<td align="right">1,219,975</td>
<td align="right">4.1%</td>
<td align="right">-91.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">3,435,460</td>
<td align="right">7.9%</td>
<td align="right">375,406</td>
<td align="right">1.3%</td>
<td align="right">-89.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">1,134,580</td>
<td align="right">2.6%</td>
<td align="right">233,739</td>
<td align="right">0.8%</td>
<td align="right">-79.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">14,681,000</td>
<td align="right">33.7%</td>
<td align="right">19,552,477</td>
<td align="right">65.2%</td>
<td align="right">33.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">8,468,680</td>
<td align="right">19.4%</td>
<td align="right">6,779,172</td>
<td align="right">22.6%</td>
<td align="right">-20.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,553,540</td>
<td align="right">3.6%</td>
<td align="right">1,400,341</td>
<td align="right">4.7%</td>
<td align="right">-9.9%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">2,080</td>
<td align="right">0.0%</td>
<td align="right">2,237</td>
<td align="right">0.0%</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">187,560</td>
<td align="right">0.4%</td>
<td align="right">185,120</td>
<td align="right">0.6%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">225,340</td>
<td align="right">0.5%</td>
<td align="right">225,313</td>
<td align="right">0.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">2,300</td>
<td align="right">0.0%</td>
<td align="right">2,300</td>
<td align="right">0.0%</td>
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
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">41,912,100</td>
<td align="right">26.4%</td>
<td align="right">41,912,100</td>
<td align="right">26.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">116,652,300</td>
<td align="right">73.6%</td>
<td align="right">116,652,300</td>
<td align="right">73.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">41,912,100</td>
<td align="right">26.4%</td>
<td align="right">41,912,100</td>
<td align="right">26.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">41,911,860</td>
<td align="right">26.4%</td>
<td align="right">41,911,860</td>
<td align="right">26.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">41,911,500</td>
<td align="right">26.4%</td>
<td align="right">41,911,500</td>
<td align="right">26.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">34,854,900</td>
<td align="right">22.0%</td>
<td align="right">34,854,900</td>
<td align="right">22.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">73,800</td>
<td align="right">0.0%</td>
<td align="right">73,800</td>
<td align="right">0.0%</td>
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
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">162,577,500</td>
<td align="right">102.5%</td>
<td align="right">162,577,500</td>
<td align="right">102.5%</td>
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
<td align="right">25,405</td>
<td align="right"></td>
<td align="right">140,148</td>
<td align="right"></td>
<td align="right">451.7%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">153,939</td>
<td align="right"></td>
<td align="right">355,283</td>
<td align="right"></td>
<td align="right">130.8%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">136,444</td>
<td align="right"></td>
<td align="right">223,106</td>
<td align="right"></td>
<td align="right">63.5%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">233,021,640</td>
<td align="right">8.5%</td>
<td align="right">89,461,436</td>
<td align="right">3.2%</td>
<td align="right">-61.6%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">692,769,996</td>
<td align="right">23.7%</td>
<td align="right">1,098,721,504</td>
<td align="right">37.6%</td>
<td align="right">58.6%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">57,551,580</td>
<td align="right">2.0%</td>
<td align="right">29,723,284</td>
<td align="right">1.0%</td>
<td align="right">-48.4%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">798,105,994</td>
<td align="right">29.0%</td>
<td align="right">1,147,458,960</td>
<td align="right">41.7%</td>
<td align="right">43.8%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">1,074,687,480</td>
<td align="right">39.1%</td>
<td align="right">730,467,029</td>
<td align="right">26.5%</td>
<td align="right">-32.0%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">1,389,250,240</td>
<td align="right">47.5%</td>
<td align="right">988,432,363</td>
<td align="right">33.8%</td>
<td align="right">-28.9%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">2,740</td>
<td align="right">0.0%</td>
<td align="right">3,392</td>
<td align="right">0.0%</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">643,882,444</td>
<td align="right">23.4%</td>
<td align="right">785,416,623</td>
<td align="right">28.5%</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">782,669,358</td>
<td align="right">26.8%</td>
<td align="right">808,920,021</td>
<td align="right">27.6%</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">82,266,436</td>
<td align="right"></td>
<td align="right">80,331,452</td>
<td align="right"></td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">84,891,375</td>
<td align="right"></td>
<td align="right">84,775,208</td>
<td align="right"></td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">27,487,200</td>
<td align="right">9.4%</td>
<td align="right">27,487,622</td>
<td align="right">9.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">133,740,560</td>
<td align="right">45.9%</td>
<td align="right">133,741,614</td>
<td align="right">45.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">157,546,440</td>
<td align="right"></td>
<td align="right">157,547,366</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">157,547,780</td>
<td align="right">54.1%</td>
<td align="right">157,548,706</td>
<td align="right">54.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">106,250,620</td>
<td align="right">36.5%</td>
<td align="right">106,250,600</td>
<td align="right">36.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">158,847,420</td>
<td align="right"></td>
<td align="right">158,847,408</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">36,013,800</td>
<td align="right"></td>
<td align="right">36,013,800</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">360</td>
<td align="right">0.0%</td>
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
<td align="right">6,660</td>
<td align="right">4,993,040</td>
<td align="right">197,448,911</td>
<td align="right">13,917,200</td>
<td align="right">17,997,240</td>
<td align="right">6,660</td>
<td align="right">4,993,040</td>
<td align="right">197,600,061</td>
<td align="right">13,994,582</td>
<td align="right">17,923,440</td>
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
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">120</td>
<td align="right">26.1%</td>
<td align="right">585</td>
<td align="right">45.2%</td>
<td align="right">387.5%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">8,660</td>
<td align="right"></td>
<td align="right">25,607</td>
<td align="right"></td>
<td align="right">195.7%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">460</td>
<td align="right">5.3%</td>
<td align="right">1,294</td>
<td align="right">5.1%</td>
<td align="right">181.3%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">3,734,602,200</td>
<td align="right">3,844.3%</td>
<td align="right">9,920,240,380</td>
<td align="right">5,328.5%</td>
<td align="right">165.6%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">2,380</td>
<td align="right">27.5%</td>
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
<td align="right">160</td>
<td align="right">1.8%</td>
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
<td align="right">5,780</td>
<td align="right">66.7%</td>
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
<td align="right">97,147,200</td>
<td align="right"></td>
<td align="right">186,174,484</td>
<td align="right"></td>
<td align="right">91.6%</td>
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
<td align="right">23</td>
<td align="right">0.1%</td>
<td align="right">23 / 0 !!</td>
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
<td align="right">240</td>
<td align="right">52.2%</td>
<td align="right">1,294</td>
<td align="right">100.0%</td>
<td align="right">439.2%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">460</td>
<td align="right"></td>
<td align="right">1,294</td>
<td align="right"></td>
<td align="right">181.3%</td>
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
<td align="right">3,384,900</td>
<td align="right">84.3%</td>
<td align="right">32,207,815</td>
<td align="right">89.3%</td>
<td align="right">851.5%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">4,014,080</td>
<td align="right"></td>
<td align="right">36,077,568</td>
<td align="right"></td>
<td align="right">798.8%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">69,280</td>
<td align="right">1.7%</td>
<td align="right">531,616</td>
<td align="right">1.5%</td>
<td align="right">667.3%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">559,660</td>
<td align="right">13.9%</td>
<td align="right">3,336,843</td>
<td align="right">9.2%</td>
<td align="right">496.2%</td>
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
<td align="left">80</td>
<td align="right">33.3%</td>
<td align="left">20</td>
<td align="right">1.5%</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">40</td>
<td align="right">16.7%</td>
<td align="left">144</td>
<td align="right">11.1%</td>
<td align="right">260.0%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">40</td>
<td align="right">16.7%</td>
<td align="left">440</td>
<td align="right">34.0%</td>
<td align="right">1,000.0%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">40</td>
<td align="right">16.7%</td>
<td align="left">284</td>
<td align="right">21.9%</td>
<td align="right">610.0%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left">40</td>
<td align="right">16.7%</td>
<td align="left">343</td>
<td align="right">26.5%</td>
<td align="right">757.5%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">63</td>
<td align="right">4.9%</td>
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
<td align="right">80</td>
<td align="right">17.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">40</td>
<td align="right">8.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">60</td>
<td align="right">13.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">280</td>
<td align="right">60.9%</td>
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
<td align="left"><= 4</td>
<td align="right">20</td>
<td align="right">4.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">60</td>
<td align="right">13.0%</td>
<td align="right">20</td>
<td align="right">1.5%</td>
<td align="right">-66.7%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">40</td>
<td align="right">8.7%</td>
<td align="right">164</td>
<td align="right">12.7%</td>
<td align="right">310.0%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">40</td>
<td align="right">8.7%</td>
<td align="right">540</td>
<td align="right">41.7%</td>
<td align="right">1,250.0%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">60</td>
<td align="right">13.0%</td>
<td align="right">203</td>
<td align="right">15.7%</td>
<td align="right">238.3%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">20</td>
<td align="right">4.3%</td>
<td align="right">324</td>
<td align="right">25.0%</td>
<td align="right">1,520.0%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">43</td>
<td align="right">3.3%</td>
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
<td align="left">_GUARD_NOS_OVERFLOWED</td>
<td align="right">8,700</td>
<td align="right">21,273,918</td>
<td align="right">244,427.8%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">8,700</td>
<td align="right">624,880</td>
<td align="right">7,082.5%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">210,920</td>
<td align="right">9,177,090</td>
<td align="right">4,251.0%</td>
</tr>
<tr>
<td align="left">_SWAP_3</td>
<td align="right">626,280</td>
<td align="right">8,585,461</td>
<td align="right">1,270.9%</td>
</tr>
<tr>
<td align="left">_CALL_KW_NON_PY</td>
<td align="right">109,720</td>
<td align="right">1,368,613</td>
<td align="right">1,147.4%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE_KW</td>
<td align="right">109,720</td>
<td align="right">1,368,613</td>
<td align="right">1,147.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">3,381,160</td>
<td align="right">40,641,593</td>
<td align="right">1,102.0%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">109,720</td>
<td align="right">1,311,340</td>
<td align="right">1,095.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">3,257,320</td>
<td align="right">31,551,883</td>
<td align="right">868.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">9,895,800</td>
<td align="right">86,970,167</td>
<td align="right">778.9%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">11,474,840</td>
<td align="right">93,158,513</td>
<td align="right">711.9%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">19,455,160</td>
<td align="right">155,981,726</td>
<td align="right">701.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION_AND_LOCK</td>
<td align="right">19,455,160</td>
<td align="right">155,981,726</td>
<td align="right">701.7%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">19,455,160</td>
<td align="right">155,981,726</td>
<td align="right">701.7%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">80</td>
<td align="right">640</td>
<td align="right">700.0%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">3,361,900</td>
<td align="right">24,661,037</td>
<td align="right">633.5%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">3,989,040</td>
<td align="right">27,125,232</td>
<td align="right">580.0%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">33,380,480</td>
<td align="right">192,406,041</td>
<td align="right">476.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">168,274,340</td>
<td align="right">872,339,448</td>
<td align="right">418.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">44,691,240</td>
<td align="right">228,872,039</td>
<td align="right">412.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">3,396,900</td>
<td align="right">14,881,553</td>
<td align="right">338.1%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">16,752,360</td>
<td align="right">71,384,705</td>
<td align="right">326.1%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">10,337,140</td>
<td align="right">39,925,314</td>
<td align="right">286.2%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">10,337,140</td>
<td align="right">39,925,314</td>
<td align="right">286.2%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">2,179,420</td>
<td align="right">7,975,220</td>
<td align="right">265.9%</td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right">1,380</td>
<td align="right">4,850</td>
<td align="right">251.4%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">6,514,640</td>
<td align="right">21,553,883</td>
<td align="right">230.9%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">6,514,640</td>
<td align="right">21,553,883</td>
<td align="right">230.9%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">6,514,640</td>
<td align="right">21,553,883</td>
<td align="right">230.9%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">5,443,480</td>
<td align="right">16,780,357</td>
<td align="right">208.3%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">62,614,000</td>
<td align="right">188,547,123</td>
<td align="right">201.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">62,614,000</td>
<td align="right">188,547,123</td>
<td align="right">201.1%</td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right">626,280</td>
<td align="right">1,820,901</td>
<td align="right">190.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">20,944,420</td>
<td align="right">60,253,843</td>
<td align="right">187.7%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">57,615,380</td>
<td align="right">162,290,444</td>
<td align="right">181.7%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">637,274,120</td>
<td align="right">1,740,458,108</td>
<td align="right">173.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">3,381,160</td>
<td align="right">9,187,080</td>
<td align="right">171.7%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">109,720</td>
<td align="right">294,929</td>
<td align="right">168.8%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right">15,925,980</td>
<td align="right">42,269,964</td>
<td align="right">165.4%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">614,031,940</td>
<td align="right">1,625,325,648</td>
<td align="right">164.7%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">13,272,680</td>
<td align="right">34,565,594</td>
<td align="right">160.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_DICT</td>
<td align="right">16,850,000</td>
<td align="right">43,487,175</td>
<td align="right">158.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">33,042,040</td>
<td align="right">83,703,592</td>
<td align="right">153.3%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">33,050,740</td>
<td align="right">81,533,117</td>
<td align="right">146.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">103,914,460</td>
<td align="right">247,281,697</td>
<td align="right">138.0%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">22,493,220</td>
<td align="right">51,730,827</td>
<td align="right">130.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">60,328,840</td>
<td align="right">135,671,173</td>
<td align="right">124.9%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">15,882,920</td>
<td align="right">35,598,510</td>
<td align="right">124.1%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,340,940</td>
<td align="right">2,981,399</td>
<td align="right">122.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">79,932,300</td>
<td align="right">174,929,814</td>
<td align="right">118.8%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">72,054,580</td>
<td align="right">157,323,847</td>
<td align="right">118.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">6,638,480</td>
<td align="right">14,320,257</td>
<td align="right">115.7%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">72,053,120</td>
<td align="right">155,373,591</td>
<td align="right">115.6%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">1,036,680</td>
<td align="right">2,217,961</td>
<td align="right">113.9%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">9,229,960</td>
<td align="right">19,677,949</td>
<td align="right">113.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">15,695,060</td>
<td align="right">33,229,389</td>
<td align="right">111.7%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">11,285,920</td>
<td align="right">22,851,345</td>
<td align="right">102.5%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">33,967,060</td>
<td align="right">68,390,732</td>
<td align="right">101.3%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">33,967,060</td>
<td align="right">68,390,732</td>
<td align="right">101.3%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">19,065,220</td>
<td align="right">37,614,056</td>
<td align="right">97.3%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">90,233,480</td>
<td align="right">174,966,346</td>
<td align="right">93.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">45,376,780</td>
<td align="right">86,802,932</td>
<td align="right">91.3%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">44,761,380</td>
<td align="right">82,253,521</td>
<td align="right">83.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">59,181,400</td>
<td align="right">108,014,711</td>
<td align="right">82.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">109,720</td>
<td align="right">187,217</td>
<td align="right">70.6%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">19,065,220</td>
<td align="right">32,184,367</td>
<td align="right">68.8%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">19,065,220</td>
<td align="right">32,184,367</td>
<td align="right">68.8%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">1,143,880</td>
<td align="right">1,887,206</td>
<td align="right">65.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">87,381,340</td>
<td align="right">139,827,423</td>
<td align="right">60.0%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">626,280</td>
<td align="right">937,573</td>
<td align="right">49.7%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">23,387,600</td>
<td align="right">34,368,606</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right">23,387,600</td>
<td align="right">34,366,607</td>
<td align="right">46.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">44,804,720</td>
<td align="right">65,306,967</td>
<td align="right">45.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right">2,626,340</td>
<td align="right">3,760,864</td>
<td align="right">43.2%</td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right">1,271,820</td>
<td align="right">1,682,520</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">31,106,760</td>
<td align="right">40,939,270</td>
<td align="right">31.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">11,956,860</td>
<td align="right">15,550,486</td>
<td align="right">30.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">49,693,640</td>
<td align="right">34,997,663</td>
<td align="right">-29.6%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">5,234,760</td>
<td align="right">6,749,300</td>
<td align="right">28.9%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">59,428,220</td>
<td align="right">76,511,416</td>
<td align="right">28.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">17,695,480</td>
<td align="right">22,545,661</td>
<td align="right">27.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">11,511,420</td>
<td align="right">14,618,679</td>
<td align="right">27.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">21,921,660</td>
<td align="right">26,960,816</td>
<td align="right">23.0%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">7,779,300</td>
<td align="right">9,405,415</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">7,779,300</td>
<td align="right">9,405,415</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">3,642,000</td>
<td align="right">2,894,255</td>
<td align="right">-20.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">8,199,520</td>
<td align="right">9,775,390</td>
<td align="right">19.2%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right">7,779,300</td>
<td align="right">9,225,310</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">24,228,340</td>
<td align="right">28,326,413</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">11,991,960</td>
<td align="right">13,847,922</td>
<td align="right">15.5%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">30,593,760</td>
<td align="right">35,256,635</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">30,593,760</td>
<td align="right">35,256,635</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">25,092,620</td>
<td align="right">28,850,637</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">8,377,620</td>
<td align="right">9,572,241</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">8,584,700</td>
<td align="right">9,399,525</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right">18,904,020</td>
<td align="right">20,544,479</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">1,391,440</td>
<td align="right">1,485,128</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">17,991,300</td>
<td align="right">18,875,958</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">27,849,440</td>
<td align="right">28,867,096</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">18,178,980</td>
<td align="right">17,643,139</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">45,997,320</td>
<td align="right">47,249,738</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">27,203,900</td>
<td align="right">27,917,524</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">15,558,600</td>
<td align="right">15,883,762</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">31,645,080</td>
<td align="right">31,183,692</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">31,645,080</td>
<td align="right">31,183,692</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">29,297,100</td>
<td align="right">29,481,252</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">8,700</td>
<td align="right">8,660</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">27,203,380</td>
<td align="right">27,293,805</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_LIST</td>
<td align="right">8,405,580</td>
<td align="right">8,406,249</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">8,405,580</td>
<td align="right">8,406,249</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">19,065,220</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">17,563,080</td>
<td align="right">17,563,080</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">1,252,560</td>
<td align="right">1,252,560</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">645,540</td>
<td align="right">645,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">645,540</td>
<td align="right">645,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">645,540</td>
<td align="right">645,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right"></td>
<td align="right">78,966,500</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">68,533,837</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right"></td>
<td align="right">46,378,043</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right"></td>
<td align="right">30,919,781</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right"></td>
<td align="right">28,998,828</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right"></td>
<td align="right">28,998,828</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right"></td>
<td align="right">28,653,503</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right"></td>
<td align="right">25,183,323</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right"></td>
<td align="right">25,070,210</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right">24,778,890</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_0</td>
<td align="right"></td>
<td align="right">24,078,641</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">11,665,655</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right"></td>
<td align="right">7,063,844</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right"></td>
<td align="right">6,052,340</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right"></td>
<td align="right">5,614,320</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right"></td>
<td align="right">5,614,320</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_CHECK_FUNC</td>
<td align="right"></td>
<td align="right">5,398,479</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_INIT_CALL</td>
<td align="right"></td>
<td align="right">5,398,479</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right"></td>
<td align="right">5,083,058</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_1</td>
<td align="right"></td>
<td align="right">4,392,452</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right"></td>
<td align="right">4,373,944</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right"></td>
<td align="right">4,373,944</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right"></td>
<td align="right">4,047,480</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right"></td>
<td align="right">4,047,480</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">1,944,766</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right"></td>
<td align="right">1,244,401</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right"></td>
<td align="right">959,595</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right"></td>
<td align="right">557,099</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right"></td>
<td align="right">556,985</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right"></td>
<td align="right">478,387</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">436,494</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right"></td>
<td align="right">430,643</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_2</td>
<td align="right"></td>
<td align="right">357,063</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">180,105</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_3</td>
<td align="right"></td>
<td align="right">155,946</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_KW</td>
<td align="right"></td>
<td align="right">107,712</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PY_FRAME_KW</td>
<td align="right"></td>
<td align="right">107,712</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LEN</td>
<td align="right"></td>
<td align="right">64,824</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NULL</td>
<td align="right"></td>
<td align="right">56,164</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_AND_ALLOCATE_OBJECT</td>
<td align="right"></td>
<td align="right">31,210</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CREATE_INIT_FRAME</td>
<td align="right"></td>
<td align="right">31,210</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_INIT_CHECK</td>
<td align="right"></td>
<td align="right">31,206</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT</td>
<td align="right"></td>
<td align="right">30,381</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right"></td>
<td align="right">736</td>
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
watched dict modification
<details>
<summary>ⓘ</summary>

A watched dict has been modified
</details>
</td>
<td align="right">120</td>
<td align="right">160</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
</details>
</td>
<td align="right">120</td>
<td align="right">160</td>
<td align="right">33.3%</td>
</tr>
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
