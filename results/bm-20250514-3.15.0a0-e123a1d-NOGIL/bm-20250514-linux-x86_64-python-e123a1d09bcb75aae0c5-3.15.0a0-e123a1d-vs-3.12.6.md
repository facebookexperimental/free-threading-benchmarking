# Results vs. 3.12.6

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: linux-x86_64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.115x faster
- HPT reliability: 96.28%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 378 ms: 1.21x faster                                                  |
| docutils       | 4.00 sec                                               | 3.61 sec: 1.11x faster                                                |
| html5lib       | 88.9 ms                                                | 82.8 ms: 1.07x faster                                                 |
| Geometric mean | (ref)                                                  | 1.13x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 667 ms: 2.90x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 713 ms: 2.59x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 291 ms: 2.42x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 389 ms: 2.39x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 432 ms: 2.26x faster                                                  |
| async_tree_none            | 741 ms                                                 | 338 ms: 2.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 580 ms: 1.90x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 628 ms: 1.72x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 671 ms: 1.11x faster                                                  |
| async_generators           | 589 ms                                                 | 536 ms: 1.10x faster                                                  |
| coroutines                 | 29.5 ms                                                | 30.4 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.84x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 91.7 ms: 1.34x faster                                                 |
| pidigits       | 250 ms                                                 | 219 ms: 1.14x faster                                                  |
| nbody          | 119 ms                                                 | 159 ms: 1.34x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 3.95 ms: 1.30x faster                                                 |
| regex_v8       | 32.5 ms                                                | 27.3 ms: 1.19x faster                                                 |
| regex_dna      | 278 ms                                                 | 253 ms: 1.10x faster                                                  |
| regex_compile  | 187 ms                                                 | 180 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                  | 1.15x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|---------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse | 169 ms                                                 | 117 ms: 1.45x faster                                                  |
| xml_etree_parse     | 241 ms                                                 | 173 ms: 1.39x faster                                                  |
| tomli_loads         | 2.88 sec                                               | 2.78 sec: 1.04x faster                                                |
| json_dumps          | 14.3 ms                                                | 15.4 ms: 1.08x slower                                                 |
| json_loads          | 37.9 us                                                | 41.6 us: 1.10x slower                                                 |
| xml_etree_process   | 83.7 ms                                                | 92.1 ms: 1.10x slower                                                 |
| Geometric mean      | (ref)                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (3): pickle_pure_python, unpickle_pure_python, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 13.8 ms: 1.27x faster                                                 |
| python_startup         | 23.7 ms                                                | 22.6 ms: 1.05x faster                                                 |
| Geometric mean         | (ref)                                                  | 1.16x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 72.2 ms: 1.07x slower                                                 |
| django_template | 44.9 ms                                                | 49.4 ms: 1.10x slower                                                 |
| genshi_text     | 30.2 ms                                                | 33.3 ms: 1.10x slower                                                 |
| mako            | 15.7 ms                                                | 20.7 ms: 1.32x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.14x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 667 ms: 2.90x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 713 ms: 2.59x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 291 ms: 2.42x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 389 ms: 2.39x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 432 ms: 2.26x faster                                                  |
| async_tree_none            | 741 ms                                                 | 338 ms: 2.19x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 2.85 ms: 2.05x faster                                                 |
| mdp                        | 3.97 sec                                               | 2.07 sec: 1.92x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 580 ms: 1.90x faster                                                  |
| bench_thread_pool          | 3.48 ms                                                | 1.89 ms: 1.84x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 628 ms: 1.72x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 117 ms: 1.45x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 173 ms: 1.39x faster                                                  |
| float                      | 123 ms                                                 | 91.7 ms: 1.34x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 2.95 us: 1.31x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 3.95 ms: 1.30x faster                                                 |
| dulwich_log                | 100 ms                                                 | 77.1 ms: 1.30x faster                                                 |
| python_startup_no_site     | 17.6 ms                                                | 13.8 ms: 1.27x faster                                                 |
| pycparser                  | 1.79 sec                                               | 1.41 sec: 1.27x faster                                                |
| pathlib                    | 31.6 ms                                                | 25.0 ms: 1.26x faster                                                 |
| deepcopy                   | 468 us                                                 | 375 us: 1.25x faster                                                  |
| 2to3                       | 456 ms                                                 | 378 ms: 1.21x faster                                                  |
| regex_v8                   | 32.5 ms                                                | 27.3 ms: 1.19x faster                                                 |
| deepcopy_memo              | 52.4 us                                                | 45.6 us: 1.15x faster                                                 |
| pidigits                   | 250 ms                                                 | 219 ms: 1.14x faster                                                  |
| pylint                     | 465 ms                                                 | 408 ms: 1.14x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 671 ms: 1.11x faster                                                  |
| comprehensions             | 27.1 us                                                | 24.4 us: 1.11x faster                                                 |
| docutils                   | 4.00 sec                                               | 3.61 sec: 1.11x faster                                                |
| pyflate                    | 727 ms                                                 | 660 ms: 1.10x faster                                                  |
| regex_dna                  | 278 ms                                                 | 253 ms: 1.10x faster                                                  |
| async_generators           | 589 ms                                                 | 536 ms: 1.10x faster                                                  |
| spectral_norm              | 156 ms                                                 | 142 ms: 1.10x faster                                                  |
| html5lib                   | 88.9 ms                                                | 82.8 ms: 1.07x faster                                                 |
| go                         | 172 ms                                                 | 161 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 6.16 sec: 1.07x faster                                                |
| raytrace                   | 408 ms                                                 | 386 ms: 1.06x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.83 us: 1.05x faster                                                 |
| chaos                      | 84.9 ms                                                | 80.5 ms: 1.05x faster                                                 |
| python_startup             | 23.7 ms                                                | 22.6 ms: 1.05x faster                                                 |
| scimark_sor                | 167 ms                                                 | 159 ms: 1.05x faster                                                  |
| scimark_fft                | 500 ms                                                 | 481 ms: 1.04x faster                                                  |
| regex_compile              | 187 ms                                                 | 180 ms: 1.04x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.78 sec: 1.04x faster                                                |
| coroutines                 | 29.5 ms                                                | 30.4 ms: 1.03x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 111 ms: 1.04x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 100 ms: 1.04x slower                                                  |
| hexiom                     | 8.27 ms                                                | 8.67 ms: 1.05x slower                                                 |
| pprint_safe_repr           | 967 ms                                                 | 1.01 sec: 1.05x slower                                                |
| deltablue                  | 4.27 ms                                                | 4.48 ms: 1.05x slower                                                 |
| json                       | 6.85 ms                                                | 7.20 ms: 1.05x slower                                                 |
| pprint_pformat             | 1.98 sec                                               | 2.10 sec: 1.06x slower                                                |
| logging_simple             | 9.45 us                                                | 10.0 us: 1.06x slower                                                 |
| genshi_xml                 | 67.6 ms                                                | 72.2 ms: 1.07x slower                                                 |
| richards                   | 60.3 ms                                                | 64.6 ms: 1.07x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 15.4 ms: 1.08x slower                                                 |
| meteor_contest             | 146 ms                                                 | 159 ms: 1.09x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 166 ms: 1.09x slower                                                  |
| telco                      | 9.59 ms                                                | 10.5 ms: 1.10x slower                                                 |
| django_template            | 44.9 ms                                                | 49.4 ms: 1.10x slower                                                 |
| json_loads                 | 37.9 us                                                | 41.6 us: 1.10x slower                                                 |
| xml_etree_process          | 83.7 ms                                                | 92.1 ms: 1.10x slower                                                 |
| genshi_text                | 30.2 ms                                                | 33.3 ms: 1.10x slower                                                 |
| logging_format             | 9.59 us                                                | 10.6 us: 1.10x slower                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.41 ms: 1.11x slower                                                 |
| sympy_expand               | 582 ms                                                 | 646 ms: 1.11x slower                                                  |
| fannkuch                   | 540 ms                                                 | 608 ms: 1.12x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.20 ms: 1.13x slower                                                 |
| typing_runtime_protocols   | 224 us                                                 | 257 us: 1.15x slower                                                  |
| mako                       | 15.7 ms                                                | 20.7 ms: 1.32x slower                                                 |
| nbody                      | 119 ms                                                 | 159 ms: 1.34x slower                                                  |
| coverage                   | 95.4 ms                                                | 143 ms: 1.50x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 74.7 ms: 3.61x slower                                                 |
| logging_silent             | 139 ns                                                 | 699 ns: 5.02x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                          |

Benchmark hidden because not significant (10): sympy_integrate, nqueens, pickle_pure_python, sympy_sum, generators, unpickle_pure_python, sympy_str, xml_etree_generate, thrift, richards_super
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-linux-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.115x faster

# HPT report

- Reliability score: 96.28% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.42x