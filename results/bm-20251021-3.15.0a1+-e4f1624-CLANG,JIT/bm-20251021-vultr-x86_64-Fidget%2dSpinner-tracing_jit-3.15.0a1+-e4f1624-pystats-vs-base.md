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
<td align="left">ENTER_EXECUTOR</td>
<td align="right">743,819,905</td>
<td align="right">1,548,866,981</td>
<td align="right">108.2%</td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">1,684,562</td>
<td align="right">140,400</td>
<td align="right">-91.7%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">345,650,812</td>
<td align="right">45,158,009</td>
<td align="right">-86.9%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,156,329</td>
<td align="right">859,449</td>
<td align="right">-86.0%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">56,950,488</td>
<td align="right">8,105,912</td>
<td align="right">-85.8%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right">1,375,253,159</td>
<td align="right">218,755,362</td>
<td align="right">-84.1%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">166,050,406</td>
<td align="right">27,368,422</td>
<td align="right">-83.5%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">7,195,408</td>
<td align="right">1,367,387</td>
<td align="right">-81.0%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">131,380,689</td>
<td align="right">25,603,258</td>
<td align="right">-80.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">249,680,471</td>
<td align="right">49,139,452</td>
<td align="right">-80.3%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">9,836,551</td>
<td align="right">2,039,897</td>
<td align="right">-79.3%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">62,089,379</td>
<td align="right">14,955,335</td>
<td align="right">-75.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">205,201,080</td>
<td align="right">50,724,908</td>
<td align="right">-75.3%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">97,601,075</td>
<td align="right">26,451,051</td>
<td align="right">-72.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">241,730,867</td>
<td align="right">73,757,815</td>
<td align="right">-69.5%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">139,585,240</td>
<td align="right">42,756,435</td>
<td align="right">-69.4%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">28,498,091</td>
<td align="right">8,757,369</td>
<td align="right">-69.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">49,565,515</td>
<td align="right">15,845,523</td>
<td align="right">-68.0%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">2,075,203</td>
<td align="right">708,686</td>
<td align="right">-65.8%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">783,913,335</td>
<td align="right">272,985,199</td>
<td align="right">-65.2%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">320,356,612</td>
<td align="right">113,317,308</td>
<td align="right">-64.6%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">542,353,298</td>
<td align="right">204,623,402</td>
<td align="right">-62.3%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">64,814,347</td>
<td align="right">25,494,803</td>
<td align="right">-60.7%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">26,549,574</td>
<td align="right">10,448,027</td>
<td align="right">-60.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">279,400,372</td>
<td align="right">110,059,858</td>
<td align="right">-60.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">572,214,314</td>
<td align="right">226,364,719</td>
<td align="right">-60.4%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">310,432,023</td>
<td align="right">126,091,793</td>
<td align="right">-59.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">158,623,007</td>
<td align="right">65,339,734</td>
<td align="right">-58.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">165,455,834</td>
<td align="right">68,486,767</td>
<td align="right">-58.6%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">1,232,574</td>
<td align="right">536,570</td>
<td align="right">-56.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,351,471,284</td>
<td align="right">590,656,408</td>
<td align="right">-56.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,076,668,832</td>
<td align="right">471,068,518</td>
<td align="right">-56.2%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">171,634,000</td>
<td align="right">75,203,287</td>
<td align="right">-56.2%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">55,173,576</td>
<td align="right">25,038,108</td>
<td align="right">-54.6%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">274,336,397</td>
<td align="right">127,484,934</td>
<td align="right">-53.5%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">813,084,264</td>
<td align="right">379,160,701</td>
<td align="right">-53.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">194,808,561</td>
<td align="right">91,523,332</td>
<td align="right">-53.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">4,879,202,821</td>
<td align="right">2,344,542,155</td>
<td align="right">-51.9%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">319,328,933</td>
<td align="right">153,959,607</td>
<td align="right">-51.8%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">343,641,924</td>
<td align="right">169,595,803</td>
<td align="right">-50.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">566,651,057</td>
<td align="right">282,170,292</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">LOAD_NAME</td>
<td align="right">9,738,721</td>
<td align="right">4,862,941</td>
<td align="right">-50.1%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">6,445,684,888</td>
<td align="right">3,225,058,294</td>
<td align="right">-50.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,160,546,821</td>
<td align="right">1,094,622,938</td>
<td align="right">-49.3%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">102,915,688</td>
<td align="right">52,190,341</td>
<td align="right">-49.3%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">467,629,575</td>
<td align="right">242,941,678</td>
<td align="right">-48.0%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">331,730,339</td>
<td align="right">173,164,656</td>
<td align="right">-47.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">474,558,885</td>
<td align="right">248,569,475</td>
<td align="right">-47.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">98,630,908</td>
<td align="right">52,762,530</td>
<td align="right">-46.5%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">1,062,191,429</td>
<td align="right">571,621,961</td>
<td align="right">-46.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">1,138,259,604</td>
<td align="right">613,253,633</td>
<td align="right">-46.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">371,561,742</td>
<td align="right">204,500,833</td>
<td align="right">-45.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">495,978,644</td>
<td align="right">273,087,726</td>
<td align="right">-44.9%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">110,718,694</td>
<td align="right">61,012,685</td>
<td align="right">-44.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">601,394,962</td>
<td align="right">333,503,341</td>
<td align="right">-44.5%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">201,330,140</td>
<td align="right">112,501,476</td>
<td align="right">-44.1%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">2,937,361,593</td>
<td align="right">1,642,577,462</td>
<td align="right">-44.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">4,806,657,146</td>
<td align="right">2,696,611,571</td>
<td align="right">-43.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">43,852,466</td>
<td align="right">24,759,257</td>
<td align="right">-43.5%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">137,556,172</td>
<td align="right">78,350,178</td>
<td align="right">-43.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,441,167,221</td>
<td align="right">1,979,669,673</td>
<td align="right">-42.5%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">659,396,776</td>
<td align="right">381,590,814</td>
<td align="right">-42.1%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">314,730,043</td>
<td align="right">183,704,133</td>
<td align="right">-41.6%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">326,064,817</td>
<td align="right">190,956,035</td>
<td align="right">-41.4%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">5,878,564,341</td>
<td align="right">3,477,610,784</td>
<td align="right">-40.8%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">24,754,352,426</td>
<td align="right">14,666,165,124</td>
<td align="right">-40.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">204,789,287</td>
<td align="right">122,354,214</td>
<td align="right">-40.3%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">131,623,348</td>
<td align="right">79,180,814</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">294,480,691</td>
<td align="right">177,239,275</td>
<td align="right">-39.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">145,102,858</td>
<td align="right">87,527,452</td>
<td align="right">-39.7%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">875,368,020</td>
<td align="right">528,504,402</td>
<td align="right">-39.6%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">2,876,171,686</td>
<td align="right">1,746,043,733</td>
<td align="right">-39.3%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">994,083,429</td>
<td align="right">616,897,280</td>
<td align="right">-37.9%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">166,357,956</td>
<td align="right">103,299,905</td>
<td align="right">-37.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">1,634,463,828</td>
<td align="right">1,023,600,871</td>
<td align="right">-37.4%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,492,539,725</td>
<td align="right">2,188,556,028</td>
<td align="right">-37.3%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">811,077,025</td>
<td align="right">520,062,913</td>
<td align="right">-35.9%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">150,188,978</td>
<td align="right">96,417,255</td>
<td align="right">-35.8%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">294,235,723</td>
<td align="right">189,021,348</td>
<td align="right">-35.8%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">142,722,718</td>
<td align="right">92,311,024</td>
<td align="right">-35.3%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">71,767,860</td>
<td align="right">46,991,643</td>
<td align="right">-34.5%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">106,674,795</td>
<td align="right">70,097,197</td>
<td align="right">-34.3%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">141,211,225</td>
<td align="right">94,136,760</td>
<td align="right">-33.3%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">1,440,120,504</td>
<td align="right">965,314,543</td>
<td align="right">-33.0%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">578,011,172</td>
<td align="right">388,559,726</td>
<td align="right">-32.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">6,124,768,197</td>
<td align="right">4,130,317,492</td>
<td align="right">-32.6%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">70,692,032</td>
<td align="right">47,955,433</td>
<td align="right">-32.2%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">114,997,567</td>
<td align="right">78,288,503</td>
<td align="right">-31.9%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,109,800,798</td>
<td align="right">2,131,583,887</td>
<td align="right">-31.5%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">96,006,542</td>
<td align="right">126,007,718</td>
<td align="right">31.2%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">485,760,380</td>
<td align="right">337,420,006</td>
<td align="right">-30.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,159,400,671</td>
<td align="right">806,580,796</td>
<td align="right">-30.4%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">4,965,877,422</td>
<td align="right">3,456,160,023</td>
<td align="right">-30.4%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,575,068,865</td>
<td align="right">4,583,231,449</td>
<td align="right">-30.3%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">315,189,697</td>
<td align="right">220,838,661</td>
<td align="right">-29.9%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">3,974,031</td>
<td align="right">2,796,920</td>
<td align="right">-29.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">373,630,761</td>
<td align="right">264,830,879</td>
<td align="right">-29.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">525,417,974</td>
<td align="right">372,540,967</td>
<td align="right">-29.1%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">442,903,131</td>
<td align="right">315,504,209</td>
<td align="right">-28.8%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">50,573,003</td>
<td align="right">36,238,884</td>
<td align="right">-28.3%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">3,167,828,705</td>
<td align="right">2,286,296,816</td>
<td align="right">-27.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">249,354,690</td>
<td align="right">182,072,302</td>
<td align="right">-27.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">611,388,695</td>
<td align="right">447,013,697</td>
<td align="right">-26.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">70,072,550</td>
<td align="right">51,363,061</td>
<td align="right">-26.7%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">205,967,457</td>
<td align="right">152,474,004</td>
<td align="right">-26.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">172,421,837</td>
<td align="right">128,426,939</td>
<td align="right">-25.5%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">1,001,868,136</td>
<td align="right">753,867,617</td>
<td align="right">-24.8%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">17,502,886</td>
<td align="right">13,202,474</td>
<td align="right">-24.6%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">54,407,878</td>
<td align="right">67,092,890</td>
<td align="right">23.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">509,447,320</td>
<td align="right">391,855,722</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">331,906,363</td>
<td align="right">256,112,064</td>
<td align="right">-22.8%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">41,073,063</td>
<td align="right">32,043,364</td>
<td align="right">-22.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">180,866,498</td>
<td align="right">144,373,117</td>
<td align="right">-20.2%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">369,342,222</td>
<td align="right">296,449,129</td>
<td align="right">-19.7%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">553,309,858</td>
<td align="right">447,233,429</td>
<td align="right">-19.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">8,560,204</td>
<td align="right">7,045,217</td>
<td align="right">-17.7%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">323,949,532</td>
<td align="right">269,800,956</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">326,002,438</td>
<td align="right">271,712,047</td>
<td align="right">-16.7%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">196,692,036</td>
<td align="right">163,962,383</td>
<td align="right">-16.6%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">59,731,885</td>
<td align="right">50,073,242</td>
<td align="right">-16.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">114,562,392</td>
<td align="right">96,334,274</td>
<td align="right">-15.9%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">42,461,633</td>
<td align="right">35,752,145</td>
<td align="right">-15.8%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">61,109,231</td>
<td align="right">51,580,540</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">158,660,719</td>
<td align="right">134,360,531</td>
<td align="right">-15.3%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">6,269,535</td>
<td align="right">5,343,519</td>
<td align="right">-14.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">3,423,912</td>
<td align="right">3,904,733</td>
<td align="right">14.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">15,587,995</td>
<td align="right">13,477,196</td>
<td align="right">-13.5%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">93,053,504</td>
<td align="right">81,752,017</td>
<td align="right">-12.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">3,023,923,533</td>
<td align="right">2,663,788,913</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">40,587,878</td>
<td align="right">35,808,064</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,151,201,022</td>
<td align="right">1,022,699,479</td>
<td align="right">-11.2%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">46,428,605</td>
<td align="right">41,546,267</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">70,937,221</td>
<td align="right">63,691,160</td>
<td align="right">-10.2%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">1,544,931,451</td>
<td align="right">1,410,988,055</td>
<td align="right">-8.7%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">418,753,267</td>
<td align="right">387,678,114</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">10,389,715</td>
<td align="right">9,620,273</td>
<td align="right">-7.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">367,104,097</td>
<td align="right">340,594,233</td>
<td align="right">-7.2%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">630,144,109</td>
<td align="right">670,242,466</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">235,809</td>
<td align="right">221,167</td>
<td align="right">-6.2%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">593,230,387</td>
<td align="right">556,756,102</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">122,065,624</td>
<td align="right">114,739,222</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">12,124,739</td>
<td align="right">11,397,341</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">35,435,819</td>
<td align="right">33,375,566</td>
<td align="right">-5.8%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">6,775,542</td>
<td align="right">6,437,837</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">70,296,197</td>
<td align="right">73,746,034</td>
<td align="right">4.9%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">143,959,325</td>
<td align="right">137,925,291</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">172,683,388</td>
<td align="right">167,527,350</td>
<td align="right">-3.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">302,140,427</td>
<td align="right">294,579,774</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">297,181,339</td>
<td align="right">290,549,447</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">71,549,631</td>
<td align="right">70,066,998</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">36,897,410</td>
<td align="right">36,200,451</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">43,316,829</td>
<td align="right">42,735,072</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">22,179,370</td>
<td align="right">21,894,359</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">1,214,968</td>
<td align="right">1,202,157</td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">1,890,276,271</td>
<td align="right">1,877,643,530</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">11,674</td>
<td align="right">11,728</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">4,510,167</td>
<td align="right">4,492,381</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">219,535,658</td>
<td align="right">218,673,749</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">222,325</td>
<td align="right">222,792</td>
<td align="right">0.2%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">31,211</td>
<td align="right">31,181</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">25,554,390</td>
<td align="right">25,535,919</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">8,975,993</td>
<td align="right">8,971,093</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">2,348</td>
<td align="right">2,347</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">6,530</td>
<td align="right">6,528</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,440,667</td>
<td align="right">128,462,129</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">437,386</td>
<td align="right">437,437</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">91,596</td>
<td align="right">91,588</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">331,611</td>
<td align="right">331,592</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">25,211,697</td>
<td align="right">25,210,639</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">25,554,392</td>
<td align="right">25,553,334</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">14,736,877</td>
<td align="right">14,737,435</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">9,211,961</td>
<td align="right">9,211,893</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">8,594,662</td>
<td align="right">8,594,674</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">6,248,578</td>
<td align="right">6,248,570</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_LINE</td>
<td align="right">58,270,440</td>
<td align="right">58,270,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">41,964,183</td>
<td align="right">41,964,183</td>
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
<td align="left">GET_AITER</td>
<td align="right">6,000,000</td>
<td align="right">6,000,000</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
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
<td align="left">SET_ADD</td>
<td align="right">73,592</td>
<td align="right">73,592</td>
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
<td align="right">47,906</td>
<td align="right">47,906</td>
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
<td align="right">9,631</td>
<td align="right">9,631</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">3,375</td>
<td align="right">3,375</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">3,352</td>
<td align="right">3,352</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">FORMAT_WITH_SPEC</td>
<td align="right">2,740</td>
<td align="right">2,740</td>
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
<td align="right">1,350,902,181</td>
<td align="right">7.5%</td>
<td align="right">590,268,681</td>
<td align="right">3.4%</td>
<td align="right">-56.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">61,043,957</td>
<td align="right">0.3%</td>
<td align="right">41,203,201</td>
<td align="right">0.2%</td>
<td align="right">-32.5%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">16,713,032,285</td>
<td align="right">92.2%</td>
<td align="right">16,666,814,984</td>
<td align="right">96.3%</td>
<td align="right">-0.3%</td>
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
<td align="right">1,111</td>
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
<td align="right">552,511</td>
<td align="right">32.1%</td>
<td align="right">371,148</td>
<td align="right">31.8%</td>
<td align="right">-32.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,168,064</td>
<td align="right">67.9%</td>
<td align="right">794,290</td>
<td align="right">68.2%</td>
<td align="right">-32.0%</td>
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
<td align="left">subscr mappingproxy</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">240</td>
<td align="right">0.1%</td>
<td align="right">300.0%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">320</td>
<td align="right">0.1%</td>
<td align="right">1,078</td>
<td align="right">0.3%</td>
<td align="right">236.9%</td>
</tr>
<tr>
<td align="left">subscr bytes</td>
<td align="right">1,808</td>
<td align="right">0.3%</td>
<td align="right">4,728</td>
<td align="right">1.3%</td>
<td align="right">161.5%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">7,170</td>
<td align="right">1.3%</td>
<td align="right">14,893</td>
<td align="right">4.0%</td>
<td align="right">107.7%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">11,588</td>
<td align="right">2.1%</td>
<td align="right">1,827</td>
<td align="right">0.5%</td>
<td align="right">-84.2%</td>
</tr>
<tr>
<td align="left">subscr array</td>
<td align="right">36,682</td>
<td align="right">6.6%</td>
<td align="right">6,384</td>
<td align="right">1.7%</td>
<td align="right">-82.6%</td>
</tr>
<tr>
<td align="left">xor int</td>
<td align="right">16,760</td>
<td align="right">3.0%</td>
<td align="right">3,680</td>
<td align="right">1.0%</td>
<td align="right">-78.0%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">11,295</td>
<td align="right">2.0%</td>
<td align="right">2,842</td>
<td align="right">0.8%</td>
<td align="right">-74.8%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">15,423</td>
<td align="right">2.8%</td>
<td align="right">4,604</td>
<td align="right">1.2%</td>
<td align="right">-70.1%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">18,468</td>
<td align="right">3.3%</td>
<td align="right">7,863</td>
<td align="right">2.1%</td>
<td align="right">-57.4%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">36,888</td>
<td align="right">6.7%</td>
<td align="right">16,017</td>
<td align="right">4.3%</td>
<td align="right">-56.6%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">25,651</td>
<td align="right">4.6%</td>
<td align="right">12,472</td>
<td align="right">3.4%</td>
<td align="right">-51.4%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">63,498</td>
<td align="right">11.5%</td>
<td align="right">35,024</td>
<td align="right">9.4%</td>
<td align="right">-44.8%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">41,347</td>
<td align="right">7.5%</td>
<td align="right">25,227</td>
<td align="right">6.8%</td>
<td align="right">-39.0%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">8,368</td>
<td align="right">1.5%</td>
<td align="right">5,315</td>
<td align="right">1.4%</td>
<td align="right">-36.5%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">30,085</td>
<td align="right">5.4%</td>
<td align="right">19,487</td>
<td align="right">5.3%</td>
<td align="right">-35.2%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">15,685</td>
<td align="right">2.8%</td>
<td align="right">11,813</td>
<td align="right">3.2%</td>
<td align="right">-24.7%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">38,247</td>
<td align="right">6.9%</td>
<td align="right">31,059</td>
<td align="right">8.4%</td>
<td align="right">-18.8%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">140</td>
<td align="right">0.0%</td>
<td align="right">120</td>
<td align="right">0.0%</td>
<td align="right">-14.3%</td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">2,261</td>
<td align="right">0.4%</td>
<td align="right">2,463</td>
<td align="right">0.7%</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">13,958</td>
<td align="right">2.5%</td>
<td align="right">12,720</td>
<td align="right">3.4%</td>
<td align="right">-8.9%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">2,114</td>
<td align="right">0.4%</td>
<td align="right">1,943</td>
<td align="right">0.5%</td>
<td align="right">-8.1%</td>
</tr>
<tr>
<td align="left">subscr other slice</td>
<td align="right">311</td>
<td align="right">0.1%</td>
<td align="right">331</td>
<td align="right">0.1%</td>
<td align="right">6.4%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">109,558</td>
<td align="right">19.8%</td>
<td align="right">104,463</td>
<td align="right">28.1%</td>
<td align="right">-4.7%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">3,100</td>
<td align="right">0.6%</td>
<td align="right">2,971</td>
<td align="right">0.8%</td>
<td align="right">-4.2%</td>
</tr>
<tr>
<td align="left">subscr range</td>
<td align="right">3,162</td>
<td align="right">0.6%</td>
<td align="right">3,082</td>
<td align="right">0.8%</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">639</td>
<td align="right">0.1%</td>
<td align="right">627</td>
<td align="right">0.2%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">subscr deque</td>
<td align="right">116</td>
<td align="right">0.0%</td>
<td align="right">114</td>
<td align="right">0.0%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">1,387</td>
<td align="right">0.3%</td>
<td align="right">1,383</td>
<td align="right">0.4%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">subscr counter</td>
<td align="right">26,852</td>
<td align="right">4.9%</td>
<td align="right">26,812</td>
<td align="right">7.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">9,129</td>
<td align="right">1.7%</td>
<td align="right">9,125</td>
<td align="right">2.5%</td>
<td align="right">-0.0%</td>
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
<td align="left">subscr ordereddict</td>
<td align="right">23</td>
<td align="right">0.0%</td>
<td align="right">23</td>
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
<td align="right">201,330,140</td>
<td align="right">100.0%</td>
<td align="right">112,501,476</td>
<td align="right">100.0%</td>
<td align="right">-44.1%</td>
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
deopt
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">8,000</td>
<td align="right">0.0%</td>
<td align="right">28,235</td>
<td align="right">0.0%</td>
<td align="right">252.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">184,587,024</td>
<td align="right">1.4%</td>
<td align="right">138,471,203</td>
<td align="right">1.1%</td>
<td align="right">-25.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">181,167,084</td>
<td align="right">1.4%</td>
<td align="right">135,910,519</td>
<td align="right">1.1%</td>
<td align="right">-25.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">12,602,104,173</td>
<td align="right">98.6%</td>
<td align="right">12,507,389,511</td>
<td align="right">98.9%</td>
<td align="right">-0.8%</td>
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
<td align="right">3,642,118</td>
<td align="right">100.0%</td>
<td align="right">2,783,329</td>
<td align="right">100.0%</td>
<td align="right">-23.6%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">147</td>
<td align="right">0.0%</td>
<td align="right">147</td>
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
<td align="left">init not python</td>
<td align="right">266</td>
<td align="right">181.0%</td>
<td align="right">286</td>
<td align="right">194.6%</td>
<td align="right">7.5%</td>
</tr>
<tr>
<td align="left">init not simple</td>
<td align="right">731</td>
<td align="right">497.3%</td>
<td align="right">731</td>
<td align="right">497.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">147</td>
<td align="right">100.0%</td>
<td align="right">147</td>
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
<td align="right">537,920</td>
<td align="right">96.6%</td>
<td align="right">537,918</td>
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
<td align="right">545,009</td>
<td align="right">97.9%</td>
<td align="right">545,009</td>
<td align="right">97.9%</td>
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
<td align="right">18,763</td>
<td align="right">100.0%</td>
<td align="right">18,819</td>
<td align="right">100.0%</td>
<td align="right">0.3%</td>
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
<td align="right">150,047,603</td>
<td align="right">2.7%</td>
<td align="right">96,286,603</td>
<td align="right">1.8%</td>
<td align="right">-35.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,306,234</td>
<td align="right">0.0%</td>
<td align="right">1,145,184</td>
<td align="right">0.0%</td>
<td align="right">-12.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,316,399,133</td>
<td align="right">97.2%</td>
<td align="right">5,273,578,608</td>
<td align="right">98.2%</td>
<td align="right">-0.8%</td>
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
<td align="right">100</td>
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
<td align="right">119,742</td>
<td align="right">72.2%</td>
<td align="right">109,046</td>
<td align="right">71.6%</td>
<td align="right">-8.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">46,210</td>
<td align="right">27.8%</td>
<td align="right">43,200</td>
<td align="right">28.4%</td>
<td align="right">-6.5%</td>
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
<td align="right">1,398</td>
<td align="right">1.2%</td>
<td align="right">4,078</td>
<td align="right">3.7%</td>
<td align="right">191.7%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">14,427</td>
<td align="right">12.0%</td>
<td align="right">6,872</td>
<td align="right">6.3%</td>
<td align="right">-52.4%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">1,909</td>
<td align="right">1.6%</td>
<td align="right">1,472</td>
<td align="right">1.3%</td>
<td align="right">-22.9%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">30,229</td>
<td align="right">25.2%</td>
<td align="right">27,518</td>
<td align="right">25.2%</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">6,424</td>
<td align="right">5.4%</td>
<td align="right">5,981</td>
<td align="right">5.5%</td>
<td align="right">-6.9%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">38,944</td>
<td align="right">32.5%</td>
<td align="right">37,001</td>
<td align="right">33.9%</td>
<td align="right">-5.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">4,106</td>
<td align="right">3.4%</td>
<td align="right">4,300</td>
<td align="right">3.9%</td>
<td align="right">4.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">10,678</td>
<td align="right">8.9%</td>
<td align="right">10,197</td>
<td align="right">9.4%</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">9,729</td>
<td align="right">8.1%</td>
<td align="right">9,729</td>
<td align="right">8.9%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">911</td>
<td align="right">0.8%</td>
<td align="right">911</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">803</td>
<td align="right">0.7%</td>
<td align="right">803</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">184</td>
<td align="right">0.2%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">158,562,287</td>
<td align="right">6.7%</td>
<td align="right">65,213,336</td>
<td align="right">2.9%</td>
<td align="right">-58.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,191,461,259</td>
<td align="right">93.2%</td>
<td align="right">2,187,466,156</td>
<td align="right">97.0%</td>
<td align="right">-0.2%</td>
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
<td align="right">1,400,826</td>
<td align="right">0.1%</td>
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
<td align="left">Failure</td>
<td align="right">58,852</td>
<td align="right">67.5%</td>
<td align="right">124,530</td>
<td align="right">81.5%</td>
<td align="right">111.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">28,320</td>
<td align="right">32.5%</td>
<td align="right">28,320</td>
<td align="right">18.5%</td>
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
<td align="right">11,038</td>
<td align="right">18.8%</td>
<td align="right">93,061</td>
<td align="right">74.7%</td>
<td align="right">743.1%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">28,522</td>
<td align="right">48.5%</td>
<td align="right">12,022</td>
<td align="right">9.7%</td>
<td align="right">-57.9%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">10,042</td>
<td align="right">17.1%</td>
<td align="right">10,904</td>
<td align="right">8.8%</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">9,250</td>
<td align="right">15.7%</td>
<td align="right">8,543</td>
<td align="right">6.9%</td>
<td align="right">-7.6%</td>
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
<td align="right">61,940,608</td>
<td align="right">3.3%</td>
<td align="right">22,270,855</td>
<td align="right">2.5%</td>
<td align="right">-64.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">310,292,451</td>
<td align="right">16.7%</td>
<td align="right">119,940,321</td>
<td align="right">13.5%</td>
<td align="right">-61.3%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,489,725,847</td>
<td align="right">80.0%</td>
<td align="right">741,427,789</td>
<td align="right">83.3%</td>
<td align="right">-50.2%</td>
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
<td align="right">155,038</td>
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
<td align="right">133,764</td>
<td align="right">10.2%</td>
<td align="right">6,145,696</td>
<td align="right">91.5%</td>
<td align="right">4,494.4%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,174,335</td>
<td align="right">89.8%</td>
<td align="right">570,696</td>
<td align="right">8.5%</td>
<td align="right">-51.4%</td>
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
<td align="left">map</td>
<td align="right">251</td>
<td align="right">0.2%</td>
<td align="right">476,371</td>
<td align="right">7.8%</td>
<td align="right">189,689.2%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">1,177</td>
<td align="right">0.9%</td>
<td align="right">359,715</td>
<td align="right">5.9%</td>
<td align="right">30,462.0%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">50,957</td>
<td align="right">38.1%</td>
<td align="right">4,280,184</td>
<td align="right">69.6%</td>
<td align="right">8,299.6%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">114</td>
<td align="right">0.1%</td>
<td align="right">7,734</td>
<td align="right">0.1%</td>
<td align="right">6,684.2%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">16,337</td>
<td align="right">12.2%</td>
<td align="right">777,207</td>
<td align="right">12.6%</td>
<td align="right">4,657.3%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">3,473</td>
<td align="right">2.6%</td>
<td align="right">78,497</td>
<td align="right">1.3%</td>
<td align="right">2,160.2%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">5,271</td>
<td align="right">3.9%</td>
<td align="right">66,910</td>
<td align="right">1.1%</td>
<td align="right">1,169.4%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">16,198</td>
<td align="right">12.1%</td>
<td align="right">66,508</td>
<td align="right">1.1%</td>
<td align="right">310.6%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">320</td>
<td align="right">0.2%</td>
<td align="right">940</td>
<td align="right">0.0%</td>
<td align="right">193.8%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">232</td>
<td align="right">0.2%</td>
<td align="right">545</td>
<td align="right">0.0%</td>
<td align="right">134.9%</td>
</tr>
<tr>
<td align="left">zip</td>
<td align="right">4,162</td>
<td align="right">3.1%</td>
<td align="right">7,044</td>
<td align="right">0.1%</td>
<td align="right">69.2%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">10,918</td>
<td align="right">8.2%</td>
<td align="right">4,311</td>
<td align="right">0.1%</td>
<td align="right">-60.5%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">1,730</td>
<td align="right">1.3%</td>
<td align="right">910</td>
<td align="right">0.0%</td>
<td align="right">-47.4%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">4,459</td>
<td align="right">3.3%</td>
<td align="right">2,472</td>
<td align="right">0.0%</td>
<td align="right">-44.6%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">5,580</td>
<td align="right">4.2%</td>
<td align="right">7,784</td>
<td align="right">0.1%</td>
<td align="right">39.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">12,545</td>
<td align="right">9.4%</td>
<td align="right">8,564</td>
<td align="right">0.1%</td>
<td align="right">-31.7%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">40</td>
<td align="right">0.0%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
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
<td align="right">126,471,520</td>
<td align="right">126,471,520 / 0 !!</td>
<td align="right">123,354,241</td>
<td align="right">123,354,241 / 0 !!</td>
<td align="right">-2.5%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">311,635,633</td>
<td align="right">311,635,633 / 0 !!</td>
<td align="right">307,479,568</td>
<td align="right">307,479,568 / 0 !!</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">12,142,612</td>
<td align="right">12,142,612 / 0 !!</td>
<td align="right">12,057,367</td>
<td align="right">12,057,367 / 0 !!</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">101,610,602</td>
<td align="right">101,610,602 / 0 !!</td>
<td align="right">101,219,259</td>
<td align="right">101,219,259 / 0 !!</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">322,215,051</td>
<td align="right">322,215,051 / 0 !!</td>
<td align="right">322,025,992</td>
<td align="right">322,025,992 / 0 !!</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">5,390,782</td>
<td align="right">5,390,782 / 0 !!</td>
<td align="right">5,388,892</td>
<td align="right">5,388,892 / 0 !!</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">172,617,249</td>
<td align="right">172,617,249 / 0 !!</td>
<td align="right">172,617,641</td>
<td align="right">172,617,641 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">34,819,624</td>
<td align="right">34,819,624 / 0 !!</td>
<td align="right">34,819,578</td>
<td align="right">34,819,578 / 0 !!</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">2,768,970</td>
<td align="right">2,768,970 / 0 !!</td>
<td align="right">2,768,970</td>
<td align="right">2,768,970 / 0 !!</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">785,160,438</td>
<td align="right">5.0%</td>
<td align="right">449,684,422</td>
<td align="right">3.2%</td>
<td align="right">-42.7%</td>
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
<td align="right">1,916,869</td>
<td align="right">0.0%</td>
<td align="right">34.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">609,698,561</td>
<td align="right">3.9%</td>
<td align="right">444,822,280</td>
<td align="right">3.1%</td>
<td align="right">-27.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">14,324,062,129</td>
<td align="right">91.1%</td>
<td align="right">13,283,587,175</td>
<td align="right">93.7%</td>
<td align="right">-7.3%</td>
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
<td align="right">464,894</td>
<td align="right">3.0%</td>
<td align="right">1,466,517</td>
<td align="right">14.2%</td>
<td align="right">215.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">14,886,732</td>
<td align="right">97.0%</td>
<td align="right">8,874,668</td>
<td align="right">85.8%</td>
<td align="right">-40.4%</td>
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
<td align="right">1,869</td>
<td align="right">0.4%</td>
<td align="right">257,706</td>
<td align="right">17.6%</td>
<td align="right">13,688.4%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">22,388</td>
<td align="right">4.8%</td>
<td align="right">532,909</td>
<td align="right">36.3%</td>
<td align="right">2,280.3%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">44,329</td>
<td align="right">9.5%</td>
<td align="right">378,721</td>
<td align="right">25.8%</td>
<td align="right">754.3%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">47,830</td>
<td align="right">10.3%</td>
<td align="right">71,642</td>
<td align="right">4.9%</td>
<td align="right">49.8%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">603</td>
<td align="right">0.1%</td>
<td align="right">881</td>
<td align="right">0.1%</td>
<td align="right">46.1%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">22,236</td>
<td align="right">4.8%</td>
<td align="right">31,396</td>
<td align="right">2.1%</td>
<td align="right">41.2%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">7,722</td>
<td align="right">1.7%</td>
<td align="right">10,173</td>
<td align="right">0.7%</td>
<td align="right">31.7%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">17,076</td>
<td align="right">3.7%</td>
<td align="right">13,106</td>
<td align="right">0.9%</td>
<td align="right">-23.2%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">45,086</td>
<td align="right">9.7%</td>
<td align="right">35,656</td>
<td align="right">2.4%</td>
<td align="right">-20.9%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">823</td>
<td align="right">0.2%</td>
<td align="right">901</td>
<td align="right">0.1%</td>
<td align="right">9.5%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">718</td>
<td align="right">0.2%</td>
<td align="right">742</td>
<td align="right">0.1%</td>
<td align="right">3.3%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">2,373</td>
<td align="right">0.5%</td>
<td align="right">2,397</td>
<td align="right">0.2%</td>
<td align="right">1.0%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">4,902</td>
<td align="right">1.1%</td>
<td align="right">4,865</td>
<td align="right">0.3%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">1,139</td>
<td align="right">0.2%</td>
<td align="right">1,139</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">400</td>
<td align="right">0.1%</td>
<td align="right">400</td>
<td align="right">0.0%</td>
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
<td align="right">6,705,898,221</td>
<td align="right">99.8%</td>
<td align="right">5,664,022,889</td>
<td align="right">99.7%</td>
<td align="right">-15.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">41,995</td>
<td align="right">0.0%</td>
<td align="right">41,950</td>
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
<td align="right">14,612,771</td>
<td align="right">0.2%</td>
<td align="right">14,612,696</td>
<td align="right">0.3%</td>
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
<td align="right">11</td>
<td align="right">0.0%</td>
<td align="right">11</td>
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
<td align="right">124,812</td>
<td align="right">100.0%</td>
<td align="right">125,443</td>
<td align="right">100.0%</td>
<td align="right">0.5%</td>
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
<td align="right">123</td>
<td align="right">0.0%</td>
<td align="right">122</td>
<td align="right">0.0%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">65,622,399</td>
<td align="right">100.0%</td>
<td align="right">65,700,600</td>
<td align="right">100.0%</td>
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
<td align="right">2,225</td>
<td align="right">100.0%</td>
<td align="right">2,225</td>
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
<td align="right">128,406,370</td>
<td align="right">17.8%</td>
<td align="right">128,405,906</td>
<td align="right">17.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">593,215,676</td>
<td align="right">82.2%</td>
<td align="right">593,215,700</td>
<td align="right">82.2%</td>
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
<td align="right">55,879</td>
<td align="right">98.9%</td>
<td align="right">64.6%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">616</td>
<td align="right">1.8%</td>
<td align="right">616</td>
<td align="right">1.1%</td>
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
<td align="left">async generator send</td>
<td align="right">24,440</td>
<td align="right">72.0%</td>
<td align="right">45,960</td>
<td align="right">82.2%</td>
<td align="right">88.1%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">640</td>
<td align="right">1.9%</td>
<td align="right">680</td>
<td align="right">1.2%</td>
<td align="right">6.2%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">5,948</td>
<td align="right">17.5%</td>
<td align="right">6,295</td>
<td align="right">11.3%</td>
<td align="right">5.8%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">2,925</td>
<td align="right">8.6%</td>
<td align="right">2,944</td>
<td align="right">5.3%</td>
<td align="right">0.6%</td>
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
<td align="right">113,415,681</td>
<td align="right">4.1%</td>
<td align="right">75,559,587</td>
<td align="right">2.8%</td>
<td align="right">-33.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">59,648,910</td>
<td align="right">2.1%</td>
<td align="right">49,869,264</td>
<td align="right">1.8%</td>
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
<td align="right">2,604,403,750</td>
<td align="right">93.8%</td>
<td align="right">2,598,898,567</td>
<td align="right">95.4%</td>
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
<td align="right">11,588</td>
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
<td align="right">44,004</td>
<td align="right">2.0%</td>
<td align="right">164,663</td>
<td align="right">10.1%</td>
<td align="right">274.2%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,178,602</td>
<td align="right">98.0%</td>
<td align="right">1,470,165</td>
<td align="right">89.9%</td>
<td align="right">-32.5%</td>
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
<td align="left">class attr simple</td>
<td align="right">20,345</td>
<td align="right">46.2%</td>
<td align="right">142,506</td>
<td align="right">86.5%</td>
<td align="right">600.4%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">236,193</td>
<td align="right">536.8%</td>
<td align="right">115,224</td>
<td align="right">70.0%</td>
<td align="right">-51.2%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">3,719</td>
<td align="right">8.5%</td>
<td align="right">2,099</td>
<td align="right">1.3%</td>
<td align="right">-43.6%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">1,729</td>
<td align="right">3.9%</td>
<td align="right">2,095</td>
<td align="right">1.3%</td>
<td align="right">21.2%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">749</td>
<td align="right">1.7%</td>
<td align="right">849</td>
<td align="right">0.5%</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">421</td>
<td align="right">1.0%</td>
<td align="right">377</td>
<td align="right">0.2%</td>
<td align="right">-10.5%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">4,889</td>
<td align="right">11.1%</td>
<td align="right">4,707</td>
<td align="right">2.9%</td>
<td align="right">-3.7%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">7,206</td>
<td align="right">16.4%</td>
<td align="right">7,086</td>
<td align="right">4.3%</td>
<td align="right">-1.7%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">3,002</td>
<td align="right">6.8%</td>
<td align="right">3,004</td>
<td align="right">1.8%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">313</td>
<td align="right">0.7%</td>
<td align="right">313</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">no dict</td>
<td align="right">101</td>
<td align="right">0.2%</td>
<td align="right">101</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">94</td>
<td align="right">0.2%</td>
<td align="right">94</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">89</td>
<td align="right">0.2%</td>
<td align="right">89</td>
<td align="right">0.1%</td>
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
<td align="right">1,232,574</td>
<td align="right">100.0%</td>
<td align="right">536,570</td>
<td align="right">100.0%</td>
<td align="right">-56.5%</td>
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
<td align="right">122,021,899</td>
<td align="right">11.4%</td>
<td align="right">114,694,231</td>
<td align="right">10.8%</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">949,074,169</td>
<td align="right">88.6%</td>
<td align="right">946,981,129</td>
<td align="right">89.2%</td>
<td align="right">-0.2%</td>
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
<td align="right">40,810</td>
<td align="right">93.2%</td>
<td align="right">42,072</td>
<td align="right">93.4%</td>
<td align="right">3.1%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,955</td>
<td align="right">6.8%</td>
<td align="right">2,959</td>
<td align="right">6.6%</td>
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
<td align="left">dict subclass no override</td>
<td align="right">3,923</td>
<td align="right">9.6%</td>
<td align="right">15,634</td>
<td align="right">37.2%</td>
<td align="right">298.5%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">1,673</td>
<td align="right">4.1%</td>
<td align="right">453</td>
<td align="right">1.1%</td>
<td align="right">-72.9%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">14,377</td>
<td align="right">35.2%</td>
<td align="right">8,401</td>
<td align="right">20.0%</td>
<td align="right">-41.6%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">2,976</td>
<td align="right">7.3%</td>
<td align="right">2,316</td>
<td align="right">5.5%</td>
<td align="right">-22.2%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">136</td>
<td align="right">0.3%</td>
<td align="right">160</td>
<td align="right">0.4%</td>
<td align="right">17.6%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">17,329</td>
<td align="right">42.5%</td>
<td align="right">14,752</td>
<td align="right">35.1%</td>
<td align="right">-14.9%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">328</td>
<td align="right">0.8%</td>
<td align="right">288</td>
<td align="right">0.7%</td>
<td align="right">-12.2%</td>
</tr>
<tr>
<td align="left">array slice</td>
<td align="right">68</td>
<td align="right">0.2%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">331,282,019</td>
<td align="right">5.8%</td>
<td align="right">255,577,688</td>
<td align="right">4.9%</td>
<td align="right">-22.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">66,399,248</td>
<td align="right">1.2%</td>
<td align="right">57,104,656</td>
<td align="right">1.1%</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">5,299,316,573</td>
<td align="right">93.0%</td>
<td align="right">4,899,203,415</td>
<td align="right">94.0%</td>
<td align="right">-7.6%</td>
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
<td align="right">5,046</td>
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
<td align="right">574,972</td>
<td align="right">30.7%</td>
<td align="right">484,910</td>
<td align="right">30.1%</td>
<td align="right">-15.7%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,300,771</td>
<td align="right">69.3%</td>
<td align="right">1,128,727</td>
<td align="right">69.9%</td>
<td align="right">-13.2%</td>
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
<td align="right">76,279</td>
<td align="right">13.3%</td>
<td align="right">151,027</td>
<td align="right">31.1%</td>
<td align="right">98.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">84,205</td>
<td align="right">14.6%</td>
<td align="right">4,741</td>
<td align="right">1.0%</td>
<td align="right">-94.4%</td>
</tr>
<tr>
<td align="left">float</td>
<td align="right">382</td>
<td align="right">0.1%</td>
<td align="right">22</td>
<td align="right">0.0%</td>
<td align="right">-94.2%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">71,858</td>
<td align="right">12.5%</td>
<td align="right">6,823</td>
<td align="right">1.4%</td>
<td align="right">-90.5%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">2,621</td>
<td align="right">0.5%</td>
<td align="right">1,321</td>
<td align="right">0.3%</td>
<td align="right">-49.6%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">9,524</td>
<td align="right">1.7%</td>
<td align="right">5,457</td>
<td align="right">1.1%</td>
<td align="right">-42.7%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">11,535</td>
<td align="right">2.0%</td>
<td align="right">7,655</td>
<td align="right">1.6%</td>
<td align="right">-33.6%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">9,503</td>
<td align="right">1.7%</td>
<td align="right">8,447</td>
<td align="right">1.7%</td>
<td align="right">-11.1%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">308,978</td>
<td align="right">53.7%</td>
<td align="right">299,330</td>
<td align="right">61.7%</td>
<td align="right">-3.1%</td>
</tr>
<tr>
<td align="left">memory view</td>
<td align="right">87</td>
<td align="right">0.0%</td>
<td align="right">87</td>
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
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">3,700</td>
<td align="right">0.0%</td>
<td align="right">3,220</td>
<td align="right">0.0%</td>
<td align="right">-13.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,204,507</td>
<td align="right">0.1%</td>
<td align="right">1,190,122</td>
<td align="right">0.1%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">1,271,149,489</td>
<td align="right">99.9%</td>
<td align="right">1,256,246,458</td>
<td align="right">99.9%</td>
<td align="right">-1.2%</td>
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
<td align="right">20</td>
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
<td align="right">754</td>
<td align="right">7.2%</td>
<td align="right">2,276</td>
<td align="right">18.8%</td>
<td align="right">201.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">9,787</td>
<td align="right">92.8%</td>
<td align="right">9,839</td>
<td align="right">81.2%</td>
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
<td align="right">523</td>
<td align="right">69.4%</td>
<td align="right">2,024</td>
<td align="right">88.9%</td>
<td align="right">287.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">99</td>
<td align="right">13.1%</td>
<td align="right">120</td>
<td align="right">5.3%</td>
<td align="right">21.2%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">132</td>
<td align="right">17.5%</td>
<td align="right">132</td>
<td align="right">5.8%</td>
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
<td align="right">4,021,010,604</td>
<td align="right">3.0%</td>
<td align="right">2,392,679,775</td>
<td align="right">2.8%</td>
<td align="right">-40.5%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">52,003,144,564</td>
<td align="right">38.7%</td>
<td align="right">31,958,224,600</td>
<td align="right">37.8%</td>
<td align="right">-38.5%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,276,024,569</td>
<td align="right">1.0%</td>
<td align="right">787,588,436</td>
<td align="right">0.9%</td>
<td align="right">-38.3%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">76,956,073,743</td>
<td align="right">57.3%</td>
<td align="right">49,461,317,571</td>
<td align="right">58.5%</td>
<td align="right">-35.7%</td>
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
<td align="right">310,292,451</td>
<td align="right">8.6%</td>
<td align="right">119,940,321</td>
<td align="right">5.6%</td>
<td align="right">-61.3%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">158,562,287</td>
<td align="right">4.4%</td>
<td align="right">65,213,336</td>
<td align="right">3.1%</td>
<td align="right">-58.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">1,350,902,181</td>
<td align="right">37.3%</td>
<td align="right">590,268,681</td>
<td align="right">27.7%</td>
<td align="right">-56.3%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">201,330,140</td>
<td align="right">5.6%</td>
<td align="right">112,501,476</td>
<td align="right">5.3%</td>
<td align="right">-44.1%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">150,047,603</td>
<td align="right">4.1%</td>
<td align="right">96,286,603</td>
<td align="right">4.5%</td>
<td align="right">-35.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">609,698,561</td>
<td align="right">16.8%</td>
<td align="right">444,822,280</td>
<td align="right">20.9%</td>
<td align="right">-27.0%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">181,167,084</td>
<td align="right">5.0%</td>
<td align="right">135,910,519</td>
<td align="right">6.4%</td>
<td align="right">-25.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">331,282,019</td>
<td align="right">9.1%</td>
<td align="right">255,577,688</td>
<td align="right">12.0%</td>
<td align="right">-22.9%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">122,021,899</td>
<td align="right">3.4%</td>
<td align="right">114,694,231</td>
<td align="right">5.4%</td>
<td align="right">-6.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,406,370</td>
<td align="right">3.5%</td>
<td align="right">128,405,906</td>
<td align="right">6.0%</td>
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
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">248,651,325</td>
<td align="right">19.5%</td>
<td align="right">112,558,208</td>
<td align="right">14.3%</td>
<td align="right">-54.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">326,268,903</td>
<td align="right">25.6%</td>
<td align="right">154,241,943</td>
<td align="right">19.6%</td>
<td align="right">-52.7%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">93,618,063</td>
<td align="right">7.3%</td>
<td align="right">55,778,341</td>
<td align="right">7.1%</td>
<td align="right">-40.4%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">78,478,484</td>
<td align="right">6.1%</td>
<td align="right">51,222,113</td>
<td align="right">6.5%</td>
<td align="right">-34.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">75,511,773</td>
<td align="right">5.9%</td>
<td align="right">57,117,623</td>
<td align="right">7.3%</td>
<td align="right">-24.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">32,153,232</td>
<td align="right">2.5%</td>
<td align="right">27,856,715</td>
<td align="right">3.5%</td>
<td align="right">-13.4%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">27,564,198</td>
<td align="right">2.2%</td>
<td align="right">24,829,416</td>
<td align="right">3.2%</td>
<td align="right">-9.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">80,512,670</td>
<td align="right">6.3%</td>
<td align="right">76,873,079</td>
<td align="right">9.8%</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">30,927,048</td>
<td align="right">2.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">30,886,784</td>
<td align="right">2.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">24,856,661</td>
<td align="right">3.2%</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">20,872,311</td>
<td align="right">2.6%</td>
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
<td align="right">4,273,296</td>
<td align="right">0.1%</td>
<td align="right">2,128,101</td>
<td align="right">0.0%</td>
<td align="right">-50.2%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">6,026,301,017</td>
<td align="right">76.1%</td>
<td align="right">5,856,274,330</td>
<td align="right">75.7%</td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">78,008,210</td>
<td align="right">1.0%</td>
<td align="right">76,010,239</td>
<td align="right">1.0%</td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">6,692,207,235</td>
<td align="right">84.5%</td>
<td align="right">6,550,702,198</td>
<td align="right">84.7%</td>
<td align="right">-2.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">613,945,675</td>
<td align="right">7.8%</td>
<td align="right">605,363,872</td>
<td align="right">7.8%</td>
<td align="right">-1.4%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">1,894,752,309</td>
<td align="right">23.9%</td>
<td align="right">1,882,119,547</td>
<td align="right">24.3%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">1,894,752,309</td>
<td align="right">23.9%</td>
<td align="right">1,882,119,547</td>
<td align="right">24.3%</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,280,806,634</td>
<td align="right">16.2%</td>
<td align="right">1,276,755,675</td>
<td align="right">16.5%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">141,112,765</td>
<td align="right">1.8%</td>
<td align="right">140,848,809</td>
<td align="right">1.8%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,276,529,963</td>
<td align="right">16.1%</td>
<td align="right">1,274,624,199</td>
<td align="right">16.5%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">458,249,144</td>
<td align="right">5.8%</td>
<td align="right">458,102,237</td>
<td align="right">5.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">24,440,081</td>
<td align="right">0.3%</td>
<td align="right">24,439,936</td>
<td align="right">0.3%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">305,854,978</td>
<td align="right">3.9%</td>
<td align="right">305,855,232</td>
<td align="right">4.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">3,375</td>
<td align="right">0.0%</td>
<td align="right">3,375</td>
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
<td align="right">30,317,041,348</td>
<td align="right">31.1%</td>
<td align="right">20,701,354,578</td>
<td align="right">21.6%</td>
<td align="right">-31.7%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">1,475,667,049</td>
<td align="right">1.3%</td>
<td align="right">1,110,625,352</td>
<td align="right">1.0%</td>
<td align="right">-24.7%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">38,023,337,790</td>
<td align="right">39.0%</td>
<td align="right">46,607,647,751</td>
<td align="right">48.6%</td>
<td align="right">22.6%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">39,307,329,349</td>
<td align="right">35.1%</td>
<td align="right">32,510,718,693</td>
<td align="right">29.4%</td>
<td align="right">-17.3%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">4,016,319,397</td>
<td align="right">4.1%</td>
<td align="right">3,332,919,203</td>
<td align="right">3.5%</td>
<td align="right">-17.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">4,056,483</td>
<td align="right">2.1%</td>
<td align="right">3,390,883</td>
<td align="right">1.8%</td>
<td align="right">-16.4%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">2,298,628,490</td>
<td align="right"></td>
<td align="right">1,967,050,862</td>
<td align="right"></td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">47,357,372,215</td>
<td align="right">42.2%</td>
<td align="right">52,917,358,939</td>
<td align="right">47.9%</td>
<td align="right">11.7%</td>
</tr>
<tr>
<td align="left">Method cache dunder misses</td>
<td align="right">6,458,103</td>
<td align="right"></td>
<td align="right">6,041,825</td>
<td align="right"></td>
<td align="right">-6.4%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">63,315,296</td>
<td align="right"></td>
<td align="right">61,655,433</td>
<td align="right"></td>
<td align="right">-2.6%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">57,660,148</td>
<td align="right"></td>
<td align="right">56,357,478</td>
<td align="right"></td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">13,845,636,634</td>
<td align="right"></td>
<td align="right">13,662,042,611</td>
<td align="right"></td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">13,845,444,683</td>
<td align="right">70.3%</td>
<td align="right">13,661,870,792</td>
<td align="right">70.1%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">6,452,380,773</td>
<td align="right"></td>
<td align="right">6,419,792,994</td>
<td align="right"></td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">5,782,280,351</td>
<td align="right">29.3%</td>
<td align="right">5,753,595,423</td>
<td align="right">29.5%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">5,860,449,587</td>
<td align="right">29.7%</td>
<td align="right">5,831,786,286</td>
<td align="right">29.9%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">25,225,776,468</td>
<td align="right">25.9%</td>
<td align="right">25,325,935,713</td>
<td align="right">26.4%</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">2,889,784,703</td>
<td align="right"></td>
<td align="right">2,879,924,712</td>
<td align="right"></td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">190,517,887</td>
<td align="right"></td>
<td align="right">189,906,212</td>
<td align="right"></td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">6,775,535</td>
<td align="right">0.0%</td>
<td align="right">6,795,896</td>
<td align="right">0.0%</td>
<td align="right">0.3%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">23,952,221,008</td>
<td align="right">21.4%</td>
<td align="right">23,899,437,847</td>
<td align="right">21.6%</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">71,393,701</td>
<td align="right">0.4%</td>
<td align="right">71,394,967</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
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
<td align="right">358,135</td>
<td align="right">98,775,759</td>
<td align="right">9,547,681,454</td>
<td align="right">776,633,094</td>
<td align="right">748,282,223</td>
<td align="right">357,602</td>
<td align="right">98,434,958</td>
<td align="right">9,555,504,368</td>
<td align="right">774,977,970</td>
<td align="right">748,057,738</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">15,998</td>
<td align="right">8,734,250</td>
<td align="right">11,440,449,438</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">15,998</td>
<td align="right">8,734,250</td>
<td align="right">11,441,292,854</td>
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
<td align="right">502,424</td>
<td align="right"></td>
<td align="right">23,737,517</td>
<td align="right"></td>
<td align="right">4,624.6%</td>
</tr>
<tr>
<td align="left">
Trace too long
<details>
<summary>ⓘ</summary>

