# Results vs. 3.13.0rc2

- fork: python
- ref: 3db3bba4d1feb3a9fbfc
- machine: linux-x86_64
- commit hash: 3db3bba
- commit date: 2026-06-24
- overall geometric mean: 1.063x slower
- HPT reliability: 97.32%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 293 ms: 1.13x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.97 sec: 1.13x slower                                                |
| html5lib       | 68.6 ms                                                                | 65.3 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 674 ms: 1.34x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 698 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 595 ms: 1.12x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 414 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 577 ms: 1.10x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 390 ms: 1.05x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 337 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 322 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                  |
| async_generators           | 375 ms                                                                 | 387 ms: 1.03x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 24.4 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 187 ms: 1.16x faster                                                  |
| float          | 76.7 ms                                                                | 85.0 ms: 1.11x slower                                                 |
| nbody          | 85.3 ms                                                                | 126 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 189 ms                                                                 | 162 ms: 1.16x faster                                                  |
| regex_effbot   | 3.21 ms                                                                | 2.78 ms: 1.16x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 20.4 ms: 1.14x faster                                                 |
| regex_compile  | 131 ms                                                                 | 138 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.96 sec: 1.03x faster                                                |
| json_dumps           | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 94.9 ms: 1.01x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 142 ms: 1.04x slower                                                  |
| json_loads           | 27.3 us                                                                | 30.2 us: 1.10x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 236 us: 1.13x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 336 us: 1.15x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 102 ms: 1.19x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 74.8 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.21 ms: 1.24x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.40x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.32x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 40.1 ms: 1.17x slower                                                 |
| mako            | 11.2 ms                                                                | 16.2 ms: 1.44x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 134 ms: 2.38x faster                                                  |
| gc_traversal               | 3.32 ms                                                                | 1.78 ms: 1.87x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.30 sec: 1.79x faster                                                |
| bench_mp_pool              | 11.0 ms                                                                | 6.79 ms: 1.62x faster                                                 |
| deepcopy                   | 357 us                                                                 | 261 us: 1.37x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 674 ms: 1.34x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 698 ms: 1.26x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 30.6 us: 1.24x faster                                                 |
| go                         | 141 ms                                                                 | 120 ms: 1.17x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 162 ms: 1.16x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.78 ms: 1.16x faster                                                 |
| pidigits                   | 216 ms                                                                 | 187 ms: 1.16x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 1.96 us: 1.15x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 20.4 ms: 1.14x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 595 ms: 1.12x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 414 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 577 ms: 1.10x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 122 ms: 1.10x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.86 us: 1.09x faster                                                 |
| pathlib                    | 19.3 ms                                                                | 17.8 ms: 1.08x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 144 us: 1.08x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 390 ms: 1.05x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 65.3 ms: 1.05x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 337 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 322 ms: 1.03x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 72.0 ms: 1.03x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 1.96 sec: 1.03x faster                                                |
| bpe_tokeniser              | 4.46 sec                                                               | 4.37 sec: 1.02x faster                                                |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                  |
| json_dumps                 | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 94.9 ms: 1.01x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                |
| pyflate                    | 449 ms                                                                 | 459 ms: 1.02x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 111 ms: 1.03x slower                                                  |
| async_generators           | 375 ms                                                                 | 387 ms: 1.03x slower                                                  |
| xml_etree_parse            | 136 ms                                                                 | 142 ms: 1.04x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 24.4 ms: 1.05x slower                                                 |
| regex_compile              | 131 ms                                                                 | 138 ms: 1.05x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 103 ns: 1.05x slower                                                  |
| comprehensions             | 16.6 us                                                                | 17.5 us: 1.06x slower                                                 |
| json                       | 4.98 ms                                                                | 5.29 ms: 1.06x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.53 ms: 1.10x slower                                                 |
| json_loads                 | 27.3 us                                                                | 30.2 us: 1.10x slower                                                 |
| float                      | 76.7 ms                                                                | 85.0 ms: 1.11x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 21.9 ms: 1.11x slower                                                 |
| chaos                      | 56.3 ms                                                                | 62.5 ms: 1.11x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 804 ms: 1.12x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.88 us: 1.12x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 87.3 ms: 1.12x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.97 sec: 1.13x slower                                                |
| 2to3                       | 259 ms                                                                 | 293 ms: 1.13x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 236 us: 1.13x slower                                                  |
| logging_format             | 6.92 us                                                                | 7.87 us: 1.14x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 128 ms: 1.14x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 313 ms: 1.14x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.67 sec: 1.15x slower                                                |
| pickle_pure_python         | 292 us                                                                 | 336 us: 1.15x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 525 ms: 1.16x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.51 ms: 1.16x slower                                                 |
| generators                 | 28.5 ms                                                                | 33.2 ms: 1.16x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 179 ms: 1.16x slower                                                  |
| django_template            | 34.2 ms                                                                | 40.1 ms: 1.17x slower                                                 |
| richards                   | 44.4 ms                                                                | 52.2 ms: 1.18x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.66 ms: 1.18x slower                                                 |
| richards_super             | 50.4 ms                                                                | 59.6 ms: 1.18x slower                                                 |
| thrift                     | 772 us                                                                 | 918 us: 1.19x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 102 ms: 1.19x slower                                                  |
| raytrace                   | 250 ms                                                                 | 301 ms: 1.20x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 79.3 ms: 1.21x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 463 ms: 1.23x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.21 ms: 1.24x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 74.8 ms: 1.26x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.27x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 89.0 ms: 1.30x slower                                                 |
| coverage                   | 82.5 ms                                                                | 113 ms: 1.37x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.40x slower                                                 |
| mako                       | 11.2 ms                                                                | 16.2 ms: 1.44x slower                                                 |
| nbody                      | 85.3 ms                                                                | 126 ms: 1.48x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.48 ms: 1.60x slower                                                 |
| telco                      | 7.77 ms                                                                | 176 ms: 22.67x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (2): scimark_fft, create_gc_cycles
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260624-3.16.0a0-3db3bba-NOGIL/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.063x slower

# HPT report

- Reliability score: 97.32% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.34x