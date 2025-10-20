# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: ec2971f
- commit date: 2025-10-20
- overall geometric mean: 1.006x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 252 ms: 1.01x slower                                                    |
| docutils       | 2.53 sec                                                               | 2.61 sec: 1.03x slower                                                  |
| html5lib       | 58.3 ms                                                                | 63.7 ms: 1.09x slower                                                   |
| sphinx         | 960 ms                                                                 | 986 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|-------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| coroutines              | 22.0 ms                                                                | 21.9 ms: 1.01x faster                                                   |
| async_tree_cpu_io_mixed | 470 ms                                                                 | 475 ms: 1.01x slower                                                    |
| async_tree_none_tg      | 241 ms                                                                 | 245 ms: 1.02x slower                                                    |
| async_tree_memoization  | 302 ms                                                                 | 308 ms: 1.02x slower                                                    |
| Geometric mean          | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (7): asyncio_websockets, async_generators, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_io, async_tree_memoization_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 66.8 ms                                                                | 62.0 ms: 1.08x faster                                                   |
| nbody          | 92.3 ms                                                                | 99.8 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                                 | 177 ms: 1.01x faster                                                    |
| regex_effbot   | 2.90 ms                                                                | 2.94 ms: 1.01x slower                                                   |
| regex_v8       | 21.2 ms                                                                | 21.8 ms: 1.03x slower                                                   |
| regex_compile  | 121 ms                                                                 | 138 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 8.92 ms                                                                | 8.74 ms: 1.02x faster                                                   |
| unpickle_pure_python | 186 us                                                                 | 183 us: 1.01x faster                                                    |
| xml_etree_parse      | 143 ms                                                                 | 143 ms: 1.01x faster                                                    |
| xml_etree_generate   | 74.8 ms                                                                | 75.5 ms: 1.01x slower                                                   |
| pickle_pure_python   | 301 us                                                                 | 305 us: 1.01x slower                                                    |
| json_loads           | 25.5 us                                                                | 25.9 us: 1.02x slower                                                   |
| tomli_loads          | 1.70 sec                                                               | 1.97 sec: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                                | 7.40 ms: 1.01x slower                                                   |
| python_startup         | 12.6 ms                                                                | 12.7 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                                | 10.9 ms: 1.03x faster                                                   |
| django_template | 32.7 ms                                                                | 33.5 ms: 1.02x slower                                                   |
| genshi_xml      | 46.9 ms                                                                | 48.6 ms: 1.04x slower                                                   |
| genshi_text     | 19.3 ms                                                                | 20.0 ms: 1.04x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark               | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-ec2971f |
|-------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                | 37.3 ms                                                                | 21.9 ms: 1.70x faster                                                   |
| richards_super          | 42.4 ms                                                                | 26.5 ms: 1.60x faster                                                   |
| deepcopy_memo           | 24.0 us                                                                | 21.9 us: 1.10x faster                                                   |
| scimark_lu              | 102 ms                                                                 | 93.6 ms: 1.09x faster                                                   |
| logging_silent          | 85.3 ns                                                                | 78.4 ns: 1.09x faster                                                   |
| float                   | 66.8 ms                                                                | 62.0 ms: 1.08x faster                                                   |
| deltablue               | 2.96 ms                                                                | 2.75 ms: 1.07x faster                                                   |
| pprint_safe_repr        | 688 ms                                                                 | 655 ms: 1.05x faster                                                    |
| comprehensions          | 15.3 us                                                                | 14.6 us: 1.05x faster                                                   |
| pprint_pformat          | 1.40 sec                                                               | 1.34 sec: 1.05x faster                                                  |
| scimark_monte_carlo     | 56.5 ms                                                                | 54.4 ms: 1.04x faster                                                   |
| scimark_sor             | 100 ms                                                                 | 97.0 ms: 1.03x faster                                                   |
| mako                    | 11.3 ms                                                                | 10.9 ms: 1.03x faster                                                   |
| json_dumps              | 8.92 ms                                                                | 8.74 ms: 1.02x faster                                                   |
| deepcopy_reduce         | 2.40 us                                                                | 2.35 us: 1.02x faster                                                   |
| json                    | 4.91 ms                                                                | 4.83 ms: 1.02x faster                                                   |
| scimark_fft             | 245 ms                                                                 | 242 ms: 1.01x faster                                                    |
| unpickle_pure_python    | 186 us                                                                 | 183 us: 1.01x faster                                                    |
| regex_dna               | 180 ms                                                                 | 177 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult | 3.96 ms                                                                | 3.91 ms: 1.01x faster                                                   |
| crypto_pyaes            | 66.3 ms                                                                | 65.8 ms: 1.01x faster                                                   |
| coverage                | 75.0 ms                                                                | 74.6 ms: 1.01x faster                                                   |
| xml_etree_parse         | 143 ms                                                                 | 143 ms: 1.01x faster                                                    |
| coroutines              | 22.0 ms                                                                | 21.9 ms: 1.01x faster                                                   |
| python_startup_no_site  | 7.35 ms                                                                | 7.40 ms: 1.01x slower                                                   |
| bpe_tokeniser           | 3.92 sec                                                               | 3.94 sec: 1.01x slower                                                  |
| spectral_norm           | 82.9 ms                                                                | 83.5 ms: 1.01x slower                                                   |
| python_startup          | 12.6 ms                                                                | 12.7 ms: 1.01x slower                                                   |
| xml_etree_generate      | 74.8 ms                                                                | 75.5 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed | 470 ms                                                                 | 475 ms: 1.01x slower                                                    |
| fannkuch                | 356 ms                                                                 | 360 ms: 1.01x slower                                                    |
| shortest_path           | 443 ms                                                                 | 449 ms: 1.01x slower                                                    |
| 2to3                    | 248 ms                                                                 | 252 ms: 1.01x slower                                                    |
| regex_effbot            | 2.90 ms                                                                | 2.94 ms: 1.01x slower                                                   |
| pickle_pure_python      | 301 us                                                                 | 305 us: 1.01x slower                                                    |
| connected_components    | 401 ms                                                                 | 407 ms: 1.02x slower                                                    |
| async_tree_none_tg      | 241 ms                                                                 | 245 ms: 1.02x slower                                                    |
| json_loads              | 25.5 us                                                                | 25.9 us: 1.02x slower                                                   |
| sympy_integrate         | 18.3 ms                                                                | 18.7 ms: 1.02x slower                                                   |
| async_tree_memoization  | 302 ms                                                                 | 308 ms: 1.02x slower                                                    |
| deepcopy                | 223 us                                                                 | 228 us: 1.02x slower                                                    |
| sqlite_synth            | 2.13 us                                                                | 2.17 us: 1.02x slower                                                   |
| generators              | 27.2 ms                                                                | 27.7 ms: 1.02x slower                                                   |
| meteor_contest          | 104 ms                                                                 | 106 ms: 1.02x slower                                                    |
| pyflate                 | 387 ms                                                                 | 395 ms: 1.02x slower                                                    |
| django_template         | 32.7 ms                                                                | 33.5 ms: 1.02x slower                                                   |
| telco                   | 156 ms                                                                 | 159 ms: 1.02x slower                                                    |
| logging_format          | 6.42 us                                                                | 6.59 us: 1.03x slower                                                   |
| sphinx                  | 960 ms                                                                 | 986 ms: 1.03x slower                                                    |
| thrift                  | 709 us                                                                 | 728 us: 1.03x slower                                                    |
| regex_v8                | 21.2 ms                                                                | 21.8 ms: 1.03x slower                                                   |
| sqlglot_v2_transpile    | 1.46 ms                                                                | 1.51 ms: 1.03x slower                                                   |
| docutils                | 2.53 sec                                                               | 2.61 sec: 1.03x slower                                                  |
| many_optionals          | 1.24 ms                                                                | 1.28 ms: 1.03x slower                                                   |
| genshi_xml              | 46.9 ms                                                                | 48.6 ms: 1.04x slower                                                   |
| genshi_text             | 19.3 ms                                                                | 20.0 ms: 1.04x slower                                                   |
| sqlglot_v2_parse        | 1.16 ms                                                                | 1.21 ms: 1.04x slower                                                   |
| sqlglot_v2_optimize     | 48.5 ms                                                                | 50.4 ms: 1.04x slower                                                   |
| sympy_sum               | 148 ms                                                                 | 155 ms: 1.04x slower                                                    |
| logging_simple          | 5.66 us                                                                | 5.93 us: 1.05x slower                                                   |
| sympy_expand            | 453 ms                                                                 | 477 ms: 1.05x slower                                                    |
| subparsers              | 44.8 ms                                                                | 47.2 ms: 1.05x slower                                                   |
| nqueens                 | 75.8 ms                                                                | 80.1 ms: 1.06x slower                                                   |
| hexiom                  | 5.49 ms                                                                | 5.81 ms: 1.06x slower                                                   |
| sympy_str               | 263 ms                                                                 | 279 ms: 1.06x slower                                                    |
| sqlglot_v2_normalize    | 97.1 ms                                                                | 103 ms: 1.06x slower                                                    |
| chaos                   | 49.9 ms                                                                | 53.1 ms: 1.06x slower                                                   |
| mdp                     | 1.11 sec                                                               | 1.18 sec: 1.06x slower                                                  |
| dulwich_log             | 68.4 ms                                                                | 73.6 ms: 1.08x slower                                                   |
| nbody                   | 92.3 ms                                                                | 99.8 ms: 1.08x slower                                                   |
| html5lib                | 58.3 ms                                                                | 63.7 ms: 1.09x slower                                                   |
| pycparser               | 1.06 sec                                                               | 1.19 sec: 1.12x slower                                                  |
| raytrace                | 235 ms                                                                 | 266 ms: 1.13x slower                                                    |
| pathlib                 | 17.0 ms                                                                | 19.4 ms: 1.14x slower                                                   |
| regex_compile           | 121 ms                                                                 | 138 ms: 1.14x slower                                                    |
| tomli_loads             | 1.70 sec                                                               | 1.97 sec: 1.16x slower                                                  |
| go                      | 99.8 ms                                                                | 120 ms: 1.20x slower                                                    |
| Geometric mean          | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (17): xml_etree_iterparse, bench_thread_pool, asyncio_websockets, pidigits, async_generators, bench_mp_pool, async_tree_cpu_io_mixed_tg, k_core, typing_runtime_protocols, async_tree_io_tg, xml_etree_process, create_gc_cycles, gc_traversal, async_tree_io, async_tree_memoization_tg, async_tree_none, pylint

- Geometric mean (including insignificant results): 1.006x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x