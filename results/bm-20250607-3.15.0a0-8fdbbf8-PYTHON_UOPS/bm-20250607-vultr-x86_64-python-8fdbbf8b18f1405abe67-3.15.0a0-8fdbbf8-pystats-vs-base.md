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
<td align="left">JUMP_BACKWARD_NO_JIT</td>
<td align="right">5,854,821,299</td>
<td align="right">7,701,947</td>
<td align="right">-99.9%</td>
</tr>
<tr>
<td align="left">STORE_SLICE</td>
<td align="right">112,724,873</td>
<td align="right">1,232,453</td>
<td align="right">-98.9%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_SLICE</td>
<td align="right">441,384,642</td>
<td align="right">13,484,489</td>
<td align="right">-96.9%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_LIST</td>
<td align="right">62,357,839</td>
<td align="right">2,345,866</td>
<td align="right">-96.2%</td>
</tr>
<tr>
<td align="left">GET_ANEXT</td>
<td align="right">100,136,760</td>
<td align="right">6,000,000</td>
<td align="right">-94.0%</td>
</tr>
<tr>
<td align="left">FOR_ITER</td>
<td align="right">1,505,634,751</td>
<td align="right">217,177,150</td>
<td align="right">-85.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">691,583,140</td>
<td align="right">103,589,153</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_STR</td>
<td align="right">1,587,808,098</td>
<td align="right">242,911,880</td>
<td align="right">-84.7%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_SET</td>
<td align="right">1,753,875,042</td>
<td align="right">272,828,934</td>
<td align="right">-84.4%</td>
</tr>
<tr>
<td align="left">CALL_LEN</td>
<td align="right">1,387,960,988</td>
<td align="right">229,749,679</td>
<td align="right">-83.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_LIST_INT</td>
<td align="right">2,707,470,570</td>
<td align="right">459,469,972</td>
<td align="right">-83.0%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_LIST_INT</td>
<td align="right">569,318,332</td>
<td align="right">97,214,178</td>
<td align="right">-82.9%</td>
</tr>
<tr>
<td align="left">CALL_LIST_APPEND</td>
<td align="right">1,220,194,147</td>
<td align="right">215,342,393</td>
<td align="right">-82.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_INT</td>
<td align="right">3,436,223,605</td>
<td align="right">617,451,239</td>
<td align="right">-82.0%</td>
</tr>
<tr>
<td align="left">SWAP</td>
<td align="right">2,092,859,983</td>
<td align="right">376,515,700</td>
<td align="right">-82.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">506,503,558</td>
<td align="right">95,852,109</td>
<td align="right">-81.1%</td>
</tr>
<tr>
<td align="left">COPY</td>
<td align="right">2,239,704,017</td>
<td align="right">456,440,076</td>
<td align="right">-79.6%</td>
</tr>
<tr>
<td align="left">LIST_EXTEND</td>
<td align="right">89,008,541</td>
<td align="right">18,654,744</td>
<td align="right">-79.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_FLOAT</td>
<td align="right">353,327,020</td>
<td align="right">76,417,238</td>
<td align="right">-78.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_STR_INT</td>
<td align="right">1,251,912,100</td>
<td align="right">276,532,535</td>
<td align="right">-77.9%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST_WITH_KEYWORDS</td>
<td align="right">158,448,845</td>
<td align="right">38,362,601</td>
<td align="right">-75.8%</td>
</tr>
<tr>
<td align="left">BUILD_LIST</td>
<td align="right">654,391,234</td>
<td align="right">168,858,033</td>
<td align="right">-74.2%</td>
</tr>
<tr>
<td align="left">FOR_ITER_RANGE</td>
<td align="right">670,672,437</td>
<td align="right">178,490,243</td>
<td align="right">-73.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBTRACT_INT</td>
<td align="right">1,623,379,407</td>
<td align="right">433,462,897</td>
<td align="right">-73.3%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_LOAD_FAST</td>
<td align="right">942,762,299</td>
<td align="right">264,419,735</td>
<td align="right">-72.0%</td>
</tr>
<tr>
<td align="left">LOAD_SMALL_INT</td>
<td align="right">7,308,800,958</td>
<td align="right">2,076,774,401</td>
<td align="right">-71.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_FLOAT</td>
<td align="right">510,992,443</td>
<td align="right">146,023,675</td>
<td align="right">-71.4%</td>
</tr>
<tr>
<td align="left">EXTENDED_ARG</td>
<td align="right">704,296,789</td>
<td align="right">206,847,352</td>
<td align="right">-70.6%</td>
</tr>
<tr>
<td align="left">CALL_TYPE_1</td>
<td align="right">375,081,244</td>
<td align="right">111,738,450</td>
<td align="right">-70.2%</td>
</tr>
<tr>
<td align="left">STORE_FAST_LOAD_FAST</td>
<td align="right">199,311,618</td>
<td align="right">59,391,862</td>
<td align="right">-70.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS</td>
<td align="right">448,150,048</td>
<td align="right">134,760,620</td>
<td align="right">-69.9%</td>
</tr>
<tr>
<td align="left">NOT_TAKEN</td>
<td align="right">94,136,760</td>
<td align="right">158,268,379</td>
<td align="right">68.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">2,154,468,292</td>
<td align="right">690,802,675</td>
<td align="right">-67.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">540,251,784</td>
<td align="right">175,995,173</td>
<td align="right">-67.4%</td>
</tr>
<tr>
<td align="left">UNARY_NOT</td>
<td align="right">57,165,234</td>
<td align="right">18,855,372</td>
<td align="right">-67.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST</td>
<td align="right">3,463,643,131</td>
<td align="right">1,143,111,496</td>
<td align="right">-67.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_INT</td>
<td align="right">2,839,358,340</td>
<td align="right">939,725,678</td>
<td align="right">-66.9%</td>
</tr>
<tr>
<td align="left">BUILD_SLICE</td>
<td align="right">158,352,247</td>
<td align="right">55,173,427</td>
<td align="right">-65.2%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_BUILTIN</td>
<td align="right">5,875,592,967</td>
<td align="right">2,073,751,460</td>
<td align="right">-64.7%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">525,657,803</td>
<td align="right">186,089,293</td>
<td align="right">-64.6%</td>
</tr>
<tr>
<td align="left">TO_BOOL_INT</td>
<td align="right">262,087,838</td>
<td align="right">92,884,489</td>
<td align="right">-64.6%</td>
</tr>
<tr>
<td align="left">NOP</td>
<td align="right">2,504,419,490</td>
<td align="right">892,697,768</td>
<td align="right">-64.4%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST</td>
<td align="right">1,256,448,267</td>
<td align="right">453,214,202</td>
<td align="right">-63.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_NO_DICT</td>
<td align="right">2,500,208,933</td>
<td align="right">906,139,019</td>
<td align="right">-63.8%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR_DICT</td>
<td align="right">357,228,160</td>
<td align="right">129,881,408</td>
<td align="right">-63.6%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW_LOAD_FAST_BORROW</td>
<td align="right">10,197,614,583</td>
<td align="right">3,796,402,134</td>
<td align="right">-62.8%</td>
</tr>
<tr>
<td align="left">STORE_FAST</td>
<td align="right">13,606,182,146</td>
<td align="right">5,138,216,653</td>
<td align="right">-62.2%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_FALSE</td>
<td align="right">10,882,158,780</td>
<td align="right">4,124,430,849</td>
<td align="right">-62.1%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_DICT</td>
<td align="right">1,041,832,804</td>
<td align="right">396,787,187</td>
<td align="right">-61.9%</td>
</tr>
<tr>
<td align="left">MAP_ADD</td>
<td align="right">67,377,350</td>
<td align="right">26,552,447</td>
<td align="right">-60.6%</td>
</tr>
<tr>
<td align="left">CALL_STR_1</td>
<td align="right">77,912,251</td>
<td align="right">30,842,800</td>
<td align="right">-60.4%</td>
</tr>
<tr>
<td align="left">LIST_APPEND</td>
<td align="right">263,840,423</td>
<td align="right">106,930,321</td>
<td align="right">-59.5%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP_DICT</td>
<td align="right">440,902,117</td>
<td align="right">179,352,230</td>
<td align="right">-59.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_CLASS_WITH_METACLASS_CHECK</td>
<td align="right">22,610,683</td>
<td align="right">9,211,630</td>
<td align="right">-59.3%</td>
</tr>
<tr>
<td align="left">STORE_GLOBAL</td>
<td align="right">6,156,329</td>
<td align="right">2,600,969</td>
<td align="right">-57.8%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_O</td>
<td align="right">883,855,363</td>
<td align="right">377,829,685</td>
<td align="right">-57.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_LAZY_DICT</td>
<td align="right">92,363,408</td>
<td align="right">39,944,695</td>
<td align="right">-56.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_FLOAT</td>
<td align="right">1,079,502,741</td>
<td align="right">468,512,477</td>
<td align="right">-56.6%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_FAST_WITH_KEYWORDS</td>
<td align="right">102,878,994</td>
<td align="right">45,518,467</td>
<td align="right">-55.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_TRUE</td>
<td align="right">2,162,379,123</td>
<td align="right">963,337,659</td>
<td align="right">-55.5%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,358,191,287</td>
<td align="right">1,079,459,403</td>
<td align="right">-54.2%</td>
</tr>
<tr>
<td align="left">CALL_NON_PY_GENERAL</td>
<td align="right">787,634,059</td>
<td align="right">363,161,258</td>
<td align="right">-53.9%</td>
</tr>
<tr>
<td align="left">STORE_FAST_STORE_FAST</td>
<td align="right">802,859,374</td>
<td align="right">375,730,561</td>
<td align="right">-53.2%</td>
</tr>
<tr>
<td align="left">BINARY_OP_MULTIPLY_INT</td>
<td align="right">275,807,382</td>
<td align="right">129,524,931</td>
<td align="right">-53.0%</td>
</tr>
<tr>
<td align="left">LOAD_CONST</td>
<td align="right">8,688,852,058</td>
<td align="right">4,254,608,978</td>
<td align="right">-51.0%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_BORROW</td>
<td align="right">34,321,488,104</td>
<td align="right">16,934,461,808</td>
<td align="right">-50.7%</td>
</tr>
<tr>
<td align="left">TO_BOOL_LIST</td>
<td align="right">92,048,387</td>
<td align="right">46,293,851</td>
<td align="right">-49.7%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TUPLE</td>
<td align="right">403,001,169</td>
<td align="right">202,702,145</td>
<td align="right">-49.7%</td>
</tr>
<tr>
<td align="left">GET_ITER</td>
<td align="right">1,091,160,621</td>
<td align="right">557,373,064</td>
<td align="right">-48.9%</td>
</tr>
<tr>
<td align="left">SET_FUNCTION_ATTRIBUTE</td>
<td align="right">99,825,321</td>
<td align="right">51,643,191</td>
<td align="right">-48.3%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_NOARGS</td>
<td align="right">329,873,054</td>
<td align="right">174,160,906</td>
<td align="right">-47.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">256,916,608</td>
<td align="right">136,631,550</td>
<td align="right">-46.8%</td>
</tr>
<tr>
<td align="left">IS_OP</td>
<td align="right">551,092,702</td>
<td align="right">296,712,990</td>
<td align="right">-46.2%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_GENERAL</td>
<td align="right">13,159,200</td>
<td align="right">7,182,055</td>
<td align="right">-45.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_INPLACE_ADD_UNICODE</td>
<td align="right">7,879,405</td>
<td align="right">4,331,754</td>
<td align="right">-45.0%</td>
</tr>
<tr>
<td align="left">TO_BOOL_STR</td>
<td align="right">77,190,782</td>
<td align="right">42,878,702</td>
<td align="right">-44.5%</td>
</tr>
<tr>
<td align="left">BUILD_TUPLE</td>
<td align="right">1,202,382,675</td>
<td align="right">673,541,055</td>
<td align="right">-44.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_EXTEND</td>
<td align="right">283,819,630</td>
<td align="right">160,564,767</td>
<td align="right">-43.4%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">200,750,705</td>
<td align="right">114,129,228</td>
<td align="right">-43.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_BOOL</td>
<td align="right">3,977,674,854</td>
<td align="right">2,269,157,436</td>
<td align="right">-43.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">2,595,486,169</td>
<td align="right">1,483,270,418</td>
<td align="right">-42.9%</td>
</tr>
<tr>
<td align="left">MAKE_FUNCTION</td>
<td align="right">117,793,829</td>
<td align="right">68,153,371</td>
<td align="right">-42.1%</td>
</tr>
<tr>
<td align="left">CALL_KW_NON_PY</td>
<td align="right">61,319,873</td>
<td align="right">35,585,341</td>
<td align="right">-42.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP_FLOAT</td>
<td align="right">195,034,949</td>
<td align="right">114,764,820</td>
<td align="right">-41.2%</td>
</tr>
<tr>
<td align="left">PUSH_NULL</td>
<td align="right">1,575,683,873</td>
<td align="right">928,395,527</td>
<td align="right">-41.1%</td>
</tr>
<tr>
<td align="left">POP_ITER</td>
<td align="right">1,051,807,744</td>
<td align="right">620,067,303</td>
<td align="right">-41.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_FAST</td>
<td align="right">373,707,239</td>
<td align="right">222,672,031</td>
<td align="right">-40.4%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE_TWO_TUPLE</td>
<td align="right">779,059,911</td>
<td align="right">464,833,363</td>
<td align="right">-40.3%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">3,352,021,796</td>
<td align="right">2,003,092,161</td>
<td align="right">-40.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">216,642,378</td>
<td align="right">130,740,480</td>
<td align="right">-39.7%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">1,542,957,697</td>
<td align="right">941,023,218</td>
<td align="right">-39.0%</td>
</tr>
<tr>
<td align="left">LOAD_DEREF</td>
<td align="right">1,369,755,380</td>
<td align="right">845,724,876</td>
<td align="right">-38.3%</td>
</tr>
<tr>
<td align="left">CALL_INTRINSIC_1</td>
<td align="right">190,480,809</td>
<td align="right">120,129,834</td>
<td align="right">-36.9%</td>
</tr>
<tr>
<td align="left">CALL_BUILTIN_CLASS</td>
<td align="right">182,193,738</td>
<td align="right">117,346,805</td>
<td align="right">-35.6%</td>
</tr>
<tr>
<td align="left">CONVERT_VALUE</td>
<td align="right">116,432,417</td>
<td align="right">75,299,425</td>
<td align="right">-35.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">5,196,554,438</td>
<td align="right">3,378,178,856</td>
<td align="right">-35.0%</td>
</tr>
<tr>
<td align="left">FORMAT_SIMPLE</td>
<td align="right">123,911,719</td>
<td align="right">82,010,943</td>
<td align="right">-33.8%</td>
</tr>
<tr>
<td align="left">BUILD_STRING</td>
<td align="right">62,994,445</td>
<td align="right">41,725,025</td>
<td align="right">-33.8%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">823,461,892</td>
<td align="right">549,721,054</td>
<td align="right">-33.2%</td>
</tr>
<tr>
<td align="left">JUMP_FORWARD</td>
<td align="right">402,147,466</td>
<td align="right">280,932,739</td>
<td align="right">-30.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_AND_CLEAR</td>
<td align="right">66,666,701</td>
<td align="right">46,612,847</td>
<td align="right">-30.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">489,663,327</td>
<td align="right">348,151,021</td>
<td align="right">-28.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">266,479,892</td>
<td align="right">192,121,397</td>
<td align="right">-27.9%</td>
</tr>
<tr>
<td align="left">CALL_BOUND_METHOD_EXACT_ARGS</td>
<td align="right">189,115,959</td>
<td align="right">136,677,384</td>
<td align="right">-27.7%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL_MODULE</td>
<td align="right">3,533,730,061</td>
<td align="right">2,582,281,731</td>
<td align="right">-26.9%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_MODULE</td>
<td align="right">689,017,649</td>
<td align="right">511,327,208</td>
<td align="right">-25.8%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NONE</td>
<td align="right">348,339,984</td>
<td align="right">263,851,906</td>
<td align="right">-24.3%</td>
</tr>
<tr>
<td align="left">UNPACK_SEQUENCE</td>
<td align="right">1,579,451</td>
<td align="right">1,214,880</td>
<td align="right">-23.1%</td>
</tr>
<tr>
<td align="left">CALL_ISINSTANCE</td>
<td align="right">850,285,261</td>
<td align="right">660,454,924</td>
<td align="right">-22.3%</td>
</tr>
<tr>
<td align="left">RESUME_CHECK</td>
<td align="right">6,526,164,644</td>
<td align="right">5,153,028,516</td>
<td align="right">-21.0%</td>
</tr>
<tr>
<td align="left">CALL_METHOD_DESCRIPTOR_O</td>
<td align="right">367,607,577</td>
<td align="right">292,654,958</td>
<td align="right">-20.4%</td>
</tr>
<tr>
<td align="left">POP_TOP</td>
<td align="right">3,372,375,809</td>
<td align="right">2,728,065,057</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">POP_JUMP_IF_NOT_NONE</td>
<td align="right">471,715,854</td>
<td align="right">382,949,628</td>
<td align="right">-18.8%</td>
</tr>
<tr>
<td align="left">BINARY_OP_ADD_UNICODE</td>
<td align="right">78,575,170</td>
<td align="right">64,646,789</td>
<td align="right">-17.7%</td>
</tr>
<tr>
<td align="left">CALL_KW_PY</td>
<td align="right">82,786,886</td>
<td align="right">68,242,529</td>
<td align="right">-17.6%</td>
</tr>
<tr>
<td align="left">COPY_FREE_VARS</td>
<td align="right">344,746,141</td>
<td align="right">285,660,503</td>
<td align="right">-17.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_NO_DICT</td>
<td align="right">68,544,976</td>
<td align="right">58,012,696</td>
<td align="right">-15.4%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_TUPLE_INT</td>
<td align="right">290,923,787</td>
<td align="right">247,763,926</td>
<td align="right">-14.8%</td>
</tr>
<tr>
<td align="left">RETURN_VALUE</td>
<td align="right">5,616,167,940</td>
<td align="right">4,811,757,754</td>
<td align="right">-14.3%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">1,100,318,299</td>
<td align="right">946,367,082</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_SLOT</td>
<td align="right">942,573,322</td>
<td align="right">811,497,652</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">RETURN_GENERATOR</td>
<td align="right">417,048,528</td>
<td align="right">367,561,378</td>
<td align="right">-11.9%</td>
</tr>
<tr>
<td align="left">CALL_PY_GENERAL</td>
<td align="right">276,032,792</td>
<td align="right">244,381,289</td>
<td align="right">-11.5%</td>
</tr>
<tr>
<td align="left">STORE_ATTR</td>
<td align="right">67,681,233</td>
<td align="right">61,718,859</td>
<td align="right">-8.8%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR_METHOD</td>
<td align="right">63,662,822</td>
<td align="right">58,379,589</td>
<td align="right">-8.3%</td>
</tr>
<tr>
<td align="left">DICT_MERGE</td>
<td align="right">77,471,881</td>
<td align="right">71,542,575</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">BUILD_MAP</td>
<td align="right">151,712,009</td>
<td align="right">143,556,157</td>
<td align="right">-5.4%</td>
</tr>
<tr>
<td align="left">UNARY_INVERT</td>
<td align="right">10,293,070</td>
<td align="right">9,796,442</td>
<td align="right">-4.8%</td>
</tr>
<tr>
<td align="left">STORE_DEREF</td>
<td align="right">74,097,339</td>
<td align="right">70,890,874</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_WITH_HINT</td>
<td align="right">74,129,699</td>
<td align="right">71,632,767</td>
<td align="right">-3.4%</td>
</tr>
<tr>
<td align="left">UNARY_NEGATIVE</td>
<td align="right">127,567,424</td>
<td align="right">123,858,376</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">IMPORT_NAME</td>
<td align="right">11,576,384</td>
<td align="right">11,474,763</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">FOR_ITER_GEN</td>
<td align="right">345,622,259</td>
<td align="right">343,246,408</td>
<td align="right">-0.7%</td>
</tr>
<tr>
<td align="left">INTERPRETER_EXIT</td>
<td align="right">1,626,730,812</td>
<td align="right">1,618,074,392</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">MAKE_CELL</td>
<td align="right">65,680,489</td>
<td align="right">65,336,726</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">CALL_TUPLE_1</td>
<td align="right">6,253,153</td>
<td align="right">6,226,267</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">CALL_KW</td>
<td align="right">11,720</td>
<td align="right">11,765</td>
<td align="right">0.4%</td>
</tr>
<tr>
<td align="left">CLEANUP_THROW</td>
<td align="right">91,596</td>
<td align="right">91,336</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">DELETE_ATTR</td>
<td align="right">324,897</td>
<td align="right">324,117</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">YIELD_VALUE</td>
<td align="right">1,151,127,133</td>
<td align="right">1,148,748,128</td>
<td align="right">-0.2%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">223,971</td>
<td align="right">224,252</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD</td>
<td align="right">6,501</td>
<td align="right">6,508</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_FAST_CHECK</td>
<td align="right">3,935,227</td>
<td align="right">3,931,097</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">LOAD_SUPER_ATTR</td>
<td align="right">2,369</td>
<td align="right">2,371</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">LOAD_SPECIAL</td>
<td align="right">14,638,612</td>
<td align="right">14,627,168</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">DELETE_SUBSCR</td>
<td align="right">131,427,675</td>
<td align="right">131,373,389</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_COMMON_CONSTANT</td>
<td align="right">28,473,465</td>
<td align="right">28,463,966</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">IMPORT_FROM</td>
<td align="right">14,183,420</td>
<td align="right">14,180,254</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">GET_YIELD_FROM_ITER</td>
<td align="right">35,435,788</td>
<td align="right">35,428,130</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_FUNCTION_EX</td>
<td align="right">195,464,827</td>
<td align="right">195,436,630</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,440,667</td>
<td align="right">128,425,585</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">END_FOR</td>
<td align="right">114,996,545</td>
<td align="right">114,987,413</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RERAISE</td>
<td align="right">3,758,776</td>
<td align="right">3,758,516</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CHECK_EXC_MATCH</td>
<td align="right">20,799,246</td>
<td align="right">20,800,235</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">POP_EXCEPT</td>
<td align="right">21,141,492</td>
<td align="right">21,142,481</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">PUSH_EXC_INFO</td>
<td align="right">21,141,493</td>
<td align="right">21,142,482</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BUILD_SET</td>
<td align="right">437,286</td>
<td align="right">437,305</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_PROPERTY</td>
<td align="right">70,259,953</td>
<td align="right">70,262,204</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">EXIT_INIT_CHECK</td>
<td align="right">253,317,102</td>
<td align="right">253,309,009</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">CALL_ALLOC_AND_ENTER_INIT</td>
<td align="right">255,369,990</td>
<td align="right">255,361,897</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">END_SEND</td>
<td align="right">302,140,427</td>
<td align="right">302,133,017</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">LOAD_GLOBAL</td>
<td align="right">14,737,939</td>
<td align="right">14,738,274</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">JUMP_BACKWARD_NO_INTERRUPT</td>
<td align="right">419,758,787</td>
<td align="right">419,752,601</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">RAISE_VARARGS</td>
<td align="right">6,160,190</td>
<td align="right">6,160,198</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">BINARY_OP_SUBSCR_GETITEM</td>
<td align="right">163,021,744</td>
<td align="right">163,021,750</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">SEND_GEN</td>
<td align="right">593,230,356</td>
<td align="right">593,230,368</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AWAITABLE</td>
<td align="right">172,683,388</td>
<td align="right">172,683,388</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">INSTRUMENTED_LINE</td>
<td align="right">58,270,440</td>
<td align="right">58,270,440</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">DELETE_FAST</td>
<td align="right">41,963,282</td>
<td align="right">41,963,282</td>
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
<td align="left">LOAD_NAME</td>
<td align="right">9,738,685</td>
<td align="right">9,738,685</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_WITH_HINT</td>
<td align="right">8,975,993</td>
<td align="right">8,975,993</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">GET_AITER</td>
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
<td align="left">LOAD_SUPER_ATTR_ATTR</td>
<td align="right">4,526,903</td>
<td align="right">4,526,903</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">CALL_KW_BOUND_METHOD</td>
<td align="right">1,713,092</td>
<td align="right">1,713,092</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">UNPACK_EX</td>
<td align="right">235,809</td>
<td align="right">235,809</td>
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
<td align="right">47,846</td>
<td align="right">47,846</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">RESUME</td>
<td align="right">31,010</td>
<td align="right">31,010</td>
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
<td align="right">9,180</td>
<td align="right">9,180</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_BUILD_CLASS</td>
<td align="right">3,372</td>
<td align="right">3,372</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">LOAD_LOCALS</td>
<td align="right">3,349</td>
<td align="right">3,349</td>
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
<tr>
<td align="left">JUMP_BACKWARD_JIT</td>
<td align="right"></td>
<td align="right">1,078,319,165</td>
<td align="right"></td>
</tr>
<tr>
<td align="left">ENTER_EXECUTOR</td>
<td align="right"></td>
<td align="right">920,304,103</td>
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
<td align="right">16,185,454,328</td>
<td align="right">87.0%</td>
<td align="right">4,056,389,215</td>
<td align="right">78.1%</td>
<td align="right">-74.9%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">2,357,258,998</td>
<td align="right">12.7%</td>
<td align="right">1,078,979,944</td>
<td align="right">20.8%</td>
<td align="right">-54.2%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">62,387,811</td>
<td align="right">0.3%</td>
<td align="right">55,489,823</td>
<td align="right">1.1%</td>
<td align="right">-11.1%</td>
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
<td align="right">915,661</td>
<td align="right">43.4%</td>
<td align="right">462,756</td>
<td align="right">30.3%</td>
<td align="right">-49.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">1,193,521</td>
<td align="right">56.6%</td>
<td align="right">1,063,455</td>
<td align="right">69.7%</td>
<td align="right">-10.9%</td>
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
<td align="left">subscr bytes</td>
<td align="right">22,288</td>
<td align="right">2.4%</td>
<td align="right">1,808</td>
<td align="right">0.4%</td>
<td align="right">-91.9%</td>
</tr>
<tr>
<td align="left">subscr mappingproxy</td>
<td align="right">440</td>
<td align="right">0.0%</td>
<td align="right">80</td>
<td align="right">0.0%</td>
<td align="right">-81.8%</td>
</tr>
<tr>
<td align="left">xor int</td>
<td align="right">85,540</td>
<td align="right">9.3%</td>
<td align="right">16,340</td>
<td align="right">3.5%</td>
<td align="right">-80.9%</td>
</tr>
<tr>
<td align="left">subscr array</td>
<td align="right">127,767</td>
<td align="right">14.0%</td>
<td align="right">25,838</td>
<td align="right">5.6%</td>
<td align="right">-79.8%</td>
</tr>
<tr>
<td align="left">true divide float</td>
<td align="right">11,587</td>
<td align="right">1.3%</td>
<td align="right">2,768</td>
<td align="right">0.6%</td>
<td align="right">-76.1%</td>
</tr>
<tr>
<td align="left">and int</td>
<td align="right">74,191</td>
<td align="right">8.1%</td>
<td align="right">18,467</td>
<td align="right">4.0%</td>
<td align="right">-75.1%</td>
</tr>
<tr>
<td align="left">subscr counter</td>
<td align="right">107,772</td>
<td align="right">11.8%</td>
<td align="right">26,892</td>
<td align="right">5.8%</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">power</td>
<td align="right">8,202</td>
<td align="right">0.9%</td>
<td align="right">2,349</td>
<td align="right">0.5%</td>
<td align="right">-71.4%</td>
</tr>
<tr>
<td align="left">and other</td>
<td align="right">1,075</td>
<td align="right">0.1%</td>
<td align="right">318</td>
<td align="right">0.1%</td>
<td align="right">-70.4%</td>
</tr>
<tr>
<td align="left">multiply other</td>
<td align="right">2,678</td>
<td align="right">0.3%</td>
<td align="right">836</td>
<td align="right">0.2%</td>
<td align="right">-68.8%</td>
</tr>
<tr>
<td align="left">rshift</td>
<td align="right">23,508</td>
<td align="right">2.6%</td>
<td align="right">8,301</td>
<td align="right">1.8%</td>
<td align="right">-64.7%</td>
</tr>
<tr>
<td align="left">xor</td>
<td align="right">320</td>
<td align="right">0.0%</td>
<td align="right">140</td>
<td align="right">0.0%</td>
<td align="right">-56.2%</td>
</tr>
<tr>
<td align="left">add different types</td>
<td align="right">43,776</td>
<td align="right">4.8%</td>
<td align="right">20,483</td>
<td align="right">4.4%</td>
<td align="right">-53.2%</td>
</tr>
<tr>
<td align="left">floor divide</td>
<td align="right">33,951</td>
<td align="right">3.7%</td>
<td align="right">19,866</td>
<td align="right">4.3%</td>
<td align="right">-41.5%</td>
</tr>
<tr>
<td align="left">lshift</td>
<td align="right">19,438</td>
<td align="right">2.1%</td>
<td align="right">11,545</td>
<td align="right">2.5%</td>
<td align="right">-40.6%</td>
</tr>
<tr>
<td align="left">add other</td>
<td align="right">37,861</td>
<td align="right">4.1%</td>
<td align="right">23,705</td>
<td align="right">5.1%</td>
<td align="right">-37.4%</td>
</tr>
<tr>
<td align="left">subtract other</td>
<td align="right">8,509</td>
<td align="right">0.9%</td>
<td align="right">6,189</td>
<td align="right">1.3%</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">subscr defaultdict</td>
<td align="right">78,712</td>
<td align="right">8.6%</td>
<td align="right">62,855</td>
<td align="right">13.6%</td>
<td align="right">-20.1%</td>
</tr>
<tr>
<td align="left">multiply different types</td>
<td align="right">7,694</td>
<td align="right">0.8%</td>
<td align="right">6,222</td>
<td align="right">1.3%</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">remainder</td>
<td align="right">43,287</td>
<td align="right">4.7%</td>
<td align="right">36,527</td>
<td align="right">7.9%</td>
<td align="right">-15.6%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">46,863</td>
<td align="right">5.1%</td>
<td align="right">41,345</td>
<td align="right">8.9%</td>
<td align="right">-11.8%</td>
</tr>
<tr>
<td align="left">subscr</td>
<td align="right">7,296</td>
<td align="right">0.8%</td>
<td align="right">7,019</td>
<td align="right">1.5%</td>
<td align="right">-3.8%</td>
</tr>
<tr>
<td align="left">true divide different types</td>
<td align="right">2,001</td>
<td align="right">0.2%</td>
<td align="right">1,962</td>
<td align="right">0.4%</td>
<td align="right">-1.9%</td>
</tr>
<tr>
<td align="left">subscr deque</td>
<td align="right">105</td>
<td align="right">0.0%</td>
<td align="right">107</td>
<td align="right">0.0%</td>
<td align="right">1.9%</td>
</tr>
<tr>
<td align="left">subtract different types</td>
<td align="right">631</td>
<td align="right">0.1%</td>
<td align="right">629</td>
<td align="right">0.1%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">true divide other</td>
<td align="right">1,387</td>
<td align="right">0.2%</td>
<td align="right">1,383</td>
<td align="right">0.3%</td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">subscr string slice</td>
<td align="right">2,216</td>
<td align="right">0.2%</td>
<td align="right">2,215</td>
<td align="right">0.5%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">subscr tuple slice</td>
<td align="right">109,555</td>
<td align="right">12.0%</td>
<td align="right">109,556</td>
<td align="right">23.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr range</td>
<td align="right">3,162</td>
<td align="right">0.3%</td>
<td align="right">3,162</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">or</td>
<td align="right">3,100</td>
<td align="right">0.3%</td>
<td align="right">3,100</td>
<td align="right">0.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr other slice</td>
<td align="right">311</td>
<td align="right">0.0%</td>
<td align="right">311</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
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
<td align="left">or int</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">20</td>
<td align="right">0.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">subscr ordereddict</td>
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
<td align="right">525,657,803</td>
<td align="right">100.0%</td>
<td align="right">186,089,293</td>
<td align="right">100.0%</td>
<td align="right">-64.6%</td>
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
<td align="right">11,370,115,500</td>
<td align="right">98.3%</td>
<td align="right">5,347,201,825</td>
<td align="right">97.0%</td>
<td align="right">-53.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">191,756,201</td>
<td align="right">1.7%</td>
<td align="right">163,814,492</td>
<td align="right">3.0%</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">188,200,455</td>
<td align="right">1.6%</td>
<td align="right">160,786,000</td>
<td align="right">2.9%</td>
<td align="right">-14.6%</td>
</tr>
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
<td align="right">8,000</td>
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
<td align="right">3,779,571</td>
<td align="right">100.0%</td>
<td align="right">3,252,598</td>
<td align="right">100.0%</td>
<td align="right">-13.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">146</td>
<td align="right">0.0%</td>
<td align="right">146</td>
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
<td align="left">init not simple</td>
<td align="right">731</td>
<td align="right">500.7%</td>
<td align="right">731</td>
<td align="right">500.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">init not python</td>
<td align="right">266</td>
<td align="right">182.2%</td>
<td align="right">266</td>
<td align="right">182.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">146</td>
<td align="right">100.0%</td>
<td align="right">146</td>
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
<td align="right">535,218</td>
<td align="right">96.6%</td>
<td align="right">535,220</td>
<td align="right">96.6%</td>
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
<td align="right">542,289</td>
<td align="right">97.9%</td>
<td align="right">542,289</td>
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
<td align="right">18,791</td>
<td align="right">100.0%</td>
<td align="right">18,834</td>
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
<td align="right">506,267,957</td>
<td align="right">9.9%</td>
<td align="right">95,716,746</td>
<td align="right">6.9%</td>
<td align="right">-81.1%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,620,759,733</td>
<td align="right">90.1%</td>
<td align="right">1,295,963,337</td>
<td align="right">93.0%</td>
<td align="right">-72.0%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">1,441,654</td>
<td align="right">0.0%</td>
<td align="right">1,439,041</td>
<td align="right">0.1%</td>
<td align="right">-0.2%</td>
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
<td align="right">213,827</td>
<td align="right">81.4%</td>
<td align="right">113,574</td>
<td align="right">70.0%</td>
<td align="right">-46.9%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">48,805</td>
<td align="right">18.6%</td>
<td align="right">48,766</td>
<td align="right">30.0%</td>
<td align="right">-0.1%</td>
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
<td align="right">84,956</td>
<td align="right">39.7%</td>
<td align="right">4,104</td>
<td align="right">3.6%</td>
<td align="right">-95.2%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">6,821</td>
<td align="right">3.2%</td>
<td align="right">360</td>
<td align="right">0.3%</td>
<td align="right">-94.7%</td>
</tr>
<tr>
<td align="left">baseobject</td>
<td align="right">10,898</td>
<td align="right">5.1%</td>
<td align="right">6,163</td>
<td align="right">5.4%</td>
<td align="right">-43.4%</td>
</tr>
<tr>
<td align="left">float long</td>
<td align="right">14,804</td>
<td align="right">6.9%</td>
<td align="right">8,941</td>
<td align="right">7.9%</td>
<td align="right">-39.6%</td>
</tr>
<tr>
<td align="left">different types</td>
<td align="right">45,908</td>
<td align="right">21.5%</td>
<td align="right">43,940</td>
<td align="right">38.7%</td>
<td align="right">-4.3%</td>
</tr>
<tr>
<td align="left">big int</td>
<td align="right">30,740</td>
<td align="right">14.4%</td>
<td align="right">30,376</td>
<td align="right">26.7%</td>
<td align="right">-1.2%</td>
</tr>
<tr>
<td align="left">bool</td>
<td align="right">1,866</td>
<td align="right">0.9%</td>
<td align="right">1,859</td>
<td align="right">1.6%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">1,349</td>
<td align="right">0.6%</td>
<td align="right">1,348</td>
<td align="right">1.2%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">7,709</td>
<td align="right">3.6%</td>
<td align="right">7,707</td>
<td align="right">6.8%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">7,641</td>
<td align="right">3.6%</td>
<td align="right">7,641</td>
<td align="right">6.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">951</td>
<td align="right">0.4%</td>
<td align="right">951</td>
<td align="right">0.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">long float</td>
<td align="right">184</td>
<td align="right">0.1%</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">2,193,375,021</td>
<td align="right">91.6%</td>
<td align="right">450,779,026</td>
<td align="right">79.6%</td>
<td align="right">-79.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">200,679,960</td>
<td align="right">8.4%</td>
<td align="right">114,079,731</td>
<td align="right">20.1%</td>
<td align="right">-43.2%</td>
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
<td align="right">1,402,138</td>
<td align="right">0.2%</td>
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
<td align="right">68,880</td>
<td align="right">70.9%</td>
<td align="right">47,632</td>
<td align="right">62.7%</td>
<td align="right">-30.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">28,317</td>
<td align="right">29.1%</td>
<td align="right">28,317</td>
<td align="right">37.3%</td>
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
<td align="right">24,144</td>
<td align="right">35.1%</td>
<td align="right">9,962</td>
<td align="right">20.9%</td>
<td align="right">-58.7%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">23,211</td>
<td align="right">33.7%</td>
<td align="right">18,445</td>
<td align="right">38.7%</td>
<td align="right">-20.5%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">10,927</td>
<td align="right">15.9%</td>
<td align="right">9,159</td>
<td align="right">19.2%</td>
<td align="right">-16.2%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">10,598</td>
<td align="right">15.4%</td>
<td align="right">10,066</td>
<td align="right">21.1%</td>
<td align="right">-5.0%</td>
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
<td align="right">1,505,198,136</td>
<td align="right">28.9%</td>
<td align="right">217,057,196</td>
<td align="right">13.5%</td>
<td align="right">-85.6%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">163,988,873</td>
<td align="right">3.1%</td>
<td align="right">55,678,507</td>
<td align="right">3.5%</td>
<td align="right">-66.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">3,547,025,899</td>
<td align="right">68.0%</td>
<td align="right">1,332,855,992</td>
<td align="right">83.0%</td>
<td align="right">-62.4%</td>
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
<td align="right">430,858</td>
<td align="right">12.2%</td>
<td align="right">114,189</td>
<td align="right">9.8%</td>
<td align="right">-73.5%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">3,099,698</td>
<td align="right">87.8%</td>
<td align="right">1,056,154</td>
<td align="right">90.2%</td>
<td align="right">-65.9%</td>
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
<td align="right">161,253</td>
<td align="right">37.4%</td>
<td align="right">4,114</td>
<td align="right">3.6%</td>
<td align="right">-97.4%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">83,645</td>
<td align="right">19.4%</td>
<td align="right">10,920</td>
<td align="right">9.6%</td>
<td align="right">-86.9%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">34,738</td>
<td align="right">8.1%</td>
<td align="right">6,524</td>
<td align="right">5.7%</td>
<td align="right">-81.2%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">18,157</td>
<td align="right">4.2%</td>
<td align="right">4,077</td>
<td align="right">3.6%</td>
<td align="right">-77.5%</td>
</tr>
<tr>
<td align="left">bytes</td>
<td align="right">1,120</td>
<td align="right">0.3%</td>
<td align="right">280</td>
<td align="right">0.2%</td>
<td align="right">-75.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">11,721</td>
<td align="right">2.7%</td>
<td align="right">4,246</td>
<td align="right">3.7%</td>
<td align="right">-63.8%</td>
</tr>
<tr>
<td align="left">ascii string</td>
<td align="right">3,396</td>
<td align="right">0.8%</td>
<td align="right">1,435</td>
<td align="right">1.3%</td>
<td align="right">-57.7%</td>
</tr>
<tr>
<td align="left">seq iter</td>
<td align="right">16,123</td>
<td align="right">3.7%</td>
<td align="right">6,892</td>
<td align="right">6.0%</td>
<td align="right">-57.3%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">533</td>
<td align="right">0.1%</td>
<td align="right">232</td>
<td align="right">0.2%</td>
<td align="right">-56.5%</td>
</tr>
<tr>
<td align="left">reversed list</td>
<td align="right">3,051</td>
<td align="right">0.7%</td>
<td align="right">1,931</td>
<td align="right">1.7%</td>
<td align="right">-36.7%</td>
</tr>
<tr>
<td align="left">map</td>
<td align="right">251</td>
<td align="right">0.1%</td>
<td align="right">171</td>
<td align="right">0.1%</td>
<td align="right">-31.9%</td>
</tr>
<tr>
<td align="left">callable</td>
<td align="right">131</td>
<td align="right">0.0%</td>
<td align="right">91</td>
<td align="right">0.1%</td>
<td align="right">-30.5%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">17,737</td>
<td align="right">4.1%</td>
<td align="right">12,490</td>
<td align="right">10.9%</td>
<td align="right">-29.6%</td>
</tr>
<tr>
<td align="left">dict items</td>
<td align="right">68,620</td>
<td align="right">15.9%</td>
<td align="right">51,638</td>
<td align="right">45.2%</td>
<td align="right">-24.7%</td>
</tr>
<tr>
<td align="left">itertools</td>
<td align="right">4,324</td>
<td align="right">1.0%</td>
<td align="right">3,430</td>
<td align="right">3.0%</td>
<td align="right">-20.7%</td>
</tr>
<tr>
<td align="left">dict values</td>
<td align="right">6,038</td>
<td align="right">1.4%</td>
<td align="right">5,678</td>
<td align="right">5.0%</td>
<td align="right">-6.0%</td>
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
<td align="right">126,675,878</td>
<td align="right">126,675,878 / 0 !!</td>
<td align="right">124,674,077</td>
<td align="right">124,674,077 / 0 !!</td>
<td align="right">-1.6%</td>
</tr>
<tr>
<td align="left">list</td>
<td align="right">311,246,857</td>
<td align="right">311,246,857 / 0 !!</td>
<td align="right">308,573,406</td>
<td align="right">308,573,406 / 0 !!</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">12,104,372</td>
<td align="right">12,104,372 / 0 !!</td>
<td align="right">12,088,839</td>
<td align="right">12,088,839 / 0 !!</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">173,265,584</td>
<td align="right">173,265,584 / 0 !!</td>
<td align="right">173,231,782</td>
<td align="right">173,231,782 / 0 !!</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">generator</td>
<td align="right">101,609,343</td>
<td align="right">101,609,343 / 0 !!</td>
<td align="right">101,600,459</td>
<td align="right">101,600,459 / 0 !!</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">self</td>
<td align="right">322,266,384</td>
<td align="right">322,266,384 / 0 !!</td>
<td align="right">322,243,593</td>
<td align="right">322,243,593 / 0 !!</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">enumerate</td>
<td align="right">5,461,008</td>
<td align="right">5,461,008 / 0 !!</td>
<td align="right">5,461,023</td>
<td align="right">5,461,023 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">dict keys</td>
<td align="right">34,932,334</td>
<td align="right">34,932,334 / 0 !!</td>
<td align="right">34,932,334</td>
<td align="right">34,932,334 / 0 !!</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">string</td>
<td align="right">2,823,421</td>
<td align="right">2,823,421 / 0 !!</td>
<td align="right">2,823,421</td>
<td align="right">2,823,421 / 0 !!</td>
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
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">12,699,665,834</td>
<td align="right">88.3%</td>
<td align="right">7,166,890,108</td>
<td align="right">85.9%</td>
<td align="right">-43.6%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">821,701,189</td>
<td align="right">5.7%</td>
<td align="right">548,049,614</td>
<td align="right">6.6%</td>
<td align="right">-33.3%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">867,147,291</td>
<td align="right">6.0%</td>
<td align="right">629,044,200</td>
<td align="right">7.5%</td>
<td align="right">-27.5%</td>
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
<td align="right">1,422,762</td>
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
<td align="right">16,437,378</td>
<td align="right">97.0%</td>
<td align="right">11,945,209</td>
<td align="right">96.5%</td>
<td align="right">-27.3%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">505,756</td>
<td align="right">3.0%</td>
<td align="right">434,179</td>
<td align="right">3.5%</td>
<td align="right">-14.2%</td>
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
<td align="right">74,992</td>
<td align="right">14.8%</td>
<td align="right">37,704</td>
<td align="right">8.7%</td>
<td align="right">-49.7%</td>
</tr>
<tr>
<td align="left">builtin class method</td>
<td align="right">1,059</td>
<td align="right">0.2%</td>
<td align="right">699</td>
<td align="right">0.2%</td>
<td align="right">-34.0%</td>
</tr>
<tr>
<td align="left">overriding descriptor</td>
<td align="right">57,947</td>
<td align="right">11.5%</td>
<td align="right">40,088</td>
<td align="right">9.2%</td>
<td align="right">-30.8%</td>
</tr>
<tr>
<td align="left">non overriding descriptor</td>
<td align="right">5,934</td>
<td align="right">1.2%</td>
<td align="right">4,689</td>
<td align="right">1.1%</td>
<td align="right">-21.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">8,779</td>
<td align="right">1.7%</td>
<td align="right">7,611</td>
<td align="right">1.8%</td>
<td align="right">-13.3%</td>
</tr>
<tr>
<td align="left">expected error</td>
<td align="right">2,734</td>
<td align="right">0.5%</td>
<td align="right">2,374</td>
<td align="right">0.5%</td>
<td align="right">-13.2%</td>
</tr>
<tr>
<td align="left">mutable class</td>
<td align="right">52,593</td>
<td align="right">10.4%</td>
<td align="right">47,874</td>
<td align="right">11.0%</td>
<td align="right">-9.0%</td>
</tr>
<tr>
<td align="left">class method obj</td>
<td align="right">17,032</td>
<td align="right">3.4%</td>
<td align="right">16,361</td>
<td align="right">3.8%</td>
<td align="right">-3.9%</td>
</tr>
<tr>
<td align="left">metaclass attribute</td>
<td align="right">24,277</td>
<td align="right">4.8%</td>
<td align="right">23,973</td>
<td align="right">5.5%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">module attr not found</td>
<td align="right">4,411</td>
<td align="right">0.9%</td>
<td align="right">4,411</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">1,713</td>
<td align="right">0.3%</td>
<td align="right">1,713</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">non object slot</td>
<td align="right">1,035</td>
<td align="right">0.2%</td>
<td align="right">1,035</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">823</td>
<td align="right">0.2%</td>
<td align="right">823</td>
<td align="right">0.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">643</td>
<td align="right">0.1%</td>
<td align="right">643</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of versions</td>
<td align="right">400</td>
<td align="right">0.1%</td>
<td align="right">400</td>
<td align="right">0.1%</td>
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
<td align="right">9,409,280,831</td>
<td align="right">99.8%</td>
<td align="right">4,655,990,996</td>
<td align="right">99.7%</td>
<td align="right">-50.5%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">42,197</td>
<td align="right">0.0%</td>
<td align="right">42,195</td>
<td align="right">0.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">14,612,307</td>
<td align="right">0.2%</td>
<td align="right">14,612,368</td>
<td align="right">0.3%</td>
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
<td align="right">1,325</td>
<td align="right">0.0%</td>
<td align="right">1,325</td>
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
<td align="right">126,358</td>
<td align="right">100.0%</td>
<td align="right">126,632</td>
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
<td align="right">68,189,725</td>
<td align="right">100.0%</td>
<td align="right">62,906,492</td>
<td align="right">100.0%</td>
<td align="right">-7.7%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">110</td>
<td align="right">0.0%</td>
<td align="right">112</td>
<td align="right">0.0%</td>
<td align="right">1.8%</td>
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
<td align="right">2,259</td>
<td align="right">100.0%</td>
<td align="right">2,259</td>
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
<td align="right">128,391,290</td>
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
<td align="right">593,215,645</td>
<td align="right">82.2%</td>
<td align="right">593,215,657</td>
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
<td align="right">33,951</td>
<td align="right">98.2%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">616</td>
<td align="right">1.8%</td>
<td align="right">616</td>
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
<td align="right">1,936,564,302</td>
<td align="right">91.4%</td>
<td align="right">1,656,856,136</td>
<td align="right">90.6%</td>
<td align="right">-14.4%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">67,595,781</td>
<td align="right">3.2%</td>
<td align="right">61,634,713</td>
<td align="right">3.4%</td>
<td align="right">-8.8%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">115,303,312</td>
<td align="right">5.4%</td>
<td align="right">109,984,591</td>
<td align="right">6.0%</td>
<td align="right">-4.6%</td>
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
<td align="right">2,214,762</td>
<td align="right">98.0%</td>
<td align="right">2,114,567</td>
<td align="right">97.9%</td>
<td align="right">-4.5%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">45,783</td>
<td align="right">2.0%</td>
<td align="right">44,315</td>
<td align="right">2.1%</td>
<td align="right">-3.2%</td>
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
<td align="right">6,084</td>
<td align="right">13.3%</td>
<td align="right">4,651</td>
<td align="right">10.5%</td>
<td align="right">-23.6%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">242,259</td>
<td align="right">529.1%</td>
<td align="right">235,344</td>
<td align="right">531.1%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">not managed dict</td>
<td align="right">2,994</td>
<td align="right">6.5%</td>
<td align="right">2,979</td>
<td align="right">6.7%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">class attr simple</td>
<td align="right">20,316</td>
<td align="right">44.4%</td>
<td align="right">20,295</td>
<td align="right">45.8%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">not in dict</td>
<td align="right">7,206</td>
<td align="right">15.7%</td>
<td align="right">7,206</td>
<td align="right">16.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">split dict</td>
<td align="right">3,673</td>
<td align="right">8.0%</td>
<td align="right">3,673</td>
<td align="right">8.3%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">property</td>
<td align="right">1,614</td>
<td align="right">3.5%</td>
<td align="right">1,614</td>
<td align="right">3.6%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">not in keys</td>
<td align="right">749</td>
<td align="right">1.6%</td>
<td align="right">749</td>
<td align="right">1.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">method</td>
<td align="right">421</td>
<td align="right">0.9%</td>
<td align="right">421</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">overridden</td>
<td align="right">313</td>
<td align="right">0.7%</td>
<td align="right">313</td>
<td align="right">0.7%</td>
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
<tr>
<td align="left">mutable class</td>
<td align="right">89</td>
<td align="right">0.2%</td>
<td align="right">89</td>
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
<td align="right">112,724,873</td>
<td align="right">100.0%</td>
<td align="right">1,232,453</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">691,400,504</td>
<td align="right">42.7%</td>
<td align="right">103,550,008</td>
<td align="right">31.3%</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">926,544,272</td>
<td align="right">57.3%</td>
<td align="right">227,093,366</td>
<td align="right">68.7%</td>
<td align="right">-75.5%</td>
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
<td align="right">179,717</td>
<td align="right">98.4%</td>
<td align="right">36,221</td>
<td align="right">92.4%</td>
<td align="right">-79.8%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">2,959</td>
<td align="right">1.6%</td>
<td align="right">2,964</td>
<td align="right">7.6%</td>
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
<td align="left">other</td>
<td align="right">81,221</td>
<td align="right">45.2%</td>
<td align="right">320</td>
<td align="right">0.9%</td>
<td align="right">-99.6%</td>
</tr>
<tr>
<td align="left">bytearray int</td>
<td align="right">5,259</td>
<td align="right">2.9%</td>
<td align="right">136</td>
<td align="right">0.4%</td>
<td align="right">-97.4%</td>
</tr>
<tr>
<td align="left">dict subclass no override</td>
<td align="right">19,143</td>
<td align="right">10.7%</td>
<td align="right">3,283</td>
<td align="right">9.1%</td>
<td align="right">-82.9%</td>
</tr>
<tr>
<td align="left">array int</td>
<td align="right">52,096</td>
<td align="right">29.0%</td>
<td align="right">10,484</td>
<td align="right">28.9%</td>
<td align="right">-79.9%</td>
</tr>
<tr>
<td align="left">py simple</td>
<td align="right">17,279</td>
<td align="right">9.6%</td>
<td align="right">17,279</td>
<td align="right">47.7%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">list slice</td>
<td align="right">2,978</td>
<td align="right">1.7%</td>
<td align="right">2,978</td>
<td align="right">8.2%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">out of range</td>
<td align="right">1,673</td>
<td align="right">0.9%</td>
<td align="right">1,673</td>
<td align="right">4.6%</td>
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
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">256,268,197</td>
<td align="right">4.9%</td>
<td align="right">136,070,434</td>
<td align="right">4.6%</td>
<td align="right">-46.9%</td>
</tr>
<tr>
<td align="left">
hit
<details>
<summary>ⓘ</summary>