A trace is truncated because it is longer than the instruction buffer.
</details>
</td>
<td align="right">60</td>
<td align="right">0.0%</td>
<td align="right">2,483</td>
<td align="right">0.0%</td>
<td align="right">4,038.3%</td>
</tr>
<tr>
<td align="left">
Executors invalidated
<details>
<summary>ⓘ</summary>

The number of executors that were invalidated due to watched dictionary changes.
</details>
</td>
<td align="right">240</td>
<td align="right">1.0%</td>
<td align="right">792</td>
<td align="right">1.2%</td>
<td align="right">230.0%</td>
</tr>
<tr>
<td align="left">
Traces created
<details>
<summary>ⓘ</summary>

The number of traces that were successfully created.
</details>
</td>
<td align="right">23,094</td>
<td align="right">4.6%</td>
<td align="right">65,898</td>
<td align="right">0.3%</td>
<td align="right">185.3%</td>
</tr>
<tr>
<td align="left">
Trace stack overflow
<details>
<summary>ⓘ</summary>

A trace is truncated because it would require more than 5 stack frames.
</details>
</td>
<td align="right">62</td>
<td align="right">0.0%</td>
<td align="right">0</td>
<td align="right">0.0%</td>
<td align="right">-100.0%</td>
</tr>
<tr>
<td align="left">
Trace stack underflow
<details>
<summary>ⓘ</summary>

