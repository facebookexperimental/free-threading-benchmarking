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
<td align="right">18,902,153</td>
<td align="right">2,678,662</td>
<td align="right">-85.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">8,933,478</td>
<td align="right">1,550,734</td>
<td align="right">-82.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">28,035,189</td>
<td align="right">50,068,468</td>
<td align="right">78.6%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">7,952,691</td>
<td align="right">1,955,766</td>
<td align="right">-75.4%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">8,116,429</td>
<td align="right">2,119,500</td>
<td align="right">-73.9%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">57,955,890</td>
<td align="right">15,371,273</td>
<td align="right">-73.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">9,827,206</td>
<td align="right">2,763,793</td>
<td align="right">-71.9%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">9,601,955</td>
<td align="right">3,282,462</td>
<td align="right">-65.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">34,336,595</td>
<td align="right">12,109,978</td>
<td align="right">-64.7%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">9,690,970</td>
<td align="right">3,613,100</td>
<td align="right">-62.7%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">11,084,733</td>
<td align="right">4,633,120</td>
<td align="right">-58.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">11,512,843</td>
<td align="right">5,140,636</td>
<td align="right">-55.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">22,402,720</td>
<td align="right">10,411,907</td>
<td align="right">-53.5%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">18,162,644</td>
<td align="right">8,906,938</td>
<td align="right">-51.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">55,588,694</td>
<td align="right">29,473,812</td>
<td align="right">-47.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">59,566,981</td>
<td align="right">32,353,991</td>
<td align="right">-45.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">23,282,485</td>
<td align="right">12,980,417</td>
<td align="right">-44.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">9,609,901</td>
<td align="right">5,437,536</td>
<td align="right">-43.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">57,098,754</td>
<td align="right">32,769,867</td>
<td align="right">-42.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">53,237,706</td>
<td align="right">30,685,720</td>
<td align="right">-42.4%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">2,995,264</td>
<td align="right">1,807,539</td>
<td align="right">-39.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">18,636,766</td>
<td align="right">11,339,256</td>
<td align="right">-39.2%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">39,402,948</td>
<td align="right">24,383,538</td>
<td align="right">-38.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">2,008,645</td>
<td align="right">1,267,878</td>
<td align="right">-36.9%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">2,585,174</td>
<td align="right">1,680,330</td>
<td align="right">-35.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">6,786,578</td>
<td align="right">4,535,730</td>
<td align="right">-33.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">21,000,749</td>
<td align="right">14,157,794</td>
<td align="right">-32.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">1,555,520</td>
<td align="right">1,063,806</td>
<td align="right">-31.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">15,917,569</td>
<td align="right">11,157,975</td>
<td align="right">-29.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">46,188,051</td>
<td align="right">32,711,669</td>
<td align="right">-29.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">6,744,514</td>
<td align="right">4,828,162</td>
<td align="right">-28.4%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">24,772,185</td>
<td align="right">18,029,258</td>
<td align="right">-27.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">51,614,294</td>
<td align="right">37,750,840</td>
<td align="right">-26.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">38,911,353</td>
<td align="right">28,574,958</td>
<td align="right">-26.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">32,214,411</td>
<td align="right">23,720,408</td>
<td align="right">-26.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">4,001,687</td>
<td align="right">2,979,919</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">178,583,844</td>
<td align="right">134,313,601</td>
<td align="right">-24.8%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">49,127,585</td>
<td align="right">37,610,609</td>
<td align="right">-23.4%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">43,219,887</td>
<td align="right">33,099,137</td>
<td align="right">-23.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">45,173,576</td>
<td align="right">35,250,735</td>
<td align="right">-22.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">67,364,539</td>
<td align="right">52,722,792</td>
<td align="right">-21.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">17,500,691</td>
<td align="right">13,712,361</td>
<td align="right">-21.6%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">389,914</td>
<td align="right">308,845</td>
<td align="right">-20.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">45,124,640</td>
<td align="right">36,023,553</td>
<td align="right">-20.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">220,728,562</td>
<td align="right">176,713,168</td>
<td align="right">-19.9%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">18,031,081</td>
<td align="right">14,525,182</td>
<td align="right">-19.4%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">44,921,965</td>
<td align="right">36,946,782</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">4,497,730</td>
<td align="right">3,708,553</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">654,912,325</td>
<td align="right">540,495,889</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">144,425,426</td>
<td align="right">119,384,816</td>
<td align="right">-17.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">199,188,262</td>
<td align="right">164,657,334</td>
<td align="right">-17.3%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">15,116,920</td>
<td align="right">12,540,793</td>
<td align="right">-17.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">1,244,533</td>
<td align="right">1,043,849</td>
<td align="right">-16.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">239,568,263</td>
<td align="right">201,489,672</td>
<td align="right">-15.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">30,605,680</td>
<td align="right">25,749,104</td>
<td align="right">-15.9%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">598,532</td>
<td align="right">508,774</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">341,720</td>
<td align="right">291,383</td>
<td align="right">-14.7%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">21,800,786</td>
<td align="right">18,597,654</td>
<td align="right">-14.7%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">41,637,554</td>
<td align="right">35,630,848</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">5,459,938</td>
<td align="right">4,686,788</td>
<td align="right">-14.2%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">48,276,512</td>
<td align="right">41,946,112</td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">12,456,661</td>
<td align="right">10,830,216</td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">388,827</td>
<td align="right">338,490</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">5,753,295</td>
<td align="right">5,012,457</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">60,054,868</td>
<td align="right">52,929,275</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">148,237,355</td>
<td align="right">130,850,640</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">58,118,930</td>
<td align="right">51,366,630</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">173,298,477</td>
<td align="right">153,767,861</td>
<td align="right">-11.3%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">6,589,917</td>
<td align="right">5,849,060</td>
<td align="right">-11.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">17,788,399</td>
<td align="right">15,841,267</td>
<td align="right">-10.9%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">746,331</td>
<td align="right">665,262</td>
<td align="right">-10.9%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">11,271,390</td>
<td align="right">10,055,634</td>
<td align="right">-10.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">33,139,137</td>
<td align="right">29,744,910</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">15,261,243</td>
<td align="right">13,700,006</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">13,387,401</td>
<td align="right">12,091,618</td>
<td align="right">-9.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">21,700,799</td>
<td align="right">19,660,279</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">86,334,991</td>
<td align="right">78,373,531</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">1,222,428</td>
<td align="right">1,121,333</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">182,023,114</td>
<td align="right">167,764,650</td>
<td align="right">-7.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">13,941,596</td>
<td align="right">15,011,503</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">2,588,520</td>
<td align="right">2,410,669</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">36,943,181</td>
<td align="right">34,457,256</td>
<td align="right">-6.7%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">21,991,849</td>
<td align="right">20,597,716</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,758,660</td>
<td align="right">1,651,952</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">32,104,290</td>
<td align="right">30,189,085</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">75,316,340</td>
<td align="right">71,814,232</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">17,506,310</td>
<td align="right">16,710,249</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">24,806,459</td>
<td align="right">23,918,406</td>
<td align="right">-3.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">6,813,052</td>
<td align="right">6,573,085</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">655,343</td>
<td align="right">637,937</td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">11,032,870</td>
<td align="right">11,290,337</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">2,281,590</td>
<td align="right">2,231,351</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">15,579,117</td>
<td align="right">15,247,594</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">942,641</td>
<td align="right">924,855</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">15,882,832</td>
<td align="right">15,592,311</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">1,029,120</td>
<td align="right">1,011,346</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,030,011</td>
<td align="right">1,012,237</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">61</td>
<td align="right">60</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">4,583,123</td>
<td align="right">4,513,704</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,287,811</td>
<td align="right">1,269,855</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">9,777,866</td>
<td align="right">9,902,588</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">6,026,358</td>
<td align="right">5,976,478</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">2,985</td>
<td align="right">2,961</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">7,541,565</td>
<td align="right">7,488,102</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">18,173</td>
<td align="right">18,066</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">4,181,682</td>
<td align="right">4,163,897</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">1,451</td>
<td align="right">1,445</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">23,877</td>
<td align="right">23,799</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">456,558</td>
<td align="right">455,093</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,003</td>
<td align="right">1,000</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">78,738,389</td>
<td align="right">78,518,487</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">1,585,744</td>
<td align="right">1,581,746</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">41,209</td>
<td align="right">41,260</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">3,725,291</td>
<td align="right">3,729,429</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">7,108</td>
<td align="right">7,113</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">10,399</td>
<td align="right">10,392</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">172,090</td>
<td align="right">171,990</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">9,062</td>
<td align="right">9,058</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">10,872,211</td>
<td align="right">10,868,047</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">20,690</td>
<td align="right">20,684</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">175,349</td>
<td align="right">175,379</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">165,591</td>
<td align="right">165,565</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">83,131</td>
<td align="right">83,143</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">495,105</td>
<td align="right">495,036</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">744,786</td>
<td align="right">744,833</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">1,389,751</td>
<td align="right">1,389,804</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">79,549</td>
<td align="right">79,552</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">745,993</td>
<td align="right">746,021</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">654,515</td>
<td align="right">654,537</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">654,533</td>
<td align="right">654,553</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">2,418,375</td>
<td align="right">2,418,310</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">6,622,750</td>
<td align="right">6,622,911</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">2,174,486</td>
<td align="right">2,174,434</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">141,400</td>
<td align="right">141,403</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">427,556</td>
<td align="right">427,547</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">2,618,065</td>
<td align="right">2,618,015</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">1,754,519</td>
<td align="right">1,754,490</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">2,007,825</td>
<td align="right">2,007,794</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">655,343</td>
<td align="right">655,350</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">655,343</td>
<td align="right">655,350</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">4,466,374</td>
<td align="right">4,466,327</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">21,977,499</td>
<td align="right">21,977,730</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">1,323,316</td>
<td align="right">1,323,328</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">10,927,374</td>
<td align="right">10,927,323</td>
<td align="right">-0.0%</td>
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
<td align="right">252,747</td>
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
<td align="right">45,132,172</td>
<td align="right">38.8%</td>
<td align="right">35,210,041</td>
<td align="right">33.1%</td>
<td align="right">-22.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">358,625</td>
<td align="right">0.3%</td>
<td align="right">347,551</td>
<td align="right">0.3%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">70,888,513</td>
<td align="right">60.9%</td>
<td align="right">70,742,523</td>
<td align="right">66.5%</td>
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
<td align="right">42</td>
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
<td align="right">8,907</td>
<td align="right">18.5%</td>
<td align="right">8,690</td>
<td align="right">18.4%</td>
<td align="right">-2.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">39,229</td>
<td align="right">81.5%</td>
<td align="right">38,550</td>
<td align="right">81.6%</td>
<td align="right">-1.7%</td>
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
<td align="right">6,683</td>
<td align="right">17.0%</td>
<td align="right">5,859</td>
<td align="right">15.2%</td>
<td align="right">-12.3%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">4,650</td>
<td align="right">11.9%</td>
<td align="right">4,986</td>
<td align="right">12.9%</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">2,225</td>
<td align="right">5.7%</td>
<td align="right">2,096</td>
<td align="right">5.4%</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">579</td>
<td align="right">1.5%</td>
<td align="right">567</td>
<td align="right">1.5%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">1,013</td>
<td align="right">2.6%</td>
<td align="right">1,031</td>
<td align="right">2.7%</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">626</td>
<td align="right">1.6%</td>
<td align="right">619</td>
<td align="right">1.6%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">367</td>
<td align="right">0.9%</td>
<td align="right">363</td>
<td align="right">0.9%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">92</td>
<td align="right">0.2%</td>
<td align="right">91</td>
<td align="right">0.2%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">2,142</td>
<td align="right">5.5%</td>
<td align="right">2,165</td>
<td align="right">5.6%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">214</td>
<td align="right">0.5%</td>
<td align="right">212</td>
<td align="right">0.5%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">708</td>
<td align="right">1.8%</td>
<td align="right">702</td>
<td align="right">1.8%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">7,181</td>
<td align="right">18.3%</td>
<td align="right">7,129</td>
<td align="right">18.5%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">3,898</td>
<td align="right">9.9%</td>
<td align="right">3,873</td>
<td align="right">10.0%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">989</td>
<td align="right">2.5%</td>
<td align="right">985</td>
<td align="right">2.6%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">1,763</td>
<td align="right">4.5%</td>
<td align="right">1,769</td>
<td align="right">4.6%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">1,212</td>
<td align="right">3.1%</td>
<td align="right">1,215</td>
<td align="right">3.2%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">1,086</td>
<td align="right">2.8%</td>
<td align="right">1,088</td>
<td align="right">2.8%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">3,222</td>
<td align="right">8.2%</td>
<td align="right">3,222</td>
<td align="right">8.4%</td>
<td align="right">0.0%</td>
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
<td align="left">true divide other</td>
<td align="right">155</td>
<td align="right">0.4%</td>
<td align="right">155</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
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
<td align="right">35,652,766</td>
<td align="right">11.4%</td>
<td align="right">35,504,521</td>
<td align="right">11.4%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">36,329,644</td>
<td align="right">11.6%</td>
<td align="right">36,181,162</td>
<td align="right">11.6%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">276,649,199</td>
<td align="right">88.4%</td>
<td align="right">276,378,906</td>
<td align="right">88.4%</td>
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
<td align="right"></td>
<td align="right"></td>
<td align="right">5,271</td>
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
<td align="right">700,755</td>
<td align="right">100.0%</td>
<td align="right">700,440</td>
<td align="right">100.0%</td>
<td align="right">-0.0%</td>
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
<td align="right">3,185</td>
<td align="right">74.8%</td>
<td align="right">3,183</td>
<td align="right">74.9%</td>
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
<td align="right">2,805</td>
<td align="right">65.9%</td>
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
<td align="right">1,071</td>
<td align="right">100.0%</td>
<td align="right">1,067</td>
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
<td align="right">30,567,498</td>
<td align="right">37.2%</td>
<td align="right">25,710,708</td>
<td align="right">33.3%</td>
<td align="right">-15.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">402,474</td>
<td align="right">0.5%</td>
<td align="right">403,550</td>
<td align="right">0.5%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">51,096,525</td>
<td align="right">62.2%</td>
<td align="right">51,095,481</td>
<td align="right">66.1%</td>
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
<td align="right">37,015</td>
<td align="right">81.0%</td>
<td align="right">37,232</td>
<td align="right">81.0%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">8,704</td>
<td align="right">19.0%</td>
<td align="right">8,721</td>
<td align="right">19.0%</td>
<td align="right">0.2%</td>
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
<td align="right">1,499</td>
<td align="right">4.0%</td>
<td align="right">1,062</td>
<td align="right">2.9%</td>
<td align="right">-29.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">6,474</td>
<td align="right">17.5%</td>
<td align="right">7,113</td>
<td align="right">19.1%</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">4,285</td>
<td align="right">11.6%</td>
<td align="right">4,271</td>
<td align="right">11.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">13,966</td>
<td align="right">37.7%</td>
<td align="right">14,001</td>
<td align="right">37.6%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">3,157</td>
<td align="right">8.5%</td>
<td align="right">3,151</td>
<td align="right">8.5%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">7,108</td>
<td align="right">19.2%</td>
<td align="right">7,108</td>
<td align="right">19.1%</td>
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
<td align="left">set</td>
<td align="right">137</td>
<td align="right">0.4%</td>
<td align="right">137</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">116</td>
<td align="right">0.3%</td>
<td align="right">116</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">91</td>
<td align="right">0.2%</td>
<td align="right">91</td>
<td align="right">0.2%</td>
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
<td align="right">11,079,151</td>
<td align="right">32.0%</td>
<td align="right">4,627,983</td>
<td align="right">16.4%</td>
<td align="right">-58.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">23,500,524</td>
<td align="right">67.9%</td>
<td align="right">23,501,193</td>
<td align="right">83.5%</td>
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
<td align="right">5,457</td>
<td align="right">97.8%</td>
<td align="right">5,012</td>
<td align="right">97.6%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">125</td>
<td align="right">2.2%</td>
<td align="right">125</td>
<td align="right">2.4%</td>
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
<td align="right">3,503</td>
<td align="right">64.2%</td>
<td align="right">3,056</td>
<td align="right">61.0%</td>
<td align="right">-12.8%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">1,473</td>
<td align="right">27.0%</td>
<td align="right">1,475</td>
<td align="right">29.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">299</td>
<td align="right">5.5%</td>
<td align="right">299</td>
<td align="right">6.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">182</td>
<td align="right">3.3%</td>
<td align="right">182</td>
<td align="right">3.6%</td>
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
<td align="right">1,226,244</td>
<td align="right">1.1%</td>
<td align="right">492,216</td>
<td align="right">0.6%</td>
<td align="right">-59.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">46,136,806</td>
<td align="right">41.3%</td>
<td align="right">28,480,928</td>
<td align="right">36.8%</td>
<td align="right">-38.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">64,273,350</td>
<td align="right">57.5%</td>
<td align="right">44,137,535</td>
<td align="right">57.1%</td>
<td align="right">-31.3%</td>
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
<td align="right">164</td>
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
<td align="right">50,440</td>
<td align="right">67.9%</td>
<td align="right">4,229,948</td>
<td align="right">99.8%</td>
<td align="right">8,286.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">23,852</td>
<td align="right">32.1%</td>
<td align="right">10,066</td>
<td align="right">0.2%</td>
<td align="right">-57.8%</td>
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
<td align="right">37,686</td>
<td align="right">74.7%</td>
<td align="right">4,218,283</td>
<td align="right">99.7%</td>
<td align="right">11,093.2%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">2,771</td>
<td align="right">5.5%</td>
<td align="right">5,418</td>
<td align="right">0.1%</td>
<td align="right">95.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">6,373</td>
<td align="right">12.6%</td>
<td align="right">2,466</td>
<td align="right">0.1%</td>
<td align="right">-61.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">557</td>
<td align="right">1.1%</td>
<td align="right">620</td>
<td align="right">0.0%</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">1,359</td>
<td align="right">2.7%</td>
<td align="right">1,467</td>
<td align="right">0.0%</td>
<td align="right">7.9%</td>
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
<td align="right">7,228,268</td>
<td align="right">7,228,268 / 0 !!</td>
<td align="right">7,143,023</td>
<td align="right">7,143,023 / 0 !!</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">70,484</td>
<td align="right">70,484 / 0 !!</td>
<td align="right">70,541</td>
<td align="right">70,541 / 0 !!</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">157,963</td>
<td align="right">157,963 / 0 !!</td>
<td align="right">157,978</td>
<td align="right">157,978 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">8,716,167</td>
<td align="right">8,716,167 / 0 !!</td>
<td align="right">8,716,587</td>
<td align="right">8,716,587 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">9,440,636</td>
<td align="right">9,440,636 / 0 !!</td>
<td align="right">9,440,830</td>
<td align="right">9,440,830 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">9,237,245</td>
<td align="right">9,237,245 / 0 !!</td>
<td align="right">9,237,398</td>
<td align="right">9,237,398 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">12,233,659</td>
<td align="right">12,233,659 / 0 !!</td>
<td align="right">12,233,748</td>
<td align="right">12,233,748 / 0 !!</td>
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
<td align="right">2,137</td>
<td align="right">0.0%</td>
<td align="right">213,600.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">59,994,480</td>
<td align="right">18.8%</td>
<td align="right">52,868,118</td>
<td align="right">18.5%</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">206,916,895</td>
<td align="right">64.7%</td>
<td align="right">185,096,107</td>
<td align="right">64.8%</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">52,800,994</td>
<td align="right">16.5%</td>
<td align="right">47,720,426</td>
<td align="right">16.7%</td>
<td align="right">-9.6%</td>
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
<td align="right">1,007,053</td>
<td align="right">95.7%</td>
<td align="right">912,420</td>
<td align="right">95.2%</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">45,195</td>
<td align="right">4.3%</td>
<td align="right">45,965</td>
<td align="right">4.8%</td>
<td align="right">1.7%</td>
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
<td align="left">mutable class</td>
<td align="right">21,443</td>
<td align="right">47.4%</td>
<td align="right">22,158</td>
<td align="right">48.2%</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">3,106</td>
<td align="right">6.9%</td>
<td align="right">3,041</td>
<td align="right">6.6%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">2,743</td>
<td align="right">6.1%</td>
<td align="right">2,784</td>
<td align="right">6.1%</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">4,080</td>
<td align="right">9.0%</td>
<td align="right">4,025</td>
<td align="right">8.8%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">6,852</td>
<td align="right">15.2%</td>
<td align="right">6,937</td>
<td align="right">15.1%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">2,324</td>
<td align="right">5.1%</td>
<td align="right">2,348</td>
<td align="right">5.1%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">3,164</td>
<td align="right">7.0%</td>
<td align="right">3,163</td>
<td align="right">6.9%</td>
<td align="right">-0.0%</td>
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
<td align="right">261,069,997</td>
<td align="right">100.0%</td>
<td align="right">235,686,004</td>
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
<td align="right">4,613</td>
<td align="right">0.0%</td>
<td align="right">4,538</td>
<td align="right">0.0%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,355</td>
<td align="right">0.0%</td>
<td align="right">1,339</td>
<td align="right">0.0%</td>
<td align="right">-1.2%</td>
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
<td align="right">13,610</td>
<td align="right">100.0%</td>
<td align="right">13,576</td>
<td align="right">100.0%</td>
<td align="right">-0.2%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">31</td>
<td align="right">0.0%</td>
<td align="right">30</td>
<td align="right">0.0%</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,265,957</td>
<td align="right">100.0%</td>
<td align="right">2,266,033</td>
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
<td align="right">731,620</td>
<td align="right">72.0%</td>
<td align="right">731,644</td>
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
<td align="right">1,576,964</td>
<td align="right">17.4%</td>
<td align="right">1,574,306</td>
<td align="right">17.3%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">7,327,376</td>
<td align="right">80.7%</td>
<td align="right">7,330,293</td>
<td align="right">80.7%</td>
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
<td align="right">174,029</td>
<td align="right">1.9%</td>
<td align="right">174,061</td>
<td align="right">1.9%</td>
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
<td align="right">30,007</td>
<td align="right">96.8%</td>
<td align="right">29,945</td>
<td align="right">96.8%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">984</td>
<td align="right">3.2%</td>
<td align="right">982</td>
<td align="right">3.2%</td>
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
<td align="left">not managed dict</td>
<td align="right">302</td>
<td align="right">30.7%</td>
<td align="right">304</td>
<td align="right">31.0%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">518</td>
<td align="right">52.6%</td>
<td align="right">518</td>
<td align="right">52.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">102</td>
<td align="right">10.4%</td>
<td align="right">102</td>
<td align="right">10.4%</td>
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
<td align="right">2,583,055</td>
<td align="right">12.7%</td>
<td align="right">1,678,140</td>
<td align="right">8.6%</td>
<td align="right">-35.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">17,740,547</td>
<td align="right">87.3%</td>
<td align="right">17,743,051</td>
<td align="right">91.3%</td>
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
<td align="right">1,543</td>
<td align="right">72.8%</td>
<td align="right">1,614</td>
<td align="right">73.7%</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">576</td>
<td align="right">27.2%</td>
<td align="right">576</td>
<td align="right">26.3%</td>
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
<td align="right">1,614</td>
<td align="right">100.0%</td>
<td align="right">4.6%</td>
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
<td align="right">623,577</td>
<td align="right">0.4%</td>
<td align="right">426,280</td>
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
<td align="right">164,238,280</td>
<td align="right">94.0%</td>
<td align="right">155,582,075</td>
<td align="right">93.8%</td>
<td align="right">-5.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">9,755,768</td>
<td align="right">5.6%</td>
<td align="right">9,883,432</td>
<td align="right">6.0%</td>
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
<td align="right">6</td>
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
<td align="right">14,313</td>
<td align="right">43.0%</td>
<td align="right">11,382</td>
<td align="right">42.7%</td>
<td align="right">-20.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">18,995</td>
<td align="right">57.0%</td>
<td align="right">15,273</td>
<td align="right">57.3%</td>
<td align="right">-19.6%</td>
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
<td align="right">2,608</td>
<td align="right">18.2%</td>
<td align="right">1,664</td>
<td align="right">14.6%</td>
<td align="right">-36.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">8,021</td>
<td align="right">56.0%</td>
<td align="right">5,987</td>
<td align="right">52.6%</td>
<td align="right">-25.4%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">729</td>
<td align="right">5.1%</td>
<td align="right">769</td>
<td align="right">6.8%</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">1,257</td>
<td align="right">8.8%</td>
<td align="right">1,265</td>
<td align="right">11.1%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">729</td>
<td align="right">5.1%</td>
<td align="right">728</td>
<td align="right">6.4%</td>
<td align="right">-0.1%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">83,696,893</td>
<td align="right">100.0%</td>
<td align="right">83,401,649</td>
<td align="right">100.0%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">6,351</td>
<td align="right">0.0%</td>
<td align="right">6,354</td>
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
<td align="right">2,399</td>
<td align="right">88.5%</td>
<td align="right">2,391</td>
<td align="right">88.4%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">312</td>
<td align="right">11.5%</td>
<td align="right">313</td>
<td align="right">11.6%</td>
<td align="right">0.3%</td>
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
<td align="right">269</td>
<td align="right">86.2%</td>
<td align="right">270</td>
<td align="right">86.3%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">43</td>
<td align="right">13.8%</td>
<td align="right">43</td>
<td align="right">13.7%</td>
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
<td align="right">1,410,882,605</td>
<td align="right">32.9%</td>
<td align="right">1,097,055,273</td>
<td align="right">31.7%</td>
<td align="right">-22.2%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">250,902,610</td>
<td align="right">5.8%</td>
<td align="right">200,314,134</td>
<td align="right">5.8%</td>
<td align="right">-20.2%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">2,537,946,960</td>
<td align="right">59.1%</td>
<td align="right">2,071,420,601</td>
<td align="right">59.9%</td>
<td align="right">-18.4%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">93,338,413</td>
<td align="right">2.2%</td>
<td align="right">87,165,368</td>
<td align="right">2.5%</td>
<td align="right">-6.6%</td>
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
<td align="right">11,079,151</td>
<td align="right">4.6%</td>
<td align="right">4,627,983</td>
<td align="right">2.4%</td>
<td align="right">-58.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">46,136,806</td>
<td align="right">19.1%</td>
<td align="right">28,480,928</td>
<td align="right">14.6%</td>
<td align="right">-38.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">2,583,055</td>
<td align="right">1.1%</td>
<td align="right">1,678,140</td>
<td align="right">0.9%</td>
<td align="right">-35.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">45,132,172</td>
<td align="right">18.7%</td>
<td align="right">35,210,041</td>
<td align="right">18.1%</td>
<td align="right">-22.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">30,567,498</td>
<td align="right">12.7%</td>
<td align="right">25,710,708</td>
<td align="right">13.2%</td>
<td align="right">-15.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">59,994,480</td>
<td align="right">24.9%</td>
<td align="right">52,868,118</td>
<td align="right">27.2%</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">9,755,768</td>
<td align="right">4.0%</td>
<td align="right">9,883,432</td>
<td align="right">5.1%</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">35,652,766</td>
<td align="right">14.8%</td>
<td align="right">35,504,521</td>
<td align="right">18.3%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">174,029</td>
<td align="right">0.1%</td>
<td align="right">174,061</td>
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
<td align="right">12,908,716</td>
<td align="right">13.8%</td>
<td align="right">9,570,029</td>
<td align="right">11.0%</td>
<td align="right">-25.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">7,331,242</td>
<td align="right">7.9%</td>
<td align="right">6,648,628</td>
<td align="right">7.6%</td>
<td align="right">-9.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">3,206,532</td>
<td align="right">3.4%</td>
<td align="right">3,025,608</td>
<td align="right">3.5%</td>
<td align="right">-5.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">6,164,202</td>
<td align="right">6.6%</td>
<td align="right">5,949,441</td>
<td align="right">6.8%</td>
<td align="right">-3.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">28,936,862</td>
<td align="right">31.0%</td>
<td align="right">28,058,361</td>
<td align="right">32.2%</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">11,146,400</td>
<td align="right">11.9%</td>
<td align="right">11,213,746</td>
<td align="right">12.9%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,576,185</td>
<td align="right">1.7%</td>
<td align="right">1,573,527</td>
<td align="right">1.8%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">11,706,483</td>
<td align="right">12.5%</td>
<td align="right">11,705,157</td>
<td align="right">13.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">2,103,577</td>
<td align="right">2.3%</td>
<td align="right">2,103,794</td>
<td align="right">2.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">5,099,600</td>
<td align="right">5.5%</td>
<td align="right">5,099,642</td>
<td align="right">5.9%</td>
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
<td align="right">41,133,494</td>
<td align="right">19.6%</td>
<td align="right">40,913,197</td>
<td align="right">19.5%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">75,423,057</td>
<td align="right">35.9%</td>
<td align="right">75,203,082</td>
<td align="right">35.8%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">75,423,842</td>
<td align="right">35.9%</td>
<td align="right">75,203,867</td>
<td align="right">35.8%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">78,892,813</td>
<td align="right">37.5%</td>
<td align="right">78,672,907</td>
<td align="right">37.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">78,892,813</td>
<td align="right">37.5%</td>
<td align="right">78,672,907</td>
<td align="right">37.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">187,863,519</td>
<td align="right">89.3%</td>
<td align="right">187,494,594</td>
<td align="right">89.3%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">131,427,288</td>
<td align="right">62.5%</td>
<td align="right">131,343,291</td>
<td align="right">62.5%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">950,354</td>
<td align="right">0.5%</td>
<td align="right">950,323</td>
<td align="right">0.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">3,468,971</td>
<td align="right">1.6%</td>
<td align="right">3,469,040</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">18,497,169</td>
<td align="right">8.8%</td>
<td align="right">18,497,427</td>
<td align="right">8.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">9,332,111</td>
<td align="right">4.4%</td>
<td align="right">9,332,190</td>
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
<td align="left">Interpreter mortal increfs</td>
<td align="right">1,118,693,110</td>
<td align="right">33.1%</td>
<td align="right">902,019,519</td>
<td align="right">26.7%</td>
<td align="right">-19.4%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">1,208,116,386</td>
<td align="right">35.8%</td>
<td align="right">1,432,005,777</td>
<td align="right">42.4%</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">977,323</td>
<td align="right"></td>
<td align="right">827,626</td>
<td align="right"></td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">8,976</td>
<td align="right">0.0%</td>
<td align="right">9,992</td>
<td align="right">0.0%</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">1,340,025,408</td>
<td align="right">36.8%</td>
<td align="right">1,486,084,624</td>
<td align="right">40.8%</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">51,577,567</td>
<td align="right">1.4%</td>
<td align="right">46,357,808</td>
<td align="right">1.3%</td>
<td align="right">-10.1%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">1,408,076,289</td>
<td align="right">38.6%</td>
<td align="right">1,268,894,434</td>
<td align="right">34.8%</td>
<td align="right">-9.9%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">3,170,360</td>
<td align="right"></td>
<td align="right">2,960,987</td>
<td align="right"></td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">150,171,062</td>
<td align="right"></td>
<td align="right">145,221,377</td>
<td align="right"></td>
<td align="right">-3.3%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">778,052</td>
<td align="right">0.2%</td>
<td align="right">755,941</td>
<td align="right">0.2%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">2,194,407</td>
<td align="right"></td>
<td align="right">2,134,771</td>
<td align="right"></td>
<td align="right">-2.7%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">974,410,676</td>
<td align="right">28.8%</td>
<td align="right">964,208,387</td>
<td align="right">28.6%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">76,300,329</td>
<td align="right">2.3%</td>
<td align="right">75,783,802</td>
<td align="right">2.2%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">844,188,142</td>
<td align="right">23.2%</td>
<td align="right">842,501,664</td>
<td align="right">23.1%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">129,172,406</td>
<td align="right">26.8%</td>
<td align="right">128,966,069</td>
<td align="right">26.8%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">141,843,719</td>
<td align="right"></td>
<td align="right">141,635,752</td>
<td align="right"></td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">128,385,378</td>
<td align="right">26.7%</td>
<td align="right">128,200,136</td>
<td align="right">26.6%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">249,448,896</td>
<td align="right"></td>
<td align="right">249,210,048</td>
<td align="right"></td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">352,241,451</td>
<td align="right">73.2%</td>
<td align="right">352,090,834</td>
<td align="right">73.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">352,277,053</td>
<td align="right"></td>
<td align="right">352,126,437</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">866,380</td>
<td align="right"></td>
<td align="right">866,429</td>
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
<td align="right">18,867</td>
<td align="right"></td>
<td align="right">4,286,694</td>
<td align="right"></td>
<td align="right">22,620.6%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">1,594,212,529</td>
<td align="right">2,099.2%</td>
<td align="right">3,947,569,323</td>
<td align="right">2,977.7%</td>
<td align="right">147.6%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">5,761</td>
<td align="right">30.5%</td>
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
<td align="right">1,807</td>
<td align="right">9.6%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Inner loop found
<details>
<summary>ⓘ</summary>

