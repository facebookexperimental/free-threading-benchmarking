# Results vs. 3.13.0rc2

- fork: python
- ref: f4bda4d6cb13d4c57fba
- machine: linux-x86_64
- commit hash: f4bda4d
- commit date: 2026-05-31
- overall geometric mean: 1.021x faster
- HPT reliability: 98.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.63 sec                                                               | 2.41 sec: 1.09x faster                                                |
| html5lib       | 68.6 ms                                                                | 61.3 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 718 ms: 1.23x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 374 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 546 ms: 1.22x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 291 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 756 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 556 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 364 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 300 ms: 1.11x faster                                                  |
| async_generators           | 375 ms                                                                 | 342 ms: 1.10x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 24.4 ms: 1.05x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 545 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.13x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 184 ms: 1.18x faster                                                  |
| float          | 76.7 ms                                                                | 75.4 ms: 1.02x faster                                                 |
| nbody          | 85.3 ms                                                                | 93.5 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.99 ms: 1.07x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 22.0 ms: 1.05x faster                                                 |
| regex_compile  | 131 ms                                                                 | 125 ms: 1.05x faster                                                  |
| regex_dna      | 189 ms                                                                 | 186 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.70 ms: 1.10x faster                                                 |
| tomli_loads          | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                                |
| xml_etree_iterparse  | 94.4 ms                                                                | 89.3 ms: 1.06x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 86.8 ms: 1.02x slower                                                 |
| json_loads           | 27.3 us                                                                | 28.1 us: 1.03x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 215 us: 1.03x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 62.2 ms: 1.05x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 144 ms: 1.06x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 316 us: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 35.5 ms: 1.04x slower                                                 |
| mako            | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 115 ms: 2.76x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.14 sec: 2.05x faster                                                |
| deepcopy                   | 357 us                                                                 | 237 us: 1.51x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 26.8 us: 1.42x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 117 us: 1.33x faster                                                  |
| go                         | 141 ms                                                                 | 108 ms: 1.30x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 718 ms: 1.23x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 374 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 546 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.56 us: 1.22x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 291 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 756 ms: 1.19x faster                                                  |
| pidigits                   | 216 ms                                                                 | 184 ms: 1.18x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 114 ms: 1.17x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 556 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 364 ms: 1.13x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 61.3 ms: 1.12x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 300 ms: 1.11x faster                                                  |
| pyflate                    | 449 ms                                                                 | 409 ms: 1.10x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 67.8 ms: 1.10x faster                                                 |
| async_generators           | 375 ms                                                                 | 342 ms: 1.10x faster                                                  |
| json_dumps                 | 10.6 ms                                                                | 9.70 ms: 1.10x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 98.2 ms: 1.09x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.41 sec: 1.09x faster                                                |
| tomli_loads                | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                                |
| pathlib                    | 19.3 ms                                                                | 17.7 ms: 1.09x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.99 ms: 1.07x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 329 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.22 sec: 1.06x faster                                                |
| xml_etree_iterparse        | 94.4 ms                                                                | 89.3 ms: 1.06x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 22.0 ms: 1.05x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 73.9 ms: 1.05x faster                                                 |
| regex_compile              | 131 ms                                                                 | 125 ms: 1.05x faster                                                  |
| comprehensions             | 16.6 us                                                                | 15.9 us: 1.04x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 19.1 ms: 1.03x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.78 ms: 1.03x faster                                                 |
| float                      | 76.7 ms                                                                | 75.4 ms: 1.02x faster                                                 |
| logging_simple             | 6.14 us                                                                | 6.04 us: 1.02x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 186 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.22 us: 1.01x faster                                                 |
| richards                   | 44.4 ms                                                                | 43.9 ms: 1.01x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 100 ms: 1.01x faster                                                  |
| chaos                      | 56.3 ms                                                                | 55.8 ms: 1.01x faster                                                 |
| sympy_sum                  | 154 ms                                                                 | 155 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.79 ms: 1.01x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 460 ms: 1.01x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 86.8 ms: 1.02x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 114 ms: 1.02x slower                                                  |
| coverage                   | 82.5 ms                                                                | 83.9 ms: 1.02x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 732 ms: 1.02x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 383 ms: 1.02x slower                                                  |
| generators                 | 28.5 ms                                                                | 29.1 ms: 1.02x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.49 sec: 1.02x slower                                                |
| json_loads                 | 27.3 us                                                                | 28.1 us: 1.03x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 215 us: 1.03x slower                                                  |
| thrift                     | 772 us                                                                 | 796 us: 1.03x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 70.5 ms: 1.03x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 102 ns: 1.04x slower                                                  |
| django_template            | 34.2 ms                                                                | 35.5 ms: 1.04x slower                                                 |
| raytrace                   | 250 ms                                                                 | 260 ms: 1.04x slower                                                  |
| json                       | 4.98 ms                                                                | 5.21 ms: 1.05x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 24.4 ms: 1.05x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 62.2 ms: 1.05x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 545 ms: 1.05x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                                |
| xml_etree_parse            | 136 ms                                                                 | 144 ms: 1.06x slower                                                  |
| mako                       | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 316 us: 1.08x slower                                                  |
| nbody                      | 85.3 ms                                                                | 93.5 ms: 1.10x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.46 ms: 1.12x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 3.88 ms: 1.17x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.80 ms: 1.35x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.34 ms: 1.45x slower                                                 |
| telco                      | 7.77 ms                                                                | 165 ms: 21.28x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 270 ms: 24.56x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (4): sympy_str, richards_super, logging_format, scimark_monte_carlo
Ignored benchmarks (23) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260531-3.16.0a0-f4bda4d/bm-20260531-vultr-x86_64-python-f4bda4d6cb13d4c57fba-3.16.0a0-f4bda4d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 98.65% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x