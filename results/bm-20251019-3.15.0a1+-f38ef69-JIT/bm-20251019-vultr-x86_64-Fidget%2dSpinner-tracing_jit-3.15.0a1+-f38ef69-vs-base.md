# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: f38ef69
- commit date: 2025-10-19
- overall geometric mean: 1.072x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                 | 291 ms: 1.15x slower                                                    |
| docutils       | 2.60 sec                                                               | 2.74 sec: 1.05x slower                                                  |
| html5lib       | 62.8 ms                                                                | 75.1 ms: 1.20x slower                                                   |
| sphinx         | 992 ms                                                                 | 1.05 sec: 1.06x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 497 ms                                                                 | 528 ms: 1.06x slower                                                    |
| async_tree_cpu_io_mixed    | 493 ms                                                                 | 535 ms: 1.09x slower                                                    |
| async_generators           | 359 ms                                                                 | 391 ms: 1.09x slower                                                    |
| async_tree_memoization_tg  | 312 ms                                                                 | 344 ms: 1.10x slower                                                    |
| async_tree_io_tg           | 622 ms                                                                 | 696 ms: 1.12x slower                                                    |
| async_tree_none_tg         | 250 ms                                                                 | 281 ms: 1.12x slower                                                    |
| async_tree_io              | 600 ms                                                                 | 675 ms: 1.12x slower                                                    |
| async_tree_memoization     | 312 ms                                                                 | 354 ms: 1.13x slower                                                    |
| async_tree_none            | 264 ms                                                                 | 301 ms: 1.14x slower                                                    |
| coroutines                 | 23.8 ms                                                                | 27.5 ms: 1.16x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 71.5 ms                                                                | 63.5 ms: 1.13x faster                                                   |
| pidigits       | 202 ms                                                                 | 194 ms: 1.04x faster                                                    |
| nbody          | 91.0 ms                                                                | 131 ms: 1.44x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 188 ms                                                                 | 168 ms: 1.12x faster                                                    |
| regex_effbot   | 2.86 ms                                                                | 2.56 ms: 1.12x faster                                                   |
| regex_v8       | 22.3 ms                                                                | 21.6 ms: 1.03x faster                                                   |
| regex_compile  | 125 ms                                                                 | 160 ms: 1.28x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 9.59 ms                                                                | 9.33 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 92.5 ms                                                                | 92.9 ms: 1.00x slower                                                   |
| xml_etree_parse      | 131 ms                                                                 | 133 ms: 1.01x slower                                                    |
| json_loads           | 27.9 us                                                                | 28.4 us: 1.02x slower                                                   |
| unpickle_pure_python | 184 us                                                                 | 190 us: 1.03x slower                                                    |
| tomli_loads          | 1.73 sec                                                               | 1.85 sec: 1.07x slower                                                  |
| xml_etree_generate   | 77.5 ms                                                                | 87.9 ms: 1.13x slower                                                   |
| pickle_pure_python   | 301 us                                                                 | 343 us: 1.14x slower                                                    |
| xml_etree_process    | 53.7 ms                                                                | 63.6 ms: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.29 ms                                                                | 7.40 ms: 1.02x slower                                                   |
| python_startup         | 12.6 ms                                                                | 12.9 ms: 1.02x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.9 ms                                                                | 10.6 ms: 1.03x faster                                                   |
| genshi_text     | 20.6 ms                                                                | 24.9 ms: 1.21x slower                                                   |
| django_template | 34.4 ms                                                                | 43.2 ms: 1.26x slower                                                   |
| genshi_xml      | 49.0 ms                                                                | 70.1 ms: 1.43x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-f38ef69 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards_super             | 46.5 ms                                                                | 34.7 ms: 1.34x faster                                                   |
| richards                   | 40.7 ms                                                                | 30.4 ms: 1.34x faster                                                   |
| spectral_norm              | 99.9 ms                                                                | 84.1 ms: 1.19x faster                                                   |
| logging_silent             | 97.1 ns                                                                | 84.1 ns: 1.15x faster                                                   |
| deepcopy_memo              | 26.6 us                                                                | 23.2 us: 1.15x faster                                                   |
| float                      | 71.5 ms                                                                | 63.5 ms: 1.13x faster                                                   |
| regex_dna                  | 188 ms                                                                 | 168 ms: 1.12x faster                                                    |
| regex_effbot               | 2.86 ms                                                                | 2.56 ms: 1.12x faster                                                   |
| deltablue                  | 3.28 ms                                                                | 3.05 ms: 1.07x faster                                                   |
| comprehensions             | 16.2 us                                                                | 15.4 us: 1.05x faster                                                   |
| pidigits                   | 202 ms                                                                 | 194 ms: 1.04x faster                                                    |
| scimark_monte_carlo        | 62.2 ms                                                                | 59.9 ms: 1.04x faster                                                   |
| regex_v8                   | 22.3 ms                                                                | 21.6 ms: 1.03x faster                                                   |
| mako                       | 10.9 ms                                                                | 10.6 ms: 1.03x faster                                                   |
| json_dumps                 | 9.59 ms                                                                | 9.33 ms: 1.03x faster                                                   |
| bpe_tokeniser              | 3.98 sec                                                               | 3.97 sec: 1.00x faster                                                  |
| xml_etree_iterparse        | 92.5 ms                                                                | 92.9 ms: 1.00x slower                                                   |
| connected_components       | 392 ms                                                                 | 395 ms: 1.01x slower                                                    |
| shortest_path              | 437 ms                                                                 | 442 ms: 1.01x slower                                                    |
| crypto_pyaes               | 68.5 ms                                                                | 69.3 ms: 1.01x slower                                                   |
| xml_etree_parse            | 131 ms                                                                 | 133 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult    | 4.35 ms                                                                | 4.41 ms: 1.01x slower                                                   |
| python_startup_no_site     | 7.29 ms                                                                | 7.40 ms: 1.02x slower                                                   |
| json_loads                 | 27.9 us                                                                | 28.4 us: 1.02x slower                                                   |
| python_startup             | 12.6 ms                                                                | 12.9 ms: 1.02x slower                                                   |
| gc_traversal               | 4.43 ms                                                                | 4.53 ms: 1.02x slower                                                   |
| sqlite_synth               | 2.18 us                                                                | 2.23 us: 1.02x slower                                                   |
| coverage                   | 82.7 ms                                                                | 84.8 ms: 1.03x slower                                                   |
| bench_mp_pool              | 12.4 ms                                                                | 12.7 ms: 1.03x slower                                                   |
| unpickle_pure_python       | 184 us                                                                 | 190 us: 1.03x slower                                                    |
| chaos                      | 57.3 ms                                                                | 59.2 ms: 1.03x slower                                                   |
| bench_thread_pool          | 1.01 ms                                                                | 1.04 ms: 1.04x slower                                                   |
| docutils                   | 2.60 sec                                                               | 2.74 sec: 1.05x slower                                                  |
| nqueens                    | 79.3 ms                                                                | 84.1 ms: 1.06x slower                                                   |
| sphinx                     | 992 ms                                                                 | 1.05 sec: 1.06x slower                                                  |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                 | 528 ms: 1.06x slower                                                    |
| tomli_loads                | 1.73 sec                                                               | 1.85 sec: 1.07x slower                                                  |
| scimark_fft                | 258 ms                                                                 | 279 ms: 1.08x slower                                                    |
| async_tree_cpu_io_mixed    | 493 ms                                                                 | 535 ms: 1.09x slower                                                    |
| pprint_safe_repr           | 704 ms                                                                 | 768 ms: 1.09x slower                                                    |
| async_generators           | 359 ms                                                                 | 391 ms: 1.09x slower                                                    |
| deepcopy                   | 244 us                                                                 | 268 us: 1.10x slower                                                    |
| many_optionals             | 1.26 ms                                                                | 1.38 ms: 1.10x slower                                                   |
| dulwich_log                | 69.3 ms                                                                | 76.4 ms: 1.10x slower                                                   |
| async_tree_memoization_tg  | 312 ms                                                                 | 344 ms: 1.10x slower                                                    |
| pprint_pformat             | 1.42 sec                                                               | 1.57 sec: 1.11x slower                                                  |
| sympy_integrate            | 19.2 ms                                                                | 21.3 ms: 1.11x slower                                                   |
| thrift                     | 735 us                                                                 | 817 us: 1.11x slower                                                    |
| sympy_expand               | 484 ms                                                                 | 540 ms: 1.12x slower                                                    |
| sympy_sum                  | 155 ms                                                                 | 173 ms: 1.12x slower                                                    |
| async_tree_io_tg           | 622 ms                                                                 | 696 ms: 1.12x slower                                                    |
| typing_runtime_protocols   | 153 us                                                                 | 171 us: 1.12x slower                                                    |
| pylint                     | 282 ms                                                                 | 316 ms: 1.12x slower                                                    |
| async_tree_none_tg         | 250 ms                                                                 | 281 ms: 1.12x slower                                                    |
| async_tree_io              | 600 ms                                                                 | 675 ms: 1.12x slower                                                    |
| deepcopy_reduce            | 2.58 us                                                                | 2.90 us: 1.13x slower                                                   |
| hexiom                     | 5.75 ms                                                                | 6.50 ms: 1.13x slower                                                   |
| sympy_str                  | 278 ms                                                                 | 315 ms: 1.13x slower                                                    |
| sqlglot_v2_optimize        | 50.8 ms                                                                | 57.5 ms: 1.13x slower                                                   |
| async_tree_memoization     | 312 ms                                                                 | 354 ms: 1.13x slower                                                    |
| xml_etree_generate         | 77.5 ms                                                                | 87.9 ms: 1.13x slower                                                   |
| pickle_pure_python         | 301 us                                                                 | 343 us: 1.14x slower                                                    |
| subparsers                 | 45.1 ms                                                                | 51.5 ms: 1.14x slower                                                   |
| async_tree_none            | 264 ms                                                                 | 301 ms: 1.14x slower                                                    |
| sqlglot_v2_normalize       | 100 ms                                                                 | 115 ms: 1.14x slower                                                    |
| 2to3                       | 252 ms                                                                 | 291 ms: 1.15x slower                                                    |
| coroutines                 | 23.8 ms                                                                | 27.5 ms: 1.16x slower                                                   |
| pycparser                  | 1.08 sec                                                               | 1.27 sec: 1.17x slower                                                  |
| pathlib                    | 17.6 ms                                                                | 20.8 ms: 1.18x slower                                                   |
| xml_etree_process          | 53.7 ms                                                                | 63.6 ms: 1.18x slower                                                   |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.80 ms: 1.19x slower                                                   |
| html5lib                   | 62.8 ms                                                                | 75.1 ms: 1.20x slower                                                   |
| scimark_lu                 | 110 ms                                                                 | 132 ms: 1.20x slower                                                    |
| logging_format             | 6.64 us                                                                | 7.98 us: 1.20x slower                                                   |
| scimark_sor                | 110 ms                                                                 | 132 ms: 1.21x slower                                                    |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.46 ms: 1.21x slower                                                   |
| telco                      | 156 ms                                                                 | 189 ms: 1.21x slower                                                    |
| raytrace                   | 255 ms                                                                 | 308 ms: 1.21x slower                                                    |
| genshi_text                | 20.6 ms                                                                | 24.9 ms: 1.21x slower                                                   |
| logging_simple             | 5.85 us                                                                | 7.12 us: 1.22x slower                                                   |
| mdp                        | 1.16 sec                                                               | 1.43 sec: 1.23x slower                                                  |
| go                         | 106 ms                                                                 | 131 ms: 1.24x slower                                                    |
| django_template            | 34.4 ms                                                                | 43.2 ms: 1.26x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.26x slower                                                    |
| regex_compile              | 125 ms                                                                 | 160 ms: 1.28x slower                                                    |
| generators                 | 28.0 ms                                                                | 37.2 ms: 1.33x slower                                                   |
| genshi_xml                 | 49.0 ms                                                                | 70.1 ms: 1.43x slower                                                   |
| nbody                      | 91.0 ms                                                                | 131 ms: 1.44x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                            |

Benchmark hidden because not significant (6): k_core, json, create_gc_cycles, fannkuch, asyncio_websockets, pyflate

- Geometric mean (including insignificant results): 1.072x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.01x