# Results vs. 3.13.0rc2

- fork: python
- ref: f4bda4d6cb13d4c57fba
- machine: linux-x86_64
- commit hash: f4bda4d
- commit date: 2026-05-31
- overall geometric mean: 1.066x slower
- HPT reliability: 96.37%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.63 sec                                                               | 2.97 sec: 1.13x slower                                                |
| html5lib       | 68.6 ms                                                                | 69.6 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 682 ms: 1.32x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 702 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 587 ms: 1.13x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 574 ms: 1.10x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 417 ms: 1.10x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 338 ms: 1.05x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 395 ms: 1.04x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 509 ms: 1.02x faster                                                  |
| async_generators           | 375 ms                                                                 | 384 ms: 1.02x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 24.6 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 185 ms: 1.17x faster                                                  |
| float          | 76.7 ms                                                                | 87.4 ms: 1.14x slower                                                 |
| nbody          | 85.3 ms                                                                | 124 ms: 1.45x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 21.4 ms: 1.08x faster                                                 |
| regex_dna      | 189 ms                                                                 | 187 ms: 1.01x faster                                                  |
| regex_effbot   | 3.21 ms                                                                | 3.19 ms: 1.01x faster                                                 |
| regex_compile  | 131 ms                                                                 | 143 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.96 sec: 1.02x faster                                                |
| xml_etree_parse      | 136 ms                                                                 | 140 ms: 1.03x slower                                                  |
| json_loads           | 27.3 us                                                                | 31.0 us: 1.13x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 337 us: 1.16x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 243 us: 1.17x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 102 ms: 1.19x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 75.4 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, json_dumps

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 39.8 ms: 1.16x slower                                                 |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 133 ms: 2.39x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.33 sec: 1.76x faster                                                |
| gc_traversal               | 3.32 ms                                                                | 1.92 ms: 1.72x faster                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 6.99 ms: 1.57x faster                                                 |
| deepcopy                   | 357 us                                                                 | 270 us: 1.32x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 682 ms: 1.32x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 702 ms: 1.26x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 31.0 us: 1.23x faster                                                 |
| pidigits                   | 216 ms                                                                 | 185 ms: 1.17x faster                                                  |
| go                         | 141 ms                                                                 | 122 ms: 1.15x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 1.97 us: 1.14x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 587 ms: 1.13x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 120 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 574 ms: 1.10x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 417 ms: 1.10x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.4 ms: 1.08x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.89 us: 1.08x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 145 us: 1.07x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 18.0 ms: 1.07x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 71.0 ms: 1.05x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 338 ms: 1.05x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 395 ms: 1.04x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.96 sec: 1.02x faster                                                |
| asyncio_websockets         | 517 ms                                                                 | 509 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.39 sec: 1.01x faster                                                |
| regex_dna                  | 189 ms                                                                 | 187 ms: 1.01x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 345 ms: 1.01x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 3.19 ms: 1.01x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                |
| html5lib                   | 68.6 ms                                                                | 69.6 ms: 1.01x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 110 ms: 1.02x slower                                                  |
| async_generators           | 375 ms                                                                 | 384 ms: 1.02x slower                                                  |
| xml_etree_parse            | 136 ms                                                                 | 140 ms: 1.03x slower                                                  |
| pyflate                    | 449 ms                                                                 | 463 ms: 1.03x slower                                                  |
| comprehensions             | 16.6 us                                                                | 17.4 us: 1.05x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 24.6 ms: 1.05x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 104 ns: 1.06x slower                                                  |
| json                       | 4.98 ms                                                                | 5.35 ms: 1.07x slower                                                 |
| regex_compile              | 131 ms                                                                 | 143 ms: 1.09x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.76 us: 1.10x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 21.8 ms: 1.11x slower                                                 |
| chaos                      | 56.3 ms                                                                | 62.4 ms: 1.11x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.61 ms: 1.11x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.69 us: 1.11x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 800 ms: 1.11x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.36 ms: 1.13x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 87.9 ms: 1.13x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 310 ms: 1.13x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.97 sec: 1.13x slower                                                |
| create_gc_cycles           | 1.33 ms                                                                | 1.51 ms: 1.13x slower                                                 |
| json_loads                 | 27.3 us                                                                | 31.0 us: 1.13x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.65 sec: 1.13x slower                                                |
| float                      | 76.7 ms                                                                | 87.4 ms: 1.14x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 518 ms: 1.14x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 129 ms: 1.15x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 178 ms: 1.15x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 337 us: 1.16x slower                                                  |
| django_template            | 34.2 ms                                                                | 39.8 ms: 1.16x slower                                                 |
| thrift                     | 772 us                                                                 | 898 us: 1.16x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 243 us: 1.17x slower                                                  |
| richards                   | 44.4 ms                                                                | 52.7 ms: 1.19x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 102 ms: 1.19x slower                                                  |
| generators                 | 28.5 ms                                                                | 34.1 ms: 1.19x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.71 ms: 1.20x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 78.9 ms: 1.20x slower                                                 |
| raytrace                   | 250 ms                                                                 | 302 ms: 1.21x slower                                                  |
| richards_super             | 50.4 ms                                                                | 61.1 ms: 1.21x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 462 ms: 1.23x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.27x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 75.4 ms: 1.27x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 90.1 ms: 1.32x slower                                                 |
| coverage                   | 82.5 ms                                                                | 115 ms: 1.39x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                 |
| nbody                      | 85.3 ms                                                                | 124 ms: 1.45x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.47 ms: 1.59x slower                                                 |
| telco                      | 7.77 ms                                                                | 176 ms: 22.59x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (3): async_tree_none_tg, xml_etree_iterparse, json_dumps
Ignored benchmarks (23) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260531-3.16.0a0-f4bda4d-NOGIL/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.066x slower

# HPT report

- Reliability score: 96.37% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x