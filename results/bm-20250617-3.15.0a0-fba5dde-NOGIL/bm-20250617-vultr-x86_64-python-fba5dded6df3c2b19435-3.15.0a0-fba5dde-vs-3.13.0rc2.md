# Results vs. 3.13.0rc2

- fork: python
- ref: fba5dded6df3c2b19435
- machine: linux-x86_64
- commit hash: fba5dde
- commit date: 2025-06-17
- overall geometric mean: 1.021x slower
- HPT reliability: 94.85%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 283 ms: 1.09x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.67 sec: 1.02x slower                                                |
| html5lib       | 68.6 ms                                                                | 66.2 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 526 ms: 1.71x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 554 ms: 1.59x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 226 ms: 1.48x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 316 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 288 ms: 1.42x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 476 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 505 ms: 1.32x faster                                                  |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.32x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 186 ms: 1.17x faster                                                  |
| float          | 76.7 ms                                                                | 69.5 ms: 1.10x faster                                                 |
| nbody          | 85.3 ms                                                                | 123 ms: 1.44x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.69 ms: 1.19x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 20.1 ms: 1.15x faster                                                 |
| regex_dna      | 189 ms                                                                 | 175 ms: 1.08x faster                                                  |
| regex_compile  | 131 ms                                                                 | 144 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 131 ms: 1.04x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.13 sec: 1.06x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 230 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 94.9 ms: 1.11x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.0 ms: 1.13x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 335 us: 1.15x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 68.4 ms: 1.15x slower                                                 |
| json_loads           | 27.3 us                                                                | 31.9 us: 1.17x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.61 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                                | 16.0 ms: 1.46x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 57.4 ms: 1.17x slower                                                 |
| django_template | 34.2 ms                                                                | 40.2 ms: 1.18x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.6 ms: 1.22x slower                                                 |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.32 sec: 1.77x faster                                                |
| gc_traversal               | 3.32 ms                                                                | 1.90 ms: 1.74x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 526 ms: 1.71x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 554 ms: 1.59x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 226 ms: 1.48x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 316 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 288 ms: 1.42x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 259 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 476 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 505 ms: 1.32x faster                                                  |
| deepcopy                   | 357 us                                                                 | 285 us: 1.25x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.69 ms: 1.19x faster                                                 |
| pidigits                   | 216 ms                                                                 | 186 ms: 1.17x faster                                                  |
| go                         | 141 ms                                                                 | 122 ms: 1.15x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 20.1 ms: 1.15x faster                                                 |
| deepcopy_memo              | 38.1 us                                                                | 34.4 us: 1.11x faster                                                 |
| float                      | 76.7 ms                                                                | 69.5 ms: 1.10x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 122 ms: 1.09x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 175 ms: 1.08x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.99 us: 1.05x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 71.5 ms: 1.04x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 131 ms: 1.04x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 66.2 ms: 1.04x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.36 sec: 1.02x faster                                                |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.3 ms: 1.00x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.00x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.67 sec: 1.02x slower                                                |
| spectral_norm              | 108 ms                                                                 | 111 ms: 1.03x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 362 ms: 1.04x slower                                                  |
| generators                 | 28.5 ms                                                                | 30.1 ms: 1.05x slower                                                 |
| pyflate                    | 449 ms                                                                 | 475 ms: 1.06x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.13 sec: 1.06x slower                                                |
| hexiom                     | 5.95 ms                                                                | 6.38 ms: 1.07x slower                                                 |
| json                       | 4.98 ms                                                                | 5.37 ms: 1.08x slower                                                 |
| comprehensions             | 16.6 us                                                                | 17.9 us: 1.08x slower                                                 |
| telco                      | 7.77 ms                                                                | 8.43 ms: 1.08x slower                                                 |
| 2to3                       | 259 ms                                                                 | 283 ms: 1.09x slower                                                  |
| regex_compile              | 131 ms                                                                 | 144 ms: 1.10x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 85.6 ms: 1.10x slower                                                 |
| chaos                      | 56.3 ms                                                                | 62.0 ms: 1.10x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 230 us: 1.10x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.47 ms: 1.10x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 94.9 ms: 1.11x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 22.1 ms: 1.12x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.0 ms: 1.13x slower                                                 |
| thrift                     | 772 us                                                                 | 882 us: 1.14x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 129 ms: 1.15x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 315 ms: 1.15x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 335 us: 1.15x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 522 ms: 1.15x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 75.8 ms: 1.15x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 68.4 ms: 1.15x slower                                                 |
| richards                   | 44.4 ms                                                                | 51.6 ms: 1.16x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.60 ms: 1.16x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 180 ms: 1.16x slower                                                  |
| json_loads                 | 27.3 us                                                                | 31.9 us: 1.17x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 57.4 ms: 1.17x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.58 ms: 1.17x slower                                                 |
| raytrace                   | 250 ms                                                                 | 294 ms: 1.18x slower                                                  |
| django_template            | 34.2 ms                                                                | 40.2 ms: 1.18x slower                                                 |
| richards_super             | 50.4 ms                                                                | 59.8 ms: 1.19x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 188 us: 1.21x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 874 ms: 1.22x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 124 ms: 1.22x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 26.6 ms: 1.22x slower                                                 |
| logging_simple             | 6.14 us                                                                | 7.54 us: 1.23x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.52 us: 1.23x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 464 ms: 1.23x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.80 sec: 1.24x slower                                                |
| crypto_pyaes               | 68.2 ms                                                                | 85.4 ms: 1.25x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 9.61 ms: 1.30x slower                                                 |
| coverage                   | 82.5 ms                                                                | 110 ms: 1.33x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.39x slower                                                 |
| nbody                      | 85.3 ms                                                                | 123 ms: 1.44x slower                                                  |
| python_startup             | 11.0 ms                                                                | 16.0 ms: 1.46x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.10 ms: 3.36x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 526 ns: 5.35x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 103 ms: 9.40x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250617-3.15.0a0-fba5dde-NOGIL/bm-20250617-vultr-x86_64-python-fba5dded6df3c2b19435-3.15.0a0-fba5dde.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.021x slower

# HPT report

- Reliability score: 94.85% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x