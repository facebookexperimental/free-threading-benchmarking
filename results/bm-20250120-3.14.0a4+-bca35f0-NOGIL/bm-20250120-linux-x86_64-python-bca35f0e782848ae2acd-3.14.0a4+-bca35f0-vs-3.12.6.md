# Results vs. 3.12.6

- fork: python
- ref: bca35f0e782848ae2acd
- machine: linux-x86_64
- commit hash: bca35f0
- commit date: 2025-01-20
- overall geometric mean: 1.073x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 558 ms: 1.22x slower                                                   |
| docutils       | 4.00 sec                                               | 4.18 sec: 1.05x slower                                                 |
| html5lib       | 88.9 ms                                                | 107 ms: 1.21x slower                                                   |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 758 ms: 2.55x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 342 ms: 2.06x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 929 ms: 1.99x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 482 ms: 1.93x faster                                                   |
| async_tree_none            | 741 ms                                                 | 393 ms: 1.89x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 534 ms: 1.83x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 677 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 810 ms: 1.33x faster                                                   |
| coroutines                 | 29.5 ms                                                | 34.2 ms: 1.16x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.56x faster                                                           |

Benchmark hidden because not significant (2): async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 240 ms: 1.04x faster                                                   |
| nbody          | 119 ms                                                 | 185 ms: 1.55x slower                                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.06 ms: 1.26x faster                                                  |
| regex_dna      | 278 ms                                                 | 299 ms: 1.08x slower                                                   |
| regex_compile  | 187 ms                                                 | 204 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 148 ms: 1.15x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.11 sec: 1.08x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 138 ms: 1.09x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 486 us: 1.12x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 343 us: 1.14x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 102 ms: 1.22x slower                                                   |
| json_loads           | 37.9 us                                                | 46.7 us: 1.23x slower                                                  |
| json_dumps           | 14.3 ms                                                | 22.5 ms: 1.57x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.14x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 22.0 ms: 1.25x slower                                                  |
| python_startup         | 23.7 ms                                                | 34.2 ms: 1.44x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 87.3 ms: 1.29x slower                                                  |
| genshi_text     | 30.2 ms                                                | 40.5 ms: 1.34x slower                                                  |
| django_template | 44.9 ms                                                | 64.6 ms: 1.44x slower                                                  |
| mako            | 15.7 ms                                                | 25.0 ms: 1.59x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.41x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 758 ms: 2.55x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 342 ms: 2.06x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 929 ms: 1.99x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 482 ms: 1.93x faster                                                   |
| async_tree_none            | 741 ms                                                 | 393 ms: 1.89x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 534 ms: 1.83x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 677 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 810 ms: 1.33x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.06 ms: 1.26x faster                                                  |
| deepcopy                   | 468 us                                                 | 397 us: 1.18x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 148 ms: 1.15x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.58 sec: 1.13x faster                                                 |
| pidigits                   | 250 ms                                                 | 240 ms: 1.04x faster                                                   |
| docutils                   | 4.00 sec                                               | 4.18 sec: 1.05x slower                                                 |
| mdp                        | 3.97 sec                                               | 4.17 sec: 1.05x slower                                                 |
| logging_silent             | 139 ns                                                 | 147 ns: 1.05x slower                                                   |
| regex_dna                  | 278 ms                                                 | 299 ms: 1.08x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.11 sec: 1.08x slower                                                 |
| sqlglot_optimize           | 76.0 ms                                                | 82.3 ms: 1.08x slower                                                  |
| sqlglot_normalize          | 157 ms                                                 | 170 ms: 1.08x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 138 ms: 1.09x slower                                                   |
| go                         | 172 ms                                                 | 188 ms: 1.09x slower                                                   |
| dulwich_log                | 100 ms                                                 | 109 ms: 1.09x slower                                                   |
| regex_compile              | 187 ms                                                 | 204 ms: 1.09x slower                                                   |
| sqlite_synth               | 3.87 us                                                | 4.28 us: 1.11x slower                                                  |
| pyflate                    | 727 ms                                                 | 807 ms: 1.11x slower                                                   |
| nqueens                    | 117 ms                                                 | 130 ms: 1.11x slower                                                   |
| chaos                      | 84.9 ms                                                | 94.3 ms: 1.11x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 486 us: 1.12x slower                                                   |
| scimark_fft                | 500 ms                                                 | 559 ms: 1.12x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 121 ms: 1.13x slower                                                   |
| scimark_sor                | 167 ms                                                 | 189 ms: 1.13x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.25 sec: 1.14x slower                                                 |
| json                       | 6.85 ms                                                | 7.80 ms: 1.14x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.10 sec: 1.14x slower                                                 |
| unpickle_pure_python       | 300 us                                                 | 343 us: 1.14x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 176 ms: 1.16x slower                                                   |
| coroutines                 | 29.5 ms                                                | 34.2 ms: 1.16x slower                                                  |
| sympy_expand               | 582 ms                                                 | 682 ms: 1.17x slower                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 7.77 sec: 1.18x slower                                                 |
| raytrace                   | 408 ms                                                 | 484 ms: 1.19x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 264 ms: 1.19x slower                                                   |
| meteor_contest             | 146 ms                                                 | 175 ms: 1.19x slower                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.80 ms: 1.20x slower                                                  |
| fannkuch                   | 540 ms                                                 | 652 ms: 1.21x slower                                                   |
| html5lib                   | 88.9 ms                                                | 107 ms: 1.21x slower                                                   |
| generators                 | 41.1 ms                                                | 50.2 ms: 1.22x slower                                                  |
| 2to3                       | 456 ms                                                 | 558 ms: 1.22x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 102 ms: 1.22x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 118 ms: 1.22x slower                                                   |
| json_loads                 | 37.9 us                                                | 46.7 us: 1.23x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 22.0 ms: 1.25x slower                                                  |
| richards_super             | 72.8 ms                                                | 92.3 ms: 1.27x slower                                                  |
| logging_simple             | 9.45 us                                                | 12.0 us: 1.27x slower                                                  |
| logging_format             | 9.59 us                                                | 12.2 us: 1.27x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.51 ms: 1.27x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 37.9 ms: 1.27x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 31.8 ms: 1.29x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 87.3 ms: 1.29x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.34 ms: 1.31x slower                                                  |
| genshi_text                | 30.2 ms                                                | 40.5 ms: 1.34x slower                                                  |
| sympy_str                  | 385 ms                                                 | 516 ms: 1.34x slower                                                   |
| richards                   | 60.3 ms                                                | 81.5 ms: 1.35x slower                                                  |
| hexiom                     | 8.27 ms                                                | 11.5 ms: 1.39x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 315 us: 1.41x slower                                                   |
| bench_thread_pool          | 3.48 ms                                                | 5.00 ms: 1.44x slower                                                  |
| django_template            | 44.9 ms                                                | 64.6 ms: 1.44x slower                                                  |
| python_startup             | 23.7 ms                                                | 34.2 ms: 1.44x slower                                                  |
| telco                      | 9.59 ms                                                | 13.9 ms: 1.45x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.83 ms: 1.46x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.55 ms: 1.46x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 8.60 ms: 1.47x slower                                                  |
| coverage                   | 95.4 ms                                                | 141 ms: 1.48x slower                                                   |
| nbody                      | 119 ms                                                 | 185 ms: 1.55x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 22.5 ms: 1.57x slower                                                  |
| mako                       | 15.7 ms                                                | 25.0 ms: 1.59x slower                                                  |
| deltablue                  | 4.27 ms                                                | 7.35 ms: 1.72x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 94.1 ms: 4.55x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.11x slower                                                           |

Benchmark hidden because not significant (12): float, async_generators, comprehensions, pathlib, regex_v8, pylint, xml_etree_parse, deepcopy_memo, deepcopy_reduce, asyncio_websockets, spectral_norm, sqlalchemy_declarative
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.073x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.34x