# Results vs. 3.13.0rc2

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: linux-x86_64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.055x faster
- HPT reliability: 99.73%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 253 ms: 1.03x faster                                                      |
| docutils       | 2.63 sec                                                               | 2.28 sec: 1.15x faster                                                    |
| html5lib       | 68.6 ms                                                                | 58.4 ms: 1.18x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.12x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_generators           | 375 ms                                                                 | 227 ms: 1.65x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 660 ms: 1.34x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 347 ms: 1.33x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 503 ms: 1.33x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 688 ms: 1.31x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 274 ms: 1.29x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 513 ms: 1.23x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 344 ms: 1.19x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 283 ms: 1.18x faster                                                      |
| asyncio_tcp                | 502 ms                                                                 | 447 ms: 1.12x faster                                                      |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.46 sec: 1.04x faster                                                    |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.21x faster                                                              |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 178 ms: 1.22x faster                                                      |
| float          | 76.7 ms                                                                | 71.8 ms: 1.07x faster                                                     |
| nbody          | 85.3 ms                                                                | 90.3 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.65 ms: 1.21x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 21.0 ms: 1.10x faster                                                     |
| regex_dna      | 189 ms                                                                 | 172 ms: 1.09x faster                                                      |
| regex_compile  | 131 ms                                                                 | 147 ms: 1.12x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.27 ms: 1.15x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.79 sec: 1.12x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.8 ms: 1.03x faster                                                     |
| unpickle             | 14.6 us                                                                | 14.3 us: 1.02x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 86.4 ms: 1.01x slower                                                     |
| unpickle_pure_python | 208 us                                                                 | 211 us: 1.01x slower                                                      |
| pickle_dict          | 32.7 us                                                                | 33.5 us: 1.02x slower                                                     |
| xml_etree_process    | 59.2 ms                                                                | 61.9 ms: 1.04x slower                                                     |
| xml_etree_parse      | 136 ms                                                                 | 144 ms: 1.06x slower                                                      |
| pickle_pure_python   | 292 us                                                                 | 315 us: 1.08x slower                                                      |
| pickle               | 11.4 us                                                                | 12.6 us: 1.10x slower                                                     |
| unpickle_list        | 4.60 us                                                                | 5.11 us: 1.11x slower                                                     |
| pickle_list          | 4.81 us                                                                | 5.42 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                              |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.32 ms: 1.01x faster                                                     |
| python_startup         | 11.0 ms                                                                | 11.0 ms: 1.00x faster                                                     |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                                | 11.4 ms: 1.02x slower                                                     |
| django_template | 34.2 ms                                                                | 36.3 ms: 1.06x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.04x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 108 ms: 2.94x faster                                                      |
| mdp                        | 2.34 sec                                                               | 1.14 sec: 2.05x faster                                                    |
| async_generators           | 375 ms                                                                 | 227 ms: 1.65x faster                                                      |
| deepcopy                   | 357 us                                                                 | 232 us: 1.54x faster                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 108 us: 1.44x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 27.8 us: 1.37x faster                                                     |
| go                         | 141 ms                                                                 | 104 ms: 1.35x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 660 ms: 1.34x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 347 ms: 1.33x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 503 ms: 1.33x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 688 ms: 1.31x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 274 ms: 1.29x faster                                                      |
| scimark_sor                | 134 ms                                                                 | 108 ms: 1.24x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 513 ms: 1.23x faster                                                      |
| deepcopy_reduce            | 3.12 us                                                                | 2.54 us: 1.23x faster                                                     |
| pidigits                   | 216 ms                                                                 | 178 ms: 1.22x faster                                                      |
| regex_effbot               | 3.21 ms                                                                | 2.65 ms: 1.21x faster                                                     |
| spectral_norm              | 108 ms                                                                 | 89.4 ms: 1.20x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 344 ms: 1.19x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 283 ms: 1.18x faster                                                      |
| html5lib                   | 68.6 ms                                                                | 58.4 ms: 1.18x faster                                                     |
| docutils                   | 2.63 sec                                                               | 2.28 sec: 1.15x faster                                                    |
| json_dumps                 | 10.6 ms                                                                | 9.27 ms: 1.15x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 304 ms: 1.14x faster                                                      |
| pyflate                    | 449 ms                                                                 | 398 ms: 1.13x faster                                                      |
| asyncio_tcp                | 502 ms                                                                 | 447 ms: 1.12x faster                                                      |
| tomli_loads                | 2.01 sec                                                               | 1.79 sec: 1.12x faster                                                    |
| dulwich_log                | 74.5 ms                                                                | 66.5 ms: 1.12x faster                                                     |
| regex_v8                   | 23.2 ms                                                                | 21.0 ms: 1.10x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 172 ms: 1.09x faster                                                      |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.38 ms: 1.08x faster                                                     |
| pathlib                    | 19.3 ms                                                                | 17.8 ms: 1.08x faster                                                     |
| bpe_tokeniser              | 4.46 sec                                                               | 4.16 sec: 1.07x faster                                                    |
| float                      | 76.7 ms                                                                | 71.8 ms: 1.07x faster                                                     |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.0 ms: 1.06x faster                                                     |
| hexiom                     | 5.95 ms                                                                | 5.63 ms: 1.06x faster                                                     |
| nqueens                    | 77.7 ms                                                                | 74.2 ms: 1.05x faster                                                     |
| comprehensions             | 16.6 us                                                                | 16.0 us: 1.04x faster                                                     |
| sympy_integrate            | 19.7 ms                                                                | 19.0 ms: 1.04x faster                                                     |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.46 sec: 1.04x faster                                                    |
| chaos                      | 56.3 ms                                                                | 54.7 ms: 1.03x faster                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 66.3 ms: 1.03x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.8 ms: 1.03x faster                                                     |
| sqlite_synth               | 2.25 us                                                                | 2.19 us: 1.03x faster                                                     |
| 2to3                       | 259 ms                                                                 | 253 ms: 1.03x faster                                                      |
| unpickle                   | 14.6 us                                                                | 14.3 us: 1.02x faster                                                     |
| generators                 | 28.5 ms                                                                | 28.1 ms: 1.01x faster                                                     |
| python_startup_no_site     | 7.41 ms                                                                | 7.32 ms: 1.01x faster                                                     |
| fannkuch                   | 376 ms                                                                 | 374 ms: 1.00x faster                                                      |
| python_startup             | 11.0 ms                                                                | 11.0 ms: 1.00x faster                                                     |
| logging_silent             | 98.2 ns                                                                | 98.8 ns: 1.01x slower                                                     |
| logging_format             | 6.92 us                                                                | 6.97 us: 1.01x slower                                                     |
| logging_simple             | 6.14 us                                                                | 6.20 us: 1.01x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 86.4 ms: 1.01x slower                                                     |
| unpickle_pure_python       | 208 us                                                                 | 211 us: 1.01x slower                                                      |
| richards_super             | 50.4 ms                                                                | 51.2 ms: 1.02x slower                                                     |
| mako                       | 11.2 ms                                                                | 11.4 ms: 1.02x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 731 ms: 1.02x slower                                                      |
| sympy_sum                  | 154 ms                                                                 | 157 ms: 1.02x slower                                                      |
| sympy_str                  | 274 ms                                                                 | 280 ms: 1.02x slower                                                      |
| pprint_pformat             | 1.46 sec                                                               | 1.49 sec: 1.02x slower                                                    |
| richards                   | 44.4 ms                                                                | 45.4 ms: 1.02x slower                                                     |
| thrift                     | 772 us                                                                 | 790 us: 1.02x slower                                                      |
| coverage                   | 82.5 ms                                                                | 84.5 ms: 1.02x slower                                                     |
| pickle_dict                | 32.7 us                                                                | 33.5 us: 1.02x slower                                                     |
| raytrace                   | 250 ms                                                                 | 257 ms: 1.03x slower                                                      |
| create_gc_cycles           | 1.33 ms                                                                | 1.37 ms: 1.03x slower                                                     |
| xml_etree_process          | 59.2 ms                                                                | 61.9 ms: 1.04x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 474 ms: 1.05x slower                                                      |
| pycparser                  | 1.12 sec                                                               | 1.18 sec: 1.05x slower                                                    |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| nbody                      | 85.3 ms                                                                | 90.3 ms: 1.06x slower                                                     |
| scimark_lu                 | 112 ms                                                                 | 119 ms: 1.06x slower                                                      |
| django_template            | 34.2 ms                                                                | 36.3 ms: 1.06x slower                                                     |
| xml_etree_parse            | 136 ms                                                                 | 144 ms: 1.06x slower                                                      |
| deltablue                  | 3.10 ms                                                                | 3.32 ms: 1.07x slower                                                     |
| pickle_pure_python         | 292 us                                                                 | 315 us: 1.08x slower                                                      |
| gc_traversal               | 3.32 ms                                                                | 3.60 ms: 1.08x slower                                                     |
| pickle                     | 11.4 us                                                                | 12.6 us: 1.10x slower                                                     |
| unpickle_list              | 4.60 us                                                                | 5.11 us: 1.11x slower                                                     |
| regex_compile              | 131 ms                                                                 | 147 ms: 1.12x slower                                                      |
| pickle_list                | 4.81 us                                                                | 5.42 us: 1.13x slower                                                     |
| unpack_sequence            | 39.3 ns                                                                | 47.5 ns: 1.21x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 1.33 ms: 1.44x slower                                                     |
| telco                      | 7.77 ms                                                                | 161 ms: 20.66x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                                | 276 ms: 25.09x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (4): json, meteor_contest, json_loads, coroutines
Ignored benchmarks (12) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20261114-3.16.0a2+dev-edd6f76/bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.055x faster

# HPT report

- Reliability score: 99.73% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x