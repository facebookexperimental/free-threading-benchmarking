# Results vs. 3.12.6

- fork: mpage
- ref: revert_gc_changes
- machine: linux-x86_64
- commit hash: 2923163
- commit date: 2024-12-03
- overall geometric mean: 1.255x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 377 ms: 1.43x slower                                               |
| docutils       | 2.64 sec                                               | 3.18 sec: 1.21x slower                                             |
| html5lib       | 63.6 ms                                                | 99.7 ms: 1.57x slower                                              |
| Geometric mean | (ref)                                                  | 1.39x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 870 ms: 1.28x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 367 ms: 1.22x faster                                               |
| async_tree_io              | 1.08 sec                                               | 893 ms: 1.21x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 463 ms: 1.21x faster                                               |
| async_tree_none            | 464 ms                                                 | 401 ms: 1.16x faster                                               |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 629 ms: 1.15x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 491 ms: 1.13x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 652 ms: 1.10x faster                                               |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                               |
| coroutines                 | 23.9 ms                                                | 27.6 ms: 1.15x slower                                              |
| async_generators           | 384 ms                                                 | 468 ms: 1.22x slower                                               |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 182 ms: 1.01x faster                                               |
| nbody          | 89.3 ms                                                | 133 ms: 1.49x slower                                               |
| float          | 80.8 ms                                                | 144 ms: 1.78x slower                                               |
| Geometric mean | (ref)                                                  | 1.38x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.67 ms: 1.19x faster                                              |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                               |
| regex_v8       | 20.6 ms                                                | 23.3 ms: 1.13x slower                                              |
| regex_compile  | 142 ms                                                 | 193 ms: 1.36x slower                                               |
| Geometric mean | (ref)                                                  | 1.08x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                               |
| xml_etree_iterparse  | 96.7 ms                                                | 94.6 ms: 1.02x faster                                              |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.20x slower                                               |
| tomli_loads          | 2.11 sec                                               | 2.76 sec: 1.31x slower                                             |
| xml_etree_process    | 59.0 ms                                                | 82.3 ms: 1.40x slower                                              |
| json_dumps           | 10.4 ms                                                | 14.6 ms: 1.41x slower                                              |
| unpickle_pure_python | 221 us                                                 | 381 us: 1.73x slower                                               |
| pickle_pure_python   | 308 us                                                 | 567 us: 1.84x slower                                               |
| Geometric mean       | (ref)                                                  | 1.29x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                              |
| python_startup         | 9.93 ms                                                | 17.5 ms: 1.76x slower                                              |
| Geometric mean         | (ref)                                                  | 1.59x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 66.9 ms: 1.33x slower                                              |
| genshi_text     | 22.8 ms                                                | 33.9 ms: 1.49x slower                                              |
| django_template | 34.7 ms                                                | 56.0 ms: 1.62x slower                                              |
| mako            | 11.0 ms                                                | 20.1 ms: 1.82x slower                                              |
| Geometric mean  | (ref)                                                  | 1.55x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 870 ms: 1.28x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 367 ms: 1.22x faster                                               |
| async_tree_io              | 1.08 sec                                               | 893 ms: 1.21x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 463 ms: 1.21x faster                                               |
| regex_effbot               | 3.17 ms                                                | 2.67 ms: 1.19x faster                                              |
| async_tree_none            | 464 ms                                                 | 401 ms: 1.16x faster                                               |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 629 ms: 1.15x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 491 ms: 1.13x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 652 ms: 1.10x faster                                               |
| gc_traversal               | 3.46 ms                                                | 3.18 ms: 1.09x faster                                              |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                               |
| xml_etree_iterparse        | 96.7 ms                                                | 94.6 ms: 1.02x faster                                              |
| pathlib                    | 21.5 ms                                                | 21.1 ms: 1.02x faster                                              |
| pidigits                   | 184 ms                                                 | 182 ms: 1.01x faster                                               |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                               |
| json                       | 5.02 ms                                                | 5.09 ms: 1.01x slower                                              |
| deepcopy                   | 352 us                                                 | 356 us: 1.01x slower                                               |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                               |
| sqlite_synth               | 2.20 us                                                | 2.30 us: 1.04x slower                                              |
| json_loads                 | 26.5 us                                                | 28.2 us: 1.06x slower                                              |
| regex_v8                   | 20.6 ms                                                | 23.3 ms: 1.13x slower                                              |
| deepcopy_memo              | 40.3 us                                                | 45.7 us: 1.13x slower                                              |
| bpe_tokeniser              | 4.74 sec                                               | 5.46 sec: 1.15x slower                                             |
| coroutines                 | 23.9 ms                                                | 27.6 ms: 1.15x slower                                              |
| scimark_fft                | 342 ms                                                 | 406 ms: 1.19x slower                                               |
| spectral_norm              | 110 ms                                                 | 132 ms: 1.19x slower                                               |
| generators                 | 32.2 ms                                                | 38.6 ms: 1.20x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.20x slower                                               |
| docutils                   | 2.64 sec                                               | 3.18 sec: 1.21x slower                                             |
| async_generators           | 384 ms                                                 | 468 ms: 1.22x slower                                               |
| crypto_pyaes               | 76.6 ms                                                | 93.4 ms: 1.22x slower                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.76 us: 1.22x slower                                              |
| mdp                        | 2.42 sec                                               | 2.98 sec: 1.23x slower                                             |
| pylint                     | 319 ms                                                 | 394 ms: 1.24x slower                                               |
| dulwich_log                | 78.9 ms                                                | 98.8 ms: 1.25x slower                                              |
| nqueens                    | 80.1 ms                                                | 103 ms: 1.29x slower                                               |
| typing_runtime_protocols   | 163 us                                                 | 213 us: 1.31x slower                                               |
| meteor_contest             | 104 ms                                                 | 135 ms: 1.31x slower                                               |
| tomli_loads                | 2.11 sec                                               | 2.76 sec: 1.31x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 66.9 ms: 1.33x slower                                              |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.87 ms: 1.34x slower                                              |
| regex_compile              | 142 ms                                                 | 193 ms: 1.36x slower                                               |
| fannkuch                   | 372 ms                                                 | 506 ms: 1.36x slower                                               |
| telco                      | 6.53 ms                                                | 8.87 ms: 1.36x slower                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 29.9 ms: 1.37x slower                                              |
| pycparser                  | 1.17 sec                                               | 1.62 sec: 1.38x slower                                             |
| xml_etree_process          | 59.0 ms                                                | 82.3 ms: 1.40x slower                                              |
| json_dumps                 | 10.4 ms                                                | 14.6 ms: 1.41x slower                                              |
| coverage                   | 71.4 ms                                                | 101 ms: 1.41x slower                                               |
| sqlglot_optimize           | 53.3 ms                                                | 75.4 ms: 1.42x slower                                              |
| sqlglot_normalize          | 107 ms                                                 | 152 ms: 1.42x slower                                               |
| pprint_safe_repr           | 743 ms                                                 | 1.06 sec: 1.43x slower                                             |
| 2to3                       | 264 ms                                                 | 377 ms: 1.43x slower                                               |
| python_startup_no_site     | 7.16 ms                                                | 10.3 ms: 1.43x slower                                              |
| pprint_pformat             | 1.52 sec                                               | 2.20 sec: 1.45x slower                                             |
| sqlalchemy_declarative     | 143 ms                                                 | 207 ms: 1.45x slower                                               |
| comprehensions             | 19.8 us                                                | 29.0 us: 1.46x slower                                              |
| genshi_text                | 22.8 ms                                                | 33.9 ms: 1.49x slower                                              |
| nbody                      | 89.3 ms                                                | 133 ms: 1.49x slower                                               |
| sympy_integrate            | 20.5 ms                                                | 30.8 ms: 1.50x slower                                              |
| thrift                     | 791 us                                                 | 1.21 ms: 1.52x slower                                              |
| html5lib                   | 63.6 ms                                                | 99.7 ms: 1.57x slower                                              |
| django_template            | 34.7 ms                                                | 56.0 ms: 1.62x slower                                              |
| pyflate                    | 448 ms                                                 | 728 ms: 1.62x slower                                               |
| logging_simple             | 6.63 us                                                | 11.0 us: 1.65x slower                                              |
| logging_format             | 7.35 us                                                | 12.2 us: 1.66x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.67x slower                                              |
| sympy_str                  | 292 ms                                                 | 494 ms: 1.69x slower                                               |
| scimark_lu                 | 114 ms                                                 | 195 ms: 1.71x slower                                               |
| unpickle_pure_python       | 221 us                                                 | 381 us: 1.73x slower                                               |
| hexiom                     | 6.17 ms                                                | 10.8 ms: 1.75x slower                                              |
| python_startup             | 9.93 ms                                                | 17.5 ms: 1.76x slower                                              |
| chaos                      | 62.8 ms                                                | 111 ms: 1.77x slower                                               |
| float                      | 80.8 ms                                                | 144 ms: 1.78x slower                                               |
| richards                   | 45.9 ms                                                | 82.2 ms: 1.79x slower                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 123 ms: 1.79x slower                                               |
| mako                       | 11.0 ms                                                | 20.1 ms: 1.82x slower                                              |
| logging_silent             | 109 ns                                                 | 200 ns: 1.84x slower                                               |
| sqlglot_transpile          | 1.67 ms                                                | 3.07 ms: 1.84x slower                                              |
| pickle_pure_python         | 308 us                                                 | 567 us: 1.84x slower                                               |
| scimark_sor                | 130 ms                                                 | 245 ms: 1.89x slower                                               |
| richards_super             | 51.9 ms                                                | 98.5 ms: 1.90x slower                                              |
| sqlglot_parse              | 1.36 ms                                                | 2.68 ms: 1.98x slower                                              |
| raytrace                   | 299 ms                                                 | 599 ms: 2.00x slower                                               |
| go                         | 139 ms                                                 | 280 ms: 2.01x slower                                               |
| sympy_expand               | 468 ms                                                 | 982 ms: 2.10x slower                                               |
| sympy_sum                  | 166 ms                                                 | 357 ms: 2.15x slower                                               |
| deltablue                  | 3.45 ms                                                | 8.83 ms: 2.56x slower                                              |
| bench_thread_pool          | 941 us                                                 | 3.39 ms: 3.60x slower                                              |
| bench_mp_pool              | 10.8 ms                                                | 110 ms: 10.15x slower                                              |
| Geometric mean             | (ref)                                                  | 1.39x slower                                                       |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241203-3.14.0a2+-2923163-NOGIL/bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.255x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.23x
- 99% likely to have a slowdown of 1.21x

# Memory
- memory change: 1.33x