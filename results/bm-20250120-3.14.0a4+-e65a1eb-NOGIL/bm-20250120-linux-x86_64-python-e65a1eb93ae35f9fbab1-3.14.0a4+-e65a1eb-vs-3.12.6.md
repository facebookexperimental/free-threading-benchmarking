# Results vs. 3.12.6

- fork: python
- ref: e65a1eb93ae35f9fbab1
- machine: linux-x86_64
- commit hash: e65a1eb
- commit date: 2025-01-20
- overall geometric mean: 1.077x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 580 ms: 1.27x slower                                                   |
| docutils       | 4.00 sec                                               | 4.47 sec: 1.12x slower                                                 |
| html5lib       | 88.9 ms                                                | 108 ms: 1.21x slower                                                   |
| Geometric mean | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 753 ms: 2.57x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 864 ms: 2.14x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 335 ms: 2.10x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 486 ms: 1.92x faster                                                   |
| async_tree_none            | 741 ms                                                 | 395 ms: 1.88x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 586 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 683 ms: 1.61x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 749 ms: 1.44x faster                                                   |
| async_generators           | 589 ms                                                 | 573 ms: 1.03x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 776 ms: 1.04x slower                                                   |
| coroutines                 | 29.5 ms                                                | 33.7 ms: 1.14x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.57x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 108 ms: 1.14x faster                                                   |
| nbody          | 119 ms                                                 | 192 ms: 1.61x slower                                                   |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.58 ms: 1.12x faster                                                  |
| regex_v8       | 32.5 ms                                                | 34.5 ms: 1.06x slower                                                  |
| regex_dna      | 278 ms                                                 | 309 ms: 1.11x slower                                                   |
| regex_compile  | 187 ms                                                 | 224 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 140 ms: 1.21x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.04 sec: 1.05x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 135 ms: 1.06x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 492 us: 1.13x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 361 us: 1.20x slower                                                   |
| json_loads           | 37.9 us                                                | 46.2 us: 1.22x slower                                                  |
| xml_etree_process    | 83.7 ms                                                | 107 ms: 1.27x slower                                                   |
| json_dumps           | 14.3 ms                                                | 19.4 ms: 1.36x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 22.4 ms: 1.28x slower                                                  |
| python_startup         | 23.7 ms                                                | 35.1 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.38x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 89.2 ms: 1.32x slower                                                  |
| django_template | 44.9 ms                                                | 60.3 ms: 1.34x slower                                                  |
| genshi_text     | 30.2 ms                                                | 40.7 ms: 1.35x slower                                                  |
| mako            | 15.7 ms                                                | 24.8 ms: 1.58x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 753 ms: 2.57x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 864 ms: 2.14x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 335 ms: 2.10x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 486 ms: 1.92x faster                                                   |
| async_tree_none            | 741 ms                                                 | 395 ms: 1.88x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 586 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 683 ms: 1.61x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 749 ms: 1.44x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 140 ms: 1.21x faster                                                   |
| float                      | 123 ms                                                 | 108 ms: 1.14x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.58 sec: 1.14x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 4.58 ms: 1.12x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.63 us: 1.07x faster                                                  |
| async_generators           | 589 ms                                                 | 573 ms: 1.03x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 776 ms: 1.04x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.04 sec: 1.05x slower                                                 |
| sympy_str                  | 385 ms                                                 | 408 ms: 1.06x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 135 ms: 1.06x slower                                                   |
| pyflate                    | 727 ms                                                 | 772 ms: 1.06x slower                                                   |
| regex_v8                   | 32.5 ms                                                | 34.5 ms: 1.06x slower                                                  |
| go                         | 172 ms                                                 | 183 ms: 1.06x slower                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 239 ms: 1.10x slower                                                   |
| json                       | 6.85 ms                                                | 7.50 ms: 1.10x slower                                                  |
| regex_dna                  | 278 ms                                                 | 309 ms: 1.11x slower                                                   |
| docutils                   | 4.00 sec                                               | 4.47 sec: 1.12x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 249 ms: 1.12x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 85.4 ms: 1.12x slower                                                  |
| generators                 | 41.1 ms                                                | 46.4 ms: 1.13x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 33.6 ms: 1.13x slower                                                  |
| mdp                        | 3.97 sec                                               | 4.48 sec: 1.13x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 492 us: 1.13x slower                                                   |
| coroutines                 | 29.5 ms                                                | 33.7 ms: 1.14x slower                                                  |
| scimark_fft                | 500 ms                                                 | 574 ms: 1.15x slower                                                   |
| pprint_safe_repr           | 967 ms                                                 | 1.11 sec: 1.15x slower                                                 |
| deepcopy_reduce            | 4.04 us                                                | 4.65 us: 1.15x slower                                                  |
| logging_silent             | 139 ns                                                 | 161 ns: 1.15x slower                                                   |
| richards                   | 60.3 ms                                                | 70.4 ms: 1.17x slower                                                  |
| chaos                      | 84.9 ms                                                | 99.1 ms: 1.17x slower                                                  |
| richards_super             | 72.8 ms                                                | 85.9 ms: 1.18x slower                                                  |
| sympy_expand               | 582 ms                                                 | 689 ms: 1.18x slower                                                   |
| nqueens                    | 117 ms                                                 | 139 ms: 1.19x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.36 sec: 1.19x slower                                                 |
| scimark_sor                | 167 ms                                                 | 199 ms: 1.19x slower                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 7.86 sec: 1.19x slower                                                 |
| logging_simple             | 9.45 us                                                | 11.3 us: 1.20x slower                                                  |
| regex_compile              | 187 ms                                                 | 224 ms: 1.20x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 129 ms: 1.20x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 361 us: 1.20x slower                                                   |
| html5lib                   | 88.9 ms                                                | 108 ms: 1.21x slower                                                   |
| json_loads                 | 37.9 us                                                | 46.2 us: 1.22x slower                                                  |
| raytrace                   | 408 ms                                                 | 503 ms: 1.23x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 121 ms: 1.25x slower                                                   |
| fannkuch                   | 540 ms                                                 | 679 ms: 1.26x slower                                                   |
| 2to3                       | 456 ms                                                 | 580 ms: 1.27x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 107 ms: 1.27x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 22.4 ms: 1.28x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 195 ms: 1.28x slower                                                   |
| meteor_contest             | 146 ms                                                 | 188 ms: 1.29x slower                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.68 ms: 1.30x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 89.2 ms: 1.32x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.36 ms: 1.32x slower                                                  |
| django_template            | 44.9 ms                                                | 60.3 ms: 1.34x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 302 us: 1.34x slower                                                   |
| genshi_text                | 30.2 ms                                                | 40.7 ms: 1.35x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 19.4 ms: 1.36x slower                                                  |
| telco                      | 9.59 ms                                                | 13.0 ms: 1.36x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 33.9 ms: 1.37x slower                                                  |
| logging_format             | 9.59 us                                                | 13.2 us: 1.38x slower                                                  |
| hexiom                     | 8.27 ms                                                | 11.5 ms: 1.40x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.49 ms: 1.40x slower                                                  |
| python_startup             | 23.7 ms                                                | 35.1 ms: 1.48x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 8.76 ms: 1.49x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 3.59 ms: 1.54x slower                                                  |
| coverage                   | 95.4 ms                                                | 150 ms: 1.57x slower                                                   |
| mako                       | 15.7 ms                                                | 24.8 ms: 1.58x slower                                                  |
| nbody                      | 119 ms                                                 | 192 ms: 1.61x slower                                                   |
| create_gc_cycles           | 1.94 ms                                                | 3.20 ms: 1.65x slower                                                  |
| deltablue                  | 4.27 ms                                                | 7.11 ms: 1.67x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 5.88 ms: 1.69x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 103 ms: 4.98x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (10): xml_etree_parse, deepcopy, pathlib, pidigits, comprehensions, spectral_norm, deepcopy_memo, pylint, dulwich_log, sqlglot_normalize
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.077x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.35x