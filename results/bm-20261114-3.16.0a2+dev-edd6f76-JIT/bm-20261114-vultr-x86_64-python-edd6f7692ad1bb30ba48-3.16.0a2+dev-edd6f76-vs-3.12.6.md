# Results vs. 3.12.6

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: linux-x86_64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.209x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                      |
| docutils       | 2.64 sec                                               | 2.39 sec: 1.10x faster                                                    |
| html5lib       | 63.6 ms                                                | 57.1 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                  | 1.09x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 255 ms: 1.82x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 620 ms: 1.75x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 324 ms: 1.71x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 652 ms: 1.70x faster                                                      |
| async_generators           | 384 ms                                                 | 242 ms: 1.59x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                      |
| asyncio_tcp                | 519 ms                                                 | 441 ms: 1.18x faster                                                      |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                     |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.47 sec: 1.03x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                | 59.6 ms: 1.50x faster                                                     |
| float          | 80.8 ms                                                | 54.6 ms: 1.48x faster                                                     |
| pidigits       | 184 ms                                                 | 177 ms: 1.04x faster                                                      |
| Geometric mean | (ref)                                                  | 1.32x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.56 ms: 1.24x faster                                                     |
| regex_dna      | 168 ms                                                 | 159 ms: 1.05x faster                                                      |
| regex_v8       | 20.6 ms                                                | 19.8 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                  | 1.08x faster                                                              |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.48 sec: 1.42x faster                                                    |
| unpickle_pure_python | 221 us                                                 | 171 us: 1.29x faster                                                      |
| json_dumps           | 10.4 ms                                                | 8.42 ms: 1.23x faster                                                     |
| pickle_pure_python   | 308 us                                                 | 271 us: 1.14x faster                                                      |
| xml_etree_iterparse  | 96.7 ms                                                | 89.8 ms: 1.08x faster                                                     |
| xml_etree_process    | 59.0 ms                                                | 55.8 ms: 1.06x faster                                                     |
| xml_etree_generate   | 85.2 ms                                                | 80.8 ms: 1.05x faster                                                     |
| json_loads           | 26.5 us                                                | 25.5 us: 1.04x faster                                                     |
| unpickle             | 14.1 us                                                | 14.3 us: 1.02x slower                                                     |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| unpickle_list        | 4.67 us                                                | 4.98 us: 1.07x slower                                                     |
| pickle_dict          | 31.8 us                                                | 35.0 us: 1.10x slower                                                     |
| pickle               | 10.9 us                                                | 12.7 us: 1.16x slower                                                     |
| pickle_list          | 4.77 us                                                | 5.71 us: 1.20x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.44 ms: 1.04x slower                                                     |
| python_startup         | 9.93 ms                                                | 11.1 ms: 1.12x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                | 9.90 ms: 1.11x faster                                                     |
| django_template | 34.7 ms                                                | 32.2 ms: 1.08x faster                                                     |
| Geometric mean  | (ref)                                                  | 1.09x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 107 ms: 2.99x faster                                                      |
| richards_super             | 51.9 ms                                                | 20.6 ms: 2.52x faster                                                     |
| richards                   | 45.9 ms                                                | 19.2 ms: 2.39x faster                                                     |
| mdp                        | 2.42 sec                                               | 1.16 sec: 2.09x faster                                                    |
| async_tree_none            | 464 ms                                                 | 255 ms: 1.82x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 620 ms: 1.75x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 324 ms: 1.71x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 652 ms: 1.70x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 23.8 us: 1.69x faster                                                     |
| scimark_sor                | 130 ms                                                 | 78.2 ms: 1.66x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 99.2 us: 1.65x faster                                                     |
| deepcopy                   | 352 us                                                 | 219 us: 1.60x faster                                                      |
| spectral_norm              | 110 ms                                                 | 68.7 ms: 1.60x faster                                                     |
| async_generators           | 384 ms                                                 | 242 ms: 1.59x faster                                                      |
| nbody                      | 89.3 ms                                                | 59.6 ms: 1.50x faster                                                     |
| float                      | 80.8 ms                                                | 54.6 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 499 ms: 1.45x faster                                                      |
| tomli_loads                | 2.11 sec                                               | 1.48 sec: 1.42x faster                                                    |
| comprehensions             | 19.8 us                                                | 13.9 us: 1.42x faster                                                     |
| go                         | 139 ms                                                 | 99.8 ms: 1.40x faster                                                     |
| logging_silent             | 109 ns                                                 | 78.4 ns: 1.39x faster                                                     |
| scimark_fft                | 342 ms                                                 | 254 ms: 1.34x faster                                                      |
| scimark_lu                 | 114 ms                                                 | 85.3 ms: 1.34x faster                                                     |
| chaos                      | 62.8 ms                                                | 47.7 ms: 1.32x faster                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 52.0 ms: 1.32x faster                                                     |
| deltablue                  | 3.45 ms                                                | 2.65 ms: 1.30x faster                                                     |
| unpickle_pure_python       | 221 us                                                 | 171 us: 1.29x faster                                                      |
| deepcopy_reduce            | 3.08 us                                                | 2.41 us: 1.28x faster                                                     |
| pyflate                    | 448 ms                                                 | 351 ms: 1.28x faster                                                      |
| pathlib                    | 21.5 ms                                                | 17.1 ms: 1.26x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.56 ms: 1.24x faster                                                     |
| nqueens                    | 80.1 ms                                                | 64.9 ms: 1.23x faster                                                     |
| logging_format             | 7.35 us                                                | 5.95 us: 1.23x faster                                                     |
| logging_simple             | 6.63 us                                                | 5.38 us: 1.23x faster                                                     |
| json_dumps                 | 10.4 ms                                                | 8.42 ms: 1.23x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 3.85 sec: 1.23x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 607 ms: 1.22x faster                                                      |
| crypto_pyaes               | 76.6 ms                                                | 62.7 ms: 1.22x faster                                                     |
| raytrace                   | 299 ms                                                 | 248 ms: 1.20x faster                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.27 sec: 1.20x faster                                                    |
| asyncio_tcp                | 519 ms                                                 | 441 ms: 1.18x faster                                                      |
| dulwich_log                | 78.9 ms                                                | 68.5 ms: 1.15x faster                                                     |
| pickle_pure_python         | 308 us                                                 | 271 us: 1.14x faster                                                      |
| fannkuch                   | 372 ms                                                 | 330 ms: 1.13x faster                                                      |
| html5lib                   | 63.6 ms                                                | 57.1 ms: 1.11x faster                                                     |
| mako                       | 11.0 ms                                                | 9.90 ms: 1.11x faster                                                     |
| docutils                   | 2.64 sec                                               | 2.39 sec: 1.10x faster                                                    |
| generators                 | 32.2 ms                                                | 29.4 ms: 1.10x faster                                                     |
| hexiom                     | 6.17 ms                                                | 5.66 ms: 1.09x faster                                                     |
| json                       | 5.02 ms                                                | 4.63 ms: 1.09x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 89.8 ms: 1.08x faster                                                     |
| django_template            | 34.7 ms                                                | 32.2 ms: 1.08x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.6 ms: 1.06x faster                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.14 ms: 1.06x faster                                                     |
| xml_etree_process          | 59.0 ms                                                | 55.8 ms: 1.06x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.08 us: 1.06x faster                                                     |
| xml_etree_generate         | 85.2 ms                                                | 80.8 ms: 1.05x faster                                                     |
| regex_dna                  | 168 ms                                                 | 159 ms: 1.05x faster                                                      |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                      |
| meteor_contest             | 104 ms                                                 | 99.2 ms: 1.04x faster                                                     |
| json_loads                 | 26.5 us                                                | 25.5 us: 1.04x faster                                                     |
| regex_v8                   | 20.6 ms                                                | 19.8 ms: 1.04x faster                                                     |
| pidigits                   | 184 ms                                                 | 177 ms: 1.04x faster                                                      |
| sympy_integrate            | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                     |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.47 sec: 1.03x faster                                                    |
| thrift                     | 791 us                                                 | 774 us: 1.02x faster                                                      |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.02x faster                                                    |
| sympy_sum                  | 166 ms                                                 | 168 ms: 1.01x slower                                                      |
| unpickle                   | 14.1 us                                                | 14.3 us: 1.02x slower                                                     |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 7.44 ms: 1.04x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 3.62 ms: 1.05x slower                                                     |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                      |
| unpickle_list              | 4.67 us                                                | 4.98 us: 1.07x slower                                                     |
| pickle_dict                | 31.8 us                                                | 35.0 us: 1.10x slower                                                     |
| python_startup             | 9.93 ms                                                | 11.1 ms: 1.12x slower                                                     |
| pickle                     | 10.9 us                                                | 12.7 us: 1.16x slower                                                     |
| coverage                   | 71.4 ms                                                | 84.0 ms: 1.18x slower                                                     |
| pickle_list                | 4.77 us                                                | 5.71 us: 1.20x slower                                                     |
| unpack_sequence            | 52.1 ns                                                | 63.9 ns: 1.23x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.40 ms: 1.28x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.31 ms: 1.39x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 183 ms: 16.92x slower                                                     |
| telco                      | 6.53 ms                                                | 134 ms: 20.57x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.14x faster                                                              |

Benchmark hidden because not significant (3): sympy_expand, regex_compile, sympy_str
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20261114-3.16.0a2+dev-edd6f76-JIT/bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.209x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.14x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.20x