A potential trace is abandoned because it pops more frames than it pushes.
</details>
</td>
<td align="right">217,659</td>
<td align="right">43.3%</td>
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
<td align="right">47,581</td>
<td align="right">9.5%</td>
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
<td align="right">691</td>
<td align="right">0.1%</td>
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
<td align="right">747</td>
<td align="right">0.1%</td>
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
<td align="right">624</td>
<td align="right">0.1%</td>
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
<td align="right">214,028</td>
<td align="right">42.6%</td>
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
<td align="right">231,338,889,893</td>
<td align="right">5,313.7%</td>
<td align="right">357,653,292,997</td>
<td align="right">6,103.1%</td>
<td align="right">54.6%</td>
</tr>
<tr>
<td align="left">
Traces executed
<details>
<summary>ⓘ</summary>

The number of traces that were executed
</details>
</td>
<td align="right">4,353,639,518</td>
<td align="right"></td>
<td align="right">5,860,227,033</td>
<td align="right"></td>
<td align="right">34.6%</td>
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
<td align="right">19,794</td>
<td align="right">85.7%</td>
<td align="right">65,151</td>
<td align="right">98.9%</td>
<td align="right">229.1%</td>
</tr>
<tr>
<td align="left">
Optimizer attempts
<details>
<summary>ⓘ</summary>

