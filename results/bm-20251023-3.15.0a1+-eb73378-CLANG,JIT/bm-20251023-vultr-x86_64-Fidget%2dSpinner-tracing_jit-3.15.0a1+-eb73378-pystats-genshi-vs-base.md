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
<td align="right">2,834,164</td>
<td align="right">10,355,601</td>
<td align="right">265.4%</td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">1,548,257</td>
<td align="right">4,116</td>
<td align="right">-99.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">64,641,903</td>
<td align="right">299,326</td>
<td align="right">-99.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">828,929</td>
<td align="right">5,028</td>
<td align="right">-99.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">12,180,154</td>
<td align="right">74,418</td>
<td align="right">-99.4%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">84,452,112</td>
<td align="right">526,237</td>
<td align="right">-99.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">17,345,790</td>
<td align="right">140,307</td>
<td align="right">-99.2%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">66,987,660</td>
<td align="right">552,116</td>
<td align="right">-99.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,563,450</td>
<td align="right">18,869</td>
<td align="right">-98.8%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,565,454</td>
<td align="right">20,845</td>
<td align="right">-98.7%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">10,871,720</td>
<td align="right">156,070</td>
<td align="right">-98.6%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">5,823,732</td>
<td align="right">128,776</td>
<td align="right">-97.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">4,270,190</td>
<td align="right">118,324</td>
<td align="right">-97.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">4,269,889</td>
<td align="right">118,592</td>
<td align="right">-97.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">4,270,280</td>
<td align="right">118,977</td>
<td align="right">-97.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">12,843,737</td>
<td align="right">383,930</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">41,642,465</td>
<td align="right">1,412,710</td>
<td align="right">-96.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">6,205,709</td>
<td align="right">244,865</td>
<td align="right">-96.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">4,407,936</td>
<td align="right">187,939</td>
<td align="right">-95.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">28,430,595</td>
<td align="right">1,230,260</td>
<td align="right">-95.7%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">10,865,433</td>
<td align="right">475,915</td>
<td align="right">-95.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">3,102,842</td>
<td align="right">137,512</td>
<td align="right">-95.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">10,984,136</td>
<td align="right">514,217</td>
<td align="right">-95.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">9,323,467</td>
<td align="right">461,805</td>
<td align="right">-95.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">9,318,631</td>
<td align="right">466,305</td>
<td align="right">-95.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">22,770,500</td>
<td align="right">1,167,316</td>
<td align="right">-94.9%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">99,444,988</td>
<td align="right">5,772,952</td>
<td align="right">-94.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">138,898,639</td>
<td align="right">8,255,606</td>
<td align="right">-94.1%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">44,886,135</td>
<td align="right">2,841,674</td>
<td align="right">-93.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">139,568,481</td>
<td align="right">8,996,079</td>
<td align="right">-93.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">23,395,784</td>
<td align="right">1,689,636</td>
<td align="right">-92.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">23,406,480</td>
<td align="right">1,699,794</td>
<td align="right">-92.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">13,599,179</td>
<td align="right">1,017,182</td>
<td align="right">-92.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">390,390,894</td>
<td align="right">34,817,956</td>
<td align="right">-91.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">141,680,958</td>
<td align="right">14,888,792</td>
<td align="right">-89.5%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">27,540,986</td>
<td align="right">3,250,896</td>
<td align="right">-88.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">5,711,566</td>
<td align="right">697,818</td>
<td align="right">-87.8%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">81,314,272</td>
<td align="right">10,630,306</td>
<td align="right">-86.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">56,311,710</td>
<td align="right">7,981,867</td>
<td align="right">-85.8%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">35,572,043</td>
<td align="right">5,149,534</td>
<td align="right">-85.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">105,790,585</td>
<td align="right">15,743,749</td>
<td align="right">-85.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">9,558,519</td>
<td align="right">1,431,883</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">119,247,150</td>
<td align="right">18,586,485</td>
<td align="right">-84.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">17,874,698</td>
<td align="right">2,809,972</td>
<td align="right">-84.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">53,564,659</td>
<td align="right">8,639,724</td>
<td align="right">-83.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">13,237,228</td>
<td align="right">2,486,743</td>
<td align="right">-81.2%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">6,872,949</td>
<td align="right">1,313,128</td>
<td align="right">-80.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">21,357,463</td>
<td align="right">4,217,083</td>
<td align="right">-80.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">39,218,947</td>
<td align="right">8,845,219</td>
<td align="right">-77.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">778,633</td>
<td align="right">184,820</td>
<td align="right">-76.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">9,060,380</td>
<td align="right">2,209,768</td>
<td align="right">-75.6%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">2,843,238</td>
<td align="right">716,352</td>
<td align="right">-74.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">11,802,359</td>
<td align="right">3,221,117</td>
<td align="right">-72.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">9,317,185</td>
<td align="right">2,629,888</td>
<td align="right">-71.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">390,816</td>
<td align="right">112,053</td>
<td align="right">-71.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">388,656</td>
<td align="right">120,259</td>
<td align="right">-69.1%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">390,851</td>
<td align="right">121,223</td>
<td align="right">-69.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">406,137</td>
<td align="right">126,828</td>
<td align="right">-68.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">391,315</td>
<td align="right">122,880</td>
<td align="right">-68.6%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">10,245,696</td>
<td align="right">3,486,588</td>
<td align="right">-66.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,699,737</td>
<td align="right">1,947,291</td>
<td align="right">-65.8%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">1,175,484</td>
<td align="right">423,252</td>
<td align="right">-64.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">10,879,113</td>
<td align="right">4,130,086</td>
<td align="right">-62.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">5,051,151</td>
<td align="right">2,348,638</td>
<td align="right">-53.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,554,535</td>
<td align="right">770,246</td>
<td align="right">-50.5%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">9,701,632</td>
<td align="right">4,825,852</td>
<td align="right">-50.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">4,269,333</td>
<td align="right">2,123,935</td>
<td align="right">-50.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">1,425,136</td>
<td align="right">709,818</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">391,635</td>
<td align="right">195,193</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">390,854</td>
<td align="right">194,865</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">4,672,429</td>
<td align="right">2,331,550</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">4,283,409</td>
<td align="right">2,137,797</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">392,552</td>
<td align="right">196,222</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">21,845,781</td>
<td align="right">10,920,575</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">146,226</td>
<td align="right">76,333</td>
<td align="right">-47.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">420</td>
<td align="right">225</td>
<td align="right">-46.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">510,082</td>
<td align="right">312,639</td>
<td align="right">-38.7%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,996</td>
<td align="right">5,290</td>
<td align="right">-33.8%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">180</td>
<td align="right">240</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">2,821</td>
<td align="right">1,896</td>
<td align="right">-32.8%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">3,438</td>
<td align="right">2,315</td>
<td align="right">-32.7%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">1,829</td>
<td align="right">1,234</td>
<td align="right">-32.5%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">1,855</td>
<td align="right">1,260</td>
<td align="right">-32.1%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">3,986</td>
<td align="right">2,728</td>
<td align="right">-31.6%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">1,447</td>
<td align="right">1,047</td>
<td align="right">-27.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,111</td>
<td align="right">842</td>
<td align="right">-24.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">2,065</td>
<td align="right">1,592</td>
<td align="right">-22.9%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">1,542</td>
<td align="right">1,267</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">1,542</td>
<td align="right">1,267</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">2,476</td>
<td align="right">2,060</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">3,148</td>
<td align="right">3,668</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">1,315</td>
<td align="right">1,106</td>
<td align="right">-15.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">3,153</td>
<td align="right">2,727</td>
<td align="right">-13.5%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">15,597</td>
<td align="right">13,722</td>
<td align="right">-12.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">4,302</td>
<td align="right">3,790</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">4,966</td>
<td align="right">4,512</td>
<td align="right">-9.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">614</td>
<td align="right">668</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">3,752</td>
<td align="right">3,467</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">18,141</td>
<td align="right">16,798</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">2,495</td>
<td align="right">2,331</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">5,958</td>
<td align="right">6,273</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">12,562</td>
<td align="right">11,931</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">10,171</td>
<td align="right">9,701</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">17,297</td>
<td align="right">16,662</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">129</td>
<td align="right">127</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">260</td>
<td align="right">256</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">65</td>
<td align="right">64</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">782</td>
<td align="right">770</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">196</td>
<td align="right">193</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">654</td>
<td align="right">644</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">262</td>
<td align="right">258</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">3,410</td>
<td align="right">3,358</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">7,345</td>
<td align="right">7,233</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">460</td>
<td align="right">453</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">3,422</td>
<td align="right">3,370</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">3,422</td>
<td align="right">3,370</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">3,422</td>
<td align="right">3,370</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">857</td>
<td align="right">844</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">264</td>
<td align="right">260</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">5,558</td>
<td align="right">5,474</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">993</td>
<td align="right">978</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">1,858</td>
<td align="right">1,830</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">665</td>
<td align="right">655</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">466</td>
<td align="right">459</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">1,876</td>
<td align="right">1,848</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,440</td>
<td align="right">3,391</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">847</td>
<td align="right">835</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">3,563</td>
<td align="right">3,513</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,283</td>
<td align="right">1,265</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">2,598</td>
<td align="right">2,564</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">157</td>
<td align="right">155</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">175</td>
<td align="right">173</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">290</td>
<td align="right">287</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">638</td>
<td align="right">632</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">388</td>
<td align="right">385</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">128,903</td>
<td align="right">128,610</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">130,143</td>
<td align="right">129,954</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">129,728</td>
<td align="right">129,546</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">1,546,023</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">258</td>
<td align="right">258</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">186</td>
<td align="right">186</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">98</td>
<td align="right">98</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">69</td>
<td align="right">69</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">54</td>
<td align="right">54</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">36</td>
<td align="right">36</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">31</td>
<td align="right">31</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">22</td>
<td align="right">22</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">21</td>
<td align="right">21</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">18</td>
<td align="right">18</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">18</td>
<td align="right">18</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">15</td>
<td align="right">15</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">8</td>
<td align="right">8</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">4</td>
<td align="right">4</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">2</td>
<td align="right">2</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">47,096,257</td>
<td align="right">100.0%</td>
<td align="right">23,432,883</td>
<td align="right">99.9%</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">15,934</td>
<td align="right">0.0%</td>
<td align="right">15,252</td>
<td align="right">0.1%</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">40</td>
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
<td align="right">348</td>
<td align="right">25.5%</td>
<td align="right">368</td>
<td align="right">26.1%</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,016</td>
<td align="right">74.5%</td>
<td align="right">1,043</td>
<td align="right">73.9%</td>
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
<td align="left">add other</td>
<td align="right">117</td>
<td align="right">11.5%</td>
<td align="right">133</td>
<td align="right">12.8%</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">347</td>
<td align="right">34.2%</td>
<td align="right">363</td>
<td align="right">34.8%</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">111</td>
<td align="right">10.9%</td>
<td align="right">108</td>
<td align="right">10.4%</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">312</td>
<td align="right">30.7%</td>
<td align="right">310</td>
<td align="right">29.7%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">129</td>
<td align="right">12.7%</td>
<td align="right">129</td>
<td align="right">12.4%</td>
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
<td align="right">1,858</td>
<td align="right">100.0%</td>
<td align="right">1,830</td>
<td align="right">100.0%</td>
<td align="right">-1.5%</td>
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
<td align="right">86,877,698</td>
<td align="right">100.0%</td>
<td align="right">43,313,589</td>
<td align="right">100.0%</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,033</td>
<td align="right">0.0%</td>
<td align="right">3,970</td>
<td align="right">0.0%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">5,743</td>
<td align="right">0.0%</td>
<td align="right">5,663</td>
<td align="right">0.0%</td>
<td align="right">-1.4%</td>
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
<td align="right">4,248</td>
<td align="right">100.0%</td>
<td align="right">4,580</td>
<td align="right">100.0%</td>
<td align="right">7.8%</td>
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
<td align="left">init not python</td>
<td align="right">1</td>
<td align="right">1 / 0 !!</td>
<td align="right">21</td>
<td align="right">21 / 0 !!</td>
<td align="right">2,000.0%</td>
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
<td align="right">28</td>
<td align="right">15.6%</td>
<td align="right">28</td>
<td align="right">11.7%</td>
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
<td align="right">152</td>
<td align="right">100.0%</td>
<td align="right">212</td>
<td align="right">100.0%</td>
<td align="right">39.5%</td>
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
<td align="right">1,424,383</td>
<td align="right">47.6%</td>
<td align="right">709,239</td>
<td align="right">47.4%</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,566,040</td>
<td align="right">52.4%</td>
<td align="right">785,457</td>
<td align="right">52.5%</td>
<td align="right">-49.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">10</td>
<td align="right">0.0%</td>
<td align="right">10</td>
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
<td align="right">577</td>
<td align="right">76.6%</td>
<td align="right">403</td>
<td align="right">69.6%</td>
<td align="right">-30.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">176</td>
<td align="right">23.4%</td>
<td align="right">176</td>
<td align="right">30.4%</td>
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
<td align="right">440</td>
<td align="right">76.3%</td>
<td align="right">266</td>
<td align="right">66.0%</td>
<td align="right">-39.5%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">93</td>
<td align="right">16.1%</td>
<td align="right">93</td>
<td align="right">23.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">43</td>
<td align="right">7.5%</td>
<td align="right">43</td>
<td align="right">10.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">1</td>
<td align="right">0.2%</td>
<td align="right">1</td>
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
<td align="right">7,889,602</td>
<td align="right">100.0%</td>
<td align="right">3,923,985</td>
<td align="right">99.9%</td>
<td align="right">-50.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">3,216</td>
<td align="right">0.0%</td>
<td align="right">3,169</td>
<td align="right">0.1%</td>
<td align="right">-1.5%</td>
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
<td align="right">339</td>
<td align="right">97.7%</td>
<td align="right">336</td>
<td align="right">97.7%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">8</td>
<td align="right">2.3%</td>
<td align="right">8</td>
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
<td align="left">list</td>
<td align="right">90</td>
<td align="right">26.5%</td>
<td align="right">89</td>
<td align="right">26.5%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">206</td>
<td align="right">60.8%</td>
<td align="right">204</td>
<td align="right">60.7%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">43</td>
<td align="right">12.7%</td>
<td align="right">43</td>
<td align="right">12.8%</td>
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
<td align="right">11,798,674</td>
<td align="right">12.6%</td>
<td align="right">3,219,404</td>
<td align="right">9.0%</td>
<td align="right">-72.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">82,119,076</td>
<td align="right">87.4%</td>
<td align="right">32,410,088</td>
<td align="right">91.0%</td>
<td align="right">-60.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">3,078</td>
<td align="right">0.0%</td>
<td align="right">2,178</td>
<td align="right">0.0%</td>
<td align="right">-29.2%</td>
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
<td align="right">3,598</td>
<td align="right">97.0%</td>
<td align="right">1,626</td>
<td align="right">94.9%</td>
<td align="right">-54.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">110</td>
<td align="right">3.0%</td>
<td align="right">88</td>
<td align="right">5.1%</td>
<td align="right">-20.0%</td>
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
<td align="right">168</td>
<td align="right">4.7%</td>
<td align="right">481</td>
<td align="right">29.6%</td>
<td align="right">186.3%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">174</td>
<td align="right">4.8%</td>
<td align="right">4</td>
<td align="right">0.2%</td>
<td align="right">-97.7%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">1,034</td>
<td align="right">28.7%</td>
<td align="right">45</td>
<td align="right">2.8%</td>
<td align="right">-95.6%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">492</td>
<td align="right">13.7%</td>
<td align="right">106</td>
<td align="right">6.5%</td>
<td align="right">-78.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">1,354</td>
<td align="right">37.6%</td>
<td align="right">641</td>
<td align="right">39.4%</td>
<td align="right">-52.7%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">43</td>
<td align="right">1.2%</td>
<td align="right">22</td>
<td align="right">1.4%</td>
<td align="right">-48.8%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">56</td>
<td align="right">1.6%</td>
<td align="right">53</td>
<td align="right">3.3%</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">66</td>
<td align="right">1.8%</td>
<td align="right">65</td>
<td align="right">4.0%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">91</td>
<td align="right">2.5%</td>
<td align="right">90</td>
<td align="right">5.5%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">118</td>
<td align="right">3.3%</td>
<td align="right">117</td>
<td align="right">7.2%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">2</td>
<td align="right">0.1%</td>
<td align="right">2</td>
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
<td align="left">other</td>
<td align="right">6,078,235</td>
<td align="right">6,078,235 / 0 !!</td>
<td align="right">3,022,304</td>
<td align="right">3,022,304 / 0 !!</td>
<td align="right">-50.3%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">778,789</td>
<td align="right">778,789 / 0 !!</td>
<td align="right">387,801</td>
<td align="right">387,801 / 0 !!</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">4,274,228</td>
<td align="right">4,274,228 / 0 !!</td>
<td align="right">2,128,882</td>
<td align="right">2,128,882 / 0 !!</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">393,156</td>
<td align="right">393,156 / 0 !!</td>
<td align="right">197,447</td>
<td align="right">197,447 / 0 !!</td>
<td align="right">-49.8%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">328</td>
<td align="right">328 / 0 !!</td>
<td align="right">323</td>
<td align="right">323 / 0 !!</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">3,019</td>
<td align="right">3,019 / 0 !!</td>
<td align="right">2,973</td>
<td align="right">2,973 / 0 !!</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">1,853</td>
<td align="right">1,853 / 0 !!</td>
<td align="right">1,825</td>
<td align="right">1,825 / 0 !!</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">string</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">12,836,058</td>
<td align="right">22.1%</td>
<td align="right">378,753</td>
<td align="right">1.7%</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">45,125,754</td>
<td align="right">77.8%</td>
<td align="right">21,285,834</td>
<td align="right">98.2%</td>
<td align="right">-52.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,211</td>
<td align="right">0.0%</td>
<td align="right">4,148</td>
<td align="right">0.0%</td>
<td align="right">-1.5%</td>
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
<td align="right">4,773</td>
<td align="right">63.8%</td>
<td align="right">1,636</td>
<td align="right">32.9%</td>
<td align="right">-65.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,705</td>
<td align="right">36.2%</td>
<td align="right">3,344</td>
<td align="right">67.1%</td>
<td align="right">23.6%</td>
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
<td align="left">class method obj</td>
<td align="right">3,339</td>
<td align="right">70.0%</td>
<td align="right">364</td>
<td align="right">22.2%</td>
<td align="right">-89.1%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">919</td>
<td align="right">19.3%</td>
<td align="right">766</td>
<td align="right">46.8%</td>
<td align="right">-16.6%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">50</td>
<td align="right">1.0%</td>
<td align="right">48</td>
<td align="right">2.9%</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">102</td>
<td align="right">2.1%</td>
<td align="right">100</td>
<td align="right">6.1%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">141</td>
<td align="right">3.0%</td>
<td align="right">139</td>
<td align="right">8.5%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">132</td>
<td align="right">2.8%</td>
<td align="right">131</td>
<td align="right">8.0%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">1</td>
<td align="right">0.1%</td>
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
<td align="right">167,997,187</td>
<td align="right">100.0%</td>
<td align="right">66,600,965</td>
<td align="right">100.0%</td>
<td align="right">-60.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,889</td>
<td align="right">0.0%</td>
<td align="right">1,860</td>
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
<td align="right">500</td>
<td align="right">0.0%</td>
<td align="right">500</td>
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
<td align="right">2,648</td>
<td align="right">100.0%</td>
<td align="right">3,168</td>
<td align="right">100.0%</td>
<td align="right">19.6%</td>
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
<td align="right">264</td>
<td align="right">98.5%</td>
<td align="right">260</td>
<td align="right">98.5%</td>
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
<td align="right">2</td>
<td align="right">0.7%</td>
<td align="right">2</td>
<td align="right">0.8%</td>
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
<td align="right">2</td>
<td align="right">100.0%</td>
<td align="right">2</td>
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
<td align="right">1,958</td>
<td align="right">7.3%</td>
<td align="right">1,552</td>
<td align="right">6.3%</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">23,107</td>
<td align="right">86.0%</td>
<td align="right">21,310</td>
<td align="right">86.0%</td>
<td align="right">-7.8%</td>
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
<td align="right">1,312</td>
<td align="right">73.1%</td>
<td align="right">1,492</td>
<td align="right">77.9%</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">482</td>
<td align="right">26.9%</td>
<td align="right">423</td>
<td align="right">22.1%</td>
<td align="right">-12.2%</td>
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
<td align="right">130</td>
<td align="right">27.0%</td>
<td align="right">86</td>
<td align="right">20.3%</td>
<td align="right">-33.8%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">330</td>
<td align="right">68.5%</td>
<td align="right">315</td>
<td align="right">74.5%</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">22</td>
<td align="right">4.6%</td>
<td align="right">22</td>
<td align="right">5.2%</td>
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
<td align="right">262</td>
<td align="right">100.0%</td>
<td align="right">258</td>
<td align="right">100.0%</td>
<td align="right">-1.5%</td>
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
<td align="right">4,271,765</td>
<td align="right">100.0%</td>
<td align="right">2,125,952</td>
<td align="right">100.0%</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">36</td>
<td align="right">0.0%</td>
<td align="right">36</td>
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
<td align="right">32</td>
<td align="right">97.0%</td>
<td align="right">32</td>
<td align="right">97.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1</td>
<td align="right">3.0%</td>
<td align="right">1</td>
<td align="right">3.0%</td>
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
<td align="right">1</td>
<td align="right">100.0%</td>
<td align="right">1</td>
<td align="right">100.0%</td>
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
<td align="right">683,971</td>
<td align="right">1.3%</td>
<td align="right">2,076</td>
<td align="right">0.0%</td>
<td align="right">-99.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">13,530,654</td>
<td align="right">25.1%</td>
<td align="right">1,015,728</td>
<td align="right">5.2%</td>
<td align="right">-92.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">39,578,859</td>
<td align="right">73.5%</td>
<td align="right">18,402,276</td>
<td align="right">94.8%</td>
<td align="right">-53.5%</td>
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
<td align="right">1</td>
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
<td align="right">67,793</td>
<td align="right">83.3%</td>
<td align="right">623</td>
<td align="right">41.8%</td>
<td align="right">-99.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">13,632</td>
<td align="right">16.7%</td>
<td align="right">866</td>
<td align="right">58.2%</td>
<td align="right">-93.6%</td>
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
<td align="left">mapping</td>
<td align="right">65,576</td>
<td align="right">96.7%</td>
<td align="right">410</td>
<td align="right">65.8%</td>
<td align="right">-99.4%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">2,110</td>
<td align="right">3.1%</td>
<td align="right">128</td>
<td align="right">20.5%</td>
<td align="right">-93.9%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">65</td>
<td align="right">0.1%</td>
<td align="right">43</td>
<td align="right">6.9%</td>
<td align="right">-33.8%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">42</td>
<td align="right">0.1%</td>
<td align="right">42</td>
<td align="right">6.7%</td>
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
<td align="right">27,660,349</td>
<td align="right">100.0%</td>
<td align="right">13,747,883</td>
<td align="right">100.0%</td>
<td align="right">-50.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">444</td>
<td align="right">0.0%</td>
<td align="right">438</td>
<td align="right">0.0%</td>
<td align="right">-1.4%</td>
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
<td align="right">124</td>
<td align="right">72.9%</td>
<td align="right">184</td>
<td align="right">80.0%</td>
<td align="right">48.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">46</td>
<td align="right">27.1%</td>
<td align="right">46</td>
<td align="right">20.0%</td>
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
<td align="left">iterator</td>
<td align="right">46</td>
<td align="right">100.0%</td>
<td align="right">46</td>
<td align="right">100.0%</td>
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
<td align="right">697,232</td>
<td align="right">0.0%</td>
<td align="right">14,282</td>
<td align="right">0.0%</td>
<td align="right">-98.0%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">713,177,705</td>
<td align="right">32.8%</td>
<td align="right">60,498,783</td>
<td align="right">25.4%</td>
<td align="right">-91.5%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">1,408,491,615</td>
<td align="right">64.8%</td>
<td align="right">168,970,753</td>
<td align="right">70.9%</td>
<td align="right">-88.0%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">49,952,812</td>
<td align="right">2.3%</td>
<td align="right">8,855,287</td>
<td align="right">3.7%</td>
<td align="right">-82.3%</td>
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
<td align="left">LOAD_ATTR</td>
<td align="right">12,836,058</td>
<td align="right">32.4%</td>
<td align="right">378,753</td>
<td align="right">7.1%</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">13,530,654</td>
<td align="right">34.2%</td>
<td align="right">1,015,728</td>
<td align="right">19.0%</td>
<td align="right">-92.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">11,798,674</td>
<td align="right">29.8%</td>
<td align="right">3,219,404</td>
<td align="right">60.2%</td>
<td align="right">-72.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">1,424,383</td>
<td align="right">3.6%</td>
<td align="right">709,239</td>
<td align="right">13.3%</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">1,958</td>
<td align="right">0.0%</td>
<td align="right">1,552</td>
<td align="right">0.0%</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">15,934</td>
<td align="right">0.0%</td>
<td align="right">15,252</td>
<td align="right">0.3%</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">1,858</td>
<td align="right">0.0%</td>
<td align="right">1,830</td>
<td align="right">0.0%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">3,216</td>
<td align="right">0.0%</td>
<td align="right">3,169</td>
<td align="right">0.1%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">5,743</td>
<td align="right">0.0%</td>
<td align="right">5,663</td>
<td align="right">0.1%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">500</td>
<td align="right">0.0%</td>
<td align="right">500</td>
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
<td align="left">TO_BOOL_STR</td>
<td align="right">683,700</td>
<td align="right">98.1%</td>
<td align="right">1,814</td>
<td align="right">12.7%</td>
<td align="right">-99.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">1,742</td>
<td align="right">0.2%</td>
<td align="right">895</td>
<td align="right">6.3%</td>
<td align="right">-48.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">191</td>
<td align="right">0.0%</td>
<td align="right">183</td>
<td align="right">1.3%</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">1,336</td>
<td align="right">0.2%</td>
<td align="right">1,283</td>
<td align="right">9.0%</td>
<td align="right">-4.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">2,425</td>
<td align="right">0.3%</td>
<td align="right">2,379</td>
<td align="right">16.7%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">910</td>
<td align="right">0.1%</td>
<td align="right">896</td>
<td align="right">6.3%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">130</td>
<td align="right">0.0%</td>
<td align="right">128</td>
<td align="right">0.9%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">979</td>
<td align="right">0.1%</td>
<td align="right">964</td>
<td align="right">6.7%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">3,945</td>
<td align="right">0.6%</td>
<td align="right">3,886</td>
<td align="right">27.2%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">1,594</td>
<td align="right">0.2%</td>
<td align="right">1,577</td>
<td align="right">11.0%</td>
<td align="right">-1.1%</td>
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
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">17,066,534</td>
<td align="right">14.1%</td>
<td align="right">8,485,237</td>
<td align="right">14.1%</td>
<td align="right">-50.3%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">99,078,317</td>
<td align="right">81.9%</td>
<td align="right">49,280,205</td>
<td align="right">81.9%</td>
<td align="right">-50.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">4,268,390</td>
<td align="right">3.5%</td>
<td align="right">2,123,195</td>
<td align="right">3.5%</td>
<td align="right">-50.3%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">39,219,103</td>
<td align="right">32.4%</td>
<td align="right">19,579,986</td>
<td align="right">32.5%</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">21,845,939</td>
<td align="right">18.1%</td>
<td align="right">10,920,731</td>
<td align="right">18.1%</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">21,845,939</td>
<td align="right">18.1%</td>
<td align="right">10,920,731</td>
<td align="right">18.1%</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">4,779,405</td>
<td align="right">4.0%</td>
<td align="right">2,435,494</td>
<td align="right">4.0%</td>
<td align="right">-49.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">510,997</td>
<td align="right">0.4%</td>
<td align="right">312,281</td>
<td align="right">0.5%</td>
<td align="right">-38.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">521</td>
<td align="right">0.0%</td>
<td align="right">324</td>
<td align="right">0.0%</td>
<td align="right">-37.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">1,179</td>
<td align="right">0.0%</td>
<td align="right">972</td>
<td align="right">0.0%</td>
<td align="right">-17.6%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">7,275</td>
<td align="right">0.0%</td>
<td align="right">7,165</td>
<td align="right">0.0%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">431</td>
<td align="right">0.0%</td>
<td align="right">427</td>
<td align="right">0.0%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">18</td>
<td align="right">0.0%</td>
<td align="right">18</td>
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
<td align="right">469,306,828</td>
<td align="right">55.6%</td>
<td align="right">59,138,397</td>
<td align="right">13.9%</td>
<td align="right">-87.4%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">556,092,564</td>
<td align="right">61.1%</td>
<td align="right">102,902,808</td>
<td align="right">22.6%</td>
<td align="right">-81.5%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">12,952,702</td>
<td align="right">1.5%</td>
<td align="right">2,692,495</td>
<td align="right">0.6%</td>
<td align="right">-79.2%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">26,104,447</td>
<td align="right"></td>
<td align="right">13,028,753</td>
<td align="right"></td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">68,518,533</td>
<td align="right"></td>
<td align="right">34,240,580</td>
<td align="right"></td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">68,520,689</td>
<td align="right">66.7%</td>
<td align="right">34,242,475</td>
<td align="right">66.5%</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">2,215,997</td>
<td align="right">0.2%</td>
<td align="right">1,107,783</td>
<td align="right">0.2%</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">40,341,135</td>
<td align="right"></td>
<td align="right">20,176,115</td>
<td align="right"></td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">8,854,578</td>
<td align="right"></td>
<td align="right">4,431,172</td>
<td align="right"></td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">34,237,405</td>
<td align="right">33.3%</td>
<td align="right">17,253,234</td>
<td align="right">33.5%</td>
<td align="right">-49.6%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">34,242,859</td>
<td align="right">33.3%</td>
<td align="right">17,258,189</td>
<td align="right">33.5%</td>
<td align="right">-49.6%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">80,295,861</td>
<td align="right">8.8%</td>
<td align="right">40,484,436</td>
<td align="right">8.9%</td>
<td align="right">-49.6%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">86,278,636</td>
<td align="right">10.2%</td>
<td align="right">48,355,861</td>
<td align="right">11.4%</td>
<td align="right">-44.0%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">877</td>
<td align="right"></td>
<td align="right">665</td>
<td align="right"></td>
<td align="right">-24.2%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">2,665</td>
<td align="right"></td>
<td align="right">2,058</td>
<td align="right"></td>
<td align="right">-22.8%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">271,385,346</td>
<td align="right">29.8%</td>
<td align="right">311,408,978</td>
<td align="right">68.3%</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">275,679,654</td>
<td align="right">32.7%</td>
<td align="right">313,984,208</td>
<td align="right">74.0%</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">2,706</td>
<td align="right">0.0%</td>
<td align="right">2,388</td>
<td align="right">0.0%</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">2,748</td>
<td align="right">0.0%</td>
<td align="right">2,567</td>
<td align="right">0.0%</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">8,066</td>
<td align="right"></td>
<td align="right">7,559</td>
<td align="right"></td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">7,760</td>
<td align="right"></td>
<td align="right">7,469</td>
<td align="right"></td>
<td align="right">-3.8%</td>
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
<td align="right">798</td>
<td align="right">26,130</td>
<td align="right">9,409,369</td>
<td align="right">541,369</td>
<td align="right">1,515,522</td>
<td align="right">408</td>
<td align="right">25,116</td>
<td align="right">4,548,078</td>
<td align="right">94,320</td>
<td align="right">737,113</td>
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
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">4</td>
<td align="right">0.0%</td>
<td align="right">154</td>
<td align="right">7.8%</td>
<td align="right">3,750.0%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">152,653,454</td>
<td align="right">2,195.7%</td>
<td align="right">2,146,981,674</td>
<td align="right">3,779.9%</td>
<td align="right">1,306.4%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">6,952,379</td>
<td align="right"></td>
<td align="right">56,800,365</td>
<td align="right"></td>
<td align="right">717.0%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">5,468</td>
<td align="right">25.7%</td>
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
<td align="right">2</td>
<td align="right">0.0%</td>
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
<td align="right">15,801</td>
<td align="right">74.3%</td>
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
<td align="right">21,273</td>
<td align="right"></td>
<td align="right">1,964</td>
<td align="right"></td>
<td align="right">-90.8%</td>
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
Trace too short
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it is too short.
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
<td align="right">6</td>
<td align="right">0.3%</td>
<td align="right">6 / 0 !!</td>
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
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">4</td>
<td align="right"></td>
<td align="right">154</td>
<td align="right"></td>
<td align="right">3,750.0%</td>
</tr>
<tr>
<td align="left">
Optimizer successes
<details>
<summary>ⓘ</summary>

