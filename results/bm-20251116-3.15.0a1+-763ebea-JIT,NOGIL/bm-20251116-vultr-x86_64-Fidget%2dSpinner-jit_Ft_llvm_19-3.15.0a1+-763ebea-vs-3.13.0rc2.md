# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: jit_Ft_llvm_19
- machine: linux-x86_64
- commit hash: 763ebea
- commit date: 2025-11-16
- overall geometric mean: 1.029x slower
- HPT reliability: 70.73%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 286 ms: 1.10x slower                                                       |
| html5lib       | 67.0 ms                                                      | 73.8 ms: 1.10x slower                                                      |
| Geometric mean | (ref)                                                        | 1.10x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 530 ms: 1.72x faster                                                       |
| async_tree_io              | 876 ms                                                       | 549 ms: 1.60x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 231 ms: 1.46x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 291 ms: 1.43x faster                                                       |
| async_tree_none            | 354 ms                                                       | 257 ms: 1.38x faster                                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 481 ms: 1.33x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 503 ms: 1.32x faster                                                       |
| asyncio_websockets         | 520 ms                                                       | 509 ms: 1.02x faster                                                       |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 55.4 ms: 1.40x faster                                                      |
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                       |
| nbody          | 85.1 ms                                                      | 101 ms: 1.18x slower                                                       |
| Geometric mean | (ref)                                                        | 1.10x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                      |
| regex_v8       | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                      |
| regex_dna      | 180 ms                                                       | 176 ms: 1.02x faster                                                       |
| regex_compile  | 132 ms                                                       | 148 ms: 1.12x slower                                                       |
| Geometric mean | (ref)                                                        | 1.02x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 85.8 ms: 1.11x faster                                                      |
| unpickle_pure_python | 210 us                                                       | 201 us: 1.05x faster                                                       |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.04x faster                                                       |
| tomli_loads          | 2.01 sec                                                     | 2.02 sec: 1.01x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 10.9 ms: 1.03x slower                                                      |
| xml_etree_generate   | 85.4 ms                                                      | 89.8 ms: 1.05x slower                                                      |
| xml_etree_process    | 59.3 ms                                                      | 63.4 ms: 1.07x slower                                                      |
| pickle_pure_python   | 294 us                                                       | 324 us: 1.10x slower                                                       |
| json_loads           | 27.0 us                                                      | 31.2 us: 1.15x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.50 ms: 1.29x slower                                                      |
| python_startup         | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 42.1 ms: 1.23x slower                                                      |
| mako            | 11.3 ms                                                      | 14.3 ms: 1.26x slower                                                      |
| genshi_text     | 21.5 ms                                                      | 28.5 ms: 1.32x slower                                                      |
| genshi_xml      | 48.8 ms                                                      | 71.8 ms: 1.47x slower                                                      |
| Geometric mean  | (ref)                                                        | 1.32x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 23.9 ms: 1.90x faster                                                      |
| richards_super             | 51.6 ms                                                      | 29.3 ms: 1.76x faster                                                      |
| async_tree_io_tg           | 913 ms                                                       | 530 ms: 1.72x faster                                                       |
| gc_traversal               | 3.14 ms                                                      | 1.93 ms: 1.63x faster                                                      |
| async_tree_io              | 876 ms                                                       | 549 ms: 1.60x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 231 ms: 1.46x faster                                                       |
| mdp                        | 2.36 sec                                                     | 1.65 sec: 1.43x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 291 ms: 1.43x faster                                                       |
| float                      | 77.5 ms                                                      | 55.4 ms: 1.40x faster                                                      |
| async_tree_none            | 354 ms                                                       | 257 ms: 1.38x faster                                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 481 ms: 1.33x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 503 ms: 1.32x faster                                                       |
| deepcopy_memo              | 39.1 us                                                      | 29.5 us: 1.32x faster                                                      |
| deepcopy                   | 355 us                                                       | 293 us: 1.21x faster                                                       |
| go                         | 141 ms                                                       | 117 ms: 1.20x faster                                                       |
| scimark_fft                | 349 ms                                                       | 293 ms: 1.19x faster                                                       |
| scimark_sor                | 134 ms                                                       | 113 ms: 1.19x faster                                                       |
| logging_silent             | 103 ns                                                       | 87.1 ns: 1.18x faster                                                      |
| spectral_norm              | 111 ms                                                       | 99.5 ms: 1.12x faster                                                      |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                       |
| sqlite_synth               | 2.21 us                                                      | 1.98 us: 1.12x faster                                                      |
| pyflate                    | 449 ms                                                       | 404 ms: 1.11x faster                                                       |
| xml_etree_iterparse        | 94.9 ms                                                      | 85.8 ms: 1.11x faster                                                      |
| regex_effbot               | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                      |
| bpe_tokeniser              | 4.45 sec                                                     | 4.10 sec: 1.08x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                      |
| regex_v8                   | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                      |
| unpickle_pure_python       | 210 us                                                       | 201 us: 1.05x faster                                                       |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.04x faster                                                       |
| deepcopy_reduce            | 3.11 us                                                      | 2.99 us: 1.04x faster                                                      |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.02x faster                                                       |
| asyncio_websockets         | 520 ms                                                       | 509 ms: 1.02x faster                                                       |
| tomli_loads                | 2.01 sec                                                     | 2.02 sec: 1.01x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.18 ms: 1.02x slower                                                      |
| pprint_safe_repr           | 738 ms                                                       | 757 ms: 1.03x slower                                                       |
| json_dumps                 | 10.5 ms                                                      | 10.9 ms: 1.03x slower                                                      |
| xml_etree_generate         | 85.4 ms                                                      | 89.8 ms: 1.05x slower                                                      |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                      |
| dulwich_log                | 74.8 ms                                                      | 79.7 ms: 1.07x slower                                                      |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.07x slower                                                     |
| json                       | 4.93 ms                                                      | 5.26 ms: 1.07x slower                                                      |
| xml_etree_process          | 59.3 ms                                                      | 63.4 ms: 1.07x slower                                                      |
| generators                 | 28.8 ms                                                      | 30.8 ms: 1.07x slower                                                      |
| pprint_pformat             | 1.50 sec                                                     | 1.60 sec: 1.07x slower                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 70.9 ms: 1.08x slower                                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.12 ms: 1.09x slower                                                      |
| scimark_lu                 | 113 ms                                                       | 124 ms: 1.10x slower                                                       |
| pickle_pure_python         | 294 us                                                       | 324 us: 1.10x slower                                                       |
| 2to3                       | 260 ms                                                       | 286 ms: 1.10x slower                                                       |
| html5lib                   | 67.0 ms                                                      | 73.8 ms: 1.10x slower                                                      |
| thrift                     | 778 us                                                       | 863 us: 1.11x slower                                                       |
| logging_simple             | 6.16 us                                                      | 6.86 us: 1.11x slower                                                      |
| regex_compile              | 132 ms                                                       | 148 ms: 1.12x slower                                                       |
| fannkuch                   | 370 ms                                                       | 418 ms: 1.13x slower                                                       |
| create_gc_cycles           | 1.34 ms                                                      | 1.52 ms: 1.13x slower                                                      |
| meteor_contest             | 102 ms                                                       | 115 ms: 1.14x slower                                                       |
| chaos                      | 57.3 ms                                                      | 65.2 ms: 1.14x slower                                                      |
| logging_format             | 6.84 us                                                      | 7.82 us: 1.14x slower                                                      |
| comprehensions             | 16.5 us                                                      | 19.0 us: 1.15x slower                                                      |
| json_loads                 | 27.0 us                                                      | 31.2 us: 1.15x slower                                                      |
| nbody                      | 85.1 ms                                                      | 101 ms: 1.18x slower                                                       |
| sympy_integrate            | 19.8 ms                                                      | 24.1 ms: 1.21x slower                                                      |
| hexiom                     | 5.99 ms                                                      | 7.29 ms: 1.22x slower                                                      |
| nqueens                    | 78.6 ms                                                      | 96.1 ms: 1.22x slower                                                      |
| django_template            | 34.1 ms                                                      | 42.1 ms: 1.23x slower                                                      |
| raytrace                   | 253 ms                                                       | 315 ms: 1.25x slower                                                       |
| crypto_pyaes               | 67.9 ms                                                      | 84.9 ms: 1.25x slower                                                      |
| typing_runtime_protocols   | 155 us                                                       | 194 us: 1.26x slower                                                       |
| mako                       | 11.3 ms                                                      | 14.3 ms: 1.26x slower                                                      |
| sympy_sum                  | 156 ms                                                       | 199 ms: 1.28x slower                                                       |
| python_startup_no_site     | 7.39 ms                                                      | 9.50 ms: 1.29x slower                                                      |
| sympy_expand               | 457 ms                                                       | 593 ms: 1.30x slower                                                       |
| genshi_text                | 21.5 ms                                                      | 28.5 ms: 1.32x slower                                                      |
| sympy_str                  | 275 ms                                                       | 367 ms: 1.34x slower                                                       |
| coverage                   | 83.0 ms                                                      | 113 ms: 1.36x slower                                                       |
| bench_mp_pool              | 11.0 ms                                                      | 15.7 ms: 1.42x slower                                                      |
| python_startup             | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                                      |
| genshi_xml                 | 48.8 ms                                                      | 71.8 ms: 1.47x slower                                                      |
| bench_thread_pool          | 919 us                                                       | 3.18 ms: 3.47x slower                                                      |
| telco                      | 7.82 ms                                                      | 179 ms: 22.92x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.05x slower                                                               |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_generators, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (7) of results/bm-20251116-3.15.0a1+-763ebea-JIT,NOGIL/bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-763ebea.json: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.029x slower

# HPT report

- Reliability score: 70.73% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x