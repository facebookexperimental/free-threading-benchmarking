
# Pystats results

- benchmark: hexiom
- fork: python
- ref: 47b01da4ccedd9c00fad4325b3e87d7732abeb6d
- commit hash: 47b01da
- commit date: 2025-07-12T21:15:04+03:00

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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">481,729,260</td>
<td align="right">16.7%</td>
<td align="right">16.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">198,187,320</td>
<td align="right">6.9%</td>
<td align="right">23.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">177,273,660</td>
<td align="right">6.1%</td>
<td align="right">29.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">149,888,640</td>
<td align="right">5.2%</td>
<td align="right">34.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">143,570,040</td>
<td align="right">5.0%</td>
<td align="right">39.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">141,756,300</td>
<td align="right">4.9%</td>
<td align="right">44.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">139,271,280</td>
<td align="right">4.8%</td>
<td align="right">49.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">136,020,840</td>
<td align="right">4.7%</td>
<td align="right">54.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">106,992,000</td>
<td align="right">3.7%</td>
<td align="right">58.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">87,654,240</td>
<td align="right">3.0%</td>
<td align="right">61.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">85,156,200</td>
<td align="right">3.0%</td>
<td align="right">64.1%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">77,554,620</td>
<td align="right">2.7%</td>
<td align="right">66.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">75,688,440</td>
<td align="right">2.6%</td>
<td align="right">69.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">72,764,660</td>
<td align="right">2.5%</td>
<td align="right">71.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">72,530,220</td>
<td align="right">2.5%</td>
<td align="right">74.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">70,414,080</td>
<td align="right">2.4%</td>
<td align="right">76.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">68,930,040</td>
<td align="right">2.4%</td>
<td align="right">79.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">65,527,740</td>
<td align="right">2.3%</td>
<td align="right">81.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">61,783,740</td>
<td align="right">2.1%</td>
<td align="right">83.7%</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">59,520,660</td>
<td align="right">2.1%</td>
<td align="right">85.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">57,446,760</td>
<td align="right">2.0%</td>
<td align="right">87.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">54,574,380</td>
<td align="right">1.9%</td>
<td align="right">89.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">50,811,180</td>
<td align="right">1.8%</td>
<td align="right">91.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">42,798,780</td>
<td align="right">1.5%</td>
<td align="right">92.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">20,654,340</td>
<td align="right">0.7%</td>
<td align="right">93.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">15,845,760</td>
<td align="right">0.5%</td>
<td align="right">94.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">14,367,360</td>
<td align="right">0.5%</td>
<td align="right">94.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">14,081,820</td>
<td align="right">0.5%</td>
<td align="right">95.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">13,868,160</td>
<td align="right">0.5%</td>
<td align="right">95.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">13,186,560</td>
<td align="right">0.5%</td>
<td align="right">96.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">12,487,740</td>
<td align="right">0.4%</td>
<td align="right">96.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">11,115,000</td>
<td align="right">0.4%</td>
<td align="right">96.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">10,871,220</td>
<td align="right">0.4%</td>
<td align="right">97.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">8,452,080</td>
<td align="right">0.3%</td>
<td align="right">97.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">6,952,320</td>
<td align="right">0.2%</td>
<td align="right">97.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">6,764,160</td>
<td align="right">0.2%</td>
<td align="right">98.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">6,624,000</td>
<td align="right">0.2%</td>
<td align="right">98.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">4,713,600</td>
<td align="right">0.2%</td>
<td align="right">98.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">4,335,660</td>
<td align="right">0.2%</td>
<td align="right">98.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">4,316,160</td>
<td align="right">0.1%</td>
<td align="right">98.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">4,189,500</td>
<td align="right">0.1%</td>
<td align="right">98.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">3,563,640</td>
<td align="right">0.1%</td>
<td align="right">99.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">3,317,820</td>
<td align="right">0.1%</td>
<td align="right">99.1%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">2,872,440</td>
<td align="right">0.1%</td>
<td align="right">99.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">2,872,380</td>
<td align="right">0.1%</td>
<td align="right">99.3%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">2,872,380</td>
<td align="right">0.1%</td>
<td align="right">99.4%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">2,872,380</td>
<td align="right">0.1%</td>
<td align="right">99.5%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">2,872,320</td>
<td align="right">0.1%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,747,860</td>
<td align="right">0.1%</td>
<td align="right">99.6%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">1,526,460</td>
<td align="right">0.1%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,416,960</td>
<td align="right">0.0%</td>
<td align="right">99.7%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">1,046,460</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">896,640</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">837,240</td>
<td align="right">0.0%</td>
<td align="right">99.8%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">472,320</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">472,320</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">414,780</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">410,940</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">410,940</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">376,380</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">312,960</td>
<td align="right">0.0%</td>
<td align="right">99.9%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">309,180</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">249,720</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">249,720</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">218,880</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">197,820</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">73,020</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">72,960</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">55,680</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">50,220</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">46,080</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">36,480</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">23,040</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">15,360</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">11,940</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">2,520</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">2,280</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">2,220</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">1,980</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,980</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">1,920</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">1,920</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">1,920</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">420</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">380</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">200</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">120</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">100</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right">100.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
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
<td align="left">LOAD_FAST_BORROW LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">125,942,540</td>
<td align="right">4.4%</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_FAST_BORROW</td>
<td align="right">118,886,400</td>
<td align="right">4.1%</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">118,039,680</td>
<td align="right">4.1%</td>
<td align="right">12.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_FAST_BORROW</td>
<td align="right">102,701,100</td>
<td align="right">3.6%</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST STORE_FAST</td>
<td align="right">77,827,200</td>
<td align="right">2.7%</td>
<td align="right">18.8%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT FOR_ITER_LIST</td>
<td align="right">77,612,460</td>
<td align="right">2.7%</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT COMPARE_OP_INT</td>
<td align="right">77,164,800</td>
<td align="right">2.7%</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN LOAD_FAST_BORROW</td>
<td align="right">73,186,620</td>
<td align="right">2.5%</td>
<td align="right">26.7%</td>
</tr>
<tr>
<td align="left">CALL_LEN LOAD_SMALL_INT</td>
<td align="right">70,152,960</td>
<td align="right">2.4%</td>
<td align="right">29.2%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS RESUME_CHECK</td>
<td align="right">69,246,900</td>
<td align="right">2.4%</td>
<td align="right">31.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF LOAD_FAST_BORROW</td>
<td align="right">67,361,280</td>
<td align="right">2.3%</td>
<td align="right">33.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW CONTAINS_OP</td>
<td align="right">67,361,280</td>
<td align="right">2.3%</td>
<td align="right">36.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">65,404,840</td>
<td align="right">2.3%</td>
<td align="right">38.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE TO_BOOL_BOOL</td>
<td align="right">65,120,640</td>
<td align="right">2.3%</td>
<td align="right">40.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES LOAD_FAST_BORROW</td>
<td align="right">62,386,620</td>
<td align="right">2.2%</td>
<td align="right">42.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW CALL_PY_EXACT_ARGS</td>
<td align="right">62,211,840</td>
<td align="right">2.2%</td>
<td align="right">45.1%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP POP_JUMP_IF_FALSE</td>
<td align="right">59,884,800</td>
<td align="right">2.1%</td>
<td align="right">47.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_FALSE</td>
<td align="right">59,752,320</td>
<td align="right">2.1%</td>
<td align="right">49.2%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_GLOBAL_BUILTIN</td>
<td align="right">59,074,560</td>
<td align="right">2.0%</td>
<td align="right">51.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT CALL_LEN</td>
<td align="right">58,970,880</td>
<td align="right">2.0%</td>
<td align="right">53.3%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT RETURN_VALUE</td>
<td align="right">58,970,880</td>
<td align="right">2.0%</td>
<td align="right">55.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_SMALL_INT</td>
<td align="right">57,331,200</td>
<td align="right">2.0%</td>
<td align="right">57.4%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT FOR_ITER_RANGE</td>
<td align="right">55,046,400</td>
<td align="right">1.9%</td>
<td align="right">59.3%</td>
</tr>
<tr>
<td align="left">POP_TOP JUMP_BACKWARD_NO_JIT</td>
<td align="right">54,774,120</td>
<td align="right">1.9%</td>
<td align="right">61.2%</td>
</tr>
<tr>
<td align="left">CACHE RESUME_CHECK</td>
<td align="right">54,574,440</td>
<td align="right">1.9%</td>
<td align="right">63.1%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE INTERPRETER_EXIT</td>
<td align="right">54,574,380</td>
<td align="right">1.9%</td>
<td align="right">65.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK POP_TOP</td>
<td align="right">54,574,380</td>
<td align="right">1.9%</td>
<td align="right">66.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_DEREF</td>
<td align="right">54,574,080</td>
<td align="right">1.9%</td>
<td align="right">68.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE STORE_FAST</td>
<td align="right">50,584,320</td>
<td align="right">1.8%</td>
<td align="right">70.5%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT YIELD_VALUE</td>
<td align="right">42,289,920</td>
<td align="right">1.5%</td>
<td align="right">72.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT STORE_FAST</td>
<td align="right">34,277,760</td>
<td align="right">1.2%</td>
<td align="right">73.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE JUMP_BACKWARD_NO_JIT</td>
<td align="right">29,790,720</td>
<td align="right">1.0%</td>
<td align="right">74.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE JUMP_BACKWARD_NO_JIT</td>
<td align="right">25,488,000</td>
<td align="right">0.9%</td>
<td align="right">75.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT POP_JUMP_IF_TRUE</td>
<td align="right">24,124,800</td>
<td align="right">0.8%</td>
<td align="right">75.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT POP_JUMP_IF_FALSE</td>
<td align="right">23,896,320</td>
<td align="right">0.8%</td>
<td align="right">76.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_FAST_BORROW</td>
<td align="right">19,365,240</td>
<td align="right">0.7%</td>
<td align="right">77.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_FAST_BORROW</td>
<td align="right">18,032,820</td>
<td align="right">0.6%</td>
<td align="right">78.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT RETURN_VALUE</td>
<td align="right">16,965,120</td>
<td align="right">0.6%</td>
<td align="right">78.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT STORE_FAST</td>
<td align="right">15,465,600</td>
<td align="right">0.5%</td>
<td align="right">79.2%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">15,456,000</td>
<td align="right">0.5%</td>
<td align="right">79.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW LOAD_SMALL_INT</td>
<td align="right">15,227,580</td>
<td align="right">0.5%</td>
<td align="right">80.2%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT BINARY_OP_ADD_INT</td>
<td align="right">15,091,200</td>
<td align="right">0.5%</td>
<td align="right">80.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW COMPARE_OP_INT</td>
<td align="right">14,899,200</td>
<td align="right">0.5%</td>
<td align="right">81.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM RESUME_CHECK</td>
<td align="right">13,868,160</td>
<td align="right">0.5%</td>
<td align="right">81.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT LOAD_SMALL_INT</td>
<td align="right">13,511,040</td>
<td align="right">0.5%</td>
<td align="right">82.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">13,382,400</td>
<td align="right">0.5%</td>
<td align="right">82.7%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP POP_JUMP_IF_TRUE</td>
<td align="right">12,862,080</td>
<td align="right">0.4%</td>
<td align="right">83.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_DEREF</td>
<td align="right">12,787,200</td>
<td align="right">0.4%</td>
<td align="right">83.6%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD YIELD_VALUE</td>
<td align="right">12,284,160</td>
<td align="right">0.4%</td>
<td align="right">84.0%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT JUMP_FORWARD</td>
<td align="right">12,284,160</td>
<td align="right">0.4%</td>
<td align="right">84.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">11,700,480</td>
<td align="right">0.4%</td>
<td align="right">84.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_GLOBAL_BUILTIN</td>
<td align="right">11,683,240</td>
<td align="right">0.4%</td>
<td align="right">85.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE COMPARE_OP_INT</td>
<td align="right">11,120,640</td>
<td align="right">0.4%</td>
<td align="right">85.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">11,030,400</td>
<td align="right">0.4%</td>
<td align="right">86.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE LOAD_SMALL_INT</td>
<td align="right">10,807,680</td>
<td align="right">0.4%</td>
<td align="right">86.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST JUMP_BACKWARD_NO_JIT</td>
<td align="right">10,604,160</td>
<td align="right">0.4%</td>
<td align="right">86.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST RETURN_VALUE</td>
<td align="right">9,106,800</td>
<td align="right">0.3%</td>
<td align="right">87.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW CALL_LEN</td>
<td align="right">8,645,760</td>
<td align="right">0.3%</td>
<td align="right">87.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">8,538,300</td>
<td align="right">0.3%</td>
<td align="right">87.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT LOAD_GLOBAL_MODULE</td>
<td align="right">8,463,360</td>
<td align="right">0.3%</td>
<td align="right">87.9%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">7,848,960</td>
<td align="right">0.3%</td>
<td align="right">88.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST POP_ITER</td>
<td align="right">7,077,180</td>
<td align="right">0.2%</td>
<td align="right">88.5%</td>
</tr>
<tr>
<td align="left">GET_ITER FOR_ITER_LIST</td>
<td align="right">6,720,060</td>
<td align="right">0.2%</td>
<td align="right">88.7%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT BINARY_OP_SUBTRACT_INT</td>
<td align="right">6,612,480</td>
<td align="right">0.2%</td>
<td align="right">88.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST GET_ITER</td>
<td align="right">6,597,240</td>
<td align="right">0.2%</td>
<td align="right">89.2%</td>
</tr>
<tr>
<td align="left">COPY COPY</td>
<td align="right">6,593,280</td>
<td align="right">0.2%</td>
<td align="right">89.4%</td>
</tr>
<tr>
<td align="left">COPY BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">6,593,280</td>
<td align="right">0.2%</td>
<td align="right">89.6%</td>
</tr>
<tr>
<td align="left">SWAP SWAP</td>
<td align="right">6,593,280</td>
<td align="right">0.2%</td>
<td align="right">89.8%</td>
</tr>
<tr>
<td align="left">SWAP STORE_SUBSCR_LIST_INT</td>
<td align="right">6,593,280</td>
<td align="right">0.2%</td>
<td align="right">90.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT SWAP</td>
<td align="right">6,556,800</td>
<td align="right">0.2%</td>
<td align="right">90.3%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT STORE_FAST</td>
<td align="right">6,336,000</td>
<td align="right">0.2%</td>
<td align="right">90.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE LOAD_DEREF</td>
<td align="right">6,190,080</td>
<td align="right">0.2%</td>
<td align="right">90.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">5,948,200</td>
<td align="right">0.2%</td>
<td align="right">90.9%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">5,907,840</td>
<td align="right">0.2%</td>
<td align="right">91.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE LOAD_CONST</td>
<td align="right">5,788,800</td>
<td align="right">0.2%</td>
<td align="right">91.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL POP_JUMP_IF_TRUE</td>
<td align="right">5,775,420</td>
<td align="right">0.2%</td>
<td align="right">91.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW CALL_PY_EXACT_ARGS</td>
<td align="right">5,571,880</td>
<td align="right">0.2%</td>
<td align="right">91.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">5,571,840</td>
<td align="right">0.2%</td>
<td align="right">91.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT CONTAINS_OP</td>
<td align="right">5,216,640</td>
<td align="right">0.2%</td>
<td align="right">92.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW LOAD_SMALL_INT</td>
<td align="right">5,068,800</td>
<td align="right">0.2%</td>
<td align="right">92.3%</td>
</tr>
<tr>
<td align="left">LOAD_CONST BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">4,713,600</td>
<td align="right">0.2%</td>
<td align="right">92.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT JUMP_BACKWARD_NO_JIT</td>
<td align="right">4,654,080</td>
<td align="right">0.2%</td>
<td align="right">92.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT COPY</td>
<td align="right">4,646,400</td>
<td align="right">0.2%</td>
<td align="right">92.8%</td>
</tr>
<tr>
<td align="left">LIST_APPEND JUMP_BACKWARD_NO_JIT</td>
<td align="right">4,316,160</td>
<td align="right">0.1%</td>
<td align="right">92.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,085,760</td>
<td align="right">0.1%</td>
<td align="right">93.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT LOAD_CONST</td>
<td align="right">4,085,760</td>
<td align="right">0.1%</td>
<td align="right">93.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE LIST_APPEND</td>
<td align="right">4,085,760</td>
<td align="right">0.1%</td>
<td align="right">93.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE STORE_FAST_LOAD_FAST</td>
<td align="right">4,085,760</td>
<td align="right">0.1%</td>
<td align="right">93.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE STORE_FAST</td>
<td align="right">4,078,080</td>
<td align="right">0.1%</td>
<td align="right">93.6%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE POP_ITER</td>
<td align="right">3,793,980</td>
<td align="right">0.1%</td>
<td align="right">93.8%</td>
</tr>
<tr>
<td align="left">GET_ITER FOR_ITER_RANGE</td>
<td align="right">3,767,100</td>
<td align="right">0.1%</td>
<td align="right">93.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS GET_ITER</td>
<td align="right">3,751,680</td>
<td align="right">0.1%</td>
<td align="right">94.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_SMALL_INT</td>
<td align="right">3,623,040</td>
<td align="right">0.1%</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST LOAD_FAST</td>
<td align="right">3,515,640</td>
<td align="right">0.1%</td>
<td align="right">94.3%</td>
</tr>
<tr>
<td align="left">STORE_DEREF LOAD_FAST_BORROW</td>
<td align="right">3,317,820</td>
<td align="right">0.1%</td>
<td align="right">94.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE STORE_DEREF</td>
<td align="right">3,317,760</td>
<td align="right">0.1%</td>
<td align="right">94.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST STORE_FAST</td>
<td align="right">3,273,780</td>
<td align="right">0.1%</td>
<td align="right">94.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW COMPARE_OP_INT</td>
<td align="right">3,168,000</td>
<td align="right">0.1%</td>
<td align="right">94.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT EXTENDED_ARG</td>
<td align="right">3,162,240</td>
<td align="right">0.1%</td>
<td align="right">94.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">3,133,440</td>
<td align="right">0.1%</td>
<td align="right">94.9%</td>
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
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">36,480</td>
<td align="right">79.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">9,600</td>
<td align="right">20.8%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">46,080</td>
<td align="right">100.0%</td>
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
<td align="right">6,597,240</td>
<td align="right">59.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">3,751,680</td>
<td align="right">33.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">416,640</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">312,960</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">36,480</td>
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
<td align="left">FOR_ITER_LIST</td>
<td align="right">6,720,060</td>
<td align="right">60.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">3,767,100</td>
<td align="right">33.9%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">627,840</td>
<td align="right">5.6%</td>
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
<td align="right">54,574,440</td>
<td align="right">95.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">2,872,380</td>
<td align="right">5.0%</td>
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
<td align="left">PUSH_NULL</td>
<td align="right">120</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">60</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">472,320</td>
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
<td align="right">472,320</td>
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
<td align="left">YIELD_VALUE</td>
<td align="right">54,574,380</td>
<td align="right">95.0%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">2,872,380</td>
<td align="right">5.0%</td>
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
<td align="right">2,872,440</td>
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
<td align="right">2,872,380</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">60</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">60</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### POP_ITER

