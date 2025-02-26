# Results vs. 3.12.6

- fork: python
- ref: 0ef4ffeefd1737c18dc9
- machine: linux-x86_64
- commit hash: 0ef4ffe
- commit date: 2025-02-25
- overall geometric mean: 1.012x slower
- HPT reliability: 99.78%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 514 ms: 1.13x slower                                                   |
| docutils       | 4.00 sec                                               | 4.22 sec: 1.06x slower                                                 |
| html5lib       | 88.9 ms                                                | 98.2 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 726 ms: 2.67x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 822 ms: 2.25x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 334 ms: 2.11x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 459 ms: 2.03x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 524 ms: 1.86x faster                                                   |
| async_tree_none            | 741 ms                                                 | 406 ms: 1.83x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 681 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 758 ms: 1.42x faster                                                   |
| async_generators           | 589 ms                                                 | 556 ms: 1.06x faster                                                   |
| coroutines                 | 29.5 ms                                                | 30.8 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.62x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 103 ms: 1.19x faster                                                   |
| nbody          | 119 ms                                                 | 174 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.50 ms: 1.14x faster                                                  |
| regex_compile  | 187 ms                                                 | 197 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 147 ms: 1.15x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 222 ms: 1.08x faster                                                   |
| unpickle_pure_python | 300 us                                                 | 315 us: 1.05x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 88.5 ms: 1.06x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 3.07 sec: 1.06x slower                                                 |
| pickle_pure_python   | 436 us                                                 | 464 us: 1.06x slower                                                   |
| json_loads           | 37.9 us                                                | 43.4 us: 1.15x slower                                                  |
| json_dumps           | 14.3 ms                                                | 17.8 ms: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.3 ms: 1.21x slower                                                  |
| python_startup         | 23.7 ms                                                | 33.2 ms: 1.40x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.30x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 55.1 ms: 1.23x slower                                                  |
| genshi_text     | 30.2 ms                                                | 37.2 ms: 1.23x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 84.1 ms: 1.24x slower                                                  |
| mako            | 15.7 ms                                                | 23.2 ms: 1.48x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.29x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 726 ms: 2.67x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 822 ms: 2.25x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 334 ms: 2.11x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 459 ms: 2.03x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 524 ms: 1.86x faster                                                   |
| async_tree_none            | 741 ms                                                 | 406 ms: 1.83x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 681 ms: 1.62x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 3.72 ms: 1.58x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 758 ms: 1.42x faster                                                   |
| float                      | 123 ms                                                 | 103 ms: 1.19x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.52 sec: 1.18x faster                                                 |
| deepcopy                   | 468 us                                                 | 404 us: 1.16x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 147 ms: 1.15x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.50 ms: 1.14x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.44 us: 1.12x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 222 ms: 1.08x faster                                                   |
| async_generators           | 589 ms                                                 | 556 ms: 1.06x faster                                                   |
| spectral_norm              | 156 ms                                                 | 147 ms: 1.06x faster                                                   |
| mdp                        | 3.97 sec                                               | 4.11 sec: 1.03x slower                                                 |
| coroutines                 | 29.5 ms                                                | 30.8 ms: 1.04x slower                                                  |
| pyflate                    | 727 ms                                                 | 765 ms: 1.05x slower                                                   |
| deepcopy_reduce            | 4.04 us                                                | 4.25 us: 1.05x slower                                                  |
| go                         | 172 ms                                                 | 181 ms: 1.05x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 315 us: 1.05x slower                                                   |
| scimark_sor                | 167 ms                                                 | 176 ms: 1.05x slower                                                   |
| regex_compile              | 187 ms                                                 | 197 ms: 1.05x slower                                                   |
| docutils                   | 4.00 sec                                               | 4.22 sec: 1.06x slower                                                 |
| xml_etree_process          | 83.7 ms                                                | 88.5 ms: 1.06x slower                                                  |
| dulwich_log                | 100 ms                                                 | 106 ms: 1.06x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.07 sec: 1.06x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 464 us: 1.06x slower                                                   |
| scimark_fft                | 500 ms                                                 | 533 ms: 1.07x slower                                                   |
| logging_format             | 9.59 us                                                | 10.2 us: 1.07x slower                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 235 ms: 1.08x slower                                                   |
| raytrace                   | 408 ms                                                 | 443 ms: 1.09x slower                                                   |
| json                       | 6.85 ms                                                | 7.46 ms: 1.09x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 2.55 ms: 1.09x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 245 ms: 1.10x slower                                                   |
| html5lib                   | 88.9 ms                                                | 98.2 ms: 1.10x slower                                                  |
| chaos                      | 84.9 ms                                                | 94.1 ms: 1.11x slower                                                  |
| sympy_str                  | 385 ms                                                 | 430 ms: 1.12x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 120 ms: 1.12x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 108 ms: 1.12x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.19 ms: 1.12x slower                                                  |
| 2to3                       | 456 ms                                                 | 514 ms: 1.13x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 33.8 ms: 1.13x slower                                                  |
| generators                 | 41.1 ms                                                | 47.0 ms: 1.14x slower                                                  |
| richards_super             | 72.8 ms                                                | 83.4 ms: 1.15x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 7.55 sec: 1.15x slower                                                 |
| json_loads                 | 37.9 us                                                | 43.4 us: 1.15x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.29 sec: 1.16x slower                                                 |
| scimark_lu                 | 152 ms                                                 | 177 ms: 1.16x slower                                                   |
| bench_thread_pool          | 3.48 ms                                                | 4.06 ms: 1.17x slower                                                  |
| nqueens                    | 117 ms                                                 | 137 ms: 1.18x slower                                                   |
| richards                   | 60.3 ms                                                | 71.2 ms: 1.18x slower                                                  |
| meteor_contest             | 146 ms                                                 | 173 ms: 1.18x slower                                                   |
| pprint_safe_repr           | 967 ms                                                 | 1.15 sec: 1.19x slower                                                 |
| sqlalchemy_imperative      | 24.7 ms                                                | 29.3 ms: 1.19x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.05 ms: 1.20x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 21.3 ms: 1.21x slower                                                  |
| sympy_expand               | 582 ms                                                 | 711 ms: 1.22x slower                                                   |
| django_template            | 44.9 ms                                                | 55.1 ms: 1.23x slower                                                  |
| genshi_text                | 30.2 ms                                                | 37.2 ms: 1.23x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.22 ms: 1.24x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 84.1 ms: 1.24x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 17.8 ms: 1.24x slower                                                  |
| hexiom                     | 8.27 ms                                                | 10.5 ms: 1.27x slower                                                  |
| fannkuch                   | 540 ms                                                 | 684 ms: 1.27x slower                                                   |
| deltablue                  | 4.27 ms                                                | 5.40 ms: 1.27x slower                                                  |
| telco                      | 9.59 ms                                                | 12.2 ms: 1.27x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.48 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 289 us: 1.29x slower                                                   |
| python_startup             | 23.7 ms                                                | 33.2 ms: 1.40x slower                                                  |
| nbody                      | 119 ms                                                 | 174 ms: 1.46x slower                                                   |
| mako                       | 15.7 ms                                                | 23.2 ms: 1.48x slower                                                  |
| coverage                   | 95.4 ms                                                | 146 ms: 1.53x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 87.6 ms: 4.23x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (13): xml_etree_generate, sqlglot_normalize, logging_simple, regex_v8, pylint, pidigits, asyncio_websockets, logging_silent, comprehensions, regex_dna, deepcopy_memo, pathlib, sqlglot_optimize
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.012x slower

# HPT report

- Reliability score: 99.78% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x