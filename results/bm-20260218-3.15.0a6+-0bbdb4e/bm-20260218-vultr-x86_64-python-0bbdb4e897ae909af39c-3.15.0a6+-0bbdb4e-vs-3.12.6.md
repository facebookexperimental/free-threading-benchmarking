# Results vs. 3.12.6

- fork: python
- ref: 0bbdb4e897ae909af39c
- machine: linux-x86_64
- commit hash: 0bbdb4e
- commit date: 2026-02-18
- overall geometric mean: 1.081x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 246 ms: 1.07x faster                                                   |
| docutils       | 2.64 sec                                               | 2.53 sec: 1.05x faster                                                 |
| html5lib       | 63.6 ms                                                | 59.8 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 568 ms: 1.95x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.90x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 573 ms: 1.89x faster                                                   |
| async_tree_none            | 464 ms                                                 | 247 ms: 1.88x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.84x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 485 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 492 ms: 1.47x faster                                                   |
| async_generators           | 384 ms                                                 | 342 ms: 1.12x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.6 ms: 1.16x faster                                                  |
| nbody          | 89.3 ms                                                | 88.2 ms: 1.01x faster                                                  |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                  |
| regex_compile  | 142 ms                                                 | 121 ms: 1.18x faster                                                   |
| regex_dna      | 168 ms                                                 | 165 ms: 1.01x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.3 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 83.8 ms: 1.15x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                 |
| json_dumps           | 10.4 ms                                                | 9.85 ms: 1.05x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 211 us: 1.04x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 83.6 ms: 1.02x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 305 us: 1.01x faster                                                   |
| json_loads           | 26.5 us                                                | 28.3 us: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.26x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.8 ms: 1.09x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 48.7 ms: 1.03x faster                                                  |
| django_template | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                  |
| mako            | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 568 ms: 1.95x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.90x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 573 ms: 1.89x faster                                                   |
| async_tree_none            | 464 ms                                                 | 247 ms: 1.88x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.84x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.3 us: 1.53x faster                                                  |
| deepcopy                   | 352 us                                                 | 231 us: 1.52x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 485 ms: 1.48x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 492 ms: 1.47x faster                                                   |
| go                         | 139 ms                                                 | 107 ms: 1.30x faster                                                   |
| scimark_sor                | 130 ms                                                 | 104 ms: 1.25x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.3 ms: 1.24x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.51 us: 1.23x faster                                                  |
| generators                 | 32.2 ms                                                | 27.0 ms: 1.20x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                  |
| raytrace                   | 299 ms                                                 | 252 ms: 1.19x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 66.8 ms: 1.18x faster                                                  |
| regex_compile              | 142 ms                                                 | 121 ms: 1.18x faster                                                   |
| spectral_norm              | 110 ms                                                 | 94.6 ms: 1.16x faster                                                  |
| float                      | 80.8 ms                                                | 69.6 ms: 1.16x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 83.8 ms: 1.15x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.18 sec: 1.13x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                 |
| chaos                      | 62.8 ms                                                | 55.6 ms: 1.13x faster                                                  |
| scimark_fft                | 342 ms                                                 | 303 ms: 1.13x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 68.0 ms: 1.13x faster                                                  |
| pylint                     | 319 ms                                                 | 283 ms: 1.12x faster                                                   |
| async_generators           | 384 ms                                                 | 342 ms: 1.12x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.92 us: 1.12x faster                                                  |
| logging_format             | 7.35 us                                                | 6.60 us: 1.11x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 61.7 ms: 1.11x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.61 ms: 1.10x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.8 ms: 1.09x faster                                                  |
| logging_silent             | 109 ns                                                 | 100 ns: 1.09x faster                                                   |
| pyflate                    | 448 ms                                                 | 415 ms: 1.08x faster                                                   |
| richards                   | 45.9 ms                                                | 42.6 ms: 1.08x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.08x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.41 sec: 1.08x faster                                                 |
| richards_super             | 51.9 ms                                                | 48.4 ms: 1.07x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                  |
| 2to3                       | 264 ms                                                 | 246 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 696 ms: 1.07x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 107 ms: 1.07x faster                                                   |
| html5lib                   | 63.6 ms                                                | 59.8 ms: 1.06x faster                                                  |
| sympy_str                  | 292 ms                                                 | 275 ms: 1.06x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 158 ms: 1.05x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.85 ms: 1.05x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.53 sec: 1.05x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 211 us: 1.04x faster                                                   |
| meteor_contest             | 104 ms                                                 | 99.6 ms: 1.04x faster                                                  |
| nqueens                    | 80.1 ms                                                | 77.1 ms: 1.04x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.33 ms: 1.04x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.7 ms: 1.03x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 160 us: 1.02x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 83.6 ms: 1.02x faster                                                  |
| regex_dna                  | 168 ms                                                 | 165 ms: 1.01x faster                                                   |
| thrift                     | 791 us                                                 | 780 us: 1.01x faster                                                   |
| nbody                      | 89.3 ms                                                | 88.2 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.34 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 305 us: 1.01x faster                                                   |
| django_template            | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                  |
| json                       | 5.02 ms                                                | 5.14 ms: 1.02x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.33 ms: 1.02x slower                                                  |
| fannkuch                   | 372 ms                                                 | 385 ms: 1.03x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 21.3 ms: 1.04x slower                                                  |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.3 us: 1.07x slower                                                  |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                  |
| coverage                   | 71.4 ms                                                | 82.0 ms: 1.15x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.26x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.47 ms: 1.29x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.31 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.70x slower                                                  |
| telco                      | 6.53 ms                                                | 157 ms: 23.98x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 331 ms: 30.63x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (4): xml_etree_process, sqlite_synth, coroutines, sympy_expand
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260218-3.15.0a6+-0bbdb4e/bm-20260218-vultr-x86_64-python-0bbdb4e897ae909af39c-3.15.0a6+-0bbdb4e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.081x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.17x