<details>
<summary> Successors and predecessors for POP_ITER </summary>

<table>
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
<td align="right">7,077,180</td>
<td align="right">65.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">3,793,980</td>
<td align="right">34.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">60</td>
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
<td align="right">2,887,740</td>
<td align="right">26.6%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">2,578,560</td>
<td align="right">23.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,795,260</td>
<td align="right">16.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,691,520</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">1,426,560</td>
<td align="right">13.1%</td>
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
<td align="right">54,574,380</td>
<td align="right">91.7%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">2,872,380</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">837,180</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">693,300</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">243,840</td>
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
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">54,774,120</td>
<td align="right">92.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">2,872,380</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">1,154,100</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">243,840</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">243,840</td>
<td align="right">0.4%</td>
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
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">2,220</td>
<td align="right">88.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">180</td>
<td align="right">7.1%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">60</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">60</td>
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
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">2,120</td>
<td align="right">84.1%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">120</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">120</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">100</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">60</td>
<td align="right">2.4%</td>
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
<td align="right">2,872,320</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">60</td>
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
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">2,872,320</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="left">COMPARE_OP_INT</td>
<td align="right">58,970,880</td>
<td align="right">67.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">16,965,120</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">9,106,800</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,169,340</td>
<td align="right">1.3%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">472,320</td>
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
<td align="left">TO_BOOL_BOOL</td>
<td align="right">65,120,640</td>
<td align="right">74.3%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">10,807,680</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">3,133,440</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">2,872,380</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">2,797,440</td>
<td align="right">3.2%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">60</td>
<td align="right">60.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">20</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">20</td>
<td align="right">20.0%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">60</td>
<td align="right">60.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">20</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">20</td>
<td align="right">20.0%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">40,360</td>
<td align="right">80.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">5,760</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">3,840</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">240</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">46,080</td>
<td align="right">91.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,920</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,920</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">240</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">725,820</td>
<td align="right">47.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">410,880</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">312,960</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">36,480</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">36,480</td>
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
<td align="left">STORE_FAST</td>
<td align="right">821,760</td>
<td align="right">53.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">314,880</td>
<td align="right">20.6%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">312,960</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">36,480</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">36,480</td>
<td align="right">2.4%</td>
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
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,920</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,920</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">2,872,380</td>
<td align="right">80.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">635,580</td>
<td align="right">17.8%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">55,680</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">2,872,380</td>
<td align="right">80.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">218,880</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">182,400</td>
<td align="right">5.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">161,280</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">72,960</td>
<td align="right">2.0%</td>
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
<td align="left">PUSH_NULL</td>
<td align="right">100</td>
<td align="right">26.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">80</td>
<td align="right">21.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">40</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">40</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">20</td>
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
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">120</td>
<td align="right">31.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">100</td>
<td align="right">26.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">40</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">40</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">20</td>
<td align="right">5.3%</td>
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
<td align="right">60</td>
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
<td align="left">PUSH_NULL</td>
<td align="right">60</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
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
<td align="left">COMPARE_OP_STR</td>
<td align="right">20</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">67,361,280</td>
<td align="right">92.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">5,216,640</td>
<td align="right">7.2%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">168,960</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">17,780</td>
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
<td align="right">59,884,800</td>
<td align="right">82.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">12,862,080</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">17,780</td>
<td align="right">0.0%</td>
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
<td align="left">COPY</td>
<td align="right">6,593,280</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">4,646,400</td>
<td align="right">35.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">1,946,880</td>
<td align="right">14.8%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">COPY</td>
<td align="right">6,593,280</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">6,593,280</td>
<td align="right">50.0%</td>
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
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,872,380</td>
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
<td align="left">RETURN_GENERATOR</td>
<td align="right">2,872,320</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">3,162,240</td>
<td align="right">46.7%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,572,480</td>
<td align="right">23.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">1,105,920</td>
<td align="right">16.3%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">627,840</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">180,480</td>
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
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">2,974,080</td>
<td align="right">44.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">2,968,320</td>
<td align="right">43.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">821,760</td>
<td align="right">12.1%</td>
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
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">60</td>
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
<td align="left">POP_ITER</td>
<td align="right">60</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">60</td>
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
<td align="left">STORE_FAST</td>
<td align="right">60</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_SMALL_INT</td>
<td align="right">12,284,160</td>
<td align="right">98.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">170,940</td>
<td align="right">1.4%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">23,040</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">7,680</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,920</td>
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
<td align="left">YIELD_VALUE</td>
<td align="right">12,284,160</td>
<td align="right">98.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">121,020</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">36,480</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">30,720</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">13,440</td>
<td align="right">0.1%</td>
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
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">4,085,760</td>
<td align="right">94.7%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">182,400</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">36,480</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">11,520</td>
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
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">4,316,160</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_DEREF</td>
<td align="right">60</td>
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
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">60</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">160</td>
<td align="right">38.1%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">120</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">40</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">20</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">20</td>
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
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">120</td>
<td align="right">28.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">100</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">60</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">60</td>
<td align="right">14.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">40</td>
<td align="right">9.5%</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,788,800</td>
<td align="right">28.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">4,085,760</td>
<td align="right">19.8%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">2,887,740</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">2,872,380</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">1,154,100</td>
<td align="right">5.6%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">9,106,800</td>
<td align="right">44.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">4,713,600</td>
<td align="right">22.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">3,273,780</td>
<td align="right">15.9%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">2,872,440</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">311,040</td>
<td align="right">1.5%</td>
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
<td align="left">STORE_FAST</td>
<td align="right">54,574,080</td>
<td align="right">72.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">12,787,200</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">6,190,080</td>
<td align="right">8.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,691,520</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">445,440</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">67,361,280</td>
<td align="right">89.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">7,848,960</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">478,080</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="right">3,515,640</td>
<td align="right">41.6%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">2,872,380</td>
<td align="right">34.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">1,766,400</td>
<td align="right">20.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">216,960</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">80,640</td>
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
<td align="left">GET_ITER</td>
<td align="right">6,597,240</td>
<td align="right">78.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">1,424,680</td>
<td align="right">16.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">216,960</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">213,120</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">216,960</td>
<td align="right">69.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">94,080</td>
<td align="right">30.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">1,920</td>
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
<td align="left">SWAP</td>
<td align="right">312,960</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST_BORROW