The number of times the trace optimizer (_Py_uop_analyze_and_optimize) was run.
</details>
</td>
<td align="right">23,094</td>
<td align="right"></td>
<td align="right">65,898</td>
<td align="right"></td>
<td align="right">185.3%</td>
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
<td align="right">806,912</td>
<td align="right">0.5%</td>
<td align="right">108,191,744</td>
<td align="right">9.7%</td>
<td align="right">13,308.1%</td>
</tr>
<tr>
<td align="left">
Code size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the code of the JIT traces
</details>
</td>
<td align="right">133,423,257</td>
<td align="right">75.2%</td>
<td align="right">961,177,328</td>
<td align="right">86.2%</td>
<td align="right">620.4%</td>
</tr>
<tr>
<td align="left">
Total memory size
<details>
<summary>ⓘ</summary>

The total size of the memory allocated for the JIT traces
</details>
</td>
<td align="right">177,336,320</td>
<td align="right"></td>
<td align="right">1,114,521,600</td>
<td align="right"></td>
<td align="right">528.5%</td>
</tr>
<tr>
<td align="left">
Data size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the data of the JIT traces
</details>
</td>
<td align="right">3,220,456</td>
<td align="right">1.8%</td>
<td align="right">17,581,536</td>
<td align="right">1.6%</td>
<td align="right">445.9%</td>
</tr>
<tr>
<td align="left">
Padding size
<details>
<summary>ⓘ</summary>

