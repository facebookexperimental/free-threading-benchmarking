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
<td align="right">23,254,743</td>
<td align="right">504</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">924,441</td>
<td align="right">113,194</td>
<td align="right">-87.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">947,389</td>
<td align="right">119,362</td>
<td align="right">-87.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,010,559</td>
<td align="right">181,370</td>
<td align="right">-82.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">1,186,634</td>
<td align="right">382,257</td>
<td align="right">-67.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">136,198</td>
<td align="right">59,156</td>
<td align="right">-56.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">136,198</td>
<td align="right">59,156</td>
<td align="right">-56.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">1,481,963</td>
<td align="right">645,880</td>
<td align="right">-56.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,701,234</td>
<td align="right">890,253</td>
<td align="right">-47.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">1,704,898</td>
<td align="right">900,805</td>
<td align="right">-47.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">170,513</td>
<td align="right">93,471</td>
<td align="right">-45.2%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">1,918,443</td>
<td align="right">1,098,408</td>
<td align="right">-42.7%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">198,170</td>
<td align="right">114,611</td>
<td align="right">-42.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">12,300,302</td>
<td align="right">8,167,067</td>
<td align="right">-33.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">2,583,217</td>
<td align="right">1,717,859</td>
<td align="right">-33.5%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">2,828,909</td>
<td align="right">1,980,909</td>
<td align="right">-30.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">5,695,596</td>
<td align="right">4,048,793</td>
<td align="right">-28.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">5,959,623</td>
<td align="right">4,333,139</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">3,169,791</td>
<td align="right">2,321,758</td>
<td align="right">-26.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">21,213,736</td>
<td align="right">16,253,669</td>
<td align="right">-23.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">8,933,582</td>
<td align="right">7,228,277</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">37,792</td>
<td align="right">30,999</td>
<td align="right">-18.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">50,899,131</td>
<td align="right">42,665,904</td>
<td align="right">-16.2%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">11,314,098</td>
<td align="right">9,502,947</td>
<td align="right">-16.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">5,464,471</td>
<td align="right">4,612,982</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">6,961,637</td>
<td align="right">5,985,004</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">36,173</td>
<td align="right">31,651</td>
<td align="right">-12.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">734,589</td>
<td align="right">643,260</td>
<td align="right">-12.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">562,636</td>
<td align="right">495,682</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">8,112,367</td>
<td align="right">7,151,323</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">214,551</td>
<td align="right">189,937</td>
<td align="right">-11.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">116,472</td>
<td align="right">103,153</td>
<td align="right">-11.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">24,644,418</td>
<td align="right">22,019,727</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">152,195</td>
<td align="right">136,369</td>
<td align="right">-10.4%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">193,617</td>
<td align="right">173,801</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">263,598</td>
<td align="right">238,984</td>
<td align="right">-9.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">9,281,618</td>
<td align="right">8,433,691</td>
<td align="right">-9.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">52,806</td>
<td align="right">48,284</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">255,124</td>
<td align="right">233,292</td>
<td align="right">-8.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">244,671</td>
<td align="right">225,025</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">338,855</td>
<td align="right">314,241</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">321,035</td>
<td align="right">298,824</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">14,904,974</td>
<td align="right">13,966,914</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">120,858</td>
<td align="right">114,176</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">119,767</td>
<td align="right">113,516</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">130,112</td>
<td align="right">123,327</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">174,659</td>
<td align="right">165,612</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,864,359</td>
<td align="right">1,776,273</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">96,376</td>
<td align="right">91,845</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">96,696</td>
<td align="right">92,165</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">20,951,179</td>
<td align="right">20,025,945</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">42,395</td>
<td align="right">40,544</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">481</td>
<td align="right">463</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">12,086</td>
<td align="right">11,680</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">59,626</td>
<td align="right">57,631</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">67,259</td>
<td align="right">65,266</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">77,458</td>
<td align="right">75,197</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,996,408</td>
<td align="right">2,910,164</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">3,420,630</td>
<td align="right">3,325,337</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">82,477</td>
<td align="right">80,484</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">5,454,847</td>
<td align="right">5,324,670</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">7,451,465</td>
<td align="right">7,280,402</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">1,178,149</td>
<td align="right">1,154,056</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,195,161</td>
<td align="right">1,171,068</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">6,314,950</td>
<td align="right">6,196,641</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">4,126,665</td>
<td align="right">4,051,244</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">4,555</td>
<td align="right">4,478</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,547,872</td>
<td align="right">2,506,051</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">2,093,778</td>
<td align="right">2,060,893</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">1,071,998</td>
<td align="right">1,055,690</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">28,803</td>
<td align="right">28,397</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">1,031,001</td>
<td align="right">1,017,965</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,931,894</td>
<td align="right">1,907,899</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">3,216</td>
<td align="right">3,178</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">2,576,461</td>
<td align="right">2,546,769</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">37,186</td>
<td align="right">36,780</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">37,186</td>
<td align="right">36,780</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">19,636,103</td>
<td align="right">19,425,865</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">2,465,889</td>
<td align="right">2,439,987</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">99</td>
<td align="right">98</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">651,284</td>
<td align="right">645,565</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">9,375,337</td>
<td align="right">9,298,295</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">372</td>
<td align="right">369</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,243,678</td>
<td align="right">1,234,474</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">900,227</td>
<td align="right">893,702</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">29,594,352</td>
<td align="right">29,383,476</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">156,100</td>
<td align="right">157,164</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">298,131</td>
<td align="right">296,408</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">9,697,107</td>
<td align="right">9,650,578</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">4,149,886</td>
<td align="right">4,132,834</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">4,519,456</td>
<td align="right">4,501,890</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">10,979,003</td>
<td align="right">10,941,307</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,652,556</td>
<td align="right">2,646,571</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">1,787,518</td>
<td align="right">1,783,528</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,047,446</td>
<td align="right">1,045,698</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,821,788</td>
<td align="right">1,819,527</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">182,455</td>
<td align="right">182,581</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">1,832,937</td>
<td align="right">1,833,735</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,018,848</td>
<td align="right">1,018,428</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">125,748</td>
<td align="right">125,730</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">134,150</td>
<td align="right">134,138</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">67,345</td>
<td align="right">67,339</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">3,614,914</td>
<td align="right">3,615,182</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">378,235</td>
<td align="right">378,217</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">42,279</td>
<td align="right">42,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">152,407</td>
<td align="right">152,408</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">10,060,280</td>
<td align="right">10,060,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">9,238,062</td>
<td align="right">9,238,062</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">846,831</td>
<td align="right">846,831</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">209,141</td>
<td align="right">209,141</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">209,111</td>
<td align="right">209,111</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">167,920</td>
<td align="right">167,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">152,236</td>
<td align="right">152,236</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">143,145</td>
<td align="right">143,145</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">109,943</td>
<td align="right">109,943</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">109,939</td>
<td align="right">109,939</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">85,611</td>
<td align="right">85,611</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">84,508</td>
<td align="right">84,508</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">75,892</td>
<td align="right">75,892</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">75,849</td>
<td align="right">75,849</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">60,372</td>
<td align="right">60,372</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">58,817</td>
<td align="right">58,817</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">58,678</td>
<td align="right">58,678</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">55,847</td>
<td align="right">55,847</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">42,708</td>
<td align="right">42,708</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">41,788</td>
<td align="right">41,788</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">40,440</td>
<td align="right">40,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">34,449</td>
<td align="right">34,449</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">34,044</td>
<td align="right">34,044</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">26,619</td>
<td align="right">26,619</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">25,317</td>
<td align="right">25,317</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">25,152</td>
<td align="right">25,152</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">18,700</td>
<td align="right">18,700</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">16,808</td>
<td align="right">16,808</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">16,766</td>
<td align="right">16,766</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">8,387</td>
<td align="right">8,387</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">WITH_EXCEPT_START</td>
<td align="right">8,383</td>
<td align="right">8,383</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">785</td>
<td align="right">785</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">491</td>
<td align="right">491</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">391</td>
<td align="right">391</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">315</td>
<td align="right">315</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">207</td>
<td align="right">207</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">181</td>
<td align="right">181</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">153</td>
<td align="right">153</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">149</td>
<td align="right">149</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">129</td>
<td align="right">129</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">128</td>
<td align="right">128</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">68</td>
<td align="right">68</td>
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
<td align="left">BUILD_SET</td>
<td align="right">1</td>
<td align="right">1</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">1</td>
<td align="right">1</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">1</td>
<td align="right">1</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right"></td>
<td align="right">21,494,279</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right"></td>
<td align="right">847,614</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right"></td>
<td align="right">16,553</td>
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
<td align="right">3,362,690</td>
<td align="right">76.5%</td>
<td align="right">2,298,615</td>
<td align="right">69.1%</td>
<td align="right">-31.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">13,261</td>
<td align="right">0.3%</td>
<td align="right">10,268</td>
<td align="right">0.3%</td>
<td align="right">-22.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,017,681</td>
<td align="right">23.2%</td>
<td align="right">1,017,263</td>
<td align="right">30.6%</td>
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
<td align="right">516</td>
<td align="right">36.3%</td>
<td align="right">458</td>
<td align="right">33.7%</td>
<td align="right">-11.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">904</td>
<td align="right">63.7%</td>
<td align="right">901</td>
<td align="right">66.3%</td>
<td align="right">-0.3%</td>
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
<td align="left">subscr deque</td>
<td align="right">79</td>
<td align="right">8.7%</td>
<td align="right">78</td>
<td align="right">8.7%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">302</td>
<td align="right">33.4%</td>
<td align="right">300</td>
<td align="right">33.3%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">252</td>
<td align="right">27.9%</td>
<td align="right">252</td>
<td align="right">28.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">189</td>
<td align="right">20.9%</td>
<td align="right">189</td>
<td align="right">21.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">66</td>
<td align="right">7.3%</td>
<td align="right">66</td>
<td align="right">7.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr bytes</td>
<td align="right">8</td>
<td align="right">0.9%</td>
<td align="right">8</td>
<td align="right">0.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">6</td>
<td align="right">0.7%</td>
<td align="right">6</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr other slice</td>
<td align="right">2</td>
<td align="right">0.2%</td>
<td align="right">2</td>
<td align="right">0.2%</td>
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
<td align="right">26,619</td>
<td align="right">100.0%</td>
<td align="right">26,619</td>
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
<td align="right">14,319,024</td>
<td align="right">100.0%</td>
<td align="right">12,431,534</td>
<td align="right">100.0%</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,138</td>
<td align="right">0.0%</td>
<td align="right">2,086</td>
<td align="right">0.0%</td>
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
<td align="right">955</td>
<td align="right">0.0%</td>
<td align="right">955</td>
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
<td align="right">3,372</td>
<td align="right">100.0%</td>
<td align="right">3,347</td>
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
<td align="right">23.2%</td>
<td align="right">42</td>
<td align="right">23.2%</td>
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
<td align="right">139</td>
<td align="right">100.0%</td>
<td align="right">139</td>
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
<td align="right">18,251</td>
<td align="right">0.4%</td>
<td align="right">16,002</td>
<td align="right">0.4%</td>
<td align="right">-12.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">119,858</td>
<td align="right">2.7%</td>
<td align="right">113,251</td>
<td align="right">2.6%</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,269,453</td>
<td align="right">96.8%</td>
<td align="right">4,243,539</td>
<td align="right">97.0%</td>
<td align="right">-0.6%</td>
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
<td align="right">727</td>
<td align="right">54.3%</td>
<td align="right">656</td>
<td align="right">53.9%</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">612</td>
<td align="right">45.7%</td>
<td align="right">562</td>
<td align="right">46.1%</td>
<td align="right">-8.2%</td>
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
<td align="right">338</td>
<td align="right">46.5%</td>
<td align="right">269</td>
<td align="right">41.0%</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">245</td>
<td align="right">33.7%</td>
<td align="right">243</td>
<td align="right">37.0%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">98</td>
<td align="right">13.5%</td>
<td align="right">98</td>
<td align="right">14.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">46</td>
<td align="right">6.3%</td>
<td align="right">46</td>
<td align="right">7.0%</td>
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
<td align="right">947,780</td>
<td align="right">100.0%</td>
<td align="right">119,753</td>
<td align="right">99.7%</td>
<td align="right">-87.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">264</td>
<td align="right">0.0%</td>
<td align="right">264</td>
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
<td align="right">8</td>
<td align="right">15.7%</td>
<td align="right">8</td>
<td align="right">15.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">43</td>
<td align="right">84.3%</td>
<td align="right">43</td>
<td align="right">84.3%</td>
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
<td align="right">43</td>
<td align="right">100.0%</td>
<td align="right">43</td>
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
<td align="right">1,863,638</td>
<td align="right">8.9%</td>
<td align="right">1,775,569</td>
<td align="right">8.5%</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">19,099,730</td>
<td align="right">91.1%</td>
<td align="right">19,046,416</td>
<td align="right">91.5%</td>
<td align="right">-0.3%</td>
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
<td align="right">53</td>
<td align="right">7.4%</td>
<td align="right">57</td>
<td align="right">8.1%</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">668</td>
<td align="right">92.6%</td>
<td align="right">647</td>
<td align="right">91.9%</td>
<td align="right">-3.1%</td>
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
<td align="right">78</td>
<td align="right">11.7%</td>
<td align="right">57</td>
<td align="right">8.8%</td>
<td align="right">-26.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">252</td>
<td align="right">37.7%</td>
<td align="right">252</td>
<td align="right">38.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">252</td>
<td align="right">37.7%</td>
<td align="right">252</td>
<td align="right">38.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">71</td>
<td align="right">10.6%</td>
<td align="right">71</td>
<td align="right">11.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">7</td>
<td align="right">1.0%</td>
<td align="right">7</td>
<td align="right">1.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">3</td>
<td align="right">0.4%</td>
<td align="right">3</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">2</td>
<td align="right">0.3%</td>
<td align="right">2</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">2</td>
<td align="right">0.3%</td>
<td align="right">2</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">1</td>
<td align="right">0.1%</td>
<td align="right">1</td>
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
<td align="left">self</td>
<td align="right">43,419</td>
<td align="right">43,419 / 0 !!</td>
<td align="right">41,158</td>
<td align="right">41,158 / 0 !!</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">1,067,239</td>
<td align="right">1,067,239 / 0 !!</td>
<td align="right">1,045,407</td>
<td align="right">1,045,407 / 0 !!</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">42,250</td>
<td align="right">42,250 / 0 !!</td>
<td align="right">42,250</td>
<td align="right">42,250 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">17,069</td>
<td align="right">17,069 / 0 !!</td>
<td align="right">17,069</td>
<td align="right">17,069 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">16,766</td>
<td align="right">16,766 / 0 !!</td>
<td align="right">16,766</td>
<td align="right">16,766 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">8,383</td>
<td align="right">8,383 / 0 !!</td>
<td align="right">8,383</td>
<td align="right">8,383 / 0 !!</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">31,909,991</td>
<td align="right">88.3%</td>
<td align="right">25,156,972</td>
<td align="right">85.9%</td>
<td align="right">-21.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">3,410,213</td>
<td align="right">9.4%</td>
<td align="right">3,314,986</td>
<td align="right">11.3%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">801,233</td>
<td align="right">2.2%</td>
<td align="right">800,624</td>
<td align="right">2.7%</td>
<td align="right">-0.1%</td>
</tr>
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
<td align="right">6</td>
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
<td align="right">5,855</td>
<td align="right">22.8%</td>
<td align="right">5,814</td>
<td align="right">22.7%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">19,861</td>
<td align="right">77.2%</td>
<td align="right">19,836</td>
<td align="right">77.3%</td>
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
<td align="left">overriding descriptor</td>
<td align="right">879</td>
<td align="right">15.0%</td>
<td align="right">861</td>
<td align="right">14.8%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">720</td>
<td align="right">12.3%</td>
<td align="right">712</td>
<td align="right">12.2%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">667</td>
<td align="right">11.4%</td>
<td align="right">666</td>
<td align="right">11.5%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,791</td>
<td align="right">30.6%</td>
<td align="right">1,790</td>
<td align="right">30.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">464</td>
<td align="right">7.9%</td>
<td align="right">464</td>
<td align="right">8.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">72</td>
<td align="right">1.2%</td>
<td align="right">72</td>
<td align="right">1.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">69</td>
<td align="right">1.2%</td>
<td align="right">69</td>
<td align="right">1.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">45</td>
<td align="right">0.8%</td>
<td align="right">45</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">23</td>
<td align="right">0.4%</td>
<td align="right">23</td>
<td align="right">0.4%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">821</td>
<td align="right">0.0%</td>
<td align="right">793</td>
<td align="right">0.0%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">11,577,905</td>
<td align="right">100.0%</td>
<td align="right">11,331,421</td>
<td align="right">100.0%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2</td>
<td align="right">0.0%</td>
<td align="right">2</td>
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
<td align="right">225</td>
<td align="right">0.0%</td>
<td align="right">225</td>
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
<td align="right">2,401</td>
<td align="right">100.0%</td>
<td align="right">2,391</td>
<td align="right">100.0%</td>
<td align="right">-0.4%</td>
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
<td align="right">254,991</td>
<td align="right">100.0%</td>
<td align="right">230,377</td>
<td align="right">100.0%</td>
<td align="right">-9.7%</td>
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
<td align="right">55</td>
<td align="right">100.0%</td>
<td align="right">55</td>
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
<td align="right">2,868,988</td>
<td align="right">85.9%</td>
<td align="right">2,020,955</td>
<td align="right">81.1%</td>
<td align="right">-29.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">150,663</td>
<td align="right">4.5%</td>
<td align="right">150,663</td>
<td align="right">6.0%</td>
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
<td align="right">9.6%</td>
<td align="right">319,503</td>
<td align="right">12.8%</td>
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
<td align="right">7,203</td>
<td align="right">90.5%</td>
<td align="right">7,204</td>
<td align="right">90.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">754</td>
<td align="right">9.5%</td>
<td align="right">754</td>
<td align="right">9.5%</td>
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
<td align="right">567</td>
<td align="right">75.2%</td>
<td align="right">554</td>
<td align="right">73.5%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">349</td>
<td align="right">46.3%</td>
<td align="right">349</td>
<td align="right">46.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">208</td>
<td align="right">27.6%</td>
<td align="right">208</td>
<td align="right">27.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">44</td>
<td align="right">5.8%</td>
<td align="right">44</td>
<td align="right">5.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">11</td>
<td align="right">1.5%</td>
<td align="right">11</td>
<td align="right">1.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">2</td>
<td align="right">0.3%</td>
<td align="right">2</td>
<td align="right">0.3%</td>
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
<td align="right">1,071,998</td>
<td align="right">96.2%</td>
<td align="right">1,055,690</td>
<td align="right">96.1%</td>
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
<td align="right">42,069</td>
<td align="right">3.8%</td>
<td align="right">42,069</td>
<td align="right">3.8%</td>
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
<td align="right">20</td>
<td align="right">9.5%</td>
<td align="right">21</td>
<td align="right">10.0%</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">190</td>
<td align="right">90.5%</td>
<td align="right">190</td>
<td align="right">90.0%</td>
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
<td align="right">121</td>
<td align="right">63.7%</td>
<td align="right">121</td>
<td align="right">63.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">69</td>
<td align="right">36.3%</td>
<td align="right">69</td>
<td align="right">36.3%</td>
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
<td align="right">3,647,896</td>
<td align="right">77.7%</td>
<td align="right">3,525,784</td>
<td align="right">77.1%</td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,046,045</td>
<td align="right">22.3%</td>
<td align="right">1,044,291</td>
<td align="right">22.8%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
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
<td align="left">Failure</td>
<td align="right">934</td>
<td align="right">66.6%</td>
<td align="right">938</td>
<td align="right">66.6%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">469</td>
<td align="right">33.4%</td>
<td align="right">471</td>
<td align="right">33.4%</td>
<td align="right">0.4%</td>
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
<td align="right">141</td>
<td align="right">15.1%</td>
<td align="right">151</td>
<td align="right">16.1%</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">294</td>
<td align="right">31.5%</td>
<td align="right">288</td>
<td align="right">30.7%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">321</td>
<td align="right">34.4%</td>
<td align="right">321</td>
<td align="right">34.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">112</td>
<td align="right">12.0%</td>
<td align="right">112</td>
<td align="right">11.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">memory view</td>
<td align="right">44</td>
<td align="right">4.7%</td>
<td align="right">44</td>
<td align="right">4.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">22</td>
<td align="right">2.4%</td>
<td align="right">22</td>
<td align="right">2.3%</td>
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
<td align="right">3,488,752</td>
<td align="right">100.0%</td>
<td align="right">2,673,781</td>
<td align="right">100.0%</td>
<td align="right">-23.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">38</td>
<td align="right">0.0%</td>
<td align="right">38</td>
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
<td align="right">111</td>
<td align="right">100.0%</td>
<td align="right">111</td>
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
<td align="right">261,170,687</td>
<td align="right">60.6%</td>
<td align="right">232,437,898</td>
<td align="right">60.2%</td>
<td align="right">-11.0%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">159,410,277</td>
<td align="right">37.0%</td>
<td align="right">143,749,020</td>
<td align="right">37.2%</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">8,897,091</td>
<td align="right">2.1%</td>
<td align="right">8,680,656</td>
<td align="right">2.2%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,153,459</td>
<td align="right">0.3%</td>
<td align="right">1,147,608</td>
<td align="right">0.3%</td>
<td align="right">-0.5%</td>
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
<td align="left">COMPARE_OP</td>
<td align="right">119,858</td>
<td align="right">1.6%</td>
<td align="right">113,251</td>
<td align="right">1.5%</td>
<td align="right">-5.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,863,638</td>
<td align="right">24.3%</td>
<td align="right">1,775,569</td>
<td align="right">23.7%</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">821</td>
<td align="right">0.0%</td>
<td align="right">793</td>
<td align="right">0.0%</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">3,410,213</td>
<td align="right">44.4%</td>
<td align="right">3,314,986</td>
<td align="right">44.3%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">2,138</td>
<td align="right">0.0%</td>
<td align="right">2,086</td>
<td align="right">0.0%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,046,045</td>
<td align="right">13.6%</td>
<td align="right">1,044,291</td>
<td align="right">13.9%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,017,681</td>
<td align="right">13.3%</td>
<td align="right">1,017,263</td>
<td align="right">13.6%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">150,663</td>
<td align="right">2.0%</td>
<td align="right">150,663</td>
<td align="right">2.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">42,069</td>
<td align="right">0.5%</td>
<td align="right">42,069</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">26,619</td>
<td align="right">0.3%</td>
<td align="right">26,619</td>
<td align="right">0.4%</td>
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
<td align="right">6,615</td>
<td align="right">0.6%</td>
<td align="right">5,033</td>
<td align="right">0.4%</td>
<td align="right">-23.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">6,646</td>
<td align="right">0.6%</td>
<td align="right">5,235</td>
<td align="right">0.5%</td>
<td align="right">-21.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">18,250</td>
<td align="right">1.6%</td>
<td align="right">16,001</td>
<td align="right">1.4%</td>
<td align="right">-12.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">680,100</td>
<td align="right">59.0%</td>
<td align="right">679,535</td>
<td align="right">59.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">100,837</td>
<td align="right">8.7%</td>
<td align="right">100,793</td>
<td align="right">8.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">319,503</td>
<td align="right">27.7%</td>
<td align="right">319,503</td>
<td align="right">27.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">20,147</td>
<td align="right">1.7%</td>
<td align="right">20,147</td>
<td align="right">1.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">397</td>
<td align="right">0.0%</td>
<td align="right">397</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">275</td>
<td align="right">0.0%</td>
<td align="right">275</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">139</td>
<td align="right">0.0%</td>
<td align="right">139</td>
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
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">301,210</td>
<td align="right">1.0%</td>
<td align="right">296,673</td>
<td align="right">1.0%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">37,200</td>
<td align="right">0.1%</td>
<td align="right">36,794</td>
<td align="right">0.1%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">19,644,492</td>
<td align="right">66.3%</td>
<td align="right">19,434,618</td>
<td align="right">66.1%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">18,632,630</td>
<td align="right">62.9%</td>
<td align="right">18,460,440</td>
<td align="right">62.8%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">10,139,927</td>
<td align="right">34.2%</td>
<td align="right">10,102,243</td>
<td align="right">34.3%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">10,139,985</td>
<td align="right">34.2%</td>
<td align="right">10,102,301</td>
<td align="right">34.3%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">10,987,520</td>
<td align="right">37.1%</td>
<td align="right">10,949,836</td>
<td align="right">37.2%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">10,987,520</td>
<td align="right">37.1%</td>
<td align="right">10,949,836</td>
<td align="right">37.2%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">847,535</td>
<td align="right">2.9%</td>
<td align="right">847,535</td>
<td align="right">2.9%</td>
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
<td align="right">905,751</td>
<td align="right">3.1%</td>
<td align="right">905,751</td>
<td align="right">3.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">882,468</td>
<td align="right">3.0%</td>
<td align="right">882,468</td>
<td align="right">3.0%</td>
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
<td align="right">17,046</td>
<td align="right"></td>
<td align="right">871,319</td>
<td align="right"></td>
<td align="right">5,011.6%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">55,171</td>
<td align="right"></td>
<td align="right">914,663</td>
<td align="right"></td>
<td align="right">1,557.9%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">38,373</td>
<td align="right"></td>
<td align="right">43,610</td>
<td align="right"></td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">8,761,895</td>
<td align="right"></td>
<td align="right">7,824,276</td>
<td align="right"></td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">436,688</td>
<td align="right"></td>
<td align="right">419,112</td>
<td align="right"></td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">3,950,067</td>
<td align="right"></td>
<td align="right">3,826,816</td>
<td align="right"></td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">34,897,891</td>
<td align="right">17.5%</td>
<td align="right">35,336,483</td>
<td align="right">17.8%</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">35,107,506</td>
<td align="right">15.6%</td>
<td align="right">35,508,527</td>
<td align="right">15.8%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">5,596,234</td>
<td align="right">2.8%</td>
<td align="right">5,544,575</td>
<td align="right">2.8%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">18,842,463</td>
<td align="right"></td>
<td align="right">18,669,320</td>
<td align="right"></td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">18,841,207</td>
<td align="right">56.6%</td>
<td align="right">18,668,275</td>
<td align="right">56.5%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">45,049,109</td>
<td align="right">22.6%</td>
<td align="right">45,442,311</td>
<td align="right">22.8%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">128,121,221</td>
<td align="right">56.9%</td>
<td align="right">127,101,879</td>
<td align="right">56.5%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">113,434,741</td>
<td align="right">57.0%</td>
<td align="right">112,589,047</td>
<td align="right">56.6%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">1,257,717</td>
<td align="right">0.6%</td>
<td align="right">1,248,907</td>
<td align="right">0.6%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">60,750,422</td>
<td align="right">27.0%</td>
<td align="right">61,101,510</td>
<td align="right">27.2%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">14,733,579</td>
<td align="right"></td>
<td align="right">14,649,431</td>
<td align="right"></td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">14,258,339</td>
<td align="right">42.8%</td>
<td align="right">14,188,739</td>
<td align="right">42.9%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">14,470,965</td>
<td align="right">43.4%</td>
<td align="right">14,401,370</td>
<td align="right">43.5%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">139,970</td>
<td align="right">0.4%</td>
<td align="right">139,975</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">72,656</td>
<td align="right">0.2%</td>
<td align="right">72,656</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">640</td>
<td align="right">0.1%</td>
<td align="right">640</td>
<td align="right">0.2%</td>
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
Stats gathered on: 2025-08-03