<details>
<summary> Successors and predecessors for LOAD_FAST_BORROW </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">118,886,400</td>
<td align="right">24.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">102,701,100</td>
<td align="right">21.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">73,186,620</td>
<td align="right">15.2%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">67,361,280</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">62,386,620</td>
<td align="right">13.0%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">125,942,540</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">118,039,680</td>
<td align="right">24.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">67,361,280</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">65,404,840</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">62,211,840</td>
<td align="right">12.9%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_FAST_BORROW_LOAD_FAST_BORROW

<details>
<summary> Successors and predecessors for LOAD_FAST_BORROW_LOAD_FAST_BORROW </summary>

<table>
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
<td align="right">11,700,480</td>
<td align="right">23.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">11,030,400</td>
<td align="right">21.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">8,538,300</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">5,907,840</td>
<td align="right">11.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">5,571,840</td>
<td align="right">11.0%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">14,899,200</td>
<td align="right">29.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">13,382,400</td>
<td align="right">26.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">5,948,200</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">5,571,880</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">5,068,800</td>
<td align="right">10.0%</td>
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
<td align="left">MAKE_FUNCTION</td>
<td align="right">60</td>
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
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">40</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">20</td>
<td align="right">33.3%</td>
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
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">410,880</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">60</td>
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
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">410,880</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="left">STORE_FAST</td>
<td align="right">100</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">60</td>
<td align="right">30.0%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">20</td>
<td align="right">10.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">20</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">180</td>
<td align="right">90.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">20</td>
<td align="right">10.0%</td>
</tr>
</tbody>
</table>


