# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 0e50451
- commit date: 2024-11-08
- overall geometric mean: 1.44x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.33x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 656 ms: 1.47x slower                                                  |
| docutils       | 4.01 sec                                                     | 4.56 sec: 1.14x slower                                                |
| html5lib       | 92.6 ms                                                      | 141 ms: 1.52x slower                                                  |
| Geometric mean | (ref)                                                        | 1.37x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|--------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets | 766 ms                                                       | 732 ms: 1.05x faster                                                  |
| asyncio_tcp        | 948 ms                                                       | 1.08 sec: 1.14x slower                                                |
| asyncio_tcp_ssl    | 2.77 sec                                                     | 3.21 sec: 1.16x slower                                                |
| async_generators   | 567 ms                                                       | 706 ms: 1.24x slower                                                  |
| coroutines         | 30.9 ms                                                      | 41.5 ms: 1.35x slower                                                 |
| Geometric mean     | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 271 ms: 1.08x slower                                                  |
| float          | 116 ms                                                       | 188 ms: 1.62x slower                                                  |
| nbody          | 119 ms                                                       | 266 ms: 2.24x slower                                                  |
| Geometric mean | (ref)                                                        | 1.58x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 299 ms: 1.06x slower                                                  |
| regex_effbot   | 4.74 ms                                                      | 5.14 ms: 1.09x slower                                                 |
| regex_v8       | 32.8 ms                                                      | 36.2 ms: 1.10x slower                                                 |
| regex_compile  | 182 ms                                                       | 290 ms: 1.59x slower                                                  |
| Geometric mean | (ref)                                                        | 1.19x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 231 ms                                                       | 216 ms: 1.07x faster                                                  |
| unpickle             | 20.5 us                                                      | 21.6 us: 1.05x slower                                                 |
| pickle               | 15.1 us                                                      | 17.4 us: 1.15x slower                                                 |
| unpickle_list        | 6.68 us                                                      | 8.36 us: 1.25x slower                                                 |
| json_loads           | 34.3 us                                                      | 43.1 us: 1.26x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 157 ms: 1.28x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 19.4 ms: 1.37x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 122 ms: 1.42x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 4.03 sec: 1.45x slower                                                |
| pickle_pure_python   | 416 us                                                       | 759 us: 1.82x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 530 us: 1.83x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                          |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_dict, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 29.8 ms: 1.33x slower                                                 |
| python_startup_no_site | 15.3 ms                                                      | 20.9 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 109 ms: 1.51x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 50.7 ms: 1.60x slower                                                 |
| django_template | 44.3 ms                                                      | 75.9 ms: 1.71x slower                                                 |
| mako            | 15.9 ms                                                      | 30.1 ms: 1.89x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.67x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|--------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal             | 5.70 ms                                                      | 4.09 ms: 1.39x faster                                                 |
| create_gc_cycles         | 2.41 ms                                                      | 2.02 ms: 1.19x faster                                                 |
| xml_etree_parse          | 231 ms                                                       | 216 ms: 1.07x faster                                                  |
| asyncio_websockets       | 766 ms                                                       | 732 ms: 1.05x faster                                                  |
| unpickle                 | 20.5 us                                                      | 21.6 us: 1.05x slower                                                 |
| regex_dna                | 282 ms                                                       | 299 ms: 1.06x slower                                                  |
| telco                    | 12.2 ms                                                      | 13.0 ms: 1.07x slower                                                 |
| pidigits                 | 251 ms                                                       | 271 ms: 1.08x slower                                                  |
| regex_effbot             | 4.74 ms                                                      | 5.14 ms: 1.09x slower                                                 |
| regex_v8                 | 32.8 ms                                                      | 36.2 ms: 1.10x slower                                                 |
| pathlib                  | 29.9 ms                                                      | 34.0 ms: 1.14x slower                                                 |
| docutils                 | 4.01 sec                                                     | 4.56 sec: 1.14x slower                                                |
| asyncio_tcp              | 948 ms                                                       | 1.08 sec: 1.14x slower                                                |
| json                     | 6.51 ms                                                      | 7.43 ms: 1.14x slower                                                 |
| pickle                   | 15.1 us                                                      | 17.4 us: 1.15x slower                                                 |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.21 sec: 1.16x slower                                                |
| pylint                   | 470 ms                                                       | 547 ms: 1.16x slower                                                  |
| scimark_fft              | 473 ms                                                       | 569 ms: 1.20x slower                                                  |
| meteor_contest           | 150 ms                                                       | 182 ms: 1.21x slower                                                  |
| async_generators         | 567 ms                                                       | 706 ms: 1.24x slower                                                  |
| unpickle_list            | 6.68 us                                                      | 8.36 us: 1.25x slower                                                 |
| deepcopy_reduce          | 4.10 us                                                      | 5.15 us: 1.26x slower                                                 |
| json_loads               | 34.3 us                                                      | 43.1 us: 1.26x slower                                                 |
| xml_etree_generate       | 122 ms                                                       | 157 ms: 1.28x slower                                                  |
| deepcopy_memo            | 50.1 us                                                      | 64.9 us: 1.29x slower                                                 |
| mdp                      | 3.80 sec                                                     | 4.98 sec: 1.31x slower                                                |
| python_startup           | 22.4 ms                                                      | 29.8 ms: 1.33x slower                                                 |
| coroutines               | 30.9 ms                                                      | 41.5 ms: 1.35x slower                                                 |
| coverage                 | 107 ms                                                       | 145 ms: 1.35x slower                                                  |
| bench_thread_pool        | 2.89 ms                                                      | 3.89 ms: 1.35x slower                                                 |
| python_startup_no_site   | 15.3 ms                                                      | 20.9 ms: 1.36x slower                                                 |
| pycparser                | 1.57 sec                                                     | 2.14 sec: 1.36x slower                                                |
| json_dumps               | 14.1 ms                                                      | 19.4 ms: 1.37x slower                                                 |
| nqueens                  | 112 ms                                                       | 154 ms: 1.38x slower                                                  |
| generators               | 40.0 ms                                                      | 56.1 ms: 1.40x slower                                                 |
| typing_runtime_protocols | 226 us                                                       | 318 us: 1.41x slower                                                  |
| sympy_integrate          | 30.2 ms                                                      | 42.6 ms: 1.41x slower                                                 |
| dulwich_log              | 93.7 ms                                                      | 132 ms: 1.41x slower                                                  |
| fannkuch                 | 547 ms                                                       | 775 ms: 1.42x slower                                                  |
| xml_etree_process        | 85.9 ms                                                      | 122 ms: 1.42x slower                                                  |
| bpe_tokeniser            | 6.28 sec                                                     | 8.96 sec: 1.43x slower                                                |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 9.71 ms: 1.44x slower                                                 |
| tomli_loads              | 2.78 sec                                                     | 4.03 sec: 1.45x slower                                                |
| spectral_norm            | 157 ms                                                       | 228 ms: 1.46x slower                                                  |
| 2to3                     | 445 ms                                                       | 656 ms: 1.47x slower                                                  |
| sqlglot_normalize        | 140 ms                                                       | 207 ms: 1.48x slower                                                  |
| sqlglot_optimize         | 74.7 ms                                                      | 112 ms: 1.50x slower                                                  |
| genshi_xml               | 72.1 ms                                                      | 109 ms: 1.51x slower                                                  |
| crypto_pyaes             | 100 ms                                                       | 151 ms: 1.51x slower                                                  |
| thrift                   | 1.10 ms                                                      | 1.67 ms: 1.52x slower                                                 |
| html5lib                 | 92.6 ms                                                      | 141 ms: 1.52x slower                                                  |
| pprint_safe_repr         | 987 ms                                                       | 1.51 sec: 1.53x slower                                                |
| richards                 | 65.5 ms                                                      | 101 ms: 1.54x slower                                                  |
| pprint_pformat           | 1.94 sec                                                     | 3.04 sec: 1.57x slower                                                |
| pyflate                  | 664 ms                                                       | 1.04 sec: 1.57x slower                                                |
| regex_compile            | 182 ms                                                       | 290 ms: 1.59x slower                                                  |
| genshi_text              | 31.7 ms                                                      | 50.7 ms: 1.60x slower                                                 |
| float                    | 116 ms                                                       | 188 ms: 1.62x slower                                                  |
| sympy_str                | 379 ms                                                       | 630 ms: 1.66x slower                                                  |
| django_template          | 44.3 ms                                                      | 75.9 ms: 1.71x slower                                                 |
| scimark_monte_carlo      | 90.6 ms                                                      | 155 ms: 1.72x slower                                                  |
| logging_simple           | 8.56 us                                                      | 14.8 us: 1.73x slower                                                 |
| comprehensions           | 22.2 us                                                      | 39.2 us: 1.76x slower                                                 |
| scimark_lu               | 146 ms                                                       | 265 ms: 1.81x slower                                                  |
| pickle_pure_python       | 416 us                                                       | 759 us: 1.82x slower                                                  |
| unpickle_pure_python     | 290 us                                                       | 530 us: 1.83x slower                                                  |
| richards_super           | 73.2 ms                                                      | 137 ms: 1.87x slower                                                  |
| logging_format           | 9.24 us                                                      | 17.3 us: 1.87x slower                                                 |
| go                       | 191 ms                                                       | 361 ms: 1.89x slower                                                  |
| mako                     | 15.9 ms                                                      | 30.1 ms: 1.89x slower                                                 |
| hexiom                   | 8.11 ms                                                      | 15.5 ms: 1.91x slower                                                 |
| chaos                    | 83.6 ms                                                      | 160 ms: 1.91x slower                                                  |
| scimark_sor              | 179 ms                                                       | 342 ms: 1.91x slower                                                  |
| sympy_expand             | 601 ms                                                       | 1.20 sec: 2.00x slower                                                |
| logging_silent           | 130 ns                                                       | 267 ns: 2.06x slower                                                  |
| sqlglot_transpile        | 2.20 ms                                                      | 4.61 ms: 2.10x slower                                                 |
| sympy_sum                | 210 ms                                                       | 446 ms: 2.12x slower                                                  |
| sqlglot_parse            | 1.76 ms                                                      | 3.79 ms: 2.16x slower                                                 |
| raytrace                 | 344 ms                                                       | 754 ms: 2.19x slower                                                  |
| nbody                    | 119 ms                                                       | 266 ms: 2.24x slower                                                  |
| deltablue                | 4.44 ms                                                      | 11.3 ms: 2.53x slower                                                 |
| unpack_sequence          | 74.3 ns                                                      | 190 ns: 2.56x slower                                                  |
| bench_mp_pool            | 18.7 ms                                                      | 64.3 ms: 3.44x slower                                                 |
| Geometric mean           | (ref)                                                        | 1.44x slower                                                          |

Benchmark hidden because not significant (5): xml_etree_iterparse, pickle_dict, pickle_list, sqlite_synth, deepcopy
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.39x
- 95% likely to have a slowdown of 1.38x
- 99% likely to have a slowdown of 1.33x

# Memory
- memory change: 1.19x