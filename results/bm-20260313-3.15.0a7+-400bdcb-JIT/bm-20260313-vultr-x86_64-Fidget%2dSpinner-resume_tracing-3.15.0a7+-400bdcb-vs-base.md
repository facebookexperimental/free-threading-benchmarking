# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 400bdcb
- commit date: 2026-03-13
- overall geometric mean: 1.000x faster
- HPT reliability: 79.13%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                               | 2.65 sec: 1.01x slower                                                     |
| html5lib       | 63.6 ms                                                                | 61.2 ms: 1.04x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (2): 2to3, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_generators          | 403 ms                                                                 | 355 ms: 1.13x faster                                                       |
| coroutines                | 23.1 ms                                                                | 21.8 ms: 1.06x faster                                                      |
| async_tree_memoization    | 299 ms                                                                 | 287 ms: 1.04x faster                                                       |
| async_tree_none           | 240 ms                                                                 | 232 ms: 1.03x faster                                                       |
| async_tree_io_tg          | 564 ms                                                                 | 550 ms: 1.03x faster                                                       |
| async_tree_io             | 582 ms                                                                 | 567 ms: 1.03x faster                                                       |
| async_tree_none_tg        | 237 ms                                                                 | 233 ms: 1.02x faster                                                       |
| async_tree_memoization_tg | 297 ms                                                                 | 292 ms: 1.02x faster                                                       |
| Geometric mean            | (ref)                                                                  | 1.03x faster                                                               |

Benchmark hidden because not significant (3): asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 76.3 ms                                                                | 74.2 ms: 1.03x faster                                                      |
| pidigits       | 200 ms                                                                 | 219 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                               |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 189 ms                                                                 | 179 ms: 1.06x faster                                                       |
| regex_effbot   | 2.89 ms                                                                | 2.81 ms: 1.03x faster                                                      |
| regex_compile  | 124 ms                                                                 | 126 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                                | 8.97 ms: 1.02x faster                                                      |
| json_loads           | 27.5 us                                                                | 27.1 us: 1.02x faster                                                      |
| xml_etree_process    | 53.9 ms                                                                | 53.1 ms: 1.01x faster                                                      |
| unpickle_pure_python | 197 us                                                                 | 199 us: 1.01x slower                                                       |
| xml_etree_parse      | 129 ms                                                                 | 131 ms: 1.01x slower                                                       |
| xml_etree_iterparse  | 82.6 ms                                                                | 84.0 ms: 1.02x slower                                                      |
| xml_etree_generate   | 77.5 ms                                                                | 79.2 ms: 1.02x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                               |