Specialized instructions that complete.
</details>
</td>
<td align="right">4,837,253,474</td>
<td align="right">92.9%</td>
<td align="right">2,760,117,715</td>
<td align="right">93.1%</td>
<td align="right">-42.9%</td>
</tr>
<tr>
<td align="left">
miss
<details>
<summary>ⓘ</summary>

Specialized instructions that deopt.
</details>
</td>
<td align="right">110,467,647</td>
<td align="right">2.1%</td>
<td align="right">67,613,886</td>
<td align="right">2.3%</td>
<td align="right">-38.8%</td>
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
<td align="right">2,132,520</td>
<td align="right">78.1%</td>
<td align="right">1,324,010</td>
<td align="right">72.1%</td>
<td align="right">-37.9%</td>
</tr>
<tr>
<td align="left">Failure</td>
<td align="right">598,760</td>
<td align="right">21.9%</td>
<td align="right">511,439</td>
<td align="right">27.9%</td>
<td align="right">-14.6%</td>
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
<td align="right">16,018</td>
<td align="right">2.7%</td>
<td align="right">1,818</td>
<td align="right">0.4%</td>
<td align="right">-88.7%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">126,831</td>
<td align="right">21.2%</td>
<td align="right">68,479</td>
<td align="right">13.4%</td>
<td align="right">-46.0%</td>
</tr>
<tr>
<td align="left">dict</td>
<td align="right">16,262</td>
<td align="right">2.7%</td>
<td align="right">10,912</td>
<td align="right">2.1%</td>
<td align="right">-32.9%</td>
</tr>
<tr>
<td align="left">tuple</td>
<td align="right">85,142</td>
<td align="right">14.2%</td>
<td align="right">76,001</td>
<td align="right">14.9%</td>
<td align="right">-10.7%</td>
</tr>
<tr>
<td align="left">sequence</td>
<td align="right">9,785</td>
<td align="right">1.6%</td>
<td align="right">9,501</td>
<td align="right">1.9%</td>
<td align="right">-2.9%</td>
</tr>
<tr>
<td align="left">set</td>
<td align="right">9,446</td>
<td align="right">1.6%</td>
<td align="right">9,451</td>
<td align="right">1.8%</td>
<td align="right">0.1%</td>
</tr>
<tr>
<td align="left">mapping</td>
<td align="right">71,789</td>
<td align="right">12.0%</td>
<td align="right">71,785</td>
<td align="right">14.0%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">number</td>
<td align="right">263,021</td>
<td align="right">43.9%</td>
<td align="right">263,026</td>
<td align="right">51.4%</td>
<td align="right">0.0%</td>
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
<td align="right">84</td>
<td align="right">0.0%</td>
<td align="right">84</td>
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
<td align="right">1,244,415,219</td>
<td align="right">99.9%</td>
<td align="right">669,877,674</td>
<td align="right">99.8%</td>
<td align="right">-46.2%</td>
</tr>
<tr>
<td align="left">
deferred
<details>
<summary>ⓘ</summary>

