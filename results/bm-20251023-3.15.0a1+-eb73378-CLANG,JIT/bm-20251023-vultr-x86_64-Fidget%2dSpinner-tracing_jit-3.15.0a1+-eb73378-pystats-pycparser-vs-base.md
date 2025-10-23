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
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">11,276,680</td>
<td align="right">278,920</td>
<td align="right">-97.5%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">37,932,880</td>
<td align="right">2,321,160</td>
<td align="right">-93.9%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">26,174,520</td>
<td align="right">1,807,240</td>
<td align="right">-93.1%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">26,601,120</td>
<td align="right">2,206,800</td>
<td align="right">-91.7%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">57,997,900</td>
<td align="right">4,945,800</td>
<td align="right">-91.5%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">38,640,980</td>
<td align="right">3,467,060</td>
<td align="right">-91.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">4,138,460</td>
<td align="right">422,600</td>
<td align="right">-89.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">31,292,180</td>
<td align="right">3,526,700</td>
<td align="right">-88.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">11,699,120</td>
<td align="right">1,328,800</td>
<td align="right">-88.6%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">19,697,720</td>
<td align="right">3,016,620</td>
<td align="right">-84.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">5,903,480</td>
<td align="right">956,620</td>
<td align="right">-83.8%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">6,225,720</td>
<td align="right">1,084,280</td>
<td align="right">-82.6%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">18,382,400</td>
<td align="right">3,265,240</td>
<td align="right">-82.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">30,116,640</td>
<td align="right">5,362,180</td>
<td align="right">-82.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">28,587,940</td>
<td align="right">5,157,240</td>
<td align="right">-82.0%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">27,454,460</td>
<td align="right">5,102,020</td>
<td align="right">-81.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">1,195,920</td>
<td align="right">258,020</td>
<td align="right">-78.4%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">10,952,100</td>
<td align="right">2,574,360</td>
<td align="right">-76.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">176,471,000</td>
<td align="right">42,919,880</td>
<td align="right">-75.7%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">263,898,800</td>
<td align="right">66,677,560</td>
<td align="right">-74.7%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">105,292,140</td>
<td align="right">27,309,620</td>
<td align="right">-74.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">36,950,160</td>
<td align="right">10,213,040</td>
<td align="right">-72.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">44,049,700</td>
<td align="right">12,550,220</td>
<td align="right">-71.5%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">7,137,220</td>
<td align="right">2,100,920</td>
<td align="right">-70.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">8,032,220</td>
<td align="right">2,376,400</td>
<td align="right">-70.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">47,252,760</td>
<td align="right">15,263,520</td>
<td align="right">-67.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,898,940</td>
<td align="right">634,620</td>
<td align="right">-66.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">1,495,260</td>
<td align="right">615,400</td>
<td align="right">-58.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">1,461,150,420</td>
<td align="right">615,556,760</td>
<td align="right">-57.9%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">52,349,040</td>
<td align="right">23,836,160</td>
<td align="right">-54.5%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">52,349,040</td>
<td align="right">23,836,160</td>
<td align="right">-54.5%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">185,323,260</td>
<td align="right">86,461,500</td>
<td align="right">-53.3%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">2,240,280</td>
<td align="right">1,053,260</td>
<td align="right">-53.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">94,649,180</td>
<td align="right">45,709,500</td>
<td align="right">-51.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,765,160</td>
<td align="right">858,160</td>
<td align="right">-51.4%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">1,091,700</td>
<td align="right">560,900</td>
<td align="right">-48.6%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,091,760</td>
<td align="right">561,020</td>
<td align="right">-48.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">251,739,960</td>
<td align="right">129,854,820</td>
<td align="right">-48.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,962,600</td>
<td align="right">1,034,620</td>
<td align="right">-47.3%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">234,295,760</td>
<td align="right">124,464,120</td>
<td align="right">-46.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">419,800</td>
<td align="right">225,220</td>
<td align="right">-46.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">3,111,320</td>
<td align="right">1,717,660</td>
<td align="right">-44.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">35,967,840</td>
<td align="right">19,953,660</td>
<td align="right">-44.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">107,327,920</td>
<td align="right">61,330,720</td>
<td align="right">-42.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">7,036,080</td>
<td align="right">4,172,540</td>
<td align="right">-40.7%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">253,782,500</td>
<td align="right">154,199,880</td>
<td align="right">-39.2%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">52,433,280</td>
<td align="right">32,236,440</td>
<td align="right">-38.5%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">10,952,240</td>
<td align="right">6,770,580</td>
<td align="right">-38.2%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,609,400</td>
<td align="right">1,671,500</td>
<td align="right">-35.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">969,720</td>
<td align="right">1,317,080</td>
<td align="right">35.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">109,965,020</td>
<td align="right">72,987,380</td>
<td align="right">-33.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">78,254,500</td>
<td align="right">52,010,340</td>
<td align="right">-33.5%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">88,219,480</td>
<td align="right">68,411,660</td>
<td align="right">-22.5%</td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right">25,093,700</td>
<td align="right">30,726,940</td>
<td align="right">22.4%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">63,978,340</td>
<td align="right">49,859,700</td>
<td align="right">-22.1%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">88,680</td>
<td align="right">70,620</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">162,577,500</td>
<td align="right">133,097,700</td>
<td align="right">-18.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">46,868,280</td>
<td align="right">38,490,640</td>
<td align="right">-17.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">6,336,120</td>
<td align="right">5,208,500</td>
<td align="right">-17.8%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">2,410,980</td>
<td align="right">2,000,280</td>
<td align="right">-17.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">26,781,000</td>
<td align="right">22,387,900</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">7,879,820</td>
<td align="right">6,642,660</td>
<td align="right">-15.7%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,054,520</td>
<td align="right">893,560</td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">28,863,200</td>
<td align="right">24,470,260</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">10,574,580</td>
<td align="right">9,023,060</td>
<td align="right">-14.7%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">35,514,600</td>
<td align="right">30,662,320</td>
<td align="right">-13.7%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">38,713,100</td>
<td align="right">33,527,520</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">106,276,480</td>
<td align="right">92,204,240</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">16,603,860</td>
<td align="right">14,619,160</td>
<td align="right">-12.0%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">139,498,760</td>
<td align="right">122,839,500</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">20,526,900</td>
<td align="right">18,574,440</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">12,358,920</td>
<td align="right">11,189,100</td>
<td align="right">-9.5%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">38,660,500</td>
<td align="right">42,165,060</td>
<td align="right">9.1%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">1,396,240</td>
<td align="right">1,274,260</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">855,060</td>
<td align="right">787,120</td>
<td align="right">-7.9%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">4,013,520</td>
<td align="right">3,757,020</td>
<td align="right">-6.4%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">4,013,340</td>
<td align="right">3,770,480</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">6,266,820</td>
<td align="right">5,898,520</td>
<td align="right">-5.9%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">34,938,680</td>
<td align="right">33,758,400</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">41,912,040</td>
<td align="right">41,912,040</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">1,852,280</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">835,200</td>
<td align="right">835,200</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">669,540</td>
<td align="right">669,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">406,300</td>
<td align="right">406,300</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">379,680</td>
<td align="right">379,680</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">378,060</td>
<td align="right">378,060</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">216,960</td>
<td align="right">216,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">180,960</td>
<td align="right">180,960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">94,920</td>
<td align="right">94,920</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">84,420</td>
<td align="right">84,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">65,880</td>
<td align="right">65,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">65,880</td>
<td align="right">65,880</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">56,100</td>
<td align="right">56,100</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">32,940</td>
<td align="right">32,940</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">30,600</td>
<td align="right">30,600</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">30,420</td>
<td align="right">30,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">30,420</td>
<td align="right">30,420</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">13,860</td>
<td align="right">13,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">13,860</td>
<td align="right">13,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">13,860</td>
<td align="right">13,860</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">3,840</td>
<td align="right">3,840</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">1,980</td>
<td align="right">1,980</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">1,620</td>
<td align="right">1,620</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">1,440</td>
<td align="right">1,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">960</td>
<td align="right">960</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">720</td>
<td align="right">720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">720</td>
<td align="right">720</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">480</td>
<td align="right">480</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">360</td>
<td align="right">360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">360</td>
<td align="right">360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">360</td>
<td align="right">360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_NAME</td>
<td align="right">360</td>
<td align="right">360</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">280</td>
<td align="right">280</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">240</td>
<td align="right">240</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">180</td>
<td align="right">180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">120</td>
<td align="right">120</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">60</td>
<td align="right">60</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">40</td>
<td align="right">40</td>
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
<td align="right">28,855,380</td>
<td align="right">6.5%</td>
<td align="right">24,463,120</td>
<td align="right">5.6%</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">415,632,600</td>
<td align="right">93.5%</td>
<td align="right">415,632,600</td>
<td align="right">94.4%</td>
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
<td align="right">7,760</td>
<td align="right">99.2%</td>
<td align="right">7,080</td>
<td align="right">99.2%</td>
<td align="right">-8.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">60</td>
<td align="right">0.8%</td>
<td align="right">60</td>
<td align="right">0.8%</td>
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
<td align="left">out of range</td>
<td align="right">7,060</td>
<td align="right">91.0%</td>
<td align="right">6,380</td>
<td align="right">90.1%</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">200</td>
<td align="right">2.6%</td>
<td align="right">200</td>
<td align="right">2.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">200</td>
<td align="right">2.6%</td>
<td align="right">200</td>
<td align="right">2.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">120</td>
<td align="right">1.5%</td>
<td align="right">120</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">120</td>
<td align="right">1.5%</td>
<td align="right">120</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">40</td>
<td align="right">0.5%</td>
<td align="right">40</td>
<td align="right">0.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">20</td>
<td align="right">0.3%</td>
<td align="right">20</td>
<td align="right">0.3%</td>
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
<td align="right">26,601,120</td>
<td align="right">100.0%</td>
<td align="right">2,206,800</td>
<td align="right">100.0%</td>
<td align="right">-91.7%</td>
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
<td align="right">28,029,800</td>
<td align="right">9.0%</td>
<td align="right">21,150,440</td>
<td align="right">6.5%</td>
<td align="right">-24.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">28,568,820</td>
<td align="right">9.2%</td>
<td align="right">21,559,620</td>
<td align="right">6.7%</td>
<td align="right">-24.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">282,821,200</td>
<td align="right">90.8%</td>
<td align="right">301,489,080</td>
<td align="right">93.3%</td>
<td align="right">6.6%</td>
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
<td align="right">4,860</td>
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
<td align="right">539,500</td>
<td align="right">100.0%</td>
<td align="right">409,660</td>
<td align="right">100.0%</td>
<td align="right">-24.1%</td>
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
<td align="right">406,200</td>
<td align="right">0.3%</td>
<td align="right">406,200</td>
<td align="right">0.3%</td>
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
<td align="right">130,939,800</td>
<td align="right">99.7%</td>
<td align="right">130,939,800</td>
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
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">100</td>
<td align="right">100.0%</td>
<td align="right">100</td>
<td align="right">100.0%</td>
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
<td align="right">100</td>
<td align="right">100.0%</td>
<td align="right">100</td>
<td align="right">100.0%</td>
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
<td align="right">1,395,660</td>
<td align="right">3.9%</td>
<td align="right">1,273,640</td>
<td align="right">3.5%</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">34,664,280</td>
<td align="right">96.1%</td>
<td align="right">34,664,280</td>
<td align="right">96.5%</td>
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
<td align="right">580</td>
<td align="right">100.0%</td>
<td align="right">620</td>
<td align="right">100.0%</td>
<td align="right">6.9%</td>
</tr>
<tr>
<td align="left">Success</td>
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
<td align="left">tuple</td>
<td align="right">300</td>
<td align="right">51.7%</td>
<td align="right">360</td>
<td align="right">58.1%</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">200</td>
<td align="right">34.5%</td>
<td align="right">180</td>
<td align="right">29.0%</td>
<td align="right">-10.0%</td>
</tr>
<tr>
<td align="left">str</td>
<td align="right">80</td>
<td align="right">13.8%</td>
<td align="right">80</td>
<td align="right">12.9%</td>
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
<td align="right">1,764,480</td>
<td align="right">63.8%</td>
<td align="right">857,580</td>
<td align="right">38.9%</td>
<td align="right">-51.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,000,440</td>
<td align="right">36.2%</td>
<td align="right">1,347,800</td>
<td align="right">61.1%</td>
<td align="right">34.7%</td>
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
<td align="right">680</td>
<td align="right">100.0%</td>
<td align="right">580</td>
<td align="right">100.0%</td>
<td align="right">-14.7%</td>
</tr>
<tr>
<td align="left">Success</td>
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
<td align="left">reversed list</td>
<td align="right">280</td>
<td align="right">41.2%</td>
<td align="right">100</td>
<td align="right">17.2%</td>
<td align="right">-64.3%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">160</td>
<td align="right">23.5%</td>
<td align="right">220</td>
<td align="right">37.9%</td>
<td align="right">37.5%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">100</td>
<td align="right">14.7%</td>
<td align="right">120</td>
<td align="right">20.7%</td>
<td align="right">20.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">60</td>
<td align="right">8.8%</td>
<td align="right">60</td>
<td align="right">10.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">40</td>
<td align="right">5.9%</td>
<td align="right">40</td>
<td align="right">6.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">40</td>
<td align="right">5.9%</td>
<td align="right">40</td>
<td align="right">6.9%</td>
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
<td align="left">list</td>
<td align="right">11,586,960</td>
<td align="right">11,586,960 / 0 !!</td>
<td align="right">11,586,960</td>
<td align="right">11,586,960 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">2,209,860</td>
<td align="right">2,209,860 / 0 !!</td>
<td align="right">2,209,860</td>
<td align="right">2,209,860 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">405,480</td>
<td align="right">405,480 / 0 !!</td>
<td align="right">405,480</td>
<td align="right">405,480 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">14,400</td>
<td align="right">14,400 / 0 !!</td>
<td align="right">14,400</td>
<td align="right">14,400 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">13,860</td>
<td align="right">13,860 / 0 !!</td>
<td align="right">13,860</td>
<td align="right">13,860 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">1,320</td>
<td align="right">1,320 / 0 !!</td>
<td align="right">1,320</td>
<td align="right">1,320 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">360</td>
<td align="right">360 / 0 !!</td>
<td align="right">360</td>
<td align="right">360 / 0 !!</td>
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
<td align="right">35,956,720</td>
<td align="right">6.5%</td>
<td align="right">19,945,740</td>
<td align="right">3.7%</td>
<td align="right">-44.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">10,247,560</td>
<td align="right">1.8%</td>
<td align="right">8,920,620</td>
<td align="right">1.7%</td>
<td align="right">-12.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">510,710,260</td>
<td align="right">91.7%</td>
<td align="right">510,592,060</td>
<td align="right">94.6%</td>
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
<td align="right">380</td>
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
<td align="right">10,760</td>
<td align="right">5.3%</td>
<td align="right">7,560</td>
<td align="right">4.3%</td>
<td align="right">-29.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">193,620</td>
<td align="right">94.7%</td>
<td align="right">168,800</td>
<td align="right">95.7%</td>
<td align="right">-12.8%</td>
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
<td align="right">1,460</td>
<td align="right">13.6%</td>
<td align="right">360</td>
<td align="right">4.8%</td>
<td align="right">-75.3%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">120</td>
<td align="right">1.1%</td>
<td align="right">120</td>
<td align="right">1.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">120</td>
<td align="right">1.1%</td>
<td align="right">120</td>
<td align="right">1.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">100</td>
<td align="right">0.9%</td>
<td align="right">100</td>
<td align="right">1.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">60</td>
<td align="right">0.6%</td>
<td align="right">60</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">40</td>
<td align="right">0.4%</td>
<td align="right">40</td>
<td align="right">0.5%</td>
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
<td align="right">156,887,080</td>
<td align="right">100.0%</td>
<td align="right">143,719,620</td>
<td align="right">100.0%</td>
<td align="right">-8.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">4,060</td>
<td align="right">0.0%</td>
<td align="right">4,060</td>
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
<td align="right">340</td>
<td align="right">100.0%</td>
<td align="right">340</td>
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
<td align="right">8,029,800</td>
<td align="right">3.3%</td>
<td align="right">2,375,240</td>
<td align="right">1.0%</td>
<td align="right">-70.4%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">187,920</td>
<td align="right">0.1%</td>
<td align="right">185,480</td>
<td align="right">0.1%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">231,820,800</td>
<td align="right">96.6%</td>
<td align="right">231,823,200</td>
<td align="right">98.9%</td>
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
<td align="right">2,420</td>
<td align="right">40.6%</td>
<td align="right">1,160</td>
<td align="right">24.9%</td>
<td align="right">-52.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,540</td>
<td align="right">59.4%</td>
<td align="right">3,500</td>
<td align="right">75.1%</td>
<td align="right">-1.1%</td>
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
<td align="left">split dict</td>
<td align="right">2,380</td>
<td align="right">98.3%</td>
<td align="right">1,120</td>
<td align="right">96.6%</td>
<td align="right">-52.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">8,840</td>
<td align="right">365.3%</td>
<td align="right">6,740</td>
<td align="right">581.0%</td>
<td align="right">-23.8%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">40</td>
<td align="right">1.7%</td>
<td align="right">40</td>
<td align="right">3.4%</td>
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
<td align="right">26,772,000</td>
<td align="right">50.2%</td>
<td align="right">22,379,740</td>
<td align="right">45.7%</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">26,554,200</td>
<td align="right">49.8%</td>
<td align="right">26,554,200</td>
<td align="right">54.3%</td>
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
<td align="right">9,000</td>
<td align="right">100.0%</td>
<td align="right">8,160</td>
<td align="right">100.0%</td>
<td align="right">-9.3%</td>
</tr>
<tr>
<td align="left">Success</td>
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
<td align="left">py simple</td>
<td align="right">9,000</td>
<td align="right">100.0%</td>
<td align="right">8,160</td>
<td align="right">100.0%</td>
<td align="right">-9.3%</td>
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
<td align="right">4,573,400</td>
<td align="right">3.5%</td>
<td align="right">821,100</td>
<td align="right">0.7%</td>
<td align="right">-82.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,880,340</td>
<td align="right">1.4%</td>
<td align="right">1,030,160</td>
<td align="right">0.8%</td>
<td align="right">-45.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">124,149,800</td>
<td align="right">95.0%</td>
<td align="right">122,828,640</td>
<td align="right">98.5%</td>
<td align="right">-1.1%</td>
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
<td align="right">120</td>
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
<td align="right">82,240</td>
<td align="right">48.8%</td>
<td align="right">4,440</td>
<td align="right">22.2%</td>
<td align="right">-94.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">86,320</td>
<td align="right">51.2%</td>
<td align="right">15,560</td>
<td align="right">77.8%</td>
<td align="right">-82.0%</td>
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
<td align="right">78,560</td>
<td align="right">95.5%</td>
<td align="right">760</td>
<td align="right">17.1%</td>
<td align="right">-99.0%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">2,660</td>
<td align="right">3.2%</td>
<td align="right">2,660</td>
<td align="right">59.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">1,000</td>
<td align="right">1.2%</td>
<td align="right">1,000</td>
<td align="right">22.5%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">20</td>
<td align="right">0.5%</td>
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
<td align="right">36,819,480</td>
<td align="right">100.0%</td>
<td align="right">36,819,480</td>
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
<td align="right">40</td>
<td align="right">100.0%</td>
<td align="right">40</td>
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
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">3,224,997,120</td>
<td align="right">63.6%</td>
<td align="right">1,488,857,280</td>
<td align="right">58.6%</td>
<td align="right">-53.8%</td>
</tr>
<tr>
<td align="left">
Not specialized
<details>
<summary>ⓘ</summary>

