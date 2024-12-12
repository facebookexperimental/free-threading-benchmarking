# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: compare_op
- machine: linux-x86_64
- commit hash: 47785d8
- commit date: 2024-12-11
- overall geometric mean: 1.243x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 364 ms: 1.40x slower                                        |
| docutils       | 2.62 sec                                                     | 3.08 sec: 1.18x slower                                      |
| html5lib       | 67.0 ms                                                      | 95.2 ms: 1.42x slower                                       |
| Geometric mean | (ref)                                                        | 1.33x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 818 ms: 1.12x faster                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 635 ms: 1.05x faster                                        |
| async_tree_io              | 876 ms                                                       | 843 ms: 1.04x faster                                        |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 615 ms: 1.04x faster                                        |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.03x slower                                       |
| async_tree_none_tg         | 336 ms                                                       | 357 ms: 1.06x slower                                        |
| async_tree_memoization_tg  | 414 ms                                                       | 449 ms: 1.08x slower                                        |
| async_tree_none            | 354 ms                                                       | 387 ms: 1.09x slower                                        |
| async_generators           | 377 ms                                                       | 462 ms: 1.22x slower                                        |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                        |
| nbody          | 85.1 ms                                                      | 130 ms: 1.53x slower                                        |
| float          | 77.5 ms                                                      | 138 ms: 1.78x slower                                        |
| Geometric mean | (ref)                                                        | 1.32x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                       |
| regex_v8       | 22.7 ms                                                      | 24.3 ms: 1.07x slower                                       |
| regex_compile  | 132 ms                                                       | 179 ms: 1.35x slower                                        |
| Geometric mean | (ref)                                                        | 1.07x slower                                                |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 90.3 ms: 1.05x faster                                       |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                        |
| json_loads           | 27.0 us                                                      | 28.5 us: 1.06x slower                                       |
| xml_etree_generate   | 85.4 ms                                                      | 98.9 ms: 1.16x slower                                       |
| tomli_loads          | 2.01 sec                                                     | 2.47 sec: 1.23x slower                                      |
| xml_etree_process    | 59.3 ms                                                      | 78.6 ms: 1.32x slower                                       |
| json_dumps           | 10.5 ms                                                      | 14.2 ms: 1.35x slower                                       |
| unpickle_pure_python | 210 us                                                       | 329 us: 1.57x slower                                        |
| pickle_pure_python   | 294 us                                                       | 497 us: 1.69x slower                                        |
| Geometric mean       | (ref)                                                        | 1.23x slower                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                       |
| python_startup         | 11.0 ms                                                      | 17.4 ms: 1.58x slower                                       |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 64.3 ms: 1.32x slower                                       |
| genshi_text     | 21.5 ms                                                      | 31.4 ms: 1.46x slower                                       |
| django_template | 34.1 ms                                                      | 50.1 ms: 1.47x slower                                       |
| mako            | 11.3 ms                                                      | 17.7 ms: 1.56x slower                                       |
| Geometric mean  | (ref)                                                        | 1.45x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                        |
| async_tree_io_tg           | 913 ms                                                       | 818 ms: 1.12x faster                                        |
| regex_effbot               | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                       |
| deepcopy                   | 355 us                                                       | 331 us: 1.07x faster                                        |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.3 ms: 1.05x faster                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 635 ms: 1.05x faster                                        |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                        |
| async_tree_io              | 876 ms                                                       | 843 ms: 1.04x faster                                        |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 615 ms: 1.04x faster                                        |
| gc_traversal               | 3.14 ms                                                      | 3.18 ms: 1.01x slower                                       |
| sqlite_synth               | 2.21 us                                                      | 2.27 us: 1.03x slower                                       |
| deepcopy_memo              | 39.1 us                                                      | 40.4 us: 1.03x slower                                       |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.03x slower                                       |
| json                       | 4.93 ms                                                      | 5.11 ms: 1.04x slower                                       |
| json_loads                 | 27.0 us                                                      | 28.5 us: 1.06x slower                                       |
| pathlib                    | 19.2 ms                                                      | 20.3 ms: 1.06x slower                                       |
| async_tree_none_tg         | 336 ms                                                       | 357 ms: 1.06x slower                                        |
| regex_v8                   | 22.7 ms                                                      | 24.3 ms: 1.07x slower                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 449 ms: 1.08x slower                                        |
| async_tree_none            | 354 ms                                                       | 387 ms: 1.09x slower                                        |
| spectral_norm              | 111 ms                                                       | 122 ms: 1.10x slower                                        |
| telco                      | 7.82 ms                                                      | 8.66 ms: 1.11x slower                                       |
| bpe_tokeniser              | 4.45 sec                                                     | 4.94 sec: 1.11x slower                                      |
| deepcopy_reduce            | 3.11 us                                                      | 3.51 us: 1.13x slower                                       |
| scimark_fft                | 349 ms                                                       | 396 ms: 1.13x slower                                        |
| xml_etree_generate         | 85.4 ms                                                      | 98.9 ms: 1.16x slower                                       |
| mdp                        | 2.36 sec                                                     | 2.76 sec: 1.17x slower                                      |
| docutils                   | 2.62 sec                                                     | 3.08 sec: 1.18x slower                                      |
| coverage                   | 83.0 ms                                                      | 98.2 ms: 1.18x slower                                       |
| pylint                     | 317 ms                                                       | 380 ms: 1.20x slower                                        |
| async_generators           | 377 ms                                                       | 462 ms: 1.22x slower                                        |
| nqueens                    | 78.6 ms                                                      | 96.9 ms: 1.23x slower                                       |
| tomli_loads                | 2.01 sec                                                     | 2.47 sec: 1.23x slower                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.88 ms: 1.25x slower                                       |
| meteor_contest             | 102 ms                                                       | 128 ms: 1.26x slower                                        |
| dulwich_log                | 74.8 ms                                                      | 95.1 ms: 1.27x slower                                       |
| sqlglot_normalize          | 106 ms                                                       | 136 ms: 1.29x slower                                        |
| fannkuch                   | 370 ms                                                       | 479 ms: 1.30x slower                                        |
| sqlglot_optimize           | 52.7 ms                                                      | 68.7 ms: 1.30x slower                                       |
| pprint_safe_repr           | 738 ms                                                       | 970 ms: 1.32x slower                                        |
| genshi_xml                 | 48.8 ms                                                      | 64.3 ms: 1.32x slower                                       |
| xml_etree_process          | 59.3 ms                                                      | 78.6 ms: 1.32x slower                                       |
| pprint_pformat             | 1.50 sec                                                     | 2.01 sec: 1.34x slower                                      |
| typing_runtime_protocols   | 155 us                                                       | 208 us: 1.34x slower                                        |
| crypto_pyaes               | 67.9 ms                                                      | 91.2 ms: 1.34x slower                                       |
| json_dumps                 | 10.5 ms                                                      | 14.2 ms: 1.35x slower                                       |
| regex_compile              | 132 ms                                                       | 179 ms: 1.35x slower                                        |
| pycparser                  | 1.12 sec                                                     | 1.51 sec: 1.36x slower                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                       |
| generators                 | 28.8 ms                                                      | 39.3 ms: 1.36x slower                                       |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                       |
| 2to3                       | 260 ms                                                       | 364 ms: 1.40x slower                                        |
| html5lib                   | 67.0 ms                                                      | 95.2 ms: 1.42x slower                                       |
| genshi_text                | 21.5 ms                                                      | 31.4 ms: 1.46x slower                                       |
| django_template            | 34.1 ms                                                      | 50.1 ms: 1.47x slower                                       |
| sympy_integrate            | 19.8 ms                                                      | 29.2 ms: 1.47x slower                                       |
| pyflate                    | 449 ms                                                       | 666 ms: 1.49x slower                                        |
| thrift                     | 778 us                                                       | 1.16 ms: 1.49x slower                                       |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.53x slower                                        |
| mako                       | 11.3 ms                                                      | 17.7 ms: 1.56x slower                                       |
| unpickle_pure_python       | 210 us                                                       | 329 us: 1.57x slower                                        |
| python_startup             | 11.0 ms                                                      | 17.4 ms: 1.58x slower                                       |
| hexiom                     | 5.99 ms                                                      | 9.55 ms: 1.59x slower                                       |
| scimark_sor                | 134 ms                                                       | 221 ms: 1.65x slower                                        |
| comprehensions             | 16.5 us                                                      | 27.1 us: 1.65x slower                                       |
| scimark_lu                 | 113 ms                                                       | 186 ms: 1.65x slower                                        |
| pickle_pure_python         | 294 us                                                       | 497 us: 1.69x slower                                        |
| logging_format             | 6.84 us                                                      | 11.7 us: 1.70x slower                                       |
| richards_super             | 51.6 ms                                                      | 88.5 ms: 1.71x slower                                       |
| sympy_str                  | 275 ms                                                       | 472 ms: 1.72x slower                                        |
| richards                   | 45.2 ms                                                      | 78.2 ms: 1.73x slower                                       |
| logging_simple             | 6.16 us                                                      | 10.7 us: 1.73x slower                                       |
| scimark_monte_carlo        | 65.4 ms                                                      | 116 ms: 1.77x slower                                        |
| float                      | 77.5 ms                                                      | 138 ms: 1.78x slower                                        |
| chaos                      | 57.3 ms                                                      | 104 ms: 1.82x slower                                        |
| logging_silent             | 103 ns                                                       | 188 ns: 1.83x slower                                        |
| sqlglot_transpile          | 1.56 ms                                                      | 2.91 ms: 1.86x slower                                       |
| go                         | 141 ms                                                       | 266 ms: 1.89x slower                                        |
| sqlglot_parse              | 1.25 ms                                                      | 2.52 ms: 2.02x slower                                       |
| sympy_expand               | 457 ms                                                       | 945 ms: 2.07x slower                                        |
| raytrace                   | 253 ms                                                       | 559 ms: 2.21x slower                                        |
| sympy_sum                  | 156 ms                                                       | 349 ms: 2.24x slower                                        |
| deltablue                  | 3.12 ms                                                      | 8.06 ms: 2.58x slower                                       |
| bench_thread_pool          | 919 us                                                       | 3.40 ms: 3.70x slower                                       |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.84x slower                                        |
| Geometric mean             | (ref)                                                        | 1.37x slower                                                |

Benchmark hidden because not significant (3): asyncio_websockets, regex_dna, async_tree_memoization
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241211-3.14.0a2+-47785d8-NOGIL/bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.243x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.23x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.32x