Lists the number of "deferred" (i.e. not specialized) instructions executed.
</details>
</td>
<td align="right">1,568,877</td>
<td align="right">0.1%</td>
<td align="right">1,204,414</td>
<td align="right">0.2%</td>
<td align="right">-23.2%</td>
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
<td align="right">860</td>
<td align="right">8.1%</td>
<td align="right">740</td>
<td align="right">7.0%</td>
<td align="right">-14.0%</td>
</tr>
<tr>
<td align="left">Success</td>
<td align="right">9,794</td>
<td align="right">91.9%</td>
<td align="right">9,806</td>
<td align="right">93.0%</td>
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
<td align="left">sequence</td>
<td align="right">629</td>
<td align="right">73.1%</td>
<td align="right">509</td>
<td align="right">68.8%</td>
<td align="right">-19.1%</td>
</tr>
<tr>
<td align="left">iterator</td>
<td align="right">132</td>
<td align="right">15.3%</td>
<td align="right">132</td>
<td align="right">17.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">other</td>
<td align="right">99</td>
<td align="right">11.5%</td>
<td align="right">99</td>
<td align="right">13.4%</td>
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
<td align="right">8,285,262,588</td>
<td align="right">3.9%</td>
<td align="right">3,247,590,443</td>
<td align="right">3.2%</td>
<td align="right">-60.8%</td>
</tr>
<tr>
<td align="left">
Specialized hits
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that complete.
</details>
</td>
<td align="right">80,507,922,571</td>
<td align="right">37.5%</td>
<td align="right">36,743,468,360</td>
<td align="right">36.1%</td>
<td align="right">-54.4%</td>
</tr>
<tr>
<td align="left">
Basic
<details>
<summary>ⓘ</summary>

