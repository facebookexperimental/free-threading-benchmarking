# Results vs. 3.13.0rc2

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 9f143eb
- commit date: 2025-02-12
- overall geometric mean: 1.078x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 305 ms: 1.17x slower                                              |
| docutils       | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                            |
| html5lib       | 68.6 ms                                                                | 71.8 ms: 1.05x slower                                             |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 574 ms: 1.57x faster                                              |
| async_tree_io              | 881 ms                                                                 | 602 ms: 1.46x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 352 ms: 1.31x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 318 ms: 1.29x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 262 ms: 1.27x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 503 ms: 1.26x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 534 ms: 1.25x faster                                              |
| async_tree_none            | 353 ms                                                                 | 287 ms: 1.23x faster                                              |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.23x faster                                                      |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 199 ms: 1.09x faster                                              |
| float          | 76.7 ms                                                                | 75.3 ms: 1.02x faster                                             |
| nbody          | 85.3 ms                                                                | 132 ms: 1.55x slower                                              |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.80 ms: 1.14x faster                                             |
| regex_dna      | 189 ms                                                                 | 178 ms: 1.06x faster                                              |
| regex_v8       | 23.2 ms                                                                | 23.6 ms: 1.02x slower                                             |
| regex_compile  | 131 ms                                                                 | 151 ms: 1.15x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.0 ms: 1.08x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 127 ms: 1.07x faster                                              |
| json_loads           | 27.3 us                                                                | 31.2 us: 1.14x slower                                             |
| xml_etree_generate   | 85.4 ms                                                                | 97.6 ms: 1.14x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.33 sec: 1.16x slower                                            |
| xml_etree_process    | 59.2 ms                                                                | 68.8 ms: 1.16x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 245 us: 1.18x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 358 us: 1.23x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.69 ms: 1.31x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.40x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.2 ms: 1.21x slower                                             |
| django_template | 34.2 ms                                                                | 41.7 ms: 1.22x slower                                             |
| genshi_text     | 21.7 ms                                                                | 27.9 ms: 1.28x slower                                             |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.78 ms: 1.87x faster                                             |
| async_tree_io_tg           | 901 ms                                                                 | 574 ms: 1.57x faster                                              |
| async_tree_io              | 881 ms                                                                 | 602 ms: 1.46x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 352 ms: 1.31x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 318 ms: 1.29x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 262 ms: 1.27x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 503 ms: 1.26x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 534 ms: 1.25x faster                                              |
| async_tree_none            | 353 ms                                                                 | 287 ms: 1.23x faster                                              |
| deepcopy                   | 357 us                                                                 | 307 us: 1.16x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 2.80 ms: 1.14x faster                                             |
| sqlite_synth               | 2.25 us                                                                | 2.00 us: 1.12x faster                                             |
| pidigits                   | 216 ms                                                                 | 199 ms: 1.09x faster                                              |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.0 ms: 1.08x faster                                             |
| xml_etree_parse            | 136 ms                                                                 | 127 ms: 1.07x faster                                              |
| regex_dna                  | 189 ms                                                                 | 178 ms: 1.06x faster                                              |
| float                      | 76.7 ms                                                                | 75.3 ms: 1.02x faster                                             |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                              |
| deepcopy_memo              | 38.1 us                                                                | 37.7 us: 1.01x faster                                             |
| spectral_norm              | 108 ms                                                                 | 107 ms: 1.01x faster                                              |
| go                         | 141 ms                                                                 | 140 ms: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                              |
| pathlib                    | 19.3 ms                                                                | 19.2 ms: 1.00x faster                                             |
| regex_v8                   | 23.2 ms                                                                | 23.6 ms: 1.02x slower                                             |
| deepcopy_reduce            | 3.12 us                                                                | 3.25 us: 1.04x slower                                             |
| html5lib                   | 68.6 ms                                                                | 71.8 ms: 1.05x slower                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.68 sec: 1.05x slower                                            |
| docutils                   | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                            |
| create_gc_cycles           | 1.33 ms                                                                | 1.42 ms: 1.07x slower                                             |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                            |
| json                       | 4.98 ms                                                                | 5.41 ms: 1.08x slower                                             |
| mdp                        | 2.34 sec                                                               | 2.57 sec: 1.10x slower                                            |
| logging_silent             | 98.2 ns                                                                | 108 ns: 1.10x slower                                              |
| telco                      | 7.77 ms                                                                | 8.64 ms: 1.11x slower                                             |
| dulwich_log                | 74.5 ms                                                                | 82.9 ms: 1.11x slower                                             |
| pprint_safe_repr           | 719 ms                                                                 | 804 ms: 1.12x slower                                              |
| generators                 | 28.5 ms                                                                | 32.1 ms: 1.12x slower                                             |
| pyflate                    | 449 ms                                                                 | 507 ms: 1.13x slower                                              |
| sqlglot_normalize          | 106 ms                                                                 | 120 ms: 1.13x slower                                              |
| json_loads                 | 27.3 us                                                                | 31.2 us: 1.14x slower                                             |
| xml_etree_generate         | 85.4 ms                                                                | 97.6 ms: 1.14x slower                                             |
| thrift                     | 772 us                                                                 | 884 us: 1.15x slower                                              |
| scimark_fft                | 348 ms                                                                 | 399 ms: 1.15x slower                                              |
| regex_compile              | 131 ms                                                                 | 151 ms: 1.15x slower                                              |
| pprint_pformat             | 1.46 sec                                                               | 1.68 sec: 1.15x slower                                            |
| sqlglot_optimize           | 52.7 ms                                                                | 60.9 ms: 1.16x slower                                             |
| tomli_loads                | 2.01 sec                                                               | 2.33 sec: 1.16x slower                                            |
| xml_etree_process          | 59.2 ms                                                                | 68.8 ms: 1.16x slower                                             |
| 2to3                       | 259 ms                                                                 | 305 ms: 1.17x slower                                              |
| coverage                   | 82.5 ms                                                                | 97.1 ms: 1.18x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 245 us: 1.18x slower                                              |
| logging_simple             | 6.14 us                                                                | 7.26 us: 1.18x slower                                             |
| logging_format             | 6.92 us                                                                | 8.22 us: 1.19x slower                                             |
| json_dumps                 | 10.6 ms                                                                | 12.7 ms: 1.19x slower                                             |
| comprehensions             | 16.6 us                                                                | 19.8 us: 1.20x slower                                             |
| genshi_xml                 | 49.1 ms                                                                | 59.2 ms: 1.21x slower                                             |
| sympy_sum                  | 154 ms                                                                 | 188 ms: 1.22x slower                                              |
| django_template            | 34.2 ms                                                                | 41.7 ms: 1.22x slower                                             |
| sympy_expand               | 454 ms                                                                 | 555 ms: 1.22x slower                                              |
| pickle_pure_python         | 292 us                                                                 | 358 us: 1.23x slower                                              |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.84 ms: 1.23x slower                                             |
| sqlglot_transpile          | 1.55 ms                                                                | 1.91 ms: 1.23x slower                                             |
| sympy_str                  | 274 ms                                                                 | 338 ms: 1.23x slower                                              |
| sympy_integrate            | 19.7 ms                                                                | 24.5 ms: 1.24x slower                                             |
| nqueens                    | 77.7 ms                                                                | 96.8 ms: 1.24x slower                                             |
| hexiom                     | 5.95 ms                                                                | 7.42 ms: 1.25x slower                                             |
| chaos                      | 56.3 ms                                                                | 70.3 ms: 1.25x slower                                             |
| deltablue                  | 3.10 ms                                                                | 3.88 ms: 1.25x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 196 us: 1.26x slower                                              |
| richards                   | 44.4 ms                                                                | 55.9 ms: 1.26x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 142 ms: 1.26x slower                                              |
| sqlglot_parse              | 1.25 ms                                                                | 1.60 ms: 1.28x slower                                             |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                              |
| genshi_text                | 21.7 ms                                                                | 27.9 ms: 1.28x slower                                             |
| richards_super             | 50.4 ms                                                                | 64.7 ms: 1.28x slower                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 85.1 ms: 1.29x slower                                             |
| raytrace                   | 250 ms                                                                 | 324 ms: 1.30x slower                                              |
| python_startup_no_site     | 7.41 ms                                                                | 9.69 ms: 1.31x slower                                             |
| fannkuch                   | 376 ms                                                                 | 493 ms: 1.31x slower                                              |
| crypto_pyaes               | 68.2 ms                                                                | 90.5 ms: 1.33x slower                                             |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.40x slower                                             |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                             |
| nbody                      | 85.3 ms                                                                | 132 ms: 1.55x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 3.33 ms: 3.60x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 95.6 ms: 8.69x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                      |

Benchmark hidden because not significant (3): scimark_sor, coroutines, pylint
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250212-3.14.0a4+-9f143eb-NOGIL/bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-9f143eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.078x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x