</details>

### LOAD_SMALL_INT

<details>
<summary> Successors and predecessors for LOAD_SMALL_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">70,152,960</td>
<td align="right">39.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">57,331,200</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">15,227,580</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">13,511,040</td>
<td align="right">7.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">10,807,680</td>
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
<td align="left">COMPARE_OP_INT</td>
<td align="right">77,164,800</td>
<td align="right">43.5%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">42,289,920</td>
<td align="right">23.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">15,456,000</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">15,091,200</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">12,284,160</td>
<td align="right">6.9%</td>
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
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">410,880</td>
<td align="right">99.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">3,900</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">414,780</td>
<td align="right">100.0%</td>
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
<td align="left">CONTAINS_OP</td>
<td align="right">59,884,800</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">59,752,320</td>
<td align="right">41.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">23,896,320</td>
<td align="right">16.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">36,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">60</td>
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
<td align="left">LOAD_SMALL_INT</td>
<td align="right">57,331,200</td>
<td align="right">39.9%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">29,790,720</td>
<td align="right">20.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">19,365,240</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">12,787,200</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">11,700,480</td>
<td align="right">8.1%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,046,460</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">821,760</td>
<td align="right">78.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">216,960</td>
<td align="right">20.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">7,680</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="left">COMPARE_OP_INT</td>
<td align="right">24,124,800</td>
<td align="right">56.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">12,862,080</td>
<td align="right">30.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">5,775,420</td>
<td align="right">13.5%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">36,480</td>
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
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">25,488,000</td>
<td align="right">59.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">11,030,400</td>
<td align="right">25.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">3,123,840</td>
<td align="right">7.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">1,681,920</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">691,200</td>
<td align="right">1.6%</td>
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
<td align="right">2,872,380</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">2,872,320</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="left">FOR_ITER_RANGE</td>
<td align="right">3,317,760</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">60</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">3,317,820</td>
<td align="right">100.0%</td>
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
<td align="right">77,827,200</td>
<td align="right">39.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">50,584,320</td>
<td align="right">25.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">34,277,760</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">15,465,600</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">6,336,000</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">102,701,100</td>
<td align="right">51.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">54,574,080</td>
<td align="right">27.5%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">11,683,240</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">10,604,160</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">8,538,300</td>
<td align="right">4.3%</td>
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
<td align="left">FOR_ITER_RANGE</td>
<td align="right">4,085,760</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">249,900</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,085,760</td>
<td align="right">94.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">238,080</td>
<td align="right">5.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">11,820</td>
<td align="right">0.3%</td>
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
<td align="right">249,720</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">213,180</td>
<td align="right">85.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">36,520</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">20</td>
<td align="right">0.0%</td>
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
<td align="left">SWAP</td>
<td align="right">6,593,280</td>
<td align="right">45.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">6,556,800</td>
<td align="right">45.6%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">312,960</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">312,960</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">311,040</td>
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
<td align="left">SWAP</td>
<td align="right">6,593,280</td>
<td align="right">45.9%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">6,593,280</td>
<td align="right">45.9%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">312,960</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">312,960</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">311,040</td>
<td align="right">2.2%</td>
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
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">20</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">20</td>
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
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">40</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_SMALL_INT</td>
<td align="right">42,289,920</td>
<td align="right">77.5%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">12,284,160</td>
<td align="right">22.5%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
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
<td align="left">INTERPRETER_EXIT</td>
<td align="right">54,574,380</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_SMALL_INT</td>
<td align="right">15,091,200</td>
<td align="right">95.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">437,760</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">261,120</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">44,160</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">7,680</td>
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
<td align="right">15,465,600</td>
<td align="right">97.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">261,120</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">36,480</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">36,480</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">26,880</td>
<td align="right">0.2%</td>
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
<td align="left">LOAD_SMALL_INT</td>
<td align="right">11,520</td>
<td align="right">75.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,920</td>
<td align="right">12.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,920</td>
<td align="right">12.5%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">13,440</td>
<td align="right">87.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,920</td>
<td align="right">12.5%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_SUBSCR_DICT

