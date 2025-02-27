# Results vs. 3.12.6

- fork: python
- ref: fda056e64bdfcac3dd3d
- machine: linux-x86_64
- commit hash: fda056e
- commit date: 2025-02-26
- overall geometric mean: 1.004x faster
- HPT reliability: 99.69%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 500 ms: 1.10x slower                                                   |
| html5lib       | 88.9 ms                                                | 94.3 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 745 ms: 2.60x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 805 ms: 2.29x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 332 ms: 2.12x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 476 ms: 1.95x faster                                                   |
| async_tree_none            | 741 ms                                                 | 391 ms: 1.90x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 525 ms: 1.86x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 639 ms: 1.72x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 734 ms: 1.47x faster                                                   |
| async_generators           | 589 ms                                                 | 570 ms: 1.03x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 805 ms: 1.08x slower                                                   |
| coroutines                 | 29.5 ms                                                | 32.5 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.61x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 105 ms: 1.17x faster                                                   |
| pidigits       | 250 ms                                                 | 233 ms: 1.07x faster                                                   |
| nbody          | 119 ms                                                 | 171 ms: 1.43x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.15 ms: 1.24x faster                                                  |
| regex_dna      | 278 ms                                                 | 295 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 134 ms: 1.27x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 201 ms: 1.20x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.01 sec: 1.04x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 87.9 ms: 1.05x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 319 us: 1.06x slower                                                   |
| json_loads           | 37.9 us                                                | 42.0 us: 1.11x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 490 us: 1.13x slower                                                   |
| json_dumps           | 14.3 ms                                                | 17.6 ms: 1.23x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.9 ms: 1.13x slower                                                  |
| python_startup         | 23.7 ms                                                | 30.5 ms: 1.29x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 50.8 ms: 1.13x slower                                                  |
| genshi_text     | 30.2 ms                                                | 35.6 ms: 1.18x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 80.1 ms: 1.18x slower                                                  |
| mako            | 15.7 ms                                                | 22.1 ms: 1.40x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 745 ms: 2.60x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 805 ms: 2.29x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 332 ms: 2.12x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 476 ms: 1.95x faster                                                   |
| async_tree_none            | 741 ms                                                 | 391 ms: 1.90x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 525 ms: 1.86x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 639 ms: 1.72x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 3.62 ms: 1.62x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 734 ms: 1.47x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 134 ms: 1.27x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.15 ms: 1.24x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 201 ms: 1.20x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.52 sec: 1.18x faster                                                 |
| float                      | 123 ms                                                 | 105 ms: 1.17x faster                                                   |
| deepcopy                   | 468 us                                                 | 415 us: 1.13x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 47.0 us: 1.12x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.58 us: 1.08x faster                                                  |
| logging_simple             | 9.45 us                                                | 8.74 us: 1.08x faster                                                  |
| pathlib                    | 31.6 ms                                                | 29.4 ms: 1.08x faster                                                  |
| pidigits                   | 250 ms                                                 | 233 ms: 1.07x faster                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 205 ms: 1.06x faster                                                   |
| comprehensions             | 27.1 us                                                | 25.6 us: 1.06x faster                                                  |
| spectral_norm              | 156 ms                                                 | 148 ms: 1.05x faster                                                   |
| async_generators           | 589 ms                                                 | 570 ms: 1.03x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 3.01 sec: 1.04x slower                                                 |
| logging_silent             | 139 ns                                                 | 146 ns: 1.05x slower                                                   |
| pyflate                    | 727 ms                                                 | 762 ms: 1.05x slower                                                   |
| generators                 | 41.1 ms                                                | 43.1 ms: 1.05x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 87.9 ms: 1.05x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 4.25 us: 1.05x slower                                                  |
| regex_dna                  | 278 ms                                                 | 295 ms: 1.06x slower                                                   |
| html5lib                   | 88.9 ms                                                | 94.3 ms: 1.06x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 319 us: 1.06x slower                                                   |
| go                         | 172 ms                                                 | 183 ms: 1.06x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.13 ms: 1.07x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 7.06 sec: 1.07x slower                                                 |
| asyncio_websockets         | 748 ms                                                 | 805 ms: 1.08x slower                                                   |
| scimark_fft                | 500 ms                                                 | 540 ms: 1.08x slower                                                   |
| chaos                      | 84.9 ms                                                | 92.1 ms: 1.09x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 27.0 ms: 1.09x slower                                                  |
| 2to3                       | 456 ms                                                 | 500 ms: 1.10x slower                                                   |
| coroutines                 | 29.5 ms                                                | 32.5 ms: 1.10x slower                                                  |
| scimark_sor                | 167 ms                                                 | 184 ms: 1.11x slower                                                   |
| json_loads                 | 37.9 us                                                | 42.0 us: 1.11x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 33.1 ms: 1.11x slower                                                  |
| sympy_str                  | 385 ms                                                 | 429 ms: 1.11x slower                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.60 ms: 1.11x slower                                                  |
| json                       | 6.85 ms                                                | 7.68 ms: 1.12x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 490 us: 1.13x slower                                                   |
| pprint_safe_repr           | 967 ms                                                 | 1.09 sec: 1.13x slower                                                 |
| python_startup_no_site     | 17.6 ms                                                | 19.9 ms: 1.13x slower                                                  |
| django_template            | 44.9 ms                                                | 50.8 ms: 1.13x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.58 ms: 1.13x slower                                                  |
| richards_super             | 72.8 ms                                                | 82.5 ms: 1.13x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 110 ms: 1.14x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 254 ms: 1.14x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.28 sec: 1.15x slower                                                 |
| richards                   | 60.3 ms                                                | 70.0 ms: 1.16x slower                                                  |
| nqueens                    | 117 ms                                                 | 136 ms: 1.16x slower                                                   |
| sympy_expand               | 582 ms                                                 | 677 ms: 1.16x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 125 ms: 1.17x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 263 us: 1.17x slower                                                   |
| deltablue                  | 4.27 ms                                                | 5.02 ms: 1.18x slower                                                  |
| genshi_text                | 30.2 ms                                                | 35.6 ms: 1.18x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 80.1 ms: 1.18x slower                                                  |
| meteor_contest             | 146 ms                                                 | 175 ms: 1.20x slower                                                   |
| logging_format             | 9.59 us                                                | 11.5 us: 1.20x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 183 ms: 1.21x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 2.16 ms: 1.21x slower                                                  |
| fannkuch                   | 540 ms                                                 | 664 ms: 1.23x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 17.6 ms: 1.23x slower                                                  |
| hexiom                     | 8.27 ms                                                | 10.4 ms: 1.26x slower                                                  |
| telco                      | 9.59 ms                                                | 12.1 ms: 1.26x slower                                                  |
| python_startup             | 23.7 ms                                                | 30.5 ms: 1.29x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.61 ms: 1.35x slower                                                  |
| mako                       | 15.7 ms                                                | 22.1 ms: 1.40x slower                                                  |
| nbody                      | 119 ms                                                 | 171 ms: 1.43x slower                                                   |
| coverage                   | 95.4 ms                                                | 138 ms: 1.45x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 81.5 ms: 3.94x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (11): pylint, xml_etree_generate, dulwich_log, mdp, regex_compile, docutils, sqlglot_normalize, regex_v8, sqlglot_optimize, raytrace, bench_thread_pool
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 99.69% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.36x