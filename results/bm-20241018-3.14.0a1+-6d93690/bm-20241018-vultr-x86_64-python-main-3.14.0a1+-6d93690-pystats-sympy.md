
# Pystats results

- benchmark: sympy
- fork: python
- ref: main
- commit hash: 6d93690
- commit date: 2024-10-18T09:26:08-06:00

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
<th align="right">Count</th>
<th align="right">Self</th>
<th align="right">Cumulative</th>
<th align="right">Miss ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,065,440,377</td>
<td align="right">16.4%</td>
<td align="right">16.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">407,987,717</td>
<td align="right">6.3%</td>
<td align="right">22.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">299,379,979</td>
<td align="right">4.6%</td>
<td align="right">27.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">297,845,375</td>
<td align="right">4.6%</td>
<td align="right">31.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">278,722,279</td>
<td align="right">4.3%</td>
<td align="right">36.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">244,763,245</td>
<td align="right">3.8%</td>
<td align="right">39.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">207,701,870</td>
<td align="right">3.2%</td>
<td align="right">43.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">192,355,940</td>
<td align="right">3.0%</td>
<td align="right">46.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">179,786,402</td>
<td align="right">2.8%</td>
<td align="right">48.9%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">178,870,864</td>
<td align="right">2.8%</td>
<td align="right">51.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">152,631,782</td>
<td align="right">2.4%</td>
<td align="right">54.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">133,933,032</td>
<td align="right">2.1%</td>
<td align="right">56.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">109,063,244</td>
<td align="right">1.7%</td>
<td align="right">57.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">107,685,056</td>
<td align="right">1.7%</td>
<td align="right">59.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">107,489,752</td>
<td align="right">1.7%</td>
<td align="right">61.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">106,967,514</td>
<td align="right">1.6%</td>
<td align="right">62.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">106,186,118</td>
<td align="right">1.6%</td>
<td align="right">64.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">100,816,875</td>
<td align="right">1.6%</td>
<td align="right">65.9%</td>
<td align="right">39.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">99,441,717</td>
<td align="right">1.5%</td>
<td align="right">67.4%</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">76,272,987</td>
<td align="right">1.2%</td>
<td align="right">68.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">73,521,686</td>
<td align="right">1.1%</td>
<td align="right">69.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">72,918,400</td>
<td align="right">1.1%</td>
<td align="right">70.8%</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">70,554,279</td>
<td align="right">1.1%</td>
<td align="right">71.9%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">70,124,822</td>
<td align="right">1.1%</td>
<td align="right">73.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">67,424,469</td>
<td align="right">1.0%</td>
<td align="right">74.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">63,459,866</td>
<td align="right">1.0%</td>
<td align="right">75.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">61,259,763</td>
<td align="right">0.9%</td>
<td align="right">75.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">61,137,162</td>
<td align="right">0.9%</td>
<td align="right">76.9%</td>
<td align="right">29.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">60,519,443</td>
<td align="right">0.9%</td>
<td align="right">77.8%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">58,798,782</td>
<td align="right">0.9%</td>
<td align="right">78.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">51,786,730</td>
<td align="right">0.8%</td>
<td align="right">79.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">50,443,262</td>
<td align="right">0.8%</td>
<td align="right">80.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">49,419,354</td>
<td align="right">0.8%</td>
<td align="right">81.1%</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">48,821,295</td>
<td align="right">0.8%</td>
<td align="right">81.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">45,725,116</td>
<td align="right">0.7%</td>
<td align="right">82.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">41,342,426</td>
<td align="right">0.6%</td>
<td align="right">83.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">39,938,384</td>
<td align="right">0.6%</td>
<td align="right">83.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">37,178,110</td>
<td align="right">0.6%</td>
<td align="right">84.3%</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">36,842,512</td>
<td align="right">0.6%</td>
<td align="right">84.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">36,118,445</td>
<td align="right">0.6%</td>
<td align="right">85.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">35,319,813</td>
<td align="right">0.5%</td>
<td align="right">86.0%</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">34,883,073</td>
<td align="right">0.5%</td>
<td align="right">86.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">34,318,576</td>
<td align="right">0.5%</td>
<td align="right">87.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">33,853,569</td>
<td align="right">0.5%</td>
<td align="right">87.6%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">32,719,437</td>
<td align="right">0.5%</td>
<td align="right">88.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">30,949,950</td>
<td align="right">0.5%</td>
<td align="right">88.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">30,650,623</td>
<td align="right">0.5%</td>
<td align="right">89.0%</td>
<td align="right">17.1%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">29,627,536</td>
<td align="right">0.5%</td>
<td align="right">89.5%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">29,160,237</td>
<td align="right">0.4%</td>
<td align="right">89.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">29,130,520</td>
<td align="right">0.4%</td>
<td align="right">90.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">28,949,626</td>
<td align="right">0.4%</td>
<td align="right">90.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">26,797,656</td>
<td align="right">0.4%</td>
<td align="right">91.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">25,563,940</td>
<td align="right">0.4%</td>
<td align="right">91.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">24,802,390</td>
<td align="right">0.4%</td>
<td align="right">92.0%</td>
<td align="right">63.1%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">24,468,303</td>
<td align="right">0.4%</td>
<td align="right">92.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">23,959,132</td>
<td align="right">0.4%</td>
<td align="right">92.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">23,265,907</td>
<td align="right">0.4%</td>
<td align="right">93.1%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">22,451,627</td>
<td align="right">0.3%</td>
<td align="right">93.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">22,072,195</td>
<td align="right">0.3%</td>
<td align="right">93.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">20,873,807</td>
<td align="right">0.3%</td>
<td align="right">94.1%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">20,038,503</td>
<td align="right">0.3%</td>
<td align="right">94.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">18,427,904</td>
<td align="right">0.3%</td>
<td align="right">94.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">17,777,642</td>
<td align="right">0.3%</td>
<td align="right">95.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">17,371,296</td>
<td align="right">0.3%</td>
<td align="right">95.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">17,228,012</td>
<td align="right">0.3%</td>
<td align="right">95.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">15,589,333</td>
<td align="right">0.2%</td>
<td align="right">95.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">15,277,850</td>
<td align="right">0.2%</td>
<td align="right">96.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">15,005,857</td>
<td align="right">0.2%</td>
<td align="right">96.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">13,671,373</td>
<td align="right">0.2%</td>
<td align="right">96.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">13,031,468</td>
<td align="right">0.2%</td>
<td align="right">96.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">11,140,297</td>
<td align="right">0.2%</td>
<td align="right">96.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">10,922,823</td>
<td align="right">0.2%</td>
<td align="right">97.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">10,692,557</td>
<td align="right">0.2%</td>
<td align="right">97.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">10,313,748</td>
<td align="right">0.2%</td>
<td align="right">97.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">9,796,229</td>
<td align="right">0.2%</td>
<td align="right">97.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">9,596,428</td>
<td align="right">0.1%</td>
<td align="right">97.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">9,524,555</td>
<td align="right">0.1%</td>
<td align="right">97.8%</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">9,010,990</td>
<td align="right">0.1%</td>
<td align="right">97.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">8,288,139</td>
<td align="right">0.1%</td>
<td align="right">98.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">7,924,858</td>
<td align="right">0.1%</td>
<td align="right">98.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">6,516,168</td>
<td align="right">0.1%</td>
<td align="right">98.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">6,465,937</td>
<td align="right">0.1%</td>
<td align="right">98.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">6,447,090</td>
<td align="right">0.1%</td>
<td align="right">98.5%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">6,213,267</td>
<td align="right">0.1%</td>
<td align="right">98.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">6,020,182</td>
<td align="right">0.1%</td>
<td align="right">98.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">5,846,786</td>
<td align="right">0.1%</td>
<td align="right">98.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">5,730,383</td>
<td align="right">0.1%</td>
<td align="right">98.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">5,414,467</td>
<td align="right">0.1%</td>
<td align="right">98.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">5,122,300</td>
<td align="right">0.1%</td>
<td align="right">99.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">4,856,962</td>
<td align="right">0.1%</td>
<td align="right">99.1%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">3,987,472</td>
<td align="right">0.1%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">3,914,914</td>
<td align="right">0.1%</td>
<td align="right">99.2%</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">3,871,192</td>
<td align="right">0.1%</td>
<td align="right">99.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">3,753,635</td>
<td align="right">0.1%</td>
<td align="right">99.3%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">2,866,211</td>
<td align="right">0.0%</td>
<td align="right">99.3%</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">2,836,396</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">2,540,720</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">2,341,645</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">2,271,892</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">2,177,251</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">1,897,673</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">1,891,068</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">1,793,109</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,693,003</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">1,604,264</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">1,407,462</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,407,102</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">1,341,900</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">1,300,964</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">1,221,390</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">1,166,976</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">1,166,976</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">1,166,976</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">954,016</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">953,694</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">930,527</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">846,928</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">805,440</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">671,389</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">617,276</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">586,620</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">526,960</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">466,120</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">457,779</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">297,066</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">287,720</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">287,680</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">262,624</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">252,508</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">38.5%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">236,280</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">220,840</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">219,948</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">208,238</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">181,904</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">178,820</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_GETITEM</td>
<td align="right">177,144</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">175,840</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">143,500</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">140,852</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">94,916</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">87,360</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">74,840</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">47,562</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">42,660</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SET_ADD</td>
<td align="right">36,880</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">34,383</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_STR_INT</td>
<td align="right">19,500</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">12,768</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">6,680</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">6,620</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,680</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">3,100</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">2,660</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">2,540</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">2,480</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">2,040</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">1,840</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">1,204</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">800</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">620</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">120</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DICT_UPDATE</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
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

