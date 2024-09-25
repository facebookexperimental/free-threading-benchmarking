# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_thread_loc
- machine: linux-x86_64
- commit hash: d8a840b
- commit date: 2024-09-03
- overall geometric mean: 1.44x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 698 ms: 1.57x slower                                                 |
| docutils       | 4.01 sec                                                     | 4.84 sec: 1.21x slower                                               |
| html5lib       | 92.6 ms                                                      | 142 ms: 1.53x slower                                                 |
| tornado_http   | 251 ms                                                       | 399 ms: 1.59x slower                                                 |
| Geometric mean | (ref)                                                        | 1.47x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|-------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg        | 1.40 sec                                                     | 1.15 sec: 1.21x faster                                               |
| async_tree_io           | 1.39 sec                                                     | 1.30 sec: 1.07x faster                                               |
| async_tree_cpu_io_mixed | 889 ms                                                       | 974 ms: 1.10x slower                                                 |
| asyncio_tcp             | 948 ms                                                       | 1.12 sec: 1.18x slower                                               |
| asyncio_tcp_ssl         | 2.77 sec                                                     | 3.41 sec: 1.23x slower                                               |
| async_generators        | 567 ms                                                       | 712 ms: 1.26x slower                                                 |
| coroutines              | 30.9 ms                                                      | 41.6 ms: 1.35x slower                                                |
| Geometric mean          | (ref)                                                        | 1.06x slower                                                         |

