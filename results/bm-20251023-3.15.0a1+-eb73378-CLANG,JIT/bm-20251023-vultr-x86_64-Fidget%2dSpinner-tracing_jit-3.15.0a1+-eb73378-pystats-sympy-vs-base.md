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
<td align="left">FOR_ITER_GEN</td>
<td align="right">18,894,371</td>
<td align="right">2,676,000</td>
<td align="right">-85.8%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">28,018,365</td>
<td align="right">52,042,506</td>
<td align="right">85.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">8,932,372</td>
<td align="right">1,302,958</td>
<td align="right">-85.4%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">57,837,537</td>
<td align="right">13,342,857</td>
<td align="right">-76.9%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">7,912,120</td>
<td align="right">1,955,576</td>
<td align="right">-75.3%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">8,075,863</td>
<td align="right">2,119,709</td>
<td align="right">-73.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">9,826,261</td>
<td align="right">2,798,388</td>
<td align="right">-71.5%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">9,561,043</td>
<td align="right">3,256,945</td>
<td align="right">-65.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">34,180,774</td>
<td align="right">12,370,325</td>
<td align="right">-63.8%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">9,650,117</td>
<td align="right">3,612,698</td>
<td align="right">-62.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">10,894,658</td>
<td align="right">4,154,602</td>
<td align="right">-61.9%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">18,162,023</td>
<td align="right">7,669,849</td>
<td align="right">-57.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">22,393,113</td>
<td align="right">10,022,056</td>
<td align="right">-55.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">11,472,156</td>
<td align="right">5,340,374</td>
<td align="right">-53.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">55,366,574</td>
<td align="right">28,476,169</td>
<td align="right">-48.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">59,323,147</td>
<td align="right">31,673,176</td>
<td align="right">-46.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">56,876,825</td>
<td align="right">31,740,418</td>
<td align="right">-44.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">23,240,244</td>
<td align="right">12,988,977</td>
<td align="right">-44.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">53,052,765</td>
<td align="right">30,570,383</td>
<td align="right">-42.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">9,435,827</td>
<td align="right">5,513,889</td>
<td align="right">-41.6%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">2,995,134</td>
<td align="right">1,807,280</td>
<td align="right">-39.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">18,635,683</td>
<td align="right">11,286,860</td>
<td align="right">-39.4%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">39,349,034</td>
<td align="right">24,300,983</td>
<td align="right">-38.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">2,585,043</td>
<td align="right">1,621,529</td>
<td align="right">-37.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">2,008,406</td>
<td align="right">1,268,067</td>
<td align="right">-36.9%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">6,784,969</td>
<td align="right">4,531,374</td>
<td align="right">-33.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">20,999,560</td>
<td align="right">14,105,657</td>
<td align="right">-32.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">1,555,021</td>
<td align="right">1,063,157</td>
<td align="right">-31.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">32,173,305</td>
<td align="right">22,449,055</td>
<td align="right">-30.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">45,936,173</td>
<td align="right">32,058,932</td>
<td align="right">-30.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">6,744,103</td>
<td align="right">4,746,138</td>
<td align="right">-29.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">15,915,519</td>
<td align="right">11,258,473</td>
<td align="right">-29.3%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">24,730,483</td>
<td align="right">17,547,612</td>
<td align="right">-29.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">51,398,520</td>
<td align="right">36,494,087</td>
<td align="right">-29.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">5,469,042</td>
<td align="right">3,925,867</td>
<td align="right">-28.2%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">38,819,317</td>
<td align="right">28,195,215</td>
<td align="right">-27.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">4,001,426</td>
<td align="right">2,921,268</td>
<td align="right">-27.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">177,857,141</td>
<td align="right">131,978,425</td>
<td align="right">-25.8%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">43,171,173</td>
<td align="right">32,872,161</td>
<td align="right">-23.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">67,342,076</td>
<td align="right">51,311,092</td>
<td align="right">-23.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">44,785,650</td>
<td align="right">34,156,187</td>
<td align="right">-23.7%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">49,125,705</td>
<td align="right">37,611,842</td>
<td align="right">-23.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">45,122,303</td>
<td align="right">35,076,575</td>
<td align="right">-22.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">220,383,585</td>
<td align="right">172,135,750</td>
<td align="right">-21.9%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">17,492,716</td>
<td align="right">13,817,888</td>
<td align="right">-21.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">389,890</td>
<td align="right">308,826</td>
<td align="right">-20.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">18,031,127</td>
<td align="right">14,353,370</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">144,372,619</td>
<td align="right">116,170,601</td>
<td align="right">-19.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">654,574,663</td>
<td align="right">528,420,845</td>
<td align="right">-19.3%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">44,859,686</td>
<td align="right">36,598,302</td>
<td align="right">-18.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">198,998,090</td>
<td align="right">162,547,972</td>
<td align="right">-18.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">239,481,356</td>
<td align="right">196,351,023</td>
<td align="right">-18.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">30,430,644</td>
<td align="right">24,979,007</td>
<td align="right">-17.9%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">4,496,948</td>
<td align="right">3,708,281</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">15,116,051</td>
<td align="right">12,518,443</td>
<td align="right">-17.2%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">48,273,506</td>
<td align="right">39,992,747</td>
<td align="right">-17.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">15,238,518</td>
<td align="right">12,698,850</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">1,244,516</td>
<td align="right">1,043,940</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">21,789,830</td>
<td align="right">18,489,936</td>
<td align="right">-15.1%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">598,522</td>
<td align="right">508,738</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">341,720</td>
<td align="right">291,383</td>
<td align="right">-14.7%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">41,575,253</td>
<td align="right">35,604,637</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">173,246,742</td>
<td align="right">148,582,107</td>
<td align="right">-14.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">58,084,025</td>
<td align="right">49,895,512</td>
<td align="right">-14.1%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">12,416,318</td>
<td align="right">10,683,897</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">11,270,500</td>
<td align="right">9,699,426</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">388,827</td>
<td align="right">338,490</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">5,752,655</td>
<td align="right">5,011,843</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">21,701,162</td>
<td align="right">18,952,417</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">21,991,299</td>
<td align="right">19,207,916</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">60,042,574</td>
<td align="right">52,630,522</td>
<td align="right">-12.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">147,974,639</td>
<td align="right">130,820,638</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">6,589,086</td>
<td align="right">5,848,492</td>
<td align="right">-11.2%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">746,307</td>
<td align="right">665,243</td>
<td align="right">-10.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">17,760,314</td>
<td align="right">15,870,826</td>
<td align="right">-10.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">86,319,695</td>
<td align="right">77,282,190</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">33,137,363</td>
<td align="right">29,744,749</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">15,579,557</td>
<td align="right">14,066,061</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">13,376,551</td>
<td align="right">12,091,640</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">37,014,027</td>
<td align="right">33,529,776</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">181,840,907</td>
<td align="right">165,990,743</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">1,221,984</td>
<td align="right">1,120,966</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">13,932,554</td>
<td align="right">15,009,286</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">75,313,482</td>
<td align="right">69,499,753</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">32,102,169</td>
<td align="right">30,082,930</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">2,588,339</td>
<td align="right">2,436,854</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">24,804,597</td>
<td align="right">23,432,363</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">456,458</td>
<td align="right">433,071</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">655,239</td>
<td align="right">624,584</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">17,484,906</td>
<td align="right">16,719,440</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">6,812,476</td>
<td align="right">6,587,880</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">15,882,214</td>
<td align="right">15,366,379</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,758,800</td>
<td align="right">1,702,710</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">11,032,317</td>
<td align="right">11,290,050</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">2,281,375</td>
<td align="right">2,231,241</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">942,573</td>
<td align="right">924,775</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">1,028,890</td>
<td align="right">1,011,233</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,029,781</td>
<td align="right">1,012,124</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,287,951</td>
<td align="right">1,270,497</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">9,777,740</td>
<td align="right">9,902,495</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">8,907</td>
<td align="right">9,018</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">6,025,631</td>
<td align="right">5,976,018</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">7,541,074</td>
<td align="right">7,488,050</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">2,977</td>
<td align="right">2,960</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">4,181,570</td>
<td align="right">4,163,779</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">4,582,979</td>
<td align="right">4,563,814</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">78,733,730</td>
<td align="right">78,428,779</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">41,062</td>
<td align="right">41,191</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">995</td>
<td align="right">992</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">1,585,264</td>
<td align="right">1,581,496</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">18,074</td>
<td align="right">18,047</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">1,443</td>
<td align="right">1,445</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">3,725,220</td>
<td align="right">3,729,338</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">23,805</td>
<td align="right">23,780</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">744,768</td>
<td align="right">745,518</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">1,754,516</td>
<td align="right">1,753,326</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">165,631</td>
<td align="right">165,731</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">20,676</td>
<td align="right">20,688</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">10,386</td>
<td align="right">10,392</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">175,228</td>
<td align="right">175,321</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">171,959</td>
<td align="right">172,046</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">83,083</td>
<td align="right">83,125</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">495,198</td>
<td align="right">495,445</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">79,518</td>
<td align="right">79,545</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">7,102</td>
<td align="right">7,104</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">1,389,619</td>
<td align="right">1,389,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">2,418,163</td>
<td align="right">2,418,615</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">6,622,299</td>
<td align="right">6,623,427</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">654,411</td>
<td align="right">654,506</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">654,427</td>
<td align="right">654,522</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">10,869,424</td>
<td align="right">10,867,973</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">141,385</td>
<td align="right">141,402</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">655,239</td>
<td align="right">655,305</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">655,239</td>
<td align="right">655,305</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">2,007,307</td>
<td align="right">2,007,113</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">4,466,385</td>
<td align="right">4,466,739</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">10,926,983</td>
<td align="right">10,927,711</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">2,617,964</td>
<td align="right">2,618,080</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">21,976,587</td>
<td align="right">21,977,447</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">745,940</td>
<td align="right">745,961</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">2,174,471</td>
<td align="right">2,174,526</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">1,323,304</td>
<td align="right">1,323,310</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">427,538</td>
<td align="right">427,539</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">1,036,043</td>
<td align="right">1,036,043</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">372,870</td>
<td align="right">372,870</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">270,096</td>
<td align="right">270,096</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">232,942</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">178,539</td>
<td align="right">178,539</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">178,537</td>
<td align="right">178,537</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">133,724</td>
<td align="right">133,724</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">89,014</td>
<td align="right">89,014</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">14,629</td>
<td align="right">14,629</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">12,037</td>
<td align="right">12,037</td>
<td align="right">0.0%</td>
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
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">2,645</td>
<td align="right">2,645</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">1,679</td>
<td align="right">1,679</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">1,055</td>
<td align="right">1,055</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">591</td>
<td align="right">591</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">447</td>
<td align="right">447</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">394</td>
<td align="right">394</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">255</td>
<td align="right">255</td>
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
<td align="right">44,744,427</td>
<td align="right">38.6%</td>
<td align="right">34,115,733</td>
<td align="right">32.4%</td>
<td align="right">-23.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">70,802,703</td>
<td align="right">61.1%</td>
<td align="right">70,856,377</td>
<td align="right">67.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">358,493</td>
<td align="right">0.3%</td>
<td align="right">358,412</td>
<td align="right">0.3%</td>
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
<td align="right">39,080</td>
<td align="right">81.5%</td>
<td align="right">38,311</td>
<td align="right">81.2%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">8,875</td>
<td align="right">18.5%</td>
<td align="right">8,876</td>
<td align="right">18.8%</td>
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
<td align="right">4,570</td>
<td align="right">11.7%</td>
<td align="right">3,831</td>
<td align="right">10.0%</td>
<td align="right">-16.2%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">2,225</td>
<td align="right">5.7%</td>
<td align="right">2,096</td>
<td align="right">5.5%</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">6,669</td>
<td align="right">17.1%</td>
<td align="right">6,853</td>
<td align="right">17.9%</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">3,222</td>
<td align="right">8.2%</td>
<td align="right">3,138</td>
<td align="right">8.2%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">622</td>
<td align="right">1.6%</td>
<td align="right">636</td>
<td align="right">1.7%</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">705</td>
<td align="right">1.8%</td>
<td align="right">697</td>
<td align="right">1.8%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">2,142</td>
<td align="right">5.5%</td>
<td align="right">2,165</td>
<td align="right">5.7%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">1,010</td>
<td align="right">2.6%</td>
<td align="right">1,020</td>
<td align="right">2.7%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">1,759</td>
<td align="right">4.5%</td>
<td align="right">1,774</td>
<td align="right">4.6%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">7,170</td>
<td align="right">18.3%</td>
<td align="right">7,129</td>
<td align="right">18.6%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">3,899</td>
<td align="right">10.0%</td>
<td align="right">3,879</td>
<td align="right">10.1%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">1,207</td>
<td align="right">3.1%</td>
<td align="right">1,212</td>
<td align="right">3.2%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">570</td>
<td align="right">1.5%</td>
<td align="right">568</td>
<td align="right">1.5%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">981</td>
<td align="right">2.5%</td>
<td align="right">983</td>
<td align="right">2.6%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">1,086</td>
<td align="right">2.8%</td>
<td align="right">1,087</td>
<td align="right">2.8%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">422</td>
<td align="right">1.1%</td>
<td align="right">422</td>
<td align="right">1.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">363</td>
<td align="right">0.9%</td>
<td align="right">363</td>
<td align="right">0.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">211</td>
<td align="right">0.5%</td>
<td align="right">211</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">155</td>
<td align="right">0.4%</td>
<td align="right">155</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">91</td>
<td align="right">0.2%</td>
<td align="right">91</td>
<td align="right">0.2%</td>
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
<td align="right">12,037</td>
<td align="right">100.0%</td>
<td align="right">12,037</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">35,636,040</td>
<td align="right">11.4%</td>
<td align="right">35,225,807</td>
<td align="right">11.3%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">36,312,647</td>
<td align="right">11.6%</td>
<td align="right">35,896,971</td>
<td align="right">11.5%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">276,403,566</td>
<td align="right">88.4%</td>
<td align="right">275,875,471</td>
<td align="right">88.5%</td>
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
<td align="right">5,202</td>
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
<td align="right">700,412</td>
<td align="right">100.0%</td>
<td align="right">694,944</td>
<td align="right">100.0%</td>
<td align="right">-0.8%</td>
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
<td align="right">3,183</td>
<td align="right">74.9%</td>
<td align="right">3,183</td>
<td align="right">74.9%</td>
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
<td align="right">2,805</td>
<td align="right">66.0%</td>
<td align="right">2,805</td>
<td align="right">66.0%</td>
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
<td align="right">1,065</td>
<td align="right">100.0%</td>
<td align="right">1,067</td>
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
<td align="right">30,392,554</td>
<td align="right">37.1%</td>
<td align="right">24,942,701</td>
<td align="right">32.7%</td>
<td align="right">-17.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">402,441</td>
<td align="right">0.5%</td>
<td align="right">382,372</td>
<td align="right">0.5%</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">51,087,124</td>
<td align="right">62.4%</td>
<td align="right">50,903,093</td>
<td align="right">66.7%</td>
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
<td align="right">36,931</td>
<td align="right">80.9%</td>
<td align="right">35,157</td>
<td align="right">80.9%</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">8,696</td>
<td align="right">19.1%</td>
<td align="right">8,308</td>
<td align="right">19.1%</td>
<td align="right">-4.5%</td>
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
<td align="left">bool</td>
<td align="right">1,455</td>
<td align="right">3.9%</td>
<td align="right">713</td>
<td align="right">2.0%</td>
<td align="right">-51.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">7,108</td>
<td align="right">19.2%</td>
<td align="right">6,604</td>
<td align="right">18.8%</td>
<td align="right">-7.1%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">13,973</td>
<td align="right">37.8%</td>
<td align="right">13,591</td>
<td align="right">38.7%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">6,449</td>
<td align="right">17.5%</td>
<td align="right">6,304</td>
<td align="right">17.9%</td>
<td align="right">-2.2%</td>
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
<td align="left">set</td>
<td align="right">135</td>
<td align="right">0.4%</td>
<td align="right">136</td>
<td align="right">0.4%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">4,267</td>
<td align="right">11.6%</td>
<td align="right">4,264</td>
<td align="right">12.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">3,156</td>
<td align="right">8.5%</td>
<td align="right">3,156</td>
<td align="right">9.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">138</td>
<td align="right">0.4%</td>
<td align="right">138</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">91</td>
<td align="right">0.2%</td>
<td align="right">91</td>
<td align="right">0.3%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">10,889,134</td>
<td align="right">31.7%</td>
<td align="right">4,150,040</td>
<td align="right">15.0%</td>
<td align="right">-61.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">23,499,781</td>
<td align="right">68.3%</td>
<td align="right">23,500,427</td>
<td align="right">85.0%</td>
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
<td align="right">5,399</td>
<td align="right">97.7%</td>
<td align="right">4,437</td>
<td align="right">97.3%</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">125</td>
<td align="right">2.3%</td>
<td align="right">125</td>
<td align="right">2.7%</td>
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
<td align="right">3,447</td>
<td align="right">63.8%</td>
<td align="right">2,483</td>
<td align="right">56.0%</td>
<td align="right">-28.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">1,471</td>
<td align="right">27.2%</td>
<td align="right">1,473</td>
<td align="right">33.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">299</td>
<td align="right">5.5%</td>
<td align="right">299</td>
<td align="right">6.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">182</td>
<td align="right">3.4%</td>
<td align="right">182</td>
<td align="right">4.1%</td>
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
<td align="right">1,230,274</td>
<td align="right">1.1%</td>
<td align="right">550,819</td>
<td align="right">0.7%</td>
<td align="right">-55.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">45,884,625</td>
<td align="right">41.2%</td>
<td align="right">27,827,375</td>
<td align="right">37.1%</td>
<td align="right">-39.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">64,228,100</td>
<td align="right">57.7%</td>
<td align="right">42,488,091</td>
<td align="right">56.6%</td>
<td align="right">-33.8%</td>
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
<td align="right">213</td>
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
<td align="right">50,750</td>
<td align="right">68.0%</td>
<td align="right">4,230,771</td>
<td align="right">99.7%</td>
<td align="right">8,236.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">23,921</td>
<td align="right">32.0%</td>
<td align="right">11,202</td>
<td align="right">0.3%</td>
<td align="right">-53.2%</td>
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
<td align="right">38,081</td>
<td align="right">75.0%</td>
<td align="right">4,220,542</td>
<td align="right">99.8%</td>
<td align="right">10,983.1%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">6,297</td>
<td align="right">12.4%</td>
<td align="right">2,005</td>
<td align="right">0.0%</td>
<td align="right">-68.2%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">2,770</td>
<td align="right">5.5%</td>
<td align="right">4,485</td>
<td align="right">0.1%</td>
<td align="right">61.9%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">1,351</td>
<td align="right">2.7%</td>
<td align="right">1,467</td>
<td align="right">0.0%</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">557</td>
<td align="right">1.1%</td>
<td align="right">578</td>
<td align="right">0.0%</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">758</td>
<td align="right">1.5%</td>
<td align="right">758</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">382</td>
<td align="right">0.8%</td>
<td align="right">382</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">243</td>
<td align="right">0.5%</td>
<td align="right">243</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">194</td>
<td align="right">0.4%</td>
<td align="right">194</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">64</td>
<td align="right">0.1%</td>
<td align="right">64</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">29</td>
<td align="right">0.1%</td>
<td align="right">29</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">24</td>
<td align="right">0.0%</td>
<td align="right">24</td>
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
<td align="left">set</td>
<td align="right">7,167,769</td>
<td align="right">7,167,769 / 0 !!</td>
<td align="right">7,215,908</td>
<td align="right">7,215,908 / 0 !!</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">157,884</td>
<td align="right">157,884 / 0 !!</td>
<td align="right">157,953</td>
<td align="right">157,953 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">8,715,140</td>
<td align="right">8,715,140 / 0 !!</td>
<td align="right">8,716,209</td>
<td align="right">8,716,209 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">70,463</td>
<td align="right">70,463 / 0 !!</td>
<td align="right">70,468</td>
<td align="right">70,468 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">9,440,286</td>
<td align="right">9,440,286 / 0 !!</td>
<td align="right">9,440,573</td>
<td align="right">9,440,573 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">9,237,071</td>
<td align="right">9,237,071 / 0 !!</td>
<td align="right">9,237,176</td>
<td align="right">9,237,176 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">12,233,534</td>
<td align="right">12,233,534 / 0 !!</td>
<td align="right">12,233,660</td>
<td align="right">12,233,660 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">6,028</td>
<td align="right">6,028 / 0 !!</td>
<td align="right">6,028</td>
<td align="right">6,028 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">443</td>
<td align="right">443 / 0 !!</td>
<td align="right">443</td>
<td align="right">443 / 0 !!</td>
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
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">2,841</td>
<td align="right">0.0%</td>
<td align="right">284,000.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">52,795,937</td>
<td align="right">16.5%</td>
<td align="right">44,638,525</td>
<td align="right">16.0%</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">59,982,338</td>
<td align="right">18.8%</td>
<td align="right">52,570,500</td>
<td align="right">18.8%</td>
<td align="right">-12.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">206,737,527</td>
<td align="right">64.7%</td>
<td align="right">182,190,903</td>
<td align="right">65.2%</td>
<td align="right">-11.9%</td>
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
<td align="right">1,006,923</td>
<td align="right">95.7%</td>
<td align="right">854,554</td>
<td align="right">95.0%</td>
<td align="right">-15.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">45,079</td>
<td align="right">4.3%</td>
<td align="right">44,825</td>
<td align="right">5.0%</td>
<td align="right">-0.6%</td>
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
<td align="right">206</td>
<td align="right">0.5%</td>
<td align="right">230</td>
<td align="right">0.5%</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">3,097</td>
<td align="right">6.9%</td>
<td align="right">3,037</td>
<td align="right">6.8%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">2,728</td>
<td align="right">6.1%</td>
<td align="right">2,777</td>
<td align="right">6.2%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">21,394</td>
<td align="right">47.5%</td>
<td align="right">21,078</td>
<td align="right">47.0%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">4,062</td>
<td align="right">9.0%</td>
<td align="right">4,018</td>
<td align="right">9.0%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">2,324</td>
<td align="right">5.2%</td>
<td align="right">2,348</td>
<td align="right">5.2%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">3,142</td>
<td align="right">7.0%</td>
<td align="right">3,166</td>
<td align="right">7.1%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">6,850</td>
<td align="right">15.2%</td>
<td align="right">6,894</td>
<td align="right">15.4%</td>
<td align="right">0.6%</td>
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
<td align="left">property</td>
<td align="right">46</td>
<td align="right">0.1%</td>
<td align="right">46</td>
<td align="right">0.1%</td>
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
<td align="right">261,002,997</td>
<td align="right">100.0%</td>
<td align="right">229,224,804</td>
<td align="right">100.0%</td>
<td align="right">-12.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">4,551</td>
<td align="right">0.0%</td>
<td align="right">4,523</td>
<td align="right">0.0%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,339</td>
<td align="right">0.0%</td>
<td align="right">1,343</td>
<td align="right">0.0%</td>
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
<td align="left">Success</td>
<td align="right">13,571</td>
<td align="right">100.0%</td>
<td align="right">13,574</td>
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
<td align="right">2,265,877</td>
<td align="right">100.0%</td>
<td align="right">2,265,956</td>
<td align="right">100.0%</td>
<td align="right">0.0%</td>
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
<td align="right">731,596</td>
<td align="right">72.0%</td>
<td align="right">731,625</td>
<td align="right">72.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">268,986</td>
<td align="right">26.5%</td>
<td align="right">268,986</td>
<td align="right">26.5%</td>
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
<td align="right">1.4%</td>
<td align="right">14,711</td>
<td align="right">1.4%</td>
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
<td align="right">274</td>
<td align="right">19.8%</td>
<td align="right">274</td>
<td align="right">19.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,108</td>
<td align="right">80.2%</td>
<td align="right">1,108</td>
<td align="right">80.2%</td>
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
<td align="right">1,108</td>
<td align="right">100.0%</td>
<td align="right">1,108</td>
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
<td align="right">1,575,753</td>
<td align="right">17.4%</td>
<td align="right">1,577,424</td>
<td align="right">17.4%</td>
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
<td align="right">173,928</td>
<td align="right">1.9%</td>
<td align="right">174,013</td>
<td align="right">1.9%</td>
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
<td align="right">7,327,921</td>
<td align="right">80.7%</td>
<td align="right">7,327,581</td>
<td align="right">80.7%</td>
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
<td align="right">964</td>
<td align="right">3.1%</td>
<td align="right">972</td>
<td align="right">3.1%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">29,975</td>
<td align="right">96.9%</td>
<td align="right">30,015</td>
<td align="right">96.9%</td>
<td align="right">0.1%</td>
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
<td align="right">288</td>
<td align="right">29.9%</td>
<td align="right">294</td>
<td align="right">30.2%</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">518</td>
<td align="right">53.7%</td>
<td align="right">518</td>
<td align="right">53.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">102</td>
<td align="right">10.6%</td>
<td align="right">102</td>
<td align="right">10.5%</td>
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
<td align="right">591</td>
<td align="right">100.0%</td>
<td align="right">591</td>
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
<td align="right">2,582,924</td>
<td align="right">12.7%</td>
<td align="right">1,619,464</td>
<td align="right">8.4%</td>
<td align="right">-37.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">17,738,494</td>
<td align="right">87.3%</td>
<td align="right">17,738,348</td>
<td align="right">91.6%</td>
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
<td align="right">1,543</td>
<td align="right">72.8%</td>
<td align="right">1,489</td>
<td align="right">72.1%</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">576</td>
<td align="right">27.2%</td>
<td align="right">576</td>
<td align="right">27.9%</td>
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
<td align="right">1,543</td>
<td align="right">100.0%</td>
<td align="right">1,489</td>
<td align="right">100.0%</td>
<td align="right">-3.5%</td>
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
<td align="right">623,163</td>
<td align="right">0.4%</td>
<td align="right">425,982</td>
<td align="right">0.3%</td>
<td align="right">-31.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">164,185,495</td>
<td align="right">94.0%</td>
<td align="right">152,933,352</td>
<td align="right">93.7%</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">9,755,729</td>
<td align="right">5.6%</td>
<td align="right">9,883,371</td>
<td align="right">6.1%</td>
<td align="right">1.3%</td>
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
<td align="right">9</td>
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
<td align="right">14,272</td>
<td align="right">43.0%</td>
<td align="right">11,357</td>
<td align="right">42.7%</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">18,937</td>
<td align="right">57.0%</td>
<td align="right">15,265</td>
<td align="right">57.3%</td>
<td align="right">-19.4%</td>
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
<td align="right">2,616</td>
<td align="right">18.3%</td>
<td align="right">1,668</td>
<td align="right">14.7%</td>
<td align="right">-36.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">7,987</td>
<td align="right">56.0%</td>
<td align="right">5,976</td>
<td align="right">52.6%</td>
<td align="right">-25.2%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">726</td>
<td align="right">5.1%</td>
<td align="right">763</td>
<td align="right">6.7%</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">709</td>
<td align="right">5.0%</td>
<td align="right">720</td>
<td align="right">6.3%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">1,265</td>
<td align="right">8.9%</td>
<td align="right">1,261</td>
<td align="right">11.1%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">883</td>
<td align="right">6.2%</td>
<td align="right">883</td>
<td align="right">7.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">84</td>
<td align="right">0.6%</td>
<td align="right">84</td>
<td align="right">0.7%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">6,222</td>
<td align="right">0.0%</td>
<td align="right">6,324</td>
<td align="right">0.0%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">83,475,615</td>
<td align="right">100.0%</td>
<td align="right">83,673,107</td>
<td align="right">100.0%</td>
<td align="right">0.2%</td>
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
<td align="right">294</td>
<td align="right">10.9%</td>
<td align="right">303</td>
<td align="right">11.2%</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,391</td>
<td align="right">89.1%</td>
<td align="right">2,391</td>
<td align="right">88.8%</td>
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
<td align="right">251</td>
<td align="right">85.4%</td>
<td align="right">260</td>
<td align="right">85.8%</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">43</td>
<td align="right">14.6%</td>
<td align="right">43</td>
<td align="right">14.2%</td>
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
<td align="right">1,409,792,474</td>
<td align="right">32.9%</td>
<td align="right">1,070,825,965</td>
<td align="right">31.6%</td>
<td align="right">-24.0%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">249,822,409</td>
<td align="right">5.8%</td>
<td align="right">196,611,971</td>
<td align="right">5.8%</td>
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
<td align="right">2,534,454,661</td>
<td align="right">59.1%</td>
<td align="right">2,039,826,469</td>
<td align="right">60.2%</td>
<td align="right">-19.5%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">93,318,586</td>
<td align="right">2.2%</td>
<td align="right">83,850,386</td>
<td align="right">2.5%</td>
<td align="right">-10.1%</td>
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
<td align="right">10,889,134</td>
<td align="right">4.5%</td>
<td align="right">4,150,040</td>
<td align="right">2.2%</td>
<td align="right">-61.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">45,884,625</td>
<td align="right">19.1%</td>
<td align="right">27,827,375</td>
<td align="right">14.6%</td>
<td align="right">-39.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">2,582,924</td>
<td align="right">1.1%</td>
<td align="right">1,619,464</td>
<td align="right">0.8%</td>
<td align="right">-37.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">44,744,427</td>
<td align="right">18.6%</td>
<td align="right">34,115,733</td>
<td align="right">17.9%</td>
<td align="right">-23.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">30,392,554</td>
<td align="right">12.6%</td>
<td align="right">24,942,701</td>
<td align="right">13.1%</td>
<td align="right">-17.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">59,982,338</td>
<td align="right">25.0%</td>
<td align="right">52,570,500</td>
<td align="right">27.6%</td>
<td align="right">-12.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">9,755,729</td>
<td align="right">4.1%</td>
<td align="right">9,883,371</td>
<td align="right">5.2%</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">35,636,040</td>
<td align="right">14.8%</td>
<td align="right">35,225,807</td>
<td align="right">18.5%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">173,928</td>
<td align="right">0.1%</td>
<td align="right">174,013</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">268,986</td>
<td align="right">0.1%</td>
<td align="right">268,986</td>
<td align="right">0.1%</td>
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
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">12,905,619</td>
<td align="right">13.8%</td>
<td align="right">9,153,647</td>
<td align="right">10.9%</td>
<td align="right">-29.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">7,330,065</td>
<td align="right">7.9%</td>
<td align="right">5,687,757</td>
<td align="right">6.8%</td>
<td align="right">-22.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">6,163,681</td>
<td align="right">6.6%</td>
<td align="right">5,618,103</td>
<td align="right">6.7%</td>
<td align="right">-8.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">28,935,407</td>
<td align="right">31.0%</td>
<td align="right">26,414,282</td>
<td align="right">31.5%</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">3,207,465</td>
<td align="right">3.4%</td>
<td align="right">2,966,100</td>
<td align="right">3.5%</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">11,138,887</td>
<td align="right">11.9%</td>
<td align="right">11,262,899</td>
<td align="right">13.4%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,574,974</td>
<td align="right">1.7%</td>
<td align="right">1,576,645</td>
<td align="right">1.9%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">11,697,554</td>
<td align="right">12.5%</td>
<td align="right">11,702,936</td>
<td align="right">14.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">2,103,562</td>
<td align="right">2.3%</td>
<td align="right">2,103,784</td>
<td align="right">2.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">5,099,526</td>
<td align="right">5.5%</td>
<td align="right">5,099,597</td>
<td align="right">6.1%</td>
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
<td align="right">41,130,525</td>
<td align="right">19.6%</td>
<td align="right">40,823,938</td>
<td align="right">19.4%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">75,418,813</td>
<td align="right">35.9%</td>
<td align="right">75,113,482</td>
<td align="right">35.7%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">75,419,598</td>
<td align="right">35.9%</td>
<td align="right">75,114,267</td>
<td align="right">35.7%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">131,200,935</td>
<td align="right">62.5%</td>
<td align="right">131,716,391</td>
<td align="right">62.6%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">78,888,148</td>
<td align="right">37.5%</td>
<td align="right">78,583,197</td>
<td align="right">37.4%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">78,888,148</td>
<td align="right">37.5%</td>
<td align="right">78,583,197</td>
<td align="right">37.4%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">187,640,624</td>
<td align="right">89.3%</td>
<td align="right">187,730,140</td>
<td align="right">89.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">3,468,550</td>
<td align="right">1.7%</td>
<td align="right">3,468,930</td>
<td align="right">1.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">950,359</td>
<td align="right">0.5%</td>
<td align="right">950,320</td>
<td align="right">0.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">18,496,431</td>
<td align="right">8.8%</td>
<td align="right">18,497,158</td>
<td align="right">8.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">9,331,863</td>
<td align="right">4.4%</td>
<td align="right">9,332,090</td>
<td align="right">4.4%</td>
<td align="right">0.0%</td>
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
<td align="right">930,156</td>
<td align="right"></td>
<td align="right">667,660</td>
<td align="right"></td>
<td align="right">-28.2%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">3,352,125</td>
<td align="right"></td>
<td align="right">2,525,789</td>
<td align="right"></td>
<td align="right">-24.7%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">2,423,188</td>
<td align="right"></td>
<td align="right">1,859,612</td>
<td align="right"></td>
<td align="right">-23.3%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">1,117,487,305</td>
<td align="right">33.1%</td>
<td align="right">889,472,438</td>
<td align="right">26.4%</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">1,207,505,876</td>
<td align="right">35.8%</td>
<td align="right">1,444,153,109</td>
<td align="right">42.8%</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">8,976</td>
<td align="right">0.0%</td>
<td align="right">10,092</td>
<td align="right">0.0%</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">1,339,613,830</td>
<td align="right">36.8%</td>
<td align="right">1,495,176,269</td>
<td align="right">41.0%</td>
<td align="right">11.6%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">1,406,416,261</td>
<td align="right">38.6%</td>
<td align="right">1,259,691,079</td>
<td align="right">34.6%</td>
<td align="right">-10.4%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">51,280,583</td>
<td align="right">1.4%</td>
<td align="right">46,486,887</td>
<td align="right">1.3%</td>
<td align="right">-9.3%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">149,932,203</td>
<td align="right"></td>
<td align="right">143,198,600</td>
<td align="right"></td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">973,164,131</td>
<td align="right">28.8%</td>
<td align="right">962,946,983</td>
<td align="right">28.6%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">762,357</td>
<td align="right">0.2%</td>
<td align="right">768,449</td>
<td align="right">0.2%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">76,216,599</td>
<td align="right">2.3%</td>
<td align="right">75,864,894</td>
<td align="right">2.2%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">249,311,121</td>
<td align="right"></td>
<td align="right">248,757,794</td>
<td align="right"></td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">843,150,144</td>
<td align="right">23.2%</td>
<td align="right">841,581,176</td>
<td align="right">23.1%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">129,010,203</td>
<td align="right">26.8%</td>
<td align="right">129,147,030</td>
<td align="right">26.8%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">128,238,870</td>
<td align="right">26.7%</td>
<td align="right">128,368,489</td>
<td align="right">26.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">141,681,712</td>
<td align="right"></td>
<td align="right">141,815,772</td>
<td align="right"></td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">352,130,093</td>
<td align="right">73.2%</td>
<td align="right">352,208,772</td>
<td align="right">73.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">352,165,698</td>
<td align="right"></td>
<td align="right">352,244,372</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">866,173</td>
<td align="right"></td>
<td align="right">866,361</td>
<td align="right"></td>
<td align="right">0.0%</td>
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
<td align="right">18,802</td>
<td align="right"></td>
<td align="right">4,290,534</td>
<td align="right"></td>
<td align="right">22,719.6%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">119</td>
<td align="right">0.6%</td>
<td align="right">340</td>
<td align="right">0.0%</td>
<td align="right">185.7%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">1,593,708,513</td>
<td align="right">2,099.9%</td>
<td align="right">4,033,385,584</td>
<td align="right">2,888.5%</td>
<td align="right">153.1%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">2,052</td>
<td align="right">10.9%</td>
<td align="right">4,518</td>
<td align="right">0.1%</td>
<td align="right">120.2%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">5,789</td>
<td align="right">30.8%</td>
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
<td align="right">1,828</td>
<td align="right">9.7%</td>
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
<td align="right">151</td>
<td align="right">0.8%</td>
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
<td align="right">9,133</td>
<td align="right">48.6%</td>
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
<td align="right">75,894,497</td>
<td align="right"></td>
<td align="right">139,633,745</td>
<td align="right"></td>
<td align="right">84.0%</td>
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
<td align="right">1,816</td>
<td align="right">88.5%</td>
<td align="right">4,518</td>
<td align="right">100.0%</td>
<td align="right">148.8%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">2,052</td>
<td align="right"></td>
<td align="right">4,518</td>
<td align="right"></td>
<td align="right">120.2%</td>
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
<td align="right">8,307,816</td>
<td align="right">65.7%</td>
<td align="right">41,028,888</td>
<td align="right">79.8%</td>
<td align="right">393.9%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">12,644,352</td>
<td align="right"></td>
<td align="right">51,392,512</td>
<td align="right"></td>
<td align="right">306.4%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">249,640</td>
<td align="right">2.0%</td>
<td align="right">866,384</td>
<td align="right">1.7%</td>
<td align="right">247.1%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">4,085,080</td>
<td align="right">32.3%</td>
<td align="right">9,492,722</td>
<td align="right">18.5%</td>
<td align="right">132.4%</td>
</tr>
<tr>
<td align="left">
Freed memory size
<details>
<summary>ⓘ</summary>

