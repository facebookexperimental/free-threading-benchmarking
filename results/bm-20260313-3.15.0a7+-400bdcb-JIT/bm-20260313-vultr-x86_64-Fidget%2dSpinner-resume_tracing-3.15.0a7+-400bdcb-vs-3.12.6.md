# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 400bdcb
- commit date: 2026-03-13
- overall geometric mean: 1.137x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                       |
| docutils       | 2.64 sec                                               | 2.65 sec: 1.01x slower                                                     |
| html5lib       | 63.6 ms                                                | 61.2 ms: 1.04x faster                                                      |
| Geometric mean | (ref)                                                  | 1.03x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 550 ms: 2.02x faster                                                       |
| async_tree_none            | 464 ms                                                 | 232 ms: 2.00x faster                                                       |
| async_tree_memoization     | 555 ms                                                 | 287 ms: 1.94x faster                                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 292 ms: 1.92x faster                                                       |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.92x faster                                                       |
| async_tree_io              | 1.08 sec                                               | 567 ms: 1.91x faster                                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 495 ms: 1.45x faster                                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                       |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                      |
| async_generators           | 384 ms                                                 | 355 ms: 1.08x faster                                                       |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 59.0 ms: 1.37x faster                                                      |
| nbody          | 89.3 ms                                                | 74.2 ms: 1.20x faster                                                      |
| pidigits       | 184 ms                                                 | 219 ms: 1.19x slower                                                       |
| Geometric mean | (ref)                                                  | 1.11x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                       |
| regex_effbot   | 3.17 ms                                                | 2.81 ms: 1.13x faster                                                      |
| regex_dna      | 168 ms                                                 | 179 ms: 1.07x slower                                                       |
| regex_v8       | 20.6 ms                                                | 23.2 ms: 1.13x slower                                                      |
| Geometric mean | (ref)                                                  | 1.02x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.53 sec: 1.37x faster                                                     |
| json_dumps           | 10.4 ms                                                | 8.97 ms: 1.16x faster                                                      |
| xml_etree_iterparse  | 96.7 ms                                                | 84.0 ms: 1.15x faster                                                      |
| xml_etree_process    | 59.0 ms                                                | 53.1 ms: 1.11x faster                                                      |
| unpickle_pure_python | 221 us                                                 | 199 us: 1.11x faster                                                       |
| xml_etree_generate   | 85.2 ms                                                | 79.2 ms: 1.08x faster                                                      |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                       |
| pickle_pure_python   | 308 us                                                 | 313 us: 1.02x slower                                                       |
| json_loads           | 26.5 us                                                | 27.1 us: 1.02x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                      |
| python_startup         | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.16x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.3 ms: 1.13x faster                                                      |
| mako            | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                      |
| django_template | 34.7 ms                                                | 33.9 ms: 1.02x faster                                                      |
| genshi_xml      | 50.2 ms                                                | 51.7 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 18.7 ms: 2.46x faster                                                      |
| richards_super             | 51.9 ms                                                | 22.2 ms: 2.33x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 550 ms: 2.02x faster                                                       |
| mdp                        | 2.42 sec                                               | 1.20 sec: 2.01x faster                                                     |
| async_tree_none            | 464 ms                                                 | 232 ms: 2.00x faster                                                       |
| async_tree_memoization     | 555 ms                                                 | 287 ms: 1.94x faster                                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 292 ms: 1.92x faster                                                       |
| async_tree_none_tg         | 446 ms                                                 | 233 ms: 1.92x faster                                                       |
| async_tree_io              | 1.08 sec                                               | 567 ms: 1.91x faster                                                       |
| deepcopy_memo              | 40.3 us                                                | 22.7 us: 1.77x faster                                                      |
| scimark_sor                | 130 ms                                                 | 82.8 ms: 1.57x faster                                                      |
| deepcopy                   | 352 us                                                 | 225 us: 1.56x faster                                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 495 ms: 1.45x faster                                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                       |
| scimark_lu                 | 114 ms                                                 | 80.0 ms: 1.43x faster                                                      |
| spectral_norm              | 110 ms                                                 | 78.5 ms: 1.40x faster                                                      |
| go                         | 139 ms                                                 | 101 ms: 1.38x faster                                                       |
| logging_silent             | 109 ns                                                 | 79.2 ns: 1.38x faster                                                      |
| tomli_loads                | 2.11 sec                                               | 1.53 sec: 1.37x faster                                                     |
| float                      | 80.8 ms                                                | 59.0 ms: 1.37x faster                                                      |
| scimark_fft                | 342 ms                                                 | 256 ms: 1.34x faster                                                       |
| scimark_monte_carlo        | 68.4 ms                                                | 51.7 ms: 1.32x faster                                                      |
| deltablue                  | 3.45 ms                                                | 2.67 ms: 1.29x faster                                                      |
| deepcopy_reduce            | 3.08 us                                                | 2.46 us: 1.25x faster                                                      |
| pyflate                    | 448 ms                                                 | 359 ms: 1.25x faster                                                       |
| logging_simple             | 6.63 us                                                | 5.36 us: 1.24x faster                                                      |
| pathlib                    | 21.5 ms                                                | 17.4 ms: 1.24x faster                                                      |
| logging_format             | 7.35 us                                                | 6.05 us: 1.21x faster                                                      |
| bpe_tokeniser              | 4.74 sec                                               | 3.93 sec: 1.20x faster                                                     |
| nbody                      | 89.3 ms                                                | 74.2 ms: 1.20x faster                                                      |
| chaos                      | 62.8 ms                                                | 52.2 ms: 1.20x faster                                                      |
| pprint_safe_repr           | 743 ms                                                 | 628 ms: 1.18x faster                                                       |
| pprint_pformat             | 1.52 sec                                               | 1.30 sec: 1.17x faster                                                     |
| crypto_pyaes               | 76.6 ms                                                | 66.0 ms: 1.16x faster                                                      |
| json_dumps                 | 10.4 ms                                                | 8.97 ms: 1.16x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 84.0 ms: 1.15x faster                                                      |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                       |
| regex_effbot               | 3.17 ms                                                | 2.81 ms: 1.13x faster                                                      |
| genshi_text                | 22.8 ms                                                | 20.3 ms: 1.13x faster                                                      |
| dulwich_log                | 78.9 ms                                                | 70.1 ms: 1.12x faster                                                      |
| comprehensions             | 19.8 us                                                | 17.8 us: 1.11x faster                                                      |
| xml_etree_process          | 59.0 ms                                                | 53.1 ms: 1.11x faster                                                      |
| unpickle_pure_python       | 221 us                                                 | 199 us: 1.11x faster                                                       |
| nqueens                    | 80.1 ms                                                | 72.5 ms: 1.10x faster                                                      |
| fannkuch                   | 372 ms                                                 | 338 ms: 1.10x faster                                                       |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                      |
| typing_runtime_protocols   | 163 us                                                 | 150 us: 1.09x faster                                                       |
| async_generators           | 384 ms                                                 | 355 ms: 1.08x faster                                                       |
| xml_etree_generate         | 85.2 ms                                                | 79.2 ms: 1.08x faster                                                      |
| hexiom                     | 6.17 ms                                                | 5.75 ms: 1.07x faster                                                      |
| meteor_contest             | 104 ms                                                 | 97.5 ms: 1.06x faster                                                      |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                       |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                       |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.18 ms: 1.05x faster                                                      |
| mako                       | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                      |
| html5lib                   | 63.6 ms                                                | 61.2 ms: 1.04x faster                                                      |
| json                       | 5.02 ms                                                | 4.85 ms: 1.04x faster                                                      |
| pylint                     | 319 ms                                                 | 308 ms: 1.03x faster                                                       |
| django_template            | 34.7 ms                                                | 33.9 ms: 1.02x faster                                                      |
| sqlite_synth               | 2.20 us                                                | 2.15 us: 1.02x faster                                                      |
| raytrace                   | 299 ms                                                 | 293 ms: 1.02x faster                                                       |
| docutils                   | 2.64 sec                                               | 2.65 sec: 1.01x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 313 us: 1.02x slower                                                       |
| json_loads                 | 26.5 us                                                | 27.1 us: 1.02x slower                                                      |
| genshi_xml                 | 50.2 ms                                                | 51.7 ms: 1.03x slower                                                      |
| sympy_str                  | 292 ms                                                 | 304 ms: 1.04x slower                                                       |
| sympy_expand               | 468 ms                                                 | 489 ms: 1.05x slower                                                       |
| python_startup_no_site     | 7.16 ms                                                | 7.51 ms: 1.05x slower                                                      |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                       |
| sympy_sum                  | 166 ms                                                 | 175 ms: 1.06x slower                                                       |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.07x slower                                                       |
| generators                 | 32.2 ms                                                | 34.6 ms: 1.07x slower                                                      |
| regex_v8                   | 20.6 ms                                                | 23.2 ms: 1.13x slower                                                      |
| coverage                   | 71.4 ms                                                | 82.4 ms: 1.15x slower                                                      |
| pidigits                   | 184 ms                                                 | 219 ms: 1.19x slower                                                       |
| gc_traversal               | 3.46 ms                                                | 4.32 ms: 1.25x slower                                                      |
| python_startup             | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                      |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.40x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.69x slower                                                      |
| bench_mp_pool              | 10.8 ms                                                | 182 ms: 16.86x slower                                                      |
| telco                      | 6.53 ms                                                | 155 ms: 23.71x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                               |

Benchmark hidden because not significant (3): pycparser, sympy_integrate, thrift
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260313-3.15.0a7+-400bdcb-JIT/bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.137x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.20x