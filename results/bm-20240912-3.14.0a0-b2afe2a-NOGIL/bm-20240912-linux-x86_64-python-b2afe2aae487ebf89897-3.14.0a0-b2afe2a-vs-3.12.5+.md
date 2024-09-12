# Results vs. 3.12.5+

- fork: python
- ref: b2afe2aae487ebf89897
- machine: linux-x86_64
- commit hash: b2afe2a
- commit date: 2024-09-12
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                               | 721 ms: 1.58x slower                                                  |
| docutils       | 4.05 sec                                             | 5.09 sec: 1.26x slower                                                |
| html5lib       | 100 ms                                               | 141 ms: 1.41x slower                                                  |
| tornado_http   | 261 ms                                               | 369 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                | 1.41x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.26 sec: 1.48x faster                                                |
| async_tree_none_tg         | 726 ms                                               | 491 ms: 1.48x faster                                                  |
| async_tree_memoization_tg  | 912 ms                                               | 649 ms: 1.41x faster                                                  |
| async_tree_io              | 1.86 sec                                             | 1.35 sec: 1.38x faster                                                |
| async_tree_memoization     | 975 ms                                               | 750 ms: 1.30x faster                                                  |
| async_tree_none            | 820 ms                                               | 647 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 915 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 906 ms: 1.24x faster                                                  |
| asyncio_websockets         | 752 ms                                               | 792 ms: 1.05x slower                                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.12 sec: 1.11x slower                                                |
| async_generators           | 615 ms                                               | 726 ms: 1.18x slower                                                  |
| asyncio_tcp                | 988 ms                                               | 1.19 sec: 1.20x slower                                                |
| coroutines                 | 30.6 ms                                              | 44.1 ms: 1.44x slower                                                 |
| Geometric mean             | (ref)                                                | 1.12x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 124 ms                                               | 202 ms: 1.62x slower                                                  |
| nbody          | 117 ms                                               | 286 ms: 2.45x slower                                                  |
| Geometric mean | (ref)                                                | 1.59x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 268 ms                                               | 290 ms: 1.08x slower                                                  |
| regex_v8       | 29.9 ms                                              | 36.2 ms: 1.21x slower                                                 |
| regex_compile  | 186 ms                                               | 301 ms: 1.62x slower                                                  |
| Geometric mean | (ref)                                                | 1.20x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle               | 15.9 us                                              | 14.5 us: 1.10x faster                                                 |
| xml_etree_parse      | 244 ms                                               | 229 ms: 1.06x faster                                                  |
| unpickle             | 21.6 us                                              | 24.2 us: 1.12x slower                                                 |
| unpickle_list        | 6.83 us                                              | 7.76 us: 1.14x slower                                                 |
| json_loads           | 35.9 us                                              | 42.8 us: 1.19x slower                                                 |
| xml_etree_generate   | 138 ms                                               | 165 ms: 1.20x slower                                                  |
| json_dumps           | 14.0 ms                                              | 18.0 ms: 1.29x slower                                                 |
| tomli_loads          | 2.86 sec                                             | 4.26 sec: 1.49x slower                                                |
| xml_etree_process    | 82.7 ms                                              | 128 ms: 1.55x slower                                                  |
| unpickle_pure_python | 304 us                                               | 581 us: 1.91x slower                                                  |
| pickle_pure_python   | 436 us                                               | 835 us: 1.91x slower                                                  |
| Geometric mean       | (ref)                                                | 1.22x slower                                                          |

