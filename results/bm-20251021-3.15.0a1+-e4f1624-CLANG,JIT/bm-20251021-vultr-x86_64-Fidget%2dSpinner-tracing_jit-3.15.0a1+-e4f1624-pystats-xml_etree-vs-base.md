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
<td align="left">FOR_ITER_LIST</td>
<td align="right">615,876</td>
<td align="right">8,740,500</td>
<td align="right">1,319.2%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,365,621</td>
<td align="right">16,549,669</td>
<td align="right">1,111.9%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">10,796,231</td>
<td align="right">35,459,100</td>
<td align="right">228.4%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">34,126</td>
<td align="right">111,015</td>
<td align="right">225.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">1,258,701</td>
<td align="right">2,731,673</td>
<td align="right">117.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">13,113,350</td>
<td align="right">50,553</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">14,156,627</td>
<td align="right">575,034</td>
<td align="right">-95.9%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">1,342,908</td>
<td align="right">68,382</td>
<td align="right">-94.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">14,319,725</td>
<td align="right">813,317</td>
<td align="right">-94.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">2,353,731</td>
<td align="right">4,566,988</td>
<td align="right">94.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">550,608</td>
<td align="right">34,697</td>
<td align="right">-93.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">4,070,717</td>
<td align="right">271,695</td>
<td align="right">-93.3%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">851,307</td>
<td align="right">1,581,342</td>
<td align="right">85.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">2,875,510</td>
<td align="right">409,978</td>
<td align="right">-85.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">26,101,261</td>
<td align="right">4,086,749</td>
<td align="right">-84.3%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">3,081,949</td>
<td align="right">500,013</td>
<td align="right">-83.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">923,111</td>
<td align="right">1,659,262</td>
<td align="right">79.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">5,312,991</td>
<td align="right">9,401,000</td>
<td align="right">76.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">706,055</td>
<td align="right">175,773</td>
<td align="right">-75.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">4,865,228</td>
<td align="right">1,282,013</td>
<td align="right">-73.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">358,045</td>
<td align="right">94,612</td>
<td align="right">-73.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">2,087,766</td>
<td align="right">555,475</td>
<td align="right">-73.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">29,065,123</td>
<td align="right">8,146,864</td>
<td align="right">-72.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">754,220</td>
<td align="right">223,930</td>
<td align="right">-70.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">760,473</td>
<td align="right">229,751</td>
<td align="right">-69.8%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">11,322,543</td>
<td align="right">19,112,823</td>
<td align="right">68.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">803,170</td>
<td align="right">272,400</td>
<td align="right">-66.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">28,995,743</td>
<td align="right">9,885,953</td>
<td align="right">-65.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">2,079,771</td>
<td align="right">720,903</td>
<td align="right">-65.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">44,832,345</td>
<td align="right">17,939,752</td>
<td align="right">-60.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">434,175</td>
<td align="right">178,325</td>
<td align="right">-58.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">15,856,504</td>
<td align="right">7,655,713</td>
<td align="right">-51.7%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">14,548,520</td>
<td align="right">7,551,719</td>
<td align="right">-48.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">225,509</td>
<td align="right">139,938</td>
<td align="right">-37.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">147,160,547</td>
<td align="right">99,400,907</td>
<td align="right">-32.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">20,863,456</td>
<td align="right">26,327,773</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">9,031,129</td>
<td align="right">10,937,781</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">34,774,197</td>
<td align="right">30,929,988</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">936,637</td>
<td align="right">850,026</td>
<td align="right">-9.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">103,022</td>
<td align="right">95,754</td>
<td align="right">-7.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">12,668,522</td>
<td align="right">13,551,954</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">128,015</td>
<td align="right">120,483</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">62,129,721</td>
<td align="right">58,880,937</td>
<td align="right">-5.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">11,691,710</td>
<td align="right">11,099,567</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">91,366,479</td>
<td align="right">87,238,260</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">164,177</td>
<td align="right">158,587</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">164,727</td>
<td align="right">159,137</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">14,998,055</td>
<td align="right">14,513,864</td>
<td align="right">-3.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">21,665,099</td>
<td align="right">21,012,737</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">17,917,267</td>
<td align="right">18,382,835</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">114,354,212</td>
<td align="right">111,424,189</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">29,982</td>
<td align="right">29,517</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">17,028</td>
<td align="right">16,764</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">516</td>
<td align="right">508</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">516</td>
<td align="right">508</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">17,025,682</td>
<td align="right">16,761,718</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">17,065,920</td>
<td align="right">16,801,644</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">15,501</td>
<td align="right">15,261</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">26,392</td>
<td align="right">25,984</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">262</td>
<td align="right">258</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">528</td>
<td align="right">520</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">14,062</td>
<td align="right">13,858</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">18,965</td>
<td align="right">18,717</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">19,204</td>
<td align="right">18,956</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">19,204</td>
<td align="right">18,956</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">311</td>
<td align="right">307</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">2,364</td>
<td align="right">2,340</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">51,597</td>
<td align="right">51,089</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">735,289</td>
<td align="right">728,279</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">30,582</td>
<td align="right">30,346</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">30,066</td>
<td align="right">29,838</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">2,318</td>
<td align="right">2,302</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">10,858,799</td>
<td align="right">10,793,243</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">18,364,763</td>
<td align="right">18,463,539</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">55,604,490</td>
<td align="right">55,339,790</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">6,995</td>
<td align="right">6,963</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">1,794</td>
<td align="right">1,786</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">5,394</td>
<td align="right">5,370</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">1,806</td>
<td align="right">1,798</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">1,806</td>
<td align="right">1,798</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">7,264</td>
<td align="right">7,232</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">10,034</td>
<td align="right">9,990</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">1,827</td>
<td align="right">1,819</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">8,227</td>
<td align="right">8,195</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">6,172</td>
<td align="right">6,148</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">2,100</td>
<td align="right">2,092</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">2,100</td>
<td align="right">2,092</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">2,100</td>
<td align="right">2,092</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">174,310</td>
<td align="right">173,650</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">12,500</td>
<td align="right">12,456</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">12,782</td>
<td align="right">12,742</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">19,779</td>
<td align="right">19,719</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">158,377</td>
<td align="right">157,949</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">10,540</td>
<td align="right">10,512</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">13,892</td>
<td align="right">13,860</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">12,705</td>
<td align="right">12,677</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">5,583</td>
<td align="right">5,571</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">26,243</td>
<td align="right">26,187</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">66,384,804</td>
<td align="right">66,524,561</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">65,316</td>
<td align="right">65,244</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">7,352</td>
<td align="right">7,344</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">1,913</td>
<td align="right">1,911</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">67,170</td>
<td align="right">67,126</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">38,965</td>
<td align="right">38,941</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">133,824</td>
<td align="right">133,744</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">133,824</td>
<td align="right">133,744</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">11,614</td>
<td align="right">11,619</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">18,753</td>
<td align="right">18,745</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">18,945</td>
<td align="right">18,937</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">672,898</td>
<td align="right">673,156</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">615,219</td>
<td align="right">615,184</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">13,078,398</td>
<td align="right">13,078,170</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">4,628,079</td>
<td align="right">4,628,047</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">13,079,038</td>
<td align="right">13,079,038</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">95,052</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">17,172</td>
<td align="right">17,172</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">10,404</td>
<td align="right">10,404</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">5,301</td>
<td align="right">5,301</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">5,151</td>
<td align="right">5,151</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">2,845</td>
<td align="right">2,845</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">2,568</td>
<td align="right">2,568</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">2,144</td>
<td align="right">2,144</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">2,088</td>
<td align="right">2,088</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">2,084</td>
<td align="right">2,084</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">1,638</td>
<td align="right">1,638</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">1,356</td>
<td align="right">1,356</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">1,304</td>
<td align="right">1,304</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FROM_DICT_OR_DEREF</td>
<td align="right">1,280</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">1,280</td>
<td align="right">1,280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">385</td>
<td align="right">385</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">333</td>
<td align="right">333</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">285</td>
<td align="right">285</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">273</td>
<td align="right">273</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">261</td>
<td align="right">261</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">261</td>
<td align="right">261</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">257</td>
<td align="right">257</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">253</td>
<td align="right">253</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">251</td>
<td align="right">251</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">224</td>
<td align="right">224</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">88</td>
<td align="right">88</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">63</td>
<td align="right">63</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">56</td>
<td align="right">56</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">24</td>
<td align="right">24</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">20</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">16</td>
<td align="right">16</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">12</td>
<td align="right">12</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">12</td>
<td align="right">12</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">12</td>
<td align="right">12</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">12</td>
<td align="right">12</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">8</td>
<td align="right">8</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">8</td>
<td align="right">8</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
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
<td align="left">IMPORT_NAME</td>
<td align="right">4</td>
<td align="right">4</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">4</td>
<td align="right">4</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">4</td>
<td align="right">4</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">4</td>
<td align="right">4</td>
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
<td align="right">734,146</td>
<td align="right">1.7%</td>
<td align="right">726,922</td>
<td align="right">1.7%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">43,326,017</td>
<td align="right">98.3%</td>
<td align="right">43,061,185</td>
<td align="right">98.3%</td>
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
<td align="right">824</td>
<td align="right">72.1%</td>
<td align="right">1,038</td>
<td align="right">76.5%</td>
<td align="right">26.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">319</td>
<td align="right">27.9%</td>
<td align="right">319</td>
<td align="right">23.5%</td>
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
<td align="left">subscr string slice</td>
<td align="right">200</td>
<td align="right">24.3%</td>
<td align="right">284</td>
<td align="right">27.4%</td>
<td align="right">42.0%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">359</td>
<td align="right">43.6%</td>
<td align="right">489</td>
<td align="right">47.1%</td>
<td align="right">36.2%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">129</td>
<td align="right">15.7%</td>
<td align="right">129</td>
<td align="right">12.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">88</td>
<td align="right">10.7%</td>
<td align="right">88</td>
<td align="right">8.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">48</td>
<td align="right">5.8%</td>
<td align="right">48</td>
<td align="right">4.6%</td>
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
<td align="right">15,501</td>
<td align="right">100.0%</td>
<td align="right">15,261</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">17,233</td>
<td align="right">0.0%</td>
<td align="right">16,970</td>
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
<td align="right">17,644</td>
<td align="right">0.0%</td>
<td align="right">17,386</td>
<td align="right">0.0%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">169,529,789</td>
<td align="right">100.0%</td>
<td align="right">168,430,317</td>
<td align="right">100.0%</td>
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
<td align="left">Success</td>
<td align="right">4,740</td>
<td align="right">100.0%</td>
<td align="right">4,735</td>
<td align="right">100.0%</td>
<td align="right">-0.1%</td>
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
<td align="right">48</td>
<td align="right">14.4%</td>
<td align="right">48</td>
<td align="right">14.4%</td>
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
<td align="right">285</td>
<td align="right">100.0%</td>
<td align="right">285</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,877,814</td>
<td align="right">99.9%</td>
<td align="right">2,834,442</td>
<td align="right">99.9%</td>
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
<td align="right">1,473</td>
<td align="right">0.1%</td>
<td align="right">1,471</td>
<td align="right">0.1%</td>
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
<td align="right">64</td>
<td align="right">0.0%</td>
<td align="right">64</td>
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
<td align="right">264</td>
<td align="right">60.0%</td>
<td align="right">264</td>
<td align="right">60.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">176</td>
<td align="right">40.0%</td>
<td align="right">176</td>
<td align="right">40.0%</td>
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
<td align="right">112</td>
<td align="right">63.6%</td>
<td align="right">112</td>
<td align="right">63.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">43</td>
<td align="right">24.4%</td>
<td align="right">43</td>
<td align="right">24.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">21</td>
<td align="right">11.9%</td>
<td align="right">21</td>
<td align="right">11.9%</td>
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
<td align="right">2,351,759</td>
<td align="right">16.6%</td>
<td align="right">4,564,322</td>
<td align="right">27.9%</td>
<td align="right">94.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">11,850,770</td>
<td align="right">83.4%</td>
<td align="right">11,769,518</td>
<td align="right">72.0%</td>
<td align="right">-0.7%</td>
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
<td align="right">1,964</td>
<td align="right">99.6%</td>
<td align="right">2,658</td>
<td align="right">99.7%</td>
<td align="right">35.3%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">8</td>
<td align="right">0.4%</td>
<td align="right">8</td>
<td align="right">0.3%</td>
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
<td align="right">1,679</td>
<td align="right">85.5%</td>
<td align="right">2,373</td>
<td align="right">89.3%</td>
<td align="right">41.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">152</td>
<td align="right">7.7%</td>
<td align="right">152</td>
<td align="right">5.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">133</td>
<td align="right">6.8%</td>
<td align="right">133</td>
<td align="right">5.0%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,360,613</td>
<td align="right">37.2%</td>
<td align="right">13,422,391</td>
<td align="right">55.1%</td>
<td align="right">150.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">9,028,311</td>
<td align="right">62.7%</td>
<td align="right">10,931,889</td>
<td align="right">44.9%</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">516</td>
<td align="right">0.0%</td>
<td align="right">508</td>
<td align="right">0.0%</td>
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
<td align="right">2,688</td>
<td align="right">95.4%</td>
<td align="right">5,762</td>
<td align="right">97.8%</td>
<td align="right">114.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">130</td>
<td align="right">4.6%</td>
<td align="right">130</td>
<td align="right">2.2%</td>
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
<td align="left">seq iter</td>
<td align="right">882</td>
<td align="right">32.8%</td>
<td align="right">5,109</td>
<td align="right">88.7%</td>
<td align="right">479.3%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">1,682</td>
<td align="right">62.6%</td>
<td align="right">529</td>
<td align="right">9.2%</td>
<td align="right">-68.5%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">96</td>
<td align="right">3.6%</td>
<td align="right">96</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">24</td>
<td align="right">0.9%</td>
<td align="right">24</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">4</td>
<td align="right">0.1%</td>
<td align="right">4</td>
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
<td align="left">generator</td>
<td align="right">17,544</td>
<td align="right">17,544 / 0 !!</td>
<td align="right">17,272</td>
<td align="right">17,272 / 0 !!</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">44,494</td>
<td align="right">44,494 / 0 !!</td>
<td align="right">43,842</td>
<td align="right">43,842 / 0 !!</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">11,866,831</td>
<td align="right">11,866,831 / 0 !!</td>
<td align="right">11,785,331</td>
<td align="right">11,785,331 / 0 !!</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">10,542,724</td>
<td align="right">10,542,724 / 0 !!</td>
<td align="right">10,481,452</td>
<td align="right">10,481,452 / 0 !!</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">546</td>
<td align="right">546 / 0 !!</td>
<td align="right">546</td>
<td align="right">546 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">13</td>
<td align="right">13 / 0 !!</td>
<td align="right">13</td>
<td align="right">13 / 0 !!</td>
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
<td align="right">32,772,614</td>
<td align="right">64.1%</td>
<td align="right">29,147,098</td>
<td align="right">61.2%</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">18,356,774</td>
<td align="right">35.9%</td>
<td align="right">18,455,228</td>
<td align="right">38.8%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">7,525</td>
<td align="right">0.0%</td>
<td align="right">7,525</td>
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
<td align="right">5,609</td>
<td align="right">69.1%</td>
<td align="right">5,931</td>
<td align="right">70.3%</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,504</td>
<td align="right">30.9%</td>
<td align="right">2,504</td>
<td align="right">29.7%</td>
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
<td align="left">overriding descriptor</td>
<td align="right">4,804</td>
<td align="right">85.6%</td>
<td align="right">5,126</td>
<td align="right">86.4%</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">523</td>
<td align="right">9.3%</td>
<td align="right">523</td>
<td align="right">8.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">45</td>
<td align="right">0.8%</td>
<td align="right">45</td>
<td align="right">0.8%</td>
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
<td align="right">49,927,959</td>
<td align="right">100.0%</td>
<td align="right">74,096,407</td>
<td align="right">100.0%</td>
<td align="right">48.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">961</td>
<td align="right">0.0%</td>
<td align="right">961</td>
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
<td align="right">620</td>
<td align="right">0.0%</td>
<td align="right">620</td>
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
<td align="right">4,340</td>
<td align="right">100.0%</td>
<td align="right">4,340</td>
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
<td align="right">1,296</td>
<td align="right">99.7%</td>
<td align="right">1,296</td>
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
<td align="right">4</td>
<td align="right">100.0%</td>
<td align="right">4</td>
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
<td align="right">29,930</td>
<td align="right">0.2%</td>
<td align="right">29,466</td>
<td align="right">0.2%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">13,079,038</td>
<td align="right">99.8%</td>
<td align="right">13,079,038</td>
<td align="right">99.8%</td>
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
<td align="right">50</td>
<td align="right">96.2%</td>
<td align="right">49</td>
<td align="right">96.1%</td>
<td align="right">-2.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2</td>
<td align="right">3.8%</td>
<td align="right">2</td>
<td align="right">3.9%</td>
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
<td align="right">50</td>
<td align="right">100.0%</td>
<td align="right">49</td>
<td align="right">100.0%</td>
<td align="right">-2.0%</td>
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
<td align="right">2,078,682</td>
<td align="right">10.9%</td>
<td align="right">719,981</td>
<td align="right">4.1%</td>
<td align="right">-65.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">17,061,057</td>
<td align="right">89.1%</td>
<td align="right">16,796,781</td>
<td align="right">95.9%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,867</td>
<td align="right">0.0%</td>
<td align="right">4,867</td>
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
<td align="right">1,042</td>
<td align="right">93.9%</td>
<td align="right">875</td>
<td align="right">92.8%</td>
<td align="right">-16.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">68</td>
<td align="right">6.1%</td>
<td align="right">68</td>
<td align="right">7.2%</td>
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
<td align="left">overriding descriptor</td>
<td align="right">712</td>
<td align="right">68.3%</td>
<td align="right">545</td>
<td align="right">62.3%</td>
<td align="right">-23.5%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">152</td>
<td align="right">14.6%</td>
<td align="right">152</td>
<td align="right">17.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">133</td>
<td align="right">12.8%</td>
<td align="right">133</td>
<td align="right">15.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">45</td>
<td align="right">4.3%</td>
<td align="right">45</td>
<td align="right">5.1%</td>
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
<td align="right">263</td>
<td align="right">0.3%</td>
<td align="right">259</td>
<td align="right">0.3%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">103,022</td>
<td align="right">99.7%</td>
<td align="right">102,558</td>
<td align="right">99.7%</td>
<td align="right">-0.5%</td>
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
<td align="right">5</td>
<td align="right">10.4%</td>
<td align="right">5</td>
<td align="right">10.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">43</td>
<td align="right">89.6%</td>
<td align="right">43</td>
<td align="right">89.6%</td>
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
<td align="right">43</td>
<td align="right">100.0%</td>
<td align="right">43</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">13,109,484</td>
<td align="right">16.1%</td>
<td align="right">49,884</td>
<td align="right">0.1%</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">68,361,861</td>
<td align="right">83.7%</td>
<td align="right">61,032,882</td>
<td align="right">99.6%</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">186,603</td>
<td align="right">0.2%</td>
<td align="right">192,467</td>
<td align="right">0.3%</td>
<td align="right">3.1%</td>
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
<td align="right">3,460</td>
<td align="right">47.1%</td>
<td align="right">263</td>
<td align="right">6.2%</td>
<td align="right">-92.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,882</td>
<td align="right">52.9%</td>
<td align="right">3,988</td>
<td align="right">93.8%</td>
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
<td align="left">sequence</td>
<td align="right">3,364</td>
<td align="right">97.2%</td>
<td align="right">167</td>
<td align="right">63.5%</td>
<td align="right">-95.0%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">96</td>
<td align="right">2.8%</td>
<td align="right">96</td>
<td align="right">36.5%</td>
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
<td align="right">15,813,356</td>
<td align="right">100.0%</td>
<td align="right">15,772,900</td>
<td align="right">100.0%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">32</td>
<td align="right">0.0%</td>
<td align="right">32</td>
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
<td align="right">192</td>
<td align="right">100.0%</td>
<td align="right">192</td>
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
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">353,144,949</td>
<td align="right">33.9%</td>
<td align="right">268,671,226</td>
<td align="right">30.3%</td>
<td align="right">-23.9%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">640,021,266</td>
<td align="right">61.5%</td>
<td align="right">564,713,930</td>
<td align="right">63.8%</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">47,102,374</td>
<td align="right">4.5%</td>
<td align="right">52,075,721</td>
<td align="right">5.9%</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">217,515</td>
<td align="right">0.0%</td>
<td align="right">223,021</td>
<td align="right">0.0%</td>
<td align="right">2.5%</td>
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
<td align="right">13,109,484</td>
<td align="right">28.7%</td>
<td align="right">49,884</td>
<td align="right">0.1%</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">2,351,759</td>
<td align="right">5.1%</td>
<td align="right">4,564,322</td>
<td align="right">12.9%</td>
<td align="right">94.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">2,078,682</td>
<td align="right">4.5%</td>
<td align="right">719,981</td>
<td align="right">2.0%</td>
<td align="right">-65.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">9,028,311</td>
<td align="right">19.7%</td>
<td align="right">10,931,889</td>
<td align="right">30.8%</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">29,930</td>
<td align="right">0.1%</td>
<td align="right">29,466</td>
<td align="right">0.1%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">15,501</td>
<td align="right">0.0%</td>
<td align="right">15,261</td>
<td align="right">0.0%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">17,644</td>
<td align="right">0.0%</td>
<td align="right">17,386</td>
<td align="right">0.0%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">734,146</td>
<td align="right">1.6%</td>
<td align="right">726,922</td>
<td align="right">2.0%</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">18,356,774</td>
<td align="right">40.1%</td>
<td align="right">18,455,228</td>
<td align="right">52.0%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">1,473</td>
<td align="right">0.0%</td>
<td align="right">1,471</td>
<td align="right">0.0%</td>
<td align="right">-0.1%</td>
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
<td align="right">93,509</td>
<td align="right">43.0%</td>
<td align="right">97,595</td>
<td align="right">43.8%</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">93,094</td>
<td align="right">42.8%</td>
<td align="right">94,872</td>
<td align="right">42.5%</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">16,679</td>
<td align="right">7.7%</td>
<td align="right">16,420</td>
<td align="right">7.4%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">516</td>
<td align="right">0.2%</td>
<td align="right">508</td>
<td align="right">0.2%</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">514</td>
<td align="right">0.2%</td>
<td align="right">510</td>
<td align="right">0.2%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">7,488</td>
<td align="right">3.4%</td>
<td align="right">7,488</td>
<td align="right">3.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">4,867</td>
<td align="right">2.2%</td>
<td align="right">4,867</td>
<td align="right">2.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">560</td>
<td align="right">0.3%</td>
<td align="right">560</td>
<td align="right">0.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">87</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">87</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">64</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">18,066</td>
<td align="right">0.0%</td>
<td align="right">17,826</td>
<td align="right">0.0%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">77,384,726</td>
<td align="right">69.0%</td>
<td align="right">76,712,864</td>
<td align="right">68.8%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">56,585,279</td>
<td align="right">50.4%</td>
<td align="right">56,114,805</td>
<td align="right">50.3%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">3,128</td>
<td align="right">0.0%</td>
<td align="right">3,104</td>
<td align="right">0.0%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">37,928,176</td>
<td align="right">33.8%</td>
<td align="right">37,663,932</td>
<td align="right">33.8%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">37,929,484</td>
<td align="right">33.8%</td>
<td align="right">37,665,240</td>
<td align="right">33.8%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">37,897,237</td>
<td align="right">33.8%</td>
<td align="right">37,633,281</td>
<td align="right">33.8%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">55,605,263</td>
<td align="right">49.6%</td>
<td align="right">55,340,555</td>
<td align="right">49.7%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">55,605,263</td>
<td align="right">49.6%</td>
<td align="right">55,340,555</td>
<td align="right">49.7%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">5,141</td>
<td align="right">0.0%</td>
<td align="right">5,117</td>
<td align="right">0.0%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">17,675,779</td>
<td align="right">15.8%</td>
<td align="right">17,675,315</td>
<td align="right">15.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">4</td>
<td align="right">0.0%</td>
<td align="right">4</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">1,304</td>
<td align="right">0.0%</td>
<td align="right">1,304</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">261</td>
<td align="right">0.0%</td>
<td align="right">261</td>
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
<td align="left">Interpreter mortal decrefs</td>
<td align="right">394,911,509</td>
<td align="right">18.8%</td>
<td align="right">356,006,375</td>
<td align="right">17.1%</td>
<td align="right">-9.9%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">269,468,636</td>
<td align="right">14.1%</td>
<td align="right">247,256,526</td>
<td align="right">13.0%</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">1,183,228,651</td>
<td align="right">56.4%</td>
<td align="right">1,213,415,096</td>
<td align="right">58.2%</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">6,050</td>
<td align="right"></td>
<td align="right">5,951</td>
<td align="right"></td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">17,148,758</td>
<td align="right">0.8%</td>
<td align="right">16,883,560</td>
<td align="right">0.8%</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">1,046,742,882</td>
<td align="right">54.6%</td>
<td align="right">1,061,115,598</td>
<td align="right">55.7%</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">55,977</td>
<td align="right"></td>
<td align="right">56,555</td>
<td align="right"></td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">28,488</td>
<td align="right"></td>
<td align="right">28,208</td>
<td align="right"></td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">59,829,531</td>
<td align="right">3.1%</td>
<td align="right">59,291,769</td>
<td align="right">3.1%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">57,605</td>
<td align="right"></td>
<td align="right">58,015</td>
<td align="right"></td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">155,246,139</td>
<td align="right"></td>
<td align="right">154,268,233</td>
<td align="right"></td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">75,582,494</td>
<td align="right">27.8%</td>
<td align="right">75,215,168</td>
<td align="right">27.7%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">75,584,384</td>
<td align="right"></td>
<td align="right">75,217,058</td>
<td align="right"></td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">501,501,159</td>
<td align="right">23.9%</td>
<td align="right">499,302,235</td>
<td align="right">23.9%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">541,063,787</td>
<td align="right">28.2%</td>
<td align="right">538,746,374</td>
<td align="right">28.3%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">52,642,612</td>
<td align="right"></td>
<td align="right">52,439,715</td>
<td align="right"></td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">74,551</td>
<td align="right">0.0%</td>
<td align="right">74,285</td>
<td align="right">0.0%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">196,589,655</td>
<td align="right">72.2%</td>
<td align="right">195,956,203</td>
<td align="right">72.2%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">196,758,805</td>
<td align="right"></td>
<td align="right">196,124,932</td>
<td align="right"></td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">196,767,125</td>
<td align="right">72.2%</td>
<td align="right">196,133,528</td>
<td align="right">72.3%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">102,919</td>
<td align="right">0.0%</td>
<td align="right">103,040</td>
<td align="right">0.0%</td>
<td align="right">0.1%</td>
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
<td align="right">12,884</td>
<td align="right">21,554</td>
<td align="right">299,482,070</td>
<td align="right">33,441,620</td>
<td align="right">14,393,277</td>
<td align="right">12,856</td>
<td align="right">21,554</td>
<td align="right">299,190,616</td>
<td align="right">33,440,884</td>
<td align="right">14,346,104</td>
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
<td align="right">8,800</td>
<td align="right"></td>
<td align="right">32,306</td>
<td align="right"></td>
<td align="right">267.1%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">7,340</td>
<td align="right">83.4%</td>
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
<td align="right">67</td>
<td align="right">0.8%</td>
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
<td align="right">135</td>
<td align="right">1.5%</td>
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
<td align="right">1,005</td>
<td align="right">11.4%</td>
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
<td align="right">56,109,197</td>
<td align="right"></td>
<td align="right">83,191,298</td>
<td align="right"></td>
<td align="right">48.3%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">455</td>
<td align="right">5.2%</td>
<td align="right">614</td>
<td align="right">1.9%</td>
<td align="right">34.9%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">3,313,653,059</td>
<td align="right">5,905.7%</td>
<td align="right">3,826,847,580</td>
<td align="right">4,600.1%</td>
<td align="right">15.5%</td>
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
Low confidence
<details>
<summary>ⓘ</summary>