The size of the memory allocated for the padding of the JIT traces
</details>
</td>
<td align="right">40,672,733</td>
<td align="right">22.9%</td>
<td align="right">135,697,543</td>
<td align="right">12.2%</td>
<td align="right">233.6%</td>
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
<td align="left">8,217</td>
<td align="right">41.3%</td>
<td align="left">15,815</td>
<td align="right">24.3%</td>
<td align="right">92.5%</td>
</tr>
<tr>
<td align="left"><= 8,192</td>
<td align="left">6,953</td>
<td align="right">35.0%</td>
<td align="left">17,047</td>
<td align="right">26.1%</td>
<td align="right">145.2%</td>
</tr>
<tr>
<td align="left"><= 16,384</td>
<td align="left">3,028</td>
<td align="right">15.2%</td>
<td align="left">15,578</td>
<td align="right">23.9%</td>
<td align="right">414.5%</td>
</tr>
<tr>
<td align="left"><= 32,768</td>
<td align="left">1,376</td>
<td align="right">6.9%</td>
<td align="left">9,791</td>
<td align="right">15.0%</td>
<td align="right">611.6%</td>
</tr>
<tr>
<td align="left"><= 65,536</td>
<td align="left">300</td>
<td align="right">1.5%</td>
<td align="left">3,892</td>
<td align="right">6.0%</td>
<td align="right">1,197.3%</td>
</tr>
<tr>
<td align="left"><= 131,072</td>
<td align="left"></td>
<td align="right"></td>
<td align="left">3,070</td>
<td align="right">4.7%</td>
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
<td align="right">1,056</td>
<td align="right">4.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">837</td>
<td align="right">3.6%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">3,566</td>
<td align="right">15.4%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">7,673</td>
<td align="right">33.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">4,421</td>
<td align="right">19.1%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">4,212</td>
<td align="right">18.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">1,201</td>
<td align="right">5.2%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right">128</td>
<td align="right">0.6%</td>
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
<td align="right">676</td>
<td align="right">2.9%</td>
<td align="right"></td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left"><= 8</td>
<td align="right">527</td>
<td align="right">2.3%</td>
<td align="right">803</td>
<td align="right">1.2%</td>
<td align="right">52.4%</td>
</tr>
<tr>
<td align="left"><= 16</td>
<td align="right">2,002</td>
<td align="right">8.7%</td>
<td align="right">6,055</td>
<td align="right">9.2%</td>
<td align="right">202.4%</td>
</tr>
<tr>
<td align="left"><= 32</td>
<td align="right">7,070</td>
<td align="right">30.6%</td>
<td align="right">13,573</td>
<td align="right">20.6%</td>
<td align="right">92.0%</td>
</tr>
<tr>
<td align="left"><= 64</td>
<td align="right">6,045</td>
<td align="right">26.2%</td>
<td align="right">17,172</td>
<td align="right">26.1%</td>
<td align="right">184.1%</td>
</tr>
<tr>
<td align="left"><= 128</td>
<td align="right">1,858</td>
<td align="right">8.0%</td>
<td align="right">13,162</td>
<td align="right">20.0%</td>
<td align="right">608.4%</td>
</tr>
<tr>
<td align="left"><= 256</td>
<td align="right">1,385</td>
<td align="right">6.0%</td>
<td align="right">9,164</td>
<td align="right">13.9%</td>
<td align="right">561.7%</td>
</tr>
<tr>
<td align="left"><= 512</td>
<td align="right">231</td>
<td align="right">1.0%</td>
<td align="right">2,792</td>
<td align="right">4.2%</td>
<td align="right">1,108.7%</td>
</tr>
<tr>
<td align="left"><= 1,024</td>
<td align="right"></td>
<td align="right"></td>
<td align="right">2,430</td>
<td align="right">3.7%</td>
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
<td align="left">_LOAD_SUPER_ATTR_METHOD</td>
<td align="right">3,001</td>
<td align="right">9,609,829</td>
<td align="right">320,120.9%</td>
</tr>
<tr>
<td align="left">_DELETE_SUBSCR</td>
<td align="right">54,160</td>
<td align="right">105,830,662</td>
<td align="right">195,303.7%</td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_1</td>
<td align="right">269,900</td>
<td align="right">200,725,670</td>
<td align="right">74,270.4%</td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_0</td>
<td align="right">352,940</td>
<td align="right">161,152,392</td>
<td align="right">45,560.0%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_ISINSTANCE</td>
<td align="right">449,298</td>
<td align="right">198,237,765</td>
<td align="right">44,021.7%</td>
</tr>
<tr>
<td align="left">_GUARD_THIRD_NULL</td>
<td align="right">449,298</td>
<td align="right">198,237,765</td>
<td align="right">44,021.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NULL</td>
<td align="right">270,020</td>
<td align="right">99,978,366</td>
<td align="right">36,926.3%</td>
</tr>
<tr>
<td align="left">_ERROR_POP_N</td>
<td align="right">263</td>
<td align="right">84,312</td>
<td align="right">31,957.8%</td>
</tr>
<tr>
<td align="left">_MAKE_CELL</td>
<td align="right">160,148</td>
<td align="right">39,478,649</td>
<td align="right">24,551.4%</td>
</tr>
<tr>
<td align="left">_UNARY_NOT</td>
<td align="right">212,260</td>
<td align="right">49,064,036</td>
<td align="right">23,015.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_MODULE</td>
<td align="right">471,948</td>
<td align="right">65,121,508</td>
<td align="right">13,698.4%</td>
</tr>
<tr>
<td align="left">_UNARY_NEGATIVE</td>
<td align="right">954,726</td>
<td align="right">97,783,623</td>
<td align="right">10,142.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">363,240</td>
<td align="right">35,175,412</td>
<td align="right">9,583.8%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LEN</td>
<td align="right">1,120,240</td>
<td align="right">84,198,632</td>
<td align="right">7,416.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_2</td>
<td align="right">5,364,242</td>
<td align="right">304,253,079</td>
<td align="right">5,571.9%</td>
</tr>
<tr>
<td align="left">_UNARY_INVERT</td>
<td align="right">162,754</td>
<td align="right">7,995,640</td>
<td align="right">4,812.7%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE_BORROW</td>
<td align="right">2,477,339</td>
<td align="right">98,056,981</td>
<td align="right">3,858.2%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL_CONDITIONAL</td>
<td align="right">56,140,150</td>
<td align="right">2,172,796,549</td>
<td align="right">3,770.3%</td>
</tr>
<tr>
<td align="left">_CALL_TUPLE_1</td>
<td align="right">26,932</td>
<td align="right">952,962</td>
<td align="right">3,438.4%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST</td>
<td align="right">23,245,502</td>
<td align="right">709,913,176</td>
<td align="right">2,954.0%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_MODULE</td>
<td align="right">21,901,050</td>
<td align="right">646,347,889</td>
<td align="right">2,851.2%</td>
</tr>
<tr>
<td align="left">_IMPORT_NAME</td>
<td align="right">27,762</td>
<td align="right">810,727</td>
<td align="right">2,820.3%</td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL_BUILTINS</td>
<td align="right">23,670,736</td>
<td align="right">542,864,106</td>
<td align="right">2,193.4%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_NO_DICT</td>
<td align="right">28,058,252</td>
<td align="right">590,297,736</td>
<td align="right">2,003.8%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">28,058,252</td>
<td align="right">590,297,736</td>
<td align="right">2,003.8%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION_AND_LOCK</td>
<td align="right">29,685,612</td>
<td align="right">591,179,647</td>
<td align="right">1,891.5%</td>
</tr>
<tr>
<td align="left">_CHECK_PEP_523</td>
<td align="right">46,427,104</td>
<td align="right">674,010,658</td>
<td align="right">1,351.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">23,189,260</td>
<td align="right">286,042,765</td>
<td align="right">1,133.5%</td>
</tr>
<tr>
<td align="left">_STORE_DEREF</td>
<td align="right">2,832,759</td>
<td align="right">25,569,014</td>
<td align="right">802.6%</td>
</tr>
<tr>
<td align="left">_BUILD_MAP</td>
<td align="right">8,083,351</td>
<td align="right">53,175,110</td>
<td align="right">557.8%</td>
</tr>
<tr>
<td align="left">_COPY_1</td>
<td align="right">56,150,589</td>
<td align="right">355,712,787</td>
<td align="right">533.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_4</td>
<td align="right">2,516,595</td>
<td align="right">14,450,260</td>
<td align="right">474.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_CLASS</td>
<td align="right">3,106,080</td>
<td align="right">16,925,755</td>
<td align="right">444.9%</td>
</tr>
<tr>
<td align="left">_HANDLE_PENDING_AND_DEOPT</td>
<td align="right">9,558</td>
<td align="right">50,321</td>
<td align="right">426.5%</td>
</tr>
<tr>
<td align="left">_PY_FRAME_KW</td>
<td align="right">12,237,291</td>
<td align="right">63,672,515</td>
<td align="right">420.3%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_KW</td>
<td align="right">12,237,291</td>
<td align="right">62,908,483</td>
<td align="right">414.1%</td>
</tr>
<tr>
<td align="left">_DICT_MERGE</td>
<td align="right">5,874,331</td>
<td align="right">29,788,485</td>
<td align="right">407.1%</td>
</tr>
<tr>
<td align="left">_RETURN_VALUE</td>
<td align="right">508,018,769</td>
<td align="right">2,361,015,311</td>
<td align="right">364.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS</td>
<td align="right">6,137,792</td>
<td align="right">27,690,667</td>
<td align="right">351.2%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NOT_NONE_POP</td>
<td align="right">51,810,074</td>
<td align="right">233,318,535</td>
<td align="right">350.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_EXTEND</td>
<td align="right">52,684,186</td>
<td align="right">217,800,570</td>
<td align="right">313.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_2</td>
<td align="right">21,198,257</td>
<td align="right">87,514,810</td>
<td align="right">312.8%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_EXACT_ARGS</td>
<td align="right">161,036,965</td>
<td align="right">661,807,314</td>
<td align="right">311.0%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_UNICODE</td>
<td align="right">42,172,928</td>
<td align="right">172,256,720</td>
<td align="right">308.5%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION</td>
<td align="right">214,341,097</td>
<td align="right">848,068,495</td>
<td align="right">295.7%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE</td>
<td align="right">111,036,562</td>
<td align="right">437,935,697</td>
<td align="right">294.4%</td>
</tr>
<tr>
<td align="left">_GUARD_BINARY_OP_EXTEND</td>
<td align="right">62,224,186</td>
<td align="right">243,765,430</td>
<td align="right">291.8%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_2</td>
<td align="right">237,237,070</td>
<td align="right">914,921,728</td>
<td align="right">285.7%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_0</td>
<td align="right">136,472,122</td>
<td align="right">517,941,208</td>
<td align="right">279.5%</td>
</tr>
<tr>
<td align="left">_PY_FRAME_GENERAL</td>
<td align="right">45,533,672</td>
<td align="right">172,356,097</td>
<td align="right">278.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">82,564,084</td>
<td align="right">296,333,053</td>
<td align="right">258.9%</td>
</tr>
<tr>
<td align="left">_CHECK_MANAGED_OBJECT_HAS_VALUES</td>
<td align="right">920,228,618</td>
<td align="right">3,268,596,475</td>
<td align="right">255.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">920,186,178</td>
<td align="right">3,267,586,434</td>
<td align="right">255.1%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR</td>
<td align="right">5,031,398</td>
<td align="right">16,646,446</td>
<td align="right">230.9%</td>
</tr>
<tr>
<td align="left">_STORE_ATTR_SLOT</td>
<td align="right">59,184,903</td>
<td align="right">193,127,852</td>
<td align="right">226.3%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_1</td>
<td align="right">217,944,466</td>
<td align="right">683,529,715</td>
<td align="right">213.6%</td>
</tr>
<tr>
<td align="left">_DEOPT</td>
<td align="right">9,888,545</td>
<td align="right">30,767,528</td>
<td align="right">211.1%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_3</td>
<td align="right">45,498,686</td>
<td align="right">138,630,661</td>
<td align="right">204.7%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_CLASS</td>
<td align="right">40,807,623</td>
<td align="right">121,942,476</td>
<td align="right">198.8%</td>
</tr>
<tr>
<td align="left">_POP_TOP_NOP</td>
<td align="right">118,787,328</td>
<td align="right">354,235,442</td>
<td align="right">198.2%</td>
</tr>
<tr>
<td align="left">_PUSH_FRAME</td>
<td align="right">967,633,844</td>
<td align="right">2,870,820,873</td>
<td align="right">196.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_0</td>
<td align="right">26,136,903</td>
<td align="right">73,768,112</td>
<td align="right">182.2%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_NONE_POP</td>
<td align="right">64,250,116</td>
<td align="right">178,654,228</td>
<td align="right">178.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_UNICODE</td>
<td align="right">10,088,679</td>
<td align="right">27,465,965</td>
<td align="right">172.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_3</td>
<td align="right">337,618,028</td>
<td align="right">869,014,414</td>
<td align="right">157.4%</td>
</tr>
<tr>
<td align="left">_RETURN_GENERATOR</td>
<td align="right">47,734,124</td>
<td align="right">120,379,615</td>
<td align="right">152.2%</td>
</tr>
<tr>
<td align="left">_SAVE_RETURN_OFFSET</td>
<td align="right">967,633,844</td>
<td align="right">2,415,100,553</td>
<td align="right">149.6%</td>
</tr>
<tr>
<td align="left">_CHECK_RECURSION_REMAINING</td>
<td align="right">967,633,844</td>
<td align="right">2,408,043,088</td>
<td align="right">148.9%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">77,195,346</td>
<td align="right">189,455,714</td>
<td align="right">145.4%</td>
</tr>
<tr>
<td align="left">_TIER2_RESUME_CHECK</td>
<td align="right">2,397,350,366</td>
<td align="right">5,812,038,919</td>
<td align="right">142.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_TUPLE</td>
<td align="right">345,585,404</td>
<td align="right">825,761,306</td>
<td align="right">138.9%</td>
</tr>
<tr>
<td align="left">_CALL_ISINSTANCE</td>
<td align="right">174,382,167</td>
<td align="right">413,912,562</td>
<td align="right">137.4%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP</td>
<td align="right">69,073,190</td>
<td align="right">161,111,434</td>
<td align="right">133.2%</td>
</tr>
<tr>
<td align="left">_CHECK_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">52,932,020</td>
<td align="right">122,548,978</td>
<td align="right">131.5%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">52,932,020</td>
<td align="right">122,468,198</td>
<td align="right">131.4%</td>
</tr>
<tr>
<td align="left">_GUARD_KEYS_VERSION</td>
<td align="right">750,269,059</td>
<td align="right">1,735,445,879</td>
<td align="right">131.3%</td>
</tr>
<tr>
<td align="left">_GUARD_DORV_VALUES_INST_ATTR_FROM_DICT</td>
<td align="right">750,411,719</td>
<td align="right">1,735,724,289</td>
<td align="right">131.3%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">263,468,762</td>
<td align="right">600,157,637</td>
<td align="right">127.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_1</td>
<td align="right">90,677,910</td>
<td align="right">202,584,646</td>
<td align="right">123.4%</td>
</tr>
<tr>
<td align="left">_POP_TOP</td>
<td align="right">611,995,695</td>
<td align="right">1,349,736,153</td>
<td align="right">120.5%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_0</td>
<td align="right">3,265,355,771</td>
<td align="right">7,195,157,570</td>
<td align="right">120.3%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_BOOL</td>
<td align="right">900,383,073</td>
<td align="right">1,968,795,000</td>
<td align="right">118.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_TUPLE</td>
<td align="right">35,941,400</td>
<td align="right">77,346,357</td>
<td align="right">115.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_FLOAT</td>
<td align="right">298,345,881</td>
<td align="right">634,430,461</td>
<td align="right">112.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">42,078,620</td>
<td align="right">87,763,222</td>
<td align="right">108.6%</td>
</tr>
<tr>
<td align="left">_CHECK_FUNCTION_VERSION_INLINE</td>
<td align="right">775,349,732</td>
<td align="right">1,598,798,620</td>
<td align="right">106.2%</td>
</tr>
<tr>
<td align="left">_GUARD_TYPE_VERSION</td>
<td align="right">2,665,130,643</td>
<td align="right">5,389,984,624</td>
<td align="right">102.2%</td>
</tr>
<tr>
<td align="left">_CHECK_STACK_SPACE_OPERAND</td>
<td align="right">450,761,535</td>
<td align="right">897,438,104</td>
<td align="right">99.1%</td>
</tr>
<tr>
<td align="left">_EXPAND_METHOD</td>
<td align="right">5,976,000</td>
<td align="right">11,812,160</td>
<td align="right">97.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_INT</td>
<td align="right">94,628,877</td>
<td align="right">179,073,252</td>
<td align="right">89.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_2</td>
<td align="right">1,748,420,871</td>
<td align="right">3,302,180,425</td>
<td align="right">88.9%</td>
</tr>
<tr>
<td align="left">_CHECK_METHOD_VERSION</td>
<td align="right">5,976,000</td>
<td align="right">10,929,520</td>
<td align="right">82.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_1</td>
<td align="right">3,745,874,415</td>
<td align="right">6,810,708,023</td>
<td align="right">81.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_SLOT</td>
<td align="right">429,239,062</td>
<td align="right">779,026,553</td>
<td align="right">81.5%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_METHOD_LAZY_DICT</td>
<td align="right">44,368,140</td>
<td align="right">76,756,695</td>
<td align="right">73.0%</td>
</tr>
<tr>
<td align="left">_LOAD_DEREF</td>
<td align="right">488,646,194</td>
<td align="right">835,223,325</td>
<td align="right">70.9%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_UNDER_INLINE</td>
<td align="right">1,079,683,147</td>
<td align="right">1,837,068,474</td>
<td align="right">70.1%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">50,628,850</td>
<td align="right">15,154,168</td>
<td align="right">-70.1%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR</td>
<td align="right">304,700,311</td>
<td align="right">516,657,108</td>
<td align="right">69.6%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_OVERFLOWED</td>
<td align="right">144,983,587</td>
<td align="right">245,267,433</td>
<td align="right">69.2%</td>
</tr>
<tr>
<td align="left">_BINARY_OP</td>
<td align="right">1,074,713,533</td>
<td align="right">1,797,390,925</td>
<td align="right">67.2%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">146,224,894</td>
<td align="right">244,529,663</td>
<td align="right">67.2%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_WITH_HINT</td>
<td align="right">1,323,217</td>
<td align="right">2,165,888</td>
<td align="right">63.7%</td>
</tr>
<tr>
<td align="left">_CHECK_PERIODIC</td>
<td align="right">4,484,384,711</td>
<td align="right">7,332,322,271</td>
<td align="right">63.5%</td>
</tr>
<tr>
<td align="left">_CHECK_VALIDITY</td>
<td align="right">33,527,682,697</td>
<td align="right">54,361,737,249</td>
<td align="right">62.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_1</td>
<td align="right">1,045,953,390</td>
<td align="right">1,688,960,670</td>
<td align="right">61.5%</td>
</tr>
<tr>
<td align="left">_CHECK_ATTR_CLASS</td>
<td align="right">213,637,320</td>
<td align="right">343,983,287</td>
<td align="right">61.0%</td>
</tr>
<tr>
<td align="left">_SET_IP</td>
<td align="right">38,093,009,837</td>
<td align="right">58,792,505,641</td>
<td align="right">54.3%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_TUPLE</td>
<td align="right">237,193,280</td>
<td align="right">362,013,255</td>
<td align="right">52.6%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_6</td>
<td align="right">404,647,767</td>
<td align="right">608,963,493</td>
<td align="right">50.5%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_FLOAT</td>
<td align="right">667,851,901</td>
<td align="right">1,002,607,999</td>
<td align="right">50.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_5</td>
<td align="right">3,445,911</td>
<td align="right">5,154,571</td>
<td align="right">49.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_FLOAT</td>
<td align="right">305,788,274</td>
<td align="right">453,482,115</td>
<td align="right">48.3%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_6</td>
<td align="right">802,098,190</td>
<td align="right">1,180,493,911</td>
<td align="right">47.2%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_FLOAT</td>
<td align="right">37,039,760</td>
<td align="right">54,174,127</td>
<td align="right">46.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_INT</td>
<td align="right">1,972,568,196</td>
<td align="right">2,884,695,005</td>
<td align="right">46.2%</td>
</tr>
<tr>
<td align="left">_BUILD_TUPLE</td>
<td align="right">569,129,783</td>
<td align="right">831,026,634</td>
<td align="right">46.0%</td>
</tr>
<tr>
<td align="left">_CALL_KW_NON_PY</td>
<td align="right">19,731,666</td>
<td align="right">28,739,281</td>
<td align="right">45.7%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE_KW</td>
<td align="right">19,731,666</td>
<td align="right">28,739,281</td>
<td align="right">45.7%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_RANGE</td>
<td align="right">427,723,907</td>
<td align="right">617,427,394</td>
<td align="right">44.4%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_RANGE</td>
<td align="right">427,723,907</td>
<td align="right">617,427,394</td>
<td align="right">44.4%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_RANGE</td>
<td align="right">406,690,152</td>
<td align="right">582,008,284</td>
<td align="right">43.1%</td>
</tr>
<tr>
<td align="left">_IS_OP</td>
<td align="right">252,648,116</td>
<td align="right">358,989,106</td>
<td align="right">42.1%</td>
</tr>
<tr>
<td align="left">_COLD_EXIT</td>
<td align="right">733,941,244</td>
<td align="right">1,033,998,510</td>
<td align="right">40.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_3</td>
<td align="right">2,602,171,818</td>
<td align="right">3,649,379,384</td>
<td align="right">40.2%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_DICT</td>
<td align="right">403,392,332</td>
<td align="right">565,018,959</td>
<td align="right">40.1%</td>
</tr>
<tr>
<td align="left">_MAP_ADD</td>
<td align="right">40,825,212</td>
<td align="right">56,926,657</td>
<td align="right">39.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_INT</td>
<td align="right">154,367,702</td>
<td align="right">215,218,967</td>
<td align="right">39.4%</td>
</tr>
<tr>
<td align="left">_GUARD_GLOBALS_VERSION</td>
<td align="right">2,191,153,276</td>
<td align="right">3,039,735,759</td>
<td align="right">38.7%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_DICT</td>
<td align="right">248,918,424</td>
<td align="right">342,564,254</td>
<td align="right">37.6%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_LIST</td>
<td align="right">1,367,779,818</td>
<td align="right">1,867,116,837</td>
<td align="right">36.5%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_FALSE_POP</td>
<td align="right">4,239,966,407</td>
<td align="right">5,773,968,108</td>
<td align="right">36.2%</td>
</tr>
<tr>
<td align="left">_GET_ITER</td>
<td align="right">512,436,311</td>
<td align="right">693,947,222</td>
<td align="right">35.4%</td>
</tr>
<tr>
<td align="left">_TO_BOOL</td>
<td align="right">140,122,676</td>
<td align="right">189,301,517</td>
<td align="right">35.1%</td>
</tr>
<tr>
<td align="left">_GUARD_IS_TRUE_POP</td>
<td align="right">2,652,160,302</td>
<td align="right">3,582,010,197</td>
<td align="right">35.1%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_DICT</td>
<td align="right">267,816,643</td>
<td align="right">361,682,276</td>
<td align="right">35.0%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_INT</td>
<td align="right">1,656,471,941</td>
<td align="right">2,234,300,847</td>
<td align="right">34.9%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_O</td>
<td align="right">573,326,095</td>
<td align="right">771,946,752</td>
<td align="right">34.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_STR</td>
<td align="right">37,123,103</td>
<td align="right">49,771,613</td>
<td align="right">34.1%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_INT</td>
<td align="right">1,781,398,265</td>
<td align="right">2,384,813,040</td>
<td align="right">33.9%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_UNICODE</td>
<td align="right">982,829,517</td>
<td align="right">653,764,021</td>
<td align="right">-33.5%</td>
</tr>
<tr>
<td align="left">_START_EXECUTOR</td>
<td align="right">3,619,698,274</td>
<td align="right">4,826,228,523</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_LIST_TIER_TWO</td>
<td align="right">1,239,548,558</td>
<td align="right">1,651,781,215</td>
<td align="right">33.3%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_TUPLE</td>
<td align="right">346,342,877</td>
<td align="right">456,952,995</td>
<td align="right">31.9%</td>
</tr>
<tr>
<td align="left">_BUILD_SLICE</td>
<td align="right">103,178,700</td>
<td align="right">133,314,168</td>
<td align="right">29.2%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_4</td>
<td align="right">1,016,568,260</td>
<td align="right">1,302,412,206</td>
<td align="right">28.1%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_LIST</td>
<td align="right">45,444,857</td>
<td align="right">58,010,588</td>
<td align="right">27.7%</td>
</tr>
<tr>
<td align="left">_SET_FUNCTION_ATTRIBUTE</td>
<td align="right">46,444,694</td>
<td align="right">33,707,954</td>
<td align="right">-27.4%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_DICT</td>
<td align="right">657,588,816</td>
<td align="right">834,323,177</td>
<td align="right">26.9%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_0</td>
<td align="right">142,238,307</td>
<td align="right">180,399,583</td>
<td align="right">26.8%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_ADD_INT</td>
<td align="right">2,303,434,304</td>
<td align="right">2,904,187,409</td>
<td align="right">26.1%</td>
</tr>
<tr>
<td align="left">_ITER_NEXT_TUPLE</td>
<td align="right">233,320,950</td>
<td align="right">294,016,468</td>
<td align="right">26.0%</td>
</tr>
<tr>
<td align="left">_BINARY_SLICE</td>
<td align="right">340,710,360</td>
<td align="right">426,876,356</td>
<td align="right">25.3%</td>
</tr>
<tr>
<td align="left">_ITER_CHECK_LIST</td>
<td align="right">1,495,931,416</td>
<td align="right">1,869,671,854</td>
<td align="right">25.0%</td>
</tr>
<tr>
<td align="left">_JUMP_TO_TOP</td>
<td align="right">2,368,756,602</td>
<td align="right">1,780,057,438</td>
<td align="right">-24.9%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_AND_CLEAR</td>
<td align="right">19,933,220</td>
<td align="right">24,836,947</td>
<td align="right">24.6%</td>
</tr>
<tr>
<td align="left">_PUSH_NULL</td>
<td align="right">3,705,105,689</td>
<td align="right">4,602,629,622</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST</td>
<td align="right">182,151,310</td>
<td align="right">226,246,890</td>
<td align="right">24.2%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW</td>
<td align="right">7,718,377,038</td>
<td align="right">9,577,053,244</td>
<td align="right">24.1%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_5</td>
<td align="right">799,894,824</td>
<td align="right">991,173,157</td>
<td align="right">23.9%</td>
</tr>
<tr>
<td align="left">_CALL_NON_PY_GENERAL</td>
<td align="right">409,313,708</td>
<td align="right">506,811,215</td>
<td align="right">23.8%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_DICT</td>
<td align="right">234,655,104</td>
<td align="right">290,135,028</td>
<td align="right">23.6%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,123,240,005</td>
<td align="right">1,388,772,755</td>
<td align="right">23.6%</td>
</tr>
<tr>
<td align="left">_CHECK_IS_NOT_PY_CALLABLE</td>
<td align="right">410,174,288</td>
<td align="right">507,083,544</td>
<td align="right">23.6%</td>
</tr>
<tr>
<td align="left">_LIST_APPEND</td>
<td align="right">156,695,612</td>
<td align="right">193,292,666</td>
<td align="right">23.4%</td>
</tr>
<tr>
<td align="left">_POP_TOP_LOAD_CONST_INLINE</td>
<td align="right">265,835,176</td>
<td align="right">326,980,394</td>
<td align="right">23.0%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">155,495,528</td>
<td align="right">189,883,445</td>
<td align="right">22.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_6</td>
<td align="right">26,715,008</td>
<td align="right">32,480,278</td>
<td align="right">21.6%</td>
</tr>
<tr>
<td align="left">_SWAP_2</td>
<td align="right">899,759,801</td>
<td align="right">1,093,485,016</td>
<td align="right">21.5%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE</td>
<td align="right">2,832,311,988</td>
<td align="right">3,439,270,487</td>
<td align="right">21.4%</td>
</tr>
<tr>
<td align="left">_STORE_FAST</td>
<td align="right">3,866,115,195</td>
<td align="right">4,668,999,540</td>
<td align="right">20.8%</td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">1,206,679,867</td>
<td align="right">1,451,952,199</td>
<td align="right">20.3%</td>
</tr>
<tr>
<td align="left">_EXIT_TRACE</td>
<td align="right">3,609,799,907</td>
<td align="right">4,311,356,106</td>
<td align="right">19.4%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_LIST</td>
<td align="right">2,345,782,880</td>
<td align="right">2,770,001,033</td>
<td align="right">18.1%</td>
</tr>
<tr>
<td align="left">_GUARD_NOT_EXHAUSTED_TUPLE</td>
<td align="right">345,648,943</td>
<td align="right">408,152,738</td>
<td align="right">18.1%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">182,690,748</td>
<td align="right">215,571,031</td>
<td align="right">18.0%</td>
</tr>
<tr>
<td align="left">_CALL_TYPE_1</td>
<td align="right">263,253,455</td>
<td align="right">309,954,018</td>
<td align="right">17.7%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">976,111,797</td>
<td align="right">1,145,537,436</td>
<td align="right">17.4%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_4</td>
<td align="right">3,879,484,598</td>
<td align="right">4,551,539,748</td>
<td align="right">17.3%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">2,141,356,686</td>
<td align="right">2,487,018,231</td>
<td align="right">16.1%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR_LIST_INT</td>
<td align="right">471,717,352</td>
<td align="right">542,869,818</td>
<td align="right">15.1%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_5</td>
<td align="right">3,755,805,130</td>
<td align="right">4,311,965,046</td>
<td align="right">14.8%</td>
</tr>
<tr>
<td align="left">_LOAD_CONST_INLINE_BORROW</td>
<td align="right">10,637,028,208</td>
<td align="right">12,181,984,129</td>
<td align="right">14.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">3,530,385</td>
<td align="right">3,049,562</td>
<td align="right">-13.6%</td>
</tr>
<tr>
<td align="left">_CALL_BUILTIN_FAST</td>
<td align="right">754,556,374</td>
<td align="right">856,805,598</td>
<td align="right">13.6%</td>
</tr>
<tr>
<td align="left">_TO_BOOL_NONE</td>
<td align="right">191,609,882</td>
<td align="right">165,701,451</td>
<td align="right">-13.5%</td>
</tr>
<tr>
<td align="left">_FOR_ITER_TIER_TWO</td>
<td align="right">1,212,707,372</td>
<td align="right">1,375,612,195</td>
<td align="right">13.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_LIST</td>
<td align="right">105,457,097</td>
<td align="right">118,885,756</td>
<td align="right">12.7%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_BORROW_7</td>
<td align="right">2,723,835,545</td>
<td align="right">3,052,079,525</td>
<td align="right">12.1%</td>
</tr>
<tr>
<td align="left">_CALL_LEN</td>
<td align="right">1,101,811,634</td>
<td align="right">1,228,359,808</td>
<td align="right">11.5%</td>
</tr>
<tr>
<td align="left">_CALL_STR_1</td>
<td align="right">47,062,820</td>
<td align="right">52,238,234</td>
<td align="right">11.0%</td>
</tr>
<tr>
<td align="left">_POP_ITER</td>
<td align="right">421,081,662</td>
<td align="right">375,383,236</td>
<td align="right">-10.9%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP_STR</td>
<td align="right">1,345,308,739</td>
<td align="right">1,490,867,230</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_OVERFLOWED</td>
<td align="right">1,228,429,102</td>
<td align="right">1,360,812,119</td>
<td align="right">10.8%</td>
</tr>
<tr>
<td align="left">_COMPARE_OP</td>
<td align="right">380,132,365</td>
<td align="right">420,130,373</td>
<td align="right">10.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_MULTIPLY_FLOAT__NO_DECREF_INPUTS</td>
<td align="right">430,309,104</td>
<td align="right">474,770,715</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">_MAKE_WARM</td>
<td align="right">5,988,453,793</td>
<td align="right">6,606,284,031</td>
<td align="right">10.3%</td>
</tr>
<tr>
<td align="left">_CONTAINS_OP_SET</td>
<td align="right">1,479,076,357</td>
<td align="right">1,624,496,485</td>
<td align="right">9.8%</td>
</tr>
<tr>
<td align="left">_COPY_FREE_VARS</td>
<td align="right">46,689,383</td>
<td align="right">51,202,896</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">_STORE_FAST_7</td>
<td align="right">1,014,606,581</td>
<td align="right">1,112,687,354</td>
<td align="right">9.7%</td>
</tr>
<tr>
<td align="left">_LIST_EXTEND</td>
<td align="right">70,350,190</td>
<td align="right">77,074,034</td>
<td align="right">9.6%</td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_LIST_APPEND</td>
<td align="right">876,883,752</td>
<td align="right">958,586,239</td>
<td align="right">9.3%</td>
</tr>
<tr>
<td align="left">_GUARD_NOS_NOT_NULL</td>
<td align="right">876,883,752</td>
<td align="right">955,178,179</td>
<td align="right">8.9%</td>
</tr>
<tr>
<td align="left">_CALL_INTRINSIC_1</td>
<td align="right">70,350,190</td>
<td align="right">76,384,274</td>
<td align="right">8.6%</td>
</tr>
<tr>
<td align="left">_COPY_2</td>
<td align="right">1,533,580,158</td>
<td align="right">1,663,291,068</td>
<td align="right">8.5%</td>
</tr>
<tr>
<td align="left">_MAKE_FUNCTION</td>
<td align="right">47,882,578</td>
<td align="right">44,380,938</td>
<td align="right">-7.3%</td>
</tr>
<tr>
<td align="left">_BUILD_LIST</td>
<td align="right">485,026,090</td>
<td align="right">517,823,595</td>
<td align="right">6.8%</td>
</tr>
<tr>
<td align="left">_LOAD_FAST_3</td>
<td align="right">78,215,044</td>
<td align="right">82,442,240</td>
<td align="right">5.4%</td>
</tr>
<tr>
<td align="left">_CALL_LIST_APPEND</td>
<td align="right">1,011,704,326</td>
<td align="right">1,065,178,626</td>
<td align="right">5.3%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_ANY_SET</td>
<td align="right">1,198,887,372</td>
<td align="right">1,253,825,402</td>
<td align="right">4.6%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE</td>
<td align="right">364,500</td>
<td align="right">378,882</td>
<td align="right">3.9%</td>
</tr>
<tr>
<td align="left">_POP_TOP_INT</td>
<td align="right">16,730,379</td>
<td align="right">17,351,414</td>
<td align="right">3.7%</td>
</tr>
<tr>
<td align="left">_CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">120,157,171</td>
<td align="right">124,539,246</td>
<td align="right">3.6%</td>
</tr>
<tr>
<td align="left">_SWAP_3</td>
<td align="right">758,452,301</td>
<td align="right">784,763,155</td>
<td align="right">3.5%</td>
</tr>
<tr>
<td align="left">_UNPACK_SEQUENCE_LIST</td>
<td align="right">60,012,240</td>
<td align="right">61,378,276</td>
<td align="right">2.3%</td>
</tr>
<tr>
<td align="left">_STORE_SUBSCR</td>
<td align="right">569,327,453</td>
<td align="right">563,654,550</td>
<td align="right">-1.0%</td>
</tr>
<tr>
<td align="left">_CONVERT_VALUE</td>
<td align="right">79,515,446</td>
<td align="right">80,171,973</td>
<td align="right">0.8%</td>
</tr>
<tr>
<td align="left">_FORMAT_SIMPLE</td>
<td align="right">80,015,830</td>
<td align="right">80,557,155</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_BUILD_STRING</td>
<td align="right">40,187,757</td>
<td align="right">40,452,548</td>
<td align="right">0.7%</td>
</tr>
<tr>
<td align="left">_STORE_SLICE</td>
<td align="right">111,492,300</td>
<td align="right">112,188,300</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">_INIT_CALL_PY_EXACT_ARGS_4</td>
<td align="right">498,445,573</td>
<td align="right">500,733,178</td>
<td align="right">0.5%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">425,721,392</td>
<td align="right">427,608,550</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_GUARD_TOS_SLICE</td>
<td align="right">425,721,392</td>
<td align="right">427,608,550</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">_RESUME_CHECK</td>
<td align="right">886,590,019</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_ANEXT</td>
<td align="right">94,136,760</td>
<td align="right">94,136,760</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBTRACT_FLOAT__NO_DECREF_INPUTS</td>
<td align="right">71,999,640</td>
<td align="right">71,999,640</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">_GUARD_IP</td>
<td align="right"></td>
<td align="right">5,439,830,164</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_DYNAMIC_EXIT</td>
<td align="right"></td>
<td align="right">483,970,257</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_FOR_ITER_GEN_FRAME</td>
<td align="right"></td>
<td align="right">267,991,753</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_CHECK_FUNC</td>
<td align="right"></td>
<td align="right">96,970,138</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_BINARY_OP_SUBSCR_INIT_CALL</td>
<td align="right"></td>
<td align="right">96,969,058</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_YIELD_VALUE</td>
<td align="right"></td>
<td align="right">87,614,365</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_AND_ALLOCATE_OBJECT</td>
<td align="right"></td>
<td align="right">55,109,368</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CREATE_INIT_FRAME</td>
<td align="right"></td>
<td align="right">54,287,908</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXIT_INIT_CHECK</td>
<td align="right"></td>
<td align="right">54,219,086</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_FOR</td>
<td align="right"></td>
<td align="right">36,512,952</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_SEND_GEN_FRAME</td>
<td align="right"></td>
<td align="right">36,474,309</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_REPLACE_WITH_TRUE</td>
<td align="right"></td>
<td align="right">28,473,220</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_COMMON_CONSTANT</td>
<td align="right"></td>
<td align="right">19,689,969</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_TYPE_1</td>
<td align="right"></td>
<td align="right">18,901,719</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT</td>
<td align="right"></td>
<td align="right">17,222,528</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_7</td>
<td align="right"></td>
<td align="right">16,924,672</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right"></td>
<td align="right">16,773,835</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_2</td>
<td align="right"></td>
<td align="right">12,790,066</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SMALL_INT_3</td>
<td align="right"></td>
<td align="right">12,597,442</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right"></td>
<td align="right">12,139,991</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_END_SEND</td>
<td align="right"></td>
<td align="right">7,560,425</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_ATTR_PROPERTY_FRAME</td>
<td align="right"></td>
<td align="right">6,293,433</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_GLOBAL</td>
<td align="right"></td>
<td align="right">5,296,880</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_AWAITABLE</td>
<td align="right"></td>
<td align="right">5,156,038</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_STR_1</td>
<td align="right"></td>
<td align="right">4,869,614</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GET_YIELD_FROM_ITER</td>
<td align="right"></td>
<td align="right">2,060,041</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_INSERT_NULL</td>
<td align="right"></td>
<td align="right">1,694,552</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SPECIAL</td>
<td align="right"></td>
<td align="right">1,694,552</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_FAST_CHECK</td>
<td align="right"></td>
<td align="right">1,198,310</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_CHECK_METHOD_VERSION_KW</td>
<td align="right"></td>
<td align="right">764,032</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_EXPAND_METHOD_KW</td>
<td align="right"></td>
<td align="right">764,032</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_IMPORT_FROM</td>
<td align="right"></td>
<td align="right">740,912</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_GLOBAL</td>
<td align="right"></td>
<td align="right">285,736</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_POP_CALL_LOAD_CONST_INLINE_BORROW</td>
<td align="right"></td>
<td align="right">33,333</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_GUARD_CALLABLE_TUPLE_1</td>
<td align="right"></td>
<td align="right">28,780</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_LOAD_SUPER_ATTR_ATTR</td>
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
<td align="left">_UNPACK_EX</td>
<td align="right"></td>
<td align="right">14,642</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">_STORE_ATTR_WITH_HINT</td>
<td align="right"></td>
<td align="right">4,900</td>
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
<td align="right">23,763</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">23,001</td>
<td align="right"></td>
<td align="right"></td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">1,811</td>
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
<td align="right">286</td>
<td align="right">138.3%</td>
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
<td align="right">286</td>
<td align="right">138.3%</td>
</tr>
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
<td align="right">313</td>
<td align="right">313</td>
<td align="right">0.0%</td>
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
<td align="right">2,436</td>
<td align="right">2,436</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-10-22