The number of traces that were successfully optimized.
</details>
</td>
<td align="right">4</td>
<td align="right">100.0%</td>
<td align="right">154</td>
<td align="right">100.0%</td>
<td align="right">3,750.0%</td>
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
<td align="right">29,695</td>
<td align="right">60.4%</td>
<td align="right">2,482,370</td>
<td align="right">87.8%</td>
<td align="right">8,259.6%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">49,152</td>
<td align="right"></td>
<td align="right">2,826,240</td>
<td align="right"></td>
<td align="right">5,650.0%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">816</td>
<td align="right">1.7%</td>
<td align="right">46,144</td>
<td align="right">1.6%</td>
<td align="right">5,554.9%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">18,635</td>
<td align="right">37.9%</td>
<td align="right">297,570</td>
<td align="right">10.5%</td>
<td align="right">1,496.8%</td>
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
<td align="left">2</td>
<td align="right">33.3%</td>
<td align="left">83</td>
<td align="right">53.2%</td>
<td align="right">4,050.0%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">2</td>
<td align="right">33.3%</td>
<td align="left">1</td>
<td align="right">0.6%</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">2</td>
<td align="right">33.3%</td>
<td align="left">23</td>
<td align="right">14.7%</td>
<td align="right">1,050.0%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">27</td>
<td align="right">17.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">22</td>
<td align="right">14.1%</td>
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
<td align="left"><= 64</td>
<td align="right">2</td>
<td align="right">50.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">1</td>
<td align="right">25.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">1</td>
<td align="right">25.0%</td>
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
<td align="left"><= 32</td>
<td align="right">2</td>
<td align="right">50.0%</td>
<td align="right">66</td>
<td align="right">42.9%</td>
<td align="right">3,200.0%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">1</td>
<td align="right">25.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">1</td>
<td align="right">25.0%</td>
<td align="right">24</td>
<td align="right">15.6%</td>
<td align="right">2,300.0%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">16</td>
<td align="right">10.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">26</td>
<td align="right">16.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">22</td>
<td align="right">14.3%</td>
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
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">2,807</td>
<td align="right">55,066,291</td>
<td align="right">1,961,648.9%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">2,807</td>
<td align="right">25,337,684</td>
<td align="right">902,560.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">2,807</td>
<td align="right">4,072,841</td>
<td align="right">144,995.9%</td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right">1</td>
<td align="right">425</td>
<td align="right">42,400.0%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">33,684</td>
<td align="right">14,042,913</td>
<td align="right">41,590.2%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,806</td>
<td align="right">167,928</td>
<td align="right">5,884.6%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,283,916</td>
<td align="right">43,344,792</td>
<td align="right">3,276.0%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">2,836,973</td>
<td align="right">56,417,372</td>
<td align="right">1,888.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">1,283,916</td>
<td align="right">23,335,178</td>
<td align="right">1,717.5%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">29,856,915</td>
<td align="right">405,923,691</td>
<td align="right">1,259.6%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">4,121,018</td>
<td align="right">48,900,536</td>
<td align="right">1,086.6%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">4,118,212</td>
<td align="right">48,732,608</td>
<td align="right">1,083.3%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">4,118,211</td>
<td align="right">46,444,748</td>
<td align="right">1,027.8%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">4,118,208</td>
<td align="right">45,716,960</td>
<td align="right">1,010.1%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">28,572,998</td>
<td align="right">303,137,798</td>
<td align="right">960.9%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">5,401,995</td>
<td align="right">52,333,359</td>
<td align="right">868.8%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,283,916</td>
<td align="right">11,506,243</td>
<td align="right">796.2%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">1,283,916</td>
<td align="right">10,742,232</td>
<td align="right">736.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">10,542,012</td>
<td align="right">87,914,018</td>
<td align="right">733.9%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">1,283,916</td>
<td align="right">9,875,880</td>
<td align="right">669.2%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,572,185</td>
<td align="right">18,907,739</td>
<td align="right">635.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">11,070,321</td>
<td align="right">51,208,848</td>
<td align="right">362.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_LIST</td>
<td align="right">1,288,140</td>
<td align="right">5,581,986</td>
<td align="right">333.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">1,288,140</td>
<td align="right">5,581,986</td>
<td align="right">333.3%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">4,121,015</td>
<td align="right">16,808,508</td>
<td align="right">307.9%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">2,834,163</td>
<td align="right">11,343,583</td>
<td align="right">300.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">4,118,208</td>
<td align="right">15,265,881</td>
<td align="right">270.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">1,283,916</td>
<td align="right">4,649,099</td>
<td align="right">262.1%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right">1,283,916</td>
<td align="right">3,903,100</td>
<td align="right">204.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">4,118,079</td>
<td align="right">11,981,658</td>
<td align="right">191.0%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">2,834,167</td>
<td align="right">8,067,757</td>
<td align="right">184.7%</td>
</tr>
<tr>
<td align="left">_PY_FRAME_GENERAL</td>
<td align="right">1,283,916</td>
<td align="right">2,643,587</td>
<td align="right">105.9%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">1,283,916</td>
<td align="right">2,254,971</td>
<td align="right">75.6%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">2,806</td>
<td align="right">902</td>
<td align="right">-67.9%</td>
</tr>
<tr>
<td align="left">_CALL_KW_NON_PY</td>
<td align="right">2,807</td>
<td align="right">903</td>
<td align="right">-67.8%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE_KW</td>
<td align="right">2,807</td>
<td align="right">903</td>
<td align="right">-67.8%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">2,807</td>
<td align="right">903</td>
<td align="right">-67.8%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">2,810</td>
<td align="right">904</td>
<td align="right">-67.8%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">2,810</td>
<td align="right">904</td>
<td align="right">-67.8%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">1,283,916</td>
<td align="right">2,038,986</td>
<td align="right">58.8%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,283,916</td>
<td align="right">638,075</td>
<td align="right">-50.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_ANY_SET</td>
<td align="right">1,283,916</td>
<td align="right">638,075</td>
<td align="right">-50.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">1,283,916</td>
<td align="right">638,075</td>
<td align="right">-50.3%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">1,283,916</td>
<td align="right">638,075</td>
<td align="right">-50.3%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">4,118,079</td>
<td align="right">4,700,246</td>
<td align="right">14.1%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">1,283,916</td>
<td align="right">1,272,809</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">1,283,916</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">83,875,221</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right"></td>
<td align="right">64,730,463</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right">50,004,963</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right"></td>
<td align="right">34,947,128</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">31,839,145</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">29,795,753</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right"></td>
<td align="right">23,127,083</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right"></td>
<td align="right">19,297,641</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_TUPLE</td>
<td align="right"></td>
<td align="right">19,224,443</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right"></td>
<td align="right">18,388,745</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right"></td>
<td align="right">18,340,226</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right"></td>
<td align="right">17,122,197</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right"></td>
<td align="right">13,830,150</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_0</td>
<td align="right"></td>
<td align="right">13,680,595</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right"></td>
<td align="right">11,791,796</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right"></td>
<td align="right">10,734,676</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right"></td>
<td align="right">10,440,711</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right"></td>
<td align="right">10,353,040</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right"></td>
<td align="right">8,955,453</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right"></td>
<td align="right">8,788,131</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right"></td>
<td align="right">8,494,319</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right"></td>
<td align="right">8,494,319</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right"></td>
<td align="right">6,839,132</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right"></td>
<td align="right">6,373,971</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">6,371,523</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right"></td>
<td align="right">6,323,984</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right"></td>
<td align="right">6,256,196</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right"></td>
<td align="right">6,109,750</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right"></td>
<td align="right">6,019,935</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">5,360,696</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right"></td>
<td align="right">5,254,972</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right"></td>
<td align="right">4,927,424</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right"></td>
<td align="right">4,927,424</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right"></td>
<td align="right">4,876,181</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">4,833,620</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_1</td>
<td align="right"></td>
<td align="right">4,708,150</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right"></td>
<td align="right">4,282,039</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right"></td>
<td align="right">4,198,886</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right"></td>
<td align="right">4,179,596</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right"></td>
<td align="right">4,169,641</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right"></td>
<td align="right">4,117,668</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">4,117,668</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right"></td>
<td align="right">4,013,290</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right"></td>
<td align="right">3,986,142</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right"></td>
<td align="right">3,986,142</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right"></td>
<td align="right">3,399,248</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right"></td>
<td align="right">2,840,507</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right"></td>
<td align="right">2,769,523</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right"></td>
<td align="right">2,642,857</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right"></td>
<td align="right">2,630,291</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right"></td>
<td align="right">2,297,940</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">2,286,839</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NULL</td>
<td align="right"></td>
<td align="right">2,135,922</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right"></td>
<td align="right">2,112,156</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right"></td>
<td align="right">2,078,710</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">2,006,645</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">2,006,645</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">2,006,645</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right"></td>
<td align="right">2,006,645</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right"></td>
<td align="right">2,005,512</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right"></td>
<td align="right">2,005,512</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">2,005,512</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right"></td>
<td align="right">1,922,359</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right"></td>
<td align="right">1,575,275</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right"></td>
<td align="right">1,288,758</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_STR_1</td>
<td align="right"></td>
<td align="right">1,288,758</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_TYPE_1</td>
<td align="right"></td>
<td align="right">847,164</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right"></td>
<td align="right">764,032</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right"></td>
<td align="right">764,032</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_OVERFLOWED</td>
<td align="right"></td>
<td align="right">764,032</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_METHOD_VERSION_KW</td>
<td align="right"></td>
<td align="right">764,011</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXPAND_METHOD_KW</td>
<td align="right"></td>
<td align="right">764,011</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PY_FRAME_KW</td>
<td align="right"></td>
<td align="right">764,011</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right"></td>
<td align="right">636,212</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right"></td>
<td align="right">203,364</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right"></td>
<td align="right">167,026</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right"></td>
<td align="right">167,026</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right"></td>
<td align="right">166,306</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right"></td>
<td align="right">83,153</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right"></td>
<td align="right">83,153</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right"></td>
<td align="right">83,153</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right"></td>
<td align="right">83,153</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right"></td>
<td align="right">73,198</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right">73,198</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right"></td>
<td align="right">73,198</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_SLICE</td>
<td align="right"></td>
<td align="right">73,198</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right"></td>
<td align="right">596</td>
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
Stats gathered on: 2025-10-23