<table>
<thead>
<tr>
<th align="left">Pair</th>
<th align="right">Count</th>
<th align="right">Self</th>
<th align="right">Cumulative</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST LOAD_FAST</td>
<td align="right">220,160,637</td>
<td align="right">3.4%</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN LOAD_FAST</td>
<td align="right">170,192,792</td>
<td align="right">2.6%</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_FAST</td>
<td align="right">129,311,356</td>
<td align="right">2.0%</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_FAST</td>
<td align="right">126,885,655</td>
<td align="right">2.0%</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_FALSE</td>
<td align="right">116,316,311</td>
<td align="right">1.8%</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">CACHE RESUME_CHECK</td>
<td align="right">103,788,982</td>
<td align="right">1.6%</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE STORE_FAST_STORE_FAST</td>
<td align="right">102,092,526</td>
<td align="right">1.6%</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_SLOT</td>
<td align="right">99,893,130</td>
<td align="right">1.5%</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">86,212,743</td>
<td align="right">1.3%</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_GLOBAL_MODULE</td>
<td align="right">81,534,496</td>
<td align="right">1.3%</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_CONST</td>
<td align="right">79,348,161</td>
<td align="right">1.2%</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE INTERPRETER_EXIT</td>
<td align="right">77,031,878</td>
<td align="right">1.2%</td>
<td align="right">21.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_FAST_LOAD_FAST</td>
<td align="right">74,607,359</td>
<td align="right">1.1%</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">73,215,975</td>
<td align="right">1.1%</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD FOR_ITER</td>
<td align="right">70,947,126</td>
<td align="right">1.1%</td>
<td align="right">24.8%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE TO_BOOL_BOOL</td>
<td align="right">62,210,888</td>
<td align="right">1.0%</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR</td>
<td align="right">61,656,848</td>
<td align="right">0.9%</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left">PUSH_NULL LOAD_FAST</td>
<td align="right">61,649,326</td>
<td align="right">0.9%</td>
<td align="right">27.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST RETURN_VALUE</td>
<td align="right">61,208,416</td>
<td align="right">0.9%</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_GLOBAL_BUILTIN</td>
<td align="right">60,553,180</td>
<td align="right">0.9%</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_TRUE</td>
<td align="right">56,605,325</td>
<td align="right">0.9%</td>
<td align="right">30.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">56,518,591</td>
<td align="right">0.9%</td>
<td align="right">31.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS RESUME_CHECK</td>
<td align="right">54,072,999</td>
<td align="right">0.8%</td>
<td align="right">32.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD FOR_ITER_LIST</td>
<td align="right">53,368,798</td>
<td align="right">0.8%</td>
<td align="right">32.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST STORE_FAST</td>
<td align="right">49,817,867</td>
<td align="right">0.8%</td>
<td align="right">33.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST POP_JUMP_IF_NOT_NONE</td>
<td align="right">47,258,793</td>
<td align="right">0.7%</td>
<td align="right">34.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE JUMP_BACKWARD</td>
<td align="right">45,679,460</td>
<td align="right">0.7%</td>
<td align="right">35.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT TO_BOOL_BOOL</td>
<td align="right">45,356,022</td>
<td align="right">0.7%</td>
<td align="right">35.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE STORE_FAST</td>
<td align="right">45,206,447</td>
<td align="right">0.7%</td>
<td align="right">36.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT POP_JUMP_IF_FALSE</td>
<td align="right">44,576,136</td>
<td align="right">0.7%</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_GLOBAL_BUILTIN</td>
<td align="right">43,718,139</td>
<td align="right">0.7%</td>
<td align="right">37.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR STORE_FAST</td>
<td align="right">43,048,627</td>
<td align="right">0.7%</td>
<td align="right">38.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST LOAD_FAST</td>
<td align="right">42,803,996</td>
<td align="right">0.7%</td>
<td align="right">39.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST PUSH_NULL</td>
<td align="right">42,569,652</td>
<td align="right">0.7%</td>
<td align="right">39.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST LOAD_CONST</td>
<td align="right">42,115,959</td>
<td align="right">0.6%</td>
<td align="right">40.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_GLOBAL_BUILTIN</td>
<td align="right">39,387,336</td>
<td align="right">0.6%</td>
<td align="right">41.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE LOAD_FAST</td>
<td align="right">39,277,185</td>
<td align="right">0.6%</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_ATTR</td>
<td align="right">38,313,360</td>
<td align="right">0.6%</td>
<td align="right">42.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_FAST_LOAD_FAST</td>
<td align="right">38,088,393</td>
<td align="right">0.6%</td>
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST BINARY_SUBSCR_LIST_INT</td>
<td align="right">38,067,255</td>
<td align="right">0.6%</td>
<td align="right">43.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE CALL_ISINSTANCE</td>
<td align="right">37,287,233</td>
<td align="right">0.6%</td>
<td align="right">44.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT RETURN_VALUE</td>
<td align="right">34,919,609</td>
<td align="right">0.5%</td>
<td align="right">44.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT LOAD_FAST</td>
<td align="right">32,881,731</td>
<td align="right">0.5%</td>
<td align="right">45.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST INTERPRETER_EXIT</td>
<td align="right">32,852,005</td>
<td align="right">0.5%</td>
<td align="right">45.6%</td>
</tr>
<tr>
<td align="left">IS_OP POP_JUMP_IF_FALSE</td>
<td align="right">31,649,760</td>
<td align="right">0.5%</td>
<td align="right">46.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_FAST</td>
<td align="right">31,550,527</td>
<td align="right">0.5%</td>
<td align="right">46.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE RETURN_CONST</td>
<td align="right">30,499,022</td>
<td align="right">0.5%</td>
<td align="right">47.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">30,239,898</td>
<td align="right">0.5%</td>
<td align="right">47.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN LOAD_FAST_LOAD_FAST</td>
<td align="right">29,724,808</td>
<td align="right">0.5%</td>
<td align="right">48.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST STORE_SUBSCR_LIST_INT</td>
<td align="right">29,457,058</td>
<td align="right">0.5%</td>
<td align="right">48.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT POP_JUMP_IF_TRUE</td>
<td align="right">29,165,058</td>
<td align="right">0.4%</td>
<td align="right">48.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP POP_JUMP_IF_FALSE</td>
<td align="right">29,078,166</td>
<td align="right">0.4%</td>
<td align="right">49.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_PROPERTY</td>
<td align="right">28,584,713</td>
<td align="right">0.4%</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_LEN</td>
<td align="right">27,952,165</td>
<td align="right">0.4%</td>
<td align="right">50.2%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS RESUME_CHECK</td>
<td align="right">27,684,038</td>
<td align="right">0.4%</td>
<td align="right">50.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST COMPARE_OP_INT</td>
<td align="right">26,765,633</td>
<td align="right">0.4%</td>
<td align="right">51.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST CONTAINS_OP</td>
<td align="right">26,550,241</td>
<td align="right">0.4%</td>
<td align="right">51.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_BUILTIN_O</td>
<td align="right">26,124,053</td>
<td align="right">0.4%</td>
<td align="right">51.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST BUILD_TUPLE</td>
<td align="right">26,053,078</td>
<td align="right">0.4%</td>
<td align="right">52.3%</td>
</tr>
<tr>
<td align="left">POP_TOP JUMP_BACKWARD</td>
<td align="right">25,981,635</td>
<td align="right">0.4%</td>
<td align="right">52.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST CALL_BUILTIN_FAST</td>
<td align="right">25,736,568</td>
<td align="right">0.4%</td>
<td align="right">53.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE STORE_FAST</td>
<td align="right">25,071,878</td>
<td align="right">0.4%</td>
<td align="right">53.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP STORE_FAST</td>
<td align="right">24,621,219</td>
<td align="right">0.4%</td>
<td align="right">53.8%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE INTERPRETER_EXIT</td>
<td align="right">24,041,409</td>
<td align="right">0.4%</td>
<td align="right">54.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O STORE_FAST</td>
<td align="right">23,972,322</td>
<td align="right">0.4%</td>
<td align="right">54.6%</td>
</tr>
<tr>
<td align="left">DICT_MERGE CALL_FUNCTION_EX</td>
<td align="right">23,959,132</td>
<td align="right">0.4%</td>
<td align="right">54.9%</td>
</tr>
<tr>
<td align="left">BUILD_MAP LOAD_FAST</td>
<td align="right">23,887,634</td>
<td align="right">0.4%</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST DICT_MERGE</td>
<td align="right">23,830,228</td>
<td align="right">0.4%</td>
<td align="right">55.7%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">23,754,011</td>
<td align="right">0.4%</td>
<td align="right">56.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT STORE_FAST</td>
<td align="right">23,700,571</td>
<td align="right">0.4%</td>
<td align="right">56.4%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS RESUME_CHECK</td>
<td align="right">23,681,467</td>
<td align="right">0.4%</td>
<td align="right">56.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST LOAD_DEREF</td>
<td align="right">23,572,069</td>
<td align="right">0.4%</td>
<td align="right">57.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD FOR_ITER_TUPLE</td>
<td align="right">23,514,788</td>
<td align="right">0.4%</td>
<td align="right">57.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST GET_ITER</td>
<td align="right">23,470,403</td>
<td align="right">0.4%</td>
<td align="right">57.8%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK NOP</td>
<td align="right">23,011,122</td>
<td align="right">0.4%</td>
<td align="right">58.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST LOAD_GLOBAL_BUILTIN</td>
<td align="right">22,636,651</td>
<td align="right">0.3%</td>
<td align="right">58.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST TO_BOOL_BOOL</td>
<td align="right">22,282,044</td>
<td align="right">0.3%</td>
<td align="right">58.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE JUMP_BACKWARD</td>
<td align="right">22,065,051</td>
<td align="right">0.3%</td>
<td align="right">59.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST COMPARE_OP_INT</td>
<td align="right">21,677,869</td>
<td align="right">0.3%</td>
<td align="right">59.6%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE RETURN_VALUE</td>
<td align="right">21,660,078</td>
<td align="right">0.3%</td>
<td align="right">59.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST COMPARE_OP</td>
<td align="right">21,555,043</td>
<td align="right">0.3%</td>
<td align="right">60.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT CALL_PY_EXACT_ARGS</td>
<td align="right">21,367,142</td>
<td align="right">0.3%</td>
<td align="right">60.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_GLOBAL_BUILTIN</td>
<td align="right">21,138,924</td>
<td align="right">0.3%</td>
<td align="right">60.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_FAST_LOAD_FAST</td>
<td align="right">21,097,376</td>
<td align="right">0.3%</td>
<td align="right">61.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP POP_JUMP_IF_FALSE</td>
<td align="right">21,008,300</td>
<td align="right">0.3%</td>
<td align="right">61.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">20,596,150</td>
<td align="right">0.3%</td>
<td align="right">61.8%</td>
</tr>
<tr>
<td align="left">GET_ITER FOR_ITER</td>
<td align="right">20,503,969</td>
<td align="right">0.3%</td>
<td align="right">62.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK CONTAINS_OP_DICT</td>
<td align="right">20,048,322</td>
<td align="right">0.3%</td>
<td align="right">62.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY RESUME_CHECK</td>
<td align="right">19,921,170</td>
<td align="right">0.3%</td>
<td align="right">62.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">19,814,777</td>
<td align="right">0.3%</td>
<td align="right">63.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN CALL_ISINSTANCE</td>
<td align="right">19,616,540</td>
<td align="right">0.3%</td>
<td align="right">63.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_GLOBAL_MODULE</td>
<td align="right">18,994,460</td>
<td align="right">0.3%</td>
<td align="right">63.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST TO_BOOL_BOOL</td>
<td align="right">18,985,715</td>
<td align="right">0.3%</td>
<td align="right">64.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST TO_BOOL_INT</td>
<td align="right">18,673,913</td>
<td align="right">0.3%</td>
<td align="right">64.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST BUILD_TUPLE</td>
<td align="right">18,147,468</td>
<td align="right">0.3%</td>
<td align="right">64.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR IS_OP</td>
<td align="right">17,878,657</td>
<td align="right">0.3%</td>
<td align="right">64.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND JUMP_BACKWARD</td>
<td align="right">17,641,694</td>
<td align="right">0.3%</td>
<td align="right">65.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST CALL_BUILTIN_FAST</td>
<td align="right">17,608,644</td>
<td align="right">0.3%</td>
<td align="right">65.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_TYPE_1</td>
<td align="right">17,236,863</td>
<td align="right">0.3%</td>
<td align="right">65.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST BINARY_OP_ADD_INT</td>
<td align="right">17,234,090</td>
<td align="right">0.3%</td>
<td align="right">65.9%</td>
</tr>
</tbody>
</table>


