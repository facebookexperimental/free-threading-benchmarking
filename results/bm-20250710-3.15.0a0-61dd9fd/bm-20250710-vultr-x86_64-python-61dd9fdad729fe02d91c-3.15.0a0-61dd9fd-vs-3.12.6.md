# Results vs. 3.12.6

- fork: python
- ref: 61dd9fdad729fe02d91c
- machine: linux-x86_64
- commit hash: 61dd9fd
- commit date: 2025-07-10
- overall geometric mean: 1.067x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 251 ms: 1.05x faster                                                  |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                |
| html5lib       | 63.6 ms                                                | 61.2 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 256 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 598 ms: 1.81x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 613 ms: 1.81x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 314 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 490 ms: 1.46x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 496 ms: 1.46x faster                                                  |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.8 ms: 1.14x faster                                                 |
| nbody          | 89.3 ms                                                | 93.6 ms: 1.05x slower                                                 |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                 |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.93 sec: 1.09x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 211 us: 1.04x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.9 ms: 1.04x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 82.7 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 57.7 ms: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 309 us: 1.00x slower                                                  |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                 |
| json_loads           | 26.5 us                                                | 28.7 us: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.35 ms: 1.03x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 48.4 ms: 1.04x faster                                                 |
| django_template | 34.7 ms                                                | 34.1 ms: 1.02x faster                                                 |
| mako            | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.10x faster                                                |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.81x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 598 ms: 1.81x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 613 ms: 1.81x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 314 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 490 ms: 1.46x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 496 ms: 1.46x faster                                                  |
| deepcopy                   | 352 us                                                 | 251 us: 1.40x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.2 us: 1.38x faster                                                 |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.6 us: 1.27x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 65.8 ms: 1.20x faster                                                 |
| raytrace                   | 299 ms                                                 | 254 ms: 1.18x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.62 us: 1.18x faster                                                 |
| scimark_sor                | 130 ms                                                 | 111 ms: 1.17x faster                                                  |
| generators                 | 32.2 ms                                                | 27.7 ms: 1.17x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                 |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                  |
| float                      | 80.8 ms                                                | 70.8 ms: 1.14x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.17 sec: 1.14x faster                                                |
| async_generators           | 384 ms                                                 | 339 ms: 1.13x faster                                                  |
| pyflate                    | 448 ms                                                 | 396 ms: 1.13x faster                                                  |
| chaos                      | 62.8 ms                                                | 55.7 ms: 1.13x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.88 us: 1.13x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 68.2 ms: 1.12x faster                                                 |
| richards                   | 45.9 ms                                                | 40.9 ms: 1.12x faster                                                 |
| spectral_norm              | 110 ms                                                 | 98.8 ms: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.11x faster                                                 |
| richards_super             | 51.9 ms                                                | 46.6 ms: 1.11x faster                                                 |
| logging_format             | 7.35 us                                                | 6.61 us: 1.11x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.10 ms: 1.11x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.6 ms: 1.11x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 62.3 ms: 1.10x faster                                                 |
| logging_silent             | 109 ns                                                 | 99.3 ns: 1.10x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.63 ms: 1.10x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.93 sec: 1.09x faster                                                |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                  |
| sympy_str                  | 292 ms                                                 | 269 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.07x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 695 ms: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.07x faster                                                |
| 2to3                       | 264 ms                                                 | 251 ms: 1.05x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                  |
| meteor_contest             | 104 ms                                                 | 98.7 ms: 1.05x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 211 us: 1.04x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 92.9 ms: 1.04x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                 |
| html5lib                   | 63.6 ms                                                | 61.2 ms: 1.04x faster                                                 |
| thrift                     | 791 us                                                 | 763 us: 1.04x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.4 ms: 1.04x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.03x faster                                                |
| xml_etree_generate         | 85.2 ms                                                | 82.7 ms: 1.03x faster                                                 |
| nqueens                    | 80.1 ms                                                | 78.1 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 57.7 ms: 1.02x faster                                                 |
| django_template            | 34.7 ms                                                | 34.1 ms: 1.02x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                                  |
| scimark_fft                | 342 ms                                                 | 338 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 309 us: 1.00x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.24 us: 1.02x slower                                                 |
| fannkuch                   | 372 ms                                                 | 380 ms: 1.02x slower                                                  |
| json                       | 5.02 ms                                                | 5.15 ms: 1.03x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.35 ms: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                 |
| nbody                      | 89.3 ms                                                | 93.6 ms: 1.05x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.7 us: 1.08x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.93 ms: 1.12x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.9 ms: 1.15x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.37 ms: 1.27x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.97 ms: 1.81x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.55x slower                                                  |
| telco                      | 6.53 ms                                                | 160 ms: 24.46x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, sympy_expand
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.067x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x