Benchmark hidden because not significant (3): pickle_list, xml_etree_iterparse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 23.8 ms: 1.47x slower                                                 |
| python_startup         | 22.7 ms                                              | 35.1 ms: 1.55x slower                                                 |
| Geometric mean         | (ref)                                                | 1.51x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|-----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 114 ms: 1.65x slower                                                  |
| django_template | 45.4 ms                                              | 82.9 ms: 1.82x slower                                                 |
| mako            | 16.1 ms                                              | 30.3 ms: 1.88x slower                                                 |
| genshi_text     | 30.3 ms                                              | 61.0 ms: 2.01x slower                                                 |
| Geometric mean  | (ref)                                                | 1.84x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.26 sec: 1.48x faster                                                |
| async_tree_none_tg         | 726 ms                                               | 491 ms: 1.48x faster                                                  |
| gc_traversal               | 6.42 ms                                              | 4.51 ms: 1.42x faster                                                 |
| async_tree_memoization_tg  | 912 ms                                               | 649 ms: 1.41x faster                                                  |
| async_tree_io              | 1.86 sec                                             | 1.35 sec: 1.38x faster                                                |
| async_tree_memoization     | 975 ms                                               | 750 ms: 1.30x faster                                                  |
| bench_mp_pool              | 21.2 ms                                              | 16.5 ms: 1.29x faster                                                 |
| async_tree_none            | 820 ms                                               | 647 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 915 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 906 ms: 1.24x faster                                                  |
| pickle                     | 15.9 us                                              | 14.5 us: 1.10x faster                                                 |
| create_gc_cycles           | 2.00 ms                                              | 1.83 ms: 1.09x faster                                                 |
| xml_etree_parse            | 244 ms                                               | 229 ms: 1.06x faster                                                  |
| asyncio_websockets         | 752 ms                                               | 792 ms: 1.05x slower                                                  |
| regex_dna                  | 268 ms                                               | 290 ms: 1.08x slower                                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.12 sec: 1.11x slower                                                |
| unpickle                   | 21.6 us                                              | 24.2 us: 1.12x slower                                                 |
| unpickle_list              | 6.83 us                                              | 7.76 us: 1.14x slower                                                 |
| json                       | 7.14 ms                                              | 8.13 ms: 1.14x slower                                                 |
| pathlib                    | 31.6 ms                                              | 36.3 ms: 1.15x slower                                                 |
| sqlite_synth               | 3.77 us                                              | 4.43 us: 1.17x slower                                                 |
| async_generators           | 615 ms                                               | 726 ms: 1.18x slower                                                  |
| json_loads                 | 35.9 us                                              | 42.8 us: 1.19x slower                                                 |
| xml_etree_generate         | 138 ms                                               | 165 ms: 1.20x slower                                                  |
| asyncio_tcp                | 988 ms                                               | 1.19 sec: 1.20x slower                                                |
| dulwich_log                | 104 ms                                               | 125 ms: 1.21x slower                                                  |
| regex_v8                   | 29.9 ms                                              | 36.2 ms: 1.21x slower                                                 |
| deepcopy                   | 486 us                                               | 595 us: 1.22x slower                                                  |
| bench_thread_pool          | 3.42 ms                                              | 4.27 ms: 1.25x slower                                                 |
| generators                 | 44.7 ms                                              | 56.1 ms: 1.25x slower                                                 |
| docutils                   | 4.05 sec                                             | 5.09 sec: 1.26x slower                                                |
| json_dumps                 | 14.0 ms                                              | 18.0 ms: 1.29x slower                                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 8.99 ms: 1.30x slower                                                 |
| pylint                     | 480 ms                                               | 627 ms: 1.31x slower                                                  |
| scimark_fft                | 481 ms                                               | 636 ms: 1.32x slower                                                  |
| deepcopy_reduce            | 4.18 us                                              | 5.61 us: 1.34x slower                                                 |
| meteor_contest             | 146 ms                                               | 199 ms: 1.36x slower                                                  |
| mdp                        | 3.77 sec                                             | 5.18 sec: 1.38x slower                                                |
| deepcopy_memo              | 51.0 us                                              | 71.2 us: 1.40x slower                                                 |
| crypto_pyaes               | 110 ms                                               | 153 ms: 1.40x slower                                                  |
| html5lib                   | 100 ms                                               | 141 ms: 1.41x slower                                                  |
| comprehensions             | 28.6 us                                              | 40.4 us: 1.41x slower                                                 |
| tornado_http               | 261 ms                                               | 369 ms: 1.41x slower                                                  |
| coroutines                 | 30.6 ms                                              | 44.1 ms: 1.44x slower                                                 |
| pycparser                  | 1.68 sec                                             | 2.43 sec: 1.45x slower                                                |
| thrift                     | 1.10 ms                                              | 1.61 ms: 1.46x slower                                                 |
| python_startup_no_site     | 16.2 ms                                              | 23.8 ms: 1.47x slower                                                 |
| tomli_loads                | 2.86 sec                                             | 4.26 sec: 1.49x slower                                                |
| typing_runtime_protocols   | 224 us                                               | 334 us: 1.49x slower                                                  |
| fannkuch                   | 525 ms                                               | 786 ms: 1.50x slower                                                  |
| nqueens                    | 116 ms                                               | 177 ms: 1.53x slower                                                  |
| telco                      | 9.53 ms                                              | 14.6 ms: 1.53x slower                                                 |
| bpe_tokeniser              | 6.76 sec                                             | 10.4 sec: 1.54x slower                                                |
| sympy_integrate            | 29.0 ms                                              | 44.8 ms: 1.55x slower                                                 |
| python_startup             | 22.7 ms                                              | 35.1 ms: 1.55x slower                                                 |
| xml_etree_process          | 82.7 ms                                              | 128 ms: 1.55x slower                                                  |
| 2to3                       | 456 ms                                               | 721 ms: 1.58x slower                                                  |
| coverage                   | 96.9 ms                                              | 154 ms: 1.59x slower                                                  |
| pyflate                    | 664 ms                                               | 1.06 sec: 1.59x slower                                                |
| regex_compile              | 186 ms                                               | 301 ms: 1.62x slower                                                  |
| float                      | 124 ms                                               | 202 ms: 1.62x slower                                                  |
| genshi_xml                 | 69.1 ms                                              | 114 ms: 1.65x slower                                                  |
| sqlglot_optimize           | 80.2 ms                                              | 134 ms: 1.67x slower                                                  |
| scimark_monte_carlo        | 96.8 ms                                              | 164 ms: 1.69x slower                                                  |
| sqlglot_normalize          | 144 ms                                               | 245 ms: 1.71x slower                                                  |
| richards                   | 62.8 ms                                              | 107 ms: 1.71x slower                                                  |
| logging_simple             | 9.68 us                                              | 16.7 us: 1.72x slower                                                 |
| pprint_safe_repr           | 972 ms                                               | 1.70 sec: 1.75x slower                                                |
| pprint_pformat             | 1.99 sec                                             | 3.58 sec: 1.80x slower                                                |
| django_template            | 45.4 ms                                              | 82.9 ms: 1.82x slower                                                 |
| logging_format             | 9.56 us                                              | 17.9 us: 1.87x slower                                                 |
| chaos                      | 92.1 ms                                              | 172 ms: 1.87x slower                                                  |
| mako                       | 16.1 ms                                              | 30.3 ms: 1.88x slower                                                 |
| logging_silent             | 139 ns                                               | 262 ns: 1.88x slower                                                  |
| raytrace                   | 405 ms                                               | 764 ms: 1.89x slower                                                  |
| sympy_str                  | 379 ms                                               | 721 ms: 1.90x slower                                                  |
| spectral_norm              | 136 ms                                               | 260 ms: 1.91x slower                                                  |
| unpickle_pure_python       | 304 us                                               | 581 us: 1.91x slower                                                  |
| pickle_pure_python         | 436 us                                               | 835 us: 1.91x slower                                                  |
| scimark_lu                 | 155 ms                                               | 302 ms: 1.95x slower                                                  |
| richards_super             | 69.7 ms                                              | 137 ms: 1.96x slower                                                  |
| sqlglot_transpile          | 2.32 ms                                              | 4.66 ms: 2.01x slower                                                 |
| genshi_text                | 30.3 ms                                              | 61.0 ms: 2.01x slower                                                 |
| sqlglot_parse              | 1.85 ms                                              | 3.75 ms: 2.03x slower                                                 |
| hexiom                     | 8.19 ms                                              | 16.9 ms: 2.06x slower                                                 |
| go                         | 173 ms                                               | 363 ms: 2.09x slower                                                  |
| sympy_sum                  | 218 ms                                               | 460 ms: 2.11x slower                                                  |
| scimark_sor                | 170 ms                                               | 367 ms: 2.16x slower                                                  |
| sympy_expand               | 591 ms                                               | 1.31 sec: 2.22x slower                                                |
| nbody                      | 117 ms                                               | 286 ms: 2.45x slower                                                  |
| deltablue                  | 4.45 ms                                              | 11.4 ms: 2.55x slower                                                 |
| unpack_sequence            | 70.8 ns                                              | 220 ns: 3.10x slower                                                  |
| Geometric mean             | (ref)                                                | 1.39x slower                                                          |

Benchmark hidden because not significant (5): regex_effbot, pickle_list, xml_etree_iterparse, pidigits, pickle_dict
Ignored benchmarks (8) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.34x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.15x