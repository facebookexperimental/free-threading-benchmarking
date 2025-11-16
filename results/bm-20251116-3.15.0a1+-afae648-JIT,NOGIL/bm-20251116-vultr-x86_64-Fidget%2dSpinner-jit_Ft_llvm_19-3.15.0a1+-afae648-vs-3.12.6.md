# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: jit_Ft_llvm_19
- machine: linux-x86_64
- commit hash: afae648
- commit date: 2025-11-16
- overall geometric mean: 1.014x slower
- HPT reliability: 70.90%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 286 ms: 1.09x slower                                                       |
| html5lib       | 63.6 ms                                                | 74.0 ms: 1.16x slower                                                      |
| Geometric mean | (ref)                                                  | 1.12x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 541 ms: 2.05x faster                                                       |
| async_tree_io              | 1.08 sec                                               | 562 ms: 1.92x faster                                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 292 ms: 1.91x faster                                                       |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.91x faster                                                       |
| async_tree_none            | 464 ms                                                 | 262 ms: 1.77x faster                                                       |
| async_tree_memoization     | 555 ms                                                 | 320 ms: 1.74x faster                                                       |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 540 ms: 1.34x faster                                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 565 ms: 1.27x faster                                                       |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                       |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 57.4 ms: 1.41x faster                                                      |
| pidigits       | 184 ms                                                 | 217 ms: 1.18x slower                                                       |
| nbody          | 89.3 ms                                                | 105 ms: 1.18x slower                                                       |
| Geometric mean | (ref)                                                  | 1.00x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                      |
| regex_compile  | 142 ms                                                 | 149 ms: 1.05x slower                                                       |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                      |
| regex_dna      | 168 ms                                                 | 179 ms: 1.07x slower                                                       |
| Geometric mean | (ref)                                                  | 1.02x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.4 ms: 1.12x faster                                                      |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                       |
| unpickle_pure_python | 221 us                                                 | 210 us: 1.05x faster                                                       |
| tomli_loads          | 2.11 sec                                               | 2.02 sec: 1.04x faster                                                     |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                      |
| xml_etree_generate   | 85.2 ms                                                | 90.7 ms: 1.06x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 335 us: 1.09x slower                                                       |
| xml_etree_process    | 59.0 ms                                                | 64.5 ms: 1.09x slower                                                      |
| json_loads           | 26.5 us                                                | 31.5 us: 1.19x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.51 ms: 1.33x slower                                                      |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 42.4 ms: 1.22x slower                                                      |
| genshi_text     | 22.8 ms                                                | 28.9 ms: 1.27x slower                                                      |
| mako            | 11.0 ms                                                | 14.3 ms: 1.30x slower                                                      |
| genshi_xml      | 50.2 ms                                                | 69.8 ms: 1.39x slower                                                      |
| Geometric mean  | (ref)                                                  | 1.29x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 541 ms: 2.05x faster                                                       |
| async_tree_io              | 1.08 sec                                               | 562 ms: 1.92x faster                                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 292 ms: 1.91x faster                                                       |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.91x faster                                                       |
| gc_traversal               | 3.46 ms                                                | 1.93 ms: 1.79x faster                                                      |
| async_tree_none            | 464 ms                                                 | 262 ms: 1.77x faster                                                       |
| async_tree_memoization     | 555 ms                                                 | 320 ms: 1.74x faster                                                       |
| richards                   | 45.9 ms                                                | 27.4 ms: 1.68x faster                                                      |
| richards_super             | 51.9 ms                                                | 32.8 ms: 1.58x faster                                                      |
| mdp                        | 2.42 sec                                               | 1.62 sec: 1.49x faster                                                     |
| float                      | 80.8 ms                                                | 57.4 ms: 1.41x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 30.0 us: 1.34x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 540 ms: 1.34x faster                                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 565 ms: 1.27x faster                                                       |
| pathlib                    | 21.5 ms                                                | 18.0 ms: 1.19x faster                                                      |
| deepcopy                   | 352 us                                                 | 299 us: 1.18x faster                                                       |
| scimark_fft                | 342 ms                                                 | 295 ms: 1.16x faster                                                       |
| scimark_sor                | 130 ms                                                 | 114 ms: 1.14x faster                                                       |
| bpe_tokeniser              | 4.74 sec                                               | 4.17 sec: 1.14x faster                                                     |
| go                         | 139 ms                                                 | 123 ms: 1.13x faster                                                       |
| xml_etree_iterparse        | 96.7 ms                                                | 86.4 ms: 1.12x faster                                                      |
| logging_silent             | 109 ns                                                 | 97.3 ns: 1.12x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                      |
| sqlite_synth               | 2.20 us                                                | 2.01 us: 1.09x faster                                                      |
| spectral_norm              | 110 ms                                                 | 101 ms: 1.09x faster                                                       |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                       |
| pyflate                    | 448 ms                                                 | 427 ms: 1.05x faster                                                       |
| unpickle_pure_python       | 221 us                                                 | 210 us: 1.05x faster                                                       |
| tomli_loads                | 2.11 sec                                               | 2.02 sec: 1.04x faster                                                     |
| comprehensions             | 19.8 us                                                | 19.1 us: 1.04x faster                                                      |
| generators                 | 32.2 ms                                                | 31.1 ms: 1.04x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                       |
| dulwich_log                | 78.9 ms                                                | 79.4 ms: 1.01x slower                                                      |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                      |
| pycparser                  | 1.17 sec                                               | 1.21 sec: 1.03x slower                                                     |
| chaos                      | 62.8 ms                                                | 65.0 ms: 1.03x slower                                                      |
| regex_compile              | 142 ms                                                 | 149 ms: 1.05x slower                                                       |
| pprint_safe_repr           | 743 ms                                                 | 777 ms: 1.05x slower                                                       |
| scimark_monte_carlo        | 68.4 ms                                                | 71.9 ms: 1.05x slower                                                      |
| json                       | 5.02 ms                                                | 5.28 ms: 1.05x slower                                                      |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                      |
| logging_simple             | 6.63 us                                                | 6.98 us: 1.05x slower                                                      |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                      |
| pylint                     | 319 ms                                                 | 337 ms: 1.06x slower                                                       |
| xml_etree_generate         | 85.2 ms                                                | 90.7 ms: 1.06x slower                                                      |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.07x slower                                                       |
| logging_format             | 7.35 us                                                | 7.94 us: 1.08x slower                                                      |
| scimark_lu                 | 114 ms                                                 | 124 ms: 1.08x slower                                                       |
| 2to3                       | 264 ms                                                 | 286 ms: 1.09x slower                                                       |
| raytrace                   | 299 ms                                                 | 326 ms: 1.09x slower                                                       |
| pickle_pure_python         | 308 us                                                 | 335 us: 1.09x slower                                                       |
| pprint_pformat             | 1.52 sec                                               | 1.66 sec: 1.09x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 64.5 ms: 1.09x slower                                                      |
| meteor_contest             | 104 ms                                                 | 115 ms: 1.11x slower                                                       |
| crypto_pyaes               | 76.6 ms                                                | 85.9 ms: 1.12x slower                                                      |
| thrift                     | 791 us                                                 | 889 us: 1.12x slower                                                       |
| fannkuch                   | 372 ms                                                 | 420 ms: 1.13x slower                                                       |
| html5lib                   | 63.6 ms                                                | 74.0 ms: 1.16x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.12 ms: 1.17x slower                                                      |
| sympy_integrate            | 20.5 ms                                                | 24.1 ms: 1.17x slower                                                      |
| pidigits                   | 184 ms                                                 | 217 ms: 1.18x slower                                                       |
| nbody                      | 89.3 ms                                                | 105 ms: 1.18x slower                                                       |
| json_loads                 | 26.5 us                                                | 31.5 us: 1.19x slower                                                      |
| nqueens                    | 80.1 ms                                                | 95.2 ms: 1.19x slower                                                      |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                                       |
| sympy_sum                  | 166 ms                                                 | 200 ms: 1.21x slower                                                       |
| hexiom                     | 6.17 ms                                                | 7.54 ms: 1.22x slower                                                      |
| django_template            | 34.7 ms                                                | 42.4 ms: 1.22x slower                                                      |
| sympy_str                  | 292 ms                                                 | 367 ms: 1.26x slower                                                       |
| genshi_text                | 22.8 ms                                                | 28.9 ms: 1.27x slower                                                      |
| sympy_expand               | 468 ms                                                 | 595 ms: 1.27x slower                                                       |
| mako                       | 11.0 ms                                                | 14.3 ms: 1.30x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 9.51 ms: 1.33x slower                                                      |
| genshi_xml                 | 50.2 ms                                                | 69.8 ms: 1.39x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.52 ms: 1.40x slower                                                      |
| bench_mp_pool              | 10.8 ms                                                | 16.2 ms: 1.50x slower                                                      |
| coverage                   | 71.4 ms                                                | 111 ms: 1.56x slower                                                       |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                      |
| bench_thread_pool          | 941 us                                                 | 3.19 ms: 3.39x slower                                                      |
| telco                      | 6.53 ms                                                | 181 ms: 27.71x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                               |

Benchmark hidden because not significant (2): deepcopy_reduce, deltablue
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_generators, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (7) of results/bm-20251116-3.15.0a1+-afae648-JIT,NOGIL/bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648.json: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.014x slower

# HPT report

- Reliability score: 70.90% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x