# Results vs. 3.12.6

- fork: nascheme
- ref: ft_gc_threshold_fix_
- machine: linux-x86_64
- commit hash: 819a848
- commit date: 2026-04-30
- overall geometric mean: 1.021x slower
- HPT reliability: 61.84%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 289 ms: 1.10x slower                                                     |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                   |
| html5lib       | 63.6 ms                                                | 69.1 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                  | 1.08x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 636 ms: 1.75x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 673 ms: 1.61x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 285 ms: 1.57x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 359 ms: 1.56x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 379 ms: 1.47x faster                                                     |
| async_tree_none            | 464 ms                                                 | 323 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 550 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 566 ms: 1.26x faster                                                     |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 508 ms: 1.02x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.6 ms: 1.03x faster                                                    |
| pidigits       | 184 ms                                                 | 180 ms: 1.02x faster                                                     |
| nbody          | 89.3 ms                                                | 123 ms: 1.38x slower                                                     |
| Geometric mean | (ref)                                                  | 1.09x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.05 ms: 1.04x faster                                                    |
| regex_compile  | 142 ms                                                 | 143 ms: 1.00x slower                                                     |
| regex_v8       | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                    |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                     |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.8 ms: 1.09x faster                                                    |
| tomli_loads          | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.04x faster                                                     |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 236 us: 1.07x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 336 us: 1.09x slower                                                     |
| json_loads           | 26.5 us                                                | 29.2 us: 1.10x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 96.0 ms: 1.13x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 68.5 ms: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.78 ms: 1.23x slower                                                    |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.37x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.9 ms: 1.15x slower                                                    |
| mako            | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 131 ms: 2.43x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 1.88 ms: 1.84x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.83x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 636 ms: 1.75x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 673 ms: 1.61x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 285 ms: 1.57x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 359 ms: 1.56x faster                                                     |
| bench_mp_pool              | 10.8 ms                                                | 7.05 ms: 1.53x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 379 ms: 1.47x faster                                                     |
| async_tree_none            | 464 ms                                                 | 323 ms: 1.44x faster                                                     |
| deepcopy                   | 352 us                                                 | 266 us: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 550 ms: 1.31x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 31.0 us: 1.30x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 566 ms: 1.26x faster                                                     |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.22x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 1.92 us: 1.15x faster                                                    |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                     |
| comprehensions             | 19.8 us                                                | 17.5 us: 1.14x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 71.5 ms: 1.10x faster                                                    |
| scimark_sor                | 130 ms                                                 | 119 ms: 1.09x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.35 sec: 1.09x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 88.8 ms: 1.09x faster                                                    |
| tomli_loads                | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.89 us: 1.07x faster                                                    |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                                     |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 134 ms: 1.04x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 3.05 ms: 1.04x faster                                                    |
| float                      | 80.8 ms                                                | 78.6 ms: 1.03x faster                                                    |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                                     |
| pidigits                   | 184 ms                                                 | 180 ms: 1.02x faster                                                     |
| scimark_fft                | 342 ms                                                 | 335 ms: 1.02x faster                                                     |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 508 ms: 1.02x faster                                                     |
| chaos                      | 62.8 ms                                                | 62.3 ms: 1.01x faster                                                    |
| regex_compile              | 142 ms                                                 | 143 ms: 1.00x slower                                                     |
| raytrace                   | 299 ms                                                 | 302 ms: 1.01x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                    |
| logging_simple             | 6.63 us                                                | 6.93 us: 1.05x slower                                                    |
| generators                 | 32.2 ms                                                | 34.1 ms: 1.06x slower                                                    |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                   |
| deltablue                  | 3.45 ms                                                | 3.67 ms: 1.06x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 791 ms: 1.06x slower                                                     |
| logging_format             | 7.35 us                                                | 7.82 us: 1.06x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 22.0 ms: 1.07x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 236 us: 1.07x slower                                                     |
| hexiom                     | 6.17 ms                                                | 6.62 ms: 1.07x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.63 sec: 1.07x slower                                                   |
| sympy_str                  | 292 ms                                                 | 315 ms: 1.08x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.08x slower                                                     |
| html5lib                   | 63.6 ms                                                | 69.1 ms: 1.09x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 336 us: 1.09x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 125 ms: 1.09x slower                                                     |
| 2to3                       | 264 ms                                                 | 289 ms: 1.10x slower                                                     |
| nqueens                    | 80.1 ms                                                | 88.1 ms: 1.10x slower                                                    |
| json_loads                 | 26.5 us                                                | 29.2 us: 1.10x slower                                                    |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                                     |
| sympy_expand               | 468 ms                                                 | 527 ms: 1.13x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 96.0 ms: 1.13x slower                                                    |
| richards                   | 45.9 ms                                                | 52.5 ms: 1.14x slower                                                    |
| thrift                     | 791 us                                                 | 909 us: 1.15x slower                                                     |
| django_template            | 34.7 ms                                                | 39.9 ms: 1.15x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 88.2 ms: 1.15x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 79.0 ms: 1.15x slower                                                    |
| richards_super             | 51.9 ms                                                | 60.2 ms: 1.16x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 68.5 ms: 1.16x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.21 ms: 1.19x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 194 us: 1.19x slower                                                     |
| fannkuch                   | 372 ms                                                 | 451 ms: 1.21x slower                                                     |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.21x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 8.78 ms: 1.23x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.44 ms: 1.32x slower                                                    |
| nbody                      | 89.3 ms                                                | 123 ms: 1.38x slower                                                     |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.42x slower                                                    |
| coverage                   | 71.4 ms                                                | 110 ms: 1.53x slower                                                     |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.46 ms: 1.55x slower                                                    |
| telco                      | 6.53 ms                                                | 176 ms: 26.98x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (3): coroutines, pyflate, json
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260430-3.15.0a8+-819a848-NOGIL/bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-819a848.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.021x slower

# HPT report

- Reliability score: 61.84% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x