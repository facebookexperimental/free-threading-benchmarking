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
<td align="right">1,078,014</td>
<td align="right">91.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">2,346,119</td>
<td align="right">570,621</td>
<td align="right">-75.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">5,808,336</td>
<td align="right">1,676,310</td>
<td align="right">-71.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,900,665</td>
<td align="right">590,440</td>
<td align="right">-68.9%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">9,223,509</td>
<td align="right">3,770,049</td>
<td align="right">-59.1%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">5,888,064</td>
<td align="right">9,065,222</td>
<td align="right">54.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">698,134</td>
<td align="right">1,019,685</td>
<td align="right">46.1%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">775,935</td>
<td align="right">420,532</td>
<td align="right">-45.8%</td>
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
<td align="right">471,428</td>
<td align="right">-43.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">14,408,577</td>
<td align="right">8,427,401</td>
<td align="right">-41.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">565,860</td>
<td align="right">332,634</td>
<td align="right">-41.2%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">3,879,410</td>
<td align="right">2,280,821</td>
<td align="right">-41.2%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">8,086,107</td>
<td align="right">4,797,122</td>
<td align="right">-40.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">3,048,915</td>
<td align="right">1,809,400</td>
<td align="right">-40.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">8,020,863</td>
<td align="right">5,089,654</td>
<td align="right">-36.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">3,313,912</td>
<td align="right">4,491,996</td>
<td align="right">35.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">7,452,966</td>
<td align="right">4,842,140</td>
<td align="right">-35.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">2,077,810</td>
<td align="right">1,412,835</td>
<td align="right">-32.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">8,074,913</td>
<td align="right">5,493,905</td>
<td align="right">-32.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">830,502</td>
<td align="right">576,863</td>
<td align="right">-30.5%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">10,272,629</td>
<td align="right">7,170,896</td>
<td align="right">-30.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">1,570,013</td>
<td align="right">1,111,810</td>
<td align="right">-29.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">9,624,831</td>
<td align="right">6,854,965</td>
<td align="right">-28.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">6,427,767</td>
<td align="right">4,605,587</td>
<td align="right">-28.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">2,483,229</td>
<td align="right">1,791,543</td>
<td align="right">-27.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">15,181,396</td>
<td align="right">11,075,578</td>
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
<td align="right">1,543,672</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">3,207,532</td>
<td align="right">2,490,653</td>
<td align="right">-22.3%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">21,969,436</td>
<td align="right">17,195,275</td>
<td align="right">-21.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">32,180,063</td>
<td align="right">25,360,837</td>
<td align="right">-21.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">23,788,856</td>
<td align="right">19,165,910</td>
<td align="right">-19.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">7,350,164</td>
<td align="right">5,966,250</td>
<td align="right">-18.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">42,520,715</td>
<td align="right">34,560,200</td>
<td align="right">-18.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">26,921,578</td>
<td align="right">22,059,491</td>
<td align="right">-18.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">5,034,025</td>
<td align="right">4,149,536</td>
<td align="right">-17.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">3,511,514</td>
<td align="right">2,921,348</td>
<td align="right">-16.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,499,398</td>
<td align="right">2,081,897</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">30,251,094</td>
<td align="right">25,350,454</td>
<td align="right">-16.2%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">7,942,592</td>
<td align="right">6,690,653</td>
<td align="right">-15.8%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">4,549,550</td>
<td align="right">3,909,036</td>
<td align="right">-14.1%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">2,592,513</td>
<td align="right">2,233,439</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">86,761,005</td>
<td align="right">74,983,871</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">138,914</td>
<td align="right">122,346</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">129,468</td>
<td align="right">114,242</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">2,241,671</td>
<td align="right">1,980,515</td>
<td align="right">-11.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">15,156,854</td>
<td align="right">13,403,892</td>
<td align="right">-11.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">1,177,790</td>
<td align="right">1,044,193</td>
<td align="right">-11.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">3,915,310</td>
<td align="right">3,495,075</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">21,311,096</td>
<td align="right">19,181,637</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">481,573</td>
<td align="right">434,553</td>
<td align="right">-9.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,015,951</td>
<td align="right">920,019</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">332,211</td>
<td align="right">301,759</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">15,306,371</td>
<td align="right">14,142,041</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">412,827</td>
<td align="right">382,375</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">218,086</td>
<td align="right">202,860</td>
<td align="right">-7.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">14,739,716</td>
<td align="right">13,808,475</td>
<td align="right">-6.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">162,292</td>
<td align="right">171,622</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">234,909</td>
<td align="right">221,453</td>
<td align="right">-5.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">24,752,521</td>
<td align="right">23,379,939</td>
<td align="right">-5.5%</td>
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
<td align="right">12,563,984</td>
<td align="right">-4.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">3,279,189</td>
<td align="right">3,168,743</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">523,312</td>
<td align="right">510,130</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">1,159,026</td>
<td align="right">1,184,479</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">655,778</td>
<td align="right">642,320</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">798,296</td>
<td align="right">783,070</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">799,514</td>
<td align="right">786,332</td>
<td align="right">-1.6%</td>
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
<td align="right">2,191,447</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">4,173,860</td>
<td align="right">4,149,196</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">5,455,707</td>
<td align="right">5,425,255</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">6,885,343</td>
<td align="right">6,913,395</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">2,781,570</td>
<td align="right">2,772,132</td>
<td align="right">-0.3%</td>
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
<td align="right">536,639</td>
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
<td align="right">527,400</td>
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
<td align="right">784,797</td>
<td align="right">47.5%</td>
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
<td align="right">867,098</td>
<td align="right">52.0%</td>
<td align="right">867,098</td>
<td align="right">52.4%</td>
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
<td align="right">1,495</td>
<td align="right">97.4%</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">40</td>
<td align="right">2.7%</td>
<td align="right">40</td>
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
<td align="left">baseobject</td>
<td align="right">662</td>
<td align="right">46.3%</td>
<td align="right">726</td>
<td align="right">48.6%</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">497</td>
<td align="right">34.7%</td>
<td align="right">497</td>
<td align="right">33.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">81</td>
<td align="right">5.7%</td>
<td align="right">81</td>
<td align="right">5.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">51</td>
<td align="right">3.6%</td>
<td align="right">51</td>
<td align="right">3.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">50</td>
<td align="right">3.5%</td>
<td align="right">50</td>
<td align="right">3.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">46</td>
<td align="right">3.2%</td>
<td align="right">46</td>
<td align="right">3.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">44</td>
<td align="right">3.1%</td>
<td align="right">44</td>
<td align="right">2.9%</td>
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
<td align="right">171,119</td>
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
<td align="right">5,086,846</td>
<td align="right">32.8%</td>
<td align="right">-36.6%</td>
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
<td align="right">10,403,073</td>
<td align="right">67.1%</td>
<td align="right">12.8%</td>
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
<td align="right">2,721</td>
<td align="right">96.9%</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">87</td>
<td align="right">2.7%</td>
<td align="right">87</td>
<td align="right">3.1%</td>
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
<td align="right">52</td>
<td align="right">1.6%</td>
<td align="right">115</td>
<td align="right">4.2%</td>
<td align="right">121.2%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">2,109</td>
<td align="right">66.2%</td>
<td align="right">1,517</td>
<td align="right">55.8%</td>
<td align="right">-28.1%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">83</td>
<td align="right">2.6%</td>
<td align="right">104</td>
<td align="right">3.8%</td>
<td align="right">25.3%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">287</td>
<td align="right">9.0%</td>
<td align="right">328</td>
<td align="right">12.1%</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">187</td>
<td align="right">5.9%</td>
<td align="right">187</td>
<td align="right">6.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">183</td>
<td align="right">5.7%</td>
<td align="right">183</td>
<td align="right">6.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">147</td>
<td align="right">4.6%</td>
<td align="right">147</td>
<td align="right">5.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">90</td>
<td align="right">2.8%</td>
<td align="right">90</td>
<td align="right">3.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">50</td>
<td align="right">1.6%</td>
<td align="right">50</td>
<td align="right">1.8%</td>
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
<td align="right">7,025,179</td>
<td align="right">14.8%</td>
<td align="right">-8.5%</td>
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
<td align="right">503,911</td>
<td align="right">1.1%</td>
<td align="right">-2.6%</td>
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
<td align="right">39,823,467</td>
<td align="right">84.1%</td>
<td align="right">-2.0%</td>
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
<td align="right">355,687</td>
<td align="right">0.8%</td>
<td align="right">0.1%</td>
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
<td align="right">133,760</td>
<td align="right">96.4%</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">4,893</td>
<td align="right">3.2%</td>
<td align="right">4,957</td>
<td align="right">3.6%</td>
<td align="right">1.3%</td>
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
<td align="right">3,989</td>
<td align="right">80.5%</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">758</td>
<td align="right">15.5%</td>
<td align="right">758</td>
<td align="right">15.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">91</td>
<td align="right">1.9%</td>
<td align="right">91</td>
<td align="right">1.8%</td>
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
<td align="right">0.9%</td>
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
<td align="right">60,359,593</td>
<td align="right">100.0%</td>
<td align="right">-7.4%</td>
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
<td align="right">589,376</td>
<td align="right">1.8%</td>
<td align="right">-69.0%</td>
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
<td align="right">2,067,786</td>
<td align="right">6.4%</td>
<td align="right">-20.2%</td>
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
<td align="right">29,608,961</td>
<td align="right">91.8%</td>
<td align="right">-5.9%</td>
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
<td align="right">69</td>
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
<td align="right">628</td>
<td align="right">1.6%</td>
<td align="right">-32.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">49,158</td>
<td align="right">98.2%</td>
<td align="right">39,355</td>
<td align="right">98.4%</td>
<td align="right">-19.9%</td>
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
<td align="right">13.5%</td>
<td align="right">-66.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">268</td>
<td align="right">29.0%</td>
<td align="right">143</td>
<td align="right">22.8%</td>
<td align="right">-46.6%</td>
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
<td align="right">13,966,275</td>
<td align="right">2.7%</td>
<td align="right">-28.3%</td>
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
<td align="right">215,183,294</td>
<td align="right">41.1%</td>
<td align="right">-17.8%</td>
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
<td align="right">282,627,356</td>
<td align="right">54.0%</td>
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
<td align="right">11,202,244</td>
<td align="right">2.1%</td>
<td align="right">-9.7%</td>
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
<td align="right">589,376</td>
<td align="right">7.6%</td>
<td align="right">-69.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">8,017,588</td>
<td align="right">66.6%</td>
<td align="right">5,086,846</td>
<td align="right">65.3%</td>
<td align="right">-36.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">161,810</td>
<td align="right">1.3%</td>
<td align="right">171,119</td>
<td align="right">2.2%</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">517,157</td>
<td align="right">4.3%</td>
<td align="right">503,911</td>
<td align="right">6.5%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">798,043</td>
<td align="right">6.6%</td>
<td align="right">784,797</td>
<td align="right">10.1%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">526,260</td>
<td align="right">4.4%</td>
<td align="right">527,400</td>
<td align="right">6.8%</td>
<td align="right">0.2%</td>
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
<td align="right">1,306,710</td>
<td align="right">11.7%</td>
<td align="right">-28.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">938,776</td>
<td align="right">7.6%</td>
<td align="right">795,093</td>
<td align="right">7.1%</td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">5,460,258</td>
<td align="right">44.0%</td>
<td align="right">4,948,337</td>
<td align="right">44.2%</td>
<td align="right">-9.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">518,073</td>
<td align="right">4.2%</td>
<td align="right">503,052</td>
<td align="right">4.5%</td>
<td align="right">-2.9%</td>
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
<td align="left">Method cache dunder misses</td>
<td align="right">20,905</td>
<td align="right"></td>
<td align="right">24,759</td>
<td align="right"></td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">156,453,903</td>
<td align="right">31.9%</td>
<td align="right">135,736,301</td>
<td align="right">27.7%</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">201,153,200</td>
<td align="right">41.0%</td>
<td align="right">223,033,294</td>
<td align="right">45.5%</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">204,372,638</td>
<td align="right">37.1%</td>
<td align="right">184,874,060</td>
<td align="right">33.5%</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">219,725,478</td>
<td align="right">39.8%</td>
<td align="right">240,386,480</td>
<td align="right">43.6%</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">10,060,267</td>
<td align="right"></td>
<td align="right">9,362,830</td>
<td align="right"></td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">10,582,198</td>
<td align="right">2.2%</td>
<td align="right">10,928,753</td>
<td align="right">2.2%</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">7,196,482</td>
<td align="right">1.3%</td>
<td align="right">7,100,260</td>
<td align="right">1.3%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">516,446</td>
<td align="right"></td>
<td align="right">511,046</td>
<td align="right"></td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">122,135,173</td>
<td align="right">24.9%</td>
<td align="right">120,924,169</td>
<td align="right">24.6%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">120,107,977</td>
<td align="right">21.8%</td>
<td align="right">119,341,076</td>
<td align="right">21.6%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">49,785,454</td>
<td align="right"></td>
<td align="right">49,487,979</td>
<td align="right"></td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">536,837</td>
<td align="right"></td>
<td align="right">535,279</td>
<td align="right"></td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">61,084</td>
<td align="right">0.1%</td>
<td align="right">61,147</td>
<td align="right">0.1%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">27,001,054</td>
<td align="right">36.6%</td>
<td align="right">27,001,269</td>
<td align="right">36.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">29,226,425</td>
<td align="right"></td>
<td align="right">29,226,477</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">46,753,427</td>
<td align="right"></td>
<td align="right">46,753,386</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">46,758,164</td>
<td align="right">63.4%</td>
<td align="right">46,758,123</td>
<td align="right">63.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">26,939,733</td>
<td align="right">36.5%</td>
<td align="right">26,939,754</td>
<td align="right">36.5%</td>
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
<td align="right">1,447,922</td>
<td align="right">90,953</td>
<td align="right">200,115</td>
<td align="right">130</td>
<td align="right">167,158</td>
<td align="right">1,457,452</td>
<td align="right">90,080</td>
<td align="right">200,964</td>
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
<td align="right">1,184,878</td>
<td align="right"></td>
<td align="right">35,122.3%</td>
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
<td align="right">136</td>
<td align="right">0.0%</td>
<td align="right">13,500.0%</td>
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
<td align="right">662,955,946</td>
<td align="right">2,672.2%</td>
<td align="right">69.2%</td>
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
<td align="right">630</td>
<td align="right">0.1%</td>
<td align="right">26.3%</td>
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
<td align="right">24,809,432</td>
<td align="right"></td>
<td align="right">10.7%</td>
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
<td align="right">630</td>
<td align="right"></td>
<td align="right">26.3%</td>
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
<td align="right">630</td>
<td align="right">100.0%</td>
<td align="right">26.3%</td>
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
<td align="right">6,413,688</td>
<td align="right">81.6%</td>
<td align="right">90.8%</td>
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
<td align="right">7,856,128</td>
<td align="right"></td>
<td align="right">76.4%</td>
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
<td align="right">126,696</td>
<td align="right">1.6%</td>
<td align="right">74.3%</td>
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
<td align="right">1,315,114</td>
<td align="right">16.7%</td>
<td align="right">29.3%</td>
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
<td align="left">259</td>
<td align="right">41.1%</td>
<td align="right">-14.5%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">88</td>
<td align="right">17.6%</td>
<td align="left">109</td>
<td align="right">17.3%</td>
<td align="right">23.9%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">24</td>
<td align="right">4.8%</td>
<td align="left">107</td>
<td align="right">17.0%</td>
<td align="right">345.8%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">84</td>
<td align="right">16.8%</td>
<td align="left">152</td>
<td align="right">24.1%</td>
<td align="right">81.0%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left">1</td>
<td align="right">0.2%</td>
<td align="left">3</td>
<td align="right">0.5%</td>
<td align="right">200.0%</td>
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
<td align="right">24</td>
<td align="right">3.8%</td>
<td align="right">-46.7%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">127</td>
<td align="right">25.5%</td>
<td align="right">151</td>
<td align="right">24.0%</td>
<td align="right">18.9%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">110</td>
<td align="right">22.0%</td>
<td align="right">84</td>
<td align="right">13.3%</td>
<td align="right">-23.6%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">87</td>
<td align="right">17.4%</td>
<td align="right">109</td>
<td align="right">17.3%</td>
<td align="right">25.3%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">24</td>
<td align="right">4.8%</td>
<td align="right">108</td>
<td align="right">17.1%</td>
<td align="right">350.0%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">84</td>
<td align="right">16.8%</td>
<td align="right">151</td>
<td align="right">24.0%</td>
<td align="right">79.8%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">1</td>
<td align="right">0.2%</td>
<td align="right">3</td>
<td align="right">0.5%</td>
<td align="right">200.0%</td>
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
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right">1</td>
<td align="right">42</td>
<td align="right">4,100.0%</td>
</tr>
<tr>
<td align="left">_PY_FRAME_GENERAL</td>
<td align="right">16,170</td>
<td align="right">544,998</td>
<td align="right">3,270.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">42,445</td>
<td align="right">1,352,375</td>
<td align="right">3,086.2%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">445,237</td>
<td align="right">12,958,851</td>
<td align="right">2,810.6%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">102,964</td>
<td align="right">1,486,878</td>
<td align="right">1,344.1%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">612,325</td>
<td align="right">6,576,719</td>
<td align="right">974.1%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right">16,170</td>
<td align="right">149,767</td>
<td align="right">826.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">16,170</td>
<td align="right">149,767</td>
<td align="right">826.2%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">525,756</td>
<td align="right">4,649,020</td>
<td align="right">784.3%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right">449,298</td>
<td align="right">3,293,026</td>
<td align="right">632.9%</td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right">449,298</td>
<td align="right">3,293,026</td>
<td align="right">632.9%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right">406,432</td>
<td align="right">1,870,476</td>
<td align="right">360.2%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right">1,863,426</td>
<td align="right">7,786,099</td>
<td align="right">317.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">781,592</td>
<td align="right">3,241,425</td>
<td align="right">314.7%</td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right">304,640</td>
<td align="right">1,189,129</td>
<td align="right">290.3%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">206,138</td>
<td align="right">796,304</td>
<td align="right">286.3%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">562,759</td>
<td align="right">2,000,454</td>
<td align="right">255.5%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">178,460</td>
<td align="right">593,278</td>
<td align="right">232.4%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">178,460</td>
<td align="right">593,278</td>
<td align="right">232.4%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">6,353</td>
<td align="right">19,936</td>
<td align="right">213.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">2,170,562</td>
<td align="right">6,578,075</td>
<td align="right">203.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">1,460,031</td>
<td align="right">4,410,261</td>
<td align="right">202.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">1,211,941</td>
<td align="right">3,537,586</td>
<td align="right">191.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">956,864</td>
<td align="right">2,717,630</td>
<td align="right">184.0%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">1,734,563</td>
<td align="right">4,836,296</td>
<td align="right">178.8%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">4,231,022</td>
<td align="right">11,431,166</td>
<td align="right">170.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">567,849</td>
<td align="right">1,450,765</td>
<td align="right">155.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">16,170</td>
<td align="right">40,834</td>
<td align="right">152.5%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">304,809</td>
<td align="right">763,012</td>
<td align="right">150.3%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">32,340</td>
<td align="right">79,360</td>
<td align="right">145.4%</td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right">592,764</td>
<td align="right">1,454,263</td>
<td align="right">145.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">1,137,384</td>
<td align="right">2,741,406</td>
<td align="right">141.0%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">817,026</td>
<td align="right">1,968,948</td>
<td align="right">141.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">1,614,810</td>
<td align="right">3,675,238</td>
<td align="right">127.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">64,680</td>
<td align="right">142,152</td>
<td align="right">119.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,614,810</td>
<td align="right">3,473,104</td>
<td align="right">115.1%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">103,624</td>
<td align="right">213,604</td>
<td align="right">106.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">360,942</td>
<td align="right">742,327</td>
<td align="right">105.7%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">841,568</td>
<td align="right">1,661,841</td>
<td align="right">97.5%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">13,923</td>
<td align="right">27,169</td>
<td align="right">95.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">4,930,996</td>
<td align="right">9,597,059</td>
<td align="right">94.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">80,850</td>
<td align="right">156,980</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">32,340</td>
<td align="right">62,792</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">32,340</td>
<td align="right">62,792</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right">32,340</td>
<td align="right">62,792</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right">32,340</td>
<td align="right">62,792</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">16,170</td>
<td align="right">31,396</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">16,170</td>
<td align="right">31,396</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right">16,170</td>
<td align="right">31,396</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">3,841,307</td>
<td align="right">7,438,985</td>
<td align="right">93.7%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">283,834</td>
<td align="right">21,201</td>
<td align="right">-92.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">283,834</td>
<td align="right">21,201</td>
<td align="right">-92.5%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">7,682,653</td>
<td align="right">14,021,509</td>
<td align="right">82.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">717,556</td>
<td align="right">1,270,331</td>
<td align="right">77.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">4,149,963</td>
<td align="right">7,286,136</td>
<td align="right">75.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">1,149,229</td>
<td align="right">2,017,497</td>
<td align="right">75.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">444,186</td>
<td align="right">110,836</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">52,104,065</td>
<td align="right">91,151,362</td>
<td align="right">74.9%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">229,017</td>
<td align="right">400,322</td>
<td align="right">74.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">1,479,259</td>
<td align="right">2,572,881</td>
<td align="right">73.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">1,096,444</td>
<td align="right">1,893,389</td>
<td align="right">72.7%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">11,961,446</td>
<td align="right">20,628,213</td>
<td align="right">72.5%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">326,103</td>
<td align="right">559,329</td>
<td align="right">71.5%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">72,359,367</td>
<td align="right">121,931,729</td>
<td align="right">68.5%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">1,873,212</td>
<td align="right">3,125,151</td>
<td align="right">66.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">7,768,714</td>
<td align="right">12,935,582</td>
<td align="right">66.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">1,252,314</td>
<td align="right">460,953</td>
<td align="right">-63.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">486,101</td>
<td align="right">190,084</td>
<td align="right">-60.9%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">7,876,269</td>
<td align="right">12,650,430</td>
<td align="right">60.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right">558,952</td>
<td align="right">237,401</td>
<td align="right">-57.5%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">558,952</td>
<td align="right">237,401</td>
<td align="right">-57.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">968,480</td>
<td align="right">439,752</td>
<td align="right">-54.6%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">1,326,565</td>
<td align="right">1,991,540</td>
<td align="right">50.1%</td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right">3,871,380</td>
<td align="right">1,969,065</td>
<td align="right">-49.1%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">3,841,307</td>
<td align="right">5,663,487</td>
<td align="right">47.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">2,982,384</td>
<td align="right">4,382,391</td>
<td align="right">46.9%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">748,995</td>
<td align="right">1,066,009</td>
<td align="right">42.3%</td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right">3,414,568</td>
<td align="right">4,787,150</td>
<td align="right">40.2%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">1,927,535</td>
<td align="right">2,689,117</td>
<td align="right">39.5%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">7,432,765</td>
<td align="right">10,363,507</td>
<td align="right">39.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">7,954,774</td>
<td align="right">11,055,321</td>
<td align="right">39.0%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">4,231,022</td>
<td align="right">5,700,551</td>
<td align="right">34.7%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">4,231,022</td>
<td align="right">5,691,113</td>
<td align="right">34.5%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">283,834</td>
<td align="right">379,766</td>
<td align="right">33.8%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right">296,382</td>
<td align="right">394,897</td>
<td align="right">33.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,918,173</td>
<td align="right">2,552,636</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">1,907,186</td>
<td align="right">2,532,342</td>
<td align="right">32.8%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">5,888,649</td>
<td align="right">4,133,873</td>
<td align="right">-29.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">2,830,231</td>
<td align="right">3,623,816</td>
<td align="right">28.0%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">2,351,628</td>
<td align="right">2,992,142</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">16,522,454</td>
<td align="right">20,675,559</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">471,312</td>
<td align="right">588,347</td>
<td align="right">24.8%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">11,502,372</td>
<td align="right">14,259,454</td>
<td align="right">24.0%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">18,447,344</td>
<td align="right">22,710,941</td>
<td align="right">23.1%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">8,488,727</td>
<td align="right">10,374,027</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">1,817,816</td>
<td align="right">2,220,935</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">13,370,528</td>
<td align="right">16,310,292</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">5,961,256</td>
<td align="right">4,783,172</td>
<td align="right">-19.8%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">5,961,256</td>
<td align="right">4,783,172</td>
<td align="right">-19.8%</td>
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
<td align="right">41,248</td>
<td align="right">-18.4%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right">3,482,027</td>
<td align="right">4,111,502</td>
<td align="right">18.1%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">149,228</td>
<td align="right">123,775</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">3,516,967</td>
<td align="right">4,098,002</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">1,738,993</td>
<td align="right">1,997,135</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">1,578,417</td>
<td align="right">1,378,845</td>
<td align="right">-12.6%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">3,186,000</td>
<td align="right">3,575,484</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">468,868</td>
<td align="right">413,587</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">919,802</td>
<td align="right">816,727</td>
<td align="right">-11.2%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">1,924,890</td>
<td align="right">2,035,382</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">16,522,453</td>
<td align="right">15,744,082</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">581,380</td>
<td align="right">566,732</td>
<td align="right">-2.5%</td>
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
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">19,866,375</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">4,931,435</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">4,132,026</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">3,288,985</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right"></td>
<td align="right">1,775,498</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SEND_GEN_FRAME</td>
<td align="right"></td>
<td align="right">1,598,589</td>
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
<td align="right">738,588</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right"></td>
<td align="right">652,463</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right"></td>
<td align="right">359,074</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right"></td>
<td align="right">359,074</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right"></td>
<td align="right">355,403</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">348,700</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_SEND</td>
<td align="right"></td>
<td align="right">253,639</td>
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
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right"></td>
<td align="right">13,458</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right"></td>
<td align="right">13,458</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_UNPACK_EX</td>
<td align="right"></td>
<td align="right">13,456</td>
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
Stats gathered on: 2025-10-23