The size of the memory freed from the JIT traces
</details>
</td>
<td align="right">110,592</td>
<td align="right">0.9%</td>
<td align="right">40,960</td>
<td align="right">0.1%</td>
<td align="right">-63.0%</td>
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
<td align="left">891</td>
<td align="right">49.1%</td>
<td align="left">1,387</td>
<td align="right">30.7%</td>
<td align="right">55.7%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">645</td>
<td align="right">35.5%</td>
<td align="left">1,522</td>
<td align="right">33.7%</td>
<td align="right">136.0%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">259</td>
<td align="right">14.3%</td>
<td align="left">867</td>
<td align="right">19.2%</td>
<td align="right">234.7%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">21</td>
<td align="right">1.2%</td>
<td align="left">654</td>
<td align="right">14.5%</td>
<td align="right">3,014.3%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">87</td>
<td align="right">1.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">1</td>
<td align="right">0.0%</td>
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
<td align="left"><= 8</td>
<td align="right">78</td>
<td align="right">3.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">257</td>
<td align="right">12.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">386</td>
<td align="right">18.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">944</td>
<td align="right">46.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">321</td>
<td align="right">15.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">45</td>
<td align="right">2.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">21</td>
<td align="right">1.0%</td>
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
<td align="right">56</td>
<td align="right">2.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">87</td>
<td align="right">4.2%</td>
<td align="right">87</td>
<td align="right">1.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">176</td>
<td align="right">8.6%</td>
<td align="right">416</td>
<td align="right">9.2%</td>
<td align="right">136.4%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">1,044</td>
<td align="right">50.9%</td>
<td align="right">1,380</td>
<td align="right">30.5%</td>
<td align="right">32.2%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">194</td>
<td align="right">9.5%</td>
<td align="right">1,199</td>
<td align="right">26.5%</td>
<td align="right">518.0%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">238</td>
<td align="right">11.6%</td>
<td align="right">810</td>
<td align="right">17.9%</td>
<td align="right">240.3%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">21</td>
<td align="right">1.0%</td>
<td align="right">567</td>
<td align="right">12.5%</td>
<td align="right">2,600.0%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">59</td>
<td align="right">1.3%</td>
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
<td align="left">_COMPARE_OP</td>
<td align="right">2,024</td>
<td align="right">5,499,363</td>
<td align="right">271,607.7%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">9,143</td>
<td align="right">22,655,081</td>
<td align="right">247,686.1%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">2,024</td>
<td align="right">2,255,936</td>
<td align="right">111,359.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">7,384</td>
<td align="right">6,404,049</td>
<td align="right">86,628.7%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">8,558</td>
<td align="right">3,403,291</td>
<td align="right">39,667.4%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">35,660</td>
<td align="right">7,141,449</td>
<td align="right">19,926.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">45,128</td>
<td align="right">7,674,471</td>
<td align="right">16,906.0%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">45,128</td>
<td align="right">7,674,471</td>
<td align="right">16,906.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">62,306</td>
<td align="right">7,065,072</td>
<td align="right">11,239.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">124,065</td>
<td align="right">10,413,588</td>
<td align="right">8,293.7%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">68,459</td>
<td align="right">4,725,352</td>
<td align="right">6,802.5%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">263,680</td>
<td align="right">17,315,347</td>
<td align="right">6,466.8%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,437,899</td>
<td align="right">44,136,000</td>
<td align="right">2,969.5%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_OVERFLOWED</td>
<td align="right">28,276</td>
<td align="right">710,295</td>
<td align="right">2,412.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right">258,585</td>
<td align="right">5,999,573</td>
<td align="right">2,220.2%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,437,899</td>
<td align="right">27,715,861</td>
<td align="right">1,827.5%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">1,242,953</td>
<td align="right">23,320,498</td>
<td align="right">1,776.2%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">1,242,953</td>
<td align="right">23,320,498</td>
<td align="right">1,776.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">1,064,624</td>
<td align="right">19,503,297</td>
<td align="right">1,731.9%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">1,437,899</td>
<td align="right">24,898,401</td>
<td align="right">1,631.6%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">2,005,157</td>
<td align="right">28,717,329</td>
<td align="right">1,332.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">3,053,388</td>
<td align="right">42,810,623</td>
<td align="right">1,302.1%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">2,345,257</td>
<td align="right">31,670,370</td>
<td align="right">1,250.4%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">18,228</td>
<td align="right">244,070</td>
<td align="right">1,239.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">1,668,159</td>
<td align="right">20,274,384</td>
<td align="right">1,115.4%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">4,822,082</td>
<td align="right">53,538,601</td>
<td align="right">1,010.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">1,072,541</td>
<td align="right">11,699,000</td>
<td align="right">990.8%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">3,149,240</td>
<td align="right">34,204,191</td>
<td align="right">986.1%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">1,437,899</td>
<td align="right">15,540,900</td>
<td align="right">980.8%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,437,899</td>
<td align="right">15,478,356</td>
<td align="right">976.5%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">174,242</td>
<td align="right">1,585,230</td>
<td align="right">809.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">5,347,693</td>
<td align="right">43,889,842</td>
<td align="right">720.7%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">1,763,669</td>
<td align="right">12,222,711</td>
<td align="right">593.0%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">1,437,899</td>
<td align="right">9,604,849</td>
<td align="right">568.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">5,912,933</td>
<td align="right">38,346,474</td>
<td align="right">548.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_DICT</td>
<td align="right">28,192</td>
<td align="right">180,073</td>
<td align="right">538.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">3,105,118</td>
<td align="right">19,120,769</td>
<td align="right">515.8%</td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right">12</td>
<td align="right">73</td>
<td align="right">508.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right">28,192</td>
<td align="right">171,121</td>
<td align="right">507.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">8,883,453</td>
<td align="right">53,484,483</td>
<td align="right">502.1%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">5,166</td>
<td align="right">28,635</td>
<td align="right">454.3%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">1,437,899</td>
<td align="right">7,780,838</td>
<td align="right">441.1%</td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right">1,437,899</td>
<td align="right">7,514,108</td>
<td align="right">422.6%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">2,168,932</td>
<td align="right">10,480,116</td>
<td align="right">383.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">1,609,444</td>
<td align="right">7,366,962</td>
<td align="right">357.7%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">1,024,726</td>
<td align="right">4,670,132</td>
<td align="right">355.7%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">1,046,440</td>
<td align="right">4,724,123</td>
<td align="right">351.4%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right">1,437,899</td>
<td align="right">6,336,097</td>
<td align="right">340.6%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">2,125,153</td>
<td align="right">9,019,140</td>
<td align="right">324.4%</td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right">1,129,773</td>
<td align="right">4,099,236</td>
<td align="right">262.8%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">1,024,726</td>
<td align="right">3,704,438</td>
<td align="right">261.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">24,336,500</td>
<td align="right">79,688,695</td>
<td align="right">227.4%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">13,302,974</td>
<td align="right">43,244,808</td>
<td align="right">225.1%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">3,872,706</td>
<td align="right">12,156,033</td>
<td align="right">213.9%</td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right">2,883,096</td>
<td align="right">8,903,475</td>
<td align="right">208.8%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">5,999,886</td>
<td align="right">16,683,131</td>
<td align="right">178.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">12,374,454</td>
<td align="right">32,890,221</td>
<td align="right">165.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">14,067,258</td>
<td align="right">35,964,587</td>
<td align="right">155.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">6,116,985</td>
<td align="right">15,597,010</td>
<td align="right">155.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">3,864,594</td>
<td align="right">9,593,386</td>
<td align="right">148.2%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">833,316</td>
<td align="right">2,023,861</td>
<td align="right">142.9%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">1,828,627</td>
<td align="right">4,427,136</td>
<td align="right">142.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">21,255,891</td>
<td align="right">50,458,606</td>
<td align="right">137.4%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">316,583,372</td>
<td align="right">746,927,982</td>
<td align="right">135.9%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">284,175,643</td>
<td align="right">667,093,799</td>
<td align="right">134.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">52,447</td>
<td align="right">108,873</td>
<td align="right">107.6%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">3,121,017</td>
<td align="right">6,400,313</td>
<td align="right">105.1%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">6,483,973</td>
<td align="right">13,264,302</td>
<td align="right">104.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">1,062,574</td>
<td align="right">2,160,174</td>
<td align="right">103.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">26,679,705</td>
<td align="right">53,785,039</td>
<td align="right">101.6%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">26,679,705</td>
<td align="right">53,767,168</td>
<td align="right">101.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">5,169,636</td>
<td align="right">42</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">5,038,597</td>
<td align="right">5,912</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">47,874,076</td>
<td align="right">94,189,831</td>
<td align="right">96.7%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">29,259,748</td>
<td align="right">56,510,121</td>
<td align="right">93.1%</td>
</tr>
<tr>
<td align="left">_COPY_2</td>
<td align="right">134,398</td>
<td align="right">256,866</td>
<td align="right">91.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">2,279,132</td>
<td align="right">4,345,121</td>
<td align="right">90.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">9,874,656</td>
<td align="right">18,082,588</td>
<td align="right">83.1%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">47,874,064</td>
<td align="right">87,590,501</td>
<td align="right">83.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">7,362,522</td>
<td align="right">13,061,842</td>
<td align="right">77.4%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">74,798,641</td>
<td align="right">132,368,628</td>
<td align="right">77.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">25,957,788</td>
<td align="right">45,789,488</td>
<td align="right">76.4%</td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">26,932</td>
<td align="right">46,230</td>
<td align="right">71.7%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">25,697,104</td>
<td align="right">43,734,710</td>
<td align="right">70.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">6,441,711</td>
<td align="right">10,914,971</td>
<td align="right">69.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">37,416,810</td>
<td align="right">63,182,178</td>
<td align="right">68.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">10,772,299</td>
<td align="right">18,186,171</td>
<td align="right">68.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">2,209,514</td>
<td align="right">3,720,537</td>
<td align="right">68.4%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">4,937,312</td>
<td align="right">8,237,760</td>
<td align="right">66.8%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">28,020,421</td>
<td align="right">45,443,914</td>
<td align="right">62.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">7,554,710</td>
<td align="right">12,180,325</td>
<td align="right">61.2%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">1,437,899</td>
<td align="right">2,255,504</td>
<td align="right">56.9%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">87,865,307</td>
<td align="right">136,140,750</td>
<td align="right">54.9%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">35,647,347</td>
<td align="right">54,317,016</td>
<td align="right">52.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right">2,162,477</td>
<td align="right">3,247,668</td>
<td align="right">50.2%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">26,080,855</td>
<td align="right">38,880,836</td>
<td align="right">49.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">3,222,435</td>
<td align="right">4,737,805</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">26,080,855</td>
<td align="right">38,222,399</td>
<td align="right">46.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">32,537,820</td>
<td align="right">47,544,715</td>
<td align="right">46.1%</td>
</tr>
<tr>
<td align="left">_SWAP_3</td>
<td align="right">2,201,073</td>
<td align="right">1,251,701</td>
<td align="right">-43.1%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">22,402,049</td>
<td align="right">31,585,351</td>
<td align="right">41.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,763,669</td>
<td align="right">2,429,388</td>
<td align="right">37.7%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">1,437,899</td>
<td align="right">958,542</td>
<td align="right">-33.3%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">1,567,863</td>
<td align="right">2,084,367</td>
<td align="right">32.9%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">1,567,863</td>
<td align="right">2,084,367</td>
<td align="right">32.9%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">4,937,312</td>
<td align="right">6,222,599</td>
<td align="right">26.0%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">15,791,327</td>
<td align="right">19,704,743</td>
<td align="right">24.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">3,350,352</td>
<td align="right">4,174,509</td>
<td align="right">24.6%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">8,175,151</td>
<td align="right">9,859,258</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">11,883,893</td>
<td align="right">14,238,041</td>
<td align="right">19.8%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">11,883,893</td>
<td align="right">14,238,041</td>
<td align="right">19.8%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">1,437,899</td>
<td align="right">1,662,875</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">2,125,148</td>
<td align="right">1,867,893</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">17,952,241</td>
<td align="right">19,496,035</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">39,991,231</td>
<td align="right">41,950,961</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">2,449,408</td>
<td align="right">2,453,569</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">2,513,400</td>
<td align="right">2,509,640</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">3,096</td>
<td align="right">3,092</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">71,346,826</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right"></td>
<td align="right">21,942,034</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">16,339,046</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right"></td>
<td align="right">15,900,947</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right"></td>
<td align="right">9,318,384</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_OVERFLOWED</td>
<td align="right"></td>
<td align="right">8,697,853</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right"></td>
<td align="right">8,352,457</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">7,351,376</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">7,351,376</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right"></td>
<td align="right">7,222,568</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">6,596,773</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right"></td>
<td align="right">6,048,015</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_COMMON_CONSTANT</td>
<td align="right"></td>
<td align="right">5,995,096</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right"></td>
<td align="right">5,994,717</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right"></td>
<td align="right">5,806,600</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">5,547,171</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right"></td>
<td align="right">3,909,881</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">3,795,771</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_PROPERTY_FRAME</td>
<td align="right"></td>
<td align="right">2,817,460</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right"></td>
<td align="right">2,812,497</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right"></td>
<td align="right">2,625,240</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right"></td>
<td align="right">2,373,329</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right"></td>
<td align="right">2,011,308</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right"></td>
<td align="right">1,998,318</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">1,698,975</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_FOR</td>
<td align="right"></td>
<td align="right">1,187,886</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PY_FRAME_GENERAL</td>
<td align="right"></td>
<td align="right">1,080,851</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right"></td>
<td align="right">1,007,758</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right"></td>
<td align="right">963,650</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right"></td>
<td align="right">789,455</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_IMPORT_FROM</td>
<td align="right"></td>
<td align="right">742,028</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_IMPORT_NAME</td>
<td align="right"></td>
<td align="right">741,940</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right"></td>
<td align="right">681,414</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right"></td>
<td align="right">681,414</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right"></td>
<td align="right">649,901</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_LIST</td>
<td align="right"></td>
<td align="right">543,398</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right"></td>
<td align="right">543,398</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right"></td>
<td align="right">438,324</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right"></td>
<td align="right">200,591</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NULL</td>
<td align="right"></td>
<td align="right">149,304</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_1</td>
<td align="right"></td>
<td align="right">136,589</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right"></td>
<td align="right">100,694</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right"></td>
<td align="right">100,674</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LEN</td>
<td align="right"></td>
<td align="right">98,967</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_KW_NON_PY</td>
<td align="right"></td>
<td align="right">89,796</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE_KW</td>
<td align="right"></td>
<td align="right">89,796</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_0</td>
<td align="right"></td>
<td align="right">85,224</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right"></td>
<td align="right">81,093</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SEND_GEN_FRAME</td>
<td align="right"></td>
<td align="right">81,093</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_TUPLE</td>
<td align="right"></td>
<td align="right">66,930</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right"></td>
<td align="right">66,213</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_KW</td>
<td align="right"></td>
<td align="right">53,644</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PY_FRAME_KW</td>
<td align="right"></td>
<td align="right">53,644</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right"></td>
<td align="right">50,620</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">50,620</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right"></td>
<td align="right">50,337</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_TYPE_1</td>
<td align="right"></td>
<td align="right">50,337</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right"></td>
<td align="right">50,337</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right"></td>
<td align="right">50,337</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION_AND_LOCK</td>
<td align="right"></td>
<td align="right">50,337</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">50,337</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right"></td>
<td align="right">50,337</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_EXCEPT</td>
<td align="right"></td>
<td align="right">30,721</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right"></td>
<td align="right">17,955</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right"></td>
<td align="right">17,871</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right"></td>
<td align="right">17,871</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_ATTR</td>
<td align="right"></td>
<td align="right">17,871</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right"></td>
<td align="right">17,871</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right"></td>
<td align="right">2,417</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">1,197</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE</td>
<td align="right"></td>
<td align="right">627</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right"></td>
<td align="right">616</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right"></td>
<td align="right">67</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_3</td>
<td align="right"></td>
<td align="right">47</td>
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
<td align="right">1,480</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">569</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND</td>
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
<td align="right">80</td>
<td align="right">80</td>
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
Stats gathered on: 2025-10-23
