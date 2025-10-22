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
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">92,494</td>
<td align="right">621,222</td>
<td align="right">571.6%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">564,512</td>
<td align="right">1,093,282</td>
<td align="right">93.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">2,346,119</td>
<td align="right">570,623</td>
<td align="right">-75.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">5,808,336</td>
<td align="right">1,678,731</td>
<td align="right">-71.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,900,665</td>
<td align="right">554,927</td>
<td align="right">-70.8%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">3,048,915</td>
<td align="right">1,173,274</td>
<td align="right">-61.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">9,223,509</td>
<td align="right">3,787,447</td>
<td align="right">-58.9%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">3,879,410</td>
<td align="right">1,643,509</td>
<td align="right">-57.6%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">5,888,064</td>
<td align="right">9,184,632</td>
<td align="right">56.0%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">775,935</td>
<td align="right">396,356</td>
<td align="right">-48.9%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">698,134</td>
<td align="right">1,019,686</td>
<td align="right">46.1%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">2,722,029</td>
<td align="right">1,512,512</td>
<td align="right">-44.4%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">830,502</td>
<td align="right">470,242</td>
<td align="right">-43.4%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">14,408,577</td>
<td align="right">8,411,924</td>
<td align="right">-41.6%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">8,086,107</td>
<td align="right">4,785,252</td>
<td align="right">-40.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">8,020,863</td>
<td align="right">5,111,882</td>
<td align="right">-36.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">3,313,912</td>
<td align="right">4,512,783</td>
<td align="right">36.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">7,452,966</td>
<td align="right">4,862,529</td>
<td align="right">-34.8%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">830,502</td>
<td align="right">552,687</td>
<td align="right">-33.5%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">1,570,013</td>
<td align="right">1,076,298</td>
<td align="right">-31.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">8,074,913</td>
<td align="right">5,539,240</td>
<td align="right">-31.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">2,077,810</td>
<td align="right">1,433,906</td>
<td align="right">-31.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">565,860</td>
<td align="right">391,035</td>
<td align="right">-30.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">10,272,629</td>
<td align="right">7,229,028</td>
<td align="right">-29.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">9,624,831</td>
<td align="right">6,874,802</td>
<td align="right">-28.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">2,483,229</td>
<td align="right">1,786,845</td>
<td align="right">-28.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">6,427,767</td>
<td align="right">4,627,161</td>
<td align="right">-28.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">15,181,396</td>
<td align="right">11,079,287</td>
<td align="right">-27.0%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">7,163,281</td>
<td align="right">9,065,596</td>
<td align="right">26.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">2,072,500</td>
<td align="right">1,523,428</td>
<td align="right">-26.5%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">32,180,063</td>
<td align="right">24,859,771</td>
<td align="right">-22.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">3,207,532</td>
<td align="right">2,479,301</td>
<td align="right">-22.7%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">21,969,436</td>
<td align="right">17,184,854</td>
<td align="right">-21.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">23,788,856</td>
<td align="right">19,221,568</td>
<td align="right">-19.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">42,520,715</td>
<td align="right">34,613,780</td>
<td align="right">-18.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">7,350,164</td>
<td align="right">5,987,342</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">26,921,578</td>
<td align="right">22,020,583</td>
<td align="right">-18.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">5,034,025</td>
<td align="right">4,143,437</td>
<td align="right">-17.7%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">3,511,514</td>
<td align="right">2,897,193</td>
<td align="right">-17.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,499,398</td>
<td align="right">2,080,646</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">30,251,094</td>
<td align="right">25,296,652</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">7,942,592</td>
<td align="right">6,732,490</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">2,592,513</td>
<td align="right">2,232,253</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">4,549,550</td>
<td align="right">3,934,110</td>
<td align="right">-13.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">86,761,005</td>
<td align="right">75,378,823</td>
<td align="right">-13.1%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">138,914</td>
<td align="right">122,346</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">3,915,310</td>
<td align="right">3,459,563</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">15,156,854</td>
<td align="right">13,513,923</td>
<td align="right">-10.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">21,311,096</td>
<td align="right">19,164,828</td>
<td align="right">-10.1%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">2,241,671</td>
<td align="right">2,016,376</td>
<td align="right">-10.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">1,177,790</td>
<td align="right">1,059,461</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,015,951</td>
<td align="right">920,021</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">234,909</td>
<td align="right">220,267</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">14,739,716</td>
<td align="right">13,828,445</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">15,306,371</td>
<td align="right">14,368,145</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">162,292</td>
<td align="right">171,643</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">24,752,521</td>
<td align="right">23,348,062</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">554,661</td>
<td align="right">582,158</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">13,171,051</td>
<td align="right">12,553,911</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">481,573</td>
<td align="right">465,089</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">655,778</td>
<td align="right">641,136</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">1,159,026</td>
<td align="right">1,184,479</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">1,891,875</td>
<td align="right">1,919,372</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">1,466,987</td>
<td align="right">1,449,919</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">2,205,030</td>
<td align="right">2,190,261</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">3,279,189</td>
<td align="right">3,260,351</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">6,885,343</td>
<td align="right">6,846,312</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">2,781,570</td>
<td align="right">2,772,132</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">4,173,860</td>
<td align="right">4,164,464</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">129,468</td>
<td align="right">129,510</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">332,211</td>
<td align="right">332,295</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">412,827</td>
<td align="right">412,911</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">218,086</td>
<td align="right">218,128</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">523,312</td>
<td align="right">523,375</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">799,514</td>
<td align="right">799,577</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">798,296</td>
<td align="right">798,338</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">5,455,707</td>
<td align="right">5,455,791</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">1,661,340</td>
<td align="right">1,661,341</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">4,848,723</td>
<td align="right">4,848,723</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">4,610,277</td>
<td align="right">4,610,277</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">3,169,517</td>
<td align="right">3,169,517</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">2,949,138</td>
<td align="right">2,949,138</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">1,879,401</td>
<td align="right">1,879,401</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">1,540,131</td>
<td align="right">1,540,131</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">1,398,872</td>
<td align="right">1,398,872</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,320,638</td>
<td align="right">1,320,638</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">1,241,238</td>
<td align="right">1,241,238</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">1,031,162</td>
<td align="right">1,031,162</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">980,478</td>
<td align="right">980,478</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">829,857</td>
<td align="right">829,857</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">482,183</td>
<td align="right">482,183</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">353,185</td>
<td align="right">353,185</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">348,633</td>
<td align="right">348,633</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">314,614</td>
<td align="right">314,614</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">269,843</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">256,323</td>
<td align="right">256,323</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">256,001</td>
<td align="right">256,001</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">254,103</td>
<td align="right">254,103</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">208,457</td>
<td align="right">208,457</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">156,220</td>
<td align="right">156,220</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">148,866</td>
<td align="right">148,866</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">144,907</td>
<td align="right">144,907</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">139,752</td>
<td align="right">139,752</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">134,261</td>
<td align="right">134,261</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">131,967</td>
<td align="right">131,967</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">113,515</td>
<td align="right">113,515</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">102,548</td>
<td align="right">102,548</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">80,561</td>
<td align="right">80,561</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">76,089</td>
<td align="right">76,089</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">74,366</td>
<td align="right">74,366</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">62,556</td>
<td align="right">62,556</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">61,662</td>
<td align="right">61,662</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">61,662</td>
<td align="right">61,662</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">61,662</td>
<td align="right">61,662</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">60,754</td>
<td align="right">60,754</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">59,339</td>
<td align="right">59,339</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">48,891</td>
<td align="right">48,891</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">45,666</td>
<td align="right">45,666</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">45,537</td>
<td align="right">45,537</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">30,556</td>
<td align="right">30,556</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">25,736</td>
<td align="right">25,736</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">25,152</td>
<td align="right">25,152</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">20,509</td>
<td align="right">20,509</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">20,251</td>
<td align="right">20,251</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">20,251</td>
<td align="right">20,251</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">14,448</td>
<td align="right">14,448</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">12,145</td>
<td align="right">12,145</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">10,445</td>
<td align="right">10,445</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">4,772</td>
<td align="right">4,772</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">2,448</td>
<td align="right">2,448</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,942</td>
<td align="right">1,942</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">1,677</td>
<td align="right">1,677</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">1,552</td>
<td align="right">1,552</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">1,548</td>
<td align="right">1,548</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">774</td>
<td align="right">774</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">320</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">257</td>
<td align="right">257</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">193</td>
<td align="right">193</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">169</td>
<td align="right">169</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">156</td>
<td align="right">156</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">150</td>
<td align="right">150</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_UPDATE</td>
<td align="right">129</td>
<td align="right">129</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">128</td>
<td align="right">128</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">125</td>
<td align="right">125</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">38</td>
<td align="right">38</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">14</td>
<td align="right">14</td>
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
<td align="right">61,985</td>
<td align="right">1.6%</td>
<td align="right">61,985</td>
<td align="right">1.6%</td>
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
<td align="right">3,743,639</td>
<td align="right">98.2%</td>
<td align="right">3,743,639</td>
<td align="right">98.2%</td>
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
<td align="right">5,179</td>
<td align="right">0.1%</td>
<td align="right">5,179</td>
<td align="right">0.1%</td>
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
<td align="right">168</td>
<td align="right">25.6%</td>
<td align="right">168</td>
<td align="right">25.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">489</td>
<td align="right">74.4%</td>
<td align="right">489</td>
<td align="right">74.4%</td>
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
<td align="left">add other</td>
<td align="right">295</td>
<td align="right">60.3%</td>
<td align="right">295</td>
<td align="right">60.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">73</td>
<td align="right">14.9%</td>
<td align="right">73</td>
<td align="right">14.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">49</td>
<td align="right">10.0%</td>
<td align="right">49</td>
<td align="right">10.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">49</td>
<td align="right">10.0%</td>
<td align="right">49</td>
<td align="right">10.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">22</td>
<td align="right">4.5%</td>
<td align="right">22</td>
<td align="right">4.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">1</td>
<td align="right">0.2%</td>
<td align="right">1</td>
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
<td align="right">48,891</td>
<td align="right">100.0%</td>
<td align="right">48,891</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">535,477</td>
<td align="right">0.8%</td>
<td align="right">536,593</td>
<td align="right">0.8%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">526,260</td>
<td align="right">0.8%</td>
<td align="right">527,354</td>
<td align="right">0.8%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">68,811,889</td>
<td align="right">99.2%</td>
<td align="right">68,810,749</td>
<td align="right">99.2%</td>
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
<td align="right"></td>
<td align="right"></td>
<td align="right">2</td>
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
<td align="right">11,159</td>
<td align="right">100.0%</td>
<td align="right">11,181</td>
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
<td align="right">75</td>
<td align="right">50.0%</td>
<td align="right">75</td>
<td align="right">50.0%</td>
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
<td align="right">75</td>
<td align="right">100.0%</td>
<td align="right">75</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">798,043</td>
<td align="right">47.9%</td>
<td align="right">798,085</td>
<td align="right">47.9%</td>
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
<td align="right">867,098</td>
<td align="right">52.0%</td>
<td align="right">867,098</td>
<td align="right">52.0%</td>
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
<td align="right">1,431</td>
<td align="right">97.3%</td>
<td align="right">1,452</td>
<td align="right">97.3%</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">40</td>
<td align="right">2.7%</td>
<td align="right">40</td>
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
<td align="left">baseobject</td>
<td align="right">662</td>
<td align="right">46.3%</td>
<td align="right">683</td>
<td align="right">47.0%</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">497</td>
<td align="right">34.7%</td>
<td align="right">497</td>
<td align="right">34.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">81</td>
<td align="right">5.7%</td>
<td align="right">81</td>
<td align="right">5.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">51</td>
<td align="right">3.6%</td>
<td align="right">51</td>
<td align="right">3.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">50</td>
<td align="right">3.5%</td>
<td align="right">50</td>
<td align="right">3.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">46</td>
<td align="right">3.2%</td>
<td align="right">46</td>
<td align="right">3.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">44</td>
<td align="right">3.1%</td>
<td align="right">44</td>
<td align="right">3.0%</td>
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
<td align="right">161,810</td>
<td align="right">25.9%</td>
<td align="right">171,140</td>
<td align="right">27.0%</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">435,222</td>
<td align="right">69.7%</td>
<td align="right">435,222</td>
<td align="right">68.6%</td>
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
<td align="right">27,338</td>
<td align="right">4.4%</td>
<td align="right">27,338</td>
<td align="right">4.3%</td>
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
<td align="right">449</td>
<td align="right">45.0%</td>
<td align="right">470</td>
<td align="right">46.2%</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">548</td>
<td align="right">55.0%</td>
<td align="right">548</td>
<td align="right">53.8%</td>
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
<td align="right">269</td>
<td align="right">59.9%</td>
<td align="right">290</td>
<td align="right">61.7%</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">180</td>
<td align="right">40.1%</td>
<td align="right">180</td>
<td align="right">38.3%</td>
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
<td align="right">8,017,588</td>
<td align="right">46.5%</td>
<td align="right">5,108,505</td>
<td align="right">32.9%</td>
<td align="right">-36.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">9,224,989</td>
<td align="right">53.5%</td>
<td align="right">10,423,860</td>
<td align="right">67.1%</td>
<td align="right">13.0%</td>
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
<td align="right">3,188</td>
<td align="right">97.3%</td>
<td align="right">3,290</td>
<td align="right">97.4%</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">87</td>
<td align="right">2.7%</td>
<td align="right">87</td>
<td align="right">2.6%</td>
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
<td align="right">83</td>
<td align="right">2.6%</td>
<td align="right">587</td>
<td align="right">17.8%</td>
<td align="right">607.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">52</td>
<td align="right">1.6%</td>
<td align="right">136</td>
<td align="right">4.1%</td>
<td align="right">161.5%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">2,109</td>
<td align="right">66.2%</td>
<td align="right">1,582</td>
<td align="right">48.1%</td>
<td align="right">-25.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">287</td>
<td align="right">9.0%</td>
<td align="right">328</td>
<td align="right">10.0%</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">187</td>
<td align="right">5.9%</td>
<td align="right">187</td>
<td align="right">5.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">183</td>
<td align="right">5.7%</td>
<td align="right">183</td>
<td align="right">5.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">147</td>
<td align="right">4.6%</td>
<td align="right">147</td>
<td align="right">4.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">90</td>
<td align="right">2.8%</td>
<td align="right">90</td>
<td align="right">2.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">50</td>
<td align="right">1.6%</td>
<td align="right">50</td>
<td align="right">1.5%</td>
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
<td align="right">4,936,121</td>
<td align="right">4,936,121 / 0 !!</td>
<td align="right">4,936,121</td>
<td align="right">4,936,121 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">4,523,385</td>
<td align="right">4,523,385 / 0 !!</td>
<td align="right">4,523,385</td>
<td align="right">4,523,385 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">225,750</td>
<td align="right">225,750 / 0 !!</td>
<td align="right">225,750</td>
<td align="right">225,750 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">33,798</td>
<td align="right">33,798 / 0 !!</td>
<td align="right">33,798</td>
<td align="right">33,798 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">31,992</td>
<td align="right">31,992 / 0 !!</td>
<td align="right">31,992</td>
<td align="right">31,992 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">27,993</td>
<td align="right">27,993 / 0 !!</td>
<td align="right">27,993</td>
<td align="right">27,993 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">19,866</td>
<td align="right">19,866 / 0 !!</td>
<td align="right">19,866</td>
<td align="right">19,866 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">14,577</td>
<td align="right">14,577 / 0 !!</td>
<td align="right">14,577</td>
<td align="right">14,577 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">2,322</td>
<td align="right">2,322 / 0 !!</td>
<td align="right">2,322</td>
<td align="right">2,322 / 0 !!</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">7,680,783</td>
<td align="right">15.7%</td>
<td align="right">7,031,870</td>
<td align="right">14.8%</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">40,629,051</td>
<td align="right">83.2%</td>
<td align="right">39,915,134</td>
<td align="right">84.1%</td>
<td align="right">-1.8%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">355,467</td>
<td align="right">0.7%</td>
<td align="right">355,707</td>
<td align="right">0.7%</td>
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
<td align="right">517,157</td>
<td align="right">1.1%</td>
<td align="right">517,199</td>
<td align="right">1.1%</td>
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
<td align="right">145,992</td>
<td align="right">96.8%</td>
<td align="right">133,862</td>
<td align="right">96.5%</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">4,893</td>
<td align="right">3.2%</td>
<td align="right">4,914</td>
<td align="right">3.5%</td>
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
<td align="left">mutable class</td>
<td align="right">3,925</td>
<td align="right">80.2%</td>
<td align="right">3,946</td>
<td align="right">80.3%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">758</td>
<td align="right">15.5%</td>
<td align="right">758</td>
<td align="right">15.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">91</td>
<td align="right">1.9%</td>
<td align="right">91</td>
<td align="right">1.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">50</td>
<td align="right">1.0%</td>
<td align="right">50</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">47</td>
<td align="right">1.0%</td>
<td align="right">47</td>
<td align="right">1.0%</td>
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
<td align="right">65,174,381</td>
<td align="right">100.0%</td>
<td align="right">60,432,580</td>
<td align="right">100.0%</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">736</td>
<td align="right">0.0%</td>
<td align="right">736</td>
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
<td align="right">212</td>
<td align="right">0.0%</td>
<td align="right">212</td>
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
<td align="right">820</td>
<td align="right">100.0%</td>
<td align="right">820</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">7</td>
<td align="right">0.0%</td>
<td align="right">7</td>
<td align="right">0.0%</td>
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
<td align="right">3,879,410</td>
<td align="right">100.0%</td>
<td align="right">3,879,410</td>
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
<td align="right">7</td>
<td align="right">100.0%</td>
<td align="right">7</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,566,366</td>
<td align="right">44.5%</td>
<td align="right">1,539,888</td>
<td align="right">43.8%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,950,708</td>
<td align="right">55.5%</td>
<td align="right">1,976,720</td>
<td align="right">56.2%</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">78</td>
<td align="right">0.0%</td>
<td align="right">78</td>
<td align="right">0.0%</td>
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
<td align="right"></td>
<td align="right"></td>
<td align="right">89</td>
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
<td align="right">29,844</td>
<td align="right">100.0%</td>
<td align="right">29,378</td>
<td align="right">100.0%</td>
<td align="right">-1.6%</td>
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
<td align="right">19</td>
<td align="right">0.0%</td>
<td align="right">19</td>
<td align="right">0.0%</td>
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
<td align="right">1,257,086</td>
<td align="right">100.0%</td>
<td align="right">1,257,086</td>
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
<td align="right">19</td>
<td align="right">100.0%</td>
<td align="right">19</td>
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
<td align="right">1,899,306</td>
<td align="right">5.3%</td>
<td align="right">553,864</td>
<td align="right">1.7%</td>
<td align="right">-70.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,591,207</td>
<td align="right">7.2%</td>
<td align="right">2,073,043</td>
<td align="right">6.5%</td>
<td align="right">-20.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">31,458,832</td>
<td align="right">87.5%</td>
<td align="right">29,477,176</td>
<td align="right">91.8%</td>
<td align="right">-6.3%</td>
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
<td align="right">88</td>
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
<td align="right">923</td>
<td align="right">1.8%</td>
<td align="right">627</td>
<td align="right">1.6%</td>
<td align="right">-32.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">49,158</td>
<td align="right">98.2%</td>
<td align="right">39,455</td>
<td align="right">98.4%</td>
<td align="right">-19.7%</td>
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
<td align="right">255</td>
<td align="right">27.6%</td>
<td align="right">85</td>
<td align="right">13.6%</td>
<td align="right">-66.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">268</td>
<td align="right">29.0%</td>
<td align="right">142</td>
<td align="right">22.6%</td>
<td align="right">-47.0%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">347</td>
<td align="right">37.6%</td>
<td align="right">347</td>
<td align="right">55.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">28</td>
<td align="right">3.0%</td>
<td align="right">28</td>
<td align="right">4.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">25</td>
<td align="right">2.7%</td>
<td align="right">25</td>
<td align="right">4.0%</td>
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
<td align="right">12,037</td>
<td align="right">0.1%</td>
<td align="right">12,037</td>
<td align="right">0.1%</td>
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
<td align="right">12,615,193</td>
<td align="right">99.9%</td>
<td align="right">12,615,193</td>
<td align="right">99.9%</td>
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
<td align="right">60</td>
<td align="right">55.6%</td>
<td align="right">60</td>
<td align="right">55.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">48</td>
<td align="right">44.4%</td>
<td align="right">48</td>
<td align="right">44.4%</td>
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
<td align="right">48</td>
<td align="right">100.0%</td>
<td align="right">48</td>
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
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">19,476,682</td>
<td align="right">3.1%</td>
<td align="right">14,021,338</td>
<td align="right">2.7%</td>
<td align="right">-28.0%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">261,627,994</td>
<td align="right">41.8%</td>
<td align="right">214,671,983</td>
<td align="right">41.1%</td>
<td align="right">-17.9%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">332,714,076</td>
<td align="right">53.1%</td>
<td align="right">282,558,989</td>
<td align="right">54.1%</td>
<td align="right">-15.1%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">12,406,602</td>
<td align="right">2.0%</td>
<td align="right">11,214,146</td>
<td align="right">2.1%</td>
<td align="right">-9.6%</td>
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
<td align="right">1,899,306</td>
<td align="right">15.8%</td>
<td align="right">553,864</td>
<td align="right">7.1%</td>
<td align="right">-70.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">8,017,588</td>
<td align="right">66.6%</td>
<td align="right">5,108,505</td>
<td align="right">65.5%</td>
<td align="right">-36.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">161,810</td>
<td align="right">1.3%</td>
<td align="right">171,140</td>
<td align="right">2.2%</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">526,260</td>
<td align="right">4.4%</td>
<td align="right">527,354</td>
<td align="right">6.8%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">517,157</td>
<td align="right">4.3%</td>
<td align="right">517,199</td>
<td align="right">6.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">798,043</td>
<td align="right">6.6%</td>
<td align="right">798,085</td>
<td align="right">10.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">61,985</td>
<td align="right">0.5%</td>
<td align="right">61,985</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">48,891</td>
<td align="right">0.4%</td>
<td align="right">48,891</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">12,037</td>
<td align="right">0.1%</td>
<td align="right">12,037</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">736</td>
<td align="right">0.0%</td>
<td align="right">736</td>
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
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">1,815,047</td>
<td align="right">14.6%</td>
<td align="right">1,311,246</td>
<td align="right">11.7%</td>
<td align="right">-27.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">938,776</td>
<td align="right">7.6%</td>
<td align="right">791,274</td>
<td align="right">7.1%</td>
<td align="right">-15.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">5,460,258</td>
<td align="right">44.0%</td>
<td align="right">4,958,847</td>
<td align="right">44.2%</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">518,073</td>
<td align="right">4.2%</td>
<td align="right">503,773</td>
<td align="right">4.5%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,566,366</td>
<td align="right">12.6%</td>
<td align="right">1,539,888</td>
<td align="right">13.7%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">285,333</td>
<td align="right">2.3%</td>
<td align="right">286,495</td>
<td align="right">2.6%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">1,228,267</td>
<td align="right">9.9%</td>
<td align="right">1,228,267</td>
<td align="right">11.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">243,441</td>
<td align="right">2.0%</td>
<td align="right">243,441</td>
<td align="right">2.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">213,187</td>
<td align="right">1.7%</td>
<td align="right">213,187</td>
<td align="right">1.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">39,469</td>
<td align="right">0.3%</td>
<td align="right">39,469</td>
<td align="right">0.4%</td>
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
<td align="right">4,610,342</td>
<td align="right">11.9%</td>
<td align="right">4,610,342</td>
<td align="right">11.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">34,215,116</td>
<td align="right">88.1%</td>
<td align="right">34,215,116</td>
<td align="right">88.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">4,610,342</td>
<td align="right">11.9%</td>
<td align="right">4,610,342</td>
<td align="right">11.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">3,619,475</td>
<td align="right">9.3%</td>
<td align="right">3,619,475</td>
<td align="right">9.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">990,867</td>
<td align="right">2.6%</td>
<td align="right">990,867</td>
<td align="right">2.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">3,619,475</td>
<td align="right">9.3%</td>
<td align="right">3,619,475</td>
<td align="right">9.3%</td>
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
<td align="right">861,463</td>
<td align="right">2.2%</td>
<td align="right">861,463</td>
<td align="right">2.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">67,661</td>
<td align="right">0.2%</td>
<td align="right">67,661</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">2,581,213</td>
<td align="right">6.6%</td>
<td align="right">2,581,213</td>
<td align="right">6.6%</td>
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
<td align="right">61,662</td>
<td align="right">0.2%</td>
<td align="right">61,662</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">28,167,089</td>
<td align="right">72.5%</td>
<td align="right">28,167,089</td>
<td align="right">72.5%</td>
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
<td align="left">Allocations over 4 kbytes</td>
<td align="right">237</td>
<td align="right">0.0%</td>
<td align="right">368</td>
<td align="right">0.0%</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">156,453,903</td>
<td align="right">31.9%</td>
<td align="right">135,861,991</td>
<td align="right">27.7%</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">201,156,461</td>
<td align="right">41.0%</td>
<td align="right">222,850,282</td>
<td align="right">45.4%</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">22,117</td>
<td align="right"></td>
<td align="right">24,211</td>
<td align="right"></td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">204,372,638</td>
<td align="right">37.1%</td>
<td align="right">185,150,901</td>
<td align="right">33.6%</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">219,728,700</td>
<td align="right">39.8%</td>
<td align="right">240,052,302</td>
<td align="right">43.5%</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">10,056,747</td>
<td align="right"></td>
<td align="right">9,368,386</td>
<td align="right"></td>
<td align="right">-6.8%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">10,582,198</td>
<td align="right">2.2%</td>
<td align="right">11,015,084</td>
<td align="right">2.2%</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">519,966</td>
<td align="right"></td>
<td align="right">509,911</td>
<td align="right"></td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">541,627</td>
<td align="right"></td>
<td align="right">533,747</td>
<td align="right"></td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">122,141,375</td>
<td align="right">24.9%</td>
<td align="right">120,852,950</td>
<td align="right">24.6%</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">120,114,217</td>
<td align="right">21.8%</td>
<td align="right">119,255,493</td>
<td align="right">21.6%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">49,784,242</td>
<td align="right"></td>
<td align="right">49,496,805</td>
<td align="right"></td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">61,084</td>
<td align="right">0.1%</td>
<td align="right">61,041</td>
<td align="right">0.1%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">7,196,482</td>
<td align="right">1.3%</td>
<td align="right">7,199,878</td>
<td align="right">1.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">26,939,733</td>
<td align="right">36.5%</td>
<td align="right">26,939,688</td>
<td align="right">36.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">27,001,054</td>
<td align="right">36.6%</td>
<td align="right">27,001,097</td>
<td align="right">36.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">29,226,388</td>
<td align="right"></td>
<td align="right">29,226,371</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">46,753,427</td>
<td align="right"></td>
<td align="right">46,753,431</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">46,758,164</td>
<td align="right">63.4%</td>
<td align="right">46,758,168</td>
<td align="right">63.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">122,421</td>
<td align="right"></td>
<td align="right">122,421</td>
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
<td align="right">130</td>
<td align="right">167,082</td>
<td align="right">1,447,928</td>
<td align="right">90,951</td>
<td align="right">200,117</td>
<td align="right">130</td>
<td align="right">167,082</td>
<td align="right">1,440,161</td>
<td align="right">97,595</td>
<td align="right">193,509</td>
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
<td align="right">3,364</td>
<td align="right"></td>
<td align="right">1,148,983</td>
<td align="right"></td>
<td align="right">34,055.3%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">1,797</td>
<td align="right">53.4%</td>
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
<td align="right">1</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Recursive call
<details>
<summary>ⓘ</summary>

