# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: jit_ft
- machine: linux-x86_64
- commit hash: 00ae7b5
- commit date: 2025-12-18
- overall geometric mean: 1.003x faster
- HPT reliability: 64.41%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.44x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.07x slower                                               |
| docutils       | 2.64 sec                                               | 2.88 sec: 1.09x slower                                             |
| html5lib       | 63.6 ms                                                | 70.6 ms: 1.11x slower                                              |
| Geometric mean | (ref)                                                  | 1.09x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 615 ms: 1.80x faster                                               |
| async_tree_io              | 1.08 sec                                               | 635 ms: 1.71x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 331 ms: 1.69x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 269 ms: 1.66x faster                                               |
| async_tree_none            | 464 ms                                                 | 291 ms: 1.60x faster                                               |
| async_tree_memoization     | 555 ms                                                 | 357 ms: 1.55x faster                                               |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 526 ms: 1.37x faster                                               |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 548 ms: 1.30x faster                                               |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                               |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                              |
| async_generators           | 384 ms                                                 | 399 ms: 1.04x slower                                               |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 58.6 ms: 1.38x faster                                              |
| nbody          | 89.3 ms                                                | 93.9 ms: 1.05x slower                                              |
| pidigits       | 184 ms                                                 | 199 ms: 1.08x slower                                               |
| Geometric mean | (ref)                                                  | 1.07x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                              |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                               |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.04x slower                                              |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                               |
| Geometric mean | (ref)                                                  | 1.00x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.0 ms: 1.11x faster                                              |
| unpickle_pure_python | 221 us                                                 | 204 us: 1.08x faster                                               |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.05x faster                                               |
| pickle_pure_python   | 308 us                                                 | 314 us: 1.02x slower                                               |
| tomli_loads          | 2.11 sec                                               | 2.17 sec: 1.03x slower                                             |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.04x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 89.8 ms: 1.05x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 63.1 ms: 1.07x slower                                              |
| json_loads           | 26.5 us                                                | 32.8 us: 1.24x slower                                              |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.63 ms: 1.35x slower                                              |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                              |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 40.3 ms: 1.16x slower                                              |
| genshi_text     | 22.8 ms                                                | 27.6 ms: 1.21x slower                                              |
| mako            | 11.0 ms                                                | 14.9 ms: 1.36x slower                                              |
| genshi_xml      | 50.2 ms                                                | 68.8 ms: 1.37x slower                                              |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 20.3 ms: 2.26x faster                                              |
| richards_super             | 51.9 ms                                                | 25.8 ms: 2.01x faster                                              |
| async_tree_io_tg           | 1.11 sec                                               | 615 ms: 1.80x faster                                               |
| gc_traversal               | 3.46 ms                                                | 1.94 ms: 1.78x faster                                              |
| async_tree_io              | 1.08 sec                                               | 635 ms: 1.71x faster                                               |
| async_tree_memoization_tg  | 560 ms                                                 | 331 ms: 1.69x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 269 ms: 1.66x faster                                               |
| async_tree_none            | 464 ms                                                 | 291 ms: 1.60x faster                                               |
| mdp                        | 2.42 sec                                               | 1.55 sec: 1.56x faster                                             |
| async_tree_memoization     | 555 ms                                                 | 357 ms: 1.55x faster                                               |
| bench_mp_pool              | 10.8 ms                                                | 7.15 ms: 1.51x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 28.5 us: 1.41x faster                                              |
| float                      | 80.8 ms                                                | 58.6 ms: 1.38x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 526 ms: 1.37x faster                                               |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                               |
| logging_silent             | 109 ns                                                 | 82.6 ns: 1.32x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 548 ms: 1.30x faster                                               |
| deepcopy                   | 352 us                                                 | 283 us: 1.24x faster                                               |
| pathlib                    | 21.5 ms                                                | 18.3 ms: 1.18x faster                                              |
| bpe_tokeniser              | 4.74 sec                                               | 4.03 sec: 1.18x faster                                             |
| scimark_fft                | 342 ms                                                 | 296 ms: 1.16x faster                                               |
| scimark_sor                | 130 ms                                                 | 114 ms: 1.14x faster                                               |
| deltablue                  | 3.45 ms                                                | 3.05 ms: 1.13x faster                                              |
| xml_etree_iterparse        | 96.7 ms                                                | 87.0 ms: 1.11x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                              |
| pyflate                    | 448 ms                                                 | 408 ms: 1.10x faster                                               |
| spectral_norm              | 110 ms                                                 | 100 ms: 1.10x faster                                               |
| sqlite_synth               | 2.20 us                                                | 2.01 us: 1.10x faster                                              |
| comprehensions             | 19.8 us                                                | 18.2 us: 1.09x faster                                              |
| unpickle_pure_python       | 221 us                                                 | 204 us: 1.08x faster                                               |
| chaos                      | 62.8 ms                                                | 59.5 ms: 1.06x faster                                              |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.05x faster                                               |
| pprint_safe_repr           | 743 ms                                                 | 706 ms: 1.05x faster                                               |
| deepcopy_reduce            | 3.08 us                                                | 2.95 us: 1.04x faster                                              |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.02x faster                                             |
| dulwich_log                | 78.9 ms                                                | 77.3 ms: 1.02x faster                                              |
| pprint_pformat             | 1.52 sec                                               | 1.49 sec: 1.02x faster                                             |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                               |
| generators                 | 32.2 ms                                                | 31.9 ms: 1.01x faster                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 67.9 ms: 1.01x faster                                              |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                               |
| raytrace                   | 299 ms                                                 | 302 ms: 1.01x slower                                               |
| pickle_pure_python         | 308 us                                                 | 314 us: 1.02x slower                                               |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                              |
| tomli_loads                | 2.11 sec                                               | 2.17 sec: 1.03x slower                                             |
| pylint                     | 319 ms                                                 | 329 ms: 1.03x slower                                               |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.04x slower                                              |
| async_generators           | 384 ms                                                 | 399 ms: 1.04x slower                                               |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.04x slower                                              |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                               |
| nbody                      | 89.3 ms                                                | 93.9 ms: 1.05x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 89.8 ms: 1.05x slower                                              |
| logging_simple             | 6.63 us                                                | 7.00 us: 1.06x slower                                              |
| 2to3                       | 264 ms                                                 | 281 ms: 1.07x slower                                               |
| xml_etree_process          | 59.0 ms                                                | 63.1 ms: 1.07x slower                                              |
| json                       | 5.02 ms                                                | 5.39 ms: 1.07x slower                                              |
| pidigits                   | 184 ms                                                 | 199 ms: 1.08x slower                                               |
| logging_format             | 7.35 us                                                | 7.96 us: 1.08x slower                                              |
| hexiom                     | 6.17 ms                                                | 6.72 ms: 1.09x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 83.6 ms: 1.09x slower                                              |
| docutils                   | 2.64 sec                                               | 2.88 sec: 1.09x slower                                             |
| scimark_lu                 | 114 ms                                                 | 125 ms: 1.10x slower                                               |
| thrift                     | 791 us                                                 | 875 us: 1.10x slower                                               |
| html5lib                   | 63.6 ms                                                | 70.6 ms: 1.11x slower                                              |
| sympy_integrate            | 20.5 ms                                                | 23.0 ms: 1.12x slower                                              |
| fannkuch                   | 372 ms                                                 | 417 ms: 1.12x slower                                               |
| meteor_contest             | 104 ms                                                 | 119 ms: 1.15x slower                                               |
| django_template            | 34.7 ms                                                | 40.3 ms: 1.16x slower                                              |
| sympy_sum                  | 166 ms                                                 | 193 ms: 1.16x slower                                               |
| nqueens                    | 80.1 ms                                                | 95.9 ms: 1.20x slower                                              |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                               |
| genshi_text                | 22.8 ms                                                | 27.6 ms: 1.21x slower                                              |
| sympy_str                  | 292 ms                                                 | 354 ms: 1.21x slower                                               |
| sympy_expand               | 468 ms                                                 | 575 ms: 1.23x slower                                               |
| json_loads                 | 26.5 us                                                | 32.8 us: 1.24x slower                                              |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.44 ms: 1.24x slower                                              |
| python_startup_no_site     | 7.16 ms                                                | 9.63 ms: 1.35x slower                                              |
| mako                       | 11.0 ms                                                | 14.9 ms: 1.36x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.49 ms: 1.36x slower                                              |
| genshi_xml                 | 50.2 ms                                                | 68.8 ms: 1.37x slower                                              |
| bench_thread_pool          | 941 us                                                 | 1.48 ms: 1.58x slower                                              |
| coverage                   | 71.4 ms                                                | 113 ms: 1.59x slower                                               |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                              |
| telco                      | 6.53 ms                                                | 179 ms: 27.44x slower                                              |
| Geometric mean             | (ref)                                                  | 1.00x faster                                                       |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251218-3.15.0a3+-00ae7b5-JIT,NOGIL/bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 64.41% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.44x