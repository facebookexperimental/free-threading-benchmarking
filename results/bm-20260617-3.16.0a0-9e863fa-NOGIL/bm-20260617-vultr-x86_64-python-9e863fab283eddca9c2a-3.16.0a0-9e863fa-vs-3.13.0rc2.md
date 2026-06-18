# Results vs. 3.13.0rc2

- fork: python
- ref: 9e863fab283eddca9c2a
- machine: linux-x86_64
- commit hash: 9e863fa
- commit date: 2026-06-17
- overall geometric mean: 1.066x slower
- HPT reliability: 97.98%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 295 ms: 1.14x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.94 sec: 1.12x slower                                                |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 677 ms: 1.33x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 698 ms: 1.26x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 417 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 606 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 579 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 390 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 319 ms: 1.04x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 340 ms: 1.04x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                                  |
| async_generators           | 375 ms                                                                 | 388 ms: 1.04x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 24.7 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 180 ms: 1.20x faster                                                  |
| float          | 76.7 ms                                                                | 86.4 ms: 1.13x slower                                                 |
| nbody          | 85.3 ms                                                                | 127 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 20.1 ms: 1.15x faster                                                 |
| regex_dna      | 189 ms                                                                 | 177 ms: 1.07x faster                                                  |
| regex_effbot   | 3.21 ms                                                                | 3.02 ms: 1.06x faster                                                 |
| regex_compile  | 131 ms                                                                 | 141 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.97 sec: 1.02x faster                                                |
| json_dumps           | 10.6 ms                                                                | 10.6 ms: 1.00x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 94.9 ms: 1.01x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 141 ms: 1.03x slower                                                  |
| json_loads           | 27.3 us                                                                | 30.5 us: 1.11x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 239 us: 1.15x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 337 us: 1.15x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 99.2 ms: 1.16x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 74.4 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.15 ms: 1.23x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.4 ms: 1.40x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.31x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 40.1 ms: 1.17x slower                                                 |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 132 ms: 2.40x faster                                                  |
| gc_traversal               | 3.32 ms                                                                | 1.77 ms: 1.88x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.32 sec: 1.78x faster                                                |
| bench_mp_pool              | 11.0 ms                                                                | 6.79 ms: 1.62x faster                                                 |
| deepcopy                   | 357 us                                                                 | 265 us: 1.35x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 677 ms: 1.33x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 698 ms: 1.26x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 31.1 us: 1.22x faster                                                 |
| pidigits                   | 216 ms                                                                 | 180 ms: 1.20x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 1.94 us: 1.16x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 20.1 ms: 1.15x faster                                                 |
| go                         | 141 ms                                                                 | 122 ms: 1.15x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 417 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 606 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 579 ms: 1.09x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 123 ms: 1.09x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 17.7 ms: 1.09x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.90 us: 1.08x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 177 ms: 1.07x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 3.02 ms: 1.06x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 148 us: 1.05x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 390 ms: 1.05x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 71.0 ms: 1.05x faster                                                 |
| async_tree_none_tg         | 333 ms                                                                 | 319 ms: 1.04x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 340 ms: 1.04x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.97 sec: 1.02x faster                                                |
| bpe_tokeniser              | 4.46 sec                                                               | 4.37 sec: 1.02x faster                                                |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                                  |
| json_dumps                 | 10.6 ms                                                                | 10.6 ms: 1.00x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 94.9 ms: 1.01x slower                                                 |
| scimark_fft                | 348 ms                                                                 | 351 ms: 1.01x slower                                                  |
| pyflate                    | 449 ms                                                                 | 457 ms: 1.02x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                                 |
| xml_etree_parse            | 136 ms                                                                 | 141 ms: 1.03x slower                                                  |
| async_generators           | 375 ms                                                                 | 388 ms: 1.04x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 112 ms: 1.04x slower                                                  |
| json                       | 4.98 ms                                                                | 5.23 ms: 1.05x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 24.7 ms: 1.06x slower                                                 |
| comprehensions             | 16.6 us                                                                | 17.8 us: 1.07x slower                                                 |
| regex_compile              | 131 ms                                                                 | 141 ms: 1.08x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 107 ns: 1.09x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 21.8 ms: 1.10x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 795 ms: 1.11x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.81 us: 1.11x slower                                                 |
| json_loads                 | 27.3 us                                                                | 30.5 us: 1.11x slower                                                 |
| chaos                      | 56.3 ms                                                                | 62.9 ms: 1.12x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.94 sec: 1.12x slower                                                |
| logging_format             | 6.92 us                                                                | 7.77 us: 1.12x slower                                                 |
| float                      | 76.7 ms                                                                | 86.4 ms: 1.13x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.71 ms: 1.13x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 87.7 ms: 1.13x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 309 ms: 1.13x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.65 sec: 1.13x slower                                                |
| 2to3                       | 259 ms                                                                 | 295 ms: 1.14x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.42 ms: 1.14x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 518 ms: 1.14x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 239 us: 1.15x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 178 ms: 1.15x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 337 us: 1.15x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 130 ms: 1.16x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 99.2 ms: 1.16x slower                                                 |
| generators                 | 28.5 ms                                                                | 33.4 ms: 1.17x slower                                                 |
| thrift                     | 772 us                                                                 | 902 us: 1.17x slower                                                  |
| django_template            | 34.2 ms                                                                | 40.1 ms: 1.17x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.69 ms: 1.19x slower                                                 |
| richards_super             | 50.4 ms                                                                | 60.2 ms: 1.19x slower                                                 |
| richards                   | 44.4 ms                                                                | 53.2 ms: 1.20x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 79.5 ms: 1.21x slower                                                 |
| raytrace                   | 250 ms                                                                 | 304 ms: 1.22x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 124 ms: 1.22x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.15 ms: 1.23x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 470 ms: 1.25x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 74.4 ms: 1.26x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 89.6 ms: 1.31x slower                                                 |
| coverage                   | 82.5 ms                                                                | 114 ms: 1.39x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.4 ms: 1.40x slower                                                 |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                                 |
| nbody                      | 85.3 ms                                                                | 127 ms: 1.49x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.47 ms: 1.59x slower                                                 |
| telco                      | 7.77 ms                                                                | 175 ms: 22.55x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260617-3.16.0a0-9e863fa-NOGIL/bm-20260617-vultr-x86_64-python-9e863fab283eddca9c2a-3.16.0a0-9e863fa.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.066x slower

# HPT report

- Reliability score: 97.98% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.34x