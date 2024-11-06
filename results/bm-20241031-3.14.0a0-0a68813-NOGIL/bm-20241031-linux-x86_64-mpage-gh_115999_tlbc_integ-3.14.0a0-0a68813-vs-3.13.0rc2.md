# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_integ
- machine: linux-x86_64
- commit hash: 0a68813
- commit date: 2024-10-31
- overall geometric mean: 1.49x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.38x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 688 ms: 1.55x slower                                                 |
| docutils       | 4.01 sec                                                     | 4.88 sec: 1.22x slower                                               |
| html5lib       | 92.6 ms                                                      | 146 ms: 1.58x slower                                                 |
| tornado_http   | 251 ms                                                       | 332 ms: 1.32x slower                                                 |
| Geometric mean | (ref)                                                        | 1.41x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_tcp        | 948 ms                                                       | 1.08 sec: 1.13x slower                                               |
| asyncio_tcp_ssl    | 2.77 sec                                                     | 3.21 sec: 1.16x slower                                               |
| async_generators   | 567 ms                                                       | 735 ms: 1.30x slower                                                 |
| coroutines         | 30.9 ms                                                      | 40.4 ms: 1.31x slower                                                |
| asyncio_websockets | 766 ms                                                       | 1.02 sec: 1.33x slower                                               |
| Geometric mean     | (ref)                                                        | 1.24x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 237 ms: 1.06x faster                                                 |
| float          | 116 ms                                                       | 216 ms: 1.86x slower                                                 |
| nbody          | 119 ms                                                       | 309 ms: 2.60x slower                                                 |
| Geometric mean | (ref)                                                        | 1.66x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 298 ms: 1.06x slower                                                 |
| regex_effbot   | 4.74 ms                                                      | 5.16 ms: 1.09x slower                                                |
| regex_v8       | 32.8 ms                                                      | 35.9 ms: 1.10x slower                                                |
| regex_compile  | 182 ms                                                       | 311 ms: 1.71x slower                                                 |
| Geometric mean | (ref)                                                        | 1.21x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_list          | 6.86 us                                                      | 5.97 us: 1.15x faster                                                |
| pickle_dict          | 47.2 us                                                      | 43.4 us: 1.09x faster                                                |
| pickle               | 15.1 us                                                      | 16.0 us: 1.06x slower                                                |
| unpickle_list        | 6.68 us                                                      | 8.31 us: 1.24x slower                                                |
| unpickle             | 20.5 us                                                      | 25.7 us: 1.25x slower                                                |
| json_loads           | 34.3 us                                                      | 43.0 us: 1.26x slower                                                |
| xml_etree_generate   | 122 ms                                                       | 165 ms: 1.35x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 20.4 ms: 1.44x slower                                                |
| xml_etree_process    | 85.9 ms                                                      | 128 ms: 1.49x slower                                                 |
| tomli_loads          | 2.78 sec                                                     | 4.33 sec: 1.56x slower                                               |
| unpickle_pure_python | 290 us                                                       | 521 us: 1.79x slower                                                 |
| pickle_pure_python   | 416 us                                                       | 769 us: 1.85x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                         |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.4 ms: 1.27x slower                                                |
| python_startup         | 22.4 ms                                                      | 29.2 ms: 1.30x slower                                                |
| Geometric mean         | (ref)                                                        | 1.28x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 117 ms: 1.63x slower                                                 |
| django_template | 44.3 ms                                                      | 83.1 ms: 1.88x slower                                                |
| mako            | 15.9 ms                                                      | 30.6 ms: 1.92x slower                                                |
| genshi_text     | 31.7 ms                                                      | 62.1 ms: 1.96x slower                                                |
| Geometric mean  | (ref)                                                        | 1.84x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| create_gc_cycles         | 2.41 ms                                                      | 1.93 ms: 1.25x faster                                                |
| pickle_list              | 6.86 us                                                      | 5.97 us: 1.15x faster                                                |
| gc_traversal             | 5.70 ms                                                      | 5.04 ms: 1.13x faster                                                |
| pickle_dict              | 47.2 us                                                      | 43.4 us: 1.09x faster                                                |
| pidigits                 | 251 ms                                                       | 237 ms: 1.06x faster                                                 |
| pickle                   | 15.1 us                                                      | 16.0 us: 1.06x slower                                                |
| regex_dna                | 282 ms                                                       | 298 ms: 1.06x slower                                                 |
| sqlite_synth             | 3.99 us                                                      | 4.23 us: 1.06x slower                                                |
| regex_effbot             | 4.74 ms                                                      | 5.16 ms: 1.09x slower                                                |
| regex_v8                 | 32.8 ms                                                      | 35.9 ms: 1.10x slower                                                |
| deepcopy                 | 498 us                                                       | 555 us: 1.12x slower                                                 |
| asyncio_tcp              | 948 ms                                                       | 1.08 sec: 1.13x slower                                               |
| pathlib                  | 29.9 ms                                                      | 34.3 ms: 1.15x slower                                                |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.21 sec: 1.16x slower                                               |
| telco                    | 12.2 ms                                                      | 14.1 ms: 1.16x slower                                                |
| scimark_fft              | 473 ms                                                       | 564 ms: 1.19x slower                                                 |
| docutils                 | 4.01 sec                                                     | 4.88 sec: 1.22x slower                                               |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 8.27 ms: 1.22x slower                                                |
| pylint                   | 470 ms                                                       | 577 ms: 1.23x slower                                                 |
| unpickle_list            | 6.68 us                                                      | 8.31 us: 1.24x slower                                                |
| unpickle                 | 20.5 us                                                      | 25.7 us: 1.25x slower                                                |
| json_loads               | 34.3 us                                                      | 43.0 us: 1.26x slower                                                |
| python_startup_no_site   | 15.3 ms                                                      | 19.4 ms: 1.27x slower                                                |
| json                     | 6.51 ms                                                      | 8.26 ms: 1.27x slower                                                |
| bench_thread_pool        | 2.89 ms                                                      | 3.71 ms: 1.29x slower                                                |
| async_generators         | 567 ms                                                       | 735 ms: 1.30x slower                                                 |
| python_startup           | 22.4 ms                                                      | 29.2 ms: 1.30x slower                                                |
| coroutines               | 30.9 ms                                                      | 40.4 ms: 1.31x slower                                                |
| coverage                 | 107 ms                                                       | 141 ms: 1.32x slower                                                 |
| tornado_http             | 251 ms                                                       | 332 ms: 1.32x slower                                                 |
| asyncio_websockets       | 766 ms                                                       | 1.02 sec: 1.33x slower                                               |
| meteor_contest           | 150 ms                                                       | 200 ms: 1.33x slower                                                 |
| xml_etree_generate       | 122 ms                                                       | 165 ms: 1.35x slower                                                 |
| deepcopy_memo            | 50.1 us                                                      | 67.9 us: 1.35x slower                                                |
| mdp                      | 3.80 sec                                                     | 5.15 sec: 1.36x slower                                               |
| fannkuch                 | 547 ms                                                       | 766 ms: 1.40x slower                                                 |
| nqueens                  | 112 ms                                                       | 158 ms: 1.41x slower                                                 |
| deepcopy_reduce          | 4.10 us                                                      | 5.79 us: 1.41x slower                                                |
| json_dumps               | 14.1 ms                                                      | 20.4 ms: 1.44x slower                                                |
| generators               | 40.0 ms                                                      | 58.8 ms: 1.47x slower                                                |
| bpe_tokeniser            | 6.28 sec                                                     | 9.26 sec: 1.47x slower                                               |
| spectral_norm            | 157 ms                                                       | 231 ms: 1.47x slower                                                 |
| sympy_integrate          | 30.2 ms                                                      | 44.6 ms: 1.48x slower                                                |
| dulwich_log              | 93.7 ms                                                      | 139 ms: 1.49x slower                                                 |
| xml_etree_process        | 85.9 ms                                                      | 128 ms: 1.49x slower                                                 |
| crypto_pyaes             | 100 ms                                                       | 154 ms: 1.53x slower                                                 |
| typing_runtime_protocols | 226 us                                                       | 347 us: 1.54x slower                                                 |
| 2to3                     | 445 ms                                                       | 688 ms: 1.55x slower                                                 |
| tomli_loads              | 2.78 sec                                                     | 4.33 sec: 1.56x slower                                               |
| pycparser                | 1.57 sec                                                     | 2.45 sec: 1.56x slower                                               |
| pprint_safe_repr         | 987 ms                                                       | 1.55 sec: 1.57x slower                                               |
| html5lib                 | 92.6 ms                                                      | 146 ms: 1.58x slower                                                 |
| thrift                   | 1.10 ms                                                      | 1.74 ms: 1.59x slower                                                |
| sqlglot_optimize         | 74.7 ms                                                      | 119 ms: 1.59x slower                                                 |
| pyflate                  | 664 ms                                                       | 1.08 sec: 1.62x slower                                               |
| genshi_xml               | 72.1 ms                                                      | 117 ms: 1.63x slower                                                 |
| sqlglot_normalize        | 140 ms                                                       | 229 ms: 1.64x slower                                                 |
| pprint_pformat           | 1.94 sec                                                     | 3.22 sec: 1.66x slower                                               |
| richards                 | 65.5 ms                                                      | 109 ms: 1.66x slower                                                 |
| scimark_monte_carlo      | 90.6 ms                                                      | 153 ms: 1.69x slower                                                 |
| regex_compile            | 182 ms                                                       | 311 ms: 1.71x slower                                                 |
| sympy_str                | 379 ms                                                       | 660 ms: 1.74x slower                                                 |
| unpickle_pure_python     | 290 us                                                       | 521 us: 1.79x slower                                                 |
| pickle_pure_python       | 416 us                                                       | 769 us: 1.85x slower                                                 |
| float                    | 116 ms                                                       | 216 ms: 1.86x slower                                                 |
| scimark_lu               | 146 ms                                                       | 274 ms: 1.87x slower                                                 |
| django_template          | 44.3 ms                                                      | 83.1 ms: 1.88x slower                                                |
| go                       | 191 ms                                                       | 361 ms: 1.89x slower                                                 |
| richards_super           | 73.2 ms                                                      | 140 ms: 1.91x slower                                                 |
| mako                     | 15.9 ms                                                      | 30.6 ms: 1.92x slower                                                |
| logging_silent           | 130 ns                                                       | 249 ns: 1.92x slower                                                 |
| scimark_sor              | 179 ms                                                       | 344 ms: 1.92x slower                                                 |
| logging_format           | 9.24 us                                                      | 17.9 us: 1.93x slower                                                |
| hexiom                   | 8.11 ms                                                      | 15.7 ms: 1.94x slower                                                |
| genshi_text              | 31.7 ms                                                      | 62.1 ms: 1.96x slower                                                |
| logging_simple           | 8.56 us                                                      | 16.8 us: 1.97x slower                                                |
| chaos                    | 83.6 ms                                                      | 166 ms: 1.99x slower                                                 |
| comprehensions           | 22.2 us                                                      | 45.2 us: 2.03x slower                                                |
| sympy_expand             | 601 ms                                                       | 1.27 sec: 2.11x slower                                               |
| sqlglot_transpile        | 2.20 ms                                                      | 4.70 ms: 2.14x slower                                                |
| raytrace                 | 344 ms                                                       | 744 ms: 2.16x slower                                                 |
| sympy_sum                | 210 ms                                                       | 477 ms: 2.27x slower                                                 |
| sqlglot_parse            | 1.76 ms                                                      | 4.10 ms: 2.33x slower                                                |
| nbody                    | 119 ms                                                       | 309 ms: 2.60x slower                                                 |
| deltablue                | 4.44 ms                                                      | 11.8 ms: 2.66x slower                                                |
| unpack_sequence          | 74.3 ns                                                      | 218 ns: 2.94x slower                                                 |
| bench_mp_pool            | 18.7 ms                                                      | 58.4 ms: 3.12x slower                                                |
| Geometric mean           | (ref)                                                        | 1.49x slower                                                         |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.44x
- 95% likely to have a slowdown of 1.42x
- 99% likely to have a slowdown of 1.38x

# Memory
- memory change: 1.18x