Benchmark hidden because not significant (2): tomli_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                | 12.7 ms: 1.00x slower                                                      |
| python_startup_no_site | 7.46 ms                                                                | 7.51 ms: 1.01x slower                                                      |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| django_template | 35.1 ms                                                                | 33.9 ms: 1.04x faster                                                      |
| genshi_text     | 20.7 ms                                                                | 20.3 ms: 1.02x faster                                                      |
| mako            | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                      |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                               |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                 | bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7+-0adc728 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|---------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| bench_mp_pool             | 209 ms                                                                 | 182 ms: 1.15x faster                                                       |
| async_generators          | 403 ms                                                                 | 355 ms: 1.13x faster                                                       |
| logging_simple            | 5.85 us                                                                | 5.36 us: 1.09x faster                                                      |
| logging_format            | 6.58 us                                                                | 6.05 us: 1.09x faster                                                      |
| regex_dna                 | 189 ms                                                                 | 179 ms: 1.06x faster                                                       |
| coroutines                | 23.1 ms                                                                | 21.8 ms: 1.06x faster                                                      |
| scimark_sor               | 86.9 ms                                                                | 82.8 ms: 1.05x faster                                                      |
| sqlglot_v2_normalize      | 103 ms                                                                 | 98.3 ms: 1.04x faster                                                      |
| typing_runtime_protocols  | 157 us                                                                 | 150 us: 1.04x faster                                                       |
| async_tree_memoization    | 299 ms                                                                 | 287 ms: 1.04x faster                                                       |
| html5lib                  | 63.6 ms                                                                | 61.2 ms: 1.04x faster                                                      |
| django_template           | 35.1 ms                                                                | 33.9 ms: 1.04x faster                                                      |
| async_tree_none           | 240 ms                                                                 | 232 ms: 1.03x faster                                                       |
| telco                     | 160 ms                                                                 | 155 ms: 1.03x faster                                                       |
| regex_effbot              | 2.89 ms                                                                | 2.81 ms: 1.03x faster                                                      |
| nbody                     | 76.3 ms                                                                | 74.2 ms: 1.03x faster                                                      |
| pprint_safe_repr          | 645 ms                                                                 | 628 ms: 1.03x faster                                                       |
| async_tree_io_tg          | 564 ms                                                                 | 550 ms: 1.03x faster                                                       |
| async_tree_io             | 582 ms                                                                 | 567 ms: 1.03x faster                                                       |
| chaos                     | 53.4 ms                                                                | 52.2 ms: 1.02x faster                                                      |
| json_dumps                | 9.16 ms                                                                | 8.97 ms: 1.02x faster                                                      |
| genshi_text               | 20.7 ms                                                                | 20.3 ms: 1.02x faster                                                      |
| meteor_contest            | 99.5 ms                                                                | 97.5 ms: 1.02x faster                                                      |
| async_tree_none_tg        | 237 ms                                                                 | 233 ms: 1.02x faster                                                       |
| logging_silent            | 80.6 ns                                                                | 79.2 ns: 1.02x faster                                                      |
| async_tree_memoization_tg | 297 ms                                                                 | 292 ms: 1.02x faster                                                       |
| json_loads                | 27.5 us                                                                | 27.1 us: 1.02x faster                                                      |
| shortest_path             | 427 ms                                                                 | 420 ms: 1.02x faster                                                       |
| deltablue                 | 2.70 ms                                                                | 2.67 ms: 1.01x faster                                                      |
| xml_etree_process         | 53.9 ms                                                                | 53.1 ms: 1.01x faster                                                      |
| scimark_fft               | 259 ms                                                                 | 256 ms: 1.01x faster                                                       |
| pathlib                   | 17.6 ms                                                                | 17.4 ms: 1.01x faster                                                      |
| connected_components      | 378 ms                                                                 | 374 ms: 1.01x faster                                                       |
| mdp                       | 1.21 sec                                                               | 1.20 sec: 1.01x faster                                                     |
| sqlglot_v2_optimize       | 51.1 ms                                                                | 50.6 ms: 1.01x faster                                                      |
| scimark_sparse_mat_mult   | 4.22 ms                                                                | 4.18 ms: 1.01x faster                                                      |
| scimark_monte_carlo       | 52.2 ms                                                                | 51.7 ms: 1.01x faster                                                      |
| fannkuch                  | 341 ms                                                                 | 338 ms: 1.01x faster                                                       |
| mako                      | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                      |
| bpe_tokeniser             | 3.92 sec                                                               | 3.93 sec: 1.00x slower                                                     |
| python_startup            | 12.6 ms                                                                | 12.7 ms: 1.00x slower                                                      |
| coverage                  | 82.0 ms                                                                | 82.4 ms: 1.01x slower                                                      |
| python_startup_no_site    | 7.46 ms                                                                | 7.51 ms: 1.01x slower                                                      |
| regex_compile             | 124 ms                                                                 | 126 ms: 1.01x slower                                                       |
| hexiom                    | 5.69 ms                                                                | 5.75 ms: 1.01x slower                                                      |
| k_core                    | 1.84 sec                                                               | 1.86 sec: 1.01x slower                                                     |
| subparsers                | 8.80 ms                                                                | 8.90 ms: 1.01x slower                                                      |
| docutils                  | 2.62 sec                                                               | 2.65 sec: 1.01x slower                                                     |
| deepcopy_memo             | 22.4 us                                                                | 22.7 us: 1.01x slower                                                      |
| dulwich_log               | 69.2 ms                                                                | 70.1 ms: 1.01x slower                                                      |
| unpickle_pure_python      | 197 us                                                                 | 199 us: 1.01x slower                                                       |
| xml_etree_parse           | 129 ms                                                                 | 131 ms: 1.01x slower                                                       |
| crypto_pyaes              | 65.0 ms                                                                | 66.0 ms: 1.01x slower                                                      |
| scimark_lu                | 78.8 ms                                                                | 80.0 ms: 1.02x slower                                                      |
| xml_etree_iterparse       | 82.6 ms                                                                | 84.0 ms: 1.02x slower                                                      |
| many_optionals            | 965 us                                                                 | 981 us: 1.02x slower                                                       |
| sqlglot_v2_transpile      | 1.47 ms                                                                | 1.50 ms: 1.02x slower                                                      |
| xml_etree_generate        | 77.5 ms                                                                | 79.2 ms: 1.02x slower                                                      |
| sqlglot_v2_parse          | 1.16 ms                                                                | 1.20 ms: 1.04x slower                                                      |
| richards_super            | 21.4 ms                                                                | 22.2 ms: 1.04x slower                                                      |
| gc_traversal              | 4.15 ms                                                                | 4.32 ms: 1.04x slower                                                      |
| raytrace                  | 280 ms                                                                 | 293 ms: 1.05x slower                                                       |
| sympy_integrate           | 19.6 ms                                                                | 20.5 ms: 1.05x slower                                                      |
| pycparser                 | 1.10 sec                                                               | 1.16 sec: 1.05x slower                                                     |
| sympy_str                 | 288 ms                                                                 | 304 ms: 1.05x slower                                                       |
| pylint                    | 290 ms                                                                 | 308 ms: 1.06x slower                                                       |
| richards                  | 17.5 ms                                                                | 18.7 ms: 1.06x slower                                                      |
| sympy_sum                 | 163 ms                                                                 | 175 ms: 1.07x slower                                                       |
| pidigits                  | 200 ms                                                                 | 219 ms: 1.10x slower                                                       |
| comprehensions            | 14.9 us                                                                | 17.8 us: 1.20x slower                                                      |
| generators                | 28.5 ms                                                                | 34.6 ms: 1.21x slower                                                      |
| Geometric mean            | (ref)                                                                  | 1.00x faster                                                               |

Benchmark hidden because not significant (23): pprint_pformat, create_gc_cycles, tomli_loads, go, sqlite_synth, pickle_pure_python, float, thrift, spectral_norm, nqueens, regex_v8, genshi_xml, asyncio_websockets, json, deepcopy, deepcopy_reduce, async_tree_cpu_io_mixed_tg, 2to3, bench_thread_pool, async_tree_cpu_io_mixed, pyflate, sympy_expand, sphinx

- Geometric mean (including insignificant results): 1.000x faster

# HPT report

- Reliability score: 79.13% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x