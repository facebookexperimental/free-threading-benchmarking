# Results vs. 3.12.6

- fork: python
- ref: 9211b3dabeacb92713ac
- machine: linux-x86_64
- commit hash: 9211b3d
- commit date: 2025-02-28
- overall geometric mean: 1.057x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 305 ms: 1.16x slower                                                   |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                 |
| html5lib       | 63.6 ms                                                | 73.7 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 551 ms: 2.02x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.87x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 581 ms: 1.86x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 337 ms: 1.65x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 542 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 575 ms: 1.24x faster                                                   |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.3 ms: 1.06x faster                                                  |
| pidigits       | 184 ms                                                 | 210 ms: 1.14x slower                                                   |
| nbody          | 89.3 ms                                                | 135 ms: 1.51x slower                                                   |
| Geometric mean | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                  |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| regex_compile  | 142 ms                                                 | 157 ms: 1.10x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.4 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.8 ms: 1.10x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| json_loads           | 26.5 us                                                | 29.6 us: 1.11x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 2.36 sec: 1.12x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 95.4 ms: 1.12x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 251 us: 1.14x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 367 us: 1.19x slower                                                   |
| json_dumps           | 10.4 ms                                                | 13.1 ms: 1.26x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.64 ms: 1.35x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.0 ms: 1.19x slower                                                  |
| genshi_text     | 22.8 ms                                                | 27.9 ms: 1.22x slower                                                  |
| django_template | 34.7 ms                                                | 43.3 ms: 1.25x slower                                                  |
| mako            | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.71 ms: 2.02x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 551 ms: 2.02x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.87x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 581 ms: 1.86x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 337 ms: 1.65x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 542 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 575 ms: 1.24x faster                                                   |
| deepcopy                   | 352 us                                                 | 310 us: 1.13x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.86 ms: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 87.8 ms: 1.10x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                  |
| float                      | 80.8 ms                                                | 76.3 ms: 1.06x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 38.1 us: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                  |
| generators                 | 32.2 ms                                                | 31.3 ms: 1.03x faster                                                  |
| comprehensions             | 19.8 us                                                | 20.0 us: 1.01x slower                                                  |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.80 sec: 1.01x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                 |
| json                       | 5.02 ms                                                | 5.12 ms: 1.02x slower                                                  |
| logging_silent             | 109 ns                                                 | 112 ns: 1.03x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.17 us: 1.03x slower                                                  |
| spectral_norm              | 110 ms                                                 | 115 ms: 1.04x slower                                                   |
| dulwich_log                | 78.9 ms                                                | 82.6 ms: 1.05x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                 |
| raytrace                   | 299 ms                                                 | 319 ms: 1.06x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.7 ms: 1.09x slower                                                  |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.24 us: 1.09x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.78 ms: 1.10x slower                                                  |
| regex_compile              | 142 ms                                                 | 157 ms: 1.10x slower                                                   |
| chaos                      | 62.8 ms                                                | 69.3 ms: 1.10x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.68 sec: 1.11x slower                                                 |
| pyflate                    | 448 ms                                                 | 498 ms: 1.11x slower                                                   |
| thrift                     | 791 us                                                 | 881 us: 1.11x slower                                                   |
| scimark_sor                | 130 ms                                                 | 144 ms: 1.11x slower                                                   |
| json_loads                 | 26.5 us                                                | 29.6 us: 1.11x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.36 sec: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.4 ms: 1.12x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 188 ms: 1.13x slower                                                   |
| logging_format             | 7.35 us                                                | 8.32 us: 1.13x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 844 ms: 1.14x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 251 us: 1.14x slower                                                   |
| pidigits                   | 184 ms                                                 | 210 ms: 1.14x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.74 sec: 1.14x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 122 ms: 1.15x slower                                                   |
| crypto_pyaes               | 76.6 ms                                                | 88.0 ms: 1.15x slower                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.92 ms: 1.15x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 61.6 ms: 1.16x slower                                                  |
| html5lib                   | 63.6 ms                                                | 73.7 ms: 1.16x slower                                                  |
| 2to3                       | 264 ms                                                 | 305 ms: 1.16x slower                                                   |
| sympy_str                  | 292 ms                                                 | 341 ms: 1.17x slower                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.59 ms: 1.17x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 24.2 ms: 1.18x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.4 ms: 1.18x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.30 ms: 1.19x slower                                                  |
| richards                   | 45.9 ms                                                | 54.7 ms: 1.19x slower                                                  |
| sympy_expand               | 468 ms                                                 | 558 ms: 1.19x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 367 us: 1.19x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 60.0 ms: 1.19x slower                                                  |
| hexiom                     | 6.17 ms                                                | 7.45 ms: 1.21x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                                   |
| genshi_text                | 22.8 ms                                                | 27.9 ms: 1.22x slower                                                  |
| nqueens                    | 80.1 ms                                                | 98.1 ms: 1.23x slower                                                  |
| richards_super             | 51.9 ms                                                | 63.9 ms: 1.23x slower                                                  |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                                   |
| django_template            | 34.7 ms                                                | 43.3 ms: 1.25x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 13.1 ms: 1.26x slower                                                  |
| fannkuch                   | 372 ms                                                 | 494 ms: 1.33x slower                                                   |
| telco                      | 6.53 ms                                                | 8.75 ms: 1.34x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.64 ms: 1.35x slower                                                  |
| coverage                   | 71.4 ms                                                | 97.2 ms: 1.36x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 156 ms: 1.36x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 95.3 ms: 1.39x slower                                                  |
| scimark_fft                | 342 ms                                                 | 493 ms: 1.44x slower                                                   |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                  |
| nbody                      | 89.3 ms                                                | 135 ms: 1.51x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 7.76 ms: 1.77x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.31 ms: 3.52x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 95.0 ms: 8.80x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.057x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x