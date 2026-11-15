# Results vs. 3.13.0rc2

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: linux-x86_64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.090x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 247 ms: 1.05x faster                                                      |
| docutils       | 2.63 sec                                                               | 2.22 sec: 1.19x faster                                                    |
| html5lib       | 68.6 ms                                                                | 57.8 ms: 1.19x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.14x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_generators           | 375 ms                                                                 | 219 ms: 1.71x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 482 ms: 1.38x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 639 ms: 1.38x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 337 ms: 1.36x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 674 ms: 1.34x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 267 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 496 ms: 1.28x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 332 ms: 1.23x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 272 ms: 1.22x faster                                                      |
| asyncio_tcp                | 502 ms                                                                 | 441 ms: 1.14x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 22.3 ms: 1.05x faster                                                     |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.46 sec: 1.04x faster                                                    |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.25x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 185 ms: 1.17x faster                                                      |
| float          | 76.7 ms                                                                | 69.5 ms: 1.10x faster                                                     |
| nbody          | 85.3 ms                                                                | 82.7 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 22.5 ms: 1.03x faster                                                     |
| regex_dna      | 189 ms                                                                 | 199 ms: 1.06x slower                                                      |
| regex_compile  | 131 ms                                                                 | 144 ms: 1.09x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                              |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 8.48 ms: 1.25x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.82 sec: 1.11x faster                                                    |
| unpickle_list        | 4.60 us                                                                | 4.21 us: 1.09x faster                                                     |
| json_loads           | 27.3 us                                                                | 26.4 us: 1.03x faster                                                     |
| unpickle             | 14.6 us                                                                | 14.1 us: 1.03x faster                                                     |
| pickle_dict          | 32.7 us                                                                | 31.7 us: 1.03x faster                                                     |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.7 ms: 1.03x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 83.3 ms: 1.03x faster                                                     |
| xml_etree_process    | 59.2 ms                                                                | 57.9 ms: 1.02x faster                                                     |
| unpickle_pure_python | 208 us                                                                 | 204 us: 1.02x faster                                                      |
| pickle_pure_python   | 292 us                                                                 | 298 us: 1.02x slower                                                      |
| pickle_list          | 4.81 us                                                                | 5.07 us: 1.05x slower                                                     |
| pickle               | 11.4 us                                                                | 12.5 us: 1.09x slower                                                     |
| xml_etree_parse      | 136 ms                                                                 | 152 ms: 1.12x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup | 11.0 ms                                                                | 11.1 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 33.2 ms: 1.03x faster                                                     |
| mako            | 11.2 ms                                                                | 11.9 ms: 1.06x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 104 ms: 3.06x faster                                                      |
| mdp                        | 2.34 sec                                                               | 1.08 sec: 2.17x faster                                                    |
| async_generators           | 375 ms                                                                 | 219 ms: 1.71x faster                                                      |
| deepcopy                   | 357 us                                                                 | 212 us: 1.69x faster                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 102 us: 1.53x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 26.9 us: 1.41x faster                                                     |
| go                         | 141 ms                                                                 | 101 ms: 1.40x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 482 ms: 1.38x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 639 ms: 1.38x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 337 ms: 1.36x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 674 ms: 1.34x faster                                                      |
| deepcopy_reduce            | 3.12 us                                                                | 2.34 us: 1.34x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 267 ms: 1.32x faster                                                      |
| scimark_sor                | 134 ms                                                                 | 103 ms: 1.29x faster                                                      |
| spectral_norm              | 108 ms                                                                 | 83.5 ms: 1.29x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 270 ms: 1.29x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 496 ms: 1.28x faster                                                      |
| json_dumps                 | 10.6 ms                                                                | 8.48 ms: 1.25x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 332 ms: 1.23x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 272 ms: 1.22x faster                                                      |
| pyflate                    | 449 ms                                                                 | 369 ms: 1.22x faster                                                      |
| html5lib                   | 68.6 ms                                                                | 57.8 ms: 1.19x faster                                                     |
| docutils                   | 2.63 sec                                                               | 2.22 sec: 1.19x faster                                                    |
| logging_silent             | 98.2 ns                                                                | 83.2 ns: 1.18x faster                                                     |
| pidigits                   | 216 ms                                                                 | 185 ms: 1.17x faster                                                      |
| comprehensions             | 16.6 us                                                                | 14.4 us: 1.15x faster                                                     |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.13 ms: 1.15x faster                                                     |
| asyncio_tcp                | 502 ms                                                                 | 441 ms: 1.14x faster                                                      |
| scimark_monte_carlo        | 65.8 ms                                                                | 58.0 ms: 1.13x faster                                                     |
| bpe_tokeniser              | 4.46 sec                                                               | 3.93 sec: 1.13x faster                                                    |
| pathlib                    | 19.3 ms                                                                | 17.0 ms: 1.13x faster                                                     |
| dulwich_log                | 74.5 ms                                                                | 66.3 ms: 1.12x faster                                                     |
| richards                   | 44.4 ms                                                                | 39.7 ms: 1.12x faster                                                     |
| nqueens                    | 77.7 ms                                                                | 69.8 ms: 1.11x faster                                                     |
| richards_super             | 50.4 ms                                                                | 45.5 ms: 1.11x faster                                                     |
| tomli_loads                | 2.01 sec                                                               | 1.82 sec: 1.11x faster                                                    |
| chaos                      | 56.3 ms                                                                | 50.9 ms: 1.11x faster                                                     |
| float                      | 76.7 ms                                                                | 69.5 ms: 1.10x faster                                                     |
| logging_simple             | 6.14 us                                                                | 5.58 us: 1.10x faster                                                     |
| hexiom                     | 5.95 ms                                                                | 5.43 ms: 1.10x faster                                                     |
| logging_format             | 6.92 us                                                                | 6.31 us: 1.10x faster                                                     |
| unpickle_list              | 4.60 us                                                                | 4.21 us: 1.09x faster                                                     |
| sympy_integrate            | 19.7 ms                                                                | 18.1 ms: 1.09x faster                                                     |
| deltablue                  | 3.10 ms                                                                | 2.87 ms: 1.08x faster                                                     |
| fannkuch                   | 376 ms                                                                 | 355 ms: 1.06x faster                                                      |
| 2to3                       | 259 ms                                                                 | 247 ms: 1.05x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 22.3 ms: 1.05x faster                                                     |
| sqlite_synth               | 2.25 us                                                                | 2.15 us: 1.04x faster                                                     |
| pycparser                  | 1.12 sec                                                               | 1.07 sec: 1.04x faster                                                    |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.46 sec: 1.04x faster                                                    |
| json_loads                 | 27.3 us                                                                | 26.4 us: 1.03x faster                                                     |
| coverage                   | 82.5 ms                                                                | 79.8 ms: 1.03x faster                                                     |
| unpickle                   | 14.6 us                                                                | 14.1 us: 1.03x faster                                                     |
| pickle_dict                | 32.7 us                                                                | 31.7 us: 1.03x faster                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 66.0 ms: 1.03x faster                                                     |
| nbody                      | 85.3 ms                                                                | 82.7 ms: 1.03x faster                                                     |
| regex_v8                   | 23.2 ms                                                                | 22.5 ms: 1.03x faster                                                     |
| sympy_sum                  | 154 ms                                                                 | 150 ms: 1.03x faster                                                      |
| scimark_lu                 | 112 ms                                                                 | 109 ms: 1.03x faster                                                      |
| django_template            | 34.2 ms                                                                | 33.2 ms: 1.03x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.7 ms: 1.03x faster                                                     |
| sympy_str                  | 274 ms                                                                 | 266 ms: 1.03x faster                                                      |
| raytrace                   | 250 ms                                                                 | 243 ms: 1.03x faster                                                      |
| xml_etree_generate         | 85.4 ms                                                                | 83.3 ms: 1.03x faster                                                     |
| xml_etree_process          | 59.2 ms                                                                | 57.9 ms: 1.02x faster                                                     |
| unpickle_pure_python       | 208 us                                                                 | 204 us: 1.02x faster                                                      |
| thrift                     | 772 us                                                                 | 755 us: 1.02x faster                                                      |
| python_startup             | 11.0 ms                                                                | 11.1 ms: 1.00x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 728 ms: 1.01x slower                                                      |
| pprint_pformat             | 1.46 sec                                                               | 1.48 sec: 1.02x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 103 ms: 1.02x slower                                                      |
| pickle_pure_python         | 292 us                                                                 | 298 us: 1.02x slower                                                      |
| generators                 | 28.5 ms                                                                | 29.5 ms: 1.03x slower                                                     |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| pickle_list                | 4.81 us                                                                | 5.07 us: 1.05x slower                                                     |
| regex_dna                  | 189 ms                                                                 | 199 ms: 1.06x slower                                                      |
| mako                       | 11.2 ms                                                                | 11.9 ms: 1.06x slower                                                     |
| unpack_sequence            | 39.3 ns                                                                | 42.4 ns: 1.08x slower                                                     |
| pickle                     | 11.4 us                                                                | 12.5 us: 1.09x slower                                                     |
| regex_compile              | 131 ms                                                                 | 144 ms: 1.09x slower                                                      |
| xml_etree_parse            | 136 ms                                                                 | 152 ms: 1.12x slower                                                      |
| gc_traversal               | 3.32 ms                                                                | 3.73 ms: 1.12x slower                                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.53 ms: 1.14x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 1.29 ms: 1.39x slower                                                     |
| telco                      | 7.77 ms                                                                | 153 ms: 19.74x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                                | 278 ms: 25.28x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                              |

Benchmark hidden because not significant (4): json, regex_effbot, python_startup_no_site, sympy_expand
Ignored benchmarks (12) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20261114-3.16.0a2+dev-edd6f76-CLANG/bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.17x