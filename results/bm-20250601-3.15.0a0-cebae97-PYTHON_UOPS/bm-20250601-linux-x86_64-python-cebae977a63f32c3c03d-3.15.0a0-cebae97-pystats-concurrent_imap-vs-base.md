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
<td align="right">23,258,072</td>
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
<td align="right">949,879</td>
<td align="right">125,417</td>
<td align="right">-86.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,014,048</td>
<td align="right">192,354</td>
<td align="right">-81.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">1,184,147</td>
<td align="right">381,304</td>
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
<td align="right">1,483,174</td>
<td align="right">650,072</td>
<td align="right">-56.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,701,168</td>
<td align="right">890,361</td>
<td align="right">-47.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">1,704,896</td>
<td align="right">900,244</td>
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
<td align="right">1,919,830</td>
<td align="right">1,102,385</td>
<td align="right">-42.6%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">199,213</td>
<td align="right">117,622</td>
<td align="right">-41.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">12,302,287</td>
<td align="right">8,192,370</td>
<td align="right">-33.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">2,587,876</td>
<td align="right">1,734,512</td>
<td align="right">-33.0%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">2,831,954</td>
<td align="right">1,999,568</td>
<td align="right">-29.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">5,690,525</td>
<td align="right">4,060,653</td>
<td align="right">-28.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">5,960,233</td>
<td align="right">4,335,289</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">3,176,704</td>
<td align="right">2,341,062</td>
<td align="right">-26.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">21,219,038</td>
<td align="right">16,298,279</td>
<td align="right">-23.2%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">8,939,137</td>
<td align="right">7,254,593</td>
<td align="right">-18.8%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">11,316,681</td>
<td align="right">9,512,625</td>
<td align="right">-15.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">50,984,957</td>
<td align="right">42,960,388</td>
<td align="right">-15.7%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">5,471,887</td>
<td align="right">4,634,656</td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">6,967,223</td>
<td align="right">6,014,080</td>
<td align="right">-13.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">38,870</td>
<td align="right">33,897</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">8,130,180</td>
<td align="right">7,210,398</td>
<td align="right">-11.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">24,665,292</td>
<td align="right">22,099,524</td>
<td align="right">-10.4%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">36,915</td>
<td align="right">33,585</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">749,098</td>
<td align="right">681,569</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">9,288,508</td>
<td align="right">8,452,591</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">573,206</td>
<td align="right">523,258</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">218,424</td>
<td align="right">200,006</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">118,558</td>
<td align="right">109,056</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">154,685</td>
<td align="right">142,465</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">114</td>
<td align="right">105</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">196,717</td>
<td align="right">182,047</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">267,471</td>
<td align="right">249,053</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">53,548</td>
<td align="right">50,218</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">14,918,311</td>
<td align="right">14,019,973</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">258,566</td>
<td align="right">243,280</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">247,771</td>
<td align="right">233,792</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">342,728</td>
<td align="right">324,310</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">323,655</td>
<td align="right">306,952</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,864,359</td>
<td align="right">1,776,269</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">20,958,054</td>
<td align="right">20,074,625</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">10,913</td>
<td align="right">11,373</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">131,227</td>
<td align="right">126,233</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">121,847</td>
<td align="right">117,236</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">176,124</td>
<td align="right">169,478</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">120,748</td>
<td align="right">116,633</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">97,079</td>
<td align="right">93,775</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">97,399</td>
<td align="right">94,095</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">42,588</td>
<td align="right">41,613</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">355</td>
<td align="right">363</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">77,829</td>
<td align="right">76,164</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">59,931</td>
<td align="right">58,706</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">3,008,898</td>
<td align="right">2,947,683</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">3,435,718</td>
<td align="right">3,367,155</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">67,566</td>
<td align="right">66,334</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">5,470,585</td>
<td align="right">5,379,042</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">7,476,997</td>
<td align="right">7,352,179</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">27,630</td>
<td align="right">28,090</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">82,780</td>
<td align="right">81,554</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">485</td>
<td align="right">478</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">1,181,962</td>
<td align="right">1,165,011</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,198,974</td>
<td align="right">1,182,023</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">6,333,351</td>
<td align="right">6,248,077</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">4,137,294</td>
<td align="right">4,082,545</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">36,013</td>
<td align="right">36,473</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">36,013</td>
<td align="right">36,473</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,551,504</td>
<td align="right">2,521,082</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">155,836</td>
<td align="right">157,596</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">2,098,798</td>
<td align="right">2,075,132</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">1,074,231</td>
<td align="right">1,063,390</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">1,033,101</td>
<td align="right">1,023,986</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">2,581,397</td>
<td align="right">2,559,088</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,933,545</td>
<td align="right">1,917,265</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">9,375,337</td>
<td align="right">9,298,295</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">19,664,913</td>
<td align="right">19,517,393</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">181,150</td>
<td align="right">182,490</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">2,467,361</td>
<td align="right">2,451,563</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">182</td>
<td align="right">181</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">29,623,174</td>
<td align="right">29,472,881</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">901,237</td>
<td align="right">896,703</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">652,112</td>
<td align="right">648,891</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">4,541</td>
<td align="right">4,524</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">9,704,391</td>
<td align="right">9,669,677</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,241,344</td>
<td align="right">1,237,838</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">4,152,508</td>
<td align="right">4,140,998</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">4,522,251</td>
<td align="right">4,509,842</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">298,370</td>
<td align="right">297,584</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">10,984,981</td>
<td align="right">10,958,092</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,046,835</td>
<td align="right">1,045,380</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,653,471</td>
<td align="right">2,649,796</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">1,788,128</td>
<td align="right">1,785,678</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,822,159</td>
<td align="right">1,820,494</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">1,832,737</td>
<td align="right">1,834,058</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,017,647</td>
<td align="right">1,018,119</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">3,201</td>
<td align="right">3,202</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">42,281</td>
<td align="right">42,273</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">3,614,846</td>
<td align="right">3,615,285</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">67,330</td>
<td align="right">67,337</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">125,736</td>
<td align="right">125,748</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">134,142</td>
<td align="right">134,150</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">152,413</td>
<td align="right">152,405</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">378,213</td>
<td align="right">378,228</td>
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
<td align="right">84,507</td>
<td align="right">84,507</td>
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
<td align="right">55,863</td>
<td align="right">55,863</td>
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
<td align="right">784</td>
<td align="right">784</td>
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
<td align="right">21,506,832</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right"></td>
<td align="right">849,200</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right"></td>
<td align="right">16,559</td>
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
<td align="right">3,378,178</td>
<td align="right">76.6%</td>
<td align="right">2,342,789</td>
<td align="right">69.5%</td>
<td align="right">-30.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">13,730</td>
<td align="right">0.3%</td>
<td align="right">11,586</td>
<td align="right">0.3%</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,016,491</td>
<td align="right">23.1%</td>
<td align="right">1,016,959</td>
<td align="right">30.2%</td>
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
<td align="right">525</td>
<td align="right">37.1%</td>
<td align="right">483</td>
<td align="right">35.0%</td>
<td align="right">-8.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">889</td>
<td align="right">62.9%</td>
<td align="right">898</td>
<td align="right">65.0%</td>
<td align="right">1.0%</td>
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
<td align="right">78</td>
<td align="right">8.8%</td>
<td align="right">82</td>
<td align="right">9.1%</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">295</td>
<td align="right">33.2%</td>
<td align="right">300</td>
<td align="right">33.4%</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">252</td>
<td align="right">28.3%</td>
<td align="right">252</td>
<td align="right">28.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">189</td>
<td align="right">21.3%</td>
<td align="right">189</td>
<td align="right">21.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">66</td>
<td align="right">7.4%</td>
<td align="right">66</td>
<td align="right">7.3%</td>
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
<td align="right">14,339,356</td>
<td align="right">100.0%</td>
<td align="right">12,517,482</td>
<td align="right">100.0%</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,029</td>
<td align="right">0.0%</td>
<td align="right">2,001</td>
<td align="right">0.0%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">823</td>
<td align="right">0.0%</td>
<td align="right">823</td>
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
<td align="right">3,335</td>
<td align="right">100.0%</td>
<td align="right">3,346</td>
<td align="right">100.0%</td>
<td align="right">0.3%</td>
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
<td align="right">23.1%</td>
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
<td align="right">140</td>
<td align="right">100.0%</td>
<td align="right">139</td>
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
<td align="right">18,636</td>
<td align="right">0.4%</td>
<td align="right">16,975</td>
<td align="right">0.4%</td>
<td align="right">-8.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">120,853</td>
<td align="right">2.7%</td>
<td align="right">116,287</td>
<td align="right">2.6%</td>
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
<td align="right">4,270,911</td>
<td align="right">96.8%</td>
<td align="right">4,255,109</td>
<td align="right">96.9%</td>
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
<td align="right">727</td>
<td align="right">54.3%</td>
<td align="right">678</td>
<td align="right">53.7%</td>
<td align="right">-6.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">613</td>
<td align="right">45.7%</td>
<td align="right">585</td>
<td align="right">46.3%</td>
<td align="right">-4.6%</td>
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
<td align="right">347</td>
<td align="right">47.7%</td>
<td align="right">293</td>
<td align="right">43.2%</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">238</td>
<td align="right">32.7%</td>
<td align="right">243</td>
<td align="right">35.8%</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">97</td>
<td align="right">13.3%</td>
<td align="right">97</td>
<td align="right">14.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">45</td>
<td align="right">6.2%</td>
<td align="right">45</td>
<td align="right">6.6%</td>
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
<td align="right">950,270</td>
<td align="right">100.0%</td>
<td align="right">125,808</td>
<td align="right">99.8%</td>
<td align="right">-86.8%</td>
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
<td align="right">19,108,129</td>
<td align="right">91.1%</td>
<td align="right">19,068,421</td>
<td align="right">91.5%</td>
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
<td align="right">666</td>
<td align="right">92.4%</td>
<td align="right">645</td>
<td align="right">92.1%</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">55</td>
<td align="right">7.6%</td>
<td align="right">55</td>
<td align="right">7.9%</td>
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
<td align="right">78</td>
<td align="right">11.7%</td>
<td align="right">57</td>
<td align="right">8.8%</td>
<td align="right">-26.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">252</td>
<td align="right">37.8%</td>
<td align="right">252</td>
<td align="right">39.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">252</td>
<td align="right">37.8%</td>
<td align="right">252</td>
<td align="right">39.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">71</td>
<td align="right">10.7%</td>
<td align="right">71</td>
<td align="right">11.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">7</td>
<td align="right">1.1%</td>
<td align="right">7</td>
<td align="right">1.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">3</td>
<td align="right">0.5%</td>
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
<td align="left">reversed list</td>
<td align="right">1</td>
<td align="right">0.2%</td>
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
<td align="right">43,790</td>
<td align="right">43,790 / 0 !!</td>
<td align="right">42,125</td>
<td align="right">42,125 / 0 !!</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">1,070,681</td>
<td align="right">1,070,681 / 0 !!</td>
<td align="right">1,055,395</td>
<td align="right">1,055,395 / 0 !!</td>
<td align="right">-1.4%</td>
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
<td align="right">31,935,364</td>
<td align="right">88.3%</td>
<td align="right">25,280,281</td>
<td align="right">85.9%</td>
<td align="right">-20.8%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">3,425,309</td>
<td align="right">9.5%</td>
<td align="right">3,356,797</td>
<td align="right">11.4%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">797,902</td>
<td align="right">2.2%</td>
<td align="right">798,608</td>
<td align="right">2.7%</td>
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
<td align="right">5,887</td>
<td align="right">23.0%</td>
<td align="right">5,833</td>
<td align="right">22.8%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">19,761</td>
<td align="right">77.0%</td>
<td align="right">19,783</td>
<td align="right">77.2%</td>
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
<td align="left">overriding descriptor</td>
<td align="right">903</td>
<td align="right">15.3%</td>
<td align="right">866</td>
<td align="right">14.8%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">744</td>
<td align="right">12.6%</td>
<td align="right">720</td>
<td align="right">12.3%</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">668</td>
<td align="right">11.3%</td>
<td align="right">667</td>
<td align="right">11.4%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">1,794</td>
<td align="right">30.5%</td>
<td align="right">1,792</td>
<td align="right">30.7%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">11,614,063</td>
<td align="right">100.0%</td>
<td align="right">11,434,496</td>
<td align="right">100.0%</td>
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
<td align="right">828</td>
<td align="right">0.0%</td>
<td align="right">817</td>
<td align="right">0.0%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">5</td>
<td align="right">0.0%</td>
<td align="right">5</td>
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
<td align="right">228</td>
<td align="right">0.0%</td>
<td align="right">228</td>
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
<td align="right">2,379</td>
<td align="right">100.0%</td>
<td align="right">2,391</td>
<td align="right">100.0%</td>
<td align="right">0.5%</td>
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
<td align="right">258,864</td>
<td align="right">100.0%</td>
<td align="right">240,446</td>
<td align="right">100.0%</td>
<td align="right">-7.1%</td>
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
<td align="right">2,875,901</td>
<td align="right">85.9%</td>
<td align="right">2,040,259</td>
<td align="right">81.2%</td>
<td align="right">-29.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">150,665</td>
<td align="right">4.5%</td>
<td align="right">150,662</td>
<td align="right">6.0%</td>
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
<td align="right">319,503</td>
<td align="right">9.5%</td>
<td align="right">319,503</td>
<td align="right">12.7%</td>
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
<td align="right">7,207</td>
<td align="right">90.5%</td>
<td align="right">7,202</td>
<td align="right">90.5%</td>
<td align="right">-0.1%</td>
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
<td align="right">543</td>
<td align="right">72.0%</td>
<td align="right">556</td>
<td align="right">73.7%</td>
<td align="right">2.4%</td>
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
<td align="right">1,074,231</td>
<td align="right">96.2%</td>
<td align="right">1,063,390</td>
<td align="right">96.2%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">42,067</td>
<td align="right">3.8%</td>
<td align="right">42,064</td>
<td align="right">3.8%</td>
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
<td align="right">24</td>
<td align="right">11.2%</td>
<td align="right">19</td>
<td align="right">9.1%</td>
<td align="right">-20.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">190</td>
<td align="right">88.8%</td>
<td align="right">190</td>
<td align="right">90.9%</td>
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
<td align="right">3,664,161</td>
<td align="right">77.8%</td>
<td align="right">3,574,304</td>
<td align="right">77.4%</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,045,433</td>
<td align="right">22.2%</td>
<td align="right">1,043,980</td>
<td align="right">22.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">31</td>
<td align="right">0.0%</td>
<td align="right">31</td>
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
<td align="right">467</td>
<td align="right">33.3%</td>
<td align="right">469</td>
<td align="right">33.5%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">936</td>
<td align="right">66.7%</td>
<td align="right">932</td>
<td align="right">66.5%</td>
<td align="right">-0.4%</td>
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
<td align="right">140</td>
<td align="right">15.0%</td>
<td align="right">150</td>
<td align="right">16.1%</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">297</td>
<td align="right">31.7%</td>
<td align="right">283</td>
<td align="right">30.4%</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">321</td>
<td align="right">34.3%</td>
<td align="right">321</td>
<td align="right">34.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">112</td>
<td align="right">12.0%</td>
<td align="right">112</td>
<td align="right">12.0%</td>
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
<td align="right">2.4%</td>
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
<td align="right">3,489,296</td>
<td align="right">100.0%</td>
<td align="right">2,676,039</td>
<td align="right">100.0%</td>
<td align="right">-23.3%</td>
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
<td align="right">261,433,357</td>
<td align="right">60.6%</td>
<td align="right">233,382,912</td>
<td align="right">60.2%</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">159,592,375</td>
<td align="right">37.0%</td>
<td align="right">144,376,442</td>
<td align="right">37.2%</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">8,915,149</td>
<td align="right">2.1%</td>
<td align="right">8,735,918</td>
<td align="right">2.3%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,150,854</td>
<td align="right">0.3%</td>
<td align="right">1,147,754</td>
<td align="right">0.3%</td>
<td align="right">-0.3%</td>
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
<td align="right">1,863,638</td>
<td align="right">24.2%</td>
<td align="right">1,775,569</td>
<td align="right">23.6%</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">120,853</td>
<td align="right">1.6%</td>
<td align="right">116,287</td>
<td align="right">1.5%</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">3,425,309</td>
<td align="right">44.5%</td>
<td align="right">3,356,797</td>
<td align="right">44.6%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">2,029</td>
<td align="right">0.0%</td>
<td align="right">2,001</td>
<td align="right">0.0%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">828</td>
<td align="right">0.0%</td>
<td align="right">817</td>
<td align="right">0.0%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,045,433</td>
<td align="right">13.6%</td>
<td align="right">1,043,980</td>
<td align="right">13.9%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,016,491</td>
<td align="right">13.2%</td>
<td align="right">1,016,959</td>
<td align="right">13.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">42,067</td>
<td align="right">0.5%</td>
<td align="right">42,064</td>
<td align="right">0.6%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">150,665</td>
<td align="right">2.0%</td>
<td align="right">150,662</td>
<td align="right">2.0%</td>
<td align="right">-0.0%</td>
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
<td align="right">6,907</td>
<td align="right">0.6%</td>
<td align="right">5,701</td>
<td align="right">0.5%</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">6,823</td>
<td align="right">0.6%</td>
<td align="right">5,885</td>
<td align="right">0.5%</td>
<td align="right">-13.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">18,635</td>
<td align="right">1.6%</td>
<td align="right">16,974</td>
<td align="right">1.5%</td>
<td align="right">-8.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">676,776</td>
<td align="right">58.8%</td>
<td align="right">677,490</td>
<td align="right">59.0%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">100,830</td>
<td align="right">8.8%</td>
<td align="right">100,822</td>
<td align="right">8.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">319,503</td>
<td align="right">27.8%</td>
<td align="right">319,503</td>
<td align="right">27.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">20,147</td>
<td align="right">1.8%</td>
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
<td align="right">142</td>
<td align="right">0.0%</td>
<td align="right">142</td>
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
<td align="left">Frame objects created</td>
<td align="right">36,027</td>
<td align="right">0.1%</td>
<td align="right">36,487</td>
<td align="right">0.1%</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">301,940</td>
<td align="right">1.0%</td>
<td align="right">298,623</td>
<td align="right">1.0%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">19,673,318</td>
<td align="right">66.4%</td>
<td align="right">19,527,162</td>
<td align="right">66.2%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">18,655,470</td>
<td align="right">62.9%</td>
<td align="right">18,536,211</td>
<td align="right">62.8%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">10,145,913</td>
<td align="right">34.2%</td>
<td align="right">10,119,016</td>
<td align="right">34.3%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">10,145,971</td>
<td align="right">34.2%</td>
<td align="right">10,119,074</td>
<td align="right">34.3%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">10,993,506</td>
<td align="right">37.1%</td>
<td align="right">10,966,609</td>
<td align="right">37.2%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">10,993,506</td>
<td align="right">37.1%</td>
<td align="right">10,966,609</td>
<td align="right">37.2%</td>
<td align="right">-0.2%</td>
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
<td align="right">46,870</td>
<td align="right"></td>
<td align="right">22,926</td>
<td align="right"></td>
<td align="right">-51.1%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">96,299</td>
<td align="right"></td>
<td align="right">68,603</td>
<td align="right"></td>
<td align="right">-28.8%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">49,900</td>
<td align="right"></td>
<td align="right">45,949</td>
<td align="right"></td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">439,454</td>
<td align="right"></td>
<td align="right">427,058</td>
<td align="right"></td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">3,953,900</td>
<td align="right"></td>
<td align="right">3,874,870</td>
<td align="right"></td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">35,584,955</td>
<td align="right">15.7%</td>
<td align="right">35,244,153</td>
<td align="right">15.7%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">34,989,258</td>
<td align="right">17.6%</td>
<td align="right">34,673,753</td>
<td align="right">17.5%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">45,156,793</td>
<td align="right">22.7%</td>
<td align="right">44,803,373</td>
<td align="right">22.6%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">18,868,059</td>
<td align="right"></td>
<td align="right">18,747,205</td>
<td align="right"></td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">18,866,888</td>
<td align="right">56.6%</td>
<td align="right">18,746,090</td>
<td align="right">56.5%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">5,604,091</td>
<td align="right">2.8%</td>
<td align="right">5,568,357</td>
<td align="right">2.8%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">60,866,543</td>
<td align="right">26.9%</td>
<td align="right">60,484,432</td>
<td align="right">26.9%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">128,241,647</td>
<td align="right">56.8%</td>
<td align="right">127,551,981</td>
<td align="right">56.8%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">113,536,385</td>
<td align="right">57.0%</td>
<td align="right">112,963,327</td>
<td align="right">57.0%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">1,259,088</td>
<td align="right">0.6%</td>
<td align="right">1,252,896</td>
<td align="right">0.6%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">8,745,184</td>
<td align="right"></td>
<td align="right">8,710,473</td>
<td align="right"></td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">14,740,420</td>
<td align="right"></td>
<td align="right">14,688,325</td>
<td align="right"></td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">14,262,417</td>
<td align="right">42.8%</td>
<td align="right">14,219,534</td>
<td align="right">42.9%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">14,475,046</td>
<td align="right">43.4%</td>
<td align="right">14,432,200</td>
<td align="right">43.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">139,972</td>
<td align="right">0.4%</td>
<td align="right">140,000</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">72,657</td>
<td align="right">0.2%</td>
<td align="right">72,666</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">640</td>
<td align="right">0.1%</td>
<td align="right">640</td>
<td align="right">0.1%</td>
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
<td align="right">2</td>
<td align="right">560</td>
<td align="right">22,471</td>
<td align="right">1,502</td>
<td align="right">1,343</td>
<td align="right">2</td>
<td align="right">560</td>
<td align="right">22,471</td>
<td align="right">1,502</td>
<td align="right">1,343</td>
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
Stats gathered on: 2025-06-02
