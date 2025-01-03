# Results vs. 3.12.6

- fork: python
- ref: 8eebe4e6d02bb4ad3f1c
- machine: linux-x86_64
- commit hash: 8eebe4e
- commit date: 2025-01-02
- overall geometric mean: 1.114x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 602 ms: 1.32x slower                                                   |
| docutils       | 4.00 sec                                               | 4.33 sec: 1.08x slower                                                 |
| html5lib       | 88.9 ms                                                | 120 ms: 1.35x slower                                                   |
| Geometric mean | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 918 ms: 2.11x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 989 ms: 1.87x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 410 ms: 1.72x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 567 ms: 1.64x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 601 ms: 1.63x faster                                                   |
| async_tree_none            | 741 ms                                                 | 493 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 738 ms: 1.49x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 834 ms: 1.29x faster                                                   |
| async_generators           | 589 ms                                                 | 642 ms: 1.09x slower                                                   |
| coroutines                 | 29.5 ms                                                | 33.0 ms: 1.12x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 242 ms: 1.03x faster                                                   |
| float          | 123 ms                                                 | 142 ms: 1.15x slower                                                   |
| nbody          | 119 ms                                                 | 170 ms: 1.43x slower                                                   |
| Geometric mean | (ref)                                                  | 1.17x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.55 ms: 1.13x faster                                                  |
| regex_dna      | 278 ms                                                 | 293 ms: 1.05x slower                                                   |
| regex_compile  | 187 ms                                                 | 211 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 128 ms: 1.33x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 208 ms: 1.16x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.27 sec: 1.13x slower                                                 |
| json_dumps           | 14.3 ms                                                | 17.1 ms: 1.20x slower                                                  |
| xml_etree_process    | 83.7 ms                                                | 106 ms: 1.26x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 416 us: 1.39x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 614 us: 1.41x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.6 ms: 1.11x slower                                                  |
| python_startup         | 23.7 ms                                                | 30.4 ms: 1.28x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 85.7 ms: 1.27x slower                                                  |
| genshi_text     | 30.2 ms                                                | 42.0 ms: 1.39x slower                                                  |
| django_template | 44.9 ms                                                | 65.0 ms: 1.45x slower                                                  |
| mako            | 15.7 ms                                                | 27.2 ms: 1.73x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.45x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 918 ms: 2.11x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 989 ms: 1.87x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 410 ms: 1.72x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 567 ms: 1.64x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 601 ms: 1.63x faster                                                   |
| async_tree_none            | 741 ms                                                 | 493 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 738 ms: 1.49x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 128 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 834 ms: 1.29x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 208 ms: 1.16x faster                                                   |
| deepcopy                   | 468 us                                                 | 414 us: 1.13x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.55 ms: 1.13x faster                                                  |
| pathlib                    | 31.6 ms                                                | 29.9 ms: 1.06x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.71 us: 1.04x faster                                                  |
| pidigits                   | 250 ms                                                 | 242 ms: 1.03x faster                                                   |
| scimark_fft                | 500 ms                                                 | 522 ms: 1.04x slower                                                   |
| regex_dna                  | 278 ms                                                 | 293 ms: 1.05x slower                                                   |
| sqlglot_normalize          | 157 ms                                                 | 169 ms: 1.08x slower                                                   |
| docutils                   | 4.00 sec                                               | 4.33 sec: 1.08x slower                                                 |
| async_generators           | 589 ms                                                 | 642 ms: 1.09x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.33 sec: 1.09x slower                                                 |
| deepcopy_reduce            | 4.04 us                                                | 4.43 us: 1.10x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 244 ms: 1.10x slower                                                   |
| nqueens                    | 117 ms                                                 | 129 ms: 1.10x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 19.6 ms: 1.11x slower                                                  |
| coroutines                 | 29.5 ms                                                | 33.0 ms: 1.12x slower                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 245 ms: 1.13x slower                                                   |
| dulwich_log                | 100 ms                                                 | 113 ms: 1.13x slower                                                   |
| regex_compile              | 187 ms                                                 | 211 ms: 1.13x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.27 sec: 1.13x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 122 ms: 1.14x slower                                                   |
| sympy_str                  | 385 ms                                                 | 443 ms: 1.15x slower                                                   |
| float                      | 123 ms                                                 | 142 ms: 1.15x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 89.1 ms: 1.17x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 35.0 ms: 1.18x slower                                                  |
| richards_super             | 72.8 ms                                                | 85.9 ms: 1.18x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 7.88 sec: 1.20x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 17.1 ms: 1.20x slower                                                  |
| telco                      | 9.59 ms                                                | 11.5 ms: 1.20x slower                                                  |
| meteor_contest             | 146 ms                                                 | 177 ms: 1.21x slower                                                   |
| fannkuch                   | 540 ms                                                 | 654 ms: 1.21x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 272 us: 1.21x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.29 ms: 1.21x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.15 ms: 1.22x slower                                                  |
| sympy_expand               | 582 ms                                                 | 717 ms: 1.23x slower                                                   |
| comprehensions             | 27.1 us                                                | 33.6 us: 1.24x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 4.33 ms: 1.24x slower                                                  |
| pyflate                    | 727 ms                                                 | 905 ms: 1.24x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 106 ms: 1.26x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 85.7 ms: 1.27x slower                                                  |
| logging_simple             | 9.45 us                                                | 12.0 us: 1.27x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.24 sec: 1.28x slower                                                 |
| scimark_lu                 | 152 ms                                                 | 195 ms: 1.28x slower                                                   |
| python_startup             | 23.7 ms                                                | 30.4 ms: 1.28x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.56 sec: 1.29x slower                                                 |
| richards                   | 60.3 ms                                                | 78.8 ms: 1.30x slower                                                  |
| logging_format             | 9.59 us                                                | 12.5 us: 1.31x slower                                                  |
| 2to3                       | 456 ms                                                 | 602 ms: 1.32x slower                                                   |
| generators                 | 41.1 ms                                                | 54.5 ms: 1.32x slower                                                  |
| html5lib                   | 88.9 ms                                                | 120 ms: 1.35x slower                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 34.0 ms: 1.38x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 416 us: 1.39x slower                                                   |
| genshi_text                | 30.2 ms                                                | 42.0 ms: 1.39x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 614 us: 1.41x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 138 ms: 1.43x slower                                                   |
| nbody                      | 119 ms                                                 | 170 ms: 1.43x slower                                                   |
| raytrace                   | 408 ms                                                 | 584 ms: 1.43x slower                                                   |
| coverage                   | 95.4 ms                                                | 137 ms: 1.43x slower                                                   |
| chaos                      | 84.9 ms                                                | 122 ms: 1.44x slower                                                   |
| django_template            | 44.9 ms                                                | 65.0 ms: 1.45x slower                                                  |
| hexiom                     | 8.27 ms                                                | 12.0 ms: 1.45x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 3.43 ms: 1.47x slower                                                  |
| scimark_sor                | 167 ms                                                 | 275 ms: 1.65x slower                                                   |
| logging_silent             | 139 ns                                                 | 230 ns: 1.65x slower                                                   |
| go                         | 172 ms                                                 | 288 ms: 1.67x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 3.03 ms: 1.69x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.32 ms: 1.71x slower                                                  |
| mako                       | 15.7 ms                                                | 27.2 ms: 1.73x slower                                                  |
| deltablue                  | 4.27 ms                                                | 10.4 ms: 2.45x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 94.2 ms: 4.55x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.16x slower                                                           |

Benchmark hidden because not significant (10): deepcopy_memo, regex_v8, asyncio_websockets, pycparser, json, pylint, gc_traversal, xml_etree_generate, spectral_norm, json_loads
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250102-3.14.0a3+-8eebe4e-NOGIL/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.114x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.34x