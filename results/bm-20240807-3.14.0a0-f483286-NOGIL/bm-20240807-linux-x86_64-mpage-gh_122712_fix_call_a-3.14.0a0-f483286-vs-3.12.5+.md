# Results vs. 3.12.5+

- fork: mpage
- ref: gh_122712_fix_call_a
- machine: linux-x86_64
- commit hash: f483286
- commit date: 2024-08-07
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 456 ms                                               | 646 ms: 1.42x slower                                                 |
| docutils       | 4.05 sec                                             | 5.06 sec: 1.25x slower                                               |
| html5lib       | 100 ms                                               | 140 ms: 1.40x slower                                                 |
| tornado_http   | 261 ms                                               | 367 ms: 1.41x slower                                                 |
| Geometric mean | (ref)                                                | 1.37x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.15 sec: 1.63x faster                                               |
| async_tree_io              | 1.86 sec                                             | 1.25 sec: 1.48x faster                                               |
| async_tree_none_tg         | 726 ms                                               | 491 ms: 1.48x faster                                                 |
| async_tree_none            | 820 ms                                               | 585 ms: 1.40x faster                                                 |
| async_tree_memoization_tg  | 912 ms                                               | 666 ms: 1.37x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 824 ms: 1.36x faster                                                 |
| async_tree_memoization     | 975 ms                                               | 751 ms: 1.30x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 933 ms: 1.22x faster                                                 |
| asyncio_tcp                | 988 ms                                               | 1.12 sec: 1.13x slower                                               |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.36 sec: 1.19x slower                                               |
| async_generators           | 615 ms                                               | 753 ms: 1.23x slower                                                 |
| coroutines                 | 30.6 ms                                              | 42.1 ms: 1.38x slower                                                |
| Geometric mean             | (ref)                                                | 1.15x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 256 ms                                               | 242 ms: 1.06x faster                                                 |
| float          | 124 ms                                               | 196 ms: 1.57x slower                                                 |
| nbody          | 117 ms                                               | 284 ms: 2.43x slower                                                 |
| Geometric mean | (ref)                                                | 1.53x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 4.82 ms: 1.04x faster                                                |
| regex_dna      | 268 ms                                               | 301 ms: 1.12x slower                                                 |
| regex_v8       | 29.9 ms                                              | 39.2 ms: 1.31x slower                                                |
| regex_compile  | 186 ms                                               | 295 ms: 1.58x slower                                                 |
| Geometric mean | (ref)                                                | 1.22x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 15.9 us                                              | 14.1 us: 1.12x faster                                                |
| xml_etree_parse      | 244 ms                                               | 232 ms: 1.05x faster                                                 |
| pickle_dict          | 45.5 us                                              | 43.9 us: 1.04x faster                                                |
| unpickle_list        | 6.83 us                                              | 7.94 us: 1.16x slower                                                |
| xml_etree_generate   | 138 ms                                               | 164 ms: 1.19x slower                                                 |
| json_dumps           | 14.0 ms                                              | 17.7 ms: 1.26x slower                                                |
| json_loads           | 35.9 us                                              | 45.4 us: 1.26x slower                                                |
| tomli_loads          | 2.86 sec                                             | 4.20 sec: 1.47x slower                                               |
| xml_etree_process    | 82.7 ms                                              | 135 ms: 1.63x slower                                                 |
| pickle_pure_python   | 436 us                                               | 778 us: 1.78x slower                                                 |
| unpickle_pure_python | 304 us                                               | 567 us: 1.87x slower                                                 |
| Geometric mean       | (ref)                                                | 1.21x slower                                                         |