</details>

## Predecessor/Successor Pairs

<details>
<summary> Top 5 predecessors and successors of each Tier 1 opcode. </summary>


This does not include the unspecialized instructions that occur after a
specialized instruction deoptimizes.

### BINARY_SLICE

<details>
<summary> Successors and predecessors for BINARY_SLICE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">52,400</td>
<td align="right">60.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">28,320</td>
<td align="right">32.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">6,320</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">320</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">40,720</td>
<td align="right">46.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">13,280</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">9,520</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,160</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">6,320</td>
<td align="right">7.2%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SLICE

<details>
<summary> Successors and predecessors for STORE_SLICE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">2,480</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">2,480</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### CACHE

<details>
<summary> Successors and predecessors for CACHE </summary>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">103,788,982</td>
<td align="right">77.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">14,794,111</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">13,976,375</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">1,608,954</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">15,818</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR

<details>
<summary> Successors and predecessors for BINARY_SUBSCR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">14,950,661</td>
<td align="right">55.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,271,694</td>
<td align="right">27.1%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,948,174</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,633,037</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">643,719</td>
<td align="right">2.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">7,377,440</td>
<td align="right">27.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,253,079</td>
<td align="right">27.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">6,949,295</td>
<td align="right">25.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,020,927</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">974,087</td>
<td align="right">3.6%</td>
</tr>
</tbody>
</table>


</details>

### CHECK_EXC_MATCH

<details>
<summary> Successors and predecessors for CHECK_EXC_MATCH </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">888,080</td>
<td align="right">76.1%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">180,284</td>
<td align="right">15.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">94,672</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,200</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">740</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,166,816</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### DELETE_SUBSCR

<details>
<summary> Successors and predecessors for DELETE_SUBSCR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,900</td>
<td align="right">61.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,200</td>
<td align="right">38.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,840</td>
<td align="right">59.4%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,200</td>
<td align="right">38.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">60</td>
<td align="right">1.9%</td>
</tr>
</tbody>
</table>


</details>

### END_SEND

<details>
<summary> Successors and predecessors for END_SEND </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">607,800</td>
<td align="right">75.5%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">175,680</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">21,960</td>
<td align="right">2.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">805,440</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### EXIT_INIT_CHECK

<details>
<summary> Successors and predecessors for EXIT_INIT_CHECK </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">953,694</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">953,694</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### FORMAT_SIMPLE

<details>
<summary> Successors and predecessors for FORMAT_SIMPLE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">287,680</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">143,320</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">109,880</td>
<td align="right">38.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">34,520</td>
<td align="right">12.0%</td>
</tr>
</tbody>
</table>


</details>

### GET_ITER

<details>
<summary> Successors and predecessors for GET_ITER </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">23,470,403</td>
<td align="right">37.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">14,744,008</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">11,079,346</td>
<td align="right">17.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,432,241</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">2,661,222</td>
<td align="right">4.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">20,503,969</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">13,893,109</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">10,709,914</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">9,520,322</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">5,100,107</td>
<td align="right">8.0%</td>
</tr>
</tbody>
</table>


</details>

### GET_YIELD_FROM_ITER

<details>
<summary> Successors and predecessors for GET_YIELD_FROM_ITER </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">632,728</td>
<td align="right">74.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">206,600</td>
<td align="right">24.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">7,520</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">846,928</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### INTERPRETER_EXIT

<details>
<summary> Successors and predecessors for INTERPRETER_EXIT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">77,031,878</td>
<td align="right">57.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">32,852,005</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">24,041,409</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">7,740</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_BUILD_CLASS

<details>
<summary> Successors and predecessors for LOAD_BUILD_CLASS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">2,220</td>
<td align="right">83.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">420</td>
<td align="right">15.8%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">20</td>
<td align="right">0.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">2,660</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_LOCALS

<details>
<summary> Successors and predecessors for LOAD_LOCALS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">2,540</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">2,540</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### MAKE_FUNCTION

<details>
<summary> Successors and predecessors for MAKE_FUNCTION </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">15,277,850</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">11,138,757</td>
<td align="right">72.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">2,737,926</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">701,035</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">587,696</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">33,580</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### NOP

<details>
<summary> Successors and predecessors for NOP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">23,011,122</td>
<td align="right">62.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">4,418,934</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">4,213,250</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,954,701</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,772,375</td>
<td align="right">4.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">13,446,508</td>
<td align="right">36.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">10,906,997</td>
<td align="right">29.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">6,989,632</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,678,242</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,530,012</td>
<td align="right">4.2%</td>
</tr>
</tbody>
</table>


</details>

### POP_EXCEPT

<details>
<summary> Successors and predecessors for POP_EXCEPT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SWAP</td>
<td align="right">527,039</td>
<td align="right">45.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">470,257</td>
<td align="right">40.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">165,640</td>
<td align="right">14.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">3,520</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">300</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">527,039</td>
<td align="right">45.2%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">250,920</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">244,877</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">86,220</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">53,040</td>
<td align="right">4.5%</td>
</tr>
</tbody>
</table>


</details>

### POP_TOP

<details>
<summary> Successors and predecessors for POP_TOP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">16,498,852</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">14,794,111</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">10,875,360</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">6,288,983</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">5,851,383</td>
<td align="right">8.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">25,981,635</td>
<td align="right">38.5%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">15,582,173</td>
<td align="right">23.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,621,992</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,367,343</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,839,183</td>
<td align="right">4.2%</td>
</tr>
</tbody>
</table>


</details>

### PUSH_EXC_INFO

<details>
<summary> Successors and predecessors for PUSH_EXC_INFO </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">486,969</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">305,651</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">133,832</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">98,700</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">69,120</td>
<td align="right">5.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,028,584</td>
<td align="right">88.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">133,352</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,200</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">1,840</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### PUSH_NULL

<details>
<summary> Successors and predecessors for PUSH_NULL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">42,569,652</td>
<td align="right">55.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">15,373,531</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">12,744,460</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">2,153,100</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">1,221,390</td>
<td align="right">1.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">61,649,326</td>
<td align="right">80.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">12,611,696</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,758,920</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">138,808</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">34,820</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### RETURN_GENERATOR

<details>
<summary> Successors and predecessors for RETURN_GENERATOR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">10,554,823</td>
<td align="right">67.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">4,836,090</td>
<td align="right">31.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">174,200</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">13,080</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">7,740</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">10,936,597</td>
<td align="right">70.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,738,798</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">856,296</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">632,728</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">169,240</td>
<td align="right">1.1%</td>
</tr>
</tbody>
</table>


</details>

### RETURN_VALUE

<details>
<summary> Successors and predecessors for RETURN_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">61,208,416</td>
<td align="right">31.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">34,919,609</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">21,660,078</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">16,052,105</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">11,998,731</td>
<td align="right">6.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">77,031,878</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">45,206,447</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">19,814,777</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">16,052,105</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,630,728</td>
<td align="right">2.9%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SUBSCR

<details>
<summary> Successors and predecessors for STORE_SUBSCR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,850,524</td>
<td align="right">96.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">93,200</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">25,680</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">10,760</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">3,900</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">3,831,044</td>
<td align="right">96.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">126,020</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">16,560</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">3,900</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">3,700</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL

<details>
<summary> Successors and predecessors for TO_BOOL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">10,405,300</td>
<td align="right">79.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,111,505</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">122,755</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">97,260</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">43,300</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">12,279,682</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">574,859</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">91,126</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">41,176</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">22,078</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### UNARY_NEGATIVE

<details>
<summary> Successors and predecessors for UNARY_NEGATIVE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">216,493</td>
<td align="right">32.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">130,271</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">109,280</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">107,760</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">62,527</td>
<td align="right">9.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">152,898</td>
<td align="right">22.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">119,120</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">108,762</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">107,760</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">80,854</td>
<td align="right">12.0%</td>
</tr>
</tbody>
</table>


</details>

### UNARY_NOT

<details>
<summary> Successors and predecessors for UNARY_NOT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">3,472,159</td>
<td align="right">64.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">1,168,019</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">682,998</td>
<td align="right">12.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">91,126</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">165</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">3,579,741</td>
<td align="right">66.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">918,927</td>
<td align="right">17.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">743,040</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">90,691</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">71,288</td>
<td align="right">1.3%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP

<details>
<summary> Successors and predecessors for BINARY_OP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">11,934,274</td>
<td align="right">33.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">6,424,820</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">6,317,240</td>
<td align="right">17.5%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">4,765,422</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,749,463</td>
<td align="right">7.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">24,621,219</td>
<td align="right">68.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,921,854</td>
<td align="right">16.4%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,580,560</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">1,141,534</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">885,081</td>
<td align="right">2.5%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_LIST

<details>
<summary> Successors and predecessors for BUILD_LIST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SWAP</td>
<td align="right">4,706,240</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">4,159,404</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,925,330</td>
<td align="right">17.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,411,970</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,605,086</td>
<td align="right">7.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">12,110,257</td>
<td align="right">53.9%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">4,706,240</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">2,350,718</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,485,842</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">762,752</td>
<td align="right">3.4%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_MAP

<details>
<summary> Successors and predecessors for BUILD_MAP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">12,868,876</td>
<td align="right">36.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">11,153,611</td>
<td align="right">32.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">4,778,802</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,684,420</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,316,040</td>
<td align="right">3.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">23,887,634</td>
<td align="right">68.5%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">4,778,802</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,565,861</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,588,880</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">743,200</td>
<td align="right">2.1%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_SET

