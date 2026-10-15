# Results vs. 3.13.0rc2

- fork: python
- ref: a6b4aa687cd9f8f95e3b
- machine: linux-x86_64
- commit hash: a6b4aa6
- commit date: 2026-10-14
- overall geometric mean: 1.072x slower
- HPT reliability: 95.41%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 294 ms: 1.13x slower                                                      |
| docutils       | 2.63 sec                                                               | 2.88 sec: 1.09x slower                                                    |
| html5lib       | 68.6 ms                                                                | 65.6 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 707 ms: 1.27x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 719 ms: 1.23x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 605 ms: 1.10x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 423 ms: 1.08x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 587 ms: 1.08x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 344 ms: 1.03x faster                                                      |
| asyncio_websockets         | 517 ms                                                                 | 508 ms: 1.02x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 26.0 ms: 1.12x slower                                                     |
| async_generators           | 375 ms                                                                 | 422 ms: 1.13x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                              |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 187 ms: 1.16x faster                                                      |
| float          | 76.7 ms                                                                | 83.9 ms: 1.09x slower                                                     |
| nbody          | 85.3 ms                                                                | 114 ms: 1.34x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 21.2 ms: 1.10x faster                                                     |
| regex_effbot   | 3.21 ms                                                                | 2.94 ms: 1.09x faster                                                     |
| regex_dna      | 189 ms                                                                 | 185 ms: 1.02x faster                                                      |
| regex_compile  | 131 ms                                                                 | 170 ms: 1.30x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 10.0 ms: 1.06x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.97 sec: 1.02x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 96.7 ms: 1.02x slower                                                     |
| xml_etree_parse      | 136 ms                                                                 | 145 ms: 1.07x slower                                                      |
| json_loads           | 27.3 us                                                                | 30.2 us: 1.10x slower                                                     |
| pickle_pure_python   | 292 us                                                                 | 334 us: 1.15x slower                                                      |
| unpickle_pure_python | 208 us                                                                 | 240 us: 1.15x slower                                                      |
| xml_etree_generate   | 85.4 ms                                                                | 102 ms: 1.20x slower                                                      |
| xml_etree_process    | 59.2 ms                                                                | 76.0 ms: 1.28x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.56 ms: 1.29x slower                                                     |
| python_startup         | 11.0 ms                                                                | 16.1 ms: 1.46x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 42.3 ms: 1.24x slower                                                     |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.32x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 130 ms: 2.43x faster                                                      |
| gc_traversal               | 3.32 ms                                                                | 1.77 ms: 1.87x faster                                                     |
| mdp                        | 2.34 sec                                                               | 1.31 sec: 1.79x faster                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 6.69 ms: 1.65x faster                                                     |
| deepcopy                   | 357 us                                                                 | 265 us: 1.35x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 707 ms: 1.27x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 719 ms: 1.23x faster                                                      |
| go                         | 141 ms                                                                 | 121 ms: 1.16x faster                                                      |
| sqlite_synth               | 2.25 us                                                                | 1.93 us: 1.16x faster                                                     |
| deepcopy_memo              | 38.1 us                                                                | 32.8 us: 1.16x faster                                                     |
| pidigits                   | 216 ms                                                                 | 187 ms: 1.16x faster                                                      |
| scimark_sor                | 134 ms                                                                 | 121 ms: 1.10x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 605 ms: 1.10x faster                                                      |
| regex_v8                   | 23.2 ms                                                                | 21.2 ms: 1.10x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.94 ms: 1.09x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 423 ms: 1.08x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 587 ms: 1.08x faster                                                      |
| deepcopy_reduce            | 3.12 us                                                                | 2.90 us: 1.08x faster                                                     |
| typing_runtime_protocols   | 156 us                                                                 | 145 us: 1.07x faster                                                      |
| pathlib                    | 19.3 ms                                                                | 18.0 ms: 1.07x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 327 ms: 1.06x faster                                                      |
| json_dumps                 | 10.6 ms                                                                | 10.0 ms: 1.06x faster                                                     |
| dulwich_log                | 74.5 ms                                                                | 70.9 ms: 1.05x faster                                                     |
| html5lib                   | 68.6 ms                                                                | 65.6 ms: 1.05x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 344 ms: 1.03x faster                                                      |
| spectral_norm              | 108 ms                                                                 | 105 ms: 1.03x faster                                                      |
| regex_dna                  | 189 ms                                                                 | 185 ms: 1.02x faster                                                      |
| tomli_loads                | 2.01 sec                                                               | 1.97 sec: 1.02x faster                                                    |
| asyncio_websockets         | 517 ms                                                                 | 508 ms: 1.02x faster                                                      |
| bpe_tokeniser              | 4.46 sec                                                               | 4.39 sec: 1.01x faster                                                    |
| pyflate                    | 449 ms                                                                 | 445 ms: 1.01x faster                                                      |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.79 ms: 1.01x slower                                                     |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                    |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 96.7 ms: 1.02x slower                                                     |
| xml_etree_parse            | 136 ms                                                                 | 145 ms: 1.07x slower                                                      |
| chaos                      | 56.3 ms                                                                | 60.3 ms: 1.07x slower                                                     |
| json                       | 4.98 ms                                                                | 5.38 ms: 1.08x slower                                                     |
| comprehensions             | 16.6 us                                                                | 18.0 us: 1.09x slower                                                     |
| float                      | 76.7 ms                                                                | 83.9 ms: 1.09x slower                                                     |
| docutils                   | 2.63 sec                                                               | 2.88 sec: 1.09x slower                                                    |
| json_loads                 | 27.3 us                                                                | 30.2 us: 1.10x slower                                                     |
| hexiom                     | 5.95 ms                                                                | 6.57 ms: 1.10x slower                                                     |
| logging_silent             | 98.2 ns                                                                | 109 ns: 1.11x slower                                                      |
| coroutines                 | 23.3 ms                                                                | 26.0 ms: 1.12x slower                                                     |
| sympy_integrate            | 19.7 ms                                                                | 22.1 ms: 1.12x slower                                                     |
| async_generators           | 375 ms                                                                 | 422 ms: 1.13x slower                                                      |
| nqueens                    | 77.7 ms                                                                | 87.6 ms: 1.13x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 812 ms: 1.13x slower                                                      |
| 2to3                       | 259 ms                                                                 | 294 ms: 1.13x slower                                                      |
| pickle_pure_python         | 292 us                                                                 | 334 us: 1.15x slower                                                      |
| unpickle_pure_python       | 208 us                                                                 | 240 us: 1.15x slower                                                      |
| scimark_lu                 | 112 ms                                                                 | 129 ms: 1.15x slower                                                      |
| scimark_monte_carlo        | 65.8 ms                                                                | 75.9 ms: 1.15x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.69 sec: 1.16x slower                                                    |
| logging_format             | 6.92 us                                                                | 8.01 us: 1.16x slower                                                     |
| sympy_str                  | 274 ms                                                                 | 320 ms: 1.17x slower                                                      |
| raytrace                   | 250 ms                                                                 | 293 ms: 1.17x slower                                                      |
| logging_simple             | 6.14 us                                                                | 7.22 us: 1.18x slower                                                     |
| generators                 | 28.5 ms                                                                | 33.7 ms: 1.18x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 537 ms: 1.18x slower                                                      |
| sympy_sum                  | 154 ms                                                                 | 183 ms: 1.18x slower                                                      |
| xml_etree_generate         | 85.4 ms                                                                | 102 ms: 1.20x slower                                                      |
| richards                   | 44.4 ms                                                                | 53.2 ms: 1.20x slower                                                     |
| richards_super             | 50.4 ms                                                                | 60.7 ms: 1.20x slower                                                     |
| thrift                     | 772 us                                                                 | 931 us: 1.21x slower                                                      |
| deltablue                  | 3.10 ms                                                                | 3.74 ms: 1.21x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 125 ms: 1.23x slower                                                      |
| fannkuch                   | 376 ms                                                                 | 465 ms: 1.24x slower                                                      |
| django_template            | 34.2 ms                                                                | 42.3 ms: 1.24x slower                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 87.3 ms: 1.28x slower                                                     |
| xml_etree_process          | 59.2 ms                                                                | 76.0 ms: 1.28x slower                                                     |
| python_startup_no_site     | 7.41 ms                                                                | 9.56 ms: 1.29x slower                                                     |
| regex_compile              | 131 ms                                                                 | 170 ms: 1.30x slower                                                      |
| nbody                      | 85.3 ms                                                                | 114 ms: 1.34x slower                                                      |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                     |
| coverage                   | 82.5 ms                                                                | 118 ms: 1.43x slower                                                      |
| python_startup             | 11.0 ms                                                                | 16.1 ms: 1.46x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 1.64 ms: 1.77x slower                                                     |
| telco                      | 7.77 ms                                                                | 179 ms: 22.96x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                              |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none_tg
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261014-3.16.0a1+dev-a6b4aa6-NOGIL/bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.072x slower

# HPT report

- Reliability score: 95.41% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.34x