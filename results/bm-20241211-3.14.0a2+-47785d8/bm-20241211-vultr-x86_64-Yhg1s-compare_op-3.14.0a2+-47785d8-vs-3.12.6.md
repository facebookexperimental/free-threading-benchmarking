# Results vs. 3.12.6

- fork: Yhg1s
- ref: compare_op
- machine: linux-x86_64
- commit hash: 47785d8
- commit date: 2024-12-11
- overall geometric mean: 1.079x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                        |
| docutils       | 2.64 sec                                               | 2.55 sec: 1.04x faster                                      |
| Geometric mean | (ref)                                                  | 1.04x faster                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                        |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                        |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                        |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                        |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.70x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 333 ms: 1.67x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 484 ms: 1.49x faster                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 501 ms: 1.43x faster                                        |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                       |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                        |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                        |
| Geometric mean             | (ref)                                                  | 1.47x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.2 ms: 1.05x faster                                       |
| pidigits       | 184 ms                                                 | 185 ms: 1.01x slower                                        |
| nbody          | 89.3 ms                                                | 90.3 ms: 1.01x slower                                       |
| Geometric mean | (ref)                                                  | 1.01x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.14x faster                                       |
| regex_compile  | 142 ms                                                 | 129 ms: 1.10x faster                                        |
| regex_dna      | 168 ms                                                 | 164 ms: 1.02x faster                                        |
| regex_v8       | 20.6 ms                                                | 24.1 ms: 1.17x slower                                       |
| Geometric mean | (ref)                                                  | 1.02x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                        |
| xml_etree_iterparse  | 96.7 ms                                                | 90.5 ms: 1.07x faster                                       |
| json_loads           | 26.5 us                                                | 25.0 us: 1.06x faster                                       |
| unpickle_pure_python | 221 us                                                 | 211 us: 1.05x faster                                        |
| xml_etree_generate   | 85.2 ms                                                | 84.2 ms: 1.01x faster                                       |
| xml_etree_process    | 59.0 ms                                                | 58.5 ms: 1.01x faster                                       |
| tomli_loads          | 2.11 sec                                               | 2.09 sec: 1.01x faster                                      |
| pickle_pure_python   | 308 us                                                 | 312 us: 1.01x slower                                        |
| json_dumps           | 10.4 ms                                                | 11.5 ms: 1.11x slower                                       |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.49 ms: 1.05x slower                                       |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                       |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.1 ms: 1.03x faster                                       |
| genshi_xml      | 50.2 ms                                                | 50.7 ms: 1.01x slower                                       |
| django_template | 34.7 ms                                                | 35.2 ms: 1.01x slower                                       |
| mako            | 11.0 ms                                                | 11.6 ms: 1.06x slower                                       |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                        |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                        |
| async_tree_io              | 1.08 sec                                               | 619 ms: 1.75x faster                                        |
| async_tree_none_tg         | 446 ms                                                 | 258 ms: 1.73x faster                                        |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.70x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 333 ms: 1.67x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 484 ms: 1.49x faster                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 501 ms: 1.43x faster                                        |
| deepcopy                   | 352 us                                                 | 258 us: 1.36x faster                                        |
| deepcopy_memo              | 40.3 us                                                | 30.2 us: 1.33x faster                                       |
| generators                 | 32.2 ms                                                | 27.0 ms: 1.19x faster                                       |
| go                         | 139 ms                                                 | 117 ms: 1.19x faster                                        |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                       |
| pathlib                    | 21.5 ms                                                | 18.4 ms: 1.17x faster                                       |
| comprehensions             | 19.8 us                                                | 17.0 us: 1.17x faster                                       |
| raytrace                   | 299 ms                                                 | 259 ms: 1.16x faster                                        |
| crypto_pyaes               | 76.6 ms                                                | 66.9 ms: 1.14x faster                                       |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.1 ms: 1.14x faster                                       |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.14x faster                                       |
| pylint                     | 319 ms                                                 | 283 ms: 1.13x faster                                        |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.13x faster                                        |
| bpe_tokeniser              | 4.74 sec                                               | 4.28 sec: 1.11x faster                                      |
| logging_simple             | 6.63 us                                                | 5.99 us: 1.11x faster                                       |
| regex_compile              | 142 ms                                                 | 129 ms: 1.10x faster                                        |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                       |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                        |
| chaos                      | 62.8 ms                                                | 58.0 ms: 1.08x faster                                       |
| thrift                     | 791 us                                                 | 732 us: 1.08x faster                                        |
| deltablue                  | 3.45 ms                                                | 3.19 ms: 1.08x faster                                       |
| logging_format             | 7.35 us                                                | 6.81 us: 1.08x faster                                       |
| sympy_str                  | 292 ms                                                 | 272 ms: 1.07x faster                                        |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                        |
| sqlglot_parse              | 1.36 ms                                                | 1.27 ms: 1.07x faster                                       |
| xml_etree_iterparse        | 96.7 ms                                                | 90.5 ms: 1.07x faster                                       |
| scimark_monte_carlo        | 68.4 ms                                                | 64.2 ms: 1.07x faster                                       |
| json                       | 5.02 ms                                                | 4.72 ms: 1.06x faster                                       |
| json_loads                 | 26.5 us                                                | 25.0 us: 1.06x faster                                       |
| sqlglot_transpile          | 1.67 ms                                                | 1.57 ms: 1.06x faster                                       |
| logging_silent             | 109 ns                                                 | 103 ns: 1.05x faster                                        |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                      |
| hexiom                     | 6.17 ms                                                | 5.88 ms: 1.05x faster                                       |
| async_generators           | 384 ms                                                 | 366 ms: 1.05x faster                                        |
| pprint_safe_repr           | 743 ms                                                 | 709 ms: 1.05x faster                                        |
| dulwich_log                | 78.9 ms                                                | 75.3 ms: 1.05x faster                                       |
| float                      | 80.8 ms                                                | 77.2 ms: 1.05x faster                                       |
| unpickle_pure_python       | 221 us                                                 | 211 us: 1.05x faster                                        |
| scimark_lu                 | 114 ms                                                 | 109 ms: 1.04x faster                                        |
| pprint_pformat             | 1.52 sec                                               | 1.46 sec: 1.04x faster                                      |
| sympy_integrate            | 20.5 ms                                                | 19.7 ms: 1.04x faster                                       |
| docutils                   | 2.64 sec                                               | 2.55 sec: 1.04x faster                                      |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                        |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                        |
| genshi_text                | 22.8 ms                                                | 22.1 ms: 1.03x faster                                       |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.03x faster                                        |
| scimark_fft                | 342 ms                                                 | 332 ms: 1.03x faster                                        |
| sympy_expand               | 468 ms                                                 | 456 ms: 1.02x faster                                        |
| regex_dna                  | 168 ms                                                 | 164 ms: 1.02x faster                                        |
| richards                   | 45.9 ms                                                | 45.0 ms: 1.02x faster                                       |
| fannkuch                   | 372 ms                                                 | 367 ms: 1.01x faster                                        |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                        |
| xml_etree_generate         | 85.2 ms                                                | 84.2 ms: 1.01x faster                                       |
| sqlglot_normalize          | 107 ms                                                 | 105 ms: 1.01x faster                                        |
| pyflate                    | 448 ms                                                 | 444 ms: 1.01x faster                                        |
| xml_etree_process          | 59.0 ms                                                | 58.5 ms: 1.01x faster                                       |
| tomli_loads                | 2.11 sec                                               | 2.09 sec: 1.01x faster                                      |
| sqlglot_optimize           | 53.3 ms                                                | 53.0 ms: 1.01x faster                                       |
| pidigits                   | 184 ms                                                 | 185 ms: 1.01x slower                                        |
| scimark_sor                | 130 ms                                                 | 131 ms: 1.01x slower                                        |
| genshi_xml                 | 50.2 ms                                                | 50.7 ms: 1.01x slower                                       |
| nbody                      | 89.3 ms                                                | 90.3 ms: 1.01x slower                                       |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                        |
| pickle_pure_python         | 308 us                                                 | 312 us: 1.01x slower                                        |
| django_template            | 34.7 ms                                                | 35.2 ms: 1.01x slower                                       |
| mdp                        | 2.42 sec                                               | 2.49 sec: 1.03x slower                                      |
| python_startup_no_site     | 7.16 ms                                                | 7.49 ms: 1.05x slower                                       |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.61 ms: 1.05x slower                                       |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.06x slower                                       |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                       |
| json_dumps                 | 10.4 ms                                                | 11.5 ms: 1.11x slower                                       |
| coverage                   | 71.4 ms                                                | 79.4 ms: 1.11x slower                                       |
| telco                      | 6.53 ms                                                | 7.52 ms: 1.15x slower                                       |
| gc_traversal               | 3.46 ms                                                | 4.04 ms: 1.17x slower                                       |
| regex_v8                   | 20.6 ms                                                | 24.1 ms: 1.17x slower                                       |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                       |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.68x slower                                       |
| bench_mp_pool              | 10.8 ms                                                | 89.1 ms: 8.25x slower                                       |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                |

Benchmark hidden because not significant (3): richards_super, nqueens, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241211-3.14.0a2+-47785d8/bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.11x