<details>
<summary> Successors and predecessors for BINARY_OP_SUBSCR_DICT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">161,280</td>
<td align="right">81.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">36,520</td>
<td align="right">18.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">161,280</td>
<td align="right">81.5%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">36,480</td>
<td align="right">18.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_SUBSCR_GETITEM

<details>
<summary> Successors and predecessors for BINARY_OP_SUBSCR_GETITEM </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">13,382,400</td>
<td align="right">96.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">410,880</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">74,880</td>
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
<td align="right">13,868,160</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_SUBSCR_LIST_INT

<details>
<summary> Successors and predecessors for BINARY_OP_SUBSCR_LIST_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">118,039,680</td>
<td align="right">78.8%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">15,456,000</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">7,848,960</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">6,593,280</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">1,950,720</td>
<td align="right">1.3%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">58,970,880</td>
<td align="right">39.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">34,277,760</td>
<td align="right">22.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">16,965,120</td>
<td align="right">11.3%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">13,511,040</td>
<td align="right">9.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">8,463,360</td>
<td align="right">5.6%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_SUBSCR_LIST_SLICE

<details>
<summary> Successors and predecessors for BINARY_OP_SUBSCR_LIST_SLICE </summary>

<table>
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
<td align="right">4,713,600</td>
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
<td align="left">LIST_APPEND</td>
<td align="right">4,085,760</td>
<td align="right">86.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">627,840</td>
<td align="right">13.3%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_SUBSCR_STR_INT

