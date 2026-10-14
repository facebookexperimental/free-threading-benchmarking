# Results vs. 3.13.0rc2

- fork: python
- ref: 084aff869c4aa2f2cbdf
- machine: linux-x86_64
- commit hash: 084aff8
- commit date: 2026-10-13
- overall geometric mean: 1.045x faster
- HPT reliability: 99.67%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 255 ms: 1.02x faster                                                      |
| docutils       | 2.63 sec                                                               | 2.33 sec: 1.13x faster                                                    |
| html5lib       | 68.6 ms                                                                | 57.9 ms: 1.19x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 657 ms: 1.34x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 348 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 514 ms: 1.30x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 696 ms: 1.30x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 341 ms: 1.20x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 529 ms: 1.20x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 281 ms: 1.18x faster                                                      |
| async_generators           | 375 ms                                                                 | 350 ms: 1.07x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                     |
| asyncio_websockets         | 517 ms                                                                 | 543 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.19x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                                      |
| float          | 76.7 ms                                                                | 70.7 ms: 1.09x faster                                                     |
| nbody          | 85.3 ms                                                                | 90.2 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.57 ms: 1.25x faster                                                     |
| regex_dna      | 189 ms                                                                 | 166 ms: 1.14x faster                                                      |
| regex_v8       | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                                     |
| regex_compile  | 131 ms                                                                 | 150 ms: 1.14x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.06 ms: 1.17x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.5 ms: 1.03x faster                                                     |
| json_loads           | 27.3 us                                                                | 26.9 us: 1.02x faster                                                     |
| unpickle_pure_python | 208 us                                                                 | 212 us: 1.02x slower                                                      |
| xml_etree_generate   | 85.4 ms                                                                | 88.6 ms: 1.04x slower                                                     |
| xml_etree_parse      | 136 ms                                                                 | 143 ms: 1.05x slower                                                      |
| pickle_pure_python   | 292 us                                                                 | 307 us: 1.05x slower                                                      |
| xml_etree_process    | 59.2 ms                                                                | 62.8 ms: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.51 ms: 1.01x slower                                                     |
| python_startup         | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.08x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                     |
| django_template | 34.2 ms                                                                | 36.8 ms: 1.08x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.06x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 113 ms: 2.81x faster                                                      |
| mdp                        | 2.34 sec                                                               | 1.15 sec: 2.04x faster                                                    |
| deepcopy                   | 357 us                                                                 | 232 us: 1.54x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 27.6 us: 1.38x faster                                                     |
| go                         | 141 ms                                                                 | 104 ms: 1.36x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 657 ms: 1.34x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 348 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 514 ms: 1.30x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 696 ms: 1.30x faster                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 120 us: 1.29x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                      |
| regex_effbot               | 3.21 ms                                                                | 2.57 ms: 1.25x faster                                                     |
| scimark_sor                | 134 ms                                                                 | 109 ms: 1.22x faster                                                      |
| deepcopy_reduce            | 3.12 us                                                                | 2.57 us: 1.22x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 341 ms: 1.20x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 529 ms: 1.20x faster                                                      |
| spectral_norm              | 108 ms                                                                 | 90.1 ms: 1.19x faster                                                     |
| html5lib                   | 68.6 ms                                                                | 57.9 ms: 1.19x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 281 ms: 1.18x faster                                                      |
| json_dumps                 | 10.6 ms                                                                | 9.06 ms: 1.17x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 300 ms: 1.16x faster                                                      |
| pyflate                    | 449 ms                                                                 | 390 ms: 1.15x faster                                                      |
| regex_dna                  | 189 ms                                                                 | 166 ms: 1.14x faster                                                      |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                                      |
| docutils                   | 2.63 sec                                                               | 2.33 sec: 1.13x faster                                                    |
| dulwich_log                | 74.5 ms                                                                | 66.7 ms: 1.12x faster                                                     |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.29 ms: 1.11x faster                                                     |
| regex_v8                   | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                                     |
| tomli_loads                | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                                    |
| pathlib                    | 19.3 ms                                                                | 17.6 ms: 1.09x faster                                                     |
| float                      | 76.7 ms                                                                | 70.7 ms: 1.09x faster                                                     |
| async_generators           | 375 ms                                                                 | 350 ms: 1.07x faster                                                      |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.3 ms: 1.06x faster                                                     |
| bpe_tokeniser              | 4.46 sec                                                               | 4.23 sec: 1.05x faster                                                    |
| hexiom                     | 5.95 ms                                                                | 5.67 ms: 1.05x faster                                                     |
| chaos                      | 56.3 ms                                                                | 53.9 ms: 1.04x faster                                                     |
| comprehensions             | 16.6 us                                                                | 15.9 us: 1.04x faster                                                     |
| sympy_integrate            | 19.7 ms                                                                | 19.0 ms: 1.04x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.5 ms: 1.03x faster                                                     |
| nqueens                    | 77.7 ms                                                                | 75.4 ms: 1.03x faster                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 66.3 ms: 1.03x faster                                                     |
| sqlite_synth               | 2.25 us                                                                | 2.19 us: 1.03x faster                                                     |
| 2to3                       | 259 ms                                                                 | 255 ms: 1.02x faster                                                      |
| logging_silent             | 98.2 ns                                                                | 96.6 ns: 1.02x faster                                                     |
| json_loads                 | 27.3 us                                                                | 26.9 us: 1.02x faster                                                     |
| pycparser                  | 1.12 sec                                                               | 1.11 sec: 1.01x faster                                                    |
| generators                 | 28.5 ms                                                                | 28.4 ms: 1.01x faster                                                     |
| coverage                   | 82.5 ms                                                                | 83.1 ms: 1.01x slower                                                     |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                     |
| richards_super             | 50.4 ms                                                                | 50.9 ms: 1.01x slower                                                     |
| python_startup_no_site     | 7.41 ms                                                                | 7.51 ms: 1.01x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 730 ms: 1.02x slower                                                      |
| sympy_sum                  | 154 ms                                                                 | 157 ms: 1.02x slower                                                      |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                                     |
| raytrace                   | 250 ms                                                                 | 254 ms: 1.02x slower                                                      |
| pprint_pformat             | 1.46 sec                                                               | 1.48 sec: 1.02x slower                                                    |
| sympy_str                  | 274 ms                                                                 | 279 ms: 1.02x slower                                                      |
| unpickle_pure_python       | 208 us                                                                 | 212 us: 1.02x slower                                                      |
| meteor_contest             | 101 ms                                                                 | 103 ms: 1.02x slower                                                      |
| xml_etree_generate         | 85.4 ms                                                                | 88.6 ms: 1.04x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 472 ms: 1.04x slower                                                      |
| scimark_lu                 | 112 ms                                                                 | 117 ms: 1.04x slower                                                      |
| thrift                     | 772 us                                                                 | 806 us: 1.04x slower                                                      |
| xml_etree_parse            | 136 ms                                                                 | 143 ms: 1.05x slower                                                      |
| asyncio_websockets         | 517 ms                                                                 | 543 ms: 1.05x slower                                                      |
| gc_traversal               | 3.32 ms                                                                | 3.49 ms: 1.05x slower                                                     |
| mako                       | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                     |
| pickle_pure_python         | 292 us                                                                 | 307 us: 1.05x slower                                                      |
| nbody                      | 85.3 ms                                                                | 90.2 ms: 1.06x slower                                                     |
| xml_etree_process          | 59.2 ms                                                                | 62.8 ms: 1.06x slower                                                     |
| deltablue                  | 3.10 ms                                                                | 3.30 ms: 1.07x slower                                                     |
| django_template            | 34.2 ms                                                                | 36.8 ms: 1.08x slower                                                     |
| regex_compile              | 131 ms                                                                 | 150 ms: 1.14x slower                                                      |
| python_startup             | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 1.34 ms: 1.45x slower                                                     |
| telco                      | 7.77 ms                                                                | 162 ms: 20.78x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                                | 340 ms: 30.88x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (5): json, logging_format, richards, fannkuch, logging_simple
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261013-3.16.0a1+dev-084aff8/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.045x faster

# HPT report

- Reliability score: 99.67% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x