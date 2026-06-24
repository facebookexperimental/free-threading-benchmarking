# Results vs. 3.13.0rc2

- fork: kumaraditya303
- ref: mrocache
- machine: linux-x86_64
- commit hash: 4fbec93
- commit date: 2026-06-16
- overall geometric mean: 1.021x faster
- HPT reliability: 98.10%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 262 ms: 1.01x slower                                              |
| docutils       | 2.63 sec                                                               | 2.39 sec: 1.10x faster                                            |
| html5lib       | 68.6 ms                                                                | 60.9 ms: 1.13x faster                                             |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 546 ms: 1.22x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 377 ms: 1.22x faster                                              |
| async_tree_io              | 881 ms                                                                 | 726 ms: 1.21x faster                                              |
| async_tree_none            | 353 ms                                                                 | 296 ms: 1.19x faster                                              |
| async_tree_io_tg           | 901 ms                                                                 | 769 ms: 1.17x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 559 ms: 1.13x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 368 ms: 1.12x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 301 ms: 1.11x faster                                              |
| async_generators           | 375 ms                                                                 | 340 ms: 1.10x faster                                              |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                             |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.13x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                              |
| float          | 76.7 ms                                                                | 74.3 ms: 1.03x faster                                             |
| nbody          | 85.3 ms                                                                | 95.0 ms: 1.11x slower                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.75 ms: 1.17x faster                                             |
| regex_compile  | 131 ms                                                                 | 125 ms: 1.05x faster                                              |
| regex_v8       | 23.2 ms                                                                | 22.2 ms: 1.05x faster                                             |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                              |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.84 ms: 1.08x faster                                             |
| tomli_loads          | 2.01 sec                                                               | 1.88 sec: 1.07x faster                                            |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.6 ms: 1.03x faster                                             |
| json_loads           | 27.3 us                                                                | 27.2 us: 1.01x faster                                             |
| xml_etree_generate   | 85.4 ms                                                                | 88.6 ms: 1.04x slower                                             |
| unpickle_pure_python | 208 us                                                                 | 216 us: 1.04x slower                                              |
| xml_etree_parse      | 136 ms                                                                 | 143 ms: 1.05x slower                                              |
| xml_etree_process    | 59.2 ms                                                                | 63.1 ms: 1.07x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 313 us: 1.07x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 6.97 ms: 1.06x faster                                             |
| python_startup         | 11.0 ms                                                                | 12.4 ms: 1.13x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.03x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 11.2 ms                                                                | 11.9 ms: 1.06x slower                                             |
| django_template | 34.2 ms                                                                | 37.2 ms: 1.09x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.07x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 116 ms: 2.74x faster                                              |
| mdp                        | 2.34 sec                                                               | 1.14 sec: 2.04x faster                                            |
| deepcopy                   | 357 us                                                                 | 238 us: 1.50x faster                                              |
| deepcopy_memo              | 38.1 us                                                                | 26.4 us: 1.44x faster                                             |
| go                         | 141 ms                                                                 | 106 ms: 1.33x faster                                              |
| typing_runtime_protocols   | 156 us                                                                 | 122 us: 1.27x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 546 ms: 1.22x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 377 ms: 1.22x faster                                              |
| async_tree_io              | 881 ms                                                                 | 726 ms: 1.21x faster                                              |
| scimark_sor                | 134 ms                                                                 | 111 ms: 1.21x faster                                              |
| async_tree_none            | 353 ms                                                                 | 296 ms: 1.19x faster                                              |
| async_tree_io_tg           | 901 ms                                                                 | 769 ms: 1.17x faster                                              |
| deepcopy_reduce            | 3.12 us                                                                | 2.67 us: 1.17x faster                                             |
| regex_effbot               | 3.21 ms                                                                | 2.75 ms: 1.17x faster                                             |
| spectral_norm              | 108 ms                                                                 | 94.3 ms: 1.14x faster                                             |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 559 ms: 1.13x faster                                              |
| html5lib                   | 68.6 ms                                                                | 60.9 ms: 1.13x faster                                             |
| async_tree_memoization_tg  | 410 ms                                                                 | 368 ms: 1.12x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 301 ms: 1.11x faster                                              |
| pyflate                    | 449 ms                                                                 | 408 ms: 1.10x faster                                              |
| async_generators           | 375 ms                                                                 | 340 ms: 1.10x faster                                              |
| docutils                   | 2.63 sec                                                               | 2.39 sec: 1.10x faster                                            |
| dulwich_log                | 74.5 ms                                                                | 68.4 ms: 1.09x faster                                             |
| json_dumps                 | 10.6 ms                                                                | 9.84 ms: 1.08x faster                                             |
| scimark_fft                | 348 ms                                                                 | 325 ms: 1.07x faster                                              |
| tomli_loads                | 2.01 sec                                                               | 1.88 sec: 1.07x faster                                            |
| python_startup_no_site     | 7.41 ms                                                                | 6.97 ms: 1.06x faster                                             |
| pathlib                    | 19.3 ms                                                                | 18.2 ms: 1.06x faster                                             |
| comprehensions             | 16.6 us                                                                | 15.7 us: 1.05x faster                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.25 sec: 1.05x faster                                            |
| regex_compile              | 131 ms                                                                 | 125 ms: 1.05x faster                                              |
| regex_v8                   | 23.2 ms                                                                | 22.2 ms: 1.05x faster                                             |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                              |
| float                      | 76.7 ms                                                                | 74.3 ms: 1.03x faster                                             |
| nqueens                    | 77.7 ms                                                                | 75.4 ms: 1.03x faster                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 63.8 ms: 1.03x faster                                             |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.6 ms: 1.03x faster                                             |
| chaos                      | 56.3 ms                                                                | 54.8 ms: 1.03x faster                                             |
| sympy_integrate            | 19.7 ms                                                                | 19.3 ms: 1.02x faster                                             |
| meteor_contest             | 101 ms                                                                 | 99.3 ms: 1.02x faster                                             |
| hexiom                     | 5.95 ms                                                                | 5.85 ms: 1.02x faster                                             |
| sqlite_synth               | 2.25 us                                                                | 2.21 us: 1.02x faster                                             |
| json                       | 4.98 ms                                                                | 4.93 ms: 1.01x faster                                             |
| generators                 | 28.5 ms                                                                | 28.3 ms: 1.01x faster                                             |
| json_loads                 | 27.3 us                                                                | 27.2 us: 1.01x faster                                             |
| richards                   | 44.4 ms                                                                | 44.7 ms: 1.01x slower                                             |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                             |
| 2to3                       | 259 ms                                                                 | 262 ms: 1.01x slower                                              |
| logging_simple             | 6.14 us                                                                | 6.22 us: 1.01x slower                                             |
| richards_super             | 50.4 ms                                                                | 51.1 ms: 1.01x slower                                             |
| fannkuch                   | 376 ms                                                                 | 381 ms: 1.01x slower                                              |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.83 ms: 1.02x slower                                             |
| logging_silent             | 98.2 ns                                                                | 100 ns: 1.02x slower                                              |
| crypto_pyaes               | 68.2 ms                                                                | 69.5 ms: 1.02x slower                                             |
| sympy_str                  | 274 ms                                                                 | 280 ms: 1.02x slower                                              |
| pycparser                  | 1.12 sec                                                               | 1.15 sec: 1.02x slower                                            |
| logging_format             | 6.92 us                                                                | 7.08 us: 1.02x slower                                             |
| raytrace                   | 250 ms                                                                 | 256 ms: 1.03x slower                                              |
| sympy_sum                  | 154 ms                                                                 | 158 ms: 1.03x slower                                              |
| pprint_safe_repr           | 719 ms                                                                 | 738 ms: 1.03x slower                                              |
| xml_etree_generate         | 85.4 ms                                                                | 88.6 ms: 1.04x slower                                             |
| unpickle_pure_python       | 208 us                                                                 | 216 us: 1.04x slower                                              |
| pprint_pformat             | 1.46 sec                                                               | 1.51 sec: 1.04x slower                                            |
| coverage                   | 82.5 ms                                                                | 85.7 ms: 1.04x slower                                             |
| sympy_expand               | 454 ms                                                                 | 475 ms: 1.05x slower                                              |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                              |
| xml_etree_parse            | 136 ms                                                                 | 143 ms: 1.05x slower                                              |
| thrift                     | 772 us                                                                 | 818 us: 1.06x slower                                              |
| mako                       | 11.2 ms                                                                | 11.9 ms: 1.06x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 119 ms: 1.06x slower                                              |
| xml_etree_process          | 59.2 ms                                                                | 63.1 ms: 1.07x slower                                             |
| gc_traversal               | 3.32 ms                                                                | 3.54 ms: 1.07x slower                                             |
| pickle_pure_python         | 292 us                                                                 | 313 us: 1.07x slower                                              |
| django_template            | 34.2 ms                                                                | 37.2 ms: 1.09x slower                                             |
| deltablue                  | 3.10 ms                                                                | 3.41 ms: 1.10x slower                                             |
| nbody                      | 85.3 ms                                                                | 95.0 ms: 1.11x slower                                             |
| python_startup             | 11.0 ms                                                                | 12.4 ms: 1.13x slower                                             |
| create_gc_cycles           | 1.33 ms                                                                | 1.65 ms: 1.24x slower                                             |
| bench_thread_pool          | 924 us                                                                 | 1.34 ms: 1.45x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 219 ms: 19.90x slower                                             |
| telco                      | 7.77 ms                                                                | 165 ms: 21.19x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                      |
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260616-3.16.0a0-4fbec93/bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 98.10% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x