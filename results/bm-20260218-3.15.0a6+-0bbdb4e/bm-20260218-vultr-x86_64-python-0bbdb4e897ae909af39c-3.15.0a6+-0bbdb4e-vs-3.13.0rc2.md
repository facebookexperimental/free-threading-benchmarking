# Results vs. 3.13.0rc2

- fork: python
- ref: 0bbdb4e897ae909af39c
- machine: linux-x86_64
- commit hash: 0bbdb4e
- commit date: 2026-02-18
- overall geometric mean: 1.045x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 246 ms: 1.05x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.53 sec: 1.04x faster                                                 |
| html5lib       | 67.0 ms                                                      | 59.8 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 568 ms: 1.61x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 301 ms: 1.53x faster                                                   |
| async_tree_io              | 876 ms                                                       | 573 ms: 1.53x faster                                                   |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 295 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 485 ms: 1.37x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 492 ms: 1.30x faster                                                   |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                   |
| float          | 77.5 ms                                                      | 69.6 ms: 1.11x faster                                                  |
| nbody          | 85.1 ms                                                      | 88.2 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.66 ms: 1.16x faster                                                  |
| regex_compile  | 132 ms                                                       | 121 ms: 1.09x faster                                                   |
| regex_dna      | 180 ms                                                       | 165 ms: 1.09x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 21.3 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                        | 1.10x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 83.8 ms: 1.13x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 9.85 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.8 ms: 1.01x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 211 us: 1.01x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 305 us: 1.04x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.3 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.33 ms: 1.01x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.8 ms: 1.03x faster                                                  |
| django_template | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                  |
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 568 ms: 1.61x faster                                                   |
| deepcopy                   | 355 us                                                       | 231 us: 1.54x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 301 ms: 1.53x faster                                                   |
| async_tree_io              | 876 ms                                                       | 573 ms: 1.53x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.3 us: 1.48x faster                                                  |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 295 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 485 ms: 1.37x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                   |
| go                         | 141 ms                                                       | 107 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 492 ms: 1.30x faster                                                   |
| scimark_sor                | 134 ms                                                       | 104 ms: 1.29x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.51 us: 1.24x faster                                                  |
| spectral_norm              | 111 ms                                                       | 94.6 ms: 1.17x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.66 ms: 1.16x faster                                                  |
| scimark_fft                | 349 ms                                                       | 303 ms: 1.15x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.8 ms: 1.13x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.8 ms: 1.12x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 66.8 ms: 1.12x faster                                                  |
| pylint                     | 317 ms                                                       | 283 ms: 1.12x faster                                                   |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                   |
| float                      | 77.5 ms                                                      | 69.6 ms: 1.11x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.3 ms: 1.11x faster                                                  |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                                   |
| regex_compile              | 132 ms                                                       | 121 ms: 1.09x faster                                                   |
| regex_dna                  | 180 ms                                                       | 165 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.34 ms: 1.09x faster                                                  |
| pyflate                    | 449 ms                                                       | 415 ms: 1.08x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.85 ms: 1.07x faster                                                  |
| generators                 | 28.8 ms                                                      | 27.0 ms: 1.07x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.61 ms: 1.07x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.4 ms: 1.07x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.3 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.18 sec: 1.06x faster                                                 |
| richards                   | 45.2 ms                                                      | 42.6 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 696 ms: 1.06x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.7 ms: 1.06x faster                                                  |
| 2to3                       | 260 ms                                                       | 246 ms: 1.05x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 107 ms: 1.05x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.92 us: 1.04x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.53 sec: 1.04x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.60 us: 1.04x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.8 ms: 1.03x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| chaos                      | 57.3 ms                                                      | 55.6 ms: 1.03x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.03x faster                                                 |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                  |
| logging_silent             | 103 ns                                                       | 100 ns: 1.02x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                  |
| meteor_contest             | 102 ms                                                       | 99.6 ms: 1.02x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 77.1 ms: 1.02x faster                                                  |
| coverage                   | 83.0 ms                                                      | 82.0 ms: 1.01x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.8 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.33 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                       | 252 ms: 1.00x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 211 us: 1.01x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 158 ms: 1.01x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                  |
| sympy_expand               | 457 ms                                                       | 470 ms: 1.03x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 160 us: 1.03x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 305 us: 1.04x slower                                                   |
| nbody                      | 85.1 ms                                                      | 88.2 ms: 1.04x slower                                                  |
| fannkuch                   | 370 ms                                                       | 385 ms: 1.04x slower                                                   |
| json                       | 4.93 ms                                                      | 5.14 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.3 us: 1.05x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.33 ms: 1.07x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.14x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.47 ms: 1.42x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.31 ms: 1.43x slower                                                  |
| telco                      | 7.82 ms                                                      | 157 ms: 20.00x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 331 ms: 30.08x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (5): sqlite_synth, genshi_xml, crypto_pyaes, sympy_str, thrift
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260218-3.15.0a6+-0bbdb4e/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.045x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.16x