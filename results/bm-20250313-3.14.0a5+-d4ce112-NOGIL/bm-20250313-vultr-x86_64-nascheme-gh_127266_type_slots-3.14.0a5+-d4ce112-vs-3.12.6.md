# Results vs. 3.12.6

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: d4ce112
- commit date: 2025-03-13
- overall geometric mean: 1.044x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 296 ms: 1.12x slower                                                     |
| docutils       | 2.64 sec                                               | 2.81 sec: 1.06x slower                                                   |
| html5lib       | 63.6 ms                                                | 72.5 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                  | 1.11x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 556 ms: 1.99x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.88x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 585 ms: 1.85x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                     |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                     |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                     |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.03x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.5 ms: 1.04x faster                                                    |
| pidigits       | 184 ms                                                 | 187 ms: 1.02x slower                                                     |
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                                     |
| Geometric mean | (ref)                                                  | 1.13x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                    |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                     |
| regex_compile  | 142 ms                                                 | 157 ms: 1.11x slower                                                     |
| regex_v8       | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                    |
| Geometric mean | (ref)                                                  | 1.05x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 2.35 sec: 1.12x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 248 us: 1.13x slower                                                     |
| json_loads           | 26.5 us                                                | 30.9 us: 1.16x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 360 us: 1.17x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 70.5 ms: 1.20x slower                                                    |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                    |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.7 ms: 1.21x slower                                                    |
| django_template | 34.7 ms                                                | 42.5 ms: 1.22x slower                                                    |
| genshi_text     | 22.8 ms                                                | 28.6 ms: 1.25x slower                                                    |
| mako            | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.72 ms: 2.01x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 556 ms: 1.99x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.88x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 585 ms: 1.85x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                     |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.72 ms: 1.16x faster                                                    |
| deepcopy                   | 352 us                                                 | 308 us: 1.14x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 87.6 ms: 1.10x faster                                                    |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 73.1 ms: 1.08x faster                                                    |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                     |
| float                      | 80.8 ms                                                | 77.5 ms: 1.04x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 38.7 us: 1.04x faster                                                    |
| generators                 | 32.2 ms                                                | 31.3 ms: 1.03x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.03x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.79 sec: 1.01x slower                                                   |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                                     |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.01x slower                                                     |
| pidigits                   | 184 ms                                                 | 187 ms: 1.02x slower                                                     |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                   |
| deepcopy_reduce            | 3.08 us                                                | 3.14 us: 1.02x slower                                                    |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.04x slower                                                     |
| comprehensions             | 19.8 us                                                | 20.6 us: 1.04x slower                                                    |
| json                       | 5.02 ms                                                | 5.31 ms: 1.06x slower                                                    |
| docutils                   | 2.64 sec                                               | 2.81 sec: 1.06x slower                                                   |
| raytrace                   | 299 ms                                                 | 320 ms: 1.07x slower                                                     |
| mdp                        | 2.42 sec                                               | 2.60 sec: 1.08x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.15 us: 1.08x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.7 ms: 1.09x slower                                                    |
| chaos                      | 62.8 ms                                                | 69.0 ms: 1.10x slower                                                    |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                     |
| logging_format             | 7.35 us                                                | 8.10 us: 1.10x slower                                                    |
| regex_compile              | 142 ms                                                 | 157 ms: 1.11x slower                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.11x slower                                                     |
| deltablue                  | 3.45 ms                                                | 3.82 ms: 1.11x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.11x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.35 sec: 1.12x slower                                                   |
| pyflate                    | 448 ms                                                 | 500 ms: 1.12x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                    |
| thrift                     | 791 us                                                 | 888 us: 1.12x slower                                                     |
| 2to3                       | 264 ms                                                 | 296 ms: 1.12x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 248 us: 1.13x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 838 ms: 1.13x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.13x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 87.2 ms: 1.14x slower                                                    |
| html5lib                   | 63.6 ms                                                | 72.5 ms: 1.14x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.74 sec: 1.14x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.92 ms: 1.15x slower                                                    |
| sympy_str                  | 292 ms                                                 | 335 ms: 1.15x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 61.2 ms: 1.15x slower                                                    |
| scimark_fft                | 342 ms                                                 | 393 ms: 1.15x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                    |
| json_loads                 | 26.5 us                                                | 30.9 us: 1.16x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 23.9 ms: 1.16x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 360 us: 1.17x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 1.59 ms: 1.17x slower                                                    |
| sympy_expand               | 468 ms                                                 | 552 ms: 1.18x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.31 ms: 1.20x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 70.5 ms: 1.20x slower                                                    |
| hexiom                     | 6.17 ms                                                | 7.39 ms: 1.20x slower                                                    |
| richards                   | 45.9 ms                                                | 55.3 ms: 1.20x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 60.7 ms: 1.21x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 83.2 ms: 1.22x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                                     |
| django_template            | 34.7 ms                                                | 42.5 ms: 1.22x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                    |
| richards_super             | 51.9 ms                                                | 64.3 ms: 1.24x slower                                                    |
| genshi_text                | 22.8 ms                                                | 28.6 ms: 1.25x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 144 ms: 1.26x slower                                                     |
| nqueens                    | 80.1 ms                                                | 101 ms: 1.26x slower                                                     |
| meteor_contest             | 104 ms                                                 | 133 ms: 1.29x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.75 ms: 1.31x slower                                                    |
| fannkuch                   | 372 ms                                                 | 489 ms: 1.31x slower                                                     |
| telco                      | 6.53 ms                                                | 8.65 ms: 1.32x slower                                                    |
| coverage                   | 71.4 ms                                                | 96.2 ms: 1.35x slower                                                    |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                    |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.36x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 95.3 ms: 8.82x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                             |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, logging_silent
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250313-3.14.0a5+-d4ce112-NOGIL/bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.044x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.36x