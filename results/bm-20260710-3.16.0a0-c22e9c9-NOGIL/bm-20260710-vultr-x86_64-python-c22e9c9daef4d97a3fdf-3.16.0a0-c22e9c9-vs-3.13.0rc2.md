# Results vs. 3.13.0rc2

- fork: python
- ref: c22e9c9daef4d97a3fdf
- machine: linux-x86_64
- commit hash: c22e9c9
- commit date: 2026-07-10
- overall geometric mean: 1.072x slower
- HPT reliability: 98.92%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.96 sec: 1.13x slower                                                |
| html5lib       | 68.6 ms                                                                | 68.1 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 686 ms: 1.31x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 702 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 601 ms: 1.11x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 418 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 581 ms: 1.09x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 338 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 396 ms: 1.04x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 323 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                                  |
| async_generators           | 375 ms                                                                 | 390 ms: 1.04x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 25.8 ms: 1.11x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 180 ms: 1.20x faster                                                  |
| float          | 76.7 ms                                                                | 84.9 ms: 1.11x slower                                                 |
| nbody          | 85.3 ms                                                                | 125 ms: 1.47x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 20.9 ms: 1.11x faster                                                 |
| regex_effbot   | 3.21 ms                                                                | 3.06 ms: 1.05x faster                                                 |
| regex_dna      | 189 ms                                                                 | 187 ms: 1.01x faster                                                  |
| regex_compile  | 131 ms                                                                 | 168 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.97 sec: 1.02x faster                                                |
| json_dumps           | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 95.3 ms: 1.01x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 140 ms: 1.03x slower                                                  |
| json_loads           | 27.3 us                                                                | 29.9 us: 1.09x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 240 us: 1.15x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 338 us: 1.16x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 101 ms: 1.18x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 74.5 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.28 ms: 1.25x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.33x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 40.3 ms: 1.18x slower                                                 |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 131 ms: 2.43x faster                                                  |
| gc_traversal               | 3.32 ms                                                                | 1.77 ms: 1.87x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.30 sec: 1.80x faster                                                |
| bench_mp_pool              | 11.0 ms                                                                | 6.93 ms: 1.59x faster                                                 |
| deepcopy                   | 357 us                                                                 | 270 us: 1.32x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 686 ms: 1.31x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 702 ms: 1.26x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 31.0 us: 1.23x faster                                                 |
| pidigits                   | 216 ms                                                                 | 180 ms: 1.20x faster                                                  |
| go                         | 141 ms                                                                 | 121 ms: 1.16x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 1.97 us: 1.14x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 20.9 ms: 1.11x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 601 ms: 1.11x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 418 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 581 ms: 1.09x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 123 ms: 1.09x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 17.9 ms: 1.07x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 146 us: 1.07x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.93 us: 1.07x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 3.06 ms: 1.05x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 70.9 ms: 1.05x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 338 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 396 ms: 1.04x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 323 ms: 1.03x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.97 sec: 1.02x faster                                                |
| bpe_tokeniser              | 4.46 sec                                                               | 4.38 sec: 1.02x faster                                                |
| regex_dna                  | 189 ms                                                                 | 187 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 68.1 ms: 1.01x faster                                                 |
| json_dumps                 | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 95.3 ms: 1.01x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 353 ms: 1.01x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                                 |
| xml_etree_parse            | 136 ms                                                                 | 140 ms: 1.03x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.16 sec: 1.04x slower                                                |
| async_generators           | 375 ms                                                                 | 390 ms: 1.04x slower                                                  |
| pyflate                    | 449 ms                                                                 | 468 ms: 1.04x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 113 ms: 1.05x slower                                                  |
| json                       | 4.98 ms                                                                | 5.26 ms: 1.06x slower                                                 |
| comprehensions             | 16.6 us                                                                | 17.8 us: 1.07x slower                                                 |
| json_loads                 | 27.3 us                                                                | 29.9 us: 1.09x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 108 ns: 1.10x slower                                                  |
| hexiom                     | 5.95 ms                                                                | 6.54 ms: 1.10x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 25.8 ms: 1.11x slower                                                 |
| float                      | 76.7 ms                                                                | 84.9 ms: 1.11x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 21.9 ms: 1.11x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 799 ms: 1.11x slower                                                  |
| logging_format             | 6.92 us                                                                | 7.72 us: 1.12x slower                                                 |
| chaos                      | 56.3 ms                                                                | 62.8 ms: 1.12x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.86 us: 1.12x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 87.3 ms: 1.12x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.96 sec: 1.13x slower                                                |
| sympy_str                  | 274 ms                                                                 | 312 ms: 1.14x slower                                                  |
| 2to3                       | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.67 sec: 1.15x slower                                                |
| scimark_lu                 | 112 ms                                                                 | 129 ms: 1.15x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 520 ms: 1.15x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 240 us: 1.15x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 179 ms: 1.16x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 338 us: 1.16x slower                                                  |
| generators                 | 28.5 ms                                                                | 33.3 ms: 1.17x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.57 ms: 1.17x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 101 ms: 1.18x slower                                                  |
| django_template            | 34.2 ms                                                                | 40.3 ms: 1.18x slower                                                 |
| thrift                     | 772 us                                                                 | 913 us: 1.18x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.68 ms: 1.19x slower                                                 |
| richards_super             | 50.4 ms                                                                | 60.2 ms: 1.19x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 79.4 ms: 1.21x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 124 ms: 1.22x slower                                                  |
| richards                   | 44.4 ms                                                                | 54.3 ms: 1.22x slower                                                 |
| raytrace                   | 250 ms                                                                 | 306 ms: 1.23x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 464 ms: 1.23x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.28 ms: 1.25x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 74.5 ms: 1.26x slower                                                 |
| regex_compile              | 131 ms                                                                 | 168 ms: 1.28x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 89.7 ms: 1.32x slower                                                 |
| coverage                   | 82.5 ms                                                                | 115 ms: 1.39x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                 |
| nbody                      | 85.3 ms                                                                | 125 ms: 1.47x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.49 ms: 1.61x slower                                                 |
| telco                      | 7.77 ms                                                                | 175 ms: 22.46x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                          |
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260710-3.16.0a0-c22e9c9-NOGIL/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.072x slower

# HPT report

- Reliability score: 98.92% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x