<details>
<summary> Successors and predecessors for BUILD_SET </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">59,556</td>
<td align="right">62.7%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">35,280</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">80</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">59,556</td>
<td align="right">62.7%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">35,280</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">80</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_STRING

<details>
<summary> Successors and predecessors for BUILD_STRING </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">143,320</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">180</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">107,760</td>
<td align="right">75.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">16,000</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">16,000</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">3,420</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">300</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### BUILD_TUPLE

<details>
<summary> Successors and predecessors for BUILD_TUPLE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">26,053,078</td>
<td align="right">44.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">18,147,468</td>
<td align="right">30.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">5,117,656</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">3,115,364</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">2,488,600</td>
<td align="right">4.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">21,660,078</td>
<td align="right">36.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">11,182,181</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">11,153,611</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">4,765,222</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">3,278,800</td>
<td align="right">5.6%</td>
</tr>
</tbody>
</table>


</details>

### CALL

<details>
<summary> Successors and predecessors for CALL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">65,573</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">57,030</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">18,640</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">17,116</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">16,498</td>
<td align="right">6.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">29,580</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">24,849</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">21,600</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">19,958</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">13,709</td>
<td align="right">5.2%</td>
</tr>
</tbody>
</table>


</details>

### CALL_FUNCTION_EX

<details>
<summary> Successors and predecessors for CALL_FUNCTION_EX </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">23,959,132</td>
<td align="right">82.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,402,710</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,306,126</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">743,200</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">208,720</td>
<td align="right">0.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">13,133,992</td>
<td align="right">45.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">11,859,659</td>
<td align="right">41.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,586,280</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">655,232</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">488,000</td>
<td align="right">1.7%</td>
</tr>
</tbody>
</table>


</details>

### CALL_INTRINSIC_1

<details>
<summary> Successors and predecessors for CALL_INTRINSIC_1 </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">1,405,882</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">1,060</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">1,306,126</td>
<td align="right">92.8%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">99,916</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,060</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### CALL_KW

<details>
<summary> Successors and predecessors for CALL_KW </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">12,768</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">3,202</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,705</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">1,540</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">1,180</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">1,000</td>
<td align="right">7.8%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP

<details>
<summary> Successors and predecessors for COMPARE_OP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">21,555,043</td>
<td align="right">54.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,730,915</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">6,117,456</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,231,182</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">989,298</td>
<td align="right">2.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">21,008,300</td>
<td align="right">52.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">6,317,240</td>
<td align="right">15.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">6,317,160</td>
<td align="right">15.8%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">3,472,159</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,348,849</td>
<td align="right">5.9%</td>
</tr>
</tbody>
</table>


</details>

### CONTAINS_OP

<details>
<summary> Successors and predecessors for CONTAINS_OP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">26,550,241</td>
<td align="right">91.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,454,040</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">599,340</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">222,157</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">162,328</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">29,078,166</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">59,340</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">17,371</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">2,580</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,140</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CONVERT_VALUE

<details>
<summary> Successors and predecessors for CONVERT_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">171,680</td>
<td align="right">59.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">113,100</td>
<td align="right">39.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">2,520</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">300</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">287,680</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### COPY

<details>
<summary> Successors and predecessors for COPY </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,272,983</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">1,219,520</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">878,000</td>
<td align="right">17.1%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">525,660</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">265,276</td>
<td align="right">5.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">1,413,349</td>
<td align="right">27.6%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">1,219,520</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,208,120</td>
<td align="right">23.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">968,880</td>
<td align="right">18.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">84,076</td>
<td align="right">1.6%</td>
</tr>
</tbody>
</table>


</details>

### COPY_FREE_VARS

<details>
<summary> Successors and predecessors for COPY_FREE_VARS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CACHE</td>
<td align="right">13,976,375</td>
<td align="right">40.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">12,861,146</td>
<td align="right">37.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">5,470,335</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">1,258,456</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">277,271</td>
<td align="right">0.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">23,681,467</td>
<td align="right">69.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">10,554,823</td>
<td align="right">30.8%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">80,100</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">2,186</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### DELETE_FAST

<details>
<summary> Successors and predecessors for DELETE_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,315,200</td>
<td align="right">98.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">25,520</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">880</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">140</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">658,280</td>
<td align="right">49.1%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">657,600</td>
<td align="right">49.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">25,660</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### DICT_MERGE

<details>
<summary> Successors and predecessors for DICT_MERGE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">23,830,228</td>
<td align="right">99.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">128,904</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">23,959,132</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### EXTENDED_ARG

<details>
<summary> Successors and predecessors for EXTENDED_ARG </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">5,783,976</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">5,694,427</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">4,629,408</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">2,452,150</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,757,144</td>
<td align="right">8.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">7,295,490</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">5,903,864</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">5,780,098</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">1,775,560</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">657,440</td>
<td align="right">3.0%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER

<details>
<summary> Successors and predecessors for FOR_ITER </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">70,947,126</td>
<td align="right">66.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">20,503,969</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,133,281</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">7,776,754</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">86,088</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">73,215,975</td>
<td align="right">68.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">9,180,087</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">7,722,742</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">5,014,451</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">4,872,532</td>
<td align="right">4.5%</td>
</tr>
</tbody>
</table>


</details>

### IMPORT_FROM

<details>
<summary> Successors and predecessors for IMPORT_FROM </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">8,286,619</td>
<td align="right">86.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,086,605</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">194,664</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">26,000</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">2,540</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">7,375,376</td>
<td align="right">76.9%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">2,180,452</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">38,060</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">2,540</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### IMPORT_NAME

<details>
<summary> Successors and predecessors for IMPORT_NAME </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">8,288,119</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">8,286,619</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,060</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### IS_OP

<details>
<summary> Successors and predecessors for IS_OP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">17,878,657</td>
<td align="right">35.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">13,709,377</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">11,913,225</td>
<td align="right">23.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">6,010,604</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">550,664</td>
<td align="right">1.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">31,649,760</td>
<td align="right">62.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">13,697,237</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">5,047,681</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">22,940</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">12,160</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### JUMP_BACKWARD

<details>
<summary> Successors and predecessors for JUMP_BACKWARD </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">45,679,460</td>
<td align="right">25.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">25,981,635</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">22,065,051</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">17,641,694</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">15,780,499</td>
<td align="right">8.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">70,947,126</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">53,368,798</td>
<td align="right">29.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">23,514,788</td>
<td align="right">13.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">15,918,181</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">8,320,209</td>
<td align="right">4.7%</td>
</tr>
</tbody>
</table>


</details>

### JUMP_BACKWARD_NO_INTERRUPT

<details>
<summary> Successors and predecessors for JUMP_BACKWARD_NO_INTERRUPT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,504,720</td>
<td align="right">83.9%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">244,877</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">43,352</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">1,225,480</td>
<td align="right">68.3%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">279,400</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">184,765</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">54,896</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">34,240</td>
<td align="right">1.9%</td>
</tr>
</tbody>
</table>


</details>

### JUMP_FORWARD

<details>
<summary> Successors and predecessors for JUMP_FORWARD </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">4,349,536</td>
<td align="right">70.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">755,584</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">257,680</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">204,629</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">174,375</td>
<td align="right">2.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,116,619</td>
<td align="right">66.3%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">740,060</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">490,205</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">466,642</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">122,795</td>
<td align="right">2.0%</td>
</tr>
</tbody>
</table>


</details>

### LIST_APPEND

<details>
<summary> Successors and predecessors for LIST_APPEND </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,082,945</td>
<td align="right">47.7%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,592,508</td>
<td align="right">24.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">583,874</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">489,428</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">396,080</td>
<td align="right">6.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">6,460,977</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">4,800</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### LIST_EXTEND

<details>
<summary> Successors and predecessors for LIST_EXTEND </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,405,002</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,580</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,405,882</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">1,200</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR

<details>
<summary> Successors and predecessors for LOAD_ATTR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">61,656,848</td>
<td align="right">57.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">38,313,360</td>
<td align="right">35.6%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">4,351,904</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">2,354,018</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">303,116</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">43,048,627</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">17,878,657</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">15,373,531</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">14,189,569</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,248,241</td>
<td align="right">3.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_CONST

<details>
<summary> Successors and predecessors for LOAD_CONST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">79,348,161</td>
<td align="right">38.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">42,115,959</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">16,312,256</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">11,182,181</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">9,658,280</td>
<td align="right">4.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">42,115,959</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">25,736,568</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">21,677,869</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">17,234,090</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">15,277,850</td>
<td align="right">7.4%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_DEREF

<details>
<summary> Successors and predecessors for LOAD_DEREF </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">23,572,069</td>
<td align="right">32.1%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">10,906,997</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,179,558</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">7,271,694</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">4,808,536</td>
<td align="right">6.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">23,754,011</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">12,744,460</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">9,835,502</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">7,896,568</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">7,271,694</td>
<td align="right">9.9%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST

<details>
<summary> Successors and predecessors for LOAD_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">220,160,637</td>
<td align="right">20.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">170,192,792</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">129,311,356</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">126,885,655</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">61,649,326</td>
<td align="right">5.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">99,893,130</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">86,212,743</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">81,534,496</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">79,348,161</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">61,656,848</td>
<td align="right">5.8%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST_AND_CLEAR

<details>
<summary> Successors and predecessors for LOAD_FAST_AND_CLEAR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">GET_ITER</td>
<td align="right">9,520,322</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">7,707,610</td>
<td align="right">44.7%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SWAP</td>
<td align="right">9,520,242</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">7,707,610</td>
<td align="right">44.7%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST_CHECK

<details>
<summary> Successors and predecessors for LOAD_FAST_CHECK </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,580,100</td>
<td align="right">98.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">9,760</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">7,360</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,860</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">400</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,580,020</td>
<td align="right">98.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">7,680</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">7,360</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,460</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">2,640</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST_LOAD_FAST

<details>
<summary> Successors and predecessors for LOAD_FAST_LOAD_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">74,607,359</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">38,088,393</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">29,724,808</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">21,097,376</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">15,862,989</td>
<td align="right">5.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">38,067,255</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">29,457,058</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">26,765,633</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">26,550,241</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">26,053,078</td>
<td align="right">8.7%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_GLOBAL

<details>
<summary> Successors and predecessors for LOAD_GLOBAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">35,219</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">34,281</td>
<td align="right">18.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">26,749</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">10,931</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">10,782</td>
<td align="right">5.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">50,585</td>
<td align="right">27.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">41,238</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">39,572</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">14,079</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">9,830</td>
<td align="right">5.4%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_NAME