<details>
<summary> Successors and predecessors for BINARY_OP_SUBSCR_STR_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">72,960</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">72,960</td>
<td align="right">100.0%</td>
</tr>
</tbody>
</table>


</details>

### BINARY_OP_SUBSCR_TUPLE_INT

<details>
<summary> Successors and predecessors for BINARY_OP_SUBSCR_TUPLE_INT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">410,920</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
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
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">410,880</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
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
<td align="left">STORE_FAST</td>
<td align="right">60</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_SMALL_INT</td>
<td align="right">6,612,480</td>
<td align="right">99.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">11,520</td>
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
<td align="right">6,556,800</td>
<td align="right">99.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">26,880</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">11,520</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">11,520</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">5,760</td>
<td align="right">0.1%</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">215,040</td>
<td align="right">45.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">215,040</td>
<td align="right">45.5%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">36,480</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">3,840</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">1,920</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">472,320</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">2,664,960</td>
<td align="right">63.6%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">1,269,120</td>
<td align="right">30.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">94,080</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">94,080</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">36,520</td>
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
<td align="left">GET_ITER</td>
<td align="right">3,751,680</td>
<td align="right">89.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">216,960</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">119,100</td>
<td align="right">2.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">94,080</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">7,680</td>
<td align="right">0.2%</td>
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
<td align="left">RETURN_GENERATOR</td>
<td align="right">2,872,320</td>
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
<td align="left">STORE_FAST</td>
<td align="right">2,872,320</td>
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
<td align="right">55,680</td>
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
<td align="right">55,680</td>
<td align="right">100.0%</td>
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
<td align="right">1,920</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">1,920</td>
<td align="right">100.0%</td>
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
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">58,970,880</td>
<td align="right">83.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">8,645,760</td>
<td align="right">12.3%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">2,797,440</td>
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
<td align="left">LOAD_SMALL_INT</td>
<td align="right">70,152,960</td>
<td align="right">99.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">261,120</td>
<td align="right">0.4%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">679,680</td>
<td align="right">75.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">161,280</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">55,680</td>
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
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">840,960</td>
<td align="right">93.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">55,680</td>
<td align="right">6.2%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">11,520</td>
<td align="right">96.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">380</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">40</td>
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
<td align="left">LIST_APPEND</td>
<td align="right">11,520</td>
<td align="right">96.5%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">300</td>
<td align="right">2.5%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">120</td>
<td align="right">1.0%</td>
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
<td align="right">1,960</td>
<td align="right">99.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
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
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">1,920</td>
<td align="right">97.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">40</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">20</td>
<td align="right">1.0%</td>
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
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">1,920</td>
<td align="right">97.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">40</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
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
<td align="left">STORE_FAST</td>
<td align="right">1,920</td>
<td align="right">97.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">40</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">20</td>
<td align="right">1.0%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">837,120</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
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
<td align="left">POP_TOP</td>
<td align="right">837,180</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="left">PUSH_NULL</td>
<td align="right">2,120</td>
<td align="right">93.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">120</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">40</td>
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
<td align="right">2,040</td>
<td align="right">89.5%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">60</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">60</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">60</td>
<td align="right">2.6%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">60</td>
<td align="right">2.6%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">62,211,840</td>
<td align="right">85.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">5,571,880</td>
<td align="right">7.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">2,872,360</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">526,080</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">478,080</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">69,246,900</td>
<td align="right">95.5%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">2,872,380</td>
<td align="right">4.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">410,880</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">305,280</td>
<td align="right">98.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">3,840</td>
<td align="right">1.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
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
<td align="right">305,280</td>
<td align="right">98.7%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">3,900</td>
<td align="right">1.3%</td>
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
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">23,040</td>
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
<td align="left">JUMP_FORWARD</td>
<td align="right">23,040</td>
<td align="right">100.0%</td>
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
<td align="left">LOAD_SMALL_INT</td>
<td align="right">77,164,800</td>
<td align="right">72.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">14,899,200</td>
<td align="right">13.9%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">11,120,640</td>
<td align="right">10.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">3,168,000</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">376,320</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">58,970,880</td>
<td align="right">55.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">24,124,800</td>
<td align="right">22.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">23,896,320</td>
<td align="right">22.3%</td>
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
<td align="left">LOAD_CONST</td>
<td align="right">72,960</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">40</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">36,540</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">36,480</td>
<td align="right">50.0%</td>
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
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">218,880</td>
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
<td align="right">218,880</td>
<td align="right">100.0%</td>
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
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">77,612,460</td>
<td align="right">91.1%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">6,720,060</td>
<td align="right">7.9%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">821,760</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">1,920</td>
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
<td align="right">77,827,200</td>
<td align="right">91.4%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">7,077,180</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">249,900</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">1,920</td>
<td align="right">0.0%</td>
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
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">55,046,400</td>
<td align="right">89.1%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">3,767,100</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">2,968,320</td>
<td align="right">4.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">1,920</td>
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
<td align="right">50,584,320</td>
<td align="right">81.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">4,085,760</td>
<td align="right">6.6%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">3,793,980</td>
<td align="right">6.1%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">3,317,760</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">1,920</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

