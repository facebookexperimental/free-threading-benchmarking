# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_integ
- machine: linux-x86_64
- commit hash: 0a68813
- commit date: 2024-10-31
- overall geometric mean: 1.51x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.40x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 677 ms: 1.52x slower                                                 |
| docutils       | 4.01 sec                                                     | 4.80 sec: 1.20x slower                                               |
| html5lib       | 92.6 ms                                                      | 149 ms: 1.61x slower                                                 |
| tornado_http   | 251 ms                                                       | 345 ms: 1.37x slower                                                 |
| Geometric mean | (ref)                                                        | 1.42x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_tcp        | 948 ms                                                       | 1.04 sec: 1.10x slower                                               |
| asyncio_tcp_ssl    | 2.77 sec                                                     | 3.30 sec: 1.19x slower                                               |
| async_generators   | 567 ms                                                       | 701 ms: 1.24x slower                                                 |
| coroutines         | 30.9 ms                                                      | 40.1 ms: 1.30x slower                                                |
| asyncio_websockets | 766 ms                                                       | 1.00 sec: 1.31x slower                                               |
| Geometric mean     | (ref)                                                        | 1.22x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 116 ms                                                       | 224 ms: 1.93x slower                                                 |
| nbody          | 119 ms                                                       | 304 ms: 2.56x slower                                                 |
| Geometric mean | (ref)                                                        | 1.69x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 5.20 ms: 1.10x slower                                                |
| regex_v8       | 32.8 ms                                                      | 37.8 ms: 1.15x slower                                                |
| regex_compile  | 182 ms                                                       | 301 ms: 1.65x slower                                                 |
| Geometric mean | (ref)                                                        | 1.20x slower                                                         |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_list          | 6.86 us                                                      | 6.46 us: 1.06x faster                                                |
| unpickle_list        | 6.68 us                                                      | 8.47 us: 1.27x slower                                                |
| xml_etree_generate   | 122 ms                                                       | 159 ms: 1.30x slower                                                 |
| unpickle             | 20.5 us                                                      | 27.2 us: 1.33x slower                                                |
| json_loads           | 34.3 us                                                      | 45.8 us: 1.34x slower                                                |
| json_dumps           | 14.1 ms                                                      | 19.7 ms: 1.40x slower                                                |
| tomli_loads          | 2.78 sec                                                     | 4.24 sec: 1.52x slower                                               |
| xml_etree_process    | 85.9 ms                                                      | 131 ms: 1.53x slower                                                 |
| pickle_pure_python   | 416 us                                                       | 785 us: 1.89x slower                                                 |
| unpickle_pure_python | 290 us                                                       | 566 us: 1.95x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.28x slower                                                         |

