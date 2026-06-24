# Results vs. 3.13.0rc2

- fork: kumaraditya303
- ref: mrocache
- machine: linux-x86_64
- commit hash: 4fbec93
- commit date: 2026-06-16
- overall geometric mean: 1.075x slower
- HPT reliability: 98.77%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 297 ms: 1.15x slower                                              |
| docutils       | 2.63 sec                                                               | 2.93 sec: 1.12x slower                                            |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                      |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 681 ms: 1.32x faster                                              |
| async_tree_io              | 881 ms                                                                 | 709 ms: 1.24x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 605 ms: 1.10x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 578 ms: 1.10x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 420 ms: 1.09x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 394 ms: 1.04x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 324 ms: 1.03x faster                                              |
| async_tree_none            | 353 ms                                                                 | 345 ms: 1.02x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                              |
| async_generators           | 375 ms                                                                 | 390 ms: 1.04x slower                                              |
| coroutines                 | 23.3 ms                                                                | 25.0 ms: 1.07x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.07x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 188 ms: 1.15x faster                                              |
| float          | 76.7 ms                                                                | 86.9 ms: 1.13x slower                                             |
| nbody          | 85.3 ms                                                                | 125 ms: 1.47x slower                                              |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                             |
| regex_effbot   | 3.21 ms                                                                | 3.14 ms: 1.02x faster                                             |
| regex_dna      | 189 ms                                                                 | 188 ms: 1.00x faster                                              |
| regex_compile  | 131 ms                                                                 | 142 ms: 1.08x slower                                              |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.98 sec: 1.01x faster                                            |
| json_dumps           | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                             |
| xml_etree_iterparse  | 94.4 ms                                                                | 95.7 ms: 1.01x slower                                             |
| xml_etree_parse      | 136 ms                                                                 | 142 ms: 1.04x slower                                              |
| json_loads           | 27.3 us                                                                | 29.8 us: 1.09x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 239 us: 1.15x slower                                              |
| pickle_pure_python   | 292 us                                                                 | 335 us: 1.15x slower                                              |
| xml_etree_generate   | 85.4 ms                                                                | 102 ms: 1.19x slower                                              |
| xml_etree_process    | 59.2 ms                                                                | 75.8 ms: 1.28x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.18 ms: 1.24x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.32x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 41.8 ms: 1.22x slower                                             |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.32x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 134 ms: 2.37x faster                                              |
| gc_traversal               | 3.32 ms                                                                | 1.78 ms: 1.87x faster                                             |
| mdp                        | 2.34 sec                                                               | 1.32 sec: 1.77x faster                                            |
| bench_mp_pool              | 11.0 ms                                                                | 6.76 ms: 1.63x faster                                             |
| deepcopy                   | 357 us                                                                 | 267 us: 1.34x faster                                              |
| async_tree_io_tg           | 901 ms                                                                 | 681 ms: 1.32x faster                                              |
| async_tree_io              | 881 ms                                                                 | 709 ms: 1.24x faster                                              |
| deepcopy_memo              | 38.1 us                                                                | 31.4 us: 1.21x faster                                             |
| go                         | 141 ms                                                                 | 122 ms: 1.15x faster                                              |
| pidigits                   | 216 ms                                                                 | 188 ms: 1.15x faster                                              |
| sqlite_synth               | 2.25 us                                                                | 1.96 us: 1.15x faster                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 605 ms: 1.10x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 578 ms: 1.10x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 420 ms: 1.09x faster                                              |
| scimark_sor                | 134 ms                                                                 | 123 ms: 1.09x faster                                              |
| regex_v8                   | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                             |
| pathlib                    | 19.3 ms                                                                | 17.9 ms: 1.08x faster                                             |
| deepcopy_reduce            | 3.12 us                                                                | 2.94 us: 1.06x faster                                             |
| typing_runtime_protocols   | 156 us                                                                 | 147 us: 1.06x faster                                              |
| dulwich_log                | 74.5 ms                                                                | 70.4 ms: 1.06x faster                                             |
| async_tree_memoization_tg  | 410 ms                                                                 | 394 ms: 1.04x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 324 ms: 1.03x faster                                              |
| async_tree_none            | 353 ms                                                                 | 345 ms: 1.02x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 3.14 ms: 1.02x faster                                             |
| tomli_loads                | 2.01 sec                                                               | 1.98 sec: 1.01x faster                                            |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                              |
| bpe_tokeniser              | 4.46 sec                                                               | 4.42 sec: 1.01x faster                                            |
| regex_dna                  | 189 ms                                                                 | 188 ms: 1.00x faster                                              |
| json_dumps                 | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                             |
| xml_etree_iterparse        | 94.4 ms                                                                | 95.7 ms: 1.01x slower                                             |
| spectral_norm              | 108 ms                                                                 | 110 ms: 1.02x slower                                              |
| create_gc_cycles           | 1.33 ms                                                                | 1.37 ms: 1.03x slower                                             |
| pyflate                    | 449 ms                                                                 | 463 ms: 1.03x slower                                              |
| async_generators           | 375 ms                                                                 | 390 ms: 1.04x slower                                              |
| xml_etree_parse            | 136 ms                                                                 | 142 ms: 1.04x slower                                              |
| json                       | 4.98 ms                                                                | 5.26 ms: 1.06x slower                                             |
| comprehensions             | 16.6 us                                                                | 17.6 us: 1.06x slower                                             |
| coroutines                 | 23.3 ms                                                                | 25.0 ms: 1.07x slower                                             |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.08x slower                                            |
| regex_compile              | 131 ms                                                                 | 142 ms: 1.08x slower                                              |
| json_loads                 | 27.3 us                                                                | 29.8 us: 1.09x slower                                             |
| logging_silent             | 98.2 ns                                                                | 108 ns: 1.10x slower                                              |
| sympy_integrate            | 19.7 ms                                                                | 21.9 ms: 1.11x slower                                             |
| docutils                   | 2.63 sec                                                               | 2.93 sec: 1.12x slower                                            |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.30 ms: 1.12x slower                                             |
| chaos                      | 56.3 ms                                                                | 62.9 ms: 1.12x slower                                             |
| hexiom                     | 5.95 ms                                                                | 6.66 ms: 1.12x slower                                             |
| pprint_safe_repr           | 719 ms                                                                 | 807 ms: 1.12x slower                                              |
| nqueens                    | 77.7 ms                                                                | 88.0 ms: 1.13x slower                                             |
| float                      | 76.7 ms                                                                | 86.9 ms: 1.13x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 239 us: 1.15x slower                                              |
| 2to3                       | 259 ms                                                                 | 297 ms: 1.15x slower                                              |
| pickle_pure_python         | 292 us                                                                 | 335 us: 1.15x slower                                              |
| pprint_pformat             | 1.46 sec                                                               | 1.68 sec: 1.15x slower                                            |
| scimark_lu                 | 112 ms                                                                 | 130 ms: 1.16x slower                                              |
| generators                 | 28.5 ms                                                                | 33.1 ms: 1.16x slower                                             |
| sympy_str                  | 274 ms                                                                 | 318 ms: 1.16x slower                                              |
| logging_format             | 6.92 us                                                                | 8.05 us: 1.16x slower                                             |
| logging_simple             | 6.14 us                                                                | 7.16 us: 1.17x slower                                             |
| sympy_expand               | 454 ms                                                                 | 531 ms: 1.17x slower                                              |
| sympy_sum                  | 154 ms                                                                 | 181 ms: 1.18x slower                                              |
| thrift                     | 772 us                                                                 | 919 us: 1.19x slower                                              |
| xml_etree_generate         | 85.4 ms                                                                | 102 ms: 1.19x slower                                              |
| richards                   | 44.4 ms                                                                | 53.1 ms: 1.20x slower                                             |
| richards_super             | 50.4 ms                                                                | 60.7 ms: 1.20x slower                                             |
| deltablue                  | 3.10 ms                                                                | 3.73 ms: 1.20x slower                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 80.0 ms: 1.21x slower                                             |
| fannkuch                   | 376 ms                                                                 | 458 ms: 1.22x slower                                              |
| django_template            | 34.2 ms                                                                | 41.8 ms: 1.22x slower                                             |
| raytrace                   | 250 ms                                                                 | 307 ms: 1.23x slower                                              |
| python_startup_no_site     | 7.41 ms                                                                | 9.18 ms: 1.24x slower                                             |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.27x slower                                              |
| xml_etree_process          | 59.2 ms                                                                | 75.8 ms: 1.28x slower                                             |
| crypto_pyaes               | 68.2 ms                                                                | 90.4 ms: 1.32x slower                                             |
| coverage                   | 82.5 ms                                                                | 115 ms: 1.39x slower                                              |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                             |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                             |
| nbody                      | 85.3 ms                                                                | 125 ms: 1.47x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 1.48 ms: 1.60x slower                                             |
| telco                      | 7.77 ms                                                                | 175 ms: 22.54x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                      |

Benchmark hidden because not significant (2): scimark_fft, html5lib
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260616-3.16.0a0-4fbec93-NOGIL/bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.075x slower

# HPT report

- Reliability score: 98.77% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x