# Results vs. 3.13.0rc2

- fork: python
- ref: 5a15a52dd1dee37af4f2
- machine: linux-x86_64
- commit hash: 5a15a52
- commit date: 2026-03-08
- overall geometric mean: 1.039x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| html5lib       | 67.0 ms                                                      | 60.3 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 565 ms: 1.62x faster                                                   |
| async_tree_io              | 876 ms                                                       | 586 ms: 1.49x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                                   |
| async_tree_none            | 354 ms                                                       | 249 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 299 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 500 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                                   |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 68.9 ms: 1.12x faster                                                  |
| pidigits       | 217 ms                                                       | 221 ms: 1.02x slower                                                   |
| nbody          | 85.1 ms                                                      | 90.3 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 123 ms: 1.07x faster                                                   |
| regex_effbot   | 3.08 ms                                                      | 3.02 ms: 1.02x faster                                                  |
| regex_dna      | 180 ms                                                       | 187 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 85.3 ms: 1.11x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.81 sec: 1.11x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 9.66 ms: 1.09x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 82.6 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 57.9 ms: 1.03x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 211 us: 1.01x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 307 us: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                                  |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                  |
| django_template | 34.1 ms                                                      | 35.2 ms: 1.03x slower                                                  |
| mako            | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.06x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 565 ms: 1.62x faster                                                   |
| deepcopy                   | 355 us                                                       | 230 us: 1.55x faster                                                   |
| async_tree_io              | 876 ms                                                       | 586 ms: 1.49x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.3 us: 1.48x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 312 ms: 1.48x faster                                                   |
| async_tree_none            | 354 ms                                                       | 249 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 299 ms: 1.38x faster                                                   |
| go                         | 141 ms                                                       | 104 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 500 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                                   |
| scimark_sor                | 134 ms                                                       | 106 ms: 1.27x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.49 us: 1.25x faster                                                  |
| spectral_norm              | 111 ms                                                       | 92.0 ms: 1.21x faster                                                  |
| scimark_fft                | 349 ms                                                       | 308 ms: 1.13x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.1 ms: 1.12x faster                                                  |
| float                      | 77.5 ms                                                      | 68.9 ms: 1.12x faster                                                  |
| pylint                     | 317 ms                                                       | 284 ms: 1.12x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 66.9 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 85.3 ms: 1.11x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 60.3 ms: 1.11x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.81 sec: 1.11x faster                                                 |
| pyflate                    | 449 ms                                                       | 405 ms: 1.11x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.66 ms: 1.09x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.09 sec: 1.09x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.53 ms: 1.08x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.1 ms: 1.07x faster                                                  |
| regex_compile              | 132 ms                                                       | 123 ms: 1.07x faster                                                   |
| chaos                      | 57.3 ms                                                      | 53.4 ms: 1.07x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.3 ms: 1.07x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 74.0 ms: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.46 ms: 1.06x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.84 us: 1.06x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.0 ms: 1.05x faster                                                  |
| generators                 | 28.8 ms                                                      | 27.4 ms: 1.05x faster                                                  |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.08 sec: 1.04x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 82.6 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| logging_silent             | 103 ns                                                       | 99.7 ns: 1.03x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.03x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 57.9 ms: 1.03x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 719 ms: 1.03x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.03x faster                                                   |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 3.02 ms: 1.02x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.73 us: 1.02x faster                                                  |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| raytrace                   | 253 ms                                                       | 250 ms: 1.01x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 67.2 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 211 us: 1.01x slower                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 157 ms: 1.01x slower                                                   |
| sympy_str                  | 275 ms                                                       | 279 ms: 1.02x slower                                                   |
| pidigits                   | 217 ms                                                       | 221 ms: 1.02x slower                                                   |
| fannkuch                   | 370 ms                                                       | 380 ms: 1.03x slower                                                   |
| json                       | 4.93 ms                                                      | 5.08 ms: 1.03x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.2 ms: 1.03x slower                                                  |
| regex_dna                  | 180 ms                                                       | 187 ms: 1.04x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 307 us: 1.04x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 162 us: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.30 ms: 1.05x slower                                                  |
| nbody                      | 85.1 ms                                                      | 90.3 ms: 1.06x slower                                                  |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                  |
| sympy_expand               | 457 ms                                                       | 487 ms: 1.07x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.03 ms: 1.28x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.43x slower                                                  |
| telco                      | 7.82 ms                                                      | 159 ms: 20.35x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 265 ms: 24.09x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (4): coverage, thrift, genshi_xml, regex_v8
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260308-3.15.0a6+-5a15a52/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x