# Results vs. 3.13.0rc2

- fork: python
- ref: c22e9c9daef4d97a3fdf
- machine: linux-x86_64
- commit hash: c22e9c9
- commit date: 2026-07-10
- overall geometric mean: 1.032x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 258 ms: 1.01x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.41 sec: 1.09x faster                                                |
| html5lib       | 68.6 ms                                                                | 60.2 ms: 1.14x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 714 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 541 ms: 1.23x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 374 ms: 1.23x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 289 ms: 1.22x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 754 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 557 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 364 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 297 ms: 1.12x faster                                                  |
| async_generators           | 375 ms                                                                 | 344 ms: 1.09x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.14x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 195 ms: 1.11x faster                                                  |
| float          | 76.7 ms                                                                | 74.1 ms: 1.04x faster                                                 |
| nbody          | 85.3 ms                                                                | 91.6 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.83 ms: 1.14x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                                 |
| regex_dna      | 189 ms                                                                 | 188 ms: 1.00x faster                                                  |
| regex_compile  | 131 ms                                                                 | 148 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.79 sec: 1.13x faster                                                |
| json_dumps           | 10.6 ms                                                                | 9.81 ms: 1.08x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 89.3 ms: 1.06x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 86.3 ms: 1.01x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 60.6 ms: 1.02x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 213 us: 1.02x slower                                                  |
| xml_etree_parse      | 136 ms                                                                 | 143 ms: 1.05x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 309 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.03 ms: 1.05x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.4 ms: 1.12x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 35.7 ms: 1.05x slower                                                 |
| mako            | 11.2 ms                                                                | 11.8 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 115 ms: 2.77x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.14 sec: 2.06x faster                                                |
| deepcopy                   | 357 us                                                                 | 233 us: 1.54x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 27.0 us: 1.41x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 117 us: 1.33x faster                                                  |
| go                         | 141 ms                                                                 | 106 ms: 1.32x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 714 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 541 ms: 1.23x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 374 ms: 1.23x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 109 ms: 1.23x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 289 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.57 us: 1.21x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 754 ms: 1.19x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 90.2 ms: 1.19x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 60.2 ms: 1.14x faster                                                 |
| pyflate                    | 449 ms                                                                 | 394 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 557 ms: 1.14x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.83 ms: 1.14x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 364 ms: 1.13x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.79 sec: 1.13x faster                                                |
| async_tree_none_tg         | 333 ms                                                                 | 297 ms: 1.12x faster                                                  |
| pidigits                   | 216 ms                                                                 | 195 ms: 1.11x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 318 ms: 1.09x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.41 sec: 1.09x faster                                                |
| async_generators           | 375 ms                                                                 | 344 ms: 1.09x faster                                                  |
| json_dumps                 | 10.6 ms                                                                | 9.81 ms: 1.08x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 68.9 ms: 1.08x faster                                                 |
| pathlib                    | 19.3 ms                                                                | 17.8 ms: 1.08x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.6 ms: 1.08x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.20 sec: 1.06x faster                                                |
| xml_etree_iterparse        | 94.4 ms                                                                | 89.3 ms: 1.06x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.63 ms: 1.06x faster                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 7.03 ms: 1.05x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.52 ms: 1.05x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 74.2 ms: 1.05x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.9 us: 1.04x faster                                                 |
| chaos                      | 56.3 ms                                                                | 54.2 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 63.4 ms: 1.04x faster                                                 |
| float                      | 76.7 ms                                                                | 74.1 ms: 1.04x faster                                                 |
| richards                   | 44.4 ms                                                                | 42.9 ms: 1.03x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 19.2 ms: 1.03x faster                                                 |
| richards_super             | 50.4 ms                                                                | 49.2 ms: 1.02x faster                                                 |
| logging_silent             | 98.2 ns                                                                | 96.0 ns: 1.02x faster                                                 |
| generators                 | 28.5 ms                                                                | 28.2 ms: 1.01x faster                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 710 ms: 1.01x faster                                                  |
| logging_format             | 6.92 us                                                                | 6.85 us: 1.01x faster                                                 |
| logging_simple             | 6.14 us                                                                | 6.10 us: 1.01x faster                                                 |
| 2to3                       | 259 ms                                                                 | 258 ms: 1.01x faster                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.45 sec: 1.01x faster                                                |
| pycparser                  | 1.12 sec                                                               | 1.11 sec: 1.00x faster                                                |
| regex_dna                  | 189 ms                                                                 | 188 ms: 1.00x faster                                                  |
| fannkuch                   | 376 ms                                                                 | 378 ms: 1.01x slower                                                  |
| json                       | 4.98 ms                                                                | 5.03 ms: 1.01x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 458 ms: 1.01x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 86.3 ms: 1.01x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 69.1 ms: 1.01x slower                                                 |
| raytrace                   | 250 ms                                                                 | 254 ms: 1.02x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 157 ms: 1.02x slower                                                  |
| thrift                     | 772 us                                                                 | 786 us: 1.02x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 60.6 ms: 1.02x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 213 us: 1.02x slower                                                  |
| django_template            | 34.2 ms                                                                | 35.7 ms: 1.05x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                  |
| xml_etree_parse            | 136 ms                                                                 | 143 ms: 1.05x slower                                                  |
| mako                       | 11.2 ms                                                                | 11.8 ms: 1.06x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 309 us: 1.06x slower                                                  |
| nbody                      | 85.3 ms                                                                | 91.6 ms: 1.07x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.34 ms: 1.08x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.4 ms: 1.12x slower                                                 |
| regex_compile              | 131 ms                                                                 | 148 ms: 1.13x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 3.86 ms: 1.16x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.69 ms: 1.27x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.34 ms: 1.45x slower                                                 |
| telco                      | 7.77 ms                                                                | 160 ms: 20.60x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 261 ms: 23.70x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (7): sqlite_synth, sympy_str, scimark_lu, coroutines, json_loads, coverage, meteor_contest
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260710-3.16.0a0-c22e9c9/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x