<details>
<summary> Successors and predecessors for LOAD_NAME </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">46,020</td>
<td align="right">25.7%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">43,200</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">36,000</td>
<td align="right">20.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">18,000</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">7,200</td>
<td align="right">4.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">43,200</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">35,920</td>
<td align="right">20.1%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">22,600</td>
<td align="right">12.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">19,660</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">18,340</td>
<td align="right">10.3%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_SPECIAL

<details>
<summary> Successors and predecessors for LOAD_SPECIAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COPY</td>
<td align="right">37,420</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">37,420</td>
<td align="right">50.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SWAP</td>
<td align="right">37,420</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">18,020</td>
<td align="right">24.1%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">17,560</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,840</td>
<td align="right">2.5%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_SUPER_ATTR

<details>
<summary> Successors and predecessors for LOAD_SUPER_ATTR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,084</td>
<td align="right">90.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">120</td>
<td align="right">10.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">500</td>
<td align="right">41.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">324</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">180</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">100</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">100</td>
<td align="right">8.3%</td>
</tr>
</tbody>
</table>


</details>

### MAKE_CELL

<details>
<summary> Successors and predecessors for MAKE_CELL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">2,454,908</td>
<td align="right">37.7%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">1,608,954</td>
<td align="right">24.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">892,126</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">683,200</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">593,149</td>
<td align="right">9.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">4,055,460</td>
<td align="right">62.2%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">2,454,908</td>
<td align="right">37.7%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">5,240</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">400</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### MAP_ADD

<details>
<summary> Successors and predecessors for MAP_ADD </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">7,911,698</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,160</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">3,620</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">1,900</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,840</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">7,924,518</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">340</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_FALSE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_FALSE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">116,316,311</td>
<td align="right">39.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">44,576,136</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">31,649,760</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">29,078,166</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">21,008,300</td>
<td align="right">7.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">129,311,356</td>
<td align="right">43.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">60,553,180</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">38,088,393</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">30,499,022</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">15,780,499</td>
<td align="right">5.3%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_NONE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_NONE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">7,377,440</td>
<td align="right">54.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,133,793</td>
<td align="right">37.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,134,296</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">10,324</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">8,380</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">7,386,225</td>
<td align="right">54.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,893,047</td>
<td align="right">21.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,172,552</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,072,134</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">876,595</td>
<td align="right">6.4%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_NOT_NONE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_NOT_NONE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">47,258,793</td>
<td align="right">96.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,340,202</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">191,620</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">11,040</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">7,360</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">22,065,051</td>
<td align="right">45.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">13,008,312</td>
<td align="right">26.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">10,036,215</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,058,763</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,478,763</td>
<td align="right">3.0%</td>
</tr>
</tbody>
</table>


</details>

### POP_JUMP_IF_TRUE

<details>
<summary> Successors and predecessors for POP_JUMP_IF_TRUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">56,605,325</td>
<td align="right">53.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">29,165,058</td>
<td align="right">27.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">9,275,129</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">5,047,681</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">2,348,849</td>
<td align="right">2.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">45,679,460</td>
<td align="right">43.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">39,277,185</td>
<td align="right">37.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,847,513</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">4,418,934</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">4,159,404</td>
<td align="right">3.9%</td>
</tr>
</tbody>
</table>


</details>

### RAISE_VARARGS

<details>
<summary> Successors and predecessors for RAISE_VARARGS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">137,252</td>
<td align="right">97.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">3,180</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">260</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">160</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">133,832</td>
<td align="right">97.4%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">3,360</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">160</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### RETURN_CONST

<details>
<summary> Successors and predecessors for RETURN_CONST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">30,499,022</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">10,602,542</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">6,207,381</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">4,872,532</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">3,831,044</td>
<td align="right">6.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">32,852,005</td>
<td align="right">53.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">10,875,360</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">9,658,280</td>
<td align="right">15.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,702,940</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,805,609</td>
<td align="right">2.9%</td>
</tr>
</tbody>
</table>


</details>

### SEND

<details>
<summary> Successors and predecessors for SEND </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">279,400</td>
<td align="right">59.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">182,220</td>
<td align="right">39.1%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">3,640</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">860</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">264,180</td>
<td align="right">56.7%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">175,680</td>
<td align="right">37.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">15,140</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">6,600</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">3,640</td>
<td align="right">0.8%</td>
</tr>
</tbody>
</table>


</details>

### SET_ADD

<details>
<summary> Successors and predecessors for SET_ADD </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">32,880</td>
<td align="right">89.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">3,960</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">40</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">36,880</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### SET_FUNCTION_ATTRIBUTE

<details>
<summary> Successors and predecessors for SET_FUNCTION_ATTRIBUTE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">11,138,757</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">1,540</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">10,452,655</td>
<td align="right">93.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">315,426</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">130,836</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">68,848</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">63,240</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>


</details>

### STORE_ATTR

<details>
<summary> Successors and predecessors for STORE_ATTR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">351,784</td>
<td align="right">76.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">98,500</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">3,757</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">3,726</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">12</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">135,992</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">134,832</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">91,583</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">74,060</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">4,000</td>
<td align="right">0.9%</td>
</tr>
</tbody>
</table>


</details>

### STORE_DEREF

<details>
<summary> Successors and predecessors for STORE_DEREF </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">4,553,060</td>
<td align="right">50.5%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">2,180,452</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,610,530</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">265,500</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">130,836</td>
<td align="right">1.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">4,552,700</td>
<td align="right">50.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,985,788</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,371,314</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">489,960</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">195,076</td>
<td align="right">2.2%</td>
</tr>
</tbody>
</table>


</details>

### STORE_FAST

<details>
<summary> Successors and predecessors for STORE_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">49,817,867</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">45,206,447</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">43,048,627</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">25,071,878</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">24,621,219</td>
<td align="right">6.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">220,160,637</td>
<td align="right">54.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">74,607,359</td>
<td align="right">18.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">39,387,336</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">18,994,460</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">9,594,243</td>
<td align="right">2.4%</td>
</tr>
</tbody>
</table>


</details>

### STORE_FAST_LOAD_FAST

<details>
<summary> Successors and predecessors for STORE_FAST_LOAD_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">4,246,516</td>
<td align="right">74.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">875,867</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">500,000</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">108,000</td>
<td align="right">1.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,382,172</td>
<td align="right">76.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">499,010</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">333,448</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">162,840</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">110,560</td>
<td align="right">1.9%</td>
</tr>
</tbody>
</table>


</details>

### STORE_FAST_STORE_FAST

<details>
<summary> Successors and predecessors for STORE_FAST_STORE_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">102,092,526</td>
<td align="right">93.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">3,317,026</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,492,963</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">805,179</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">418,880</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">42,803,996</td>
<td align="right">39.2%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">23,572,069</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">22,636,651</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">15,862,989</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,995,460</td>
<td align="right">1.8%</td>
</tr>
</tbody>
</table>


</details>

### STORE_NAME

<details>
<summary> Successors and predecessors for STORE_NAME </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">38,060</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">33,580</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">21,720</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">21,600</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">18,940</td>
<td align="right">10.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">51,480</td>
<td align="right">29.3%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">46,020</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">26,000</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">21,720</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">12,080</td>
<td align="right">6.9%</td>
</tr>
</tbody>
</table>


</details>

### SWAP

<details>
<summary> Successors and predecessors for SWAP </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">14,699,257</td>
<td align="right">28.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">9,520,242</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">7,722,742</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">4,778,802</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">4,706,240</td>
<td align="right">9.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">14,699,477</td>
<td align="right">28.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">8,170,390</td>
<td align="right">15.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">7,776,754</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">5,851,383</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">4,778,802</td>
<td align="right">9.2%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">10,452</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">6,803</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">6,340</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">6,140</td>
<td align="right">14.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,970</td>
<td align="right">9.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">18,673</td>
<td align="right">43.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">11,003</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">9,429</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,139</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">936</td>
<td align="right">2.2%</td>
</tr>
</tbody>
</table>


</details>

### YIELD_VALUE

<details>
<summary> Successors and predecessors for YIELD_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">IS_OP</td>
<td align="right">13,697,237</td>
<td align="right">53.6%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">7,203,140</td>
<td align="right">28.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,496,844</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,260,168</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">568,142</td>
<td align="right">2.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">24,041,409</td>
<td align="right">94.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,260,168</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">256,723</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">3,120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">2,520</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### RESUME

<details>
<summary> Successors and predecessors for RESUME </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CACHE</td>
<td align="right">15,818</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">11,056</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">6,015</td>
<td align="right">12.6%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">5,240</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,960</td>
<td align="right">8.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">17,693</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">10,782</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">8,762</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">3,700</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,360</td>
<td align="right">7.1%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_ADD_INT

<details>
<summary> Successors and predecessors for BINARY_OP_ADD_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">17,234,090</td>
<td align="right">93.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">592,580</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">422,960</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">84,915</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">52,642</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">14,694,933</td>
<td align="right">79.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,681,528</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,092,897</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">279,096</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">211,893</td>
<td align="right">1.1%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_ADD_UNICODE

<details>
<summary> Successors and predecessors for BINARY_OP_ADD_UNICODE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">488,560</td>
<td align="right">83.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">39,600</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">33,640</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">13,440</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">3,680</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">525,560</td>
<td align="right">89.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">43,280</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">6,720</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">6,720</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">3,120</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_MULTIPLY_INT

<details>
<summary> Successors and predecessors for BINARY_OP_MULTIPLY_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">1,705,598</td>
<td align="right">60.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">741,334</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">287,227</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">100,685</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,445</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">2,328,820</td>
<td align="right">82.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">185,720</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">181,166</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">95,626</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">37,361</td>
<td align="right">1.3%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_SUBTRACT_FLOAT

<details>
<summary> Successors and predecessors for BINARY_OP_SUBTRACT_FLOAT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">720</td>
<td align="right">90.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">80</td>
<td align="right">10.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">600</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">200</td>
<td align="right">25.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_SUBTRACT_INT

<details>
<summary> Successors and predecessors for BINARY_OP_SUBTRACT_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,587,133</td>
<td align="right">62.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">632,558</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">181,120</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">130,593</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">4,200</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">SWAP</td>
<td align="right">1,088,660</td>
<td align="right">42.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">736,046</td>
<td align="right">29.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">316,136</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">185,800</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">54,440</td>
<td align="right">2.1%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_DICT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_DICT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,365,439</td>
<td align="right">35.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,286,050</td>
<td align="right">33.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">650,480</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">443,840</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">116,321</td>
<td align="right">3.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,216,404</td>
<td align="right">31.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">829,530</td>
<td align="right">21.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">422,960</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">379,860</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">322,900</td>
<td align="right">8.3%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_GETITEM

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_GETITEM </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">80,480</td>
<td align="right">45.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">59,680</td>
<td align="right">33.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">36,264</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">720</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">177,142</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_LIST_INT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_LIST_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">38,067,255</td>
<td align="right">92.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">1,208,120</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,086,126</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">571,522</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">292,803</td>
<td align="right">0.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">14,761,957</td>
<td align="right">35.7%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">14,699,257</td>
<td align="right">35.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">8,004,721</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,208,580</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">527,723</td>
<td align="right">1.3%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_STR_INT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_STR_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">18,880</td>
<td align="right">96.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">600</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">20</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">18,880</td>
<td align="right">96.8%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">620</td>
<td align="right">3.2%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_SUBSCR_TUPLE_INT