Benchmark hidden because not significant (4): pickle_dict, xml_etree_parse, xml_etree_iterparse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.1 ms: 1.25x slower                                                |
| python_startup         | 22.4 ms                                                      | 28.8 ms: 1.29x slower                                                |
| Geometric mean         | (ref)                                                        | 1.27x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 128 ms: 1.77x slower                                                 |
| django_template | 44.3 ms                                                      | 83.0 ms: 1.87x slower                                                |
| genshi_text     | 31.7 ms                                                      | 61.6 ms: 1.95x slower                                                |
| mako            | 15.9 ms                                                      | 31.1 ms: 1.95x slower                                                |
| Geometric mean  | (ref)                                                        | 1.88x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| create_gc_cycles         | 2.41 ms                                                      | 1.94 ms: 1.24x faster                                                |
| gc_traversal             | 5.70 ms                                                      | 4.99 ms: 1.14x faster                                                |
| pickle_list              | 6.86 us                                                      | 6.46 us: 1.06x faster                                                |
| asyncio_tcp              | 948 ms                                                       | 1.04 sec: 1.10x slower                                               |
| regex_effbot             | 4.74 ms                                                      | 5.20 ms: 1.10x slower                                                |
| sqlite_synth             | 3.99 us                                                      | 4.39 us: 1.10x slower                                                |
| pathlib                  | 29.9 ms                                                      | 34.1 ms: 1.14x slower                                                |
| deepcopy                 | 498 us                                                       | 568 us: 1.14x slower                                                 |
| regex_v8                 | 32.8 ms                                                      | 37.8 ms: 1.15x slower                                                |
| bench_thread_pool        | 2.89 ms                                                      | 3.38 ms: 1.17x slower                                                |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.30 sec: 1.19x slower                                               |
| docutils                 | 4.01 sec                                                     | 4.80 sec: 1.20x slower                                               |
| telco                    | 12.2 ms                                                      | 14.9 ms: 1.23x slower                                                |
| async_generators         | 567 ms                                                       | 701 ms: 1.24x slower                                                 |
| python_startup_no_site   | 15.3 ms                                                      | 19.1 ms: 1.25x slower                                                |
| pylint                   | 470 ms                                                       | 594 ms: 1.26x slower                                                 |
| unpickle_list            | 6.68 us                                                      | 8.47 us: 1.27x slower                                                |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 8.57 ms: 1.27x slower                                                |
| scimark_fft              | 473 ms                                                       | 606 ms: 1.28x slower                                                 |
| python_startup           | 22.4 ms                                                      | 28.8 ms: 1.29x slower                                                |
| coroutines               | 30.9 ms                                                      | 40.1 ms: 1.30x slower                                                |
| xml_etree_generate       | 122 ms                                                       | 159 ms: 1.30x slower                                                 |
| asyncio_websockets       | 766 ms                                                       | 1.00 sec: 1.31x slower                                               |
| unpickle                 | 20.5 us                                                      | 27.2 us: 1.33x slower                                                |
| meteor_contest           | 150 ms                                                       | 201 ms: 1.34x slower                                                 |
| json_loads               | 34.3 us                                                      | 45.8 us: 1.34x slower                                                |
| json                     | 6.51 ms                                                      | 8.73 ms: 1.34x slower                                                |
| mdp                      | 3.80 sec                                                     | 5.10 sec: 1.34x slower                                               |
| tornado_http             | 251 ms                                                       | 345 ms: 1.37x slower                                                 |
| json_dumps               | 14.1 ms                                                      | 19.7 ms: 1.40x slower                                                |
| deepcopy_memo            | 50.1 us                                                      | 70.2 us: 1.40x slower                                                |
| fannkuch                 | 547 ms                                                       | 769 ms: 1.41x slower                                                 |
| coverage                 | 107 ms                                                       | 154 ms: 1.43x slower                                                 |
| spectral_norm            | 157 ms                                                       | 226 ms: 1.44x slower                                                 |
| bpe_tokeniser            | 6.28 sec                                                     | 9.16 sec: 1.46x slower                                               |
| typing_runtime_protocols | 226 us                                                       | 330 us: 1.46x slower                                                 |
| nqueens                  | 112 ms                                                       | 164 ms: 1.47x slower                                                 |
| deepcopy_reduce          | 4.10 us                                                      | 6.03 us: 1.47x slower                                                |
| generators               | 40.0 ms                                                      | 60.7 ms: 1.52x slower                                                |
| 2to3                     | 445 ms                                                       | 677 ms: 1.52x slower                                                 |
| tomli_loads              | 2.78 sec                                                     | 4.24 sec: 1.52x slower                                               |
| xml_etree_process        | 85.9 ms                                                      | 131 ms: 1.53x slower                                                 |
| sympy_integrate          | 30.2 ms                                                      | 46.5 ms: 1.54x slower                                                |
| dulwich_log              | 93.7 ms                                                      | 146 ms: 1.56x slower                                                 |
| pprint_safe_repr         | 987 ms                                                       | 1.56 sec: 1.58x slower                                               |
| pyflate                  | 664 ms                                                       | 1.05 sec: 1.58x slower                                               |
| sqlglot_optimize         | 74.7 ms                                                      | 119 ms: 1.59x slower                                                 |
| pycparser                | 1.57 sec                                                     | 2.51 sec: 1.60x slower                                               |
| html5lib                 | 92.6 ms                                                      | 149 ms: 1.61x slower                                                 |
| crypto_pyaes             | 100 ms                                                       | 162 ms: 1.61x slower                                                 |
| regex_compile            | 182 ms                                                       | 301 ms: 1.65x slower                                                 |
| pprint_pformat           | 1.94 sec                                                     | 3.24 sec: 1.67x slower                                               |
| sqlglot_normalize        | 140 ms                                                       | 234 ms: 1.67x slower                                                 |
| thrift                   | 1.10 ms                                                      | 1.86 ms: 1.69x slower                                                |
| scimark_monte_carlo      | 90.6 ms                                                      | 157 ms: 1.73x slower                                                 |
| genshi_xml               | 72.1 ms                                                      | 128 ms: 1.77x slower                                                 |
| sympy_str                | 379 ms                                                       | 682 ms: 1.80x slower                                                 |
| richards                 | 65.5 ms                                                      | 119 ms: 1.81x slower                                                 |
| richards_super           | 73.2 ms                                                      | 134 ms: 1.82x slower                                                 |
| comprehensions           | 22.2 us                                                      | 41.6 us: 1.87x slower                                                |
| django_template          | 44.3 ms                                                      | 83.0 ms: 1.87x slower                                                |
| scimark_sor              | 179 ms                                                       | 335 ms: 1.88x slower                                                 |
| pickle_pure_python       | 416 us                                                       | 785 us: 1.89x slower                                                 |
| chaos                    | 83.6 ms                                                      | 159 ms: 1.90x slower                                                 |
| scimark_lu               | 146 ms                                                       | 279 ms: 1.91x slower                                                 |
| logging_simple           | 8.56 us                                                      | 16.4 us: 1.92x slower                                                |
| logging_format           | 9.24 us                                                      | 17.8 us: 1.93x slower                                                |
| float                    | 116 ms                                                       | 224 ms: 1.93x slower                                                 |
| logging_silent           | 130 ns                                                       | 253 ns: 1.94x slower                                                 |
| genshi_text              | 31.7 ms                                                      | 61.6 ms: 1.95x slower                                                |
| mako                     | 15.9 ms                                                      | 31.1 ms: 1.95x slower                                                |
| unpickle_pure_python     | 290 us                                                       | 566 us: 1.95x slower                                                 |
| hexiom                   | 8.11 ms                                                      | 16.1 ms: 1.98x slower                                                |
| go                       | 191 ms                                                       | 379 ms: 1.98x slower                                                 |
| sympy_expand             | 601 ms                                                       | 1.31 sec: 2.17x slower                                               |
| sympy_sum                | 210 ms                                                       | 469 ms: 2.23x slower                                                 |
| sqlglot_transpile        | 2.20 ms                                                      | 4.99 ms: 2.27x slower                                                |
| raytrace                 | 344 ms                                                       | 783 ms: 2.28x slower                                                 |
| sqlglot_parse            | 1.76 ms                                                      | 4.27 ms: 2.43x slower                                                |
| nbody                    | 119 ms                                                       | 304 ms: 2.56x slower                                                 |
| deltablue                | 4.44 ms                                                      | 12.0 ms: 2.70x slower                                                |
| unpack_sequence          | 74.3 ns                                                      | 213 ns: 2.87x slower                                                 |
| bench_mp_pool            | 18.7 ms                                                      | 58.4 ms: 3.13x slower                                                |
| Geometric mean           | (ref)                                                        | 1.51x slower                                                         |

Benchmark hidden because not significant (6): pickle_dict, xml_etree_parse, pidigits, xml_etree_iterparse, regex_dna, pickle
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.45x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.40x

# Memory
- memory change: 1.18x