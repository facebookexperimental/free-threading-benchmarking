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
<td align="left">STORE_SLICE</td>
<td align="right">112,686,473</td>
<td align="right">1,194,051</td>
<td align="right">-98.9%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">5,874,393,305</td>
<td align="right">172,702,459</td>
<td align="right">-97.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">62,370,662</td>
<td align="right">2,093,761</td>
<td align="right">-96.6%</td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">100,136,760</td>
<td align="right">6,000,000</td>
<td align="right">-94.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">728,165,571</td>
<td align="right">52,540,171</td>
<td align="right">-92.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">2,710,664,982</td>
<td align="right">207,073,416</td>
<td align="right">-92.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,450,739,834</td>
<td align="right">125,440,428</td>
<td align="right">-91.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">2,237,676,640</td>
<td align="right">239,133,255</td>
<td align="right">-89.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,750,738,936</td>
<td align="right">192,589,739</td>
<td align="right">-89.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">569,422,330</td>
<td align="right">62,811,555</td>
<td align="right">-89.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">1,743,969</td>
<td align="right">199,806</td>
<td align="right">-88.5%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">2,122,181,594</td>
<td align="right">266,203,900</td>
<td align="right">-87.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">201,838,634</td>
<td align="right">26,415,985</td>
<td align="right">-86.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,462,745,749</td>
<td align="right">463,044,859</td>
<td align="right">-86.6%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,229,657,880</td>
<td align="right">299,090,238</td>
<td align="right">-86.6%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,389,268,495</td>
<td align="right">192,247,376</td>
<td align="right">-86.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">419,664,129</td>
<td align="right">58,668,771</td>
<td align="right">-86.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,131,444,881</td>
<td align="right">158,202,420</td>
<td align="right">-86.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,592,672,789</td>
<td align="right">236,848,528</td>
<td align="right">-85.1%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">390,243,834</td>
<td align="right">58,481,194</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,222,215,999</td>
<td align="right">193,805,683</td>
<td align="right">-84.1%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">375,900,504</td>
<td align="right">61,883,419</td>
<td align="right">-83.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">522,984,960</td>
<td align="right">89,398,740</td>
<td align="right">-82.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,634,903,822</td>
<td align="right">289,379,341</td>
<td align="right">-82.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">568,786,479</td>
<td align="right">101,177,252</td>
<td align="right">-82.2%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">10,291,479</td>
<td align="right">1,882,799</td>
<td align="right">-81.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">692,868,419</td>
<td align="right">133,552,737</td>
<td align="right">-80.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">2,475,394,425</td>
<td align="right">477,734,103</td>
<td align="right">-80.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">365,345,180</td>
<td align="right">71,740,703</td>
<td align="right">-80.4%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">89,404,343</td>
<td align="right">18,133,296</td>
<td align="right">-79.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">1,271,339,388</td>
<td align="right">267,283,987</td>
<td align="right">-79.0%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">156,807,776</td>
<td align="right">33,184,736</td>
<td align="right">-78.8%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">7,359,761,924</td>
<td align="right">1,621,255,495</td>
<td align="right">-78.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">2,877,472,108</td>
<td align="right">661,876,403</td>
<td align="right">-77.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">446,063,156</td>
<td align="right">107,478,940</td>
<td align="right">-75.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,077,435,642</td>
<td align="right">262,913,798</td>
<td align="right">-75.6%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">649,711,147</td>
<td align="right">158,907,650</td>
<td align="right">-75.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">158,442,558</td>
<td align="right">39,535,961</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">544,314,555</td>
<td align="right">135,853,064</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">268,260,299</td>
<td align="right">67,423,214</td>
<td align="right">-74.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,725,369,273</td>
<td align="right">445,887,613</td>
<td align="right">-74.2%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">131,478,240</td>
<td align="right">34,211,585</td>
<td align="right">-74.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">203,383,274</td>
<td align="right">53,331,162</td>
<td align="right">-73.8%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">227,317,709</td>
<td align="right">59,935,601</td>
<td align="right">-73.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,832,965,245</td>
<td align="right">1,548,344,601</td>
<td align="right">-73.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">1,082,073,094</td>
<td align="right">287,636,674</td>
<td align="right">-73.4%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,511,288,148</td>
<td align="right">677,644,351</td>
<td align="right">-73.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">11,313,505,390</td>
<td align="right">3,134,692,899</td>
<td align="right">-72.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">13,849,830,820</td>
<td align="right">3,948,281,643</td>
<td align="right">-71.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">788,896,530</td>
<td align="right">225,606,663</td>
<td align="right">-71.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,565,546,042</td>
<td align="right">745,220,018</td>
<td align="right">-71.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">11,011,327,304</td>
<td align="right">3,270,384,890</td>
<td align="right">-70.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">453,623,551</td>
<td align="right">134,731,125</td>
<td align="right">-70.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,095,252,786</td>
<td align="right">328,060,049</td>
<td align="right">-70.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">360,195,782</td>
<td align="right">108,731,618</td>
<td align="right">-69.8%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">57,644,872</td>
<td align="right">17,623,943</td>
<td align="right">-69.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">943,867,956</td>
<td align="right">296,221,001</td>
<td align="right">-68.6%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">35,381,638</td>
<td align="right">11,124,221</td>
<td align="right">-68.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">282,882,500</td>
<td align="right">89,623,148</td>
<td align="right">-68.3%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">116,449,490</td>
<td align="right">36,943,224</td>
<td align="right">-68.3%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">592,989,406</td>
<td align="right">206,149,960</td>
<td align="right">-65.2%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">124,939,540</td>
<td align="right">44,159,990</td>
<td align="right">-64.7%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">63,718,512</td>
<td align="right">22,756,955</td>
<td align="right">-64.3%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,167,144,051</td>
<td align="right">419,602,335</td>
<td align="right">-64.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">38,474,411,500</td>
<td align="right">13,899,154,257</td>
<td align="right">-63.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">93,745,955</td>
<td align="right">34,646,273</td>
<td align="right">-63.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">815,182,768</td>
<td align="right">307,843,055</td>
<td align="right">-62.2%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">76,723,033</td>
<td align="right">28,987,973</td>
<td align="right">-62.2%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">127,567,585</td>
<td align="right">48,850,953</td>
<td align="right">-61.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,178,810,240</td>
<td align="right">861,395,906</td>
<td align="right">-60.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">239,241,333</td>
<td align="right">95,460,394</td>
<td align="right">-60.1%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">67,308,816</td>
<td align="right">26,878,463</td>
<td align="right">-60.1%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">531,921,205</td>
<td align="right">212,472,051</td>
<td align="right">-60.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">94,187,226</td>
<td align="right">37,761,608</td>
<td align="right">-59.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">266,519,566</td>
<td align="right">107,314,858</td>
<td align="right">-59.7%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">405,457,500</td>
<td align="right">164,612,637</td>
<td align="right">-59.4%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">808,059,084</td>
<td align="right">330,090,453</td>
<td align="right">-59.2%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,156,327</td>
<td align="right">2,576,867</td>
<td align="right">-58.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">94,297,981</td>
<td align="right">39,647,123</td>
<td align="right">-58.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">79,240,367</td>
<td align="right">33,787,609</td>
<td align="right">-57.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST_IMMORTAL</td>
<td align="right">6,694,967,319</td>
<td align="right">2,877,732,958</td>
<td align="right">-57.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">404,032,389</td>
<td align="right">173,991,226</td>
<td align="right">-56.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">23,515,711</td>
<td align="right">10,319,883</td>
<td align="right">-56.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">5,344,672,203</td>
<td align="right">2,346,540,661</td>
<td align="right">-56.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,389,948,198</td>
<td align="right">615,215,465</td>
<td align="right">-55.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">247,598,036</td>
<td align="right">114,203,514</td>
<td align="right">-53.9%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,420,214,000</td>
<td align="right">670,950,629</td>
<td align="right">-52.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">349,316,296</td>
<td align="right">165,811,532</td>
<td align="right">-52.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,999,237,667</td>
<td align="right">1,920,220,826</td>
<td align="right">-52.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">397,357,208</td>
<td align="right">191,549,671</td>
<td align="right">-51.8%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">13,310,568</td>
<td align="right">6,418,522</td>
<td align="right">-51.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">344,835,093</td>
<td align="right">168,472,755</td>
<td align="right">-51.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,680,898,639</td>
<td align="right">1,313,066,695</td>
<td align="right">-51.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,264,276,541</td>
<td align="right">620,730,474</td>
<td align="right">-50.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">255,614,901</td>
<td align="right">131,336,444</td>
<td align="right">-48.6%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">185,963,196</td>
<td align="right">97,719,169</td>
<td align="right">-47.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">185,869,633</td>
<td align="right">98,424,243</td>
<td align="right">-47.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">3,426,441,483</td>
<td align="right">1,819,085,222</td>
<td align="right">-46.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,751,154,376</td>
<td align="right">942,553,259</td>
<td align="right">-46.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">8,961,388</td>
<td align="right">4,867,069</td>
<td align="right">-45.7%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">15,907,807</td>
<td align="right">8,863,927</td>
<td align="right">-44.3%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">190,778,127</td>
<td align="right">107,429,010</td>
<td align="right">-43.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">298,032,095</td>
<td align="right">168,477,993</td>
<td align="right">-43.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">294,479,638</td>
<td align="right">170,414,578</td>
<td align="right">-42.1%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">117,210,930</td>
<td align="right">68,108,456</td>
<td align="right">-41.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,118,251,396</td>
<td align="right">652,782,099</td>
<td align="right">-41.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">798,209,980</td>
<td align="right">475,799,105</td>
<td align="right">-40.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,620,132,110</td>
<td align="right">3,984,289,638</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">97,967,912</td>
<td align="right">59,106,905</td>
<td align="right">-39.7%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">182,888,761</td>
<td align="right">111,785,427</td>
<td align="right">-38.9%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">858,142,230</td>
<td align="right">548,838,968</td>
<td align="right">-36.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,467,144,917</td>
<td align="right">2,221,883,405</td>
<td align="right">-35.9%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">86,678,353</td>
<td align="right">56,120,659</td>
<td align="right">-35.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">517,655,679</td>
<td align="right">336,178,742</td>
<td align="right">-35.1%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">87,933,024</td>
<td align="right">58,968,865</td>
<td align="right">-32.9%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">96,403,758</td>
<td align="right">64,995,862</td>
<td align="right">-32.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">69,064,144</td>
<td align="right">47,755,236</td>
<td align="right">-30.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">334,256,504</td>
<td align="right">234,006,835</td>
<td align="right">-30.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">530,921,757</td>
<td align="right">378,650,776</td>
<td align="right">-28.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">195,700,699</td>
<td align="right">139,892,665</td>
<td align="right">-28.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">163,270,833</td>
<td align="right">117,885,887</td>
<td align="right">-27.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">553,510,677</td>
<td align="right">401,907,113</td>
<td align="right">-27.4%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,374,119,912</td>
<td align="right">2,461,685,878</td>
<td align="right">-27.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">86,411,943</td>
<td align="right">63,252,396</td>
<td align="right">-26.8%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">17,319,022</td>
<td align="right">13,013,212</td>
<td align="right">-24.9%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">1,686,064</td>
<td align="right">1,321,349</td>
<td align="right">-21.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">104,878,919</td>
<td align="right">82,616,348</td>
<td align="right">-21.2%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">114,322,761</td>
<td align="right">90,291,322</td>
<td align="right">-21.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,008,162,648</td>
<td align="right">817,993,633</td>
<td align="right">-18.9%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">39,048,354</td>
<td align="right">31,772,365</td>
<td align="right">-18.6%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">9,737,782</td>
<td align="right">8,112,522</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">4,390,022</td>
<td align="right">3,659,783</td>
<td align="right">-16.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,546,632,356</td>
<td align="right">4,682,490,110</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">76,243,092</td>
<td align="right">67,421,672</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">344,649,422</td>
<td align="right">314,757,595</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">74,277,221</td>
<td align="right">68,576,277</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">74,905,057</td>
<td align="right">70,040,989</td>
<td align="right">-6.5%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">417,643,969</td>
<td align="right">392,548,665</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,758,056</td>
<td align="right">3,924,003</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">78,441,328</td>
<td align="right">75,154,191</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,147,176,457</td>
<td align="right">1,124,969,504</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">61,737,584</td>
<td align="right">60,668,621</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">172,683,388</td>
<td align="right">170,068,018</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">10,799,063</td>
<td align="right">10,697,092</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">1,834,026,473</td>
<td align="right">1,817,852,263</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">68,031,801</td>
<td align="right">67,554,346</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">157,146,570</td>
<td align="right">156,469,542</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">91,536</td>
<td align="right">91,276</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">76,486</td>
<td align="right">76,584</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">85,876,080</td>
<td align="right">85,952,996</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">100,741,679</td>
<td align="right">100,667,714</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">1,705,643</td>
<td align="right">1,704,859</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">10,176,490</td>
<td align="right">10,172,570</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">639,202</td>
<td align="right">639,046</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">31,338</td>
<td align="right">31,342</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,439,391</td>
<td align="right">128,424,309</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">14,738,174</td>
<td align="right">14,738,878</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">302,086,306</td>
<td align="right">302,078,896</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">20,802,969</td>
<td align="right">20,803,284</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">21,145,515</td>
<td align="right">21,145,830</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">21,145,516</td>
<td align="right">21,145,831</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">4,526,976</td>
<td align="right">4,526,914</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,160,326</td>
<td align="right">6,160,272</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">167,887,374</td>
<td align="right">167,887,857</td>
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
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">8,975,994</td>
<td align="right">8,975,994</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">END_ASYNC_FOR</td>
<td align="right">6,000,000</td>
<td align="right">6,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AITER</td>
<td align="right">6,000,000</td>
<td align="right">6,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">1,198,210</td>
<td align="right">1,198,210</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">781,020</td>
<td align="right">781,020</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">80,787</td>
<td align="right">80,787</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">57,292</td>
<td align="right">57,292</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_GETATTRIBUTE_OVERRIDDEN</td>
<td align="right">52,020</td>
<td align="right">52,020</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">47,747</td>
<td align="right">47,747</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">25,191</td>
<td align="right">25,191</td>
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
<td align="right">3,391</td>
<td align="right">3,391</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">3,359</td>
<td align="right">3,359</td>
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
<td align="right">2,390</td>
<td align="right">2,390</td>
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
<td align="right">26</td>
<td align="right">26</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right"></td>
<td align="right">2,038,034,851</td>
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
<td align="right">7,496,638,005</td>
<td align="right">86.9%</td>
<td align="right">1,191,412,607</td>
<td align="right">77.4%</td>
<td align="right">-84.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,094,054,453</td>
<td align="right">12.7%</td>
<td align="right">327,258,691</td>
<td align="right">21.3%</td>
<td align="right">-70.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">37,672,361</td>
<td align="right">0.4%</td>
<td align="right">20,409,794</td>
<td align="right">1.3%</td>
<td align="right">-45.8%</td>
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
<td align="right">717,573</td>
<td align="right">37.6%</td>
<td align="right">391,884</td>
<td align="right">33.0%</td>
<td align="right">-45.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">1,191,546</td>
<td align="right">62.4%</td>
<td align="right">794,589</td>
<td align="right">67.0%</td>
<td align="right">-33.3%</td>
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
<td align="left">xor</td>
<td align="right">18,866</td>
<td align="right">1.6%</td>
<td align="right">1,326</td>
<td align="right">0.2%</td>
<td align="right">-93.0%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">11,587</td>
<td align="right">1.0%</td>
<td align="right">1,407</td>
<td align="right">0.2%</td>
<td align="right">-87.9%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">23,512</td>
<td align="right">2.0%</td>
<td align="right">3,294</td>
<td align="right">0.4%</td>
<td align="right">-86.0%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">19,478</td>
<td align="right">1.6%</td>
<td align="right">4,902</td>
<td align="right">0.6%</td>
<td align="right">-74.8%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">175,772</td>
<td align="right">14.8%</td>
<td align="right">44,577</td>
<td align="right">5.6%</td>
<td align="right">-74.6%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">34,123</td>
<td align="right">2.9%</td>
<td align="right">9,035</td>
<td align="right">1.1%</td>
<td align="right">-73.5%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">8,202</td>
<td align="right">0.7%</td>
<td align="right">2,342</td>
<td align="right">0.3%</td>
<td align="right">-71.4%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">20,159</td>
<td align="right">1.7%</td>
<td align="right">5,992</td>
<td align="right">0.8%</td>
<td align="right">-70.3%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">43,851</td>
<td align="right">3.7%</td>
<td align="right">13,441</td>
<td align="right">1.7%</td>
<td align="right">-69.3%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">161,674</td>
<td align="right">13.6%</td>
<td align="right">49,965</td>
<td align="right">6.3%</td>
<td align="right">-69.1%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">2,678</td>
<td align="right">0.2%</td>
<td align="right">836</td>
<td align="right">0.1%</td>
<td align="right">-68.8%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">1,273</td>
<td align="right">0.1%</td>
<td align="right">508</td>
<td align="right">0.1%</td>
<td align="right">-60.1%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">8,507</td>
<td align="right">0.7%</td>
<td align="right">4,207</td>
<td align="right">0.5%</td>
<td align="right">-50.5%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">34,124</td>
<td align="right">2.9%</td>
<td align="right">19,834</td>
<td align="right">2.5%</td>
<td align="right">-41.9%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">38,718</td>
<td align="right">3.2%</td>
<td align="right">24,510</td>
<td align="right">3.1%</td>
<td align="right">-36.7%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">6,992</td>
<td align="right">0.6%</td>
<td align="right">6,172</td>
<td align="right">0.8%</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">580,534</td>
<td align="right">48.7%</td>
<td align="right">600,788</td>
<td align="right">75.6%</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">1,406</td>
<td align="right">0.1%</td>
<td align="right">1,363</td>
<td align="right">0.2%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">and different types</td>
<td align="right">90</td>
<td align="right">0.0%</td>
<td align="right">90</td>
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
<td align="right">185,963,196</td>
<td align="right">100.0%</td>
<td align="right">97,719,169</td>
<td align="right">100.0%</td>
<td align="right">-47.5%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR

<details>
<summary> specialization stats for BINARY_SUBSCR family </summary>

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
<td align="right">5,515,901,253</td>
<td align="right">69.0%</td>
<td align="right">1,044,464,656</td>
<td align="right">68.4%</td>
<td align="right">-81.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,474,750,610</td>
<td align="right">30.9%</td>
<td align="right">477,579,068</td>
<td align="right">31.3%</td>
<td align="right">-80.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">5,926,682</td>
<td align="right">0.1%</td>
<td align="right">5,829,886</td>
<td align="right">0.4%</td>
<td align="right">-1.6%</td>
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
<td align="right">636,036</td>
<td align="right">84.2%</td>
<td align="right">147,236</td>
<td align="right">55.6%</td>
<td align="right">-76.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">119,413</td>
<td align="right">15.8%</td>
<td align="right">117,593</td>
<td align="right">44.4%</td>
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
<td align="left">list slice</td>
<td align="right">184,515</td>
<td align="right">29.0%</td>
<td align="right">7,168</td>
<td align="right">4.9%</td>
<td align="right">-96.1%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">28,576</td>
<td align="right">4.5%</td>
<td align="right">3,604</td>
<td align="right">2.4%</td>
<td align="right">-87.4%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">166,356</td>
<td align="right">26.2%</td>
<td align="right">24,073</td>
<td align="right">16.3%</td>
<td align="right">-85.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">189,648</td>
<td align="right">29.8%</td>
<td align="right">57,616</td>
<td align="right">39.1%</td>
<td align="right">-69.6%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">47,209</td>
<td align="right">7.4%</td>
<td align="right">35,267</td>
<td align="right">24.0%</td>
<td align="right">-25.3%</td>
</tr>
<tr>
<td align="left">buffer slice</td>
<td align="right">973</td>
<td align="right">0.2%</td>
<td align="right">753</td>
<td align="right">0.5%</td>
<td align="right">-22.6%</td>
</tr>
<tr>
<td align="left">string slice</td>
<td align="right">3,461</td>
<td align="right">0.5%</td>
<td align="right">3,458</td>
<td align="right">2.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">12,277</td>
<td align="right">1.9%</td>
<td align="right">12,276</td>
<td align="right">8.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">sequence int</td>
<td align="right">2,940</td>
<td align="right">0.5%</td>
<td align="right">2,940</td>
<td align="right">2.0%</td>
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
<td align="left">array slice</td>
<td align="right">21</td>
<td align="right">0.0%</td>
<td align="right">21</td>
<td align="right">0.0%</td>
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
<td align="right">11,238,376,057</td>
<td align="right">97.2%</td>
<td align="right">4,296,474,228</td>
<td align="right">93.4%</td>
<td align="right">-61.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">161,258,587</td>
<td align="right">1.4%</td>
<td align="right">134,916,123</td>
<td align="right">2.9%</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">167,680,615</td>
<td align="right">1.4%</td>
<td align="right">167,680,564</td>
<td align="right">3.6%</td>
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
<td align="right">21,673</td>
<td align="right">0.0%</td>
<td align="right">21,673</td>
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
<td align="right">3,204,039</td>
<td align="right">98.6%</td>
<td align="right">2,707,468</td>
<td align="right">98.4%</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">44,379</td>
<td align="right">1.4%</td>
<td align="right">44,377</td>
<td align="right">1.6%</td>
<td align="right">-0.0%</td>
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
<td align="right">266</td>
<td align="right">0.6%</td>
<td align="right">286</td>
<td align="right">0.6%</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">init not inline values</td>
<td align="right">43,882</td>
<td align="right">98.9%</td>
<td align="right">43,880</td>
<td align="right">98.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">44,525</td>
<td align="right">100.3%</td>
<td align="right">44,523</td>
<td align="right">100.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">init not simple</td>
<td align="right">730</td>
<td align="right">1.6%</td>
<td align="right">730</td>
<td align="right">1.6%</td>
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
<td align="right">67,713</td>
<td align="right">10.9%</td>
<td align="right">67,713</td>
<td align="right">10.9%</td>
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
<td align="right">545,260</td>
<td align="right">87.7%</td>
<td align="right">545,260</td>
<td align="right">87.7%</td>
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
<td align="right">18,878</td>
<td align="right">99.2%</td>
<td align="right">18,976</td>
<td align="right">99.2%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">146</td>
<td align="right">0.8%</td>
<td align="right">146</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
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
<td align="right">522,745,049</td>
<td align="right">10.1%</td>
<td align="right">89,264,830</td>
<td align="right">7.9%</td>
<td align="right">-82.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,664,405,154</td>
<td align="right">89.9%</td>
<td align="right">1,037,178,054</td>
<td align="right">91.9%</td>
<td align="right">-77.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,440,442</td>
<td align="right">0.0%</td>
<td align="right">1,439,542</td>
<td align="right">0.1%</td>
<td align="right">-0.1%</td>
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
<td align="right">218,193</td>
<td align="right">81.7%</td>
<td align="right">112,181</td>
<td align="right">69.7%</td>
<td align="right">-48.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">48,728</td>
<td align="right">18.3%</td>
<td align="right">48,721</td>
<td align="right">30.3%</td>
<td align="right">-0.0%</td>
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
<td align="right">85,018</td>
<td align="right">39.0%</td>
<td align="right">4,151</td>
<td align="right">3.7%</td>
<td align="right">-95.1%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">6,810</td>
<td align="right">3.1%</td>
<td align="right">351</td>
<td align="right">0.3%</td>
<td align="right">-94.8%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">14,814</td>
<td align="right">6.8%</td>
<td align="right">6,719</td>
<td align="right">6.0%</td>
<td align="right">-54.6%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">2,010</td>
<td align="right">0.9%</td>
<td align="right">950</td>
<td align="right">0.8%</td>
<td align="right">-52.7%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">14,461</td>
<td align="right">6.6%</td>
<td align="right">7,842</td>
<td align="right">7.0%</td>
<td align="right">-45.8%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">1,348</td>
<td align="right">0.6%</td>
<td align="right">1,247</td>
<td align="right">1.1%</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">46,228</td>
<td align="right">21.2%</td>
<td align="right">43,912</td>
<td align="right">39.1%</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">971</td>
<td align="right">0.4%</td>
<td align="right">931</td>
<td align="right">0.8%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">7,801</td>
<td align="right">3.6%</td>
<td align="right">7,703</td>
<td align="right">6.9%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">30,715</td>
<td align="right">14.1%</td>
<td align="right">30,358</td>
<td align="right">27.1%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">7,631</td>
<td align="right">3.5%</td>
<td align="right">7,631</td>
<td align="right">6.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">386</td>
<td align="right">0.2%</td>
<td align="right">386</td>
<td align="right">0.3%</td>
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
<td align="right">2,201,836,201</td>
<td align="right">91.4%</td>
<td align="right">324,794,578</td>
<td align="right">85.3%</td>
<td align="right">-85.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">203,310,922</td>
<td align="right">8.4%</td>
<td align="right">53,295,492</td>
<td align="right">14.0%</td>
<td align="right">-73.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,526,286</td>
<td align="right">0.1%</td>
<td align="right">2,526,286</td>
<td align="right">0.7%</td>
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
<td align="right">70,477</td>
<td align="right">58.7%</td>
<td align="right">33,795</td>
<td align="right">40.6%</td>
<td align="right">-52.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">49,545</td>
<td align="right">41.3%</td>
<td align="right">49,545</td>
<td align="right">59.4%</td>
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
<td align="right">23,240</td>
<td align="right">33.0%</td>
<td align="right">5,853</td>
<td align="right">17.3%</td>
<td align="right">-74.8%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">24,231</td>
<td align="right">34.4%</td>
<td align="right">9,221</td>
<td align="right">27.3%</td>
<td align="right">-61.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">11,791</td>
<td align="right">16.7%</td>
<td align="right">7,906</td>
<td align="right">23.4%</td>
<td align="right">-32.9%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">11,215</td>
<td align="right">15.9%</td>
<td align="right">10,815</td>
<td align="right">32.0%</td>
<td align="right">-3.6%</td>
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
<td align="right">1,450,309,991</td>
<td align="right">27.8%</td>
<td align="right">125,342,748</td>
<td align="right">18.8%</td>
<td align="right">-91.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,593,683,062</td>
<td align="right">69.0%</td>
<td align="right">509,502,930</td>
<td align="right">76.4%</td>
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
<td align="right">164,071,740</td>
<td align="right">3.2%</td>
<td align="right">32,227,074</td>
<td align="right">4.8%</td>
<td align="right">-80.4%</td>
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
<td align="right">3,101,140</td>
<td align="right">88.0%</td>
<td align="right">613,583</td>
<td align="right">87.0%</td>
<td align="right">-80.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">424,207</td>
<td align="right">12.0%</td>
<td align="right">92,050</td>
<td align="right">13.0%</td>
<td align="right">-78.3%</td>
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
<td align="right">161,898</td>
<td align="right">38.2%</td>
<td align="right">4,466</td>
<td align="right">4.9%</td>
<td align="right">-97.2%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">84,258</td>
<td align="right">19.9%</td>
<td align="right">3,115</td>
<td align="right">3.4%</td>
<td align="right">-96.3%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">35,072</td>
<td align="right">8.3%</td>
<td align="right">5,767</td>
<td align="right">6.3%</td>
<td align="right">-83.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">12,373</td>
<td align="right">2.9%</td>
<td align="right">2,600</td>
<td align="right">2.8%</td>
<td align="right">-79.0%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">19,434</td>
<td align="right">4.6%</td>
<td align="right">4,177</td>
<td align="right">4.5%</td>
<td align="right">-78.5%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">727</td>
<td align="right">0.2%</td>
<td align="right">167</td>
<td align="right">0.2%</td>
<td align="right">-77.0%</td>
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
<td align="left">reversed list</td>
<td align="right">3,091</td>
<td align="right">0.7%</td>
<td align="right">1,431</td>
<td align="right">1.6%</td>
<td align="right">-53.7%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">3,950</td>
<td align="right">0.9%</td>
<td align="right">1,879</td>
<td align="right">2.0%</td>
<td align="right">-52.4%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">19,349</td>
<td align="right">4.6%</td>
<td align="right">10,597</td>
<td align="right">11.5%</td>
<td align="right">-45.2%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">4,624</td>
<td align="right">1.1%</td>
<td align="right">2,829</td>
<td align="right">3.1%</td>
<td align="right">-38.8%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">71,241</td>
<td align="right">16.8%</td>
<td align="right">49,756</td>
<td align="right">54.1%</td>
<td align="right">-30.2%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">6,879</td>
<td align="right">1.6%</td>
<td align="right">4,815</td>
<td align="right">5.2%</td>
<td align="right">-30.0%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">171</td>
<td align="right">0.0%</td>
<td align="right">131</td>
<td align="right">0.1%</td>
<td align="right">-23.4%</td>
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
<td align="right">13,057,470,044</td>
<td align="right">88.5%</td>
<td align="right">5,578,214,478</td>
<td align="right">83.1%</td>
<td align="right">-57.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">796,647,868</td>
<td align="right">5.4%</td>
<td align="right">474,330,174</td>
<td align="right">7.1%</td>
<td align="right">-40.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">896,434,128</td>
<td align="right">6.1%</td>
<td align="right">661,889,692</td>
<td align="right">9.9%</td>
<td align="right">-26.2%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,858,759</td>
<td align="right">0.0%</td>
<td align="right">1,858,759</td>
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
<td align="right">295,615</td>
<td align="right">1.7%</td>
<td align="right">216,712</td>
<td align="right">1.7%</td>
<td align="right">-26.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">16,991,112</td>
<td align="right">98.3%</td>
<td align="right">12,567,391</td>
<td align="right">98.3%</td>
<td align="right">-26.0%</td>
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
<td align="right">80,781</td>
<td align="right">27.3%</td>
<td align="right">40,887</td>
<td align="right">18.9%</td>
<td align="right">-49.4%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">61,404</td>
<td align="right">20.8%</td>
<td align="right">37,100</td>
<td align="right">17.1%</td>
<td align="right">-39.6%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">1,159</td>
<td align="right">0.4%</td>
<td align="right">835</td>
<td align="right">0.4%</td>
<td align="right">-28.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">5,967</td>
<td align="right">2.0%</td>
<td align="right">4,734</td>
<td align="right">2.2%</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">9,334</td>
<td align="right">3.2%</td>
<td align="right">8,150</td>
<td align="right">3.8%</td>
<td align="right">-12.7%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">17,982</td>
<td align="right">6.1%</td>
<td align="right">15,784</td>
<td align="right">7.3%</td>
<td align="right">-12.2%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">2,726</td>
<td align="right">0.9%</td>
<td align="right">2,402</td>
<td align="right">1.1%</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">69,996</td>
<td align="right">23.7%</td>
<td align="right">62,858</td>
<td align="right">29.0%</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1,752</td>
<td align="right">0.6%</td>
<td align="right">1,604</td>
<td align="right">0.7%</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">25,195</td>
<td align="right">8.5%</td>
<td align="right">23,787</td>
<td align="right">11.0%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">585</td>
<td align="right">0.2%</td>
<td align="right">584</td>
<td align="right">0.3%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">5,745</td>
<td align="right">1.9%</td>
<td align="right">5,745</td>
<td align="right">2.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">1,127</td>
<td align="right">0.4%</td>
<td align="right">1,127</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">1,101</td>
<td align="right">0.4%</td>
<td align="right">1,101</td>
<td align="right">0.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">400</td>
<td align="right">0.1%</td>
<td align="right">400</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">wrong number arguments</td>
<td align="right">180</td>
<td align="right">0.1%</td>
<td align="right">180</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">160</td>
<td align="right">0.1%</td>
<td align="right">160</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property not py function</td>
<td align="right">55</td>
<td align="right">0.0%</td>
<td align="right">55</td>
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
<td align="right">9,300,068,341</td>
<td align="right">99.8%</td>
<td align="right">3,770,186,214</td>
<td align="right">99.6%</td>
<td align="right">-59.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">41,821</td>
<td align="right">0.0%</td>
<td align="right">41,792</td>
<td align="right">0.0%</td>
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
<td align="right">14,612,480</td>
<td align="right">0.2%</td>
<td align="right">14,612,476</td>
<td align="right">0.4%</td>
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
<td align="right">1,483</td>
<td align="right">0.0%</td>
<td align="right">1,483</td>
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
<td align="right">126,436</td>
<td align="right">100.0%</td>
<td align="right">127,144</td>
<td align="right">100.0%</td>
<td align="right">0.6%</td>
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
<td align="right">66,264,560</td>
<td align="right">100.0%</td>
<td align="right">65,195,535</td>
<td align="right">100.0%</td>
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
<td align="right">122</td>
<td align="right">0.0%</td>
<td align="right">122</td>
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
<td align="right">2,268</td>
<td align="right">100.0%</td>
<td align="right">2,268</td>
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
<td align="right">592,974,695</td>
<td align="right">82.2%</td>
<td align="right">206,135,249</td>
<td align="right">61.6%</td>
<td align="right">-65.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">128,405,102</td>
<td align="right">17.8%</td>
<td align="right">128,390,022</td>
<td align="right">38.4%</td>
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
<td align="right">608</td>
<td align="right">1.8%</td>
<td align="right">608</td>
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
<td align="right">2,015,454,197</td>
<td align="right">91.1%</td>
<td align="right">1,360,555,923</td>
<td align="right">87.9%</td>
<td align="right">-32.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">76,149,087</td>
<td align="right">3.4%</td>
<td align="right">67,329,534</td>
<td align="right">4.4%</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">119,935,841</td>
<td align="right">5.4%</td>
<td align="right">119,195,803</td>
<td align="right">7.7%</td>
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
<td align="right">54,260</td>
<td align="right">1.3%</td>
<td align="right">52,051</td>
<td align="right">1.2%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">4,135,269</td>
<td align="right">98.7%</td>
<td align="right">4,121,921</td>
<td align="right">98.8%</td>
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
<td align="left">overriding descriptor</td>
<td align="right">6,352</td>
<td align="right">11.7%</td>
<td align="right">4,989</td>
<td align="right">9.6%</td>
<td align="right">-21.5%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">5,364</td>
<td align="right">9.9%</td>
<td align="right">5,144</td>
<td align="right">9.9%</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">25,869</td>
<td align="right">47.7%</td>
<td align="right">25,268</td>
<td align="right">48.5%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">2,996</td>
<td align="right">5.5%</td>
<td align="right">2,975</td>
<td align="right">5.7%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">787</td>
<td align="right">1.5%</td>
<td align="right">785</td>
<td align="right">1.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">1,710</td>
<td align="right">3.2%</td>
<td align="right">1,708</td>
<td align="right">3.3%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">7,735</td>
<td align="right">14.3%</td>
<td align="right">7,735</td>
<td align="right">14.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">1,614</td>
<td align="right">3.0%</td>
<td align="right">1,614</td>
<td align="right">3.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">876</td>
<td align="right">1.6%</td>
<td align="right">876</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">762</td>
<td align="right">1.4%</td>
<td align="right">762</td>
<td align="right">1.5%</td>
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
<td align="right">112,686,473</td>
<td align="right">100.0%</td>
<td align="right">1,194,051</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">929,615,892</td>
<td align="right">57.3%</td>
<td align="right">171,540,953</td>
<td align="right">56.2%</td>
<td align="right">-81.5%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">692,685,167</td>
<td align="right">42.7%</td>
<td align="right">133,506,039</td>
<td align="right">43.8%</td>
<td align="right">-80.7%</td>
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
<td align="right">180,274</td>
<td align="right">98.4%</td>
<td align="right">43,718</td>
<td align="right">93.5%</td>
<td align="right">-75.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,018</td>
<td align="right">1.6%</td>
<td align="right">3,020</td>
<td align="right">6.5%</td>
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
<td align="left">other</td>
<td align="right">81,221</td>
<td align="right">45.1%</td>
<td align="right">320</td>
<td align="right">0.7%</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">5,256</td>
<td align="right">2.9%</td>
<td align="right">213</td>
<td align="right">0.5%</td>
<td align="right">-95.9%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">52,368</td>
<td align="right">29.0%</td>
<td align="right">8,143</td>
<td align="right">18.6%</td>
<td align="right">-84.5%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">1,672</td>
<td align="right">0.9%</td>
<td align="right">492</td>
<td align="right">1.1%</td>
<td align="right">-70.6%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">19,337</td>
<td align="right">10.7%</td>
<td align="right">14,750</td>
<td align="right">33.7%</td>
<td align="right">-23.7%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">17,333</td>
<td align="right">9.6%</td>
<td align="right">16,713</td>
<td align="right">38.2%</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">3,019</td>
<td align="right">1.7%</td>
<td align="right">3,019</td>
<td align="right">6.9%</td>
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
<td align="right">116,751,032</td>
<td align="right">2.2%</td>
<td align="right">43,008,254</td>
<td align="right">1.7%</td>
<td align="right">-63.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">265,841,661</td>
<td align="right">5.0%</td>
<td align="right">106,865,014</td>
<td align="right">4.2%</td>
<td align="right">-59.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,908,362,014</td>
<td align="right">92.8%</td>
<td align="right">2,374,291,168</td>
<td align="right">94.0%</td>
<td align="right">-51.6%</td>
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
<td align="right">2,251,032</td>
<td align="right">78.2%</td>
<td align="right">859,757</td>
<td align="right">68.2%</td>
<td align="right">-61.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">628,476</td>
<td align="right">21.8%</td>
<td align="right">400,318</td>
<td align="right">31.8%</td>
<td align="right">-36.3%</td>
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
<td align="right">131,354</td>
<td align="right">20.9%</td>
<td align="right">9,179</td>
<td align="right">2.3%</td>
<td align="right">-93.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">16,061</td>
<td align="right">2.6%</td>
<td align="right">1,681</td>
<td align="right">0.4%</td>
<td align="right">-89.5%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">77,197</td>
<td align="right">12.3%</td>
<td align="right">8,383</td>
<td align="right">2.1%</td>
<td align="right">-89.1%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">10,037</td>
<td align="right">1.6%</td>
<td align="right">6,313</td>
<td align="right">1.6%</td>
<td align="right">-37.1%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">19,122</td>
<td align="right">3.0%</td>
<td align="right">12,764</td>
<td align="right">3.2%</td>
<td align="right">-33.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">97,412</td>
<td align="right">15.5%</td>
<td align="right">86,823</td>
<td align="right">21.7%</td>
<td align="right">-10.9%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">12,890</td>
<td align="right">2.1%</td>
<td align="right">11,918</td>
<td align="right">3.0%</td>
<td align="right">-7.5%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">263,981</td>
<td align="right">42.0%</td>
<td align="right">262,835</td>
<td align="right">65.7%</td>
<td align="right">-0.4%</td>
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
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">40</td>
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
<td align="right">1,255,295,881</td>
<td align="right">99.9%</td>
<td align="right">401,687,950</td>
<td align="right">99.7%</td>
<td align="right">-68.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,673,780</td>
<td align="right">0.1%</td>
<td align="right">1,309,133</td>
<td align="right">0.3%</td>
<td align="right">-21.8%</td>
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
<td align="right">964</td>
<td align="right">7.8%</td>
<td align="right">836</td>
<td align="right">6.8%</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">11,400</td>
<td align="right">92.2%</td>
<td align="right">11,460</td>
<td align="right">93.2%</td>
<td align="right">0.5%</td>
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
<td align="right">741</td>
<td align="right">76.9%</td>
<td align="right">613</td>
<td align="right">73.3%</td>
<td align="right">-17.3%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">132</td>
<td align="right">13.7%</td>
<td align="right">132</td>
<td align="right">15.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">91</td>
<td align="right">9.4%</td>
<td align="right">91</td>
<td align="right">10.9%</td>
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
<td align="right">8,193,075,884</td>
<td align="right">3.8%</td>
<td align="right">2,269,417,441</td>
<td align="right">2.8%</td>
<td align="right">-72.3%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">81,484,666,472</td>
<td align="right">37.9%</td>
<td align="right">29,858,439,336</td>
<td align="right">37.1%</td>
<td align="right">-63.4%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">123,954,571,396</td>
<td align="right">57.6%</td>
<td align="right">47,268,027,559</td>
<td align="right">58.8%</td>
<td align="right">-61.9%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,506,756,602</td>
<td align="right">0.7%</td>
<td align="right">1,022,212,683</td>
<td align="right">1.3%</td>
<td align="right">-32.2%</td>
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
<td align="right">1,450,309,991</td>
<td align="right">17.7%</td>
<td align="right">125,342,748</td>
<td align="right">5.5%</td>
<td align="right">-91.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">522,745,049</td>
<td align="right">6.4%</td>
<td align="right">89,264,830</td>
<td align="right">3.9%</td>
<td align="right">-82.9%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">692,685,167</td>
<td align="right">8.5%</td>
<td align="right">133,506,039</td>
<td align="right">5.9%</td>
<td align="right">-80.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">2,474,750,610</td>
<td align="right">30.2%</td>
<td align="right">477,579,068</td>
<td align="right">21.1%</td>
<td align="right">-80.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,094,054,453</td>
<td align="right">13.4%</td>
<td align="right">327,258,691</td>
<td align="right">14.4%</td>
<td align="right">-70.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">265,841,661</td>
<td align="right">3.2%</td>
<td align="right">106,865,014</td>
<td align="right">4.7%</td>
<td align="right">-59.8%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">185,963,196</td>
<td align="right">2.3%</td>
<td align="right">97,719,169</td>
<td align="right">4.3%</td>
<td align="right">-47.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">796,647,868</td>
<td align="right">9.7%</td>
<td align="right">474,330,174</td>
<td align="right">20.9%</td>
<td align="right">-40.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">167,680,615</td>
<td align="right">2.0%</td>
<td align="right">167,680,564</td>
<td align="right">7.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">203,310,922</td>
<td align="right">2.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">128,390,022</td>
<td align="right">5.7%</td>
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
<td align="left">TO_BOOL_NONE</td>
<td align="right">57,260,515</td>
<td align="right">3.8%</td>
<td align="right">19,942,103</td>
<td align="right">2.0%</td>
<td align="right">-65.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">270,844,362</td>
<td align="right">18.0%</td>
<td align="right">183,858,161</td>
<td align="right">18.0%</td>
<td align="right">-32.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">390,655,652</td>
<td align="right">25.9%</td>
<td align="right">274,349,501</td>
<td align="right">26.8%</td>
<td align="right">-29.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">92,991,821</td>
<td align="right">6.2%</td>
<td align="right">77,714,709</td>
<td align="right">7.6%</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">85,770,358</td>
<td align="right">5.7%</td>
<td align="right">73,034,716</td>
<td align="right">7.1%</td>
<td align="right">-14.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">85,070,707</td>
<td align="right">5.6%</td>
<td align="right">73,877,156</td>
<td align="right">7.2%</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">95,104,319</td>
<td align="right">6.3%</td>
<td align="right">95,098,034</td>
<td align="right">9.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">82,053,817</td>
<td align="right">5.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">81,889,949</td>
<td align="right">5.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">51,474,194</td>
<td align="right">3.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">24,062,257</td>
<td align="right">2.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">21,247,293</td>
<td align="right">2.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">20,872,248</td>
<td align="right">2.0%</td>
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
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">4,273,304</td>
<td align="right">0.1%</td>
<td align="right">3,558,239</td>
<td align="right">0.1%</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">141,112,048</td>
<td align="right">2.0%</td>
<td align="right">132,513,115</td>
<td align="right">1.9%</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">73,562,220</td>
<td align="right">1.0%</td>
<td align="right">71,881,410</td>
<td align="right">1.0%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">5,228,591,426</td>
<td align="right">74.0%</td>
<td align="right">5,156,731,389</td>
<td align="right">73.9%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">5,603,626,606</td>
<td align="right">79.3%</td>
<td align="right">5,537,958,337</td>
<td align="right">79.3%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,129,714,207</td>
<td align="right">16.0%</td>
<td align="right">1,118,827,397</td>
<td align="right">16.0%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,125,437,512</td>
<td align="right">15.9%</td>
<td align="right">1,115,265,767</td>
<td align="right">16.0%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">1,838,502,211</td>
<td align="right">26.0%</td>
<td align="right">1,822,493,942</td>
<td align="right">26.1%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">1,838,502,211</td>
<td align="right">26.0%</td>
<td align="right">1,822,493,942</td>
<td align="right">26.1%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">708,788,004</td>
<td align="right">10.0%</td>
<td align="right">703,666,545</td>
<td align="right">10.1%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">276,250,032</td>
<td align="right">3.9%</td>
<td align="right">276,175,096</td>
<td align="right">4.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">24,960,566</td>
<td align="right">0.4%</td>
<td align="right">24,959,423</td>
<td align="right">0.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">262,334,414</td>
<td align="right">3.7%</td>
<td align="right">262,333,396</td>
<td align="right">3.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">3,391</td>
<td align="right">0.0%</td>
<td align="right">3,391</td>
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
<td align="right">12,409,834</td>
<td align="right"></td>
<td align="right">9,459,531</td>
<td align="right"></td>
<td align="right">-23.8%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">87,023,385</td>
<td align="right"></td>
<td align="right">73,607,617</td>
<td align="right"></td>
<td align="right">-15.4%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">75,417,162</td>
<td align="right"></td>
<td align="right">64,956,072</td>
<td align="right"></td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">4,978,085</td>
<td align="right">2.6%</td>
<td align="right">4,312,485</td>
<td align="right">2.2%</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">28,187,806,259</td>
<td align="right">17.6%</td>
<td align="right">26,135,883,680</td>
<td align="right">16.0%</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">82,252,715,027</td>
<td align="right">51.2%</td>
<td align="right">87,983,983,110</td>
<td align="right">53.9%</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">2,302,104,662</td>
<td align="right"></td>
<td align="right">2,164,563,041</td>
<td align="right"></td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">91,720,023,622</td>
<td align="right">46.7%</td>
<td align="right">96,878,471,444</td>
<td align="right">47.8%</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">46,146,641,695</td>
<td align="right">23.5%</td>
<td align="right">47,787,039,854</td>
<td align="right">23.6%</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">10,923,613,741</td>
<td align="right">58.3%</td>
<td align="right">10,634,297,902</td>
<td align="right">57.8%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">10,923,807,163</td>
<td align="right"></td>
<td align="right">10,634,501,792</td>
<td align="right"></td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">25,927,453,841</td>
<td align="right">16.2%</td>
<td align="right">25,487,227,689</td>
<td align="right">15.6%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">24,125,998,463</td>
<td align="right">15.0%</td>
<td align="right">23,777,794,129</td>
<td align="right">14.6%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">24,525,691,347</td>
<td align="right">12.5%</td>
<td align="right">24,233,716,171</td>
<td align="right">12.0%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">7,723,208,674</td>
<td align="right">41.2%</td>
<td align="right">7,671,451,025</td>
<td align="right">41.7%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">7,801,602,718</td>
<td align="right">41.7%</td>
<td align="right">7,749,879,499</td>
<td align="right">42.2%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">8,378,551,012</td>
<td align="right"></td>
<td align="right">8,324,209,855</td>
<td align="right"></td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">33,843,981,172</td>
<td align="right">17.2%</td>
<td align="right">33,647,315,159</td>
<td align="right">16.6%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">3,032,868,544</td>
<td align="right"></td>
<td align="right">3,020,253,227</td>
<td align="right"></td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">195,007,395</td>
<td align="right"></td>
<td align="right">194,326,799</td>
<td align="right"></td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">6,711,953</td>
<td align="right">0.0%</td>
<td align="right">6,706,511</td>
<td align="right">0.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">71,682,091</td>
<td align="right">0.4%</td>
<td align="right">71,721,963</td>
<td align="right">0.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">410,620</td>
<td align="right">0.2%</td>
<td align="right">410,620</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">4,406</td>
<td align="right">0.0%</td>
<td align="right">4,406</td>
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
<td align="right">359,243</td>
<td align="right">107,366,977</td>
<td align="right">9,609,465,009</td>
<td align="right">795,142,215</td>
<td align="right">756,450,605</td>
<td align="right">358,112</td>
<td align="right">107,772,981</td>
<td align="right">9,634,036,096</td>
<td align="right">803,106,489</td>
<td align="right">755,164,077</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">15,998</td>
<td align="right">8,734,432</td>
<td align="right">11,205,783,268</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">15,998</td>
<td align="right">8,734,432</td>
<td align="right">11,206,940,330</td>
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
<td align="right">23</td>
<td align="right">23</td>
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
<td align="right">30</td>
<td align="right">30</td>
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
<td align="right">160</td>
<td align="right">160 / 0 !!</td>
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
<td align="right">160</td>
<td align="right">160 / 0 !!</td>
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
<td align="right">2,474</td>
<td align="right">2,474</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-12-15