Instructions that could be specialized but aren't, e.g. `LOAD_ATTR`, `BINARY_SLICE`.
</details>
</td>
<td align="right">134,016,760</td>
<td align="right">2.6%</td>
<td align="right">76,022,420</td>
<td align="right">3.0%</td>
<td align="right">-43.3%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">1,664,730,840</td>
<td align="right">32.9%</td>
<td align="right">945,587,740</td>
<td align="right">37.2%</td>
<td align="right">-43.2%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">43,583,840</td>
<td align="right">0.9%</td>
<td align="right">31,493,100</td>
<td align="right">1.2%</td>
<td align="right">-27.7%</td>
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
<td align="left">BINARY_SLICE</td>
<td align="right">26,601,120</td>
<td align="right">16.7%</td>
<td align="right">2,206,800</td>
<td align="right">2.3%</td>
<td align="right">-91.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">8,029,800</td>
<td align="right">5.0%</td>
<td align="right">2,375,240</td>
<td align="right">2.5%</td>
<td align="right">-70.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,764,480</td>
<td align="right">1.1%</td>
<td align="right">857,580</td>
<td align="right">0.9%</td>
<td align="right">-51.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">1,880,340</td>
<td align="right">1.2%</td>
<td align="right">1,030,160</td>
<td align="right">1.1%</td>
<td align="right">-45.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">35,956,720</td>
<td align="right">22.5%</td>
<td align="right">19,945,740</td>
<td align="right">20.8%</td>
<td align="right">-44.5%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">28,029,800</td>
<td align="right">17.6%</td>
<td align="right">21,150,440</td>
<td align="right">22.0%</td>
<td align="right">-24.5%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">26,772,000</td>
<td align="right">16.8%</td>
<td align="right">22,379,740</td>
<td align="right">23.3%</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">28,855,380</td>
<td align="right">18.1%</td>
<td align="right">24,463,120</td>
<td align="right">25.5%</td>
<td align="right">-15.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">1,395,660</td>
<td align="right">0.9%</td>
<td align="right">1,273,640</td>
<td align="right">1.3%</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">406,200</td>
<td align="right">0.3%</td>
<td align="right">406,200</td>
<td align="right">0.4%</td>
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
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">13,887,460</td>
<td align="right">31.9%</td>
<td align="right">1,885,540</td>
<td align="right">6.0%</td>
<td align="right">-86.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">3,435,460</td>
<td align="right">7.9%</td>
<td align="right">480,980</td>
<td align="right">1.5%</td>
<td align="right">-86.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">1,134,580</td>
<td align="right">2.6%</td>
<td align="right">336,760</td>
<td align="right">1.1%</td>
<td align="right">-70.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">14,681,000</td>
<td align="right">33.7%</td>
<td align="right">19,673,720</td>
<td align="right">62.5%</td>
<td align="right">34.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">8,468,680</td>
<td align="right">19.4%</td>
<td align="right">7,291,340</td>
<td align="right">23.2%</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,553,540</td>
<td align="right">3.6%</td>
<td align="right">1,403,940</td>
<td align="right">4.5%</td>
<td align="right">-9.6%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">2,080</td>
<td align="right">0.0%</td>
<td align="right">2,220</td>
<td align="right">0.0%</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">187,560</td>
<td align="right">0.4%</td>
<td align="right">185,120</td>
<td align="right">0.6%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">225,340</td>
<td align="right">0.5%</td>
<td align="right">225,340</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">2,300</td>
<td align="right">0.0%</td>
<td align="right">2,300</td>
<td align="right">0.0%</td>
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
<td align="right">41,912,100</td>
<td align="right">26.4%</td>
<td align="right">41,912,100</td>
<td align="right">26.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">116,652,300</td>
<td align="right">73.6%</td>
<td align="right">116,652,300</td>
<td align="right">73.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">41,912,100</td>
<td align="right">26.4%</td>
<td align="right">41,912,100</td>
<td align="right">26.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">41,911,860</td>
<td align="right">26.4%</td>
<td align="right">41,911,860</td>
<td align="right">26.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">41,911,500</td>
<td align="right">26.4%</td>
<td align="right">41,911,500</td>
<td align="right">26.4%</td>
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
<td align="right">34,854,900</td>
<td align="right">22.0%</td>
<td align="right">34,854,900</td>
<td align="right">22.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">240</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">73,800</td>
<td align="right">0.0%</td>
<td align="right">73,800</td>
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
<tr>
<td align="left">Frame objects created</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">162,577,500</td>
<td align="right">102.5%</td>
<td align="right">162,577,500</td>
<td align="right">102.5%</td>
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
<td align="right">21,132</td>
<td align="right"></td>
<td align="right">232,370</td>
<td align="right"></td>
<td align="right">999.6%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">152,627</td>
<td align="right"></td>
<td align="right">547,431</td>
<td align="right"></td>
<td align="right">258.7%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">139,427</td>
<td align="right"></td>
<td align="right">323,081</td>
<td align="right"></td>
<td align="right">131.7%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">233,021,640</td>
<td align="right">8.5%</td>
<td align="right">91,730,780</td>
<td align="right">3.3%</td>
<td align="right">-60.6%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">692,761,865</td>
<td align="right">23.7%</td>
<td align="right">1,086,934,133</td>
<td align="right">37.1%</td>
<td align="right">56.9%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">57,551,580</td>
<td align="right">2.0%</td>
<td align="right">30,636,600</td>
<td align="right">1.0%</td>
<td align="right">-46.8%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">798,097,391</td>
<td align="right">29.0%</td>
<td align="right">1,136,016,739</td>
<td align="right">41.2%</td>
<td align="right">42.3%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">2,740</td>
<td align="right">0.0%</td>
<td align="right">3,660</td>
<td align="right">0.0%</td>
<td align="right">33.6%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">1,074,687,480</td>
<td align="right">39.1%</td>
<td align="right">743,512,960</td>
<td align="right">27.0%</td>
<td align="right">-30.8%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">1,389,250,240</td>
<td align="right">47.5%</td>
<td align="right">1,001,823,200</td>
<td align="right">34.2%</td>
<td align="right">-27.9%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">643,888,533</td>
<td align="right">23.4%</td>
<td align="right">784,337,571</td>
<td align="right">28.5%</td>
<td align="right">21.8%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">782,674,903</td>
<td align="right">26.8%</td>
<td align="right">808,891,797</td>
<td align="right">27.6%</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">82,263,453</td>
<td align="right"></td>
<td align="right">80,825,079</td>
<td align="right"></td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">84,895,648</td>
<td align="right"></td>
<td align="right">84,682,890</td>
<td align="right"></td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">27,487,200</td>
<td align="right">9.4%</td>
<td align="right">27,487,460</td>
<td align="right">9.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">157,546,440</td>
<td align="right"></td>
<td align="right">157,547,540</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">157,547,780</td>
<td align="right">54.1%</td>
<td align="right">157,548,880</td>
<td align="right">54.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">133,740,560</td>
<td align="right">45.9%</td>
<td align="right">133,741,380</td>
<td align="right">45.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">158,847,928</td>
<td align="right"></td>
<td align="right">158,847,164</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">106,250,620</td>
<td align="right">36.5%</td>
<td align="right">106,250,260</td>
<td align="right">36.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">36,013,800</td>
<td align="right"></td>
<td align="right">36,013,800</td>
<td align="right"></td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">360</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
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
<td align="right">6,660</td>
<td align="right">4,993,040</td>
<td align="right">197,448,731</td>
<td align="right">13,917,200</td>
<td align="right">17,997,240</td>
<td align="right">6,660</td>
<td align="right">4,993,040</td>
<td align="right">197,561,737</td>
<td align="right">13,961,200</td>
<td align="right">17,951,880</td>
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
<td align="right">460</td>
<td align="right">5.3%</td>
<td align="right">1,400</td>
<td align="right">5.5%</td>
<td align="right">204.3%</td>
</tr>
<tr>
<td align="left">
Optimization attempts
<details>
<summary>ⓘ</summary>

