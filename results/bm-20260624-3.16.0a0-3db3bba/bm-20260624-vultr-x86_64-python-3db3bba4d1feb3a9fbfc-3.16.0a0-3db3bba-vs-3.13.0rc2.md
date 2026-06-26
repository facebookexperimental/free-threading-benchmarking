# Results vs. 3.13.0rc2

- fork: python
- ref: 3db3bba4d1feb3a9fbfc
- machine: linux-x86_64
- commit hash: 3db3bba
- commit date: 2026-06-24
- overall geometric mean: 1.039x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 253 ms: 1.02x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.38 sec: 1.10x faster                                                |
| html5lib       | 68.6 ms                                                                | 59.0 ms: 1.16x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 720 ms: 1.22x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 376 ms: 1.22x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 289 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 546 ms: 1.22x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 767 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 558 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 368 ms: 1.11x faster                                                  |
| async_generators           | 375 ms                                                                 | 338 ms: 1.11x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 301 ms: 1.11x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 545 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.13x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 184 ms: 1.18x faster                                                  |
| float          | 76.7 ms                                                                | 74.1 ms: 1.04x faster                                                 |
| nbody          | 85.3 ms                                                                | 91.8 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.83 ms: 1.13x faster                                                 |
| regex_compile  | 131 ms                                                                 | 120 ms: 1.10x faster                                                  |
| regex_dna      | 189 ms                                                                 | 177 ms: 1.06x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 22.2 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.85 sec: 1.09x faster                                                |
| json_dumps           | 10.6 ms                                                                | 9.79 ms: 1.09x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 90.0 ms: 1.05x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 209 us: 1.00x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 60.4 ms: 1.02x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 143 ms: 1.05x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 307 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 6.94 ms: 1.07x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 35.7 ms: 1.04x slower                                                 |
| mako            | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 114 ms: 2.79x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.13 sec: 2.07x faster                                                |
| deepcopy                   | 357 us                                                                 | 229 us: 1.56x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 26.4 us: 1.44x faster                                                 |
| go                         | 141 ms                                                                 | 102 ms: 1.37x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 117 us: 1.33x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 107 ms: 1.25x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.53 us: 1.23x faster                                                 |
| async_tree_io              | 881 ms                                                                 | 720 ms: 1.22x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 376 ms: 1.22x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 289 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 546 ms: 1.22x faster                                                  |
| pidigits                   | 216 ms                                                                 | 184 ms: 1.18x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 767 ms: 1.18x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 59.0 ms: 1.16x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 93.9 ms: 1.15x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 558 ms: 1.14x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.83 ms: 1.13x faster                                                 |
| pyflate                    | 449 ms                                                                 | 402 ms: 1.12x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 368 ms: 1.11x faster                                                  |
| async_generators           | 375 ms                                                                 | 338 ms: 1.11x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 301 ms: 1.11x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.38 sec: 1.10x faster                                                |
| dulwich_log                | 74.5 ms                                                                | 67.4 ms: 1.10x faster                                                 |
| regex_compile              | 131 ms                                                                 | 120 ms: 1.10x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.85 sec: 1.09x faster                                                |
| pathlib                    | 19.3 ms                                                                | 17.7 ms: 1.09x faster                                                 |
| json_dumps                 | 10.6 ms                                                                | 9.79 ms: 1.09x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 321 ms: 1.09x faster                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 6.94 ms: 1.07x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 177 ms: 1.06x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.61 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.20 sec: 1.06x faster                                                |
| comprehensions             | 16.6 us                                                                | 15.6 us: 1.06x faster                                                 |
| richards                   | 44.4 ms                                                                | 42.0 ms: 1.06x faster                                                 |
| richards_super             | 50.4 ms                                                                | 48.0 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 90.0 ms: 1.05x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.8 ms: 1.05x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 74.3 ms: 1.05x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 22.2 ms: 1.04x faster                                                 |
| chaos                      | 56.3 ms                                                                | 54.1 ms: 1.04x faster                                                 |
| float                      | 76.7 ms                                                                | 74.1 ms: 1.04x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 19.0 ms: 1.04x faster                                                 |
| generators                 | 28.5 ms                                                                | 27.9 ms: 1.02x faster                                                 |
| 2to3                       | 259 ms                                                                 | 253 ms: 1.02x faster                                                  |
| logging_silent             | 98.2 ns                                                                | 96.0 ns: 1.02x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 99.1 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.20 us: 1.02x faster                                                 |
| logging_simple             | 6.14 us                                                                | 6.07 us: 1.01x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.11 sec: 1.01x faster                                                |
| sympy_str                  | 274 ms                                                                 | 273 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 208 us                                                                 | 209 us: 1.00x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 378 ms: 1.01x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 723 ms: 1.01x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.47 sec: 1.01x slower                                                |
| sympy_sum                  | 154 ms                                                                 | 156 ms: 1.01x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 69.2 ms: 1.02x slower                                                 |
| coverage                   | 82.5 ms                                                                | 83.9 ms: 1.02x slower                                                 |
| json                       | 4.98 ms                                                                | 5.08 ms: 1.02x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 60.4 ms: 1.02x slower                                                 |
| django_template            | 34.2 ms                                                                | 35.7 ms: 1.04x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.25 ms: 1.05x slower                                                 |
| xml_etree_parse            | 136 ms                                                                 | 143 ms: 1.05x slower                                                  |
| asyncio_websockets         | 517 ms                                                                 | 545 ms: 1.05x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 307 us: 1.05x slower                                                  |
| mako                       | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                 |
| nbody                      | 85.3 ms                                                                | 91.8 ms: 1.08x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 3.72 ms: 1.12x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.68 ms: 1.26x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.33 ms: 1.44x slower                                                 |
| telco                      | 7.77 ms                                                                | 158 ms: 20.32x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 227 ms: 20.66x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (8): scimark_sparse_mat_mult, thrift, logging_format, json_loads, raytrace, xml_etree_generate, scimark_lu, sympy_expand
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260624-3.16.0a0-3db3bba/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x