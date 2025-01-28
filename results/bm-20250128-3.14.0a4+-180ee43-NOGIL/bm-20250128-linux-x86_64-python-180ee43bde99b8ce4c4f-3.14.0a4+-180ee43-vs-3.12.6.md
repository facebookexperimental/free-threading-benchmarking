# Results vs. 3.12.6

- fork: python
- ref: 180ee43bde99b8ce4c4f
- machine: linux-x86_64
- commit hash: 180ee43
- commit date: 2025-01-28
- overall geometric mean: 1.099x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 620 ms: 1.36x slower                                                   |
| docutils       | 4.00 sec                                               | 4.25 sec: 1.06x slower                                                 |
| html5lib       | 88.9 ms                                                | 102 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 838 ms: 2.31x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 963 ms: 1.92x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 517 ms: 1.80x faster                                                   |
| async_tree_none            | 741 ms                                                 | 449 ms: 1.65x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 429 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 690 ms: 1.59x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 632 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 822 ms: 1.31x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 811 ms: 1.08x slower                                                   |
| coroutines                 | 29.5 ms                                                | 32.3 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                           |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 117 ms: 1.05x faster                                                   |
| pidigits       | 250 ms                                                 | 264 ms: 1.06x slower                                                   |
| nbody          | 119 ms                                                 | 192 ms: 1.61x slower                                                   |
| Geometric mean | (ref)                                                  | 1.17x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.53 ms: 1.13x faster                                                  |
| regex_dna      | 278 ms                                                 | 301 ms: 1.08x slower                                                   |
| regex_v8       | 32.5 ms                                                | 35.5 ms: 1.09x slower                                                  |
| regex_compile  | 187 ms                                                 | 224 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 156 ms: 1.09x faster                                                   |
| xml_etree_generate   | 127 ms                                                 | 143 ms: 1.12x slower                                                   |
| tomli_loads          | 2.88 sec                                               | 3.28 sec: 1.14x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 98.7 ms: 1.18x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 532 us: 1.22x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 371 us: 1.24x slower                                                   |
| json_dumps           | 14.3 ms                                                | 18.2 ms: 1.27x slower                                                  |
| json_loads           | 37.9 us                                                | 52.2 us: 1.38x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.15x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 22.7 ms: 1.29x slower                                                  |
| python_startup         | 23.7 ms                                                | 36.2 ms: 1.53x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.40x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 56.0 ms: 1.25x slower                                                  |
| genshi_text     | 30.2 ms                                                | 39.2 ms: 1.30x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 95.0 ms: 1.41x slower                                                  |
| mako            | 15.7 ms                                                | 27.3 ms: 1.73x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.41x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 838 ms: 2.31x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 963 ms: 1.92x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 517 ms: 1.80x faster                                                   |
| async_tree_none            | 741 ms                                                 | 449 ms: 1.65x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 429 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 690 ms: 1.59x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 632 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 822 ms: 1.31x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.53 ms: 1.13x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.61 sec: 1.12x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 156 ms: 1.09x faster                                                   |
| float                      | 123 ms                                                 | 117 ms: 1.05x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 50.3 us: 1.04x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.73 us: 1.04x faster                                                  |
| pidigits                   | 250 ms                                                 | 264 ms: 1.06x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 114 ms: 1.06x slower                                                   |
| comprehensions             | 27.1 us                                                | 28.8 us: 1.06x slower                                                  |
| docutils                   | 4.00 sec                                               | 4.25 sec: 1.06x slower                                                 |
| regex_dna                  | 278 ms                                                 | 301 ms: 1.08x slower                                                   |
| asyncio_websockets         | 748 ms                                                 | 811 ms: 1.08x slower                                                   |
| coroutines                 | 29.5 ms                                                | 32.3 ms: 1.09x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 35.5 ms: 1.09x slower                                                  |
| pylint                     | 465 ms                                                 | 512 ms: 1.10x slower                                                   |
| pathlib                    | 31.6 ms                                                | 34.9 ms: 1.10x slower                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 241 ms: 1.11x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.42 sec: 1.11x slower                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.51 ms: 1.12x slower                                                  |
| xml_etree_generate         | 127 ms                                                 | 143 ms: 1.12x slower                                                   |
| raytrace                   | 408 ms                                                 | 462 ms: 1.13x slower                                                   |
| pyflate                    | 727 ms                                                 | 825 ms: 1.14x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.28 sec: 1.14x slower                                                 |
| html5lib                   | 88.9 ms                                                | 102 ms: 1.14x slower                                                   |
| scimark_sor                | 167 ms                                                 | 191 ms: 1.15x slower                                                   |
| sympy_str                  | 385 ms                                                 | 443 ms: 1.15x slower                                                   |
| dulwich_log                | 100 ms                                                 | 116 ms: 1.15x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 34.3 ms: 1.15x slower                                                  |
| nqueens                    | 117 ms                                                 | 135 ms: 1.16x slower                                                   |
| json                       | 6.85 ms                                                | 8.02 ms: 1.17x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 98.7 ms: 1.18x slower                                                  |
| chaos                      | 84.9 ms                                                | 101 ms: 1.19x slower                                                   |
| richards                   | 60.3 ms                                                | 71.9 ms: 1.19x slower                                                  |
| scimark_fft                | 500 ms                                                 | 597 ms: 1.19x slower                                                   |
| regex_compile              | 187 ms                                                 | 224 ms: 1.20x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 268 ms: 1.21x slower                                                   |
| sqlglot_normalize          | 157 ms                                                 | 190 ms: 1.21x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.40 sec: 1.21x slower                                                 |
| sympy_expand               | 582 ms                                                 | 707 ms: 1.22x slower                                                   |
| pprint_safe_repr           | 967 ms                                                 | 1.18 sec: 1.22x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 532 us: 1.22x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 2.22 ms: 1.24x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 371 us: 1.24x slower                                                   |
| deepcopy_reduce            | 4.04 us                                                | 5.01 us: 1.24x slower                                                  |
| generators                 | 41.1 ms                                                | 51.2 ms: 1.24x slower                                                  |
| django_template            | 44.9 ms                                                | 56.0 ms: 1.25x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.33 ms: 1.26x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 8.35 sec: 1.27x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 18.2 ms: 1.27x slower                                                  |
| go                         | 172 ms                                                 | 221 ms: 1.28x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 22.7 ms: 1.29x slower                                                  |
| logging_format             | 9.59 us                                                | 12.4 us: 1.29x slower                                                  |
| genshi_text                | 30.2 ms                                                | 39.2 ms: 1.30x slower                                                  |
| logging_simple             | 9.45 us                                                | 12.3 us: 1.30x slower                                                  |
| logging_silent             | 139 ns                                                 | 182 ns: 1.30x slower                                                   |
| fannkuch                   | 540 ms                                                 | 712 ms: 1.32x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 129 ms: 1.34x slower                                                   |
| richards_super             | 72.8 ms                                                | 97.2 ms: 1.34x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 206 ms: 1.35x slower                                                   |
| 2to3                       | 456 ms                                                 | 620 ms: 1.36x slower                                                   |
| json_loads                 | 37.9 us                                                | 52.2 us: 1.38x slower                                                  |
| meteor_contest             | 146 ms                                                 | 203 ms: 1.39x slower                                                   |
| coverage                   | 95.4 ms                                                | 133 ms: 1.40x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 315 us: 1.40x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 95.0 ms: 1.41x slower                                                  |
| telco                      | 9.59 ms                                                | 13.5 ms: 1.41x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 5.05 ms: 1.45x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 3.40 ms: 1.45x slower                                                  |
| hexiom                     | 8.27 ms                                                | 12.1 ms: 1.46x slower                                                  |
| deltablue                  | 4.27 ms                                                | 6.42 ms: 1.50x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 8.84 ms: 1.51x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 37.3 ms: 1.51x slower                                                  |
| python_startup             | 23.7 ms                                                | 36.2 ms: 1.53x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.09 ms: 1.59x slower                                                  |
| nbody                      | 119 ms                                                 | 192 ms: 1.61x slower                                                   |
| mako                       | 15.7 ms                                                | 27.3 ms: 1.73x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 99.4 ms: 4.80x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.15x slower                                                           |

Benchmark hidden because not significant (5): deepcopy, xml_etree_parse, sqlglot_optimize, spectral_norm, async_generators
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.099x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.35x