<details>
<summary> Successors and predecessors for BINARY_SUBSCR_TUPLE_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">9,512,292</td>
<td align="right">97.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">280,561</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">2,776</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">480</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,332,799</td>
<td align="right">54.4%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,831,400</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">1,581,920</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">346,792</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">249,400</td>
<td align="right">2.5%</td>
</tr>
</tbody>
</table>


</details>

### CALL_ALLOC_AND_ENTER_INIT

<details>
<summary> Successors and predecessors for CALL_ALLOC_AND_ENTER_INIT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">931,676</td>
<td align="right">97.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">20,460</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,000</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">680</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">953,834</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">1</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BOUND_METHOD_EXACT_ARGS

<details>
<summary> Successors and predecessors for CALL_BOUND_METHOD_EXACT_ARGS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">14,694,933</td>
<td align="right">49.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">14,008,564</td>
<td align="right">47.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">512,189</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">168,120</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">150,880</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">27,684,038</td>
<td align="right">93.4%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">1,258,456</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">683,200</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">1,222</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">620</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BOUND_METHOD_GENERAL

<details>
<summary> Successors and predecessors for CALL_BOUND_METHOD_GENERAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">220,270</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">468</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">209,179</td>
<td align="right">94.7%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">11,661</td>
<td align="right">5.3%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BUILTIN_CLASS

<details>
<summary> Successors and predecessors for CALL_BUILTIN_CLASS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,014,836</td>
<td align="right">28.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">2,339,497</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,076,303</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">930,077</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">889,937</td>
<td align="right">8.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,909,683</td>
<td align="right">36.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">2,339,497</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">2,256,958</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">292,803</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">281,258</td>
<td align="right">2.6%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BUILTIN_FAST

<details>
<summary> Successors and predecessors for CALL_BUILTIN_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">25,736,568</td>
<td align="right">56.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">17,608,644</td>
<td align="right">38.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,737,832</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">484,440</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">75,424</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">18,985,715</td>
<td align="right">41.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">11,781,224</td>
<td align="right">25.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">10,405,300</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">2,153,100</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,904,228</td>
<td align="right">4.2%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BUILTIN_FAST_WITH_KEYWORDS

<details>
<summary> Successors and predecessors for CALL_BUILTIN_FAST_WITH_KEYWORDS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">4,968,102</td>
<td align="right">85.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">267,432</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">245,390</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">152,055</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">128,115</td>
<td align="right">2.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">4,765,222</td>
<td align="right">81.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">324,440</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">254,990</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">191,060</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">172,155</td>
<td align="right">2.9%</td>
</tr>
</tbody>
</table>


</details>

### CALL_BUILTIN_O

<details>
<summary> Successors and predecessors for CALL_BUILTIN_O </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">26,124,053</td>
<td align="right">52.9%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">10,936,597</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">5,999,905</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">4,934,670</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,141,534</td>
<td align="right">2.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">23,972,322</td>
<td align="right">48.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">11,998,731</td>
<td align="right">24.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">10,515,169</td>
<td align="right">21.3%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">2,661,222</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">55,420</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### CALL_ISINSTANCE

<details>
<summary> Successors and predecessors for CALL_ISINSTANCE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">37,287,233</td>
<td align="right">53.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">19,616,540</td>
<td align="right">28.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,896,568</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">3,150,327</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,691,480</td>
<td align="right">2.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">62,210,888</td>
<td align="right">88.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">7,203,140</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">525,660</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">164,016</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">9,662</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_KW_BOUND_METHOD

<details>
<summary> Successors and predecessors for CALL_KW_BOUND_METHOD </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">6,640</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">40</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,680</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_KW_NON_PY

<details>
<summary> Successors and predecessors for CALL_KW_NON_PY </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">928,987</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">1,540</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">722,330</td>
<td align="right">77.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">86,117</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">40,380</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">35,620</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">18,880</td>
<td align="right">2.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_KW_PY

<details>
<summary> Successors and predecessors for CALL_KW_PY </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">10,310,526</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">3,202</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">10,011,748</td>
<td align="right">97.1%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">277,180</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">13,080</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">11,640</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">80</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_LEN

<details>
<summary> Successors and predecessors for CALL_LEN </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">27,952,165</td>
<td align="right">96.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">633,000</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">206,600</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">124,578</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">94,560</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">10,417,745</td>
<td align="right">35.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">9,812,519</td>
<td align="right">33.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">7,590,551</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">930,077</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">101,548</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>


</details>

### CALL_LIST_APPEND

<details>
<summary> Successors and predecessors for CALL_LIST_APPEND </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">16,719,589</td>
<td align="right">68.3%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">3,278,800</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">1,831,400</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">1,580,020</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">697,188</td>
<td align="right">2.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">17,641,694</td>
<td align="right">72.1%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">4,629,408</td>
<td align="right">18.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,720,432</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">251,660</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">204,629</td>
<td align="right">0.8%</td>
</tr>
</tbody>
</table>


</details>

### CALL_METHOD_DESCRIPTOR_FAST

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_FAST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">16,501,777</td>
<td align="right">66.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,650,517</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">2,350,718</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">1,588,880</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">974,087</td>
<td align="right">3.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">13,742,117</td>
<td align="right">55.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,983,076</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">3,164,800</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,917,621</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">769,598</td>
<td align="right">3.1%</td>
</tr>
</tbody>
</table>


</details>

### CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">3,160</td>
<td align="right">47.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,540</td>
<td align="right">38.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">800</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">120</td>
<td align="right">1.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,480</td>
<td align="right">37.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,860</td>
<td align="right">28.1%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,200</td>
<td align="right">18.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">680</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">220</td>
<td align="right">3.3%</td>
</tr>
</tbody>
</table>


</details>

### CALL_METHOD_DESCRIPTOR_NOARGS

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_NOARGS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">30,239,898</td>
<td align="right">85.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">4,950,001</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">124,254</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">3,820</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">1,840</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">15,042,755</td>
<td align="right">42.6%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">14,744,008</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">4,968,102</td>
<td align="right">14.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">204,057</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">124,254</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>


</details>

### CALL_METHOD_DESCRIPTOR_O

<details>
<summary> Successors and predecessors for CALL_METHOD_DESCRIPTOR_O </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,909,280</td>
<td align="right">59.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,341,702</td>
<td align="right">27.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">368,040</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">112,400</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">44,300</td>
<td align="right">0.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,322,900</td>
<td align="right">68.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,339,702</td>
<td align="right">27.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">107,200</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">39,600</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">27,440</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>


</details>

### CALL_NON_PY_GENERAL

<details>
<summary> Successors and predecessors for CALL_NON_PY_GENERAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">9,736,803</td>
<td align="right">41.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,086,684</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">3,164,402</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">2,328,820</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,643,942</td>
<td align="right">7.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">GET_ITER</td>
<td align="right">11,079,346</td>
<td align="right">47.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,851,041</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,598,530</td>
<td align="right">19.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">697,188</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">261,520</td>
<td align="right">1.1%</td>
</tr>
</tbody>
</table>


</details>

### CALL_PY_EXACT_ARGS

<details>
<summary> Successors and predecessors for CALL_PY_EXACT_ARGS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">21,367,142</td>
<td align="right">29.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">17,079,201</td>
<td align="right">23.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">15,233,954</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">13,893,109</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">1,592,510</td>
<td align="right">2.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">54,072,999</td>
<td align="right">74.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">12,861,146</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">4,836,090</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">892,126</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">152,655</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### CALL_PY_GENERAL

<details>
<summary> Successors and predecessors for CALL_PY_GENERAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,296,088</td>
<td align="right">51.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,243,720</td>
<td align="right">34.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">198,495</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">165,990</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">128,160</td>
<td align="right">2.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">5,401,550</td>
<td align="right">83.8%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">593,149</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">277,271</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">174,200</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">420</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_STR_1

<details>
<summary> Successors and predecessors for CALL_STR_1 </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">147,120</td>
<td align="right">62.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">74,960</td>
<td align="right">31.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">14,020</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">180</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">222,140</td>
<td align="right">94.0%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">6,860</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">4,380</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">1,840</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">980</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>


</details>

### CALL_TUPLE_1

<details>
<summary> Successors and predecessors for CALL_TUPLE_1 </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">4,765,222</td>
<td align="right">79.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,076,444</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">148,948</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">7,920</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,328</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">4,765,422</td>
<td align="right">79.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">447,268</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">443,840</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">181,360</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">60,040</td>
<td align="right">1.0%</td>
</tr>
</tbody>
</table>


</details>

### CALL_TYPE_1

<details>
<summary> Successors and predecessors for CALL_TYPE_1 </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">17,236,863</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">131,512</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,081</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">6,670,727</td>
<td align="right">38.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">6,117,456</td>
<td align="right">35.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">4,351,904</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">75,772</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">55,800</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP_FLOAT

<details>
<summary> Successors and predecessors for COMPARE_OP_FLOAT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">535,023</td>
<td align="right">86.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">39,800</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">39,473</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,840</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">320</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">615,676</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">1,580</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP_INT

<details>
<summary> Successors and predecessors for COMPARE_OP_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">26,765,633</td>
<td align="right">44.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">21,677,869</td>
<td align="right">35.8%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">10,417,745</td>
<td align="right">17.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,067,534</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">238,706</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">44,576,136</td>
<td align="right">73.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">6,424,820</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">4,801,740</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">1,757,144</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,623,000</td>
<td align="right">2.7%</td>
</tr>
</tbody>
</table>


</details>

### COMPARE_OP_STR

<details>
<summary> Successors and predecessors for COMPARE_OP_STR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">10,236,800</td>
<td align="right">68.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">4,561,694</td>
<td align="right">30.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">198,263</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">6,360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,040</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">14,885,229</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">113,048</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">6,720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">860</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CONTAINS_OP_DICT

