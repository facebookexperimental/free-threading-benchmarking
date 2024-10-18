
# Pystats results

- benchmark: sympy
- fork: colesbury
- ref: gh-125610-STORE_ATTR_INSTANCE_VALUE
- commit hash: 3a126a8
- commit date: 2024-10-16T19:41:13+00:00

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
<td align="right">1,065,144,959</td>
<td align="right">16.4%</td>
<td align="right">16.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">407,987,051</td>
<td align="right">6.3%</td>
<td align="right">22.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">299,712,777</td>
<td align="right">4.6%</td>
<td align="right">27.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">297,994,686</td>
<td align="right">4.6%</td>
<td align="right">31.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">278,588,413</td>
<td align="right">4.3%</td>
<td align="right">36.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">244,768,078</td>
<td align="right">3.8%</td>
<td align="right">39.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">207,702,257</td>
<td align="right">3.2%</td>
<td align="right">43.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">192,353,246</td>
<td align="right">3.0%</td>
<td align="right">46.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">179,791,273</td>
<td align="right">2.8%</td>
<td align="right">48.9%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">178,742,813</td>
<td align="right">2.8%</td>
<td align="right">51.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">152,627,042</td>
<td align="right">2.4%</td>
<td align="right">54.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">133,722,960</td>
<td align="right">2.1%</td>
<td align="right">56.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">108,942,719</td>
<td align="right">1.7%</td>
<td align="right">57.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">107,684,724</td>
<td align="right">1.7%</td>
<td align="right">59.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">107,361,921</td>
<td align="right">1.7%</td>
<td align="right">61.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">106,848,389</td>
<td align="right">1.6%</td>
<td align="right">62.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">106,191,364</td>
<td align="right">1.6%</td>
<td align="right">64.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">100,810,013</td>
<td align="right">1.6%</td>
<td align="right">65.9%</td>
<td align="right">39.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">99,449,147</td>
<td align="right">1.5%</td>
<td align="right">67.4%</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">76,269,649</td>
<td align="right">1.2%</td>
<td align="right">68.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">73,391,084</td>
<td align="right">1.1%</td>
<td align="right">69.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">73,001,674</td>
<td align="right">1.1%</td>
<td align="right">70.8%</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">70,581,903</td>
<td align="right">1.1%</td>
<td align="right">71.9%</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">70,124,625</td>
<td align="right">1.1%</td>
<td align="right">73.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">67,303,197</td>
<td align="right">1.0%</td>
<td align="right">74.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">63,476,972</td>
<td align="right">1.0%</td>
<td align="right">75.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">61,337,877</td>
<td align="right">0.9%</td>
<td align="right">75.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">61,138,653</td>
<td align="right">0.9%</td>
<td align="right">76.9%</td>
<td align="right">29.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">60,516,187</td>
<td align="right">0.9%</td>
<td align="right">77.8%</td>
<td align="right">0.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">58,824,937</td>
<td align="right">0.9%</td>
<td align="right">78.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">51,786,425</td>
<td align="right">0.8%</td>
<td align="right">79.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">50,233,850</td>
<td align="right">0.8%</td>
<td align="right">80.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">49,424,567</td>
<td align="right">0.8%</td>
<td align="right">81.1%</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">48,835,795</td>
<td align="right">0.8%</td>
<td align="right">81.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">45,724,449</td>
<td align="right">0.7%</td>
<td align="right">82.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">41,348,546</td>
<td align="right">0.6%</td>
<td align="right">83.2%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">40,015,320</td>
<td align="right">0.6%</td>
<td align="right">83.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">37,169,691</td>
<td align="right">0.6%</td>
<td align="right">84.3%</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">36,842,294</td>
<td align="right">0.6%</td>
<td align="right">84.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">36,117,615</td>
<td align="right">0.6%</td>
<td align="right">85.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">35,319,411</td>
<td align="right">0.5%</td>
<td align="right">86.0%</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">34,882,921</td>
<td align="right">0.5%</td>
<td align="right">86.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">34,325,861</td>
<td align="right">0.5%</td>
<td align="right">87.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">33,723,325</td>
<td align="right">0.5%</td>
<td align="right">87.6%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">32,719,560</td>
<td align="right">0.5%</td>
<td align="right">88.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">30,949,283</td>
<td align="right">0.5%</td>
<td align="right">88.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">30,653,954</td>
<td align="right">0.5%</td>
<td align="right">89.0%</td>
<td align="right">17.1%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">29,627,580</td>
<td align="right">0.5%</td>
<td align="right">89.5%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">29,238,687</td>
<td align="right">0.5%</td>
<td align="right">89.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">29,130,633</td>
<td align="right">0.4%</td>
<td align="right">90.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">28,949,787</td>
<td align="right">0.4%</td>
<td align="right">90.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">26,974,188</td>
<td align="right">0.4%</td>
<td align="right">91.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">25,354,663</td>
<td align="right">0.4%</td>
<td align="right">91.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">24,598,476</td>
<td align="right">0.4%</td>
<td align="right">92.0%</td>
<td align="right">62.7%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">24,467,667</td>
<td align="right">0.4%</td>
<td align="right">92.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">23,959,118</td>
<td align="right">0.4%</td>
<td align="right">92.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">23,265,751</td>
<td align="right">0.4%</td>
<td align="right">93.1%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">22,451,973</td>
<td align="right">0.3%</td>
<td align="right">93.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">22,072,350</td>
<td align="right">0.3%</td>
<td align="right">93.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">20,874,150</td>
<td align="right">0.3%</td>
<td align="right">94.1%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">20,036,216</td>
<td align="right">0.3%</td>
<td align="right">94.4%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">18,426,914</td>
<td align="right">0.3%</td>
<td align="right">94.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">17,777,281</td>
<td align="right">0.3%</td>
<td align="right">95.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">17,371,499</td>
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
<td align="right">15,596,462</td>
<td align="right">0.2%</td>
<td align="right">95.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">15,285,028</td>
<td align="right">0.2%</td>
<td align="right">96.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">15,005,572</td>
<td align="right">0.2%</td>
<td align="right">96.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">13,748,999</td>
<td align="right">0.2%</td>
<td align="right">96.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">13,031,416</td>
<td align="right">0.2%</td>
<td align="right">96.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">11,147,336</td>
<td align="right">0.2%</td>
<td align="right">96.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">10,922,731</td>
<td align="right">0.2%</td>
<td align="right">97.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">10,691,279</td>
<td align="right">0.2%</td>
<td align="right">97.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">10,313,568</td>
<td align="right">0.2%</td>
<td align="right">97.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">9,796,303</td>
<td align="right">0.2%</td>
<td align="right">97.5%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">9,595,825</td>
<td align="right">0.1%</td>
<td align="right">97.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">9,523,886</td>
<td align="right">0.1%</td>
<td align="right">97.8%</td>
<td align="right">26.3%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">9,011,046</td>
<td align="right">0.1%</td>
<td align="right">97.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">8,287,696</td>
<td align="right">0.1%</td>
<td align="right">98.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">7,924,735</td>
<td align="right">0.1%</td>
<td align="right">98.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">6,516,265</td>
<td align="right">0.1%</td>
<td align="right">98.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">6,466,106</td>
<td align="right">0.1%</td>
<td align="right">98.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">6,446,505</td>
<td align="right">0.1%</td>
<td align="right">98.5%</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">6,212,756</td>
<td align="right">0.1%</td>
<td align="right">98.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">6,020,134</td>
<td align="right">0.1%</td>
<td align="right">98.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">5,846,182</td>
<td align="right">0.1%</td>
<td align="right">98.7%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">5,730,591</td>
<td align="right">0.1%</td>
<td align="right">98.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">5,414,486</td>
<td align="right">0.1%</td>
<td align="right">98.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">5,122,239</td>
<td align="right">0.1%</td>
<td align="right">99.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">4,857,020</td>
<td align="right">0.1%</td>
<td align="right">99.1%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">3,987,805</td>
<td align="right">0.1%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">3,915,022</td>
<td align="right">0.1%</td>
<td align="right">99.2%</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">3,870,845</td>
<td align="right">0.1%</td>
<td align="right">99.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">3,753,690</td>
<td align="right">0.1%</td>
<td align="right">99.3%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">2,866,241</td>
<td align="right">0.0%</td>
<td align="right">99.3%</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">2,836,419</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">2,540,101</td>
<td align="right">0.0%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">2,341,684</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">2,273,652</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right">27.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">2,177,125</td>
<td align="right">0.0%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">1,897,725</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">1,891,036</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">1,793,061</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,692,203</td>
<td align="right">0.0%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">1,604,269</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">1,407,539</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,407,179</td>
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
<td align="right">1,300,435</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">1,221,420</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">1,166,905</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">1,166,905</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">1,166,905</td>
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
<td align="right">953,684</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">930,561</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">846,896</td>
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
<td align="right">671,394</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">617,266</td>
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
<td align="right">457,838</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">297,178</td>
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
<td align="right">262,890</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">252,548</td>
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
<td align="right">220,634</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">219,957</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">208,257</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">182,244</td>
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
<td align="right">177,148</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
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
<td align="right">140,866</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">94,959</td>
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
<td align="right">47,619</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">42,755</td>
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
<td align="right">34,425</td>
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
<td align="right">12,776</td>
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
<td align="right">1,208</td>
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
<td align="right">220,157,285</td>
<td align="right">3.4%</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN LOAD_FAST</td>
<td align="right">170,198,644</td>
<td align="right">2.6%</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_FAST</td>
<td align="right">129,316,852</td>
<td align="right">2.0%</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_FAST</td>
<td align="right">126,890,934</td>
<td align="right">2.0%</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_FALSE</td>
<td align="right">116,314,408</td>
<td align="right">1.8%</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">CACHE RESUME_CHECK</td>
<td align="right">103,572,240</td>
<td align="right">1.6%</td>
<td align="right">13.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE STORE_FAST_STORE_FAST</td>
<td align="right">101,973,380</td>
<td align="right">1.6%</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_SLOT</td>
<td align="right">99,886,243</td>
<td align="right">1.5%</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">86,220,270</td>
<td align="right">1.3%</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_GLOBAL_MODULE</td>
<td align="right">81,532,556</td>
<td align="right">1.3%</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_CONST</td>
<td align="right">79,344,591</td>
<td align="right">1.2%</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE INTERPRETER_EXIT</td>
<td align="right">77,031,707</td>
<td align="right">1.2%</td>
<td align="right">21.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_FAST_LOAD_FAST</td>
<td align="right">74,613,242</td>
<td align="right">1.1%</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">73,074,954</td>
<td align="right">1.1%</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD FOR_ITER</td>
<td align="right">70,805,358</td>
<td align="right">1.1%</td>
<td align="right">24.8%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE TO_BOOL_BOOL</td>
<td align="right">62,210,562</td>
<td align="right">1.0%</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR</td>
<td align="right">61,656,468</td>
<td align="right">0.9%</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left">PUSH_NULL LOAD_FAST</td>
<td align="right">61,646,200</td>
<td align="right">0.9%</td>
<td align="right">27.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST RETURN_VALUE</td>
<td align="right">61,207,441</td>
<td align="right">0.9%</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_GLOBAL_BUILTIN</td>
<td align="right">60,552,860</td>
<td align="right">0.9%</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_TRUE</td>
<td align="right">56,612,100</td>
<td align="right">0.9%</td>
<td align="right">30.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">56,520,950</td>
<td align="right">0.9%</td>
<td align="right">31.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS RESUME_CHECK</td>
<td align="right">54,149,305</td>
<td align="right">0.8%</td>
<td align="right">32.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD FOR_ITER_LIST</td>
<td align="right">53,391,336</td>
<td align="right">0.8%</td>
<td align="right">32.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST STORE_FAST</td>
<td align="right">49,818,160</td>
<td align="right">0.8%</td>
<td align="right">33.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST POP_JUMP_IF_NOT_NONE</td>
<td align="right">47,273,235</td>
<td align="right">0.7%</td>
<td align="right">34.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE JUMP_BACKWARD</td>
<td align="right">45,687,472</td>
<td align="right">0.7%</td>
<td align="right">35.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT TO_BOOL_BOOL</td>
<td align="right">45,355,587</td>
<td align="right">0.7%</td>
<td align="right">35.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE STORE_FAST</td>
<td align="right">45,205,228</td>
<td align="right">0.7%</td>
<td align="right">36.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT POP_JUMP_IF_FALSE</td>
<td align="right">44,572,850</td>
<td align="right">0.7%</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_GLOBAL_BUILTIN</td>
<td align="right">43,717,945</td>
<td align="right">0.7%</td>
<td align="right">37.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR STORE_FAST</td>
<td align="right">43,048,347</td>
<td align="right">0.7%</td>
<td align="right">38.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST LOAD_FAST</td>
<td align="right">42,808,043</td>
<td align="right">0.7%</td>
<td align="right">39.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST PUSH_NULL</td>
<td align="right">42,567,024</td>
<td align="right">0.7%</td>
<td align="right">39.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST LOAD_CONST</td>
<td align="right">42,115,006</td>
<td align="right">0.6%</td>
<td align="right">40.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_GLOBAL_BUILTIN</td>
<td align="right">39,387,342</td>
<td align="right">0.6%</td>
<td align="right">41.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE LOAD_FAST</td>
<td align="right">39,275,724</td>
<td align="right">0.6%</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_ATTR</td>
<td align="right">38,313,160</td>
<td align="right">0.6%</td>
<td align="right">42.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_FAST_LOAD_FAST</td>
<td align="right">38,166,477</td>
<td align="right">0.6%</td>
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST BINARY_SUBSCR_LIST_INT</td>
<td align="right">38,073,603</td>
<td align="right">0.6%</td>
<td align="right">43.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE CALL_ISINSTANCE</td>
<td align="right">37,287,016</td>
<td align="right">0.6%</td>
<td align="right">44.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT RETURN_VALUE</td>
<td align="right">34,919,759</td>
<td align="right">0.5%</td>
<td align="right">44.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT LOAD_FAST</td>
<td align="right">32,880,802</td>
<td align="right">0.5%</td>
<td align="right">45.1%</td>
</tr>
<tr>
<td align="left">RETURN_CONST INTERPRETER_EXIT</td>
<td align="right">32,851,419</td>
<td align="right">0.5%</td>
<td align="right">45.6%</td>
</tr>
<tr>
<td align="left">IS_OP POP_JUMP_IF_FALSE</td>
<td align="right">31,649,698</td>
<td align="right">0.5%</td>
<td align="right">46.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_FAST</td>
<td align="right">31,549,635</td>
<td align="right">0.5%</td>
<td align="right">46.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE RETURN_CONST</td>
<td align="right">30,577,300</td>
<td align="right">0.5%</td>
<td align="right">47.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">30,239,562</td>
<td align="right">0.5%</td>
<td align="right">47.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN LOAD_FAST_LOAD_FAST</td>
<td align="right">29,724,437</td>
<td align="right">0.5%</td>
<td align="right">48.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST STORE_SUBSCR_LIST_INT</td>
<td align="right">29,456,389</td>
<td align="right">0.5%</td>
<td align="right">48.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT POP_JUMP_IF_TRUE</td>
<td align="right">29,165,386</td>
<td align="right">0.4%</td>
<td align="right">48.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP POP_JUMP_IF_FALSE</td>
<td align="right">29,156,597</td>
<td align="right">0.4%</td>
<td align="right">49.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_ATTR_PROPERTY</td>
<td align="right">28,586,914</td>
<td align="right">0.4%</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_LEN</td>
<td align="right">27,952,242</td>
<td align="right">0.4%</td>
<td align="right">50.2%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS RESUME_CHECK</td>
<td align="right">27,684,085</td>
<td align="right">0.4%</td>
<td align="right">50.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST COMPARE_OP_INT</td>
<td align="right">26,763,706</td>
<td align="right">0.4%</td>
<td align="right">51.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST CONTAINS_OP</td>
<td align="right">26,628,633</td>
<td align="right">0.4%</td>
<td align="right">51.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_BUILTIN_O</td>
<td align="right">26,122,152</td>
<td align="right">0.4%</td>
<td align="right">51.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST BUILD_TUPLE</td>
<td align="right">26,052,667</td>
<td align="right">0.4%</td>
<td align="right">52.3%</td>
</tr>
<tr>
<td align="left">POP_TOP JUMP_BACKWARD</td>
<td align="right">25,853,977</td>
<td align="right">0.4%</td>
<td align="right">52.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST CALL_BUILTIN_FAST</td>
<td align="right">25,736,190</td>
<td align="right">0.4%</td>
<td align="right">53.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE STORE_FAST</td>
<td align="right">25,071,883</td>
<td align="right">0.4%</td>
<td align="right">53.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP STORE_FAST</td>
<td align="right">24,620,992</td>
<td align="right">0.4%</td>
<td align="right">53.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O STORE_FAST</td>
<td align="right">23,970,411</td>
<td align="right">0.4%</td>
<td align="right">54.2%</td>
</tr>
<tr>
<td align="left">DICT_MERGE CALL_FUNCTION_EX</td>
<td align="right">23,959,118</td>
<td align="right">0.4%</td>
<td align="right">54.6%</td>
</tr>
<tr>
<td align="left">BUILD_MAP LOAD_FAST</td>
<td align="right">23,887,624</td>
<td align="right">0.4%</td>
<td align="right">54.9%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE INTERPRETER_EXIT</td>
<td align="right">23,832,094</td>
<td align="right">0.4%</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST DICT_MERGE</td>
<td align="right">23,830,210</td>
<td align="right">0.4%</td>
<td align="right">55.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT STORE_FAST</td>
<td align="right">23,700,631</td>
<td align="right">0.4%</td>
<td align="right">56.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS RESUME_CHECK</td>
<td align="right">23,681,715</td>
<td align="right">0.4%</td>
<td align="right">56.4%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">23,623,165</td>
<td align="right">0.4%</td>
<td align="right">56.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD FOR_ITER_TUPLE</td>
<td align="right">23,507,784</td>
<td align="right">0.4%</td>
<td align="right">57.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST GET_ITER</td>
<td align="right">23,477,432</td>
<td align="right">0.4%</td>
<td align="right">57.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST LOAD_DEREF</td>
<td align="right">23,441,276</td>
<td align="right">0.4%</td>
<td align="right">57.8%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK NOP</td>
<td align="right">23,011,317</td>
<td align="right">0.4%</td>
<td align="right">58.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST LOAD_GLOBAL_BUILTIN</td>
<td align="right">22,643,647</td>
<td align="right">0.3%</td>
<td align="right">58.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST TO_BOOL_BOOL</td>
<td align="right">22,281,810</td>
<td align="right">0.3%</td>
<td align="right">58.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE JUMP_BACKWARD</td>
<td align="right">22,069,972</td>
<td align="right">0.3%</td>
<td align="right">59.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST COMPARE_OP_INT</td>
<td align="right">21,676,526</td>
<td align="right">0.3%</td>
<td align="right">59.6%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE RETURN_VALUE</td>
<td align="right">21,659,525</td>
<td align="right">0.3%</td>
<td align="right">59.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST COMPARE_OP</td>
<td align="right">21,555,073</td>
<td align="right">0.3%</td>
<td align="right">60.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT CALL_PY_EXACT_ARGS</td>
<td align="right">21,366,393</td>
<td align="right">0.3%</td>
<td align="right">60.5%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_FAST_LOAD_FAST</td>
<td align="right">21,176,035</td>
<td align="right">0.3%</td>
<td align="right">60.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST LOAD_GLOBAL_BUILTIN</td>
<td align="right">21,138,567</td>
<td align="right">0.3%</td>
<td align="right">61.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP POP_JUMP_IF_FALSE</td>
<td align="right">21,085,405</td>
<td align="right">0.3%</td>
<td align="right">61.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">20,596,480</td>
<td align="right">0.3%</td>
<td align="right">61.8%</td>
</tr>
<tr>
<td align="left">GET_ITER FOR_ITER</td>
<td align="right">20,510,601</td>
<td align="right">0.3%</td>
<td align="right">62.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK CONTAINS_OP_DICT</td>
<td align="right">20,048,593</td>
<td align="right">0.3%</td>
<td align="right">62.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY RESUME_CHECK</td>
<td align="right">19,921,255</td>
<td align="right">0.3%</td>
<td align="right">62.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">19,814,764</td>
<td align="right">0.3%</td>
<td align="right">63.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN CALL_ISINSTANCE</td>
<td align="right">19,616,346</td>
<td align="right">0.3%</td>
<td align="right">63.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_GLOBAL_MODULE</td>
<td align="right">18,994,258</td>
<td align="right">0.3%</td>
<td align="right">63.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST TO_BOOL_BOOL</td>
<td align="right">18,985,413</td>
<td align="right">0.3%</td>
<td align="right">64.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST TO_BOOL_INT</td>
<td align="right">18,671,995</td>
<td align="right">0.3%</td>
<td align="right">64.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST BUILD_TUPLE</td>
<td align="right">18,174,196</td>
<td align="right">0.3%</td>
<td align="right">64.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR IS_OP</td>
<td align="right">17,878,692</td>
<td align="right">0.3%</td>
<td align="right">64.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND JUMP_BACKWARD</td>
<td align="right">17,641,036</td>
<td align="right">0.3%</td>
<td align="right">65.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST CALL_BUILTIN_FAST</td>
<td align="right">17,608,330</td>
<td align="right">0.3%</td>
<td align="right">65.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST CALL_TYPE_1</td>
<td align="right">17,237,051</td>
<td align="right">0.3%</td>
<td align="right">65.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST BINARY_OP_ADD_INT</td>
<td align="right">17,233,546</td>
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
<td align="right">103,572,240</td>
<td align="right">77.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">14,801,238</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">13,975,934</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">1,608,947</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">15,819</td>
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
<td align="right">15,107,082</td>
<td align="right">56.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,271,954</td>
<td align="right">27.0%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,967,888</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,633,003</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">643,769</td>
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
<td align="right">7,455,617</td>
<td align="right">27.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,331,385</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">6,949,634</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,030,784</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">983,944</td>
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
<td align="right">887,967</td>
<td align="right">76.1%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">180,312</td>
<td align="right">15.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">94,686</td>
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
<td align="right">1,166,745</td>
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
<td align="right">34,425</td>
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
<td align="right">34,425</td>
<td align="right">100.0%</td>
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
<td align="right">953,684</td>
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
<td align="right">953,684</td>
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
<td align="right">23,477,432</td>
<td align="right">37.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">14,743,956</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">11,079,364</td>
<td align="right">17.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,432,587</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">2,661,248</td>
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
<td align="right">20,510,601</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">13,900,268</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">10,708,479</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">9,520,382</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">5,104,757</td>
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
<td align="right">632,696</td>
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
<td align="right">846,896</td>
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
<td align="right">77,031,707</td>
<td align="right">57.6%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">32,851,419</td>
<td align="right">24.6%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">23,832,094</td>
<td align="right">17.8%</td>
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
<td align="right">15,285,028</td>
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
<td align="right">11,145,796</td>
<td align="right">72.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">2,737,980</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">701,030</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">587,768</td>
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
<td align="right">23,011,317</td>
<td align="right">62.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">4,418,923</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">4,213,352</td>
<td align="right">11.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,954,510</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,772,135</td>
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
<td align="right">13,446,669</td>
<td align="right">36.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">10,906,929</td>
<td align="right">29.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">6,989,331</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,678,268</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,530,040</td>
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
<td align="right">526,960</td>
<td align="right">45.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">470,265</td>
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
<td align="right">526,960</td>
<td align="right">45.2%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">250,990</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">244,815</td>
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
<td align="right">16,281,945</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">14,801,238</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">10,954,664</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">6,288,511</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">5,851,349</td>
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
<td align="right">25,853,977</td>
<td align="right">38.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">15,589,300</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,621,721</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,367,309</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,839,190</td>
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
<td align="right">486,891</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">305,616</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">133,846</td>
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
<td align="right">1,028,499</td>
<td align="right">88.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">133,366</td>
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
<td align="right">42,567,024</td>
<td align="right">55.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">15,373,514</td>
<td align="right">20.2%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">12,744,335</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">2,153,100</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">1,221,420</td>
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
<td align="right">61,646,200</td>
<td align="right">80.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">12,611,491</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,758,920</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">138,816</td>
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
<td align="right">10,561,854</td>
<td align="right">67.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">4,836,186</td>
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
<td align="right">10,943,667</td>
<td align="right">70.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">2,738,853</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">856,296</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">632,696</td>
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
<td align="right">61,207,441</td>
<td align="right">31.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">34,919,759</td>
<td align="right">18.2%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">21,659,525</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">16,051,128</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">11,998,734</td>
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
<td align="right">77,031,707</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">45,205,228</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">19,814,764</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">16,051,128</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,630,433</td>
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
<td align="right">3,850,849</td>
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
<td align="right">3,831,369</td>
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
<td align="right">2,111,442</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">122,647</td>
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
<td align="right">12,279,655</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">574,842</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">91,029</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">41,198</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">22,092</td>
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
<td align="right">216,469</td>
<td align="right">32.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">130,276</td>
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
<td align="right">62,533</td>
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
<td align="right">152,899</td>
<td align="right">22.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">119,120</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">108,764</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">107,760</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">80,821</td>
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
<td align="right">3,472,176</td>
<td align="right">64.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">1,168,094</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">683,017</td>
<td align="right">12.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">91,029</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">170</td>
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
<td align="right">3,579,812</td>
<td align="right">66.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">918,957</td>
<td align="right">17.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">743,040</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">90,599</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">71,298</td>
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
<td align="right">11,934,015</td>
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
<td align="right">4,765,353</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,749,485</td>
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
<td align="right">24,620,992</td>
<td align="right">68.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,921,683</td>
<td align="right">16.4%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,580,560</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">1,141,555</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">885,143</td>
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
<td align="right">4,706,369</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">4,159,408</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,925,393</td>
<td align="right">17.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,412,088</td>
<td align="right">10.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,605,105</td>
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
<td align="right">12,110,346</td>
<td align="right">53.9%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">4,706,369</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">2,350,737</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,485,919</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">762,754</td>
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
<td align="right">12,868,715</td>
<td align="right">36.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">11,153,639</td>
<td align="right">32.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">4,778,733</td>
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
<td align="right">23,887,624</td>
<td align="right">68.5%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">4,778,733</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,565,770</td>
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
<td align="right">59,599</td>
<td align="right">62.8%</td>
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
<td align="right">59,599</td>
<td align="right">62.8%</td>
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
<td align="right">26,052,667</td>
<td align="right">44.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">18,174,196</td>
<td align="right">30.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">5,117,590</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">3,115,281</td>
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
<td align="right">21,659,525</td>
<td align="right">36.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">11,189,224</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">11,153,639</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">4,765,153</td>
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
<td align="right">65,693</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">57,040</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">18,640</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">17,136</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">16,509</td>
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
<td align="right">24,895</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">21,600</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">20,031</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">13,720</td>
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
<td align="right">23,959,118</td>
<td align="right">82.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,402,752</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">1,306,185</td>
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
<td align="right">13,133,951</td>
<td align="right">45.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">11,859,748</td>
<td align="right">41.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,586,280</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">655,235</td>
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
<td align="right">1,405,959</td>
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
<td align="right">1,306,185</td>
<td align="right">92.8%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">99,934</td>
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
<td align="right">12,776</td>
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
<td align="right">3,204</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">1,703</td>
<td align="right">13.3%</td>
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
<td align="right">21,555,073</td>
<td align="right">53.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,809,113</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">6,117,464</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,229,969</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">989,117</td>
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
<td align="right">21,085,405</td>
<td align="right">52.7%</td>
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
<td align="right">3,472,176</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,348,778</td>
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
<td align="right">26,628,633</td>
<td align="right">91.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,454,040</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">599,340</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">222,188</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">162,336</td>
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
<td align="right">29,156,597</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">59,340</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">17,390</td>
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
<td align="right">1,273,008</td>
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
<td align="right">265,280</td>
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
<td align="right">1,413,233</td>
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
<td align="right">84,080</td>
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
<td align="right">13,975,934</td>
<td align="right">40.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">12,868,156</td>
<td align="right">37.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">5,470,990</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">1,258,492</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">277,283</td>
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
<td align="right">23,681,715</td>
<td align="right">69.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">10,561,854</td>
<td align="right">30.8%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">80,100</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">2,192</td>
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
<td align="right">23,830,210</td>
<td align="right">99.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">128,908</td>
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
<td align="right">23,959,118</td>
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
<td align="right">5,784,026</td>
<td align="right">26.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">5,694,351</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">4,629,417</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">2,452,183</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,757,149</td>
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
<td align="right">7,295,428</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">5,903,970</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">5,780,149</td>
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
<td align="right">70,805,358</td>
<td align="right">66.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">20,510,601</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,140,285</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">7,776,697</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">86,295</td>
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
<td align="right">73,074,954</td>
<td align="right">68.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">9,187,075</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">7,722,673</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">5,014,440</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">4,871,806</td>
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
<td align="right">8,286,176</td>
<td align="right">86.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,086,440</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">194,669</td>
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
<td align="right">7,374,737</td>
<td align="right">76.9%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">2,180,488</td>
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
<td align="right">8,287,676</td>
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
<td align="right">8,286,176</td>
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
<td align="right">17,878,692</td>
<td align="right">35.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">13,499,948</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">11,913,135</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">6,010,653</td>
<td align="right">12.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">550,670</td>
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
<td align="right">31,649,698</td>
<td align="right">63.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">13,487,810</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">5,047,754</td>
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
<td align="right">45,687,472</td>
<td align="right">25.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">25,853,977</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">22,069,972</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">17,641,036</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">15,769,521</td>
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
<td align="right">70,805,358</td>
<td align="right">39.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">53,391,336</td>
<td align="right">29.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">23,507,784</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">15,917,849</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">8,318,614</td>
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
<td align="right">244,815</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">43,366</td>
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
<td align="right">184,706</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">54,903</td>
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
<td align="right">4,349,086</td>
<td align="right">70.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">755,588</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">257,680</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">204,640</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">174,267</td>
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
<td align="right">4,116,264</td>
<td align="right">66.3%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">740,060</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">490,211</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">466,582</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">122,687</td>
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
<td align="right">3,082,995</td>
<td align="right">47.7%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,592,517</td>
<td align="right">24.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">583,774</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">489,436</td>
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
<td align="right">6,461,146</td>
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
<td align="right">1,405,079</td>
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
<td align="right">1,405,959</td>
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
<td align="right">61,656,468</td>
<td align="right">57.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">38,313,160</td>
<td align="right">35.6%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">4,351,994</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">2,354,037</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">303,123</td>
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
<td align="right">43,048,347</td>
<td align="right">40.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">17,878,692</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">15,373,514</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">14,189,328</td>
<td align="right">13.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,248,262</td>
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
<td align="right">79,344,591</td>
<td align="right">38.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">42,115,006</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">16,312,026</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">11,189,224</td>
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
<td align="right">42,115,006</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">25,736,190</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">21,676,526</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">17,233,546</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">15,285,028</td>
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
<td align="right">23,441,276</td>
<td align="right">31.9%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">10,906,929</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,179,661</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">7,271,954</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">4,808,555</td>
<td align="right">6.6%</td>
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
<td align="right">23,623,165</td>
<td align="right">32.2%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">12,744,335</td>
<td align="right">17.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">9,835,425</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">7,896,660</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">7,271,954</td>
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
<td align="right">220,157,285</td>
<td align="right">20.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">170,198,644</td>
<td align="right">16.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">129,316,852</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">126,890,934</td>
<td align="right">11.9%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">61,646,200</td>
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
<td align="right">99,886,243</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">86,220,270</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">81,532,556</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">79,344,591</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">61,656,468</td>
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
<td align="right">9,520,382</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">7,707,550</td>
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
<td align="right">9,520,302</td>
<td align="right">55.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">7,707,550</td>
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
<td align="right">74,613,242</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">38,166,477</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">29,724,437</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">21,176,035</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">15,862,875</td>
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
<td align="right">38,073,603</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">29,456,389</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">26,763,706</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">26,628,633</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">26,052,667</td>
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
<td align="right">35,297</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">34,338</td>
<td align="right">18.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">26,798</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">10,947</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">10,805</td>
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
<td align="right">50,701</td>
<td align="right">27.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">41,262</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">39,658</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">14,099</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">9,841</td>
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
<td align="right">1,088</td>
<td align="right">90.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">120</td>
<td align="right">9.9%</td>
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
<td align="right">41.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">328</td>
<td align="right">27.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">180</td>
<td align="right">14.9%</td>
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
<td align="right">2,455,020</td>
<td align="right">37.7%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">1,608,947</td>
<td align="right">24.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">892,112</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">683,168</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">593,170</td>
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
<td align="right">4,055,445</td>
<td align="right">62.2%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">2,455,020</td>
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
<td align="right">7,911,575</td>
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
<td align="right">7,924,395</td>
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
<td align="right">116,314,408</td>
<td align="right">39.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">44,572,850</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">31,649,698</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">29,156,597</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">21,085,405</td>
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
<td align="right">129,316,852</td>
<td align="right">43.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">60,552,860</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">38,166,477</td>
<td align="right">12.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">30,577,300</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">15,769,521</td>
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
<td align="right">7,455,617</td>
<td align="right">54.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,133,219</td>
<td align="right">37.3%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,134,314</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">10,329</td>
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
<td align="right">7,464,413</td>
<td align="right">54.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,892,665</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,172,568</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,071,973</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">876,515</td>
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
<td align="right">47,273,235</td>
<td align="right">96.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,340,260</td>
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
<td align="right">22,069,972</td>
<td align="right">45.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">13,008,308</td>
<td align="right">26.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">10,045,979</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,058,651</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,478,702</td>
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
<td align="right">56,612,100</td>
<td align="right">53.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">29,165,386</td>
<td align="right">27.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">9,273,185</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">5,047,754</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">2,348,778</td>
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
<td align="right">45,687,472</td>
<td align="right">43.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">39,275,724</td>
<td align="right">37.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,847,584</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">4,418,923</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">4,159,408</td>
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
<td align="right">137,266</td>
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
<td align="right">133,846</td>
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
<td align="right">30,577,300</td>
<td align="right">49.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">10,602,468</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">6,207,465</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">4,871,806</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">3,831,369</td>
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
<td align="right">32,851,419</td>
<td align="right">53.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">10,954,664</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">9,658,280</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,702,224</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,805,639</td>
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
<td align="right">11,145,796</td>
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
<td align="right">10,459,718</td>
<td align="right">93.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">315,444</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">130,854</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">68,816</td>
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
<td align="right">351,812</td>
<td align="right">76.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">98,500</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">3,770</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">3,732</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">24</td>
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
<td align="right">136,006</td>
<td align="right">29.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">134,846</td>
<td align="right">29.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">91,602</td>
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
<td align="right">2,180,488</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">1,610,545</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">265,500</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">130,854</td>
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
<td align="right">1,985,819</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,371,334</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">489,960</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">195,035</td>
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
<td align="right">49,818,160</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">45,205,228</td>
<td align="right">11.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">43,048,347</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">25,071,883</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">24,620,992</td>
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
<td align="right">220,157,285</td>
<td align="right">54.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">74,613,242</td>
<td align="right">18.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">39,387,342</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">18,994,258</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">9,593,979</td>
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
<td align="right">4,246,556</td>
<td align="right">74.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">876,033</td>
<td align="right">15.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">500,000</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">108,002</td>
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
<td align="right">4,382,208</td>
<td align="right">76.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">500,154</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">332,485</td>
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
<td align="right">101,973,380</td>
<td align="right">93.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">3,317,000</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,492,266</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">804,457</td>
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
<td align="right">42,808,043</td>
<td align="right">39.3%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">23,441,276</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">22,643,647</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">15,862,875</td>
<td align="right">14.6%</td>
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
<td align="right">14,698,920</td>
<td align="right">28.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">9,520,302</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">7,722,673</td>
<td align="right">14.9%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">4,778,733</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">4,706,369</td>
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
<td align="right">14,699,140</td>
<td align="right">28.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">8,170,402</td>
<td align="right">15.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">7,776,697</td>
<td align="right">15.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">5,851,349</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">4,778,733</td>
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
<td align="right">10,484</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">6,806</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">6,340</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">6,140</td>
<td align="right">14.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,001</td>
<td align="right">9.4%</td>
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
<td align="right">18,706</td>
<td align="right">43.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">11,040</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">9,438</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">1,158</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">933</td>
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
<td align="right">13,487,810</td>
<td align="right">53.2%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">7,203,239</td>
<td align="right">28.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,496,812</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,260,136</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">568,146</td>
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
<td align="right">23,832,094</td>
<td align="right">94.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,260,136</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">256,793</td>
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
<td align="right">15,819</td>
<td align="right">33.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">11,069</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">6,036</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">5,240</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,962</td>
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
<td align="right">17,716</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">10,805</td>
<td align="right">22.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">8,765</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">3,700</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,362</td>
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
<td align="right">17,233,546</td>
<td align="right">93.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">592,156</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_DICT</td>
<td align="right">422,960</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">84,807</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">52,644</td>
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
<td align="right">14,694,960</td>
<td align="right">79.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,681,221</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,092,910</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">278,886</td>
<td align="right">1.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">211,700</td>
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
<td align="right">1,705,596</td>
<td align="right">60.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">741,318</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">287,131</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">100,730</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,510</td>
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
<td align="right">185,637</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">181,172</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">95,632</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">37,352</td>
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
<td align="right">1,587,005</td>
<td align="right">62.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">632,040</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">181,120</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">130,594</td>
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
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">735,427</td>
<td align="right">29.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">316,080</td>
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
<td align="right">1,365,246</td>
<td align="right">35.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">1,285,996</td>
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
<td align="right">115,992</td>
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
<td align="right">1,216,320</td>
<td align="right">31.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">829,314</td>
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
<td align="right">36,268</td>
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
<td align="right">177,148</td>
<td align="right">100.0%</td>
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
<td align="right">38,073,603</td>
<td align="right">92.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">1,208,120</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,086,141</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">571,588</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">292,494</td>
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
<td align="right">14,761,620</td>
<td align="right">35.7%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">14,698,920</td>
<td align="right">35.5%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">8,011,743</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,208,580</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">527,414</td>
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
<td align="right">9,512,359</td>
<td align="right">97.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">280,552</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">2,792</td>
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
<td align="right">5,332,842</td>
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
<td align="right">346,795</td>
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
<td align="right">953,824</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">6</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">6</td>
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
<td align="right">14,694,960</td>
<td align="right">49.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">14,008,620</td>
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
<td align="right">27,684,085</td>
<td align="right">93.4%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">1,258,492</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">683,168</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">1,215</td>
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
<td align="right">220,054</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">476</td>
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
<td align="right">208,972</td>
<td align="right">94.7%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">11,662</td>
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
<td align="right">3,014,239</td>
<td align="right">28.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">2,339,486</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,076,336</td>
<td align="right">10.1%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">930,043</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">889,903</td>
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
<td align="right">3,909,460</td>
<td align="right">36.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">2,339,486</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">2,256,965</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">292,494</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">281,170</td>
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
<td align="right">25,736,190</td>
<td align="right">56.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">17,608,330</td>
<td align="right">38.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,737,810</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">484,440</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">75,428</td>
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
<td align="right">18,985,413</td>
<td align="right">41.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">11,780,994</td>
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
<td align="right">1,904,257</td>
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
<td align="right">4,968,033</td>
<td align="right">85.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">267,317</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">245,174</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">151,947</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">128,007</td>
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
<td align="right">4,765,153</td>
<td align="right">81.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">324,333</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">254,774</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">191,060</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">172,047</td>
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
<td align="right">26,122,152</td>
<td align="right">52.9%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">10,943,667</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">6,006,326</td>
<td align="right">12.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">4,928,287</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,141,555</td>
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
<td align="right">23,970,411</td>
<td align="right">48.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">11,998,734</td>
<td align="right">24.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">10,522,261</td>
<td align="right">21.3%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">2,661,248</td>
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
<td align="right">37,287,016</td>
<td align="right">53.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">19,616,346</td>
<td align="right">28.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,896,660</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">3,150,437</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,691,460</td>
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
<td align="right">62,210,562</td>
<td align="right">88.7%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">7,203,239</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">525,660</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">164,023</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">9,668</td>
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
<td align="right">929,021</td>
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
<td align="right">722,351</td>
<td align="right">77.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">86,130</td>
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
<td align="right">10,310,344</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">3,204</td>
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
<td align="right">10,011,568</td>
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
<td align="right">27,952,242</td>
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
<td align="right">124,609</td>
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
<td align="right">10,417,729</td>
<td align="right">35.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">9,812,495</td>
<td align="right">33.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">7,590,729</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">930,043</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">101,557</td>
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
<td align="right">16,718,938</td>
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
<td align="right">697,197</td>
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
<td align="right">17,641,036</td>
<td align="right">72.1%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">4,629,417</td>
<td align="right">18.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,720,434</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">251,660</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">204,640</td>
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
<td align="right">16,292,377</td>
<td align="right">66.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">2,650,138</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">2,350,737</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">1,588,880</td>
<td align="right">6.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">983,944</td>
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
<td align="left">LOAD_FAST</td>
<td align="right">13,532,688</td>
<td align="right">55.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,982,843</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">3,164,800</td>
<td align="right">12.9%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,927,504</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">769,617</td>
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
<td align="right">30,239,562</td>
<td align="right">85.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">4,949,936</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">124,253</td>
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
<td align="right">15,042,449</td>
<td align="right">42.6%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">14,743,956</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">4,968,033</td>
<td align="right">14.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">204,070</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">124,253</td>
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
<td align="right">1,341,760</td>
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
<td align="right">1,339,760</td>
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
<td align="right">9,736,787</td>
<td align="right">41.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,086,505</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">3,164,428</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">2,328,820</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,643,965</td>
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
<td align="right">11,079,364</td>
<td align="right">47.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">5,850,946</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,598,593</td>
<td align="right">19.8%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">697,197</td>
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
<td align="right">21,366,393</td>
<td align="right">29.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">17,078,508</td>
<td align="right">23.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">15,311,722</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">13,900,268</td>
<td align="right">19.0%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">1,592,541</td>
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
<td align="right">54,149,305</td>
<td align="right">74.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">12,868,156</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">4,836,186</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">892,112</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">152,680</td>
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
<td align="right">3,295,875</td>
<td align="right">51.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,243,732</td>
<td align="right">34.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">198,387</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">165,774</td>
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
<td align="right">5,400,932</td>
<td align="right">83.8%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">593,170</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">277,283</td>
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
<td align="right">4,765,153</td>
<td align="right">79.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,076,449</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">148,956</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">7,920</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,336</td>
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
<td align="right">4,765,353</td>
<td align="right">79.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">447,276</td>
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
<td align="right">17,237,051</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">131,526</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">1,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,082</td>
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
<td align="right">6,670,748</td>
<td align="right">38.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">6,117,464</td>
<td align="right">35.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">4,351,994</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">75,786</td>
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
<td align="right">535,301</td>
<td align="right">86.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">39,800</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">39,185</td>
<td align="right">6.3%</td>
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
<td align="right">615,666</td>
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
<td align="right">26,763,706</td>
<td align="right">44.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">21,676,526</td>
<td align="right">35.8%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">10,417,729</td>
<td align="right">17.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,067,518</td>
<td align="right">1.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">238,779</td>
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
<td align="right">44,572,850</td>
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
<td align="right">1,757,149</td>
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
<td align="right">4,561,488</td>
<td align="right">30.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">198,184</td>
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
<td align="right">14,884,888</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">113,104</td>
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
<td align="right">20,048,593</td>
<td align="right">61.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">7,236,493</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">5,366,874</td>
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
<td align="right">29,165,386</td>
<td align="right">89.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">3,551,614</td>
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
<td align="right">17,757</td>
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
<td align="right">99,237</td>
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
<td align="right">154,150</td>
<td align="right">51.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">142,928</td>
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
<td align="right">153,230</td>
<td align="right">51.6%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">142,768</td>
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
<td align="right">53,391,336</td>
<td align="right">75.6%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">5,780,149</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">5,104,757</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,010,879</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">1,273,885</td>
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
<td align="right">49,818,160</td>
<td align="right">70.6%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">6,207,465</td>
<td align="right">8.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">4,919,270</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">4,246,556</td>
<td align="right">6.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,214,228</td>
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
<td align="right">15,917,849</td>
<td align="right">89.5%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,130,432</td>
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
<td align="right">16,083,629</td>
<td align="right">90.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">950,543</td>
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
<td align="right">23,507,784</td>
<td align="right">63.2%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">10,708,479</td>
<td align="right">28.8%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">1,775,560</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">724,766</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">430,920</td>
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
<td align="right">25,071,883</td>
<td align="right">67.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,749,502</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,209,091</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">876,033</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">779,213</td>
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
<td align="right">1,986,525</td>
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
<td align="right">2,011,145</td>
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
<td align="right">20,596,480</td>
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
<td align="right">3,530</td>
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
<td align="right">20,048,593</td>
<td align="right">96.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">364,670</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">172,157</td>
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
<td align="right">6,668,190</td>
<td align="right">61.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,177,979</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,175,439</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">968,880</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">889,903</td>
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
<td align="right">1,737,810</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,703,340</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">1,340,260</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,201,379</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,177,979</td>
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
<td align="right">86,220,270</td>
<td align="right">86.7%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">4,710,565</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">3,164,800</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">2,237,893</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,703,340</td>
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
<td align="right">32,880,802</td>
<td align="right">33.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">30,239,562</td>
<td align="right">30.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">21,366,393</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">4,360,711</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">3,392,438</td>
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
<td align="right">23,623,165</td>
<td align="right">70.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,945,274</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">4,769,793</td>
<td align="right">14.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">167,654</td>
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
<td align="right">16,497,459</td>
<td align="right">48.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">11,817,263</td>
<td align="right">35.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">4,949,936</td>
<td align="right">14.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">430,543</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">15,421</td>
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
<td align="right">1,289,829</td>
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
<td align="right">1,406</td>
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
<td align="right">1,063,028</td>
<td align="right">81.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">84,307</td>
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
<td align="right">56,520,950</td>
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
<td align="right">332,485</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">252,397</td>
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
<td align="right">45,355,587</td>
<td align="right">74.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">6,006,326</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">2,488,600</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,079,003</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">1,705,596</td>
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
<td align="right">1,381,941</td>
<td align="right">60.8%</td>
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
<td align="right">9,190</td>
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
<td align="right">743,680</td>
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
<td align="right">215,197</td>
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
<td align="right">28,586,914</td>
<td align="right">93.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">930,998</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">500,154</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">246,968</td>
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
<td align="right">19,921,255</td>
<td align="right">65.0%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">5,470,990</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">2,116,499</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">853,561</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">841,314</td>
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
<td align="right">99,886,243</td>
<td align="right">99.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">665,410</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">106,316</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">74,006</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">35,480</td>
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
<td align="right">34,919,759</td>
<td align="right">34.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">23,700,631</td>
<td align="right">23.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,271,954</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">5,734,754</td>
<td align="right">5.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">5,432,731</td>
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
<td align="right">60,552,860</td>
<td align="right">24.7%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">43,717,945</td>
<td align="right">17.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">39,387,342</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">22,643,647</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">21,138,567</td>
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
<td align="right">170,198,644</td>
<td align="right">69.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">29,724,437</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">19,616,346</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">9,580,956</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">3,646,055</td>
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
<td align="right">81,532,556</td>
<td align="right">53.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">18,994,258</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">16,854,023</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">10,205,184</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">6,989,331</td>
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
<td align="right">38,313,160</td>
<td align="right">25.1%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">37,287,016</td>
<td align="right">24.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">31,549,635</td>
<td align="right">20.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">20,596,480</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">5,366,874</td>
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
<td align="right">1,142,420</td>
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
<td align="right">1,221,420</td>
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
<td align="right">1,897,225</td>
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
<td align="right">1,592,541</td>
<td align="right">83.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">202,684</td>
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
<td align="right">103,572,240</td>
<td align="right">37.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">54,149,305</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">27,684,085</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">23,681,715</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">19,921,255</td>
<td align="right">7.2%</td>
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
<td align="right">126,890,934</td>
<td align="right">45.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">43,717,945</td>
<td align="right">15.7%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">23,011,317</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">21,176,035</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">16,854,023</td>
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
<td align="right">664,676</td>
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
<td align="right">642,656</td>
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
<td align="right">2,267,936</td>
<td align="right">60.4%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">968,880</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">471,624</td>
<td align="right">12.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">41,230</td>
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
<td align="right">1,294,206</td>
<td align="right">34.5%</td>
</tr>
<tr>
<td align="left">RETURN_CONST</td>
<td align="right">1,154,200</td>
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
<td align="right">4,946,530</td>
<td align="right">51.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">4,529,204</td>
<td align="right">47.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">47,052</td>
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
<td align="right">4,891,790</td>
<td align="right">51.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">2,370,185</td>
<td align="right">24.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,982,605</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">162,794</td>
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
<td align="right">1,604,830</td>
<td align="right">68.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">412,380</td>
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
<td align="right">48,630</td>
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
<td align="right">1,873,370</td>
<td align="right">80.0%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">237,960</td>
<td align="right">10.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">174,762</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">45,050</td>
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
<td align="right">29,456,389</td>
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
<td align="right">101,014</td>
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
<td align="right">15,419,043</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">15,323,980</td>
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
<td align="right">249,224</td>
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
<td align="right">241,088</td>
<td align="right">95.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">9,708</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">1,700</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">52</td>
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
<td align="right">62,210,562</td>
<td align="right">34.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">45,355,587</td>
<td align="right">25.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">22,281,810</td>
<td align="right">12.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">18,985,413</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">10,522,261</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">116,314,408</td>
<td align="right">64.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">56,612,100</td>
<td align="right">31.5%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">5,694,351</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">1,168,094</td>
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
<td align="right">18,671,995</td>
<td align="right">93.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">754,953</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">486,860</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_TUPLE_INT</td>
<td align="right">64,588</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">37,014</td>
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
<td align="right">10,762,349</td>
<td align="right">53.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">9,273,185</td>
<td align="right">46.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">480</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">170</td>
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
<td align="right">2,790,180</td>
<td align="right">97.3%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">39,560</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">11,543</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">9,558</td>
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
<td align="right">1,300,327</td>
<td align="right">45.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">814,169</td>
<td align="right">28.4%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">683,017</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">61,000</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">7,368</td>
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
<td align="right">2,635,649</td>
<td align="right">67.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">546,142</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">489,771</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">107,200</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">83,584</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">2,756,491</td>
<td align="right">70.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,129,211</td>
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
<td align="right">140,817</td>
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
<td align="right">76,677</td>
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
<td align="right">922,816</td>
<td align="right">54.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">683,649</td>
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
<td align="right">1,158</td>
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
<td align="right">1,492,266</td>
<td align="right">88.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">160,017</td>
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
<td align="right">73,074,954</td>
<td align="right">68.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">19,814,764</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR_LIST_INT</td>
<td align="right">8,011,743</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">4,919,270</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">779,213</td>
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
<td align="right">101,973,380</td>
<td align="right">95.4%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">4,553,060</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">296,449</td>
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
<td align="right">36,057,187</td>
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
<td align="right">24,393,454</td>
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
<td align="right">6,840</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">53,588</td>
<td align="right">88.7%</td>
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
<td align="right">9,724</td>
<td align="right">18.1%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">7,966</td>
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
<td align="right">4,028</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">3,740</td>
<td align="right">7.0%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">3,082</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">2,686</td>
<td align="right">5.0%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">2,420</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">2,413</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">2,122</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">1,324</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">1,288</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">626</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">393</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">320</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">270</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">6</td>
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
<td align="right">26,944,380</td>
<td align="right">32.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">55,157,928</td>
<td align="right">67.1%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">54,414</td>
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
<td align="right">8,552</td>
<td align="right">27.8%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">22,216</td>
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
<td align="right">13,105</td>
<td align="right">59.0%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">3,720</td>
<td align="right">16.7%</td>
</tr>
<tr>
<td align="left">tuple slice</td>
<td align="right">2,311</td>
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
<td align="right">167,715</td>
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
<td align="right">423,860,920</td>
<td align="right">92.7%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">33,316,055</td>
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
<td align="right">727,151</td>
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
<td align="right">7,992</td>
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
<td align="right">39,933,136</td>
<td align="right">34.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">75,581,824</td>
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
<td align="right">557,201</td>
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
<td align="right">19,965</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">72,519</td>
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
<td align="right">19,498</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">15,702</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">12,914</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">10,520</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">10,300</td>
<td align="right">14.2%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">2,285</td>
<td align="right">3.2%</td>
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
<td align="right">29,220,057</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">32,938,317</td>
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
<td align="right">17,390</td>
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
<td align="right">10,068</td>
<td align="right">57.9%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">5,762</td>
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
<td align="right">107,243,959</td>
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
<td align="right">124,094,056</td>
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
<td align="right">1,731,997</td>
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
<td align="right">44,579</td>
<td align="right">29.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">105,920</td>
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
<td align="right">76,385</td>
<td align="right">72.1%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">9,904</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">7,660</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">4,351</td>
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
<td align="right">107,449,426</td>
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
<td align="right">289,857,867</td>
<td align="right">61.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">73,467,158</td>
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
<td align="right">1,471,620</td>
<td align="right">91.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">140,491</td>
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
<td align="right">65,615</td>
<td align="right">46.7%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">16,960</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">13,167</td>
<td align="right">9.4%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">12,227</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">11,592</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">9,490</td>
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
<td align="right">90,281</td>
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
<td align="right">397,374,740</td>
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
<td align="right">92,123</td>
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
<td align="right">608</td>
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
<td align="right">3,119,145</td>
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
<td align="right">1,846,196</td>
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
<td align="right">449,006</td>
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
<td align="right">10,775,201</td>
<td align="right">78.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">2,502,375</td>
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
<td align="right">52,172</td>
<td align="right">93.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">3,732</td>
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
<td align="right">52.5%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1,452</td>
<td align="right">38.9%</td>
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
<td align="right">3,981,181</td>
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
<td align="right">33,290,967</td>
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
<td align="right">2,724</td>
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
<td align="right">12,947,550</td>
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
<td align="right">206,253,569</td>
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
<td align="right">979,335</td>
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
<td align="right">69,934</td>
<td align="right">69.2%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">31,172</td>
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
<td align="right">16,110</td>
<td align="right">51.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">4,018</td>
<td align="right">12.9%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">3,695</td>
<td align="right">11.9%</td>
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
<td align="right">1,589</td>
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
<td align="right">30,546</td>
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
<td align="right">108,748,849</td>
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
<td align="right">11,416</td>
<td align="right">93.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">793</td>
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
<td align="right">733</td>
<td align="right">92.4%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">60</td>
<td align="right">7.6%</td>
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
<td align="right">3,937,928,533</td>
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
<td align="right">365,927,347</td>
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
<td align="right">2,077,441,418</td>
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
<td align="right">112,679,295</td>
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
<td align="right">107,449,426</td>
<td align="right">29.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">107,243,959</td>
<td align="right">29.4%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">39,933,136</td>
<td align="right">10.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">36,057,187</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">29,220,057</td>
<td align="right">8.0%</td>
</tr>
<tr>
<td align="left">BINARY_SUBSCR</td>
<td align="right">26,944,380</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">12,947,550</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">3,981,181</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">461,600</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">449,006</td>
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
<td align="right">39,442,192</td>
<td align="right">35.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">18,249,185</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">15,434,002</td>
<td align="right">13.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">9,520,168</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">8,308,770</td>
<td align="right">7.4%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">6,609,286</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">5,254,129</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">2,732,639</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">2,500,415</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">877,515</td>
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
<td align="right">133,981,918</td>
<td align="right">45.5%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">160,250,576</td>
<td align="right">54.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">133,981,918</td>
<td align="right">45.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">102,763,263</td>
<td align="right">34.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">31,218,655</td>
<td align="right">10.6%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">4,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">102,755,963</td>
<td align="right">34.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">2,660</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">24,801,185</td>
<td align="right">8.4%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">12,040,677</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">56,594,161</td>
<td align="right">19.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">6,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">1,639,709</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">261,802,889</td>
<td align="right">89.0%</td>
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
<td align="right">374,625,461</td>
<td align="right">53.4%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">374,864,303</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">326,858,026</td>
<td align="right">46.6%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">325,735,896</td>
<td align="right">46.4%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">1,097,030</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">25,100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">341,462,590</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">1,509,105</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">2,776,587,860</td>
<td align="right">40.9%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">3,205,685,453</td>
<td align="right">42.3%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">1,501,123,147</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">1,688,526,948</td>
<td align="right">22.3%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">1,076,637,722</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">1,230,344,839</td>
<td align="right">16.2%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">1,435,309,553</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">1,451,647,461</td>
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
<td align="right">219,717,745</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">4,928,202</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">6,539,308</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">362,265,130</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">1,616,280</td>
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
