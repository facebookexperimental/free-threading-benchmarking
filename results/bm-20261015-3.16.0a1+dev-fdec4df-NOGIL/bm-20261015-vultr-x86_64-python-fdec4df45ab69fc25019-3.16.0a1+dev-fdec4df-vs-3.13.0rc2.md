# Results vs. 3.13.0rc2

- fork: python
- ref: fdec4df45ab69fc25019
- machine: linux-x86_64
- commit hash: fdec4df
- commit date: 2026-10-15
- overall geometric mean: 1.076x slower
- HPT reliability: 97.03%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 292 ms: 1.13x slower                                                      |
| docutils       | 2.63 sec                                                               | 2.88 sec: 1.10x slower                                                    |
| html5lib       | 68.6 ms                                                                | 66.9 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 708 ms: 1.27x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 725 ms: 1.22x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 428 ms: 1.07x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 634 ms: 1.05x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 617 ms: 1.03x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 345 ms: 1.03x faster                                                      |
| asyncio_websockets         | 517 ms                                                                 | 507 ms: 1.02x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 26.1 ms: 1.12x slower                                                     |
| async_generators           | 375 ms                                                                 | 424 ms: 1.13x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                              |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 204 ms: 1.06x faster                                                      |
| float          | 76.7 ms                                                                | 85.4 ms: 1.11x slower                                                     |
| nbody          | 85.3 ms                                                                | 122 ms: 1.43x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.79 ms: 1.15x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 21.2 ms: 1.10x faster                                                     |
| regex_dna      | 189 ms                                                                 | 178 ms: 1.06x faster                                                      |
| regex_compile  | 131 ms                                                                 | 170 ms: 1.29x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.87 ms: 1.08x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.94 sec: 1.04x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 97.2 ms: 1.03x slower                                                     |
| xml_etree_parse      | 136 ms                                                                 | 142 ms: 1.05x slower                                                      |
| json_loads           | 27.3 us                                                                | 30.6 us: 1.12x slower                                                     |
| pickle_pure_python   | 292 us                                                                 | 333 us: 1.14x slower                                                      |
| unpickle_pure_python | 208 us                                                                 | 239 us: 1.15x slower                                                      |
| xml_etree_generate   | 85.4 ms                                                                | 103 ms: 1.21x slower                                                      |
| xml_etree_process    | 59.2 ms                                                                | 77.0 ms: 1.30x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.55 ms: 1.29x slower                                                     |
| python_startup         | 11.0 ms                                                                | 16.1 ms: 1.46x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 41.2 ms: 1.20x slower                                                     |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 130 ms: 2.43x faster                                                      |
| gc_traversal               | 3.32 ms                                                                | 1.77 ms: 1.87x faster                                                     |
| mdp                        | 2.34 sec                                                               | 1.31 sec: 1.78x faster                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 6.71 ms: 1.64x faster                                                     |
| deepcopy                   | 357 us                                                                 | 267 us: 1.34x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 708 ms: 1.27x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 725 ms: 1.22x faster                                                      |
| go                         | 141 ms                                                                 | 121 ms: 1.17x faster                                                      |
| sqlite_synth               | 2.25 us                                                                | 1.94 us: 1.16x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.79 ms: 1.15x faster                                                     |
| deepcopy_memo              | 38.1 us                                                                | 33.2 us: 1.15x faster                                                     |
| scimark_sor                | 134 ms                                                                 | 120 ms: 1.11x faster                                                      |
| regex_v8                   | 23.2 ms                                                                | 21.2 ms: 1.10x faster                                                     |
| json_dumps                 | 10.6 ms                                                                | 9.87 ms: 1.08x faster                                                     |
| pathlib                    | 19.3 ms                                                                | 17.9 ms: 1.08x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 428 ms: 1.07x faster                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 146 us: 1.06x faster                                                      |
| pidigits                   | 216 ms                                                                 | 204 ms: 1.06x faster                                                      |
| regex_dna                  | 189 ms                                                                 | 178 ms: 1.06x faster                                                      |
| scimark_fft                | 348 ms                                                                 | 330 ms: 1.06x faster                                                      |
| spectral_norm              | 108 ms                                                                 | 102 ms: 1.05x faster                                                      |
| deepcopy_reduce            | 3.12 us                                                                | 2.97 us: 1.05x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 634 ms: 1.05x faster                                                      |
| tomli_loads                | 2.01 sec                                                               | 1.94 sec: 1.04x faster                                                    |
| dulwich_log                | 74.5 ms                                                                | 72.4 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 617 ms: 1.03x faster                                                      |
| html5lib                   | 68.6 ms                                                                | 66.9 ms: 1.03x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 345 ms: 1.03x faster                                                      |
| asyncio_websockets         | 517 ms                                                                 | 507 ms: 1.02x faster                                                      |
| pyflate                    | 449 ms                                                                 | 440 ms: 1.02x faster                                                      |
| bpe_tokeniser              | 4.46 sec                                                               | 4.38 sec: 1.02x faster                                                    |
| create_gc_cycles           | 1.33 ms                                                                | 1.31 ms: 1.01x faster                                                     |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                    |
| xml_etree_iterparse        | 94.4 ms                                                                | 97.2 ms: 1.03x slower                                                     |
| xml_etree_parse            | 136 ms                                                                 | 142 ms: 1.05x slower                                                      |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.99 ms: 1.05x slower                                                     |
| chaos                      | 56.3 ms                                                                | 60.4 ms: 1.07x slower                                                     |
| json                       | 4.98 ms                                                                | 5.43 ms: 1.09x slower                                                     |
| docutils                   | 2.63 sec                                                               | 2.88 sec: 1.10x slower                                                    |
| logging_silent             | 98.2 ns                                                                | 108 ns: 1.10x slower                                                      |
| float                      | 76.7 ms                                                                | 85.4 ms: 1.11x slower                                                     |
| sympy_integrate            | 19.7 ms                                                                | 22.0 ms: 1.11x slower                                                     |
| comprehensions             | 16.6 us                                                                | 18.5 us: 1.12x slower                                                     |
| json_loads                 | 27.3 us                                                                | 30.6 us: 1.12x slower                                                     |
| coroutines                 | 23.3 ms                                                                | 26.1 ms: 1.12x slower                                                     |
| 2to3                       | 259 ms                                                                 | 292 ms: 1.13x slower                                                      |
| hexiom                     | 5.95 ms                                                                | 6.72 ms: 1.13x slower                                                     |
| async_generators           | 375 ms                                                                 | 424 ms: 1.13x slower                                                      |
| pprint_safe_repr           | 719 ms                                                                 | 813 ms: 1.13x slower                                                      |
| nqueens                    | 77.7 ms                                                                | 88.5 ms: 1.14x slower                                                     |
| pickle_pure_python         | 292 us                                                                 | 333 us: 1.14x slower                                                      |
| unpickle_pure_python       | 208 us                                                                 | 239 us: 1.15x slower                                                      |
| scimark_lu                 | 112 ms                                                                 | 130 ms: 1.16x slower                                                      |
| sympy_str                  | 274 ms                                                                 | 318 ms: 1.16x slower                                                      |
| logging_simple             | 6.14 us                                                                | 7.14 us: 1.16x slower                                                     |
| logging_format             | 6.92 us                                                                | 8.06 us: 1.16x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.70 sec: 1.17x slower                                                    |
| generators                 | 28.5 ms                                                                | 33.5 ms: 1.17x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 181 ms: 1.17x slower                                                      |
| scimark_monte_carlo        | 65.8 ms                                                                | 77.4 ms: 1.18x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 534 ms: 1.18x slower                                                      |
| raytrace                   | 250 ms                                                                 | 294 ms: 1.18x slower                                                      |
| thrift                     | 772 us                                                                 | 918 us: 1.19x slower                                                      |
| richards                   | 44.4 ms                                                                | 53.4 ms: 1.20x slower                                                     |
| richards_super             | 50.4 ms                                                                | 60.7 ms: 1.20x slower                                                     |
| django_template            | 34.2 ms                                                                | 41.2 ms: 1.20x slower                                                     |
| deltablue                  | 3.10 ms                                                                | 3.73 ms: 1.21x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 103 ms: 1.21x slower                                                      |
| meteor_contest             | 101 ms                                                                 | 125 ms: 1.23x slower                                                      |
| fannkuch                   | 376 ms                                                                 | 466 ms: 1.24x slower                                                      |
| crypto_pyaes               | 68.2 ms                                                                | 87.4 ms: 1.28x slower                                                     |
| python_startup_no_site     | 7.41 ms                                                                | 9.55 ms: 1.29x slower                                                     |
| regex_compile              | 131 ms                                                                 | 170 ms: 1.29x slower                                                      |
| xml_etree_process          | 59.2 ms                                                                | 77.0 ms: 1.30x slower                                                     |
| coverage                   | 82.5 ms                                                                | 116 ms: 1.40x slower                                                      |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                     |
| nbody                      | 85.3 ms                                                                | 122 ms: 1.43x slower                                                      |
| python_startup             | 11.0 ms                                                                | 16.1 ms: 1.46x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 1.63 ms: 1.77x slower                                                     |
| telco                      | 7.77 ms                                                                | 176 ms: 22.67x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                              |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_none_tg
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261015-3.16.0a1+dev-fdec4df-NOGIL/bm-20261015-vultr-x86_64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.076x slower

# HPT report

- Reliability score: 97.03% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.34x