Instructions that are not and cannot be specialized, e.g. `LOAD_FAST`.
</details>
</td>
<td align="right">124,346,572,956</td>
<td align="right">57.9%</td>
<td align="right">60,720,560,859</td>
<td align="right">59.6%</td>
<td align="right">-51.2%</td>
</tr>
<tr>
<td align="left">
Specialized misses
<details>
<summary>ⓘ</summary>

Specialized instructions, e.g. `LOAD_ATTR_MODULE` that deopt.
</details>
</td>
<td align="right">1,514,659,733</td>
<td align="right">0.7%</td>
<td align="right">1,085,234,134</td>
<td align="right">1.1%</td>
<td align="right">-28.4%</td>
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
<td align="right">1,505,198,136</td>
<td align="right">20.4%</td>
<td align="right">217,057,196</td>
<td align="right">7.6%</td>
<td align="right">-85.6%</td>
</tr>
<tr>
<td align="left">STORE_SUBSCR</td>
<td align="right">691,400,504</td>
<td align="right">9.4%</td>
<td align="right">103,550,008</td>
<td align="right">3.6%</td>
<td align="right">-85.0%</td>
</tr>
<tr>
<td align="left">COMPARE_OP</td>
<td align="right">506,267,957</td>
<td align="right">6.9%</td>
<td align="right">95,716,746</td>
<td align="right">3.4%</td>
<td align="right">-81.1%</td>
</tr>
<tr>
<td align="left">BINARY_SLICE</td>
<td align="right">525,657,803</td>
<td align="right">7.1%</td>
<td align="right">186,089,293</td>
<td align="right">6.5%</td>
<td align="right">-64.6%</td>
</tr>
<tr>
<td align="left">BINARY_OP</td>
<td align="right">2,357,258,998</td>
<td align="right">31.9%</td>
<td align="right">1,078,979,944</td>
<td align="right">37.9%</td>
<td align="right">-54.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL</td>
<td align="right">256,268,197</td>
<td align="right">3.5%</td>
<td align="right">136,070,434</td>
<td align="right">4.8%</td>
<td align="right">-46.9%</td>
</tr>
<tr>
<td align="left">CONTAINS_OP</td>
<td align="right">200,679,960</td>
<td align="right">2.7%</td>
<td align="right">114,079,731</td>
<td align="right">4.0%</td>
<td align="right">-43.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR</td>
<td align="right">821,701,189</td>
<td align="right">11.1%</td>
<td align="right">548,049,614</td>
<td align="right">19.2%</td>
<td align="right">-33.3%</td>
</tr>
<tr>
<td align="left">CALL</td>
<td align="right">188,200,455</td>
<td align="right">2.6%</td>
<td align="right">160,786,000</td>
<td align="right">5.6%</td>
<td align="right">-14.6%</td>
</tr>
<tr>
<td align="left">SEND</td>
<td align="right">128,406,370</td>
<td align="right">1.7%</td>
<td align="right">128,391,290</td>
<td align="right">4.5%</td>
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
<td align="left">FOR_ITER_TUPLE</td>
<td align="right">81,874,545</td>
<td align="right">5.4%</td>
<td align="right">27,754,511</td>
<td align="right">2.6%</td>
<td align="right">-66.1%</td>
</tr>
<tr>
<td align="left">FOR_ITER_LIST</td>
<td align="right">81,987,554</td>
<td align="right">5.4%</td>
<td align="right">27,797,482</td>
<td align="right">2.6%</td>
<td align="right">-66.1%</td>
</tr>
<tr>
<td align="left">TO_BOOL_ALWAYS_TRUE</td>
<td align="right">49,055,933</td>
<td align="right">3.2%</td>
<td align="right">28,366,102</td>
<td align="right">2.6%</td>
<td align="right">-42.2%</td>
</tr>
<tr>
<td align="left">TO_BOOL_NONE</td>
<td align="right">54,600,773</td>
<td align="right">3.6%</td>
<td align="right">32,518,447</td>
<td align="right">3.0%</td>
<td align="right">-40.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_INSTANCE_VALUE</td>
<td align="right">369,061,221</td>
<td align="right">24.4%</td>
<td align="right">227,168,860</td>
<td align="right">20.9%</td>
<td align="right">-38.4%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_METHOD_WITH_VALUES</td>
<td align="right">268,643,009</td>
<td align="right">17.7%</td>
<td align="right">177,991,870</td>
<td align="right">16.4%</td>
<td align="right">-33.7%</td>
</tr>
<tr>
<td align="left">CALL_PY_EXACT_ARGS</td>
<td align="right">84,583,205</td>
<td align="right">5.6%</td>
<td align="right">57,694,255</td>
<td align="right">5.3%</td>
<td align="right">-31.8%</td>
</tr>
<tr>
<td align="left">STORE_ATTR_INSTANCE_VALUE</td>
<td align="right">95,065,142</td>
<td align="right">6.3%</td>
<td align="right">90,187,557</td>
<td align="right">8.3%</td>
<td align="right">-5.1%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_SLOT</td>
<td align="right">89,829,584</td>
<td align="right">5.9%</td>
<td align="right">87,872,181</td>
<td align="right">8.1%</td>
<td align="right">-2.2%</td>
</tr>
<tr>
<td align="left">LOAD_ATTR_NONDESCRIPTOR_WITH_VALUES</td>
<td align="right">82,487,728</td>
<td align="right">5.4%</td>
<td align="right">81,828,030</td>
<td align="right">7.5%</td>
<td align="right">-0.8%</td>
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
<td align="left">Calls via PyEval_EvalFrame (method)</td>
<td align="right">141,112,765</td>
<td align="right">2.0%</td>
<td align="right">132,513,832</td>
<td align="right">1.9%</td>
<td align="right">-6.1%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function vectorcall)</td>
<td align="right">1,013,031,771</td>
<td align="right">14.5%</td>
<td align="right">1,004,395,158</td>
<td align="right">14.5%</td>
<td align="right">-0.9%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (vector)</td>
<td align="right">1,017,308,438</td>
<td align="right">14.6%</td>
<td align="right">1,008,671,825</td>
<td align="right">14.5%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Frames pushed</td>
<td align="right">5,673,128,293</td>
<td align="right">81.4%</td>
<td align="right">5,638,007,932</td>
<td align="right">81.3%</td>
<td align="right">-0.6%</td>
</tr>
<tr>
<td align="left">Calls to Python functions inlined</td>
<td align="right">5,341,324,119</td>
<td align="right">76.6%</td>
<td align="right">5,312,472,885</td>
<td align="right">76.6%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Calls to PyEval_EvalDefault</td>
<td align="right">1,631,206,343</td>
<td align="right">23.4%</td>
<td align="right">1,622,549,659</td>
<td align="right">23.4%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (total)</td>
<td align="right">1,631,206,343</td>
<td align="right">23.4%</td>
<td align="right">1,622,549,659</td>
<td align="right">23.4%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (api)</td>
<td align="right">270,647,130</td>
<td align="right">3.9%</td>
<td align="right">270,632,571</td>
<td align="right">3.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (generator)</td>
<td align="right">613,897,905</td>
<td align="right">8.8%</td>
<td align="right">613,877,834</td>
<td align="right">8.9%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (function ex)</td>
<td align="right">24,435,419</td>
<td align="right">0.4%</td>
<td align="right">24,434,682</td>
<td align="right">0.4%</td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Frame objects created</td>
<td align="right">70,981,662</td>
<td align="right">1.0%</td>
<td align="right">70,982,116</td>
<td align="right">1.0%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (slot)</td>
<td align="right">260,362,207</td>
<td align="right">3.7%</td>
<td align="right">260,362,277</td>
<td align="right">3.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (legacy)</td>
<td align="right">4,273,295</td>
<td align="right">0.1%</td>
<td align="right">4,273,295</td>
<td align="right">0.1%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Calls via PyEval_EvalFrame (build class)</td>
<td align="right">3,372</td>
<td align="right">0.0%</td>
<td align="right">3,372</td>
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
<td align="right">6,873,269</td>
<td align="right"></td>
<td align="right">27,003,360</td>
<td align="right"></td>
<td align="right">292.9%</td>
</tr>
<tr>
<td align="left">Method cache collisions</td>
<td align="right">61,465,602</td>
<td align="right"></td>
<td align="right">80,039,182</td>
<td align="right"></td>
<td align="right">30.2%</td>
</tr>
<tr>
<td align="left">Method cache hits</td>
<td align="right">2,436,421,823</td>
<td align="right"></td>
<td align="right">2,236,566,510</td>
<td align="right"></td>
<td align="right">-8.2%</td>
</tr>
<tr>
<td align="left">Method cache misses</td>
<td align="right">55,396,537</td>
<td align="right"></td>
<td align="right">53,838,440</td>
<td align="right"></td>
<td align="right">-2.8%</td>
</tr>
<tr>
<td align="left">Interpreter immortal decrefs</td>
<td align="right">1,942,253,191</td>
<td align="right">1.8%</td>
<td align="right">1,897,936,469</td>
<td align="right">1.7%</td>
<td align="right">-2.3%</td>
</tr>
<tr>
<td align="left">Immortal increfs</td>
<td align="right">23,065,695,961</td>
<td align="right">24.9%</td>
<td align="right">22,765,565,745</td>
<td align="right">24.6%</td>
<td align="right">-1.3%</td>
</tr>
<tr>
<td align="left">Method cache dunder hits</td>
<td align="right">2,437,264,220</td>
<td align="right"></td>
<td align="right">2,409,829,381</td>
<td align="right"></td>
<td align="right">-1.1%</td>
</tr>
<tr>
<td align="left">Interpreter mortal increfs</td>
<td align="right">40,071,116,507</td>
<td align="right">43.2%</td>
<td align="right">40,516,318,134</td>
<td align="right">43.7%</td>
<td align="right">1.1%</td>
</tr>
<tr>
<td align="left">Immortal decrefs</td>
<td align="right">24,962,504,941</td>
<td align="right">22.8%</td>
<td align="right">24,752,740,120</td>
<td align="right">22.6%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Interpreter immortal increfs</td>
<td align="right">4,754,224,786</td>
<td align="right">5.1%</td>
<td align="right">4,714,418,615</td>
<td align="right">5.1%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Mortal increfs</td>
<td align="right">24,903,260,854</td>
<td align="right">26.8%</td>
<td align="right">24,698,458,413</td>
<td align="right">26.6%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Allocations from freelist</td>
<td align="right">13,512,495,335</td>
<td align="right">70.7%</td>
<td align="right">13,410,425,160</td>
<td align="right">70.6%</td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Frees to freelist</td>
<td align="right">13,512,680,388</td>
<td align="right"></td>
<td align="right">13,410,612,403</td>
<td align="right"></td>
<td align="right">-0.8%</td>
</tr>
<tr>
<td align="left">Interpreter mortal decrefs</td>
<td align="right">51,239,438,281</td>
<td align="right">46.7%</td>
<td align="right">51,521,974,338</td>
<td align="right">47.0%</td>
<td align="right">0.6%</td>
</tr>
<tr>
<td align="left">Mortal decrefs</td>
<td align="right">31,526,930,370</td>
<td align="right">28.7%</td>
<td align="right">31,367,020,053</td>
<td align="right">28.6%</td>
<td align="right">-0.5%</td>
</tr>
<tr>
<td align="left">Allocations to 512 bytes</td>
<td align="right">5,525,335,848</td>
<td align="right">28.9%</td>
<td align="right">5,504,831,841</td>
<td align="right">29.0%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Allocations</td>
<td align="right">5,603,518,888</td>
<td align="right">29.3%</td>
<td align="right">5,583,024,989</td>
<td align="right">29.4%</td>
<td align="right">-0.4%</td>
</tr>
<tr>
<td align="left">Frees</td>
<td align="right">6,184,768,634</td>
<td align="right"></td>
<td align="right">6,164,913,964</td>
<td align="right"></td>
<td align="right">-0.3%</td>
</tr>
<tr>
<td align="left">Allocations over 4 kbytes</td>
<td align="right">6,700,390</td>
<td align="right">0.0%</td>
<td align="right">6,695,636</td>
<td align="right">0.0%</td>
<td align="right">-0.1%</td>
</tr>
<tr>
<td align="left">Allocations to 4 kbytes</td>
<td align="right">71,482,650</td>
<td align="right">0.4%</td>
<td align="right">71,497,512</td>
<td align="right">0.4%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Inline values</td>
<td align="right">190,785,125</td>
<td align="right"></td>
<td align="right">190,764,665</td>
<td align="right"></td>
<td align="right">-0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (on request)</td>
<td align="right">3,386,403</td>
<td align="right">1.8%</td>
<td align="right">3,386,403</td>
<td align="right">1.8%</td>
<td align="right">0.0%</td>
</tr>
<tr>
<td align="left">Materialize dict (new key)</td>
<td align="right">306,669</td>
<td align="right">0.2%</td>
<td align="right">306,669</td>
<td align="right">0.2%</td>
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
<td align="right">359,145</td>
<td align="right">103,802,567</td>
<td align="right">9,627,763,093</td>
<td align="right">782,281,660</td>
<td align="right">756,116,917</td>
<td align="right">358,289</td>
<td align="right">104,072,414</td>
<td align="right">9,615,567,075</td>
<td align="right">784,360,658</td>
<td align="right">754,504,046</td>
</tr>
<tr>
<td align="right">2</td>
<td align="right">15,998</td>
<td align="right">8,734,500</td>
<td align="right">11,360,884,992</td>
<td align="right">0</td>
<td align="right">0</td>
<td align="right">15,998</td>
<td align="right">8,734,500</td>
<td align="right">11,361,360,088</td>
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
<td align="right">29</td>
<td align="right">29</td>
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
<td align="right">120</td>
<td align="right">120 / 0 !!</td>
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
<td align="right">120</td>
<td align="right">120 / 0 !!</td>
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
<td align="right">2,435</td>
<td align="right">2,435</td>
<td align="right">0.0%</td>
</tr>
</tbody>
</table>


</details>

---
Stats gathered on: 2025-06-08