A trace is truncated because it has a recursive call.
</details>
</td>
<td align="right">45</td>
<td align="right">1.3%</td>
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
<td align="right">1</td>
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
<td align="right">1,068</td>
<td align="right">31.7%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">391,713,551</td>
<td align="right">1,747.9%</td>
<td align="right">660,979,490</td>
<td align="right">2,565.7%</td>
<td align="right">68.7%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">22,411,103</td>
<td align="right"></td>
<td align="right">25,761,977</td>
<td align="right"></td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">499</td>
<td align="right">14.8%</td>
<td align="right">524</td>
<td align="right">0.0%</td>
<td align="right">5.0%</td>
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
<td align="right">21</td>
<td align="right">0.0%</td>
<td align="right">21 / 0 !!</td>
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
<td align="right">499</td>
<td align="right"></td>
<td align="right">524</td>
<td align="right"></td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">
Optimizer successes
<details>
<summary>ⓘ</summary>

The number of traces that were successfully optimized.
</details>
</td>
<td align="right">499</td>
<td align="right">100.0%</td>
<td align="right">524</td>
<td align="right">100.0%</td>
<td align="right">5.0%</td>
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
<td align="right">3,361,998</td>
<td align="right">75.5%</td>
<td align="right">8,306,381</td>
<td align="right">87.1%</td>
<td align="right">147.1%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">4,452,352</td>
<td align="right"></td>
<td align="right">9,535,488</td>
<td align="right"></td>
<td align="right">114.2%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">72,672</td>
<td align="right">1.6%</td>
<td align="right">144,688</td>
<td align="right">1.5%</td>
<td align="right">99.1%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">1,017,182</td>
<td align="right">22.8%</td>
<td align="right">1,083,895</td>
<td align="right">11.4%</td>
<td align="right">6.6%</td>
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
<td align="left">303</td>
<td align="right">60.6%</td>
<td align="left">174</td>
<td align="right">33.2%</td>
<td align="right">-42.6%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">88</td>
<td align="right">17.6%</td>
<td align="left">109</td>
<td align="right">20.8%</td>
<td align="right">23.9%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">24</td>
<td align="right">4.8%</td>
<td align="left">89</td>
<td align="right">17.0%</td>
<td align="right">270.8%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">84</td>
<td align="right">16.8%</td>
<td align="left">107</td>
<td align="right">20.4%</td>
<td align="right">27.4%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left">1</td>
<td align="right">0.2%</td>
<td align="left">3</td>
<td align="right">0.6%</td>
<td align="right">200.0%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">42</td>
<td align="right">8.0%</td>
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
<td align="right">66</td>
<td align="right">13.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">105</td>
<td align="right">21.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">65</td>
<td align="right">13.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">90</td>
<td align="right">18.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">64</td>
<td align="right">12.8%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">3</td>
<td align="right">0.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">106</td>
<td align="right">21.2%</td>
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
<td align="right">21</td>
<td align="right">4.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">45</td>
<td align="right">9.0%</td>
<td align="right">3</td>
<td align="right">0.6%</td>
<td align="right">-93.3%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">127</td>
<td align="right">25.5%</td>
<td align="right">108</td>
<td align="right">20.6%</td>
<td align="right">-15.0%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">110</td>
<td align="right">22.0%</td>
<td align="right">63</td>
<td align="right">12.0%</td>
<td align="right">-42.7%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">87</td>
<td align="right">17.4%</td>
<td align="right">109</td>
<td align="right">20.8%</td>
<td align="right">25.3%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">24</td>
<td align="right">4.8%</td>
<td align="right">89</td>
<td align="right">17.0%</td>
<td align="right">270.8%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">84</td>
<td align="right">16.8%</td>
<td align="right">107</td>
<td align="right">20.4%</td>
<td align="right">27.4%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">1</td>
<td align="right">0.2%</td>
<td align="right">24</td>
<td align="right">4.6%</td>
<td align="right">2,300.0%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">21</td>
<td align="right">4.0%</td>
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
<td align="left">_LOAD_FAST_2</td>
<td align="right">25,856</td>
<td align="right">1,157,942</td>
<td align="right">4,378.4%</td>
</tr>
<tr>
<td align="left">_PY_FRAME_GENERAL</td>
<td align="right">16,170</td>
<td align="right">565,242</td>
<td align="right">3,395.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">42,445</td>
<td align="right">1,387,887</td>
<td align="right">3,169.8%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">445,237</td>
<td align="right">13,365,134</td>
<td align="right">2,901.8%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">102,964</td>
<td align="right">1,465,786</td>
<td align="right">1,323.6%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">612,325</td>
<td align="right">6,797,276</td>
<td align="right">1,010.1%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">525,756</td>
<td align="right">4,583,509</td>
<td align="right">771.8%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right">16,170</td>
<td align="right">134,499</td>
<td align="right">731.8%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">16,170</td>
<td align="right">134,499</td>
<td align="right">731.8%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right">449,298</td>
<td align="right">3,172,921</td>
<td align="right">606.2%</td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right">449,298</td>
<td align="right">3,172,921</td>
<td align="right">606.2%</td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right">592,764</td>
<td align="right">3,400,232</td>
<td align="right">473.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">781,592</td>
<td align="right">3,260,033</td>
<td align="right">317.1%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right">1,863,426</td>
<td align="right">7,729,544</td>
<td align="right">314.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right">406,432</td>
<td align="right">1,638,443</td>
<td align="right">303.1%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">206,138</td>
<td align="right">820,459</td>
<td align="right">298.0%</td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right">304,640</td>
<td align="right">1,195,228</td>
<td align="right">292.3%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">562,759</td>
<td align="right">1,911,517</td>
<td align="right">239.7%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">178,460</td>
<td align="right">594,464</td>
<td align="right">233.1%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">178,460</td>
<td align="right">594,464</td>
<td align="right">233.1%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">6,353</td>
<td align="right">21,122</td>
<td align="right">232.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">2,170,562</td>
<td align="right">6,599,995</td>
<td align="right">204.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">1,460,031</td>
<td align="right">4,318,706</td>
<td align="right">195.8%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">4,231,022</td>
<td align="right">12,066,331</td>
<td align="right">185.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">956,864</td>
<td align="right">2,717,126</td>
<td align="right">184.0%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">1,734,563</td>
<td align="right">4,778,164</td>
<td align="right">175.5%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">1,211,941</td>
<td align="right">3,326,286</td>
<td align="right">174.5%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">304,809</td>
<td align="right">798,524</td>
<td align="right">162.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">567,849</td>
<td align="right">1,466,783</td>
<td align="right">158.3%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">817,026</td>
<td align="right">2,070,675</td>
<td align="right">153.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">1,137,384</td>
<td align="right">2,757,444</td>
<td align="right">142.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">1,614,810</td>
<td align="right">3,692,294</td>
<td align="right">128.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,614,810</td>
<td align="right">3,475,476</td>
<td align="right">115.2%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">841,568</td>
<td align="right">1,716,341</td>
<td align="right">103.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">360,942</td>
<td align="right">721,233</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">4,930,996</td>
<td align="right">9,546,315</td>
<td align="right">93.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">3,841,307</td>
<td align="right">7,417,409</td>
<td align="right">93.1%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">283,834</td>
<td align="right">21,199</td>
<td align="right">-92.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">283,834</td>
<td align="right">21,199</td>
<td align="right">-92.5%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">4,149,963</td>
<td align="right">7,790,958</td>
<td align="right">87.7%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">1,924,890</td>
<td align="right">283,851</td>
<td align="right">-85.3%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">7,682,653</td>
<td align="right">14,006,423</td>
<td align="right">82.3%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">52,104,065</td>
<td align="right">92,787,740</td>
<td align="right">78.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">1,149,229</td>
<td align="right">2,033,515</td>
<td align="right">76.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">229,017</td>
<td align="right">401,487</td>
<td align="right">75.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">717,556</td>
<td align="right">1,234,714</td>
<td align="right">72.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">1,479,259</td>
<td align="right">2,501,646</td>
<td align="right">69.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">7,768,714</td>
<td align="right">12,965,558</td>
<td align="right">66.9%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">72,359,367</td>
<td align="right">119,353,471</td>
<td align="right">64.9%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">1,873,212</td>
<td align="right">3,083,314</td>
<td align="right">64.6%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">1,096,444</td>
<td align="right">1,799,370</td>
<td align="right">64.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">1,252,314</td>
<td align="right">460,951</td>
<td align="right">-63.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">486,101</td>
<td align="right">182,892</td>
<td align="right">-62.4%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">7,876,269</td>
<td align="right">12,660,851</td>
<td align="right">60.7%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">444,186</td>
<td align="right">178,066</td>
<td align="right">-59.9%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">16,170</td>
<td align="right">25,566</td>
<td align="right">58.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right">558,952</td>
<td align="right">237,400</td>
<td align="right">-57.5%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">558,952</td>
<td align="right">237,400</td>
<td align="right">-57.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">968,480</td>
<td align="right">439,752</td>
<td align="right">-54.6%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">326,103</td>
<td align="right">500,928</td>
<td align="right">53.6%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">32,340</td>
<td align="right">48,824</td>
<td align="right">51.0%</td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right">3,871,380</td>
<td align="right">1,969,065</td>
<td align="right">-49.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">1,326,565</td>
<td align="right">1,970,469</td>
<td align="right">48.5%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">3,841,307</td>
<td align="right">5,641,913</td>
<td align="right">46.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">2,982,384</td>
<td align="right">4,367,807</td>
<td align="right">46.5%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">748,995</td>
<td align="right">1,084,997</td>
<td align="right">44.9%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">11,961,446</td>
<td align="right">17,299,138</td>
<td align="right">44.6%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right">296,382</td>
<td align="right">420,259</td>
<td align="right">41.8%</td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right">3,414,568</td>
<td align="right">4,819,027</td>
<td align="right">41.1%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">7,432,765</td>
<td align="right">10,341,848</td>
<td align="right">39.1%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">1,927,535</td>
<td align="right">2,668,351</td>
<td align="right">38.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">7,954,774</td>
<td align="right">10,788,846</td>
<td align="right">35.6%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">4,231,022</td>
<td align="right">5,700,825</td>
<td align="right">34.7%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">4,231,022</td>
<td align="right">5,691,387</td>
<td align="right">34.5%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">283,834</td>
<td align="right">379,764</td>
<td align="right">33.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,918,173</td>
<td align="right">2,530,376</td>
<td align="right">31.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">1,907,186</td>
<td align="right">2,510,061</td>
<td align="right">31.6%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">16,522,454</td>
<td align="right">21,641,603</td>
<td align="right">31.0%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">5,888,649</td>
<td align="right">4,120,374</td>
<td align="right">-30.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">471,312</td>
<td align="right">603,199</td>
<td align="right">28.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">2,830,231</td>
<td align="right">3,616,408</td>
<td align="right">27.8%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">2,351,628</td>
<td align="right">2,967,068</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">64,680</td>
<td align="right">81,080</td>
<td align="right">25.4%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">11,502,372</td>
<td align="right">14,386,534</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">1,817,816</td>
<td align="right">2,222,099</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">13,370,528</td>
<td align="right">16,340,632</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">8,488,727</td>
<td align="right">10,224,875</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">5,961,256</td>
<td align="right">4,762,385</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">5,961,256</td>
<td align="right">4,762,385</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">18,447,344</td>
<td align="right">21,925,454</td>
<td align="right">18.9%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">148,454</td>
<td align="right">120,957</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">148,454</td>
<td align="right">120,957</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">50,557</td>
<td align="right">41,227</td>
<td align="right">-18.5%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">103,624</td>
<td align="right">121,996</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">149,228</td>
<td align="right">123,775</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right">3,482,027</td>
<td align="right">4,057,276</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">1,578,417</td>
<td align="right">1,320,444</td>
<td align="right">-16.3%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">3,516,967</td>
<td align="right">4,076,888</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">1,738,993</td>
<td align="right">1,997,135</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">468,868</td>
<td align="right">413,566</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">3,186,000</td>
<td align="right">3,536,568</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">919,802</td>
<td align="right">835,715</td>
<td align="right">-9.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">581,380</td>
<td align="right">566,732</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">16,522,453</td>
<td align="right">16,577,296</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">13,923</td>
<td align="right">13,881</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">80,850</td>
<td align="right">80,640</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">32,340</td>
<td align="right">32,256</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">32,340</td>
<td align="right">32,256</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right">32,340</td>
<td align="right">32,256</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right">32,340</td>
<td align="right">32,256</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">16,170</td>
<td align="right">16,128</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">16,170</td>
<td align="right">16,128</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right">16,170</td>
<td align="right">16,128</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">1,584,429</td>
<td align="right">1,584,428</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">4,052,562</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right">1</td>
<td align="right">1</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">20,546,473</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">5,064,306</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">4,129,605</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">3,300,855</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SEND_GEN_FRAME</td>
<td align="right"></td>
<td align="right">2,235,901</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right"></td>
<td align="right">1,775,496</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right"></td>
<td align="right">1,209,517</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right"></td>
<td align="right">742,685</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right"></td>
<td align="right">474,662</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right"></td>
<td align="right">379,579</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right"></td>
<td align="right">360,260</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right"></td>
<td align="right">360,260</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">349,886</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_SEND</td>
<td align="right"></td>
<td align="right">277,815</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right"></td>
<td align="right">234,204</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_FOR</td>
<td align="right"></td>
<td align="right">17,068</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right"></td>
<td align="right">16,568</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_OVERFLOWED</td>
<td align="right"></td>
<td align="right">16,568</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_EX</td>
<td align="right"></td>
<td align="right">14,642</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right"></td>
<td align="right">14,642</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">14,642</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_PROPERTY_FRAME</td>
<td align="right"></td>
<td align="right">9,438</td>
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
<td align="right">21</td>
<td align="right">21</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-10-22
