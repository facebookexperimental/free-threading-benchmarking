# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 7b2a8ca
- commit date: 2025-10-24
- overall geometric mean: 1.005x slower
- HPT reliability: 99.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                 | 253 ms: 1.00x slower                                                    |
| docutils       | 2.60 sec                                                               | 2.65 sec: 1.02x slower                                                  |
| html5lib       | 62.8 ms                                                                | 71.7 ms: 1.14x slower                                                   |
| sphinx         | 992 ms                                                                 | 1.01 sec: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 497 ms                                                                 | 493 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed    | 493 ms                                                                 | 498 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 250 ms                                                                 | 255 ms: 1.02x slower                                                    |
| async_tree_none            | 264 ms                                                                 | 269 ms: 1.02x slower                                                    |
| async_tree_io_tg           | 622 ms                                                                 | 635 ms: 1.02x slower                                                    |
| async_generators           | 359 ms                                                                 | 367 ms: 1.02x slower                                                    |
| async_tree_memoization     | 312 ms                                                                 | 320 ms: 1.02x slower                                                    |
| async_tree_io              | 600 ms                                                                 | 619 ms: 1.03x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (3): asyncio_websockets, coroutines, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 71.5 ms                                                                | 63.3 ms: 1.13x faster                                                   |
| pidigits       | 202 ms                                                                 | 193 ms: 1.04x faster                                                    |
| nbody          | 91.0 ms                                                                | 90.1 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 188 ms                                                                 | 182 ms: 1.03x faster                                                    |
| regex_effbot   | 2.86 ms                                                                | 2.78 ms: 1.03x faster                                                   |
| regex_compile  | 125 ms                                                                 | 128 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.5 ms                                                                | 90.1 ms: 1.03x faster                                                   |
| json_dumps           | 9.59 ms                                                                | 9.48 ms: 1.01x faster                                                   |
| unpickle_pure_python | 184 us                                                                 | 183 us: 1.01x faster                                                    |
| json_loads           | 27.9 us                                                                | 28.4 us: 1.02x slower                                                   |
| xml_etree_generate   | 77.5 ms                                                                | 79.4 ms: 1.02x slower                                                   |
| xml_etree_process    | 53.7 ms                                                                | 55.0 ms: 1.02x slower                                                   |
| pickle_pure_python   | 301 us                                                                 | 309 us: 1.03x slower                                                    |
| tomli_loads          | 1.73 sec                                                               | 1.79 sec: 1.03x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.29 ms                                                                | 7.30 ms: 1.00x slower                                                   |
| python_startup         | 12.6 ms                                                                | 12.6 ms: 1.00x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.9 ms                                                                | 10.6 ms: 1.02x faster                                                   |
| genshi_text     | 20.6 ms                                                                | 21.5 ms: 1.04x slower                                                   |
| django_template | 34.4 ms                                                                | 36.2 ms: 1.05x slower                                                   |
| genshi_xml      | 49.0 ms                                                                | 52.5 ms: 1.07x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251024-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-7b2a8ca |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 40.7 ms                                                                | 22.4 ms: 1.81x faster                                                   |
| richards_super             | 46.5 ms                                                                | 27.2 ms: 1.71x faster                                                   |
| spectral_norm              | 99.9 ms                                                                | 85.3 ms: 1.17x faster                                                   |
| float                      | 71.5 ms                                                                | 63.3 ms: 1.13x faster                                                   |
| logging_silent             | 97.1 ns                                                                | 86.7 ns: 1.12x faster                                                   |
| deepcopy_memo              | 26.6 us                                                                | 23.9 us: 1.12x faster                                                   |
| gc_traversal               | 4.43 ms                                                                | 4.08 ms: 1.09x faster                                                   |
| crypto_pyaes               | 68.5 ms                                                                | 65.0 ms: 1.05x faster                                                   |
| comprehensions             | 16.2 us                                                                | 15.4 us: 1.05x faster                                                   |
| pidigits                   | 202 ms                                                                 | 193 ms: 1.04x faster                                                    |
| scimark_monte_carlo        | 62.2 ms                                                                | 59.8 ms: 1.04x faster                                                   |
| pyflate                    | 393 ms                                                                 | 379 ms: 1.04x faster                                                    |
| regex_dna                  | 188 ms                                                                 | 182 ms: 1.03x faster                                                    |
| regex_effbot               | 2.86 ms                                                                | 2.78 ms: 1.03x faster                                                   |
| xml_etree_iterparse        | 92.5 ms                                                                | 90.1 ms: 1.03x faster                                                   |
| mako                       | 10.9 ms                                                                | 10.6 ms: 1.02x faster                                                   |
| fannkuch                   | 363 ms                                                                 | 355 ms: 1.02x faster                                                    |
| json_dumps                 | 9.59 ms                                                                | 9.48 ms: 1.01x faster                                                   |
| nbody                      | 91.0 ms                                                                | 90.1 ms: 1.01x faster                                                   |
| create_gc_cycles           | 1.93 ms                                                                | 1.92 ms: 1.01x faster                                                   |
| json                       | 5.01 ms                                                                | 4.97 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                 | 493 ms: 1.01x faster                                                    |
| unpickle_pure_python       | 184 us                                                                 | 183 us: 1.01x faster                                                    |
| python_startup_no_site     | 7.29 ms                                                                | 7.30 ms: 1.00x slower                                                   |
| python_startup             | 12.6 ms                                                                | 12.6 ms: 1.00x slower                                                   |
| 2to3                       | 252 ms                                                                 | 253 ms: 1.00x slower                                                    |
| coverage                   | 82.7 ms                                                                | 83.1 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed    | 493 ms                                                                 | 498 ms: 1.01x slower                                                    |
| bench_thread_pool          | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                   |
| sphinx                     | 992 ms                                                                 | 1.01 sec: 1.01x slower                                                  |
| many_optionals             | 1.26 ms                                                                | 1.28 ms: 1.02x slower                                                   |
| docutils                   | 2.60 sec                                                               | 2.65 sec: 1.02x slower                                                  |
| async_tree_none_tg         | 250 ms                                                                 | 255 ms: 1.02x slower                                                    |
| deepcopy_reduce            | 2.58 us                                                                | 2.63 us: 1.02x slower                                                   |
| json_loads                 | 27.9 us                                                                | 28.4 us: 1.02x slower                                                   |
| async_tree_none            | 264 ms                                                                 | 269 ms: 1.02x slower                                                    |
| scimark_fft                | 258 ms                                                                 | 264 ms: 1.02x slower                                                    |
| async_tree_io_tg           | 622 ms                                                                 | 635 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.18 us                                                                | 2.23 us: 1.02x slower                                                   |
| async_generators           | 359 ms                                                                 | 367 ms: 1.02x slower                                                    |
| xml_etree_generate         | 77.5 ms                                                                | 79.4 ms: 1.02x slower                                                   |
| telco                      | 156 ms                                                                 | 160 ms: 1.02x slower                                                    |
| xml_etree_process          | 53.7 ms                                                                | 55.0 ms: 1.02x slower                                                   |
| async_tree_memoization     | 312 ms                                                                 | 320 ms: 1.02x slower                                                    |
| pickle_pure_python         | 301 us                                                                 | 309 us: 1.03x slower                                                    |
| scimark_sparse_mat_mult    | 4.35 ms                                                                | 4.47 ms: 1.03x slower                                                   |
| deepcopy                   | 244 us                                                                 | 251 us: 1.03x slower                                                    |
| hexiom                     | 5.75 ms                                                                | 5.92 ms: 1.03x slower                                                   |
| regex_compile              | 125 ms                                                                 | 128 ms: 1.03x slower                                                    |
| async_tree_io              | 600 ms                                                                 | 619 ms: 1.03x slower                                                    |
| subparsers                 | 45.1 ms                                                                | 46.6 ms: 1.03x slower                                                   |
| tomli_loads                | 1.73 sec                                                               | 1.79 sec: 1.03x slower                                                  |
| typing_runtime_protocols   | 153 us                                                                 | 158 us: 1.03x slower                                                    |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.57 ms: 1.03x slower                                                   |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.25 ms: 1.04x slower                                                   |
| sqlglot_v2_optimize        | 50.8 ms                                                                | 52.6 ms: 1.04x slower                                                   |
| scimark_lu                 | 110 ms                                                                 | 115 ms: 1.04x slower                                                    |
| generators                 | 28.0 ms                                                                | 29.1 ms: 1.04x slower                                                   |
| genshi_text                | 20.6 ms                                                                | 21.5 ms: 1.04x slower                                                   |
| logging_format             | 6.64 us                                                                | 6.92 us: 1.04x slower                                                   |
| thrift                     | 735 us                                                                 | 768 us: 1.05x slower                                                    |
| logging_simple             | 5.85 us                                                                | 6.11 us: 1.05x slower                                                   |
| pycparser                  | 1.08 sec                                                               | 1.13 sec: 1.05x slower                                                  |
| django_template            | 34.4 ms                                                                | 36.2 ms: 1.05x slower                                                   |
| sympy_integrate            | 19.2 ms                                                                | 20.2 ms: 1.05x slower                                                   |
| dulwich_log                | 69.3 ms                                                                | 73.5 ms: 1.06x slower                                                   |
| mdp                        | 1.16 sec                                                               | 1.23 sec: 1.06x slower                                                  |
| sympy_str                  | 278 ms                                                                 | 296 ms: 1.06x slower                                                    |
| sympy_expand               | 484 ms                                                                 | 515 ms: 1.06x slower                                                    |
| nqueens                    | 79.3 ms                                                                | 84.5 ms: 1.07x slower                                                   |
| sympy_sum                  | 155 ms                                                                 | 165 ms: 1.07x slower                                                    |
| genshi_xml                 | 49.0 ms                                                                | 52.5 ms: 1.07x slower                                                   |
| sqlglot_v2_normalize       | 100 ms                                                                 | 108 ms: 1.08x slower                                                    |
| raytrace                   | 255 ms                                                                 | 280 ms: 1.10x slower                                                    |
| pathlib                    | 17.6 ms                                                                | 20.1 ms: 1.14x slower                                                   |
| html5lib                   | 62.8 ms                                                                | 71.7 ms: 1.14x slower                                                   |
| go                         | 106 ms                                                                 | 125 ms: 1.18x slower                                                    |
| deltablue                  | 3.28 ms                                                                | 4.69 ms: 1.43x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (16): pprint_safe_repr, k_core, connected_components, meteor_contest, xml_etree_parse, asyncio_websockets, scimark_sor, bpe_tokeniser, regex_v8, bench_mp_pool, coroutines, chaos, shortest_path, pprint_pformat, async_tree_memoization_tg, pylint

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 99.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x