The number of times a potential trace is identified.  Specifically, this occurs in the JUMP BACKWARD instruction when the counter reaches a threshold.
</details>
</td>
<td align="right">8,660</td>
<td align="right"></td>
<td align="right">25,460</td>
<td align="right"></td>
<td align="right">194.0%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">120</td>
<td align="right">26.1%</td>
<td align="right">340</td>
<td align="right">24.3%</td>
<td align="right">183.3%</td>
</tr>
<tr>
<td align="left">
Uops executed
<details>
<summary>ⓘ</summary>

The total number of uops (micro-operations) that were executed
</details>
</td>
<td align="right">3,734,602,200</td>
<td align="right">3,844.3%</td>
<td align="right">9,668,993,600</td>
<td align="right">5,690.2%</td>
<td align="right">158.9%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">2,380</td>
<td align="right">27.5%</td>
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
<td align="right">40</td>
<td align="right">0.5%</td>
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
<td align="right">160</td>
<td align="right">1.8%</td>
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
<td align="right">5,780</td>
<td align="right">66.7%</td>
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
<td align="right">97,147,200</td>
<td align="right"></td>
<td align="right">169,923,620</td>
<td align="right"></td>
<td align="right">74.9%</td>
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
<td align="right">60</td>
<td align="right">0.2%</td>
<td align="right">60 / 0 !!</td>
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
<td align="right">20</td>
<td align="right">0.1%</td>
<td align="right">20 / 0 !!</td>
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
<td align="right">240</td>
<td align="right">52.2%</td>
<td align="right">1,400</td>
<td align="right">100.0%</td>
<td align="right">483.3%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">460</td>
<td align="right"></td>
<td align="right">1,400</td>
<td align="right"></td>
<td align="right">204.3%</td>
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
<td align="right">3,384,900</td>
<td align="right">84.3%</td>
<td align="right">42,130,080</td>
<td align="right">92.2%</td>
<td align="right">1,144.6%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">4,014,080</td>
<td align="right"></td>
<td align="right">45,711,360</td>
<td align="right"></td>
<td align="right">1,038.8%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">69,280</td>
<td align="right">1.7%</td>
<td align="right">677,120</td>
<td align="right">1.5%</td>
<td align="right">877.4%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">559,660</td>
<td align="right">13.9%</td>
<td align="right">2,902,760</td>
<td align="right">6.4%</td>
<td align="right">418.7%</td>
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
<td align="left">80</td>
<td align="right">33.3%</td>
<td align="left">20</td>
<td align="right">1.4%</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">40</td>
<td align="right">16.7%</td>
<td align="left">280</td>
<td align="right">20.0%</td>
<td align="right">600.0%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">40</td>
<td align="right">16.7%</td>
<td align="left">160</td>
<td align="right">11.4%</td>
<td align="right">300.0%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">40</td>
<td align="right">16.7%</td>
<td align="left">520</td>
<td align="right">37.1%</td>
<td align="right">1,200.0%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left">40</td>
<td align="right">16.7%</td>
<td align="left">260</td>
<td align="right">18.6%</td>
<td align="right">550.0%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">160</td>
<td align="right">11.4%</td>
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
<td align="left"><= 16</td>
<td align="right">80</td>
<td align="right">17.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">40</td>
<td align="right">8.7%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">60</td>
<td align="right">13.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">280</td>
<td align="right">60.9%</td>
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
<td align="right">20</td>
<td align="right">4.3%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">60</td>
<td align="right">13.0%</td>
<td align="right">20</td>
<td align="right">1.4%</td>
<td align="right">-66.7%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">40</td>
<td align="right">8.7%</td>
<td align="right">280</td>
<td align="right">20.0%</td>
<td align="right">600.0%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">40</td>
<td align="right">8.7%</td>
<td align="right">240</td>
<td align="right">17.1%</td>
<td align="right">500.0%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">60</td>
<td align="right">13.0%</td>
<td align="right">500</td>
<td align="right">35.7%</td>
<td align="right">733.3%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">20</td>
<td align="right">4.3%</td>
<td align="right">260</td>
<td align="right">18.6%</td>
<td align="right">1,200.0%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">100</td>
<td align="right">7.1%</td>
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
<td align="left">_GUARD_NOS_OVERFLOWED</td>
<td align="right">8,700</td>
<td align="right">2,177,460</td>
<td align="right">24,928.3%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">8,700</td>
<td align="right">1,993,400</td>
<td align="right">22,812.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">210,920</td>
<td align="right">8,407,080</td>
<td align="right">3,885.9%</td>
</tr>
<tr>
<td align="left">_SWAP_3</td>
<td align="right">626,280</td>
<td align="right">8,066,120</td>
<td align="right">1,187.9%</td>
</tr>
<tr>
<td align="left">_CALL_KW_NON_PY</td>
<td align="right">109,720</td>
<td align="right">1,346,880</td>
<td align="right">1,127.6%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE_KW</td>
<td align="right">109,720</td>
<td align="right">1,346,880</td>
<td align="right">1,127.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">3,381,160</td>
<td align="right">40,358,800</td>
<td align="right">1,093.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">109,720</td>
<td align="right">1,303,020</td>
<td align="right">1,087.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">3,257,320</td>
<td align="right">31,022,800</td>
<td align="right">852.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">9,895,800</td>
<td align="right">85,359,360</td>
<td align="right">762.6%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">19,455,160</td>
<td align="right">153,006,280</td>
<td align="right">686.5%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION_AND_LOCK</td>
<td align="right">19,455,160</td>
<td align="right">153,006,280</td>
<td align="right">686.5%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">19,455,160</td>
<td align="right">153,006,280</td>
<td align="right">686.5%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">3,361,900</td>
<td align="right">24,975,820</td>
<td align="right">642.9%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">11,474,840</td>
<td align="right">83,960,420</td>
<td align="right">631.7%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">3,989,040</td>
<td align="right">27,377,800</td>
<td align="right">586.3%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">13,272,680</td>
<td align="right">82,965,620</td>
<td align="right">525.1%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">33,380,480</td>
<td align="right">186,248,140</td>
<td align="right">458.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">168,274,340</td>
<td align="right">862,918,060</td>
<td align="right">412.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">44,691,240</td>
<td align="right">227,871,900</td>
<td align="right">409.9%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">16,752,360</td>
<td align="right">70,870,680</td>
<td align="right">323.0%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">3,396,900</td>
<td align="right">13,573,800</td>
<td align="right">299.6%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">80</td>
<td align="right">300</td>
<td align="right">275.0%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">10,337,140</td>
<td align="right">38,214,220</td>
<td align="right">269.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">10,337,140</td>
<td align="right">38,214,220</td>
<td align="right">269.7%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">2,179,420</td>
<td align="right">7,365,000</td>
<td align="right">237.9%</td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right">1,380</td>
<td align="right">4,520</td>
<td align="right">227.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">5,443,480</td>
<td align="right">17,743,120</td>
<td align="right">226.0%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">6,514,640</td>
<td align="right">20,633,280</td>
<td align="right">216.7%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">6,514,640</td>
<td align="right">20,633,280</td>
<td align="right">216.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">6,514,640</td>
<td align="right">20,633,280</td>
<td align="right">216.7%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">8,700</td>
<td align="right">26,760</td>
<td align="right">207.6%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">62,614,000</td>
<td align="right">184,477,100</td>
<td align="right">194.6%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">62,614,000</td>
<td align="right">184,477,100</td>
<td align="right">194.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">20,944,420</td>
<td align="right">60,075,900</td>
<td align="right">186.8%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">57,615,380</td>
<td align="right">158,556,020</td>
<td align="right">175.2%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">637,274,120</td>
<td align="right">1,697,695,100</td>
<td align="right">166.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right">15,925,980</td>
<td align="right">41,878,680</td>
<td align="right">163.0%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">33,042,040</td>
<td align="right">86,775,180</td>
<td align="right">162.6%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">614,031,940</td>
<td align="right">1,577,813,940</td>
<td align="right">157.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_DICT</td>
<td align="right">16,850,000</td>
<td align="right">43,094,160</td>
<td align="right">155.8%</td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right">626,280</td>
<td align="right">1,564,180</td>
<td align="right">149.8%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">33,050,740</td>
<td align="right">81,990,420</td>
<td align="right">148.1%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">103,914,460</td>
<td align="right">256,391,660</td>
<td align="right">146.7%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">109,720</td>
<td align="right">270,680</td>
<td align="right">146.7%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">22,493,220</td>
<td align="right">49,230,340</td>
<td align="right">118.9%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">3,381,160</td>
<td align="right">7,331,160</td>
<td align="right">116.8%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">15,882,920</td>
<td align="right">34,268,500</td>
<td align="right">115.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">60,328,840</td>
<td align="right">129,861,820</td>
<td align="right">115.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">6,638,480</td>
<td align="right">14,250,140</td>
<td align="right">114.7%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">33,967,060</td>
<td align="right">69,140,980</td>
<td align="right">103.6%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">33,967,060</td>
<td align="right">69,140,980</td>
<td align="right">103.6%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">1,143,880</td>
<td align="right">2,324,120</td>
<td align="right">103.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">15,695,060</td>
<td align="right">31,785,040</td>
<td align="right">102.5%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">11,285,920</td>
<td align="right">22,452,680</td>
<td align="right">98.9%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">72,054,580</td>
<td align="right">141,200,880</td>
<td align="right">96.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,340,940</td>
<td align="right">2,605,260</td>
<td align="right">94.3%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">72,053,120</td>
<td align="right">139,196,080</td>
<td align="right">93.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">45,376,780</td>
<td align="right">86,048,480</td>
<td align="right">89.6%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">9,229,960</td>
<td align="right">17,480,080</td>
<td align="right">89.4%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">19,065,220</td>
<td align="right">35,724,700</td>
<td align="right">87.4%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">1,036,680</td>
<td align="right">1,916,540</td>
<td align="right">84.9%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">44,761,380</td>
<td align="right">81,496,860</td>
<td align="right">82.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">59,181,400</td>
<td align="right">105,048,740</td>
<td align="right">77.5%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">90,233,480</td>
<td align="right">159,485,500</td>
<td align="right">76.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">109,720</td>
<td align="right">186,800</td>
<td align="right">70.3%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">19,065,220</td>
<td align="right">30,615,920</td>
<td align="right">60.6%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">19,065,220</td>
<td align="right">30,615,920</td>
<td align="right">60.6%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">626,280</td>
<td align="right">994,580</td>
<td align="right">58.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">87,381,340</td>
<td align="right">136,899,120</td>
<td align="right">56.7%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">79,932,300</td>
<td align="right">122,284,940</td>
<td align="right">53.0%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">23,387,600</td>
<td align="right">34,385,360</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right">23,387,600</td>
<td align="right">34,385,360</td>
<td align="right">47.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">44,804,720</td>
<td align="right">64,100,140</td>
<td align="right">43.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right">2,626,340</td>
<td align="right">3,751,180</td>
<td align="right">42.8%</td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right">1,271,820</td>
<td align="right">1,682,520</td>
<td align="right">32.3%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">31,106,760</td>
<td align="right">40,228,920</td>
<td align="right">29.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">49,693,640</td>
<td align="right">36,658,900</td>
<td align="right">-26.2%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">7,779,300</td>
<td align="right">9,652,760</td>
<td align="right">24.1%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">7,779,300</td>
<td align="right">9,652,760</td>
<td align="right">24.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">11,956,860</td>
<td align="right">14,614,980</td>
<td align="right">22.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">21,921,660</td>
<td align="right">26,739,960</td>
<td align="right">22.0%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">17,695,480</td>
<td align="right">21,406,060</td>
<td align="right">21.0%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">59,428,220</td>
<td align="right">71,093,160</td>
<td align="right">19.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">11,511,420</td>
<td align="right">13,647,140</td>
<td align="right">18.6%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">5,234,760</td>
<td align="right">6,141,660</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">30,593,760</td>
<td align="right">35,735,200</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">30,593,760</td>
<td align="right">35,735,200</td>
<td align="right">16.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">24,228,340</td>
<td align="right">28,000,820</td>
<td align="right">15.6%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">25,092,620</td>
<td align="right">28,722,740</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">8,377,620</td>
<td align="right">9,315,520</td>
<td align="right">11.2%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">11,991,960</td>
<td align="right">13,178,980</td>
<td align="right">9.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">1,391,440</td>
<td align="right">1,513,100</td>
<td align="right">8.7%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">3,642,000</td>
<td align="right">3,331,180</td>
<td align="right">-8.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right">18,904,020</td>
<td align="right">20,168,340</td>
<td align="right">6.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">8,584,700</td>
<td align="right">9,094,180</td>
<td align="right">5.9%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">8,199,520</td>
<td align="right">8,645,380</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right">7,779,300</td>
<td align="right">8,095,300</td>
<td align="right">4.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">27,849,440</td>
<td align="right">28,913,380</td>
<td align="right">3.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">27,203,900</td>
<td align="right">28,003,580</td>
<td align="right">2.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">45,997,320</td>
<td align="right">46,736,760</td>
<td align="right">1.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">31,645,080</td>
<td align="right">31,297,720</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">31,645,080</td>
<td align="right">31,297,720</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">29,297,100</td>
<td align="right">29,595,280</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">15,558,600</td>
<td align="right">15,671,160</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">17,991,300</td>
<td align="right">18,113,320</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">27,203,380</td>
<td align="right">27,379,980</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">18,178,980</td>
<td align="right">18,284,920</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">19,065,220</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">17,563,080</td>
<td align="right">17,563,080</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_LIST</td>
<td align="right">8,405,580</td>
<td align="right">8,405,580</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">8,405,580</td>
<td align="right">8,405,580</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">1,252,560</td>
<td align="right">1,252,560</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">645,540</td>
<td align="right">645,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">645,540</td>
<td align="right">645,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">645,540</td>
<td align="right">645,540</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right"></td>
<td align="right">77,982,520</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">65,204,500</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right"></td>
<td align="right">46,809,920</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right"></td>
<td align="right">29,479,800</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right"></td>
<td align="right">28,512,880</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right"></td>
<td align="right">28,512,880</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right"></td>
<td align="right">27,812,720</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right"></td>
<td align="right">24,754,460</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right"></td>
<td align="right">24,394,320</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right"></td>
<td align="right">24,367,280</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_0</td>
<td align="right"></td>
<td align="right">24,292,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right"></td>
<td align="right">11,280,100</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right"></td>
<td align="right">6,980,760</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right"></td>
<td align="right">6,755,160</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right"></td>
<td align="right">5,654,560</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right"></td>
<td align="right">5,004,100</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right"></td>
<td align="right">5,004,100</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_CHECK_FUNC</td>
<td align="right"></td>
<td align="right">4,852,280</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_INIT_CALL</td>
<td align="right"></td>
<td align="right">4,852,280</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_1</td>
<td align="right"></td>
<td align="right">4,748,280</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right"></td>
<td align="right">4,392,260</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right"></td>
<td align="right">4,392,260</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right"></td>
<td align="right">3,715,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right"></td>
<td align="right">3,715,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right"></td>
<td align="right">2,088,620</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">1,999,980</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right"></td>
<td align="right">1,557,460</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right"></td>
<td align="right">1,169,820</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right"></td>
<td align="right">937,900</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right"></td>
<td align="right">656,060</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right"></td>
<td align="right">530,800</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right"></td>
<td align="right">530,740</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right"></td>
<td align="right">359,220</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_AND_ALLOCATE_OBJECT</td>
<td align="right"></td>
<td align="right">256,500</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CREATE_INIT_FRAME</td>
<td align="right"></td>
<td align="right">256,500</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_INIT_CHECK</td>
<td align="right"></td>
<td align="right">242,860</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LEN</td>
<td align="right"></td>
<td align="right">227,140</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_3</td>
<td align="right"></td>
<td align="right">208,400</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NULL</td>
<td align="right"></td>
<td align="right">200,380</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT</td>
<td align="right"></td>
<td align="right">185,100</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_2</td>
<td align="right"></td>
<td align="right">153,040</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_KW</td>
<td align="right"></td>
<td align="right">67,940</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_PY_FRAME_KW</td>
<td align="right"></td>
<td align="right">67,940</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right"></td>
<td align="right">14,720</td>
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
<td align="left">CALL</td>
<td align="right">40</td>
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
watched dict modification
<details>
<summary>ⓘ</summary>

A watched dict has been modified
</details>
</td>
<td align="right">120</td>
<td align="right">160</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">
watched globals modification
<details>
<summary>ⓘ</summary>

A watched `globals()` dict has been modified
</details>
</td>
<td align="right">120</td>
<td align="right">160</td>
<td align="right">33.3%</td>
</tr>
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
<td align="right">20</td>
<td align="right">20</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-10-23
