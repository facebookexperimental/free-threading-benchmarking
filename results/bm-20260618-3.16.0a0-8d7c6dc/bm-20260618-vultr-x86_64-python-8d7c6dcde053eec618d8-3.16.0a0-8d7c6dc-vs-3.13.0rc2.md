# Results vs. 3.13.0rc2

- fork: python
- ref: 8d7c6dcde053eec618d8
- machine: linux-x86_64
- commit hash: 8d7c6dc
- commit date: 2026-06-18
- overall geometric mean: 1.033x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 256 ms: 1.01x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.39 sec: 1.10x faster                                                |
| html5lib       | 68.6 ms                                                                | 58.9 ms: 1.16x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 540 ms: 1.24x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 720 ms: 1.22x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 380 ms: 1.21x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 292 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 758 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 558 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 297 ms: 1.12x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 369 ms: 1.11x faster                                                  |
| async_generators           | 375 ms                                                                 | 339 ms: 1.10x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.00x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.13x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 187 ms: 1.15x faster                                                  |
| float          | 76.7 ms                                                                | 74.7 ms: 1.03x faster                                                 |
| nbody          | 85.3 ms                                                                | 94.3 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.75 ms: 1.17x faster                                                 |
| regex_compile  | 131 ms                                                                 | 122 ms: 1.07x faster                                                  |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 22.2 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                                |
| json_dumps           | 10.6 ms                                                                | 9.80 ms: 1.08x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 89.7 ms: 1.05x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 86.0 ms: 1.01x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 60.8 ms: 1.03x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 214 us: 1.03x slower                                                  |
| xml_etree_parse      | 136 ms                                                                 | 143 ms: 1.05x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 311 us: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 6.94 ms: 1.07x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 35.4 ms: 1.04x slower                                                 |
| mako            | 11.2 ms                                                                | 11.8 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 115 ms: 2.76x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.13 sec: 2.07x faster                                                |
| deepcopy                   | 357 us                                                                 | 234 us: 1.53x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 26.3 us: 1.45x faster                                                 |
| go                         | 141 ms                                                                 | 105 ms: 1.34x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 118 us: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 540 ms: 1.24x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 720 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.56 us: 1.22x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 110 ms: 1.21x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 380 ms: 1.21x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 292 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 758 ms: 1.19x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.75 ms: 1.17x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 58.9 ms: 1.16x faster                                                 |
| pidigits                   | 216 ms                                                                 | 187 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 558 ms: 1.13x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 95.2 ms: 1.13x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 297 ms: 1.12x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 369 ms: 1.11x faster                                                  |
| async_generators           | 375 ms                                                                 | 339 ms: 1.10x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.39 sec: 1.10x faster                                                |
| dulwich_log                | 74.5 ms                                                                | 68.1 ms: 1.09x faster                                                 |
| pyflate                    | 449 ms                                                                 | 411 ms: 1.09x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                                |
| json_dumps                 | 10.6 ms                                                                | 9.80 ms: 1.08x faster                                                 |
| pathlib                    | 19.3 ms                                                                | 17.9 ms: 1.08x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 324 ms: 1.08x faster                                                  |
| regex_compile              | 131 ms                                                                 | 122 ms: 1.07x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 6.94 ms: 1.07x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.19 sec: 1.06x faster                                                |
| xml_etree_iterparse        | 94.4 ms                                                                | 89.7 ms: 1.05x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 22.2 ms: 1.05x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 18.9 ms: 1.04x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.9 us: 1.04x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 74.6 ms: 1.04x faster                                                 |
| richards                   | 44.4 ms                                                                | 42.8 ms: 1.04x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.75 ms: 1.04x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.59 ms: 1.03x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 63.6 ms: 1.03x faster                                                 |
| richards_super             | 50.4 ms                                                                | 48.8 ms: 1.03x faster                                                 |
| float                      | 76.7 ms                                                                | 74.7 ms: 1.03x faster                                                 |
| logging_simple             | 6.14 us                                                                | 5.98 us: 1.03x faster                                                 |
| chaos                      | 56.3 ms                                                                | 54.9 ms: 1.03x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 99.7 ms: 1.02x faster                                                 |
| 2to3                       | 259 ms                                                                 | 256 ms: 1.01x faster                                                  |
| logging_format             | 6.92 us                                                                | 6.87 us: 1.01x faster                                                 |
| sympy_str                  | 274 ms                                                                 | 273 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.00x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.12 sec: 1.00x faster                                                |
| sympy_expand               | 454 ms                                                                 | 457 ms: 1.01x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 86.0 ms: 1.01x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 724 ms: 1.01x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.47 sec: 1.01x slower                                                |
| scimark_lu                 | 112 ms                                                                 | 114 ms: 1.02x slower                                                  |
| json                       | 4.98 ms                                                                | 5.07 ms: 1.02x slower                                                 |
| raytrace                   | 250 ms                                                                 | 254 ms: 1.02x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 383 ms: 1.02x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 69.6 ms: 1.02x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 60.8 ms: 1.03x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 214 us: 1.03x slower                                                  |
| django_template            | 34.2 ms                                                                | 35.4 ms: 1.04x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                  |
| xml_etree_parse            | 136 ms                                                                 | 143 ms: 1.05x slower                                                  |
| mako                       | 11.2 ms                                                                | 11.8 ms: 1.06x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 311 us: 1.07x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.35 ms: 1.08x slower                                                 |
| nbody                      | 85.3 ms                                                                | 94.3 ms: 1.10x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.02 ms: 1.21x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.66 ms: 1.25x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.35 ms: 1.46x slower                                                 |
| telco                      | 7.77 ms                                                                | 159 ms: 20.47x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 253 ms: 22.99x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (7): generators, logging_silent, json_loads, sympy_sum, coverage, thrift, sqlite_synth
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.033x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x