### JUMP_BACKWARD_NO_JIT

<details>
<summary> Successors and predecessors for JUMP_BACKWARD_NO_JIT </summary>

<table>
<thead>
<tr>
<th align="left">Predecessors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">POP_TOP</td>
<td align="right">54,774,120</td>
<td align="right">40.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">29,790,720</td>
<td align="right">21.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">25,488,000</td>
<td align="right">18.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">10,604,160</td>
<td align="right">7.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">4,654,080</td>
<td align="right">3.4%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">77,612,460</td>
<td align="right">57.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">55,046,400</td>
<td align="right">40.5%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">3,162,240</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">199,680</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">376,360</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
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
<td align="left">COMPARE_OP_INT</td>
<td align="right">376,320</td>
<td align="right">100.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">60</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">125,942,540</td>
<td align="right">90.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">5,948,200</td>
<td align="right">4.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">4,085,760</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">3,133,440</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">161,280</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">118,886,400</td>
<td align="right">85.4%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">6,190,080</td>
<td align="right">4.4%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">4,078,080</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,872,360</td>
<td align="right">2.1%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">2,664,960</td>
<td align="right">1.9%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,920</td>
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
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">1,920</td>
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
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">837,120</td>
<td align="right">47.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">737,360</td>
<td align="right">42.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">161,360</td>
<td align="right">9.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">11,820</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,733,760</td>
<td align="right">99.2%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">11,580</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">1,960</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">380</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">80</td>
<td align="right">0.0%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">65,404,840</td>
<td align="right">94.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">2,100,480</td>
<td align="right">3.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">1,424,680</td>
<td align="right">2.1%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">62,386,620</td>
<td align="right">90.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">5,571,840</td>
<td align="right">8.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">526,080</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">445,440</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">60</td>
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
<td align="right">2,120</td>
<td align="right">95.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">100</td>
<td align="right">4.5%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">2,220</td>
<td align="right">100.0%</td>
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
<td align="left">RESUME_CHECK</td>
<td align="right">59,074,560</td>
<td align="right">76.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">11,683,240</td>
<td align="right">15.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">3,014,400</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">1,691,520</td>
<td align="right">2.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,681,920</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">73,186,620</td>
<td align="right">94.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">2,943,360</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">1,274,880</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">94,080</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">55,680</td>
<td align="right">0.1%</td>
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
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">8,463,360</td>
<td align="right">60.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">3,091,200</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">735,520</td>
<td align="right">5.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">451,200</td>
<td align="right">3.2%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">434,040</td>
<td align="right">3.1%</td>
</tr>
</tbody>
</table>