<details>
<summary> Successors and predecessors for CONTAINS_OP_DICT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">20,048,322</td>
<td align="right">61.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">7,236,425</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">5,367,090</td>
<td align="right">16.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">41,420</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">12,040</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">29,165,058</td>
<td align="right">89.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">3,551,819</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">720</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### CONTAINS_OP_SET

<details>
<summary> Successors and predecessors for CONTAINS_OP_SET </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">99,760</td>
<td align="right">45.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">79,460</td>
<td align="right">36.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">17,748</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">9,440</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">6,700</td>
<td align="right">3.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">113,720</td>
<td align="right">51.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">99,228</td>
<td align="right">45.1%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">3,820</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,180</td>
<td align="right">1.4%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER_LIST

<details>
<summary> Successors and predecessors for FOR_ITER_LIST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">53,368,798</td>
<td align="right">75.6%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">5,780,098</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">5,100,107</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,010,810</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,273,851</td>
<td align="right">1.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">49,817,867</td>
<td align="right">70.6%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">6,207,381</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">4,897,053</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">4,246,516</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,214,172</td>
<td align="right">6.0%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER_RANGE

<details>
<summary> Successors and predecessors for FOR_ITER_RANGE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">15,918,181</td>
<td align="right">89.5%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,130,461</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">657,440</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">38,880</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">31,280</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">16,083,961</td>
<td align="right">90.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">950,577</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">500,000</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">195,820</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">38,520</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER_TUPLE

<details>
<summary> Successors and predecessors for FOR_ITER_TUPLE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">23,514,788</td>
<td align="right">63.2%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">10,709,914</td>
<td align="right">28.8%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">1,775,560</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">724,678</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">430,837</td>
<td align="right">1.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">25,071,878</td>
<td align="right">67.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,749,524</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,208,940</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">875,867</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">786,444</td>
<td align="right">2.1%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_CLASS

<details>
<summary> Successors and predecessors for LOAD_ATTR_CLASS </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,986,651</td>
<td align="right">91.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">173,060</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">16,900</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">280</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,011,271</td>
<td align="right">92.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">149,840</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,080</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">6,320</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,620</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_CLASS_WITH_METACLASS_CHECK

<details>
<summary> Successors and predecessors for LOAD_ATTR_CLASS_WITH_METACLASS_CHECK </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">20,596,150</td>
<td align="right">98.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">209,480</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">58,960</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">3,517</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,460</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">20,048,322</td>
<td align="right">96.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">364,645</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">172,149</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">97,260</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">78,800</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_INSTANCE_VALUE

<details>
<summary> Successors and predecessors for LOAD_ATTR_INSTANCE_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">6,668,128</td>
<td align="right">61.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,178,039</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,175,499</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">968,880</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">889,937</td>
<td align="right">8.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,737,832</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,703,282</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">1,340,202</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,201,439</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,178,039</td>
<td align="right">10.8%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_METHOD_LAZY_DICT

<details>
<summary> Successors and predecessors for LOAD_ATTR_METHOD_LAZY_DICT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,840</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">1,840</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_METHOD_NO_DICT

<details>
<summary> Successors and predecessors for LOAD_ATTR_METHOD_NO_DICT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">86,212,743</td>
<td align="right">86.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,710,710</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">3,164,800</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,238,054</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,703,282</td>
<td align="right">1.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">32,881,731</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">30,239,898</td>
<td align="right">30.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">21,367,142</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">4,361,179</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">3,392,428</td>
<td align="right">3.4%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_METHOD_WITH_VALUES

<details>
<summary> Successors and predecessors for LOAD_ATTR_METHOD_WITH_VALUES </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">23,754,011</td>
<td align="right">70.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,944,615</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">4,769,862</td>
<td align="right">14.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">167,646</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">162,840</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">16,706,983</td>
<td align="right">49.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">11,738,692</td>
<td align="right">34.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">4,950,001</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">429,815</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">15,386</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_MODULE

<details>
<summary> Successors and predecessors for LOAD_ATTR_MODULE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,290,363</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,540</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">2,660</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,401</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,000</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,063,449</td>
<td align="right">81.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">84,417</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">57,200</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">26,100</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">15,920</td>
<td align="right">1.2%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_NONDESCRIPTOR_NO_DICT

<details>
<summary> Successors and predecessors for LOAD_ATTR_NONDESCRIPTOR_NO_DICT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">56,518,591</td>
<td align="right">92.4%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">3,145,700</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">361,960</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">333,448</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">252,273</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">45,356,022</td>
<td align="right">74.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">5,999,905</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">2,488,600</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,078,810</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">1,705,598</td>
<td align="right">2.8%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES

<details>
<summary> Successors and predecessors for LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,380,172</td>
<td align="right">60.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">485,860</td>
<td align="right">21.4%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">376,980</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">9,980</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">9,153</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">743,301</td>
<td align="right">32.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">484,440</td>
<td align="right">21.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">484,440</td>
<td align="right">21.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">215,200</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">108,120</td>
<td align="right">4.8%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_PROPERTY

<details>
<summary> Successors and predecessors for LOAD_ATTR_PROPERTY </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">28,584,713</td>
<td align="right">93.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">931,032</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">499,010</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">246,964</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">170,200</td>
<td align="right">0.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">19,921,170</td>
<td align="right">65.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">5,470,335</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">2,116,701</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">853,310</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">841,379</td>
<td align="right">2.7%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_ATTR_SLOT

<details>
<summary> Successors and predecessors for LOAD_ATTR_SLOT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">99,893,130</td>
<td align="right">99.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">665,329</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">106,300</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">74,086</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">35,476</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">34,919,609</td>
<td align="right">34.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">23,700,571</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,271,694</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,734,817</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,433,231</td>
<td align="right">5.4%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_GLOBAL_BUILTIN

<details>
<summary> Successors and predecessors for LOAD_GLOBAL_BUILTIN </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">60,553,180</td>
<td align="right">24.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">43,718,139</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">39,387,336</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">22,636,651</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">21,138,924</td>
<td align="right">8.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">170,192,792</td>
<td align="right">69.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">29,724,808</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">19,616,540</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">9,581,296</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">3,645,995</td>
<td align="right">1.5%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_GLOBAL_MODULE

<details>
<summary> Successors and predecessors for LOAD_GLOBAL_MODULE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">81,534,496</td>
<td align="right">53.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">18,994,460</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">16,854,578</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">10,206,159</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">6,989,632</td>
<td align="right">4.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">38,313,360</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">37,287,233</td>
<td align="right">24.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">31,550,527</td>
<td align="right">20.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">20,596,150</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">5,367,090</td>
<td align="right">3.5%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_SUPER_ATTR_ATTR

<details>
<summary> Successors and predecessors for LOAD_SUPER_ATTR_ATTR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,142,390</td>
<td align="right">93.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">78,900</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">100</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,221,390</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_SUPER_ATTR_METHOD

<details>
<summary> Successors and predecessors for LOAD_SUPER_ATTR_METHOD </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,897,173</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">500</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">1,592,510</td>
<td align="right">83.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">202,663</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">84,580</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">17,560</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">320</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### RESUME_CHECK

<details>
<summary> Successors and predecessors for RESUME_CHECK </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CACHE</td>
<td align="right">103,788,982</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">54,072,999</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">27,684,038</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">23,681,467</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">19,921,170</td>
<td align="right">7.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">126,885,655</td>
<td align="right">45.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">43,718,139</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">23,011,122</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">21,097,376</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">16,854,578</td>
<td align="right">6.0%</td>
</tr>
</tbody>
</table>


</details>

### SEND_GEN

<details>
<summary> Successors and predecessors for SEND_GEN </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">1,225,480</td>
<td align="right">64.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">664,708</td>
<td align="right">35.1%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">880</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,203,540</td>
<td align="right">63.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">642,688</td>
<td align="right">34.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">22,020</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">21,960</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">860</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### STORE_ATTR_INSTANCE_VALUE

<details>
<summary> Successors and predecessors for STORE_ATTR_INSTANCE_VALUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,267,915</td>
<td align="right">60.4%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">968,880</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">471,603</td>
<td align="right">12.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">41,217</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">4,000</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,294,193</td>
<td align="right">34.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,154,179</td>
<td align="right">30.7%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">486,340</td>
<td align="right">13.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">484,500</td>
<td align="right">12.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">122,720</td>
<td align="right">3.3%</td>
</tr>
</tbody>
</table>


</details>

### STORE_ATTR_SLOT

<details>
<summary> Successors and predecessors for STORE_ATTR_SLOT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">4,946,777</td>
<td align="right">51.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,529,633</td>
<td align="right">47.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">47,045</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">1,100</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,892,037</td>
<td align="right">51.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,370,496</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,982,731</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">162,786</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">48,860</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SUBSCR_DICT

<details>
<summary> Successors and predecessors for STORE_SUBSCR_DICT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,604,817</td>
<td align="right">68.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">412,369</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">181,360</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">86,040</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">48,617</td>
<td align="right">2.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">1,873,357</td>
<td align="right">80.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">237,949</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">174,761</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">45,037</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">4,120</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>


</details>

### STORE_SUBSCR_LIST_INT

<details>
<summary> Successors and predecessors for STORE_SUBSCR_LIST_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">29,457,058</td>
<td align="right">95.2%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,208,120</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">112,800</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">101,012</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">49,280</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">15,419,373</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">15,324,317</td>
<td align="right">49.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">160,200</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">21,140</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">21,060</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_ALWAYS_TRUE

<details>
<summary> Successors and predecessors for TO_BOOL_ALWAYS_TRUE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">249,184</td>
<td align="right">98.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">1,700</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">1,240</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">384</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">241,084</td>
<td align="right">95.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">9,673</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">1,700</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">51</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_BOOL

<details>
<summary> Successors and predecessors for TO_BOOL_BOOL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">62,210,888</td>
<td align="right">34.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">45,356,022</td>
<td align="right">25.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">22,282,044</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">18,985,715</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">10,515,169</td>
<td align="right">5.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">116,316,311</td>
<td align="right">64.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">56,605,325</td>
<td align="right">31.5%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">5,694,427</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">1,168,019</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">2,320</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_INT

<details>
<summary> Successors and predecessors for TO_BOOL_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">18,673,913</td>
<td align="right">93.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">755,306</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">486,860</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">64,599</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">37,032</td>
<td align="right">0.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">10,762,703</td>
<td align="right">53.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">9,275,129</td>
<td align="right">46.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">480</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">165</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_LIST

<details>
<summary> Successors and predecessors for TO_BOOL_LIST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,790,169</td>
<td align="right">97.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">39,560</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">11,536</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">9,546</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">8,780</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,300,339</td>
<td align="right">45.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">814,153</td>
<td align="right">28.4%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">682,998</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">61,000</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">7,361</td>
<td align="right">0.3%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_NONE