A trace is truncated because it has an inner loop
</details>
</td>
<td align="right">115</td>
<td align="right">0.6%</td>
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
<td align="right">9,211</td>
<td align="right">48.8%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">2,088</td>
<td align="right">11.1%</td>
<td align="right">3,893</td>
<td align="right">0.1%</td>
<td align="right">86.4%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">75,942,863</td>
<td align="right"></td>
<td align="right">132,571,298</td>
<td align="right"></td>
<td align="right">74.6%</td>
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
<td align="right">66</td>
<td align="right">0.0%</td>
<td align="right">66 / 0 !!</td>
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
<td align="right">1,852</td>
<td align="right">88.7%</td>
<td align="right">3,893</td>
<td align="right">100.0%</td>
<td align="right">110.2%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">2,088</td>
<td align="right"></td>
<td align="right">3,893</td>
<td align="right"></td>
<td align="right">86.4%</td>
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
<td align="right">8,409,457</td>
<td align="right">65.7%</td>
<td align="right">43,139,212</td>
<td align="right">80.7%</td>
<td align="right">413.0%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">12,808,192</td>
<td align="right"></td>
<td align="right">53,485,568</td>
<td align="right"></td>
<td align="right">317.6%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">253,152</td>
<td align="right">2.0%</td>
<td align="right">855,408</td>
<td align="right">1.6%</td>
<td align="right">237.9%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">4,143,731</td>
<td align="right">32.4%</td>
<td align="right">9,487,055</td>
<td align="right">17.7%</td>
<td align="right">128.9%</td>
</tr>
<tr>
<td align="left">
Freed memory size
<details>
<summary>ⓘ</summary>

