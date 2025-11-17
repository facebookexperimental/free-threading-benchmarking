# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: jit_Ft_llvm_19
- machine: linux-x86_64
- commit hash: 763ebea
- commit date: 2025-11-16
- overall geometric mean: 1.004x faster
- HPT reliability: 60.51%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 286 ms: 1.09x slower                                                       |
| html5lib       | 63.6 ms                                                | 73.8 ms: 1.16x slower                                                      |
| Geometric mean | (ref)                                                  | 1.12x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 530 ms: 2.09x faster                                                       |
| async_tree_io              | 1.08 sec                                               | 549 ms: 1.97x faster                                                       |
| async_tree_none_tg         | 446 ms                                                 | 231 ms: 1.93x faster                                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 291 ms: 1.93x faster                                                       |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                       |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 481 ms: 1.50x faster                                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                       |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.01x faster                                                       |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.59x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 55.4 ms: 1.46x faster                                                      |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                       |
| nbody          | 89.3 ms                                                | 101 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                  | 1.07x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                      |
| regex_v8       | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                      |
| regex_compile  | 142 ms                                                 | 148 ms: 1.04x slower                                                       |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                  | 1.00x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 85.8 ms: 1.13x faster                                                      |
| unpickle_pure_python | 221 us                                                 | 201 us: 1.10x faster                                                       |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                       |
| tomli_loads          | 2.11 sec                                               | 2.02 sec: 1.04x faster                                                     |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                      |
| xml_etree_generate   | 85.2 ms                                                | 89.8 ms: 1.05x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 324 us: 1.05x slower                                                       |
| xml_etree_process    | 59.0 ms                                                | 63.4 ms: 1.07x slower                                                      |
| json_loads           | 26.5 us                                                | 31.2 us: 1.18x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.50 ms: 1.33x slower                                                      |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 42.1 ms: 1.21x slower                                                      |
| genshi_text     | 22.8 ms                                                | 28.5 ms: 1.25x slower                                                      |
| mako            | 11.0 ms                                                | 14.3 ms: 1.30x slower                                                      |
| genshi_xml      | 50.2 ms                                                | 71.8 ms: 1.43x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.30x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 530 ms: 2.09x faster                                                       |
| async_tree_io              | 1.08 sec                                               | 549 ms: 1.97x faster                                                       |
| async_tree_none_tg         | 446 ms                                                 | 231 ms: 1.93x faster                                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 291 ms: 1.93x faster                                                       |
| richards                   | 45.9 ms                                                | 23.9 ms: 1.93x faster                                                      |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                                       |
| gc_traversal               | 3.46 ms                                                | 1.93 ms: 1.79x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                       |
| richards_super             | 51.9 ms                                                | 29.3 ms: 1.77x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 481 ms: 1.50x faster                                                       |
| mdp                        | 2.42 sec                                               | 1.65 sec: 1.47x faster                                                     |
| float                      | 80.8 ms                                                | 55.4 ms: 1.46x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                       |
| deepcopy_memo              | 40.3 us                                                | 29.5 us: 1.37x faster                                                      |
| logging_silent             | 109 ns                                                 | 87.1 ns: 1.25x faster                                                      |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                      |
| deepcopy                   | 352 us                                                 | 293 us: 1.20x faster                                                       |
| go                         | 139 ms                                                 | 117 ms: 1.19x faster                                                       |
| scimark_fft                | 342 ms                                                 | 293 ms: 1.17x faster                                                       |
| bpe_tokeniser              | 4.74 sec                                               | 4.10 sec: 1.15x faster                                                     |
| scimark_sor                | 130 ms                                                 | 113 ms: 1.15x faster                                                       |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 85.8 ms: 1.13x faster                                                      |
| sqlite_synth               | 2.20 us                                                | 1.98 us: 1.11x faster                                                      |
| pyflate                    | 448 ms                                                 | 404 ms: 1.11x faster                                                       |
| spectral_norm              | 110 ms                                                 | 99.5 ms: 1.11x faster                                                      |
| unpickle_pure_python       | 221 us                                                 | 201 us: 1.10x faster                                                       |
| deltablue                  | 3.45 ms                                                | 3.18 ms: 1.08x faster                                                      |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                       |
| generators                 | 32.2 ms                                                | 30.8 ms: 1.05x faster                                                      |
| comprehensions             | 19.8 us                                                | 19.0 us: 1.04x faster                                                      |
| tomli_loads                | 2.11 sec                                               | 2.02 sec: 1.04x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.99 us: 1.03x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.01x faster                                                       |
| dulwich_log                | 78.9 ms                                                | 79.7 ms: 1.01x slower                                                      |
| pprint_safe_repr           | 743 ms                                                 | 757 ms: 1.02x slower                                                       |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                      |
| logging_simple             | 6.63 us                                                | 6.86 us: 1.04x slower                                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 70.9 ms: 1.04x slower                                                      |
| chaos                      | 62.8 ms                                                | 65.2 ms: 1.04x slower                                                      |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                      |
| regex_compile              | 142 ms                                                 | 148 ms: 1.04x slower                                                       |
| json                       | 5.02 ms                                                | 5.26 ms: 1.05x slower                                                      |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                       |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                      |
| pylint                     | 319 ms                                                 | 335 ms: 1.05x slower                                                       |
| raytrace                   | 299 ms                                                 | 315 ms: 1.05x slower                                                       |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                       |
| xml_etree_generate         | 85.2 ms                                                | 89.8 ms: 1.05x slower                                                      |
| pickle_pure_python         | 308 us                                                 | 324 us: 1.05x slower                                                       |
| pprint_pformat             | 1.52 sec                                               | 1.60 sec: 1.06x slower                                                     |
| logging_format             | 7.35 us                                                | 7.82 us: 1.07x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 63.4 ms: 1.07x slower                                                      |
| scimark_lu                 | 114 ms                                                 | 124 ms: 1.08x slower                                                       |
| 2to3                       | 264 ms                                                 | 286 ms: 1.09x slower                                                       |
| thrift                     | 791 us                                                 | 863 us: 1.09x slower                                                       |
| crypto_pyaes               | 76.6 ms                                                | 84.9 ms: 1.11x slower                                                      |
| meteor_contest             | 104 ms                                                 | 115 ms: 1.11x slower                                                       |
| fannkuch                   | 372 ms                                                 | 418 ms: 1.12x slower                                                       |
| nbody                      | 89.3 ms                                                | 101 ms: 1.13x slower                                                       |
| html5lib                   | 63.6 ms                                                | 73.8 ms: 1.16x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.12 ms: 1.17x slower                                                      |
| sympy_integrate            | 20.5 ms                                                | 24.1 ms: 1.17x slower                                                      |
| json_loads                 | 26.5 us                                                | 31.2 us: 1.18x slower                                                      |
| hexiom                     | 6.17 ms                                                | 7.29 ms: 1.18x slower                                                      |
| typing_runtime_protocols   | 163 us                                                 | 194 us: 1.19x slower                                                       |
| sympy_sum                  | 166 ms                                                 | 199 ms: 1.20x slower                                                       |
| nqueens                    | 80.1 ms                                                | 96.1 ms: 1.20x slower                                                      |
| django_template            | 34.7 ms                                                | 42.1 ms: 1.21x slower                                                      |
| genshi_text                | 22.8 ms                                                | 28.5 ms: 1.25x slower                                                      |
| sympy_str                  | 292 ms                                                 | 367 ms: 1.26x slower                                                       |
| sympy_expand               | 468 ms                                                 | 593 ms: 1.27x slower                                                       |
| mako                       | 11.0 ms                                                | 14.3 ms: 1.30x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 9.50 ms: 1.33x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.52 ms: 1.39x slower                                                      |
| genshi_xml                 | 50.2 ms                                                | 71.8 ms: 1.43x slower                                                      |
| bench_mp_pool              | 10.8 ms                                                | 15.7 ms: 1.45x slower                                                      |
| coverage                   | 71.4 ms                                                | 113 ms: 1.58x slower                                                       |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                      |
| bench_thread_pool          | 941 us                                                 | 3.18 ms: 3.38x slower                                                      |
| telco                      | 6.53 ms                                                | 179 ms: 27.48x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.01x slower                                                               |
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_generators, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (7) of results/bm-20251116-3.15.0a1+-763ebea-JIT,NOGIL/bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea.json: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 60.51% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x