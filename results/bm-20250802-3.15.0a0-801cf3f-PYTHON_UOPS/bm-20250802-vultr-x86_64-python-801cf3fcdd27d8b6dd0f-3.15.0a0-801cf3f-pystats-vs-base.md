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
<td align="right">5,874,855,008</td>
<td align="right">6,775,942</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">112,725,134</td>
<td align="right">1,232,574</td>
<td align="right">-98.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">441,311,212</td>
<td align="right">13,408,958</td>
<td align="right">-97.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">62,109,938</td>
<td align="right">2,075,069</td>
<td align="right">-96.7%</td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">100,136,760</td>
<td align="right">6,000,000</td>
<td align="right">-94.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,506,631,831</td>
<td align="right">213,686,685</td>
<td align="right">-85.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">691,982,607</td>
<td align="right">103,564,937</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,753,419,233</td>
<td align="right">272,671,005</td>
<td align="right">-84.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">577,934,918</td>
<td align="right">97,092,446</td>
<td align="right">-83.2%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,218,036,588</td>
<td align="right">209,958,687</td>
<td align="right">-82.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">2,722,713,947</td>
<td align="right">469,563,836</td>
<td align="right">-82.8%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">2,130,888,980</td>
<td align="right">406,600,049</td>
<td align="right">-80.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">353,326,884</td>
<td align="right">76,414,650</td>
<td align="right">-78.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">1,255,486,715</td>
<td align="right">279,536,810</td>
<td align="right">-77.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">531,309,698</td>
<td align="right">124,379,299</td>
<td align="right">-76.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,727,671,208</td>
<td align="right">903,468,379</td>
<td align="right">-75.8%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,545,180,776</td>
<td align="right">385,589,855</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">160,417,226</td>
<td align="right">40,085,257</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,831,237,287</td>
<td align="right">481,390,023</td>
<td align="right">-73.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">681,992,973</td>
<td align="right">186,174,050</td>
<td align="right">-72.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,460,920,533</td>
<td align="right">671,965,201</td>
<td align="right">-72.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">942,844,047</td>
<td align="right">258,385,474</td>
<td align="right">-72.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">510,992,416</td>
<td align="right">146,022,524</td>
<td align="right">-71.4%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">682,455,759</td>
<td align="right">196,353,373</td>
<td align="right">-71.2%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">374,560,148</td>
<td align="right">110,708,071</td>
<td align="right">-70.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">199,520,089</td>
<td align="right">59,356,489</td>
<td align="right">-70.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">540,359,282</td>
<td align="right">172,305,452</td>
<td align="right">-68.1%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">57,251,720</td>
<td align="right">18,641,452</td>
<td align="right">-67.4%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">7,779,507,527</td>
<td align="right">2,539,228,357</td>
<td align="right">-67.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">2,158,794,370</td>
<td align="right">720,883,840</td>
<td align="right">-66.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,129,749,160</td>
<td align="right">379,315,848</td>
<td align="right">-66.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,510,679,855</td>
<td align="right">1,180,065,177</td>
<td align="right">-66.4%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">158,352,274</td>
<td align="right">55,173,576</td>
<td align="right">-65.2%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">94,136,760</td>
<td align="right">154,962,938</td>
<td align="right">64.6%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">542,033,124</td>
<td align="right">198,809,226</td>
<td align="right">-63.3%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">112,863,364</td>
<td align="right">42,461,040</td>
<td align="right">-62.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,679,398,039</td>
<td align="right">1,012,177,469</td>
<td align="right">-62.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,936,410,573</td>
<td align="right">744,439,576</td>
<td align="right">-61.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">10,633,626,517</td>
<td align="right">4,175,871,097</td>
<td align="right">-60.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">379,811,554</td>
<td align="right">149,441,348</td>
<td align="right">-60.7%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">67,396,554</td>
<td align="right">26,549,465</td>
<td align="right">-60.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">1,154,001,039</td>
<td align="right">456,210,664</td>
<td align="right">-60.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">442,054,546</td>
<td align="right">174,957,179</td>
<td align="right">-60.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">23,179,833</td>
<td align="right">9,211,640</td>
<td align="right">-60.3%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">263,718,109</td>
<td align="right">105,441,020</td>
<td align="right">-60.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,736,000,423</td>
<td align="right">1,127,472,067</td>
<td align="right">-58.8%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">752,122,646</td>
<td align="right">310,967,128</td>
<td align="right">-58.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">14,494,189,061</td>
<td align="right">6,010,316,076</td>
<td align="right">-58.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">539,588,803</td>
<td align="right">226,085,597</td>
<td align="right">-58.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">3,297,743,485</td>
<td align="right">1,384,038,382</td>
<td align="right">-58.0%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,156,329</td>
<td align="right">2,600,969</td>
<td align="right">-57.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">888,934,265</td>
<td align="right">381,405,319</td>
<td align="right">-57.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,079,502,741</td>
<td align="right">468,512,517</td>
<td align="right">-56.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">12,156,664,592</td>
<td align="right">5,322,211,087</td>
<td align="right">-56.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">6,849,359,595</td>
<td align="right">3,085,961,856</td>
<td align="right">-54.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">93,694,540</td>
<td align="right">44,742,837</td>
<td align="right">-52.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">832,613,020</td>
<td align="right">398,308,252</td>
<td align="right">-52.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,417,492,915</td>
<td align="right">1,165,740,243</td>
<td align="right">-51.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">320,953,358</td>
<td align="right">156,304,511</td>
<td align="right">-51.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">89,477,513</td>
<td align="right">43,824,920</td>
<td align="right">-51.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">403,200,989</td>
<td align="right">203,171,333</td>
<td align="right">-49.6%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,093,199,523</td>
<td align="right">553,486,697</td>
<td align="right">-49.4%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">100,116,633</td>
<td align="right">51,331,671</td>
<td align="right">-48.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">9,289,752,809</td>
<td align="right">4,783,773,910</td>
<td align="right">-48.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">6,953,466</td>
<td align="right">3,586,960</td>
<td align="right">-48.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">334,687,672</td>
<td align="right">173,801,722</td>
<td align="right">-48.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">303,188,776</td>
<td align="right">161,197,590</td>
<td align="right">-46.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,619,520,628</td>
<td align="right">1,399,665,472</td>
<td align="right">-46.6%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">13,133,596</td>
<td align="right">7,147,453</td>
<td align="right">-45.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">39,557,950,224</td>
<td align="right">21,868,464,775</td>
<td align="right">-44.7%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">973,598,520</td>
<td align="right">549,767,061</td>
<td align="right">-43.5%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,229,818,727</td>
<td align="right">694,888,374</td>
<td align="right">-43.5%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">595,180,651</td>
<td align="right">338,707,356</td>
<td align="right">-43.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">87,696,763</td>
<td align="right">49,973,863</td>
<td align="right">-43.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">117,652,330</td>
<td align="right">67,195,273</td>
<td align="right">-42.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,875,884,378</td>
<td align="right">1,661,382,703</td>
<td align="right">-42.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">146,550,948</td>
<td align="right">85,516,810</td>
<td align="right">-41.6%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">1,054,041,575</td>
<td align="right">617,848,467</td>
<td align="right">-41.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">195,759,976</td>
<td align="right">114,764,823</td>
<td align="right">-41.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">219,417,314</td>
<td align="right">129,844,526</td>
<td align="right">-40.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">295,985,500</td>
<td align="right">176,767,410</td>
<td align="right">-40.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,669,222,837</td>
<td align="right">1,004,158,746</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">233,135,926</td>
<td align="right">140,341,335</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">808,207,325</td>
<td align="right">491,220,229</td>
<td align="right">-39.2%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,369,966,880</td>
<td align="right">842,559,513</td>
<td align="right">-38.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">3,765,622,924</td>
<td align="right">2,364,040,713</td>
<td align="right">-37.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">4,864,439,367</td>
<td align="right">3,099,422,373</td>
<td align="right">-36.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">436,878,355</td>
<td align="right">281,207,918</td>
<td align="right">-35.6%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">116,410,057</td>
<td align="right">75,260,205</td>
<td align="right">-35.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">851,940,781</td>
<td align="right">563,877,916</td>
<td align="right">-33.8%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">123,210,245</td>
<td align="right">81,725,849</td>
<td align="right">-33.7%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">142,158,025</td>
<td align="right">94,420,374</td>
<td align="right">-33.6%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">60,819,253</td>
<td align="right">40,405,088</td>
<td align="right">-33.6%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">62,324,951</td>
<td align="right">41,487,471</td>
<td align="right">-33.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">5,832,186,502</td>
<td align="right">3,890,992,071</td>
<td align="right">-33.3%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">214,357,754</td>
<td align="right">143,958,652</td>
<td align="right">-32.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">251,485,856</td>
<td align="right">172,274,452</td>
<td align="right">-31.5%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">193,705,254</td>
<td align="right">133,869,934</td>
<td align="right">-30.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">66,728,215</td>
<td align="right">46,272,278</td>
<td align="right">-30.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">511,909,750</td>
<td align="right">357,699,429</td>
<td align="right">-30.1%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">437,142,821</td>
<td align="right">312,587,597</td>
<td align="right">-28.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">446,394,695</td>
<td align="right">324,946,838</td>
<td align="right">-27.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">349,921,477</td>
<td align="right">261,847,292</td>
<td align="right">-25.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">4,133,515,309</td>
<td align="right">3,167,598,761</td>
<td align="right">-23.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">1,581,803</td>
<td align="right">1,214,839</td>
<td align="right">-23.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">374,187,570</td>
<td align="right">291,526,514</td>
<td align="right">-22.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">7,488,271,163</td>
<td align="right">5,975,337,434</td>
<td align="right">-20.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">443,663,275</td>
<td align="right">358,483,821</td>
<td align="right">-19.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,658,936,471</td>
<td align="right">2,963,077,338</td>
<td align="right">-19.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">357,274,055</td>
<td align="right">290,116,324</td>
<td align="right">-18.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">3,457,535,374</td>
<td align="right">2,845,291,200</td>
<td align="right">-17.7%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">347,960,986</td>
<td align="right">286,798,339</td>
<td align="right">-17.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">611,672,230</td>
<td align="right">507,439,843</td>
<td align="right">-17.0%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">1,178,261,371</td>
<td align="right">981,752,834</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">87,892</td>
<td align="right">73,592</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">17,299,854</td>
<td align="right">14,619,354</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">292,068,587</td>
<td align="right">247,592,353</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,104,756,897</td>
<td align="right">936,771,807</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">82,140,605</td>
<td align="right">69,953,518</td>
<td align="right">-14.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">6,644,741,630</td>
<td align="right">5,715,812,807</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">589,334,411</td>
<td align="right">509,468,898</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">115,588,676</td>
<td align="right">100,289,396</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">418,093,393</td>
<td align="right">367,578,272</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">124,667,700</td>
<td align="right">109,892,219</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">64,733,893</td>
<td align="right">58,740,070</td>
<td align="right">-9.3%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">78,193,080</td>
<td align="right">71,042,811</td>
<td align="right">-9.1%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">63,239,187</td>
<td align="right">57,880,504</td>
<td align="right">-8.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,600,406,172</td>
<td align="right">1,468,954,964</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">473,447</td>
<td align="right">437,297</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">151,502,832</td>
<td align="right">141,912,826</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">73,771,905</td>
<td align="right">70,311,547</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">10,833,757</td>
<td align="right">10,373,333</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">12,634,082</td>
<td align="right">12,110,063</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">73,046,859</td>
<td align="right">70,257,262</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">10,019,422</td>
<td align="right">9,678,733</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">74,135,772</td>
<td align="right">71,759,916</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">140,586,889</td>
<td align="right">136,830,826</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">6,360,944</td>
<td align="right">6,223,501</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">29,102,664</td>
<td align="right">28,480,481</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">65,348,658</td>
<td align="right">64,623,361</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">346,718,580</td>
<td align="right">343,139,299</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">25,421,974</td>
<td align="right">25,210,473</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">25,764,220</td>
<td align="right">25,552,719</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">25,764,221</td>
<td align="right">25,552,720</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">1,894,402,504</td>
<td align="right">1,880,101,047</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">35,684,632</td>
<td align="right">35,428,137</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">4,491,958</td>
<td align="right">4,459,956</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">220,199,877</td>
<td align="right">218,661,995</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">3,956,236</td>
<td align="right">3,928,649</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,152,796,930</td>
<td align="right">1,148,640,764</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">11,721</td>
<td align="right">11,762</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">91,596</td>
<td align="right">91,336</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">324,894</td>
<td align="right">324,090</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">115,240,002</td>
<td align="right">114,987,829</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">8,632,636</td>
<td align="right">8,614,954</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">419,298,782</td>
<td align="right">418,745,133</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">593,932,750</td>
<td align="right">593,230,375</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">31,012</td>
<td align="right">30,983</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">302,372,867</td>
<td align="right">302,133,017</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">41,995,522</td>
<td align="right">41,963,282</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">223,541</td>
<td align="right">223,646</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">131,427,681</td>
<td align="right">131,373,381</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">6,269,306</td>
<td align="right">6,267,746</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,456,875</td>
<td align="right">128,425,585</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">323,990,503</td>
<td align="right">323,929,073</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">326,043,393</td>
<td align="right">325,981,961</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">6,491</td>
<td align="right">6,492</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">165,489,591</td>
<td align="right">165,476,593</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">14,737,724</td>
<td align="right">14,737,852</td>
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
<td align="right">9,738,717</td>
<td align="right">9,738,717</td>
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
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">1,685,022</td>
<td align="right">1,685,022</td>
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
<td align="left">STORE_NAME</td>
<td align="right">47,863</td>
<td align="right">47,863</td>
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
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">2,369</td>
<td align="right">2,369</td>
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
<td align="right">1,114,022,119</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right"></td>
<td align="right">872,969,166</td>
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
<td align="right">17,014,648,689</td>
<td align="right">87.2%</td>
<td align="right">4,821,500,721</td>
<td align="right">79.7%</td>
<td align="right">-71.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,416,545,973</td>
<td align="right">12.4%</td>
<td align="right">1,165,239,711</td>
<td align="right">19.3%</td>
<td align="right">-51.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">72,193,975</td>
<td align="right">0.4%</td>
<td align="right">64,609,771</td>
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
<td align="right">930,316</td>
<td align="right">40.3%</td>
<td align="right">483,884</td>
<td align="right">28.1%</td>
<td align="right">-48.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,378,552</td>
<td align="right">59.7%</td>
<td align="right">1,235,474</td>
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
<td align="right">11,587</td>
<td align="right">1.2%</td>
<td align="right">2,767</td>
<td align="right">0.6%</td>
<td align="right">-76.1%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">74,226</td>
<td align="right">8.0%</td>
<td align="right">18,473</td>
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
<td align="right">1,078</td>
<td align="right">0.1%</td>
<td align="right">315</td>
<td align="right">0.1%</td>
<td align="right">-70.8%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">23,527</td>
<td align="right">2.5%</td>
<td align="right">8,297</td>
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
<td align="right">43,756</td>
<td align="right">4.7%</td>
<td align="right">20,483</td>
<td align="right">4.2%</td>
<td align="right">-53.2%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">34,120</td>
<td align="right">3.7%</td>
<td align="right">20,048</td>
<td align="right">4.1%</td>
<td align="right">-41.2%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">19,440</td>
<td align="right">2.1%</td>
<td align="right">11,542</td>
<td align="right">2.4%</td>
<td align="right">-40.6%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">15,012</td>
<td align="right">1.6%</td>
<td align="right">9,122</td>
<td align="right">1.9%</td>
<td align="right">-39.2%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">8,519</td>
<td align="right">0.9%</td>
<td align="right">6,189</td>
<td align="right">1.3%</td>
<td align="right">-27.4%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">37,903</td>
<td align="right">4.1%</td>
<td align="right">28,450</td>
<td align="right">5.9%</td>
<td align="right">-24.9%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">78,846</td>
<td align="right">8.5%</td>
<td align="right">62,859</td>
<td align="right">13.0%</td>
<td align="right">-20.3%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">43,532</td>
<td align="right">4.7%</td>
<td align="right">36,453</td>
<td align="right">7.5%</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">46,907</td>
<td align="right">5.0%</td>
<td align="right">41,345</td>
<td align="right">8.5%</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">2,162</td>
<td align="right">0.2%</td>
<td align="right">1,961</td>
<td align="right">0.4%</td>
<td align="right">-9.3%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">7,696</td>
<td align="right">0.8%</td>
<td align="right">6,999</td>
<td align="right">1.4%</td>
<td align="right">-9.1%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">2,681</td>
<td align="right">0.3%</td>
<td align="right">2,616</td>
<td align="right">0.5%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">14,292</td>
<td align="right">1.5%</td>
<td align="right">13,977</td>
<td align="right">2.9%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">subscr deque</td>
<td align="right">99</td>
<td align="right">0.0%</td>
<td align="right">98</td>
<td align="right">0.0%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">631</td>
<td align="right">0.1%</td>
<td align="right">626</td>
<td align="right">0.1%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">1,388</td>
<td align="right">0.1%</td>
<td align="right">1,383</td>
<td align="right">0.3%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">3,103</td>
<td align="right">0.3%</td>
<td align="right">3,100</td>
<td align="right">0.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">2,214</td>
<td align="right">0.2%</td>
<td align="right">2,213</td>
<td align="right">0.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">109,554</td>
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
<td align="right">542,033,124</td>
<td align="right">100.0%</td>
<td align="right">198,809,226</td>
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
<td align="right">12,569,648,815</td>
<td align="right">98.4%</td>
<td align="right">6,504,093,099</td>
<td align="right">97.5%</td>
<td align="right">-48.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">206,236,930</td>
<td align="right">1.6%</td>
<td align="right">168,053,897</td>
<td align="right">2.5%</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">202,408,053</td>
<td align="right">1.6%</td>
<td align="right">164,945,340</td>
<td align="right">2.5%</td>
<td align="right">-18.5%</td>
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
<td align="right">4,052,272</td>
<td align="right">100.0%</td>
<td align="right">3,332,057</td>
<td align="right">100.0%</td>
<td align="right">-17.8%</td>
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
<td align="right">536,954</td>
<td align="right">96.6%</td>
<td align="right">536,738</td>
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
<td align="right">544,066</td>
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
<td align="right">18,833</td>
<td align="right">100.0%</td>
<td align="right">18,873</td>
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
<td align="right">531,075,216</td>
<td align="right">9.1%</td>
<td align="right">124,244,336</td>
<td align="right">5.9%</td>
<td align="right">-76.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,323,431,124</td>
<td align="right">90.9%</td>
<td align="right">1,978,887,516</td>
<td align="right">94.0%</td>
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
<td align="right">1,309,624</td>
<td align="right">0.0%</td>
<td align="right">1,305,832</td>
<td align="right">0.1%</td>
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
<td align="left">Failure</td>
<td align="right">212,754</td>
<td align="right">82.1%</td>
<td align="right">113,222</td>
<td align="right">71.0%</td>
<td align="right">-46.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">46,417</td>
<td align="right">17.9%</td>
<td align="right">46,320</td>
<td align="right">29.0%</td>
<td align="right">-0.2%</td>
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
<td align="right">84,960</td>
<td align="right">39.9%</td>
<td align="right">4,102</td>
<td align="right">3.6%</td>
<td align="right">-95.2%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">6,822</td>
<td align="right">3.2%</td>
<td align="right">362</td>
<td align="right">0.3%</td>
<td align="right">-94.7%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">10,939</td>
<td align="right">5.1%</td>
<td align="right">6,204</td>
<td align="right">5.5%</td>
<td align="right">-43.3%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">14,809</td>
<td align="right">7.0%</td>
<td align="right">8,917</td>
<td align="right">7.9%</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">1,960</td>
<td align="right">0.9%</td>
<td align="right">1,849</td>
<td align="right">1.6%</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">39,626</td>
<td align="right">18.6%</td>
<td align="right">38,703</td>
<td align="right">34.2%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">932</td>
<td align="right">0.4%</td>
<td align="right">911</td>
<td align="right">0.8%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">9,899</td>
<td align="right">4.7%</td>
<td align="right">9,729</td>
<td align="right">8.6%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">30,594</td>
<td align="right">14.4%</td>
<td align="right">30,250</td>
<td align="right">26.7%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">10,679</td>
<td align="right">5.0%</td>
<td align="right">10,662</td>
<td align="right">9.4%</td>
<td align="right">-0.2%</td>
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
<td align="right">2,194,071,641</td>
<td align="right">90.3%</td>
<td align="right">446,226,046</td>
<td align="right">75.9%</td>
<td align="right">-79.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">233,057,032</td>
<td align="right">9.6%</td>
<td align="right">140,285,197</td>
<td align="right">23.9%</td>
<td align="right">-39.8%</td>
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
<td align="right">77,029</td>
<td align="right">73.1%</td>
<td align="right">54,273</td>
<td align="right">65.7%</td>
<td align="right">-29.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">28,317</td>
<td align="right">26.9%</td>
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
<td align="right">25,221</td>
<td align="right">32.7%</td>
<td align="right">10,869</td>
<td align="right">20.0%</td>
<td align="right">-56.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">12,249</td>
<td align="right">15.9%</td>
<td align="right">9,124</td>
<td align="right">16.8%</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">29,005</td>
<td align="right">37.7%</td>
<td align="right">24,280</td>
<td align="right">44.7%</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">10,554</td>
<td align="right">13.7%</td>
<td align="right">10,000</td>
<td align="right">18.4%</td>
<td align="right">-5.2%</td>
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
<td align="right">1,506,185,417</td>
<td align="right">28.8%</td>
<td align="right">213,567,718</td>
<td align="right">13.1%</td>
<td align="right">-85.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">164,187,843</td>
<td align="right">3.1%</td>
<td align="right">62,130,162</td>
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
<td align="right">3,563,677,362</td>
<td align="right">68.1%</td>
<td align="right">1,360,372,479</td>
<td align="right">83.1%</td>
<td align="right">-61.8%</td>
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
<td align="right">440,641</td>
<td align="right">12.4%</td>
<td align="right">113,212</td>
<td align="right">8.8%</td>
<td align="right">-74.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,103,501</td>
<td align="right">87.6%</td>
<td align="right">1,177,870</td>
<td align="right">91.2%</td>
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
<td align="right">161,275</td>
<td align="right">36.6%</td>
<td align="right">4,127</td>
<td align="right">3.6%</td>
<td align="right">-97.4%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">83,599</td>
<td align="right">19.0%</td>
<td align="right">10,915</td>
<td align="right">9.6%</td>
<td align="right">-86.9%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">34,594</td>
<td align="right">7.9%</td>
<td align="right">6,251</td>
<td align="right">5.5%</td>
<td align="right">-81.9%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">18,158</td>
<td align="right">4.1%</td>
<td align="right">4,077</td>
<td align="right">3.6%</td>
<td align="right">-77.5%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">1,120</td>
<td align="right">0.3%</td>
<td align="right">280</td>
<td align="right">0.2%</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">19,424</td>
<td align="right">4.4%</td>
<td align="right">6,473</td>
<td align="right">5.7%</td>
<td align="right">-66.7%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">3,310</td>
<td align="right">0.8%</td>
<td align="right">1,148</td>
<td align="right">1.0%</td>
<td align="right">-65.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">11,770</td>
<td align="right">2.7%</td>
<td align="right">4,246</td>
<td align="right">3.8%</td>
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
<td align="right">1,671</td>
<td align="right">1.5%</td>
<td align="right">-46.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">18,346</td>
<td align="right">4.2%</td>
<td align="right">12,432</td>
<td align="right">11.0%</td>
<td align="right">-32.2%</td>
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
<td align="right">74,653</td>
<td align="right">16.9%</td>
<td align="right">51,951</td>
<td align="right">45.9%</td>
<td align="right">-30.4%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">4,326</td>
<td align="right">1.0%</td>
<td align="right">3,430</td>
<td align="right">3.0%</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">6,037</td>
<td align="right">1.4%</td>
<td align="right">5,597</td>
<td align="right">4.9%</td>
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
<td align="left">set</td>
<td align="right">12,635,471</td>
<td align="right">12,635,471 / 0 !!</td>
<td align="right">12,106,485</td>
<td align="right">12,106,485 / 0 !!</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">126,750,562</td>
<td align="right">126,750,562 / 0 !!</td>
<td align="right">124,465,540</td>
<td align="right">124,465,540 / 0 !!</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">312,233,807</td>
<td align="right">312,233,807 / 0 !!</td>
<td align="right">306,930,747</td>
<td align="right">306,930,747 / 0 !!</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">173,570,994</td>
<td align="right">173,570,994 / 0 !!</td>
<td align="right">172,547,763</td>
<td align="right">172,547,763 / 0 !!</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">5,402,437</td>
<td align="right">5,402,437 / 0 !!</td>
<td align="right">5,390,215</td>
<td align="right">5,390,215 / 0 !!</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">322,590,075</td>
<td align="right">322,590,075 / 0 !!</td>
<td align="right">322,191,474</td>
<td align="right">322,191,474 / 0 !!</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">101,651,908</td>
<td align="right">101,651,908 / 0 !!</td>
<td align="right">101,600,680</td>
<td align="right">101,600,680 / 0 !!</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">2,769,211</td>
<td align="right">2,769,211 / 0 !!</td>
<td align="right">2,768,951</td>
<td align="right">2,768,951 / 0 !!</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">34,819,618</td>
<td align="right">34,819,618 / 0 !!</td>
<td align="right">34,819,618</td>
<td align="right">34,819,618 / 0 !!</td>
<td align="right">0.0%</td>
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
<td align="right">15,759,068,059</td>
<td align="right">90.2%</td>
<td align="right">10,081,416,087</td>
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
<td align="right">850,178,359</td>
<td align="right">4.9%</td>
<td align="right">562,209,530</td>
<td align="right">5.0%</td>
<td align="right">-33.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">869,194,877</td>
<td align="right">5.0%</td>
<td align="right">617,525,654</td>
<td align="right">5.5%</td>
<td align="right">-29.0%</td>
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
<td align="right">16,476,100</td>
<td align="right">97.0%</td>
<td align="right">11,727,589</td>
<td align="right">96.4%</td>
<td align="right">-28.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">513,807</td>
<td align="right">3.0%</td>
<td align="right">439,636</td>
<td align="right">3.6%</td>
<td align="right">-14.4%</td>
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
<td align="right">80,904</td>
<td align="right">15.7%</td>
<td align="right">43,263</td>
<td align="right">9.8%</td>
<td align="right">-46.5%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">1,079</td>
<td align="right">0.2%</td>
<td align="right">718</td>
<td align="right">0.2%</td>
<td align="right">-33.5%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">59,367</td>
<td align="right">11.6%</td>
<td align="right">40,154</td>
<td align="right">9.1%</td>
<td align="right">-32.4%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">5,977</td>
<td align="right">1.2%</td>
<td align="right">4,687</td>
<td align="right">1.1%</td>
<td align="right">-21.6%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">2,737</td>
<td align="right">0.5%</td>
<td align="right">2,374</td>
<td align="right">0.5%</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">53,052</td>
<td align="right">10.3%</td>
<td align="right">47,762</td>
<td align="right">10.9%</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">17,110</td>
<td align="right">3.3%</td>
<td align="right">16,351</td>
<td align="right">3.7%</td>
<td align="right">-4.4%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">24,287</td>
<td align="right">4.7%</td>
<td align="right">23,223</td>
<td align="right">5.3%</td>
<td align="right">-4.4%</td>
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
<td align="left">overridden</td>
<td align="right">7,652</td>
<td align="right">1.5%</td>
<td align="right">7,626</td>
<td align="right">1.7%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">4,345</td>
<td align="right">0.8%</td>
<td align="right">4,345</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1,822</td>
<td align="right">0.4%</td>
<td align="right">1,822</td>
<td align="right">0.4%</td>
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
<td align="left">class attr simple</td>
<td align="right">781</td>
<td align="right">0.2%</td>
<td align="right">781</td>
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
<td align="right">10,982,833,070</td>
<td align="right">99.9%</td>
<td align="right">6,253,518,785</td>
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
<td align="right">41,834</td>
<td align="right">0.0%</td>
<td align="right">41,832</td>
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
<td align="right">14,612,325</td>
<td align="right">0.1%</td>
<td align="right">14,612,272</td>
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
<td align="right">16</td>
<td align="right">0.0%</td>
<td align="right">16</td>
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
<td align="right">126,101</td>
<td align="right">100.0%</td>
<td align="right">126,282</td>
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
<td align="right">67,731,145</td>
<td align="right">100.0%</td>
<td align="right">62,340,460</td>
<td align="right">100.0%</td>
<td align="right">-8.0%</td>
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
<td align="right">110</td>
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
<td align="right">27,600</td>
<td align="right">0.0%</td>
<td align="right">14,711</td>
<td align="right">0.0%</td>
<td align="right">-46.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">593,905,150</td>
<td align="right">82.2%</td>
<td align="right">593,215,664</td>
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
<td align="right">128,421,336</td>
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
<td align="right">852</td>
<td align="right">2.4%</td>
<td align="right">616</td>
<td align="right">1.8%</td>
<td align="right">-27.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">35,215</td>
<td align="right">97.6%</td>
<td align="right">33,951</td>
<td align="right">98.2%</td>
<td align="right">-3.6%</td>
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
<td align="right">4,187</td>
<td align="right">11.9%</td>
<td align="right">2,923</td>
<td align="right">8.6%</td>
<td align="right">-30.2%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,599,917,114</td>
<td align="right">93.6%</td>
<td align="right">2,306,107,859</td>
<td align="right">93.2%</td>
<td align="right">-11.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">64,649,273</td>
<td align="right">2.3%</td>
<td align="right">58,656,720</td>
<td align="right">2.4%</td>
<td align="right">-9.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">114,221,948</td>
<td align="right">4.1%</td>
<td align="right">108,594,905</td>
<td align="right">4.4%</td>
<td align="right">-4.9%</td>
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
<td align="right">2,194,489</td>
<td align="right">98.0%</td>
<td align="right">2,088,465</td>
<td align="right">98.0%</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">44,953</td>
<td align="right">2.0%</td>
<td align="right">43,522</td>
<td align="right">2.0%</td>
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
<td align="left">overriding descriptor</td>
<td align="right">6,084</td>
<td align="right">13.5%</td>
<td align="right">4,651</td>
<td align="right">10.7%</td>
<td align="right">-23.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">243,550</td>
<td align="right">541.8%</td>
<td align="right">236,078</td>
<td align="right">542.4%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">2,954</td>
<td align="right">6.6%</td>
<td align="right">2,977</td>
<td align="right">6.8%</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">20,316</td>
<td align="right">45.2%</td>
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
<td align="right">112,725,134</td>
<td align="right">100.0%</td>
<td align="right">1,232,574</td>
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
<td align="right">691,799,819</td>
<td align="right">41.9%</td>
<td align="right">103,525,799</td>
<td align="right">29.6%</td>
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
<td align="right">957,744,252</td>
<td align="right">58.1%</td>
<td align="right">246,531,574</td>
<td align="right">70.4%</td>
<td align="right">-74.3%</td>
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
<td align="right">179,870</td>
<td align="right">98.4%</td>
<td align="right">36,219</td>
<td align="right">92.4%</td>
<td align="right">-79.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,958</td>
<td align="right">1.6%</td>
<td align="right">2,959</td>
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
<td align="right">19,298</td>
<td align="right">10.7%</td>
<td align="right">3,283</td>
<td align="right">9.1%</td>
<td align="right">-83.0%</td>
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
<td align="left">py simple</td>
<td align="right">17,279</td>
<td align="right">9.6%</td>
<td align="right">17,279</td>
<td align="right">47.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">2,976</td>
<td align="right">1.7%</td>
<td align="right">2,976</td>
<td align="right">8.2%</td>
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
<td align="right">111,379,495</td>
<td align="right">1.7%</td>
<td align="right">64,962,508</td>
<td align="right">1.6%</td>
<td align="right">-41.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,812,585,110</td>
<td align="right">91.2%</td>
<td align="right">3,669,467,849</td>
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
<td align="right">445,699,483</td>
<td align="right">7.0%</td>
<td align="right">324,349,157</td>
<td align="right">8.0%</td>
<td align="right">-27.2%</td>
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
<td align="right">2,149,558</td>
<td align="right">76.9%</td>
<td align="right">1,273,824</td>
<td align="right">69.9%</td>
<td align="right">-40.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">645,706</td>
<td align="right">23.1%</td>
<td align="right">548,179</td>
<td align="right">30.1%</td>
<td align="right">-15.1%</td>
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
<td align="right">127,013</td>
<td align="right">19.7%</td>
<td align="right">59,366</td>
<td align="right">10.8%</td>
<td align="right">-53.3%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">16,248</td>
<td align="right">2.5%</td>
<td align="right">10,893</td>
<td align="right">2.0%</td>
<td align="right">-33.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">85,959</td>
<td align="right">13.3%</td>
<td align="right">75,932</td>
<td align="right">13.9%</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">9,779</td>
<td align="right">1.5%</td>
<td align="right">9,507</td>
<td align="right">1.7%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">9,459</td>
<td align="right">1.5%</td>
<td align="right">9,450</td>
<td align="right">1.7%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">71,756</td>
<td align="right">11.1%</td>
<td align="right">71,768</td>
<td align="right">13.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">309,008</td>
<td align="right">47.9%</td>
<td align="right">308,979</td>
<td align="right">56.4%</td>
<td align="right">-0.0%</td>
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
<td align="right">1,273,514,552</td>
<td align="right">99.9%</td>
<td align="right">696,462,931</td>
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
<td align="right">1,571,229</td>
<td align="right">0.1%</td>
<td align="right">1,204,388</td>
<td align="right">0.2%</td>
<td align="right">-23.3%</td>
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
<td align="right">860</td>
<td align="right">8.1%</td>
<td align="right">737</td>
<td align="right">7.0%</td>
<td align="right">-14.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">9,794</td>
<td align="right">91.9%</td>
<td align="right">9,794</td>
<td align="right">93.0%</td>
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
<td align="right">629</td>
<td align="right">73.1%</td>
<td align="right">506</td>
<td align="right">68.7%</td>
<td align="right">-19.6%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">132</td>
<td align="right">15.3%</td>
<td align="right">132</td>
<td align="right">17.9%</td>
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
<td align="right">8,636,594,160</td>
<td align="right">3.6%</td>
<td align="right">3,593,421,873</td>
<td align="right">2.9%</td>
<td align="right">-58.4%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">90,939,268,024</td>
<td align="right">38.3%</td>
<td align="right">46,675,342,565</td>
<td align="right">37.9%</td>
<td align="right">-48.7%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">136,405,040,987</td>
<td align="right">57.4%</td>
<td align="right">71,882,430,959</td>
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
<td align="right">1,540,904,836</td>
<td align="right">0.6%</td>
<td align="right">1,089,353,509</td>
<td align="right">0.9%</td>
<td align="right">-29.3%</td>
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
<td align="right">1,506,185,417</td>
<td align="right">19.5%</td>
<td align="right">213,567,718</td>
<td align="right">6.7%</td>
<td align="right">-85.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">691,799,819</td>
<td align="right">8.9%</td>
<td align="right">103,525,799</td>
<td align="right">3.2%</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">531,075,216</td>
<td align="right">6.9%</td>
<td align="right">124,244,336</td>
<td align="right">3.9%</td>
<td align="right">-76.6%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">542,033,124</td>
<td align="right">7.0%</td>
<td align="right">198,809,226</td>
<td align="right">6.2%</td>
<td align="right">-63.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,416,545,973</td>
<td align="right">31.2%</td>
<td align="right">1,165,239,711</td>
<td align="right">36.4%</td>
<td align="right">-51.8%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">233,057,032</td>
<td align="right">3.0%</td>
<td align="right">140,285,197</td>
<td align="right">4.4%</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">850,178,359</td>
<td align="right">11.0%</td>
<td align="right">562,209,530</td>
<td align="right">17.6%</td>
<td align="right">-33.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">445,699,483</td>
<td align="right">5.8%</td>
<td align="right">324,349,157</td>
<td align="right">10.1%</td>
<td align="right">-27.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">202,408,053</td>
<td align="right">2.6%</td>
<td align="right">164,945,340</td>
<td align="right">5.2%</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,421,336</td>
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
<td align="left">FOR_ITER_LIST</td>
<td align="right">82,110,406</td>
<td align="right">5.3%</td>
<td align="right">31,018,798</td>
<td align="right">2.8%</td>
<td align="right">-62.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">81,950,663</td>
<td align="right">5.3%</td>
<td align="right">30,984,850</td>
<td align="right">2.8%</td>
<td align="right">-62.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">49,487,854</td>
<td align="right">3.2%</td>
<td align="right">27,205,261</td>
<td align="right">2.5%</td>
<td align="right">-45.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">55,035,444</td>
<td align="right">3.6%</td>
<td align="right">31,086,863</td>
<td align="right">2.9%</td>
<td align="right">-43.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">367,120,158</td>
<td align="right">23.8%</td>
<td align="right">220,136,181</td>
<td align="right">20.2%</td>
<td align="right">-40.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">268,005,389</td>
<td align="right">17.4%</td>
<td align="right">179,039,792</td>
<td align="right">16.4%</td>
<td align="right">-33.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">90,766,260</td>
<td align="right">5.9%</td>
<td align="right">62,930,722</td>
<td align="right">5.8%</td>
<td align="right">-30.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">92,091,968</td>
<td align="right">6.0%</td>
<td align="right">84,907,121</td>
<td align="right">7.8%</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">93,755,562</td>
<td align="right">6.1%</td>
<td align="right">88,799,457</td>
<td align="right">8.2%</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">82,725,814</td>
<td align="right">5.4%</td>
<td align="right">79,139,537</td>
<td align="right">7.3%</td>
<td align="right">-4.3%</td>
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
<td align="right">78,292,944</td>
<td align="right">1.0%</td>
<td align="right">76,009,244</td>
<td align="right">1.0%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,036,758,809</td>
<td align="right">76.1%</td>
<td align="right">5,887,700,138</td>
<td align="right">75.8%</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,704,692,959</td>
<td align="right">84.5%</td>
<td align="right">6,545,988,911</td>
<td align="right">84.2%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,280,278,891</td>
<td align="right">16.1%</td>
<td align="right">1,266,421,718</td>
<td align="right">16.3%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,284,555,558</td>
<td align="right">16.2%</td>
<td align="right">1,270,698,385</td>
<td align="right">16.3%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">1,898,923,039</td>
<td align="right">23.9%</td>
<td align="right">1,884,576,347</td>
<td align="right">24.2%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">1,898,923,039</td>
<td align="right">23.9%</td>
<td align="right">1,884,576,347</td>
<td align="right">24.2%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">24,610,705</td>
<td align="right">0.3%</td>
<td align="right">24,434,660</td>
<td align="right">0.3%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">460,708,964</td>
<td align="right">5.8%</td>
<td align="right">458,211,514</td>
<td align="right">5.9%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">306,630,798</td>
<td align="right">3.9%</td>
<td align="right">305,803,355</td>
<td align="right">3.9%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">614,367,481</td>
<td align="right">7.7%</td>
<td align="right">613,877,962</td>
<td align="right">7.9%</td>
<td align="right">-0.1%</td>
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
<td align="right">4,609,097</td>
<td align="right"></td>
<td align="right">8,332,480</td>
<td align="right"></td>
<td align="right">80.8%</td>
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
<td align="left">Method cache hits</td>
<td align="right">2,312,358,415</td>
<td align="right"></td>
<td align="right">2,087,754,009</td>
<td align="right"></td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">62,545,393</td>
<td align="right"></td>
<td align="right">65,675,764</td>
<td align="right"></td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">2,042,061,759</td>
<td align="right">1.8%</td>
<td align="right">1,994,264,128</td>
<td align="right">1.8%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">23,568,007,918</td>
<td align="right">23.7%</td>
<td align="right">23,109,664,588</td>
<td align="right">23.4%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">23,129,588,705</td>
<td align="right">20.2%</td>
<td align="right">22,806,921,453</td>
<td align="right">20.1%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">14,213,704,481</td>
<td align="right">70.5%</td>
<td align="right">14,037,683,604</td>
<td align="right">70.4%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">14,213,873,715</td>
<td align="right"></td>
<td align="right">14,037,866,441</td>
<td align="right"></td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">25,836,051,210</td>
<td align="right">26.0%</td>
<td align="right">25,522,963,679</td>
<td align="right">25.9%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">2,913,326,938</td>
<td align="right"></td>
<td align="right">2,879,236,243</td>
<td align="right"></td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">5,509,496,404</td>
<td align="right">5.5%</td>
<td align="right">5,451,682,419</td>
<td align="right">5.5%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">58,737,343</td>
<td align="right"></td>
<td align="right">58,142,475</td>
<td align="right"></td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">32,599,667,619</td>
<td align="right">28.5%</td>
<td align="right">32,336,252,242</td>
<td align="right">28.5%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">5,869,195,484</td>
<td align="right">29.1%</td>
<td align="right">5,830,807,251</td>
<td align="right">29.2%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">5,947,222,212</td>
<td align="right">29.5%</td>
<td align="right">5,908,793,672</td>
<td align="right">29.6%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">6,544,409,097</td>
<td align="right"></td>
<td align="right">6,505,600,081</td>
<td align="right"></td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">190,554,371</td>
<td align="right"></td>
<td align="right">189,767,889</td>
<td align="right"></td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">56,524,378,434</td>
<td align="right">49.5%</td>
<td align="right">56,348,923,661</td>
<td align="right">49.7%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">44,485,463,467</td>
<td align="right">44.8%</td>
<td align="right">44,566,061,342</td>
<td align="right">45.2%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">6,697,462</td>
<td align="right">0.0%</td>
<td align="right">6,691,946</td>
<td align="right">0.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">71,329,266</td>
<td align="right">0.4%</td>
<td align="right">71,294,475</td>
<td align="right">0.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">264,809</td>
<td align="right">0.1%</td>
<td align="right">264,809</td>
<td align="right">0.1%</td>
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
<td align="right">358,153</td>
<td align="right">102,929,375</td>
<td align="right">9,633,910,300</td>
<td align="right">792,287,171</td>
<td align="right">751,320,189</td>
<td align="right">357,213</td>
<td align="right">103,099,954</td>
<td align="right">9,640,483,624</td>
<td align="right">790,974,067</td>
<td align="right">750,873,742</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">15,998</td>
<td align="right">8,734,500</td>
<td align="right">11,444,989,444</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">15,998</td>
<td align="right">8,734,500</td>
<td align="right">11,445,679,780</td>
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
Stats gathered on: 2025-08-03