The size of the memory freed from the JIT traces
</details>
</td>
<td align="right">102,400</td>
<td align="right">0.8%</td>
<td align="right">172,032</td>
<td align="right">0.3%</td>
<td align="right">68.0%</td>
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
<td align="left">923</td>
<td align="right">49.8%</td>
<td align="left">735</td>
<td align="right">18.9%</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">649</td>
<td align="right">35.0%</td>
<td align="left">1,644</td>
<td align="right">42.2%</td>
<td align="right">153.3%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">259</td>
<td align="right">14.0%</td>
<td align="left">861</td>
<td align="right">22.1%</td>
<td align="right">232.4%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">21</td>
<td align="right">1.1%</td>
<td align="left">426</td>
<td align="right">10.9%</td>
<td align="right">1,928.6%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">151</td>
<td align="right">3.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">76</td>
<td align="right">2.0%</td>
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
<td align="right">81</td>
<td align="right">3.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">280</td>
<td align="right">13.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">370</td>
<td align="right">17.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">970</td>
<td align="right">46.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">321</td>
<td align="right">15.4%</td>
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
<td align="right">59</td>
<td align="right">2.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">88</td>
<td align="right">4.2%</td>
<td align="right">66</td>
<td align="right">1.7%</td>
<td align="right">-25.0%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">190</td>
<td align="right">9.1%</td>
<td align="right">271</td>
<td align="right">7.0%</td>
<td align="right">42.6%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">1,063</td>
<td align="right">50.9%</td>
<td align="right">883</td>
<td align="right">22.7%</td>
<td align="right">-16.9%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">193</td>
<td align="right">9.2%</td>
<td align="right">1,244</td>
<td align="right">32.0%</td>
<td align="right">544.6%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">238</td>
<td align="right">11.4%</td>
<td align="right">867</td>
<td align="right">22.3%</td>
<td align="right">264.3%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">21</td>
<td align="right">1.0%</td>
<td align="right">382</td>
<td align="right">9.8%</td>
<td align="right">1,719.0%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">105</td>
<td align="right">2.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">75</td>
<td align="right">1.9%</td>
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
<td align="right">759</td>
<td align="right">4,532,489</td>
<td align="right">597,065.9%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">6,613</td>
<td align="right">22,301,767</td>
<td align="right">337,141.3%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">759</td>
<td align="right">2,251,694</td>
<td align="right">296,565.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">7,384</td>
<td align="right">6,329,889</td>
<td align="right">85,624.4%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">8,566</td>
<td align="right">3,402,860</td>
<td align="right">39,625.2%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">35,660</td>
<td align="right">6,980,320</td>
<td align="right">19,474.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">45,128</td>
<td align="right">7,429,204</td>
<td align="right">16,362.5%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">45,128</td>
<td align="right">7,429,204</td>
<td align="right">16,362.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">62,306</td>
<td align="right">7,068,272</td>
<td align="right">11,244.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">124,065</td>
<td align="right">10,377,732</td>
<td align="right">8,264.8%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">68,459</td>
<td align="right">4,830,523</td>
<td align="right">6,956.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">263,680</td>
<td align="right">16,720,522</td>
<td align="right">6,241.2%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">1,437,884</td>
<td align="right">41,749,959</td>
<td align="right">2,803.6%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">1,276,622</td>
<td align="right">23,344,792</td>
<td align="right">1,728.6%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">1,276,622</td>
<td align="right">23,344,792</td>
<td align="right">1,728.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">1,064,624</td>
<td align="right">19,072,978</td>
<td align="right">1,691.5%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">1,437,884</td>
<td align="right">25,380,424</td>
<td align="right">1,665.1%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">1,437,884</td>
<td align="right">23,299,077</td>
<td align="right">1,520.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right">258,585</td>
<td align="right">3,738,070</td>
<td align="right">1,345.6%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">18,228</td>
<td align="right">258,687</td>
<td align="right">1,319.2%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">2,345,196</td>
<td align="right">30,394,967</td>
<td align="right">1,196.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">3,087,060</td>
<td align="right">39,475,870</td>
<td align="right">1,178.8%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">2,038,824</td>
<td align="right">23,391,618</td>
<td align="right">1,047.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">1,668,152</td>
<td align="right">18,230,266</td>
<td align="right">992.8%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">1,437,884</td>
<td align="right">15,478,195</td>
<td align="right">976.5%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">1,437,884</td>
<td align="right">15,420,611</td>
<td align="right">972.5%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">4,819,543</td>
<td align="right">50,939,448</td>
<td align="right">956.9%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">3,149,226</td>
<td align="right">31,684,770</td>
<td align="right">906.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">1,072,547</td>
<td align="right">10,310,972</td>
<td align="right">861.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">5,347,697</td>
<td align="right">41,350,717</td>
<td align="right">673.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_DICT</td>
<td align="right">28,192</td>
<td align="right">206,188</td>
<td align="right">631.4%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">1,763,664</td>
<td align="right">11,898,468</td>
<td align="right">574.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right">28,192</td>
<td align="right">178,418</td>
<td align="right">532.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">1,437,884</td>
<td align="right">8,697,033</td>
<td align="right">504.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">5,912,937</td>
<td align="right">35,670,986</td>
<td align="right">503.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">3,184,989</td>
<td align="right">19,097,418</td>
<td align="right">499.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">8,916,744</td>
<td align="right">50,486,292</td>
<td align="right">466.2%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">1,437,884</td>
<td align="right">7,706,744</td>
<td align="right">436.0%</td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right">1,437,884</td>
<td align="right">7,465,130</td>
<td align="right">419.2%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">2,168,928</td>
<td align="right">10,059,794</td>
<td align="right">363.8%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_OVERFLOWED</td>
<td align="right">28,276</td>
<td align="right">128,167</td>
<td align="right">353.3%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">1,046,440</td>
<td align="right">4,552,467</td>
<td align="right">335.0%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">1,024,726</td>
<td align="right">4,421,469</td>
<td align="right">331.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">2,125,151</td>
<td align="right">8,969,485</td>
<td align="right">322.1%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right">1,437,884</td>
<td align="right">5,855,018</td>
<td align="right">307.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">1,609,437</td>
<td align="right">6,159,690</td>
<td align="right">282.7%</td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right">1,129,771</td>
<td align="right">4,203,583</td>
<td align="right">272.1%</td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">26,932</td>
<td align="right">96,378</td>
<td align="right">257.9%</td>
</tr>
<tr>
<td align="left">_COPY_2</td>
<td align="right">134,398</td>
<td align="right">457,458</td>
<td align="right">240.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">1,024,726</td>
<td align="right">3,477,739</td>
<td align="right">239.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">24,406,500</td>
<td align="right">78,128,243</td>
<td align="right">220.1%</td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right">2,883,096</td>
<td align="right">8,805,550</td>
<td align="right">205.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">52,447</td>
<td align="right">159,021</td>
<td align="right">203.2%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">13,289,203</td>
<td align="right">40,259,824</td>
<td align="right">203.0%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">11,816,601</td>
<td align="right">31,977,389</td>
<td align="right">170.6%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">5,989,400</td>
<td align="right">16,206,290</td>
<td align="right">170.6%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">3,871,971</td>
<td align="right">10,202,801</td>
<td align="right">163.5%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">174,242</td>
<td align="right">432,854</td>
<td align="right">148.4%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">3,864,592</td>
<td align="right">9,565,712</td>
<td align="right">147.5%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">6,116,248</td>
<td align="right">14,851,278</td>
<td align="right">142.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">14,146,332</td>
<td align="right">34,280,919</td>
<td align="right">142.3%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">1,828,625</td>
<td align="right">4,405,176</td>
<td align="right">140.9%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">284,126,966</td>
<td align="right">681,583,784</td>
<td align="right">139.9%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">833,316</td>
<td align="right">1,979,913</td>
<td align="right">137.6%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">316,568,736</td>
<td align="right">742,729,483</td>
<td align="right">134.6%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">21,885,921</td>
<td align="right">45,497,028</td>
<td align="right">107.9%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">74,943,751</td>
<td align="right">155,377,796</td>
<td align="right">107.3%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">5,104,481</td>
<td align="right">42</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">5,036,037</td>
<td align="right">5,912</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">26,678,988</td>
<td align="right">52,516,579</td>
<td align="right">96.8%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">26,678,988</td>
<td align="right">52,498,729</td>
<td align="right">96.8%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">6,468,418</td>
<td align="right">12,598,551</td>
<td align="right">94.8%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">47,905,613</td>
<td align="right">89,064,572</td>
<td align="right">85.9%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">1,437,884</td>
<td align="right">2,573,635</td>
<td align="right">79.0%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">29,245,399</td>
<td align="right">52,246,872</td>
<td align="right">78.6%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">3,200,888</td>
<td align="right">5,686,905</td>
<td align="right">77.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">25,957,073</td>
<td align="right">45,219,160</td>
<td align="right">74.2%</td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right">22</td>
<td align="right">38</td>
<td align="right">72.7%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">47,905,591</td>
<td align="right">82,502,175</td>
<td align="right">72.2%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">25,684,740</td>
<td align="right">43,042,277</td>
<td align="right">67.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">10,761,780</td>
<td align="right">17,888,714</td>
<td align="right">66.2%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">4,926,828</td>
<td align="right">8,130,010</td>
<td align="right">65.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">37,433,705</td>
<td align="right">61,527,247</td>
<td align="right">64.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">2,279,117</td>
<td align="right">3,644,840</td>
<td align="right">59.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">9,868,790</td>
<td align="right">15,530,385</td>
<td align="right">57.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">7,346,967</td>
<td align="right">11,468,487</td>
<td align="right">56.1%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">28,037,250</td>
<td align="right">43,506,726</td>
<td align="right">55.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">6,431,222</td>
<td align="right">9,836,093</td>
<td align="right">52.9%</td>
</tr>
<tr>
<td align="left">_SWAP_3</td>
<td align="right">2,201,071</td>
<td align="right">1,044,139</td>
<td align="right">-52.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">7,544,221</td>
<td align="right">11,495,147</td>
<td align="right">52.4%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">35,642,800</td>
<td align="right">53,541,550</td>
<td align="right">50.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">3,302,306</td>
<td align="right">4,872,784</td>
<td align="right">47.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">32,537,969</td>
<td align="right">47,806,877</td>
<td align="right">46.9%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">26,063,219</td>
<td align="right">38,149,856</td>
<td align="right">46.4%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">87,879,048</td>
<td align="right">127,358,659</td>
<td align="right">44.9%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">26,063,219</td>
<td align="right">37,691,681</td>
<td align="right">44.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">2,209,499</td>
<td align="right">3,155,651</td>
<td align="right">42.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">1,062,572</td>
<td align="right">1,503,566</td>
<td align="right">41.5%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">22,385,351</td>
<td align="right">31,085,818</td>
<td align="right">38.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">1,763,664</td>
<td align="right">2,421,193</td>
<td align="right">37.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right">2,172,166</td>
<td align="right">2,946,185</td>
<td align="right">35.6%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">5,166</td>
<td align="right">6,723</td>
<td align="right">30.1%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">4,926,828</td>
<td align="right">6,222,602</td>
<td align="right">26.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">15,790,849</td>
<td align="right">19,721,559</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">1,437,884</td>
<td align="right">1,773,999</td>
<td align="right">23.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">3,350,860</td>
<td align="right">4,045,467</td>
<td align="right">20.7%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">1,567,848</td>
<td align="right">1,858,697</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">1,567,848</td>
<td align="right">1,858,697</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">1,437,884</td>
<td align="right">1,196,511</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">2,125,144</td>
<td align="right">1,867,893</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">8,164,652</td>
<td align="right">9,102,190</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">11,867,483</td>
<td align="right">13,207,684</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">11,867,483</td>
<td align="right">13,207,684</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">17,962,057</td>
<td align="right">18,735,873</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">39,973,435</td>
<td align="right">38,294,151</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">3,096</td>
<td align="right">3,088</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">2,449,401</td>
<td align="right">2,453,553</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">2,513,886</td>
<td align="right">2,509,646</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">67,008,606</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right"></td>
<td align="right">20,534,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">16,288,442</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right"></td>
<td align="right">13,940,320</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">9,509,021</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right"></td>
<td align="right">8,044,812</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_OVERFLOWED</td>
<td align="right"></td>
<td align="right">8,005,441</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right"></td>
<td align="right">7,776,739</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">7,301,517</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">7,301,517</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right"></td>
<td align="right">6,692,941</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">6,560,040</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right"></td>
<td align="right">5,998,423</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_COMMON_CONSTANT</td>
<td align="right"></td>
<td align="right">5,946,180</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right"></td>
<td align="right">5,946,157</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right"></td>
<td align="right">5,481,832</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">3,853,197</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right"></td>
<td align="right">3,839,469</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right"></td>
<td align="right">2,848,322</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right"></td>
<td align="right">2,606,653</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_PROPERTY_FRAME</td>
<td align="right"></td>
<td align="right">2,081,347</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right"></td>
<td align="right">1,969,393</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right"></td>
<td align="right">1,916,291</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">1,771,952</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right"></td>
<td align="right">1,394,507</td>
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
<td align="right">1,021,765</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right"></td>
<td align="right">905,449</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right"></td>
<td align="right">792,212</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right"></td>
<td align="right">792,212</td>
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
<td align="right">740,912</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_IMPORT_NAME</td>
<td align="right"></td>
<td align="right">740,902</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right"></td>
<td align="right">664,545</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_LIST</td>
<td align="right"></td>
<td align="right">543,569</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right"></td>
<td align="right">543,569</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right"></td>
<td align="right">438,324</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right"></td>
<td align="right">411,840</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_1</td>
<td align="right"></td>
<td align="right">270,093</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right"></td>
<td align="right">200,693</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NULL</td>
<td align="right"></td>
<td align="right">112,112</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right"></td>
<td align="right">100,686</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right"></td>
<td align="right">100,674</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_KW_NON_PY</td>
<td align="right"></td>
<td align="right">89,775</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE_KW</td>
<td align="right"></td>
<td align="right">89,775</td>
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
<td align="left">_TO_BOOL</td>
<td align="right"></td>
<td align="right">66,213</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LEN</td>
<td align="right"></td>
<td align="right">61,775</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_KW</td>
<td align="right"></td>
<td align="right">53,635</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PY_FRAME_KW</td>
<td align="right"></td>
<td align="right">53,635</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right"></td>
<td align="right">50,566</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">50,566</td>
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
<td align="left">_LOAD_SMALL_INT_0</td>
<td align="right"></td>
<td align="right">46,236</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_TUPLE</td>
<td align="right"></td>
<td align="right">28,831</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right"></td>
<td align="right">17,892</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right"></td>
<td align="right">17,850</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right"></td>
<td align="right">17,850</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_ATTR</td>
<td align="right"></td>
<td align="right">17,850</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right"></td>
<td align="right">17,850</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_EXCEPT</td>
<td align="right"></td>
<td align="right">17,413</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right"></td>
<td align="right">2,309</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE</td>
<td align="right"></td>
<td align="right">657</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right"></td>
<td align="right">484</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right"></td>
<td align="right">70</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS</td>
<td align="right"></td>
<td align="right">70</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">63</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_2</td>
<td align="right"></td>
<td align="right">63</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_3</td>
<td align="right"></td>
<td align="right">16</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right"></td>
<td align="right">10</td>
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
<td align="right">1,482</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">550</td>
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
Stats gathered on: 2025-10-22