<details>
<summary> Successors and predecessors for TO_BOOL_NONE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,635,846</td>
<td align="right">67.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">545,631</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">488,700</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">107,200</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">84,881</td>
<td align="right">2.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">2,756,427</td>
<td align="right">70.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,129,167</td>
<td align="right">28.8%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">24,380</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">2,740</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,640</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### TO_BOOL_STR

<details>
<summary> Successors and predecessors for TO_BOOL_STR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">484,440</td>
<td align="right">91.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">26,080</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">14,040</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,120</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">160</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">493,620</td>
<td align="right">93.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">33,340</td>
<td align="right">6.3%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE_LIST

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE_LIST </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">140,798</td>
<td align="right">67.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">53,280</td>
<td align="right">25.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">4,200</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">3,360</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">1,880</td>
<td align="right">0.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">131,580</td>
<td align="right">63.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">76,658</td>
<td align="right">36.8%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE_TUPLE

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE_TUPLE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">923,660</td>
<td align="right">54.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">683,624</td>
<td align="right">40.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">79,520</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">3,680</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">1,139</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">1,492,963</td>
<td align="right">88.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">160,120</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">39,760</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### UNPACK_SEQUENCE_TWO_TUPLE

<details>
<summary> Successors and predecessors for UNPACK_SEQUENCE_TWO_TUPLE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">73,215,975</td>
<td align="right">68.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">19,814,777</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">8,004,721</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">4,897,053</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">786,444</td>
<td align="right">0.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">102,092,526</td>
<td align="right">95.4%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">4,553,060</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">296,428</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">18,940</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">3,360</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### END_FOR

<details>
<summary> Successors and predecessors for END_FOR </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">34,383</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">34,383</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### DELETE_NAME

<details>
<summary> Successors and predecessors for DELETE_NAME </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">80</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">20</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">20</td>
<td align="right">16.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">DELETE_NAME</td>
<td align="right">80</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">20</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">20</td>
<td align="right">16.7%</td>
</tr>
</tbody>
</table>


</details>

### RERAISE

<details>
<summary> Successors and predecessors for RERAISE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">3,520</td>
<td align="right">95.7%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">160</td>
<td align="right">4.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">320</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">160</td>
<td align="right">33.3%</td>
</tr>
</tbody>
</table>


</details>

### STORE_GLOBAL

<details>
<summary> Successors and predecessors for STORE_GLOBAL </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">20</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">20</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_ADD_FLOAT

<details>
<summary> Successors and predecessors for BINARY_OP_ADD_FLOAT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">600</td>
<td align="right">96.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">20</td>
<td align="right">3.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">620</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### FOR_ITER_GEN

<details>
<summary> Successors and predecessors for FOR_ITER_GEN </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">154,072</td>
<td align="right">51.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">142,894</td>
<td align="right">48.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">100</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">153,152</td>
<td align="right">51.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">142,734</td>
<td align="right">48.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">860</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">320</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_INPLACE_ADD_UNICODE

<details>
<summary> Successors and predecessors for BINARY_OP_INPLACE_ADD_UNICODE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,020</td>
<td align="right">99.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">20</td>
<td align="right">1.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,040</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### DICT_UPDATE

<details>
<summary> Successors and predecessors for DICT_UPDATE </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">20</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">20</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_MULTIPLY_FLOAT

<details>
<summary> Successors and predecessors for BINARY_OP_MULTIPLY_FLOAT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">40</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">20</td>
<td align="right">33.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">40</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">20</td>
<td align="right">33.3%</td>
</tr>
</tbody>
</table>


</details>


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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">36,058,183</td>
<td align="right">59.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">24,395,040</td>
<td align="right">40.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">6,730</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">53,532</td>
<td align="right">88.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">add other</td>
<td align="right">9,721</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">7,963</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">7,020</td>
<td align="right">13.1%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">4,160</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">4,024</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">3,740</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">3,061</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">2,683</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">2,420</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">2,409</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">2,123</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">1,312</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">1,289</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">623</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">396</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">320</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">265</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">3</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">87,360</td>
<td align="right">100.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">26,767,915</td>
<td align="right">32.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">55,152,080</td>
<td align="right">67.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">54,411</td>
<td align="right">0.1%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">8,536</td>
<td align="right">27.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">22,165</td>
<td align="right">72.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">other</td>
<td align="right">13,058</td>
<td align="right">58.9%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">3,720</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">2,307</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">buffer int</td>
<td align="right">1,780</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">1,280</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">20</td>
<td align="right">0.1%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">167,555</td>
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
<td align="right">44,800</td>
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
<td align="right">423,766,591</td>
<td align="right">92.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">33,529,315</td>
<td align="right">7.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">731,059</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">init not inline values</td>
<td align="right">260</td>
<td align="right">260 / 0 !!</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">7,986</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,220</td>
<td align="right">24.8%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">39,856,269</td>
<td align="right">34.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">75,585,424</td>
<td align="right">65.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">557,152</td>
<td align="right">0.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">19,939</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">72,476</td>
<td align="right">78.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">big int</td>
<td align="right">19,496</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">15,694</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">12,908</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">10,520</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">10,296</td>
<td align="right">14.2%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">2,262</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">360</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">320</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">300</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">240</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">80</td>
<td align="right">0.1%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">29,141,626</td>
<td align="right">46.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">32,938,185</td>
<td align="right">53.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,200</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">1,240</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">17,371</td>
<td align="right">93.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">other</td>
<td align="right">10,055</td>
<td align="right">57.9%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">5,756</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">1,220</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">340</td>
<td align="right">2.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">107,372,138</td>
<td align="right">46.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">124,080,967</td>
<td align="right">53.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,726,130</td>
<td align="right">0.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">44,448</td>
<td align="right">29.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">105,594</td>
<td align="right">70.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">dict items</td>
<td align="right">76,029</td>
<td align="right">72.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">9,933</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">7,660</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">4,352</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">2,880</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">1,980</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">1,660</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">920</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">100</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">80</td>
<td align="right">0.1%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">107,449,810</td>
<td align="right">22.8%</td>
</tr>
<tr>
<td align="left">
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">37,440</td>
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
<td align="right">289,988,381</td>
<td align="right">61.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">73,460,142</td>
<td align="right">15.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">1,471,457</td>
<td align="right">91.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">140,480</td>
<td align="right">8.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">mutable class</td>
<td align="right">65,611</td>
<td align="right">46.7%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">16,960</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">13,164</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">12,226</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">11,588</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">9,491</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">5,320</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">1,360</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">560</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">140</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">140</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">40</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">90,081</td>
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
<td align="right">397,374,647</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">20,380</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">91,983</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">604</td>
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
<td align="right">3,119,063</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">600</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">0</td>
<td align="right">0.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">461,600</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,846,228</td>
<td align="right">78.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">44,840</td>
<td align="right">1.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">880</td>
<td align="right">16.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">4,500</td>
<td align="right">83.6%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">list</td>
<td align="right">4,500</td>
<td align="right">100.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">448,953</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">10,776,456</td>
<td align="right">78.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,501,734</td>
<td align="right">18.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">52,165</td>
<td align="right">93.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">3,726</td>
<td align="right">6.7%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">class attr simple</td>
<td align="right">1,960</td>
<td align="right">52.6%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1,446</td>
<td align="right">38.8%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">260</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">60</td>
<td align="right">1.6%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">2,480</td>
<td align="right">100.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">3,980,850</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">33,291,595</td>
<td align="right">89.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">2,722</td>
<td align="right">41.1%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">3,900</td>
<td align="right">58.9%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">3,900</td>
<td align="right">100.0%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">12,947,679</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">206,250,994</td>
<td align="right">93.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">979,120</td>
<td align="right">0.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">69,871</td>
<td align="right">69.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">31,150</td>
<td align="right">30.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">tuple</td>
<td align="right">16,149</td>
<td align="right">51.8%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">3,963</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">3,686</td>
<td align="right">11.8%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">3,260</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">2,460</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">1,592</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">40</td>
<td align="right">0.1%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">30,476</td>
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
<td align="right">108,868,755</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Success</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Success</td>
<td align="right">11,388</td>
<td align="right">93.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">796</td>
<td align="right">6.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Failure kind</th>
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">sequence</td>
<td align="right">736</td>
<td align="right">92.5%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">60</td>
<td align="right">7.5%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
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
<td align="right">3,938,631,188</td>
<td align="right">60.6%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">365,723,369</td>
<td align="right">5.6%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">2,077,717,688</td>
<td align="right">32.0%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">112,878,764</td>
<td align="right">1.7%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">107,449,810</td>
<td align="right">29.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">107,372,138</td>
<td align="right">29.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">39,856,269</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">36,058,183</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">29,141,626</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">26,767,915</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">12,947,679</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">3,980,850</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">461,600</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">448,953</td>
<td align="right">0.1%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">39,442,646</td>
<td align="right">34.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">18,246,103</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">15,647,426</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">9,520,391</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">8,308,462</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">6,609,356</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">5,251,538</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">2,732,611</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">2,499,774</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">863,457</td>
<td align="right">0.8%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">134,191,980</td>
<td align="right">45.6%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">160,167,194</td>
<td align="right">54.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">134,191,980</td>
<td align="right">45.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">102,763,469</td>
<td align="right">34.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">31,428,511</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">4,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">102,756,169</td>
<td align="right">34.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">2,660</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">24,801,218</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">12,040,573</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">56,594,427</td>
<td align="right">19.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">6,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">1,639,794</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">261,719,803</td>
<td align="right">88.9%</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">374,589,473</td>
<td align="right">53.4%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">374,828,309</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">326,822,902</td>
<td align="right">46.6%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">325,694,882</td>
<td align="right">46.4%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">1,102,920</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">25,100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">341,426,692</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">1,509,055</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">2,776,437,458</td>
<td align="right">40.9%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">3,205,622,335</td>
<td align="right">42.3%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">1,500,597,589</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">1,687,836,228</td>
<td align="right">22.3%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">1,076,932,986</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">1,230,614,533</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">1,434,270,735</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">1,450,687,506</td>
<td align="right">19.2%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (too big)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (str subclass)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">220,102,773</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">4,537,783</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">6,064,355</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">362,115,015</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">1,532,089</td>
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
<th align="right">Collections</th>
<th align="right">Objects collected</th>
<th align="right">Object visits</th>
</tr>
</thead>
<tbody>
<tr>
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
</tr>
<tr>
<td align="right">2</td>
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
<th align="right">Count</th>
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
<th align="right">Count</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Number of data files</td>
<td align="right">80</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2024-10-18
