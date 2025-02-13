# Results vs. 3.12.6

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 9f143eb
- commit date: 2025-02-12
- overall geometric mean: 1.046x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 305 ms: 1.16x slower                                              |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                            |
| html5lib       | 63.6 ms                                                | 71.8 ms: 1.13x slower                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 574 ms: 1.93x faster                                              |
| async_tree_io              | 1.08 sec                                               | 602 ms: 1.80x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                              |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 503 ms: 1.44x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 534 ms: 1.34x faster                                              |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                             |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.00x faster                                              |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.3 ms: 1.07x faster                                             |
| pidigits       | 184 ms                                                 | 199 ms: 1.08x slower                                              |
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                              |
| Geometric mean | (ref)                                                  | 1.14x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                             |
| regex_dna      | 168 ms                                                 | 178 ms: 1.06x slower                                              |
| regex_compile  | 142 ms                                                 | 151 ms: 1.06x slower                                              |
| regex_v8       | 20.6 ms                                                | 23.6 ms: 1.15x slower                                             |
| Geometric mean | (ref)                                                  | 1.03x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.0 ms: 1.11x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                              |
| tomli_loads          | 2.11 sec                                               | 2.33 sec: 1.11x slower                                            |
| unpickle_pure_python | 221 us                                                 | 245 us: 1.11x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 97.6 ms: 1.15x slower                                             |
| pickle_pure_python   | 308 us                                                 | 358 us: 1.16x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 68.8 ms: 1.17x slower                                             |
| json_loads           | 26.5 us                                                | 31.2 us: 1.18x slower                                             |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.22x slower                                             |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.69 ms: 1.35x slower                                             |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                             |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.2 ms: 1.18x slower                                             |
| django_template | 34.7 ms                                                | 41.7 ms: 1.20x slower                                             |
| genshi_text     | 22.8 ms                                                | 27.9 ms: 1.22x slower                                             |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                             |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.95x faster                                             |
| async_tree_io_tg           | 1.11 sec                                               | 574 ms: 1.93x faster                                              |
| async_tree_io              | 1.08 sec                                               | 602 ms: 1.80x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                              |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 503 ms: 1.44x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 534 ms: 1.34x faster                                              |
| deepcopy                   | 352 us                                                 | 307 us: 1.15x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                             |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 87.0 ms: 1.11x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.00 us: 1.10x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                              |
| float                      | 80.8 ms                                                | 75.3 ms: 1.07x faster                                             |
| deepcopy_memo              | 40.3 us                                                | 37.7 us: 1.07x faster                                             |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                              |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                             |
| bpe_tokeniser              | 4.74 sec                                               | 4.68 sec: 1.01x faster                                            |
| generators                 | 32.2 ms                                                | 32.1 ms: 1.01x faster                                             |
| asyncio_websockets         | 517 ms                                                 | 514 ms: 1.00x faster                                              |
| scimark_sor                | 130 ms                                                 | 133 ms: 1.02x slower                                              |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.03x slower                                            |
| dulwich_log                | 78.9 ms                                                | 82.9 ms: 1.05x slower                                             |
| deepcopy_reduce            | 3.08 us                                                | 3.25 us: 1.05x slower                                             |
| regex_dna                  | 168 ms                                                 | 178 ms: 1.06x slower                                              |
| regex_compile              | 142 ms                                                 | 151 ms: 1.06x slower                                              |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                            |
| mdp                        | 2.42 sec                                               | 2.57 sec: 1.06x slower                                            |
| json                       | 5.02 ms                                                | 5.41 ms: 1.08x slower                                             |
| pidigits                   | 184 ms                                                 | 199 ms: 1.08x slower                                              |
| pprint_safe_repr           | 743 ms                                                 | 804 ms: 1.08x slower                                              |
| raytrace                   | 299 ms                                                 | 324 ms: 1.08x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 156 ms: 1.09x slower                                              |
| logging_simple             | 6.63 us                                                | 7.26 us: 1.10x slower                                             |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.10x slower                                            |
| tomli_loads                | 2.11 sec                                               | 2.33 sec: 1.11x slower                                            |
| unpickle_pure_python       | 221 us                                                 | 245 us: 1.11x slower                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.3 ms: 1.12x slower                                             |
| thrift                     | 791 us                                                 | 884 us: 1.12x slower                                              |
| chaos                      | 62.8 ms                                                | 70.3 ms: 1.12x slower                                             |
| logging_format             | 7.35 us                                                | 8.22 us: 1.12x slower                                             |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.12x slower                                              |
| deltablue                  | 3.45 ms                                                | 3.88 ms: 1.13x slower                                             |
| html5lib                   | 63.6 ms                                                | 71.8 ms: 1.13x slower                                             |
| pyflate                    | 448 ms                                                 | 507 ms: 1.13x slower                                              |
| sympy_sum                  | 166 ms                                                 | 188 ms: 1.13x slower                                              |
| sqlglot_optimize           | 53.3 ms                                                | 60.9 ms: 1.14x slower                                             |
| xml_etree_generate         | 85.2 ms                                                | 97.6 ms: 1.15x slower                                             |
| sqlglot_transpile          | 1.67 ms                                                | 1.91 ms: 1.15x slower                                             |
| regex_v8                   | 20.6 ms                                                | 23.6 ms: 1.15x slower                                             |
| 2to3                       | 264 ms                                                 | 305 ms: 1.16x slower                                              |
| sympy_str                  | 292 ms                                                 | 338 ms: 1.16x slower                                              |
| pickle_pure_python         | 308 us                                                 | 358 us: 1.16x slower                                              |
| xml_etree_process          | 59.0 ms                                                | 68.8 ms: 1.17x slower                                             |
| scimark_fft                | 342 ms                                                 | 399 ms: 1.17x slower                                              |
| json_loads                 | 26.5 us                                                | 31.2 us: 1.18x slower                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.60 ms: 1.18x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 59.2 ms: 1.18x slower                                             |
| crypto_pyaes               | 76.6 ms                                                | 90.5 ms: 1.18x slower                                             |
| sympy_expand               | 468 ms                                                 | 555 ms: 1.19x slower                                              |
| sympy_integrate            | 20.5 ms                                                | 24.5 ms: 1.19x slower                                             |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                              |
| django_template            | 34.7 ms                                                | 41.7 ms: 1.20x slower                                             |
| hexiom                     | 6.17 ms                                                | 7.42 ms: 1.20x slower                                             |
| nqueens                    | 80.1 ms                                                | 96.8 ms: 1.21x slower                                             |
| richards                   | 45.9 ms                                                | 55.9 ms: 1.22x slower                                             |
| genshi_text                | 22.8 ms                                                | 27.9 ms: 1.22x slower                                             |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.22x slower                                             |
| scimark_lu                 | 114 ms                                                 | 142 ms: 1.24x slower                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 85.1 ms: 1.24x slower                                             |
| richards_super             | 51.9 ms                                                | 64.7 ms: 1.25x slower                                             |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.42 ms: 1.30x slower                                             |
| telco                      | 6.53 ms                                                | 8.64 ms: 1.32x slower                                             |
| fannkuch                   | 372 ms                                                 | 493 ms: 1.32x slower                                              |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.84 ms: 1.33x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.69 ms: 1.35x slower                                             |
| coverage                   | 71.4 ms                                                | 97.1 ms: 1.36x slower                                             |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                             |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                              |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.33 ms: 3.54x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 95.6 ms: 8.85x slower                                             |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                      |

Benchmark hidden because not significant (4): logging_silent, comprehensions, go, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250212-3.14.0a4+-9f143eb-NOGIL/bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.046x slower

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x