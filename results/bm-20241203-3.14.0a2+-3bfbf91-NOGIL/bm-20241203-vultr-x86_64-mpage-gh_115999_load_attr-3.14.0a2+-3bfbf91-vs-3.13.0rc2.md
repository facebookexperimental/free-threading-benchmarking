# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr
- machine: linux-x86_64
- commit hash: 3bfbf91
- commit date: 2024-12-03
- overall geometric mean: 1.244x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 365 ms: 1.40x slower                                                 |
| docutils       | 2.62 sec                                                     | 3.08 sec: 1.18x slower                                               |
| html5lib       | 67.0 ms                                                      | 97.5 ms: 1.46x slower                                                |
| Geometric mean | (ref)                                                        | 1.34x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 800 ms: 1.14x faster                                                 |
| async_tree_io              | 876 ms                                                       | 821 ms: 1.07x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 626 ms: 1.06x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 604 ms: 1.06x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 352 ms: 1.05x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.8 ms: 1.05x slower                                                |
| async_tree_memoization_tg  | 414 ms                                                       | 438 ms: 1.06x slower                                                 |
| async_tree_none            | 354 ms                                                       | 378 ms: 1.07x slower                                                 |
| async_generators           | 377 ms                                                       | 455 ms: 1.21x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                         |

Benchmark hidden because not significant (2): async_tree_memoization, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                 |
| nbody          | 85.1 ms                                                      | 130 ms: 1.52x slower                                                 |
| float          | 77.5 ms                                                      | 139 ms: 1.80x slower                                                 |
| Geometric mean | (ref)                                                        | 1.32x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.86 ms: 1.08x faster                                                |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                 |
| regex_v8       | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                |
| regex_compile  | 132 ms                                                       | 180 ms: 1.36x slower                                                 |
| Geometric mean | (ref)                                                        | 1.09x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.1 ms: 1.03x faster                                                |
| json_loads           | 27.0 us                                                      | 28.5 us: 1.05x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 97.7 ms: 1.14x slower                                                |
| xml_etree_process    | 59.3 ms                                                      | 78.4 ms: 1.32x slower                                                |
| json_dumps           | 10.5 ms                                                      | 13.9 ms: 1.32x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 2.68 sec: 1.33x slower                                               |
| unpickle_pure_python | 210 us                                                       | 333 us: 1.58x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 511 us: 1.73x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.39x slower                                                |
| python_startup         | 11.0 ms                                                      | 17.2 ms: 1.56x slower                                                |
| Geometric mean         | (ref)                                                        | 1.47x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.0 ms: 1.29x slower                                                |
| genshi_text     | 21.5 ms                                                      | 30.4 ms: 1.41x slower                                                |
| django_template | 34.1 ms                                                      | 50.6 ms: 1.48x slower                                                |
| mako            | 11.3 ms                                                      | 17.1 ms: 1.51x slower                                                |
| Geometric mean  | (ref)                                                        | 1.42x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 800 ms: 1.14x faster                                                 |
| deepcopy                   | 355 us                                                       | 325 us: 1.09x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.86 ms: 1.08x faster                                                |
| async_tree_io              | 876 ms                                                       | 821 ms: 1.07x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 626 ms: 1.06x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 604 ms: 1.06x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.1 ms: 1.03x faster                                                |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.02x slower                                                 |
| deepcopy_memo              | 39.1 us                                                      | 39.9 us: 1.02x slower                                                |
| json                       | 4.93 ms                                                      | 5.07 ms: 1.03x slower                                                |
| pathlib                    | 19.2 ms                                                      | 19.9 ms: 1.04x slower                                                |
| gc_traversal               | 3.14 ms                                                      | 3.28 ms: 1.04x slower                                                |
| async_tree_none_tg         | 336 ms                                                       | 352 ms: 1.05x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.8 ms: 1.05x slower                                                |
| json_loads                 | 27.0 us                                                      | 28.5 us: 1.05x slower                                                |
| async_tree_memoization_tg  | 414 ms                                                       | 438 ms: 1.06x slower                                                 |
| spectral_norm              | 111 ms                                                       | 118 ms: 1.06x slower                                                 |
| async_tree_none            | 354 ms                                                       | 378 ms: 1.07x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                |
| deepcopy_reduce            | 3.11 us                                                      | 3.47 us: 1.12x slower                                                |
| telco                      | 7.82 ms                                                      | 8.78 ms: 1.12x slower                                                |
| bpe_tokeniser              | 4.45 sec                                                     | 5.01 sec: 1.13x slower                                               |
| xml_etree_generate         | 85.4 ms                                                      | 97.7 ms: 1.14x slower                                                |
| scimark_fft                | 349 ms                                                       | 400 ms: 1.15x slower                                                 |
| pylint                     | 317 ms                                                       | 372 ms: 1.17x slower                                                 |
| docutils                   | 2.62 sec                                                     | 3.08 sec: 1.18x slower                                               |
| async_generators           | 377 ms                                                       | 455 ms: 1.21x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.86 sec: 1.21x slower                                               |
| nqueens                    | 78.6 ms                                                      | 96.0 ms: 1.22x slower                                                |
| dulwich_log                | 74.8 ms                                                      | 94.6 ms: 1.26x slower                                                |
| coverage                   | 83.0 ms                                                      | 106 ms: 1.27x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 67.4 ms: 1.28x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 6.08 ms: 1.29x slower                                                |
| genshi_xml                 | 48.8 ms                                                      | 63.0 ms: 1.29x slower                                                |
| sqlglot_normalize          | 106 ms                                                       | 137 ms: 1.29x slower                                                 |
| meteor_contest             | 102 ms                                                       | 133 ms: 1.31x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 963 ms: 1.31x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 78.4 ms: 1.32x slower                                                |
| json_dumps                 | 10.5 ms                                                      | 13.9 ms: 1.32x slower                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.99 sec: 1.33x slower                                               |
| typing_runtime_protocols   | 155 us                                                       | 206 us: 1.33x slower                                                 |
| fannkuch                   | 370 ms                                                       | 492 ms: 1.33x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.68 sec: 1.33x slower                                               |
| crypto_pyaes               | 67.9 ms                                                      | 90.6 ms: 1.33x slower                                                |
| generators                 | 28.8 ms                                                      | 39.0 ms: 1.35x slower                                                |
| create_gc_cycles           | 1.34 ms                                                      | 1.81 ms: 1.35x slower                                                |
| regex_compile              | 132 ms                                                       | 180 ms: 1.36x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.52 sec: 1.36x slower                                               |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.39x slower                                                |
| 2to3                       | 260 ms                                                       | 365 ms: 1.40x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 30.4 ms: 1.41x slower                                                |
| thrift                     | 778 us                                                       | 1.11 ms: 1.42x slower                                                |
| html5lib                   | 67.0 ms                                                      | 97.5 ms: 1.46x slower                                                |
| django_template            | 34.1 ms                                                      | 50.6 ms: 1.48x slower                                                |
| sympy_integrate            | 19.8 ms                                                      | 29.6 ms: 1.49x slower                                                |
| mako                       | 11.3 ms                                                      | 17.1 ms: 1.51x slower                                                |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.52x slower                                                 |
| pyflate                    | 449 ms                                                       | 694 ms: 1.55x slower                                                 |
| python_startup             | 11.0 ms                                                      | 17.2 ms: 1.56x slower                                                |
| unpickle_pure_python       | 210 us                                                       | 333 us: 1.58x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 184 ms: 1.64x slower                                                 |
| logging_simple             | 6.16 us                                                      | 10.1 us: 1.64x slower                                                |
| logging_format             | 6.84 us                                                      | 11.3 us: 1.65x slower                                                |
| hexiom                     | 5.99 ms                                                      | 9.90 ms: 1.65x slower                                                |
| richards_super             | 51.6 ms                                                      | 86.8 ms: 1.68x slower                                                |
| comprehensions             | 16.5 us                                                      | 27.7 us: 1.68x slower                                                |
| richards                   | 45.2 ms                                                      | 77.6 ms: 1.72x slower                                                |
| pickle_pure_python         | 294 us                                                       | 511 us: 1.73x slower                                                 |
| sympy_str                  | 275 ms                                                       | 477 ms: 1.74x slower                                                 |
| scimark_sor                | 134 ms                                                       | 235 ms: 1.75x slower                                                 |
| float                      | 77.5 ms                                                      | 139 ms: 1.80x slower                                                 |
| chaos                      | 57.3 ms                                                      | 104 ms: 1.81x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 119 ms: 1.82x slower                                                 |
| logging_silent             | 103 ns                                                       | 188 ns: 1.83x slower                                                 |
| go                         | 141 ms                                                       | 269 ms: 1.91x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 2.98 ms: 1.91x slower                                                |
| sqlglot_parse              | 1.25 ms                                                      | 2.58 ms: 2.07x slower                                                |
| sympy_expand               | 457 ms                                                       | 961 ms: 2.10x slower                                                 |
| raytrace                   | 253 ms                                                       | 556 ms: 2.20x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 352 ms: 2.26x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 8.13 ms: 2.60x slower                                                |
| bench_thread_pool          | 919 us                                                       | 3.34 ms: 3.63x slower                                                |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.81x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.37x slower                                                         |

Benchmark hidden because not significant (3): async_tree_memoization, asyncio_websockets, sqlite_synth
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241203-3.14.0a2+-3bfbf91-NOGIL/bm-20241203-vultr-x86_64-mpage-gh_115999_load_attr-3.14.0a2+-3bfbf91.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.244x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.24x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.32x