Benchmark hidden because not significant (6): asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 116 ms                                                       | 192 ms: 1.66x slower                                                 |
| nbody          | 119 ms                                                       | 271 ms: 2.29x slower                                                 |
| Geometric mean | (ref)                                                        | 1.55x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 297 ms: 1.06x slower                                                 |
| regex_v8       | 32.8 ms                                                      | 35.5 ms: 1.08x slower                                                |
| regex_compile  | 182 ms                                                       | 312 ms: 1.71x slower                                                 |
| Geometric mean | (ref)                                                        | 1.17x slower                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 15.1 us                                                      | 13.8 us: 1.09x faster                                                |
| pickle_dict          | 47.2 us                                                      | 44.6 us: 1.06x faster                                                |
| unpickle             | 20.5 us                                                      | 22.9 us: 1.12x slower                                                |
| json_dumps           | 14.1 ms                                                      | 17.3 ms: 1.23x slower                                                |
| unpickle_list        | 6.68 us                                                      | 8.26 us: 1.24x slower                                                |
| json_loads           | 34.3 us                                                      | 43.5 us: 1.27x slower                                                |
| xml_etree_generate   | 122 ms                                                       | 166 ms: 1.36x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 131 ms: 1.53x slower                                                 |
| tomli_loads          | 2.78 sec                                                     | 4.40 sec: 1.58x slower                                               |
| pickle_pure_python   | 416 us                                                       | 812 us: 1.95x slower                                                 |
| unpickle_pure_python | 290 us                                                       | 597 us: 2.06x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.26x slower                                                         |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_list, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 21.7 ms: 1.42x slower                                                |
| python_startup         | 22.4 ms                                                      | 35.2 ms: 1.57x slower                                                |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 120 ms: 1.66x slower                                                 |
| genshi_text     | 31.7 ms                                                      | 55.2 ms: 1.74x slower                                                |
| django_template | 44.3 ms                                                      | 82.3 ms: 1.86x slower                                                |
| mako            | 15.9 ms                                                      | 32.1 ms: 2.01x slower                                                |
| Geometric mean  | (ref)                                                        | 1.81x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| create_gc_cycles         | 2.41 ms                                                      | 1.85 ms: 1.31x faster                                                |
| async_tree_io_tg         | 1.40 sec                                                     | 1.15 sec: 1.21x faster                                               |
| gc_traversal             | 5.70 ms                                                      | 5.05 ms: 1.13x faster                                                |
| pickle                   | 15.1 us                                                      | 13.8 us: 1.09x faster                                                |
| async_tree_io            | 1.39 sec                                                     | 1.30 sec: 1.07x faster                                               |
| pickle_dict              | 47.2 us                                                      | 44.6 us: 1.06x faster                                                |
| regex_dna                | 282 ms                                                       | 297 ms: 1.06x slower                                                 |
| regex_v8                 | 32.8 ms                                                      | 35.5 ms: 1.08x slower                                                |
| async_tree_cpu_io_mixed  | 889 ms                                                       | 974 ms: 1.10x slower                                                 |
| unpickle                 | 20.5 us                                                      | 22.9 us: 1.12x slower                                                |
| deepcopy                 | 498 us                                                       | 564 us: 1.13x slower                                                 |
| scimark_fft              | 473 ms                                                       | 539 ms: 1.14x slower                                                 |
| telco                    | 12.2 ms                                                      | 14.0 ms: 1.15x slower                                                |
| sqlite_synth             | 3.99 us                                                      | 4.64 us: 1.16x slower                                                |
| asyncio_tcp              | 948 ms                                                       | 1.12 sec: 1.18x slower                                               |
| docutils                 | 4.01 sec                                                     | 4.84 sec: 1.21x slower                                               |
| pathlib                  | 29.9 ms                                                      | 36.3 ms: 1.21x slower                                                |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 8.22 ms: 1.22x slower                                                |
| json_dumps               | 14.1 ms                                                      | 17.3 ms: 1.23x slower                                                |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.41 sec: 1.23x slower                                               |
| unpickle_list            | 6.68 us                                                      | 8.26 us: 1.24x slower                                                |
| async_generators         | 567 ms                                                       | 712 ms: 1.26x slower                                                 |
| json_loads               | 34.3 us                                                      | 43.5 us: 1.27x slower                                                |
| mdp                      | 3.80 sec                                                     | 4.90 sec: 1.29x slower                                               |
| pylint                   | 470 ms                                                       | 609 ms: 1.30x slower                                                 |
| meteor_contest           | 150 ms                                                       | 195 ms: 1.30x slower                                                 |
| json                     | 6.51 ms                                                      | 8.56 ms: 1.31x slower                                                |
| generators               | 40.0 ms                                                      | 53.5 ms: 1.34x slower                                                |
| coverage                 | 107 ms                                                       | 144 ms: 1.35x slower                                                 |
| coroutines               | 30.9 ms                                                      | 41.6 ms: 1.35x slower                                                |
| xml_etree_generate       | 122 ms                                                       | 166 ms: 1.36x slower                                                 |
| fannkuch                 | 547 ms                                                       | 761 ms: 1.39x slower                                                 |
| pycparser                | 1.57 sec                                                     | 2.20 sec: 1.40x slower                                               |
| python_startup_no_site   | 15.3 ms                                                      | 21.7 ms: 1.42x slower                                                |
| spectral_norm            | 157 ms                                                       | 224 ms: 1.43x slower                                                 |
| nqueens                  | 112 ms                                                       | 160 ms: 1.43x slower                                                 |
| deepcopy_memo            | 50.1 us                                                      | 72.1 us: 1.44x slower                                                |
| deepcopy_reduce          | 4.10 us                                                      | 6.24 us: 1.52x slower                                                |
| xml_etree_process        | 85.9 ms                                                      | 131 ms: 1.53x slower                                                 |
| html5lib                 | 92.6 ms                                                      | 142 ms: 1.53x slower                                                 |
| crypto_pyaes             | 100 ms                                                       | 156 ms: 1.56x slower                                                 |
| bench_thread_pool        | 2.89 ms                                                      | 4.51 ms: 1.56x slower                                                |
| 2to3                     | 445 ms                                                       | 698 ms: 1.57x slower                                                 |
| pyflate                  | 664 ms                                                       | 1.04 sec: 1.57x slower                                               |
| bpe_tokeniser            | 6.28 sec                                                     | 9.87 sec: 1.57x slower                                               |
| python_startup           | 22.4 ms                                                      | 35.2 ms: 1.57x slower                                                |
| thrift                   | 1.10 ms                                                      | 1.73 ms: 1.58x slower                                                |
| tomli_loads              | 2.78 sec                                                     | 4.40 sec: 1.58x slower                                               |
| tornado_http             | 251 ms                                                       | 399 ms: 1.59x slower                                                 |
| sqlglot_optimize         | 74.7 ms                                                      | 119 ms: 1.60x slower                                                 |
| richards                 | 65.5 ms                                                      | 107 ms: 1.63x slower                                                 |
| float                    | 116 ms                                                       | 192 ms: 1.66x slower                                                 |
| genshi_xml               | 72.1 ms                                                      | 120 ms: 1.66x slower                                                 |
| typing_runtime_protocols | 226 us                                                       | 381 us: 1.69x slower                                                 |
| sympy_integrate          | 30.2 ms                                                      | 51.4 ms: 1.70x slower                                                |
| regex_compile            | 182 ms                                                       | 312 ms: 1.71x slower                                                 |
| comprehensions           | 22.2 us                                                      | 38.6 us: 1.74x slower                                                |
| genshi_text              | 31.7 ms                                                      | 55.2 ms: 1.74x slower                                                |
| scimark_monte_carlo      | 90.6 ms                                                      | 160 ms: 1.77x slower                                                 |
| sqlglot_normalize        | 140 ms                                                       | 249 ms: 1.78x slower                                                 |
| pprint_pformat           | 1.94 sec                                                     | 3.47 sec: 1.79x slower                                               |
| pprint_safe_repr         | 987 ms                                                       | 1.77 sec: 1.79x slower                                               |
| sympy_str                | 379 ms                                                       | 698 ms: 1.84x slower                                                 |
| chaos                    | 83.6 ms                                                      | 154 ms: 1.85x slower                                                 |
| scimark_sor              | 179 ms                                                       | 331 ms: 1.85x slower                                                 |
| django_template          | 44.3 ms                                                      | 82.3 ms: 1.86x slower                                                |
| richards_super           | 73.2 ms                                                      | 137 ms: 1.87x slower                                                 |
| go                       | 191 ms                                                       | 370 ms: 1.94x slower                                                 |
| logging_simple           | 8.56 us                                                      | 16.6 us: 1.94x slower                                                |
| hexiom                   | 8.11 ms                                                      | 15.8 ms: 1.95x slower                                                |
| pickle_pure_python       | 416 us                                                       | 812 us: 1.95x slower                                                 |
| mako                     | 15.9 ms                                                      | 32.1 ms: 2.01x slower                                                |
| logging_silent           | 130 ns                                                       | 262 ns: 2.01x slower                                                 |
| unpickle_pure_python     | 290 us                                                       | 597 us: 2.06x slower                                                 |
| logging_format           | 9.24 us                                                      | 19.1 us: 2.06x slower                                                |
| sqlglot_transpile        | 2.20 ms                                                      | 4.66 ms: 2.12x slower                                                |
| scimark_lu               | 146 ms                                                       | 317 ms: 2.17x slower                                                 |
| sympy_expand             | 601 ms                                                       | 1.35 sec: 2.24x slower                                               |
| nbody                    | 119 ms                                                       | 271 ms: 2.29x slower                                                 |
| raytrace                 | 344 ms                                                       | 788 ms: 2.29x slower                                                 |
| sqlglot_parse            | 1.76 ms                                                      | 4.06 ms: 2.31x slower                                                |
| sympy_sum                | 210 ms                                                       | 512 ms: 2.44x slower                                                 |
| unpack_sequence          | 74.3 ns                                                      | 191 ns: 2.57x slower                                                 |
| deltablue                | 4.44 ms                                                      | 11.5 ms: 2.59x slower                                                |
| Geometric mean           | (ref)                                                        | 1.44x slower                                                         |

Benchmark hidden because not significant (12): regex_effbot, bench_mp_pool, asyncio_websockets, xml_etree_iterparse, pidigits, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_none, async_tree_memoization, pickle_list, xml_etree_parse
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.17x