A trace is abandoned because the likelihood of the jump to top being taken is too low.
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
<td align="right">455</td>
<td align="right"></td>
<td align="right">614</td>
<td align="right"></td>
<td align="right">34.9%</td>
</tr>
<tr>
<td align="left">
Optimizer successes
<details>
<summary>ⓘ</summary>

The number of traces that were successfully optimized.
</details>
</td>
<td align="right">455</td>
<td align="right">100.0%</td>
<td align="right">614</td>
<td align="right">100.0%</td>
<td align="right">34.9%</td>
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
Freed memory size
<details>
<summary>ⓘ</summary>

The size of the memory freed from the JIT traces
</details>
</td>
<td align="right">4,096</td>
<td align="right">0.1%</td>
<td align="right">86,016</td>
<td align="right">1.3%</td>
<td align="right">2,000.0%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">902,346</td>
<td align="right">18.7%</td>
<td align="right">1,332,030</td>
<td align="right">19.5%</td>
<td align="right">47.6%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">4,837,376</td>
<td align="right"></td>
<td align="right">6,832,128</td>
<td align="right"></td>
<td align="right">41.2%</td>
</tr>
<tr>
<td align="left">
Code size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the code of the JIT traces
</details>
</td>
<td align="right">3,838,707</td>
<td align="right">79.4%</td>
<td align="right">5,378,888</td>
<td align="right">78.7%</td>
<td align="right">40.1%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">95,864</td>
<td align="right">2.0%</td>
<td align="right">120,592</td>
<td align="right">1.8%</td>
<td align="right">25.8%</td>
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
<td align="left">146</td>
<td align="right">31.8%</td>
<td align="left">263</td>
<td align="right">42.6%</td>
<td align="right">80.1%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">176</td>
<td align="right">38.3%</td>
<td align="left">182</td>
<td align="right">29.4%</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">68</td>
<td align="right">14.8%</td>
<td align="left">42</td>
<td align="right">6.8%</td>
<td align="right">-38.2%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">69</td>
<td align="right">15.0%</td>
<td align="left">131</td>
<td align="right">21.2%</td>
<td align="right">89.9%</td>
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
<td align="left"><= 32</td>
<td align="right">7</td>
<td align="right">1.5%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">310</td>
<td align="right">68.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">1</td>
<td align="right">0.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">70</td>
<td align="right">15.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">67</td>
<td align="right">14.7%</td>
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
<td align="right">272</td>
<td align="right">59.8%</td>
<td align="right">28</td>
<td align="right">4.6%</td>
<td align="right">-89.7%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">46</td>
<td align="right">10.1%</td>
<td align="right">200</td>
<td align="right">32.6%</td>
<td align="right">334.8%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">68</td>
<td align="right">14.9%</td>
<td align="right">21</td>
<td align="right">3.4%</td>
<td align="right">-69.1%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">69</td>
<td align="right">15.2%</td>
<td align="right">131</td>
<td align="right">21.3%</td>
<td align="right">89.9%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">234</td>
<td align="right">38.1%</td>
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
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,282,883</td>
<td align="right">11,427,907</td>
<td align="right">790.8%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">10,794,320</td>
<td align="right">35,156,868</td>
<td align="right">225.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">22,246,259</td>
<td align="right">51,770,631</td>
<td align="right">132.7%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">43,746,426</td>
<td align="right">85,980,816</td>
<td align="right">96.5%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right">10,998,620</td>
<td align="right">1,284,810</td>
<td align="right">-88.3%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">10,998,620</td>
<td align="right">1,291,551</td>
<td align="right">-88.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">33,232,237</td>
<td align="right">61,930,024</td>
<td align="right">86.4%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">21,106,531</td>
<td align="right">5,778,787</td>
<td align="right">-72.6%</td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right">11,148,552</td>
<td align="right">3,214,592</td>
<td align="right">-71.2%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">19,880,990</td>
<td align="right">33,340,459</td>
<td align="right">67.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">21,163,873</td>
<td align="right">34,526,045</td>
<td align="right">63.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">14,025,815</td>
<td align="right">5,778,787</td>
<td align="right">-58.8%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">14,025,815</td>
<td align="right">5,778,787</td>
<td align="right">-58.8%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">66,273,788</td>
<td align="right">104,604,447</td>
<td align="right">57.8%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right">19,487,217</td>
<td align="right">30,449,063</td>
<td align="right">56.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">29,590,271</td>
<td align="right">45,680,702</td>
<td align="right">54.4%</td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right">2,285</td>
<td align="right">3,393</td>
<td align="right">48.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">110,615,142</td>
<td align="right">65,810,656</td>
<td align="right">-40.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">102,393,069</td>
<td align="right">73,614,771</td>
<td align="right">-28.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">10,202,963</td>
<td align="right">12,997,036</td>
<td align="right">27.4%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">5,031,398</td>
<td align="right">6,349,471</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">35,441,520</td>
<td align="right">42,174,345</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">43,577,806</td>
<td align="right">50,884,814</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">19,880,990</td>
<td align="right">23,098,138</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">579,002,332</td>
<td align="right">672,159,157</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">21,046,151</td>
<td align="right">24,165,272</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">40,182,083</td>
<td align="right">34,345,489</td>
<td align="right">-14.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">44,238,619</td>
<td align="right">50,494,147</td>
<td align="right">14.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">42,446,546</td>
<td align="right">36,753,439</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">105,386,906</td>
<td align="right">119,342,683</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">19,368,491</td>
<td align="right">21,820,612</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">11,492,705</td>
<td align="right">12,919,924</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">102,880,469</td>
<td align="right">90,564,675</td>
<td align="right">-12.0%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">20,666,841</td>
<td align="right">23,083,465</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">630,287,828</td>
<td align="right">693,339,778</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">119,884,280</td>
<td align="right">109,106,518</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">19,387,308</td>
<td align="right">17,790,854</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">9,693,654</td>
<td align="right">8,895,427</td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">64,683,368</td>
<td align="right">69,855,042</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">1,282,883</td>
<td align="right">1,185,586</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">1,282,883</td>
<td align="right">1,185,586</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">1,282,883</td>
<td align="right">1,185,586</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">1,282,883</td>
<td align="right">1,185,586</td>
<td align="right">-7.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">22,827,289</td>
<td align="right">24,551,044</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right">10,998,620</td>
<td align="right">10,187,021</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">10,998,620</td>
<td align="right">10,187,041</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">38,215,724</td>
<td align="right">35,679,811</td>
<td align="right">-6.6%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">45,314,877</td>
<td align="right">48,034,430</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">1,120,683</td>
<td align="right">1,185,586</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">45,312,505</td>
<td align="right">47,732,196</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">9,716,730</td>
<td align="right">10,187,549</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">9,773,079</td>
<td align="right">10,242,321</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">9,773,079</td>
<td align="right">10,242,321</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">9,773,079</td>
<td align="right">10,242,321</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_LIST</td>
<td align="right">9,773,079</td>
<td align="right">10,242,321</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">9,773,079</td>
<td align="right">10,242,321</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">45,584,750</td>
<td align="right">43,412,320</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right">11,078,045</td>
<td align="right">11,533,915</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">72,886,466</td>
<td align="right">69,920,506</td>
<td align="right">-4.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_DICT</td>
<td align="right">11,078,045</td>
<td align="right">11,527,111</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">30,465,353</td>
<td align="right">29,317,965</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">21,046,151</td>
<td align="right">20,429,362</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">21,046,151</td>
<td align="right">20,429,362</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">26,139,074</td>
<td align="right">26,710,224</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_KW</td>
<td align="right">10,047,531</td>
<td align="right">10,242,321</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">_PY_FRAME_KW</td>
<td align="right">10,047,531</td>
<td align="right">10,242,321</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">10,202,963</td>
<td align="right">10,399,849</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">32,273,255</td>
<td align="right">32,836,582</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">11,492,705</td>
<td align="right">11,674,886</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right">11,492,705</td>
<td align="right">11,674,886</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">2,609,932</td>
<td align="right">2,569,580</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">2,609,932</td>
<td align="right">2,569,580</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">1,304,966</td>
<td align="right">1,284,790</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">1,304,966</td>
<td align="right">1,284,810</td>
<td align="right">-1.5%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">2,594,708</td>
<td align="right">2,559,847</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">5,033,683</td>
<td align="right">5,098,326</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">5,033,683</td>
<td align="right">5,098,326</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">1,289,742</td>
<td align="right">1,275,037</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">16,540,015</td>
<td align="right">16,705,198</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">53,770,192</td>
<td align="right">53,263,290</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">5,202,742</td>
<td align="right">5,181,351</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">5,202,742</td>
<td align="right">5,187,777</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">42,155,656</td>
<td align="right">42,250,030</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">15,648,918</td>
<td align="right">15,614,052</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">15,648,918</td>
<td align="right">15,614,052</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">3,913,000</td>
<td align="right">3,919,544</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">3,913,000</td>
<td align="right">3,912,740</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">3,952,650</td>
<td align="right">3,952,390</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">3,952,650</td>
<td align="right">3,952,390</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">16,967,210</td>
<td align="right">16,966,945</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">13,054,210</td>
<td align="right">13,054,205</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">20,771,786</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">87</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right"></td>
<td align="right">49,517,015</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right"></td>
<td align="right">39,622,390</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">38,133,430</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right"></td>
<td align="right">29,380,069</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right"></td>
<td align="right">13,094,267</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right"></td>
<td align="right">13,059,584</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right"></td>
<td align="right">12,664,505</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right"></td>
<td align="right">11,810,827</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">10,242,321</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right"></td>
<td align="right">8,902,231</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right"></td>
<td align="right">8,902,231</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right"></td>
<td align="right">8,895,427</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right"></td>
<td align="right">5,743,934</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">3,781,137</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">3,735,910</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right"></td>
<td align="right">2,422,184</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_KW_NON_PY</td>
<td align="right"></td>
<td align="right">1,254,518</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE_KW</td>
<td align="right"></td>
<td align="right">1,254,518</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right"></td>
<td align="right">1,183,950</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">298,841</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right"></td>
<td align="right">6,804</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right"></td>
<td align="right">6,804</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right"></td>
<td align="right">6,804</td>
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
<td align="right">84</td>
<td align="right">84</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-10-22
