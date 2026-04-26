# Results vs. 3.13.0rc2

- fork: python
- ref: c5fcdb4a9bd04b88f363
- machine: linux-x86_64
- commit hash: c5fcdb4
- commit date: 2026-04-25
- overall geometric mean: 1.096x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.40 sec: 1.09x faster                                                 |
| html5lib       | 67.0 ms                                                      | 55.1 ms: 1.22x faster                                                  |
| Geometric mean | (ref)                                                        | 1.11x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 567 ms: 1.61x faster                                                   |
| async_tree_io              | 876 ms                                                       | 557 ms: 1.57x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 299 ms: 1.54x faster                                                   |
| async_tree_none            | 354 ms                                                       | 235 ms: 1.51x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 469 ms: 1.42x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 292 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 240 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 469 ms: 1.36x faster                                                   |
| async_generators           | 377 ms                                                       | 320 ms: 1.18x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 452 ms: 1.12x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.46 sec: 1.04x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 65.6 ms: 1.18x faster                                                  |
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                                   |
| nbody          | 85.1 ms                                                      | 76.9 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                        | 1.14x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 119 ms: 1.11x faster                                                   |
| regex_effbot   | 3.08 ms                                                      | 3.10 ms: 1.01x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                  |
| regex_dna      | 180 ms                                                       | 191 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 8.88 ms: 1.19x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.74 sec: 1.15x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 87.5 ms: 1.08x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 55.1 ms: 1.08x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 30.4 us: 1.07x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 81.1 ms: 1.05x faster                                                  |
| unpickle_list        | 4.71 us                                                      | 4.52 us: 1.04x faster                                                  |
| pickle_list          | 4.93 us                                                      | 4.81 us: 1.02x faster                                                  |
| json_loads           | 27.0 us                                                      | 26.4 us: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 208 us: 1.01x faster                                                   |
| pickle_pure_python   | 294 us                                                       | 298 us: 1.01x slower                                                   |
| xml_etree_parse      | 136 ms                                                       | 148 ms: 1.09x slower                                                   |
| pickle               | 11.3 us                                                      | 12.9 us: 1.14x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 6.88 ms: 1.08x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 19.6 ms: 1.10x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 45.8 ms: 1.07x faster                                                  |
| django_template | 34.1 ms                                                      | 33.0 ms: 1.03x faster                                                  |
| mako            | 11.3 ms                                                      | 12.3 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 114 ms: 2.78x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.10 sec: 2.14x faster                                                 |
| deepcopy                   | 355 us                                                       | 216 us: 1.64x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 567 ms: 1.61x faster                                                   |
| async_tree_io              | 876 ms                                                       | 557 ms: 1.57x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 25.3 us: 1.54x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 299 ms: 1.54x faster                                                   |
| async_tree_none            | 354 ms                                                       | 235 ms: 1.51x faster                                                   |
| go                         | 141 ms                                                       | 99.0 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 469 ms: 1.42x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 292 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 240 ms: 1.40x faster                                                   |
| spectral_norm              | 111 ms                                                       | 81.5 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 469 ms: 1.36x faster                                                   |
| scimark_sor                | 134 ms                                                       | 102 ms: 1.32x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.37 us: 1.31x faster                                                  |
| scimark_fft                | 349 ms                                                       | 268 ms: 1.30x faster                                                   |
| logging_silent             | 103 ns                                                       | 82.9 ns: 1.24x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 55.1 ms: 1.22x faster                                                  |
| richards                   | 45.2 ms                                                      | 37.7 ms: 1.20x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 3.94 ms: 1.19x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 8.88 ms: 1.19x faster                                                  |
| richards_super             | 51.6 ms                                                      | 43.6 ms: 1.18x faster                                                  |
| float                      | 77.5 ms                                                      | 65.6 ms: 1.18x faster                                                  |
| async_generators           | 377 ms                                                       | 320 ms: 1.18x faster                                                   |
| pyflate                    | 449 ms                                                       | 384 ms: 1.17x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 56.0 ms: 1.17x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.74 sec: 1.15x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 16.7 ms: 1.15x faster                                                  |
| chaos                      | 57.3 ms                                                      | 50.0 ms: 1.15x faster                                                  |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 3.95 sec: 1.13x faster                                                 |
| comprehensions             | 16.5 us                                                      | 14.6 us: 1.12x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 452 ms: 1.12x faster                                                   |
| nqueens                    | 78.6 ms                                                      | 70.3 ms: 1.12x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.53 us: 1.11x faster                                                  |
| regex_compile              | 132 ms                                                       | 119 ms: 1.11x faster                                                   |
| coverage                   | 83.0 ms                                                      | 74.9 ms: 1.11x faster                                                  |
| nbody                      | 85.1 ms                                                      | 76.9 ms: 1.11x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 67.8 ms: 1.10x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.45 ms: 1.10x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 19.6 ms: 1.10x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.23 us: 1.10x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 103 ms: 1.10x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 18.1 ms: 1.09x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.40 sec: 1.09x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.5 ms: 1.08x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 55.1 ms: 1.08x faster                                                  |
| deltablue                  | 3.12 ms                                                      | 2.90 ms: 1.08x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 6.88 ms: 1.08x faster                                                  |
| raytrace                   | 253 ms                                                       | 235 ms: 1.07x faster                                                   |
| pickle_dict                | 32.5 us                                                      | 30.4 us: 1.07x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 45.8 ms: 1.07x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 81.1 ms: 1.05x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 147 us: 1.05x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.06 sec: 1.05x faster                                                 |
| fannkuch                   | 370 ms                                                       | 353 ms: 1.05x faster                                                   |
| unpickle_list              | 4.71 us                                                      | 4.52 us: 1.04x faster                                                  |
| sympy_str                  | 275 ms                                                       | 264 ms: 1.04x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 150 ms: 1.04x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.46 sec: 1.04x faster                                                 |
| django_template            | 34.1 ms                                                      | 33.0 ms: 1.03x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.14 us: 1.03x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                  |
| 2to3                       | 260 ms                                                       | 253 ms: 1.03x faster                                                   |
| generators                 | 28.8 ms                                                      | 28.1 ms: 1.02x faster                                                  |
| pickle_list                | 4.93 us                                                      | 4.81 us: 1.02x faster                                                  |
| sympy_expand               | 457 ms                                                       | 447 ms: 1.02x faster                                                   |
| json_loads                 | 27.0 us                                                      | 26.4 us: 1.02x faster                                                  |
| thrift                     | 778 us                                                       | 766 us: 1.02x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 729 ms: 1.01x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 208 us: 1.01x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 3.10 ms: 1.01x slower                                                  |
| meteor_contest             | 102 ms                                                       | 102 ms: 1.01x slower                                                   |
| json                       | 4.93 ms                                                      | 4.98 ms: 1.01x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 298 us: 1.01x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| unpack_sequence            | 44.8 ns                                                      | 47.0 ns: 1.05x slower                                                  |
| regex_dna                  | 180 ms                                                       | 191 ms: 1.06x slower                                                   |
| mako                       | 11.3 ms                                                      | 12.3 ms: 1.08x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 148 ms: 1.09x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                  |
| pickle                     | 11.3 us                                                      | 12.9 us: 1.14x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.28 ms: 1.40x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.41 ms: 1.40x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 2.00 ms: 1.49x slower                                                  |
| telco                      | 7.82 ms                                                      | 151 ms: 19.28x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 318 ms: 28.93x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (2): crypto_pyaes, unpickle
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260425-3.15.0a8+-c5fcdb4-CLANG/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.096x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.19x