Benchmark hidden because not significant (3): pickle_list, unpickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|------------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 20.7 ms: 1.28x slower                                                |
| python_startup         | 22.7 ms                                              | 29.3 ms: 1.29x slower                                                |
| Geometric mean         | (ref)                                                | 1.29x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|-----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 45.4 ms                                              | 77.1 ms: 1.70x slower                                                |
| genshi_xml      | 69.1 ms                                              | 118 ms: 1.70x slower                                                 |
| genshi_text     | 30.3 ms                                              | 54.2 ms: 1.79x slower                                                |
| mako            | 16.1 ms                                              | 32.1 ms: 1.99x slower                                                |
| Geometric mean  | (ref)                                                | 1.79x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286 |
|----------------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.15 sec: 1.63x faster                                               |
| async_tree_io              | 1.86 sec                                             | 1.25 sec: 1.48x faster                                               |
| async_tree_none_tg         | 726 ms                                               | 491 ms: 1.48x faster                                                 |
| async_tree_none            | 820 ms                                               | 585 ms: 1.40x faster                                                 |
| gc_traversal               | 6.42 ms                                              | 4.63 ms: 1.39x faster                                                |
| async_tree_memoization_tg  | 912 ms                                               | 666 ms: 1.37x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 824 ms: 1.36x faster                                                 |
| async_tree_memoization     | 975 ms                                               | 751 ms: 1.30x faster                                                 |
| bench_mp_pool              | 21.2 ms                                              | 16.8 ms: 1.27x faster                                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 933 ms: 1.22x faster                                                 |
| pickle                     | 15.9 us                                              | 14.1 us: 1.12x faster                                                |
| pidigits                   | 256 ms                                               | 242 ms: 1.06x faster                                                 |
| xml_etree_parse            | 244 ms                                               | 232 ms: 1.05x faster                                                 |
| regex_effbot               | 5.02 ms                                              | 4.82 ms: 1.04x faster                                                |
| pickle_dict                | 45.5 us                                              | 43.9 us: 1.04x faster                                                |
| regex_dna                  | 268 ms                                               | 301 ms: 1.12x slower                                                 |
| pathlib                    | 31.6 ms                                              | 35.6 ms: 1.13x slower                                                |
| asyncio_tcp                | 988 ms                                               | 1.12 sec: 1.13x slower                                               |
| deepcopy                   | 486 us                                               | 556 us: 1.14x slower                                                 |
| json                       | 7.14 ms                                              | 8.22 ms: 1.15x slower                                                |
| unpickle_list              | 6.83 us                                              | 7.94 us: 1.16x slower                                                |
| sqlite_synth               | 3.77 us                                              | 4.44 us: 1.18x slower                                                |
| xml_etree_generate         | 138 ms                                               | 164 ms: 1.19x slower                                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.36 sec: 1.19x slower                                               |
| async_generators           | 615 ms                                               | 753 ms: 1.23x slower                                                 |
| pylint                     | 480 ms                                               | 590 ms: 1.23x slower                                                 |
| docutils                   | 4.05 sec                                             | 5.06 sec: 1.25x slower                                               |
| json_dumps                 | 14.0 ms                                              | 17.7 ms: 1.26x slower                                                |
| json_loads                 | 35.9 us                                              | 45.4 us: 1.26x slower                                                |
| bench_thread_pool          | 3.42 ms                                              | 4.33 ms: 1.27x slower                                                |
| python_startup_no_site     | 16.2 ms                                              | 20.7 ms: 1.28x slower                                                |
| generators                 | 44.7 ms                                              | 57.5 ms: 1.29x slower                                                |
| python_startup             | 22.7 ms                                              | 29.3 ms: 1.29x slower                                                |
| regex_v8                   | 29.9 ms                                              | 39.2 ms: 1.31x slower                                                |
| scimark_fft                | 481 ms                                               | 635 ms: 1.32x slower                                                 |
| meteor_contest             | 146 ms                                               | 194 ms: 1.33x slower                                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 9.23 ms: 1.33x slower                                                |
| comprehensions             | 28.6 us                                              | 38.3 us: 1.34x slower                                                |
| deepcopy_memo              | 51.0 us                                              | 69.7 us: 1.37x slower                                                |
| pycparser                  | 1.68 sec                                             | 2.29 sec: 1.37x slower                                               |
| mdp                        | 3.77 sec                                             | 5.16 sec: 1.37x slower                                               |
| coroutines                 | 30.6 ms                                              | 42.1 ms: 1.38x slower                                                |
| crypto_pyaes               | 110 ms                                               | 152 ms: 1.39x slower                                                 |
| nqueens                    | 116 ms                                               | 161 ms: 1.39x slower                                                 |
| deepcopy_reduce            | 4.18 us                                              | 5.84 us: 1.40x slower                                                |
| html5lib                   | 100 ms                                               | 140 ms: 1.40x slower                                                 |
| tornado_http               | 261 ms                                               | 367 ms: 1.41x slower                                                 |
| 2to3                       | 456 ms                                               | 646 ms: 1.42x slower                                                 |
| telco                      | 9.53 ms                                              | 13.8 ms: 1.45x slower                                                |
| tomli_loads                | 2.86 sec                                             | 4.20 sec: 1.47x slower                                               |
| fannkuch                   | 525 ms                                               | 776 ms: 1.48x slower                                                 |
| coverage                   | 96.9 ms                                              | 146 ms: 1.50x slower                                                 |
| bpe_tokeniser              | 6.76 sec                                             | 10.3 sec: 1.52x slower                                               |
| sympy_integrate            | 29.0 ms                                              | 44.3 ms: 1.53x slower                                                |
| logging_simple             | 9.68 us                                              | 15.0 us: 1.55x slower                                                |
| float                      | 124 ms                                               | 196 ms: 1.57x slower                                                 |
| regex_compile              | 186 ms                                               | 295 ms: 1.58x slower                                                 |
| typing_runtime_protocols   | 224 us                                               | 356 us: 1.59x slower                                                 |
| thrift                     | 1.10 ms                                              | 1.77 ms: 1.61x slower                                                |
| xml_etree_process          | 82.7 ms                                              | 135 ms: 1.63x slower                                                 |
| pyflate                    | 664 ms                                               | 1.09 sec: 1.64x slower                                               |
| scimark_monte_carlo        | 96.8 ms                                              | 160 ms: 1.66x slower                                                 |
| sqlglot_normalize          | 144 ms                                               | 242 ms: 1.69x slower                                                 |
| pprint_safe_repr           | 972 ms                                               | 1.64 sec: 1.69x slower                                               |
| django_template            | 45.4 ms                                              | 77.1 ms: 1.70x slower                                                |
| genshi_xml                 | 69.1 ms                                              | 118 ms: 1.70x slower                                                 |
| pprint_pformat             | 1.99 sec                                             | 3.45 sec: 1.74x slower                                               |
| richards                   | 62.8 ms                                              | 110 ms: 1.75x slower                                                 |
| sympy_str                  | 379 ms                                               | 673 ms: 1.78x slower                                                 |
| richards_super             | 69.7 ms                                              | 124 ms: 1.78x slower                                                 |
| pickle_pure_python         | 436 us                                               | 778 us: 1.78x slower                                                 |
| genshi_text                | 30.3 ms                                              | 54.2 ms: 1.79x slower                                                |
| sqlglot_optimize           | 80.2 ms                                              | 143 ms: 1.79x slower                                                 |
| logging_silent             | 139 ns                                               | 254 ns: 1.83x slower                                                 |
| chaos                      | 92.1 ms                                              | 169 ms: 1.83x slower                                                 |
| spectral_norm              | 136 ms                                               | 253 ms: 1.85x slower                                                 |
| unpickle_pure_python       | 304 us                                               | 567 us: 1.87x slower                                                 |
| raytrace                   | 405 ms                                               | 765 ms: 1.89x slower                                                 |
| logging_format             | 9.56 us                                              | 18.5 us: 1.94x slower                                                |
| scimark_lu                 | 155 ms                                               | 303 ms: 1.95x slower                                                 |
| mako                       | 16.1 ms                                              | 32.1 ms: 1.99x slower                                                |
| sqlglot_transpile          | 2.32 ms                                              | 4.62 ms: 1.99x slower                                                |
| scimark_sor                | 170 ms                                               | 342 ms: 2.01x slower                                                 |
| hexiom                     | 8.19 ms                                              | 17.2 ms: 2.10x slower                                                |
| sympy_sum                  | 218 ms                                               | 465 ms: 2.13x slower                                                 |
| sympy_expand               | 591 ms                                               | 1.26 sec: 2.14x slower                                               |
| sqlglot_parse              | 1.85 ms                                              | 4.43 ms: 2.39x slower                                                |
| nbody                      | 117 ms                                               | 284 ms: 2.43x slower                                                 |
| deltablue                  | 4.45 ms                                              | 11.3 ms: 2.55x slower                                                |
| go                         | 173 ms                                               | 446 ms: 2.57x slower                                                 |
| unpack_sequence            | 70.8 ns                                              | 211 ns: 2.98x slower                                                 |
| Geometric mean             | (ref)                                                | 1.37x slower                                                         |

Benchmark hidden because not significant (5): create_gc_cycles, pickle_list, asyncio_websockets, unpickle, xml_etree_iterparse
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.15x