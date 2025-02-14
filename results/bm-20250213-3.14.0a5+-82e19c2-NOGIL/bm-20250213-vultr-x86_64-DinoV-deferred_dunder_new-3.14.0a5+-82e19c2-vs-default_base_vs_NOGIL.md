# Results vs. default_base_vs_NOGIL

- fork: DinoV
- ref: deferred_dunder_new
- machine: linux-x86_64
- commit hash: 82e19c2
- commit date: 2025-02-13
- overall geometric mean: 1.121x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 302 ms: 1.18x slower                                                 |
| docutils       | 2.57 sec                                                               | 2.77 sec: 1.08x slower                                               |
| sphinx         | 981 ms                                                                 | 1.10 sec: 1.12x slower                                               |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg        | 628 ms                                                                 | 578 ms: 1.09x faster                                                 |
| async_tree_io           | 622 ms                                                                 | 608 ms: 1.02x faster                                                 |
| async_tree_none_tg      | 265 ms                                                                 | 259 ms: 1.02x faster                                                 |
| asyncio_websockets      | 517 ms                                                                 | 514 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed | 514 ms                                                                 | 537 ms: 1.04x slower                                                 |
| coroutines              | 22.2 ms                                                                | 23.6 ms: 1.06x slower                                                |
| async_tree_none         | 269 ms                                                                 | 288 ms: 1.07x slower                                                 |
| async_tree_memoization  | 326 ms                                                                 | 354 ms: 1.08x slower                                                 |
| async_generators        | 326 ms                                                                 | 373 ms: 1.14x slower                                                 |
| Geometric mean          | (ref)                                                                  | 1.02x slower                                                         |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                 | 192 ms: 1.04x slower                                                 |
| float          | 72.5 ms                                                                | 76.4 ms: 1.05x slower                                                |
| nbody          | 91.6 ms                                                                | 133 ms: 1.46x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 24.3 ms                                                                | 23.7 ms: 1.03x faster                                                |
| regex_effbot   | 2.84 ms                                                                | 2.79 ms: 1.02x faster                                                |
| regex_dna      | 168 ms                                                                 | 181 ms: 1.08x slower                                                 |
| regex_compile  | 128 ms                                                                 | 152 ms: 1.19x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.5 ms                                                                | 88.1 ms: 1.04x faster                                                |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.01x slower                                                 |
| json_loads           | 28.9 us                                                                | 31.3 us: 1.08x slower                                                |
| json_dumps           | 11.4 ms                                                                | 12.7 ms: 1.11x slower                                                |
| pickle_pure_python   | 318 us                                                                 | 362 us: 1.14x slower                                                 |
| unpickle_pure_python | 220 us                                                                 | 252 us: 1.15x slower                                                 |
| xml_etree_generate   | 83.4 ms                                                                | 96.2 ms: 1.15x slower                                                |
| xml_etree_process    | 58.9 ms                                                                | 70.1 ms: 1.19x slower                                                |
| tomli_loads          | 1.95 sec                                                               | 2.35 sec: 1.21x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.3 ms: 1.04x slower                                                |
| python_startup_no_site | 7.48 ms                                                                | 9.59 ms: 1.28x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.15x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 34.6 ms                                                                | 42.0 ms: 1.22x slower                                                |
| genshi_xml      | 48.6 ms                                                                | 59.6 ms: 1.23x slower                                                |
| genshi_text     | 21.6 ms                                                                | 27.9 ms: 1.29x slower                                                |
| mako            | 11.7 ms                                                                | 15.9 ms: 1.36x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.27x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20250213-vultr-x86_64-python-05e89c34bd8389f87bd6-3.14.0a5+-05e89c3 | bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 4.43 ms                                                                | 1.75 ms: 2.54x faster                                                |
| create_gc_cycles         | 1.86 ms                                                                | 1.39 ms: 1.33x faster                                                |
| async_tree_io_tg         | 628 ms                                                                 | 578 ms: 1.09x faster                                                 |
| sqlite_synth             | 2.20 us                                                                | 2.03 us: 1.08x faster                                                |
| xml_etree_iterparse      | 91.5 ms                                                                | 88.1 ms: 1.04x faster                                                |
| regex_v8                 | 24.3 ms                                                                | 23.7 ms: 1.03x faster                                                |
| async_tree_io            | 622 ms                                                                 | 608 ms: 1.02x faster                                                 |
| async_tree_none_tg       | 265 ms                                                                 | 259 ms: 1.02x faster                                                 |
| regex_effbot             | 2.84 ms                                                                | 2.79 ms: 1.02x faster                                                |
| asyncio_websockets       | 517 ms                                                                 | 514 ms: 1.01x faster                                                 |
| xml_etree_parse          | 128 ms                                                                 | 129 ms: 1.01x slower                                                 |
| pathlib                  | 18.7 ms                                                                | 19.1 ms: 1.02x slower                                                |
| python_startup           | 14.7 ms                                                                | 15.3 ms: 1.04x slower                                                |
| pycparser                | 1.13 sec                                                               | 1.18 sec: 1.04x slower                                               |
| pidigits                 | 184 ms                                                                 | 192 ms: 1.04x slower                                                 |
| json                     | 5.15 ms                                                                | 5.38 ms: 1.04x slower                                                |
| async_tree_cpu_io_mixed  | 514 ms                                                                 | 537 ms: 1.04x slower                                                 |
| float                    | 72.5 ms                                                                | 76.4 ms: 1.05x slower                                                |
| coroutines               | 22.2 ms                                                                | 23.6 ms: 1.06x slower                                                |
| async_tree_none          | 269 ms                                                                 | 288 ms: 1.07x slower                                                 |
| bench_mp_pool            | 87.7 ms                                                                | 94.6 ms: 1.08x slower                                                |
| docutils                 | 2.57 sec                                                               | 2.77 sec: 1.08x slower                                               |
| regex_dna                | 168 ms                                                                 | 181 ms: 1.08x slower                                                 |
| json_loads               | 28.9 us                                                                | 31.3 us: 1.08x slower                                                |
| async_tree_memoization   | 326 ms                                                                 | 354 ms: 1.08x slower                                                 |
| dulwich_log              | 75.8 ms                                                                | 82.4 ms: 1.09x slower                                                |
| generators               | 29.9 ms                                                                | 32.5 ms: 1.09x slower                                                |
| logging_silent           | 105 ns                                                                 | 115 ns: 1.10x slower                                                 |
| bpe_tokeniser            | 4.22 sec                                                               | 4.66 sec: 1.10x slower                                               |
| json_dumps               | 11.4 ms                                                                | 12.7 ms: 1.11x slower                                                |
| mdp                      | 2.33 sec                                                               | 2.60 sec: 1.11x slower                                               |
| sphinx                   | 981 ms                                                                 | 1.10 sec: 1.12x slower                                               |
| scimark_sor              | 119 ms                                                                 | 134 ms: 1.12x slower                                                 |
| pylint                   | 279 ms                                                                 | 314 ms: 1.12x slower                                                 |
| k_core                   | 2.04 sec                                                               | 2.31 sec: 1.13x slower                                               |
| pickle_pure_python       | 318 us                                                                 | 362 us: 1.14x slower                                                 |
| async_generators         | 326 ms                                                                 | 373 ms: 1.14x slower                                                 |
| unpickle_pure_python     | 220 us                                                                 | 252 us: 1.15x slower                                                 |
| xml_etree_generate       | 83.4 ms                                                                | 96.2 ms: 1.15x slower                                                |
| subparsers               | 21.8 ms                                                                | 25.2 ms: 1.16x slower                                                |
| many_optionals           | 1.01 ms                                                                | 1.17 ms: 1.16x slower                                                |
| telco                    | 7.30 ms                                                                | 8.56 ms: 1.17x slower                                                |
| sqlglot_normalize        | 102 ms                                                                 | 120 ms: 1.18x slower                                                 |
| 2to3                     | 256 ms                                                                 | 302 ms: 1.18x slower                                                 |
| pprint_safe_repr         | 701 ms                                                                 | 830 ms: 1.18x slower                                                 |
| regex_compile            | 128 ms                                                                 | 152 ms: 1.19x slower                                                 |
| pprint_pformat           | 1.43 sec                                                               | 1.70 sec: 1.19x slower                                               |
| xml_etree_process        | 58.9 ms                                                                | 70.1 ms: 1.19x slower                                                |
| sqlglot_optimize         | 51.4 ms                                                                | 61.3 ms: 1.19x slower                                                |
| go                       | 119 ms                                                                 | 142 ms: 1.19x slower                                                 |
| tomli_loads              | 1.95 sec                                                               | 2.35 sec: 1.21x slower                                               |
| logging_simple           | 5.89 us                                                                | 7.12 us: 1.21x slower                                                |
| coverage                 | 80.1 ms                                                                | 96.8 ms: 1.21x slower                                                |
| sqlglot_transpile        | 1.59 ms                                                                | 1.93 ms: 1.21x slower                                                |
| sympy_sum                | 152 ms                                                                 | 184 ms: 1.21x slower                                                 |
| pyflate                  | 423 ms                                                                 | 512 ms: 1.21x slower                                                 |
| sympy_expand             | 450 ms                                                                 | 545 ms: 1.21x slower                                                 |
| thrift                   | 735 us                                                                 | 892 us: 1.21x slower                                                 |
| spectral_norm            | 91.6 ms                                                                | 111 ms: 1.21x slower                                                 |
| comprehensions           | 16.4 us                                                                | 19.9 us: 1.21x slower                                                |
| sqlalchemy_declarative   | 127 ms                                                                 | 155 ms: 1.21x slower                                                 |
| django_template          | 34.6 ms                                                                | 42.0 ms: 1.22x slower                                                |
| sympy_integrate          | 19.7 ms                                                                | 23.9 ms: 1.22x slower                                                |
| deepcopy_reduce          | 2.61 us                                                                | 3.19 us: 1.22x slower                                                |
| deepcopy                 | 252 us                                                                 | 307 us: 1.22x slower                                                 |
| logging_format           | 6.61 us                                                                | 8.10 us: 1.23x slower                                                |
| deltablue                | 3.22 ms                                                                | 3.94 ms: 1.23x slower                                                |
| genshi_xml               | 48.6 ms                                                                | 59.6 ms: 1.23x slower                                                |
| sqlalchemy_imperative    | 19.2 ms                                                                | 23.6 ms: 1.23x slower                                                |
| scimark_lu               | 114 ms                                                                 | 141 ms: 1.23x slower                                                 |
| hexiom                   | 6.01 ms                                                                | 7.42 ms: 1.23x slower                                                |
| nqueens                  | 79.5 ms                                                                | 98.3 ms: 1.24x slower                                                |
| sympy_str                | 269 ms                                                                 | 334 ms: 1.24x slower                                                 |
| sqlglot_parse            | 1.29 ms                                                                | 1.60 ms: 1.24x slower                                                |
| chaos                    | 56.5 ms                                                                | 70.3 ms: 1.24x slower                                                |
| raytrace                 | 265 ms                                                                 | 332 ms: 1.25x slower                                                 |
| scimark_fft              | 314 ms                                                                 | 394 ms: 1.25x slower                                                 |
| shortest_path            | 431 ms                                                                 | 545 ms: 1.26x slower                                                 |
| connected_components     | 388 ms                                                                 | 490 ms: 1.26x slower                                                 |
| richards                 | 43.8 ms                                                                | 55.5 ms: 1.27x slower                                                |
| scimark_monte_carlo      | 65.1 ms                                                                | 83.4 ms: 1.28x slower                                                |
| python_startup_no_site   | 7.48 ms                                                                | 9.59 ms: 1.28x slower                                                |
| crypto_pyaes             | 68.7 ms                                                                | 88.5 ms: 1.29x slower                                                |
| scimark_sparse_mat_mult  | 4.40 ms                                                                | 5.67 ms: 1.29x slower                                                |
| genshi_text              | 21.6 ms                                                                | 27.9 ms: 1.29x slower                                                |
| deepcopy_memo            | 30.3 us                                                                | 39.2 us: 1.29x slower                                                |
| typing_runtime_protocols | 155 us                                                                 | 200 us: 1.30x slower                                                 |
| meteor_contest           | 99.4 ms                                                                | 130 ms: 1.30x slower                                                 |
| richards_super           | 49.3 ms                                                                | 64.6 ms: 1.31x slower                                                |
| fannkuch                 | 380 ms                                                                 | 501 ms: 1.32x slower                                                 |
| mako                     | 11.7 ms                                                                | 15.9 ms: 1.36x slower                                                |
| nbody                    | 91.6 ms                                                                | 133 ms: 1.46x slower                                                 |
| bench_thread_pool        | 1.03 ms                                                                | 3.32 ms: 3.24x slower                                                |
| Geometric mean           | (ref)                                                                  | 1.15x slower                                                         |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg
Ignored benchmarks (1) of results/bm-20250213-3.14.0a5+-82e19c2-NOGIL/bm-20250213-vultr-x86_64-DinoV-deferred_dunder_new-3.14.0a5+-82e19c2.json: html5lib

- Geometric mean (including insignificant results): 1.121x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.20x