<table>
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
<td align="right">11,120,640</td>
<td align="right">79.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">1,163,580</td>
<td align="right">8.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">516,540</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">376,360</td>
<td align="right">2.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">240,000</td>
<td align="right">1.7%</td>
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
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">69,246,900</td>
<td align="right">48.8%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">54,574,440</td>
<td align="right">38.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">13,868,160</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">2,872,380</td>
<td align="right">2.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">472,320</td>
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
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">59,074,560</td>
<td align="right">41.7%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">54,574,380</td>
<td align="right">38.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">18,032,820</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">5,907,840</td>
<td align="right">4.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">2,872,380</td>
<td align="right">2.0%</td>
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
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">762,240</td>
<td align="right">53.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">654,720</td>
<td align="right">46.2%</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th align="left">Successors</th>
<th align="right">Count</th>
<th align="right">Percentage</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">650,880</td>
<td align="right">45.9%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">470,400</td>
<td align="right">33.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">289,920</td>
<td align="right">20.5%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">3,840</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">1,920</td>
<td align="right">0.1%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">36,480</td>
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
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">36,480</td>
<td align="right">100.0%</td>
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
<td align="left">SWAP</td>
<td align="right">6,593,280</td>
<td align="right">94.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">314,880</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">36,480</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">7,680</td>
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
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">4,654,080</td>
<td align="right">66.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">1,910,400</td>
<td align="right">27.5%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">314,880</td>
<td align="right">4.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">72,960</td>
<td align="right">1.0%</td>
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
<td align="left">RETURN_VALUE</td>
<td align="right">65,120,640</td>
<td align="right">99.4%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">407,080</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
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
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">59,752,320</td>
<td align="right">91.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">5,775,420</td>
<td align="right">8.8%</td>
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
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">213,120</td>
<td align="right">85.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">36,480</td>
<td align="right">14.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">40</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
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
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">249,720</td>
<td align="right">100.0%</td>
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
<td align="right">49,920</td>
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
<td align="right">341,525,940</td>
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
<td align="right">60</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">240</td>
<td align="right">80.0%</td>
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
<td align="left">multiply different types</td>
<td align="right">160</td>
<td align="right">66.7%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">80</td>
<td align="right">33.3%</td>
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
<td align="right">46,080</td>
<td align="right">100.0%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">152,251,260</td>
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
<td align="right">380</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">107,065,020</td>
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
<td align="right">20</td>
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
<td align="right">72,746,880</td>
<td align="right">99.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">218,880</td>
<td align="right">0.3%</td>
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
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">17,780</td>
<td align="right">100.0%</td>
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
<td align="right">17,780</td>
<td align="right">100.0%</td>
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
<td align="right">60</td>
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
<td align="right">146,736,420</td>
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
<td align="right">203,520</td>
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
<td align="right">3,840</td>
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

### GET_ITER

<details>
<summary> specialization stats for GET_ITER family </summary>

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
<td align="right">7,138,620</td>
<td align="right">7,138,620 / 0 !!</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">3,976,380</td>
<td align="right">3,976,380 / 0 !!</td>
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
<td align="right">60</td>
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
<td align="right">210,329,700</td>
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
<td align="right">340</td>
<td align="right">94.4%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">20</td>
<td align="right">5.6%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">91,636,440</td>
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
<td align="right">200</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,416,960</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">6,988,800</td>
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
<td align="right">60</td>
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
<td align="right">65,527,740</td>
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
<td align="right">20</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">20</td>
<td align="right">50.0%</td>
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
<td align="right">20</td>
<td align="right">100.0%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">249,720</td>
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
<td align="right">40</td>
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
<td align="right">1,547,499,540</td>
<td align="right">53.7%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">83,977,180</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">1,252,204,440</td>
<td align="right">43.4%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">203,520</td>
<td align="right">0.0%</td>
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
<td align="left">CONTAINS_OP</td>
<td align="right">72,746,880</td>
<td align="right">99.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">49,920</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">46,080</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">0</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">101,760</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">101,760</td>
<td align="right">50.0%</td>
</tr>
<tr>
<td align="left">CACHE</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">0</td>
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
<th align="right">Count</th>
<th align="right">Ratio</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">57,446,820</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">87,181,860</td>
<td align="right">60.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">57,446,820</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">57,446,760</td>
<td align="right">39.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">87,654,240</td>
<td align="right">60.6%</td>
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
<td align="right">16,983,180</td>
<td align="right">55.4%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">16,983,100</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">13,698,660</td>
<td align="right">44.6%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">13,696,740</td>
<td align="right">44.6%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">1,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">0</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">14,345,644</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">472,320</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">584,046,540</td>
<td align="right">62.7%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">600,701,920</td>
<td align="right">67.2%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">22,348,775</td>
<td align="right">2.4%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">30,785,559</td>
<td align="right">3.4%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">147,333,300</td>
<td align="right">15.8%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">15,500,280</td>
<td align="right">1.7%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">177,926,684</td>
<td align="right">19.1%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">247,166,799</td>
<td align="right">27.6%</td>
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
<td align="right">102,053</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">47</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">52</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">188,208</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">12</td>
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
<th align="right">Reachable from roots</th>
<th align="right">Not reachable from roots</th>
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
</tr>
<tr>
<td align="right">1</td>
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
<td align="right">20</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-07-13
