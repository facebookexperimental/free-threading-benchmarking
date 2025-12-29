# Results vs. base

- fork: Fidget-Spinner
- ref: jit_ft
- machine: darwin-arm64
- commit hash: 0678505
- commit date: 2025-12-28
- overall geometric mean: 1.084x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 125 ms                                                                   | 120 ms: 1.04x faster                                                 |
| docutils       | 1.03 sec                                                                 | 1.02 sec: 1.01x faster                                               |
| html5lib       | 23.9 ms                                                                  | 22.1 ms: 1.08x faster                                                |
| sphinx         | 433 ms                                                                   | 431 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                    | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_eager             | 48.1 ms                                                                  | 43.9 ms: 1.10x faster                                                |
| async_tree_none              | 117 ms                                                                   | 112 ms: 1.04x faster                                                 |
| async_tree_io                | 254 ms                                                                   | 247 ms: 1.03x faster                                                 |
| async_tree_none_tg           | 107 ms                                                                   | 104 ms: 1.03x faster                                                 |
| async_tree_eager_io          | 256 ms                                                                   | 249 ms: 1.03x faster                                                 |
| async_tree_memoization       | 153 ms                                                                   | 149 ms: 1.03x faster                                                 |
| async_tree_eager_memoization | 115 ms                                                                   | 112 ms: 1.03x faster                                                 |
| async_tree_eager_tg          | 95.2 ms                                                                  | 93.0 ms: 1.02x faster                                                |
| async_tree_io_tg             | 242 ms                                                                   | 237 ms: 1.02x faster                                                 |
| asyncio_websockets           | 190 ms                                                                   | 189 ms: 1.00x faster                                                 |
| coroutines                   | 10.6 ms                                                                  | 11.0 ms: 1.03x slower                                                |
| async_generators             | 189 ms                                                                   | 198 ms: 1.05x slower                                                 |
| Geometric mean               | (ref)                                                                    | 1.02x faster                                                         |

Benchmark hidden because not significant (7): async_tree_eager_io_tg, async_tree_memoization_tg, async_tree_eager_memoization_tg, async_tree_cpu_io_mixed, async_tree_eager_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_eager_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 58.2 ms                                                                  | 44.2 ms: 1.32x faster                                                |
| float          | 29.1 ms                                                                  | 23.0 ms: 1.26x faster                                                |
| pidigits       | 169 ms                                                                   | 167 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                    | 1.19x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 51.7 ms                                                                  | 45.6 ms: 1.13x faster                                                |
| regex_v8       | 9.35 ms                                                                  | 9.19 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                         |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 112 us                                                                   | 78.3 us: 1.43x faster                                                |
| pickle_pure_python   | 149 us                                                                   | 116 us: 1.28x faster                                                 |
| tomli_loads          | 1.02 sec                                                                 | 849 ms: 1.20x faster                                                 |
| xml_etree_process    | 27.6 ms                                                                  | 23.8 ms: 1.16x faster                                                |
| xml_etree_generate   | 37.7 ms                                                                  | 33.4 ms: 1.13x faster                                                |
| json_dumps           | 4.07 ms                                                                  | 3.72 ms: 1.09x faster                                                |
| xml_etree_iterparse  | 38.9 ms                                                                  | 36.7 ms: 1.06x faster                                                |
| json_loads           | 11.5 us                                                                  | 11.3 us: 1.02x faster                                                |
| xml_etree_parse      | 57.1 ms                                                                  | 58.8 ms: 1.03x slower                                                |
| Geometric mean       | (ref)                                                                    | 1.14x faster                                                         |

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 5.56 ms                                                                  | 4.74 ms: 1.17x faster                                                |
| django_template | 16.4 ms                                                                  | 15.3 ms: 1.07x faster                                                |
| genshi_text     | 11.7 ms                                                                  | 11.4 ms: 1.03x faster                                                |
| genshi_xml      | 24.2 ms                                                                  | 28.3 ms: 1.17x slower                                                |
| Geometric mean  | (ref)                                                                    | 1.03x faster                                                         |

All benchmarks:
===============

| Benchmark                    | bm-20251228-macm4pro-arm64-python-daa9aa4c0a8490f09b01-3.15.0a3+-daa9aa4 | bm-20251228-macm4pro-arm64-Fidget%2dSpinner-jit_ft-3.15.0a3+-0678505 |
|------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| richards                     | 23.6 ms                                                                  | 11.5 ms: 2.05x faster                                                |
| richards_super               | 27.1 ms                                                                  | 13.8 ms: 1.97x faster                                                |
| logging_silent               | 45.0 ns                                                                  | 31.4 ns: 1.43x faster                                                |
| unpickle_pure_python         | 112 us                                                                   | 78.3 us: 1.43x faster                                                |
| deltablue                    | 1.68 ms                                                                  | 1.20 ms: 1.40x faster                                                |
| scimark_lu                   | 57.9 ms                                                                  | 41.9 ms: 1.38x faster                                                |
| pyflate                      | 197 ms                                                                   | 148 ms: 1.33x faster                                                 |
| nbody                        | 58.2 ms                                                                  | 44.2 ms: 1.32x faster                                                |
| scimark_monte_carlo          | 32.9 ms                                                                  | 25.6 ms: 1.29x faster                                                |
| pickle_pure_python           | 149 us                                                                   | 116 us: 1.28x faster                                                 |
| float                        | 29.1 ms                                                                  | 23.0 ms: 1.26x faster                                                |
| scimark_sor                  | 55.8 ms                                                                  | 44.3 ms: 1.26x faster                                                |
| go                           | 61.2 ms                                                                  | 49.0 ms: 1.25x faster                                                |
| crypto_pyaes                 | 43.0 ms                                                                  | 34.8 ms: 1.23x faster                                                |
| tomli_loads                  | 1.02 sec                                                                 | 849 ms: 1.20x faster                                                 |
| pprint_safe_repr             | 338 ms                                                                   | 283 ms: 1.20x faster                                                 |
| pprint_pformat               | 688 ms                                                                   | 581 ms: 1.18x faster                                                 |
| mako                         | 5.56 ms                                                                  | 4.74 ms: 1.17x faster                                                |
| spectral_norm                | 51.4 ms                                                                  | 43.9 ms: 1.17x faster                                                |
| comprehensions               | 8.60 us                                                                  | 7.36 us: 1.17x faster                                                |
| chaos                        | 28.5 ms                                                                  | 24.4 ms: 1.17x faster                                                |
| xml_etree_process            | 27.6 ms                                                                  | 23.8 ms: 1.16x faster                                                |
| fannkuch                     | 175 ms                                                                   | 152 ms: 1.15x faster                                                 |
| scimark_fft                  | 127 ms                                                                   | 111 ms: 1.14x faster                                                 |
| regex_compile                | 51.7 ms                                                                  | 45.6 ms: 1.13x faster                                                |
| hexiom                       | 3.22 ms                                                                  | 2.85 ms: 1.13x faster                                                |
| xml_etree_generate           | 37.7 ms                                                                  | 33.4 ms: 1.13x faster                                                |
| sqlglot_v2_parse             | 590 us                                                                   | 523 us: 1.13x faster                                                 |
| bpe_tokeniser                | 2.02 sec                                                                 | 1.81 sec: 1.11x faster                                               |
| meteor_contest               | 57.1 ms                                                                  | 51.6 ms: 1.11x faster                                                |
| raytrace                     | 129 ms                                                                   | 117 ms: 1.10x faster                                                 |
| telco                        | 3.08 ms                                                                  | 2.80 ms: 1.10x faster                                                |
| async_tree_eager             | 48.1 ms                                                                  | 43.9 ms: 1.10x faster                                                |
| json_dumps                   | 4.07 ms                                                                  | 3.72 ms: 1.09x faster                                                |
| deepcopy_memo                | 12.7 us                                                                  | 11.6 us: 1.09x faster                                                |
| subparsers                   | 4.22 ms                                                                  | 3.88 ms: 1.09x faster                                                |
| sqlglot_v2_transpile         | 715 us                                                                   | 659 us: 1.09x faster                                                 |
| html5lib                     | 23.9 ms                                                                  | 22.1 ms: 1.08x faster                                                |
| django_template              | 16.4 ms                                                                  | 15.3 ms: 1.07x faster                                                |
| thrift                       | 339 us                                                                   | 319 us: 1.06x faster                                                 |
| pycparser                    | 477 ms                                                                   | 449 ms: 1.06x faster                                                 |
| xml_etree_iterparse          | 38.9 ms                                                                  | 36.7 ms: 1.06x faster                                                |
| deepcopy                     | 113 us                                                                   | 107 us: 1.06x faster                                                 |
| deepcopy_reduce              | 1.23 us                                                                  | 1.16 us: 1.06x faster                                                |
| nqueens                      | 45.9 ms                                                                  | 43.3 ms: 1.06x faster                                                |
| logging_simple               | 2.52 us                                                                  | 2.40 us: 1.05x faster                                                |
| logging_format               | 2.77 us                                                                  | 2.65 us: 1.05x faster                                                |
| k_core                       | 1.01 sec                                                                 | 963 ms: 1.05x faster                                                 |
| async_tree_none              | 117 ms                                                                   | 112 ms: 1.04x faster                                                 |
| json                         | 2.01 ms                                                                  | 1.93 ms: 1.04x faster                                                |
| 2to3                         | 125 ms                                                                   | 120 ms: 1.04x faster                                                 |
| connected_components         | 249 ms                                                                   | 239 ms: 1.04x faster                                                 |
| many_optionals               | 278 us                                                                   | 267 us: 1.04x faster                                                 |
| async_tree_io                | 254 ms                                                                   | 247 ms: 1.03x faster                                                 |
| async_tree_none_tg           | 107 ms                                                                   | 104 ms: 1.03x faster                                                 |
| genshi_text                  | 11.7 ms                                                                  | 11.4 ms: 1.03x faster                                                |
| async_tree_eager_io          | 256 ms                                                                   | 249 ms: 1.03x faster                                                 |
| async_tree_memoization       | 153 ms                                                                   | 149 ms: 1.03x faster                                                 |
| async_tree_eager_memoization | 115 ms                                                                   | 112 ms: 1.03x faster                                                 |
| shortest_path                | 257 ms                                                                   | 251 ms: 1.02x faster                                                 |
| async_tree_eager_tg          | 95.2 ms                                                                  | 93.0 ms: 1.02x faster                                                |
| async_tree_io_tg             | 242 ms                                                                   | 237 ms: 1.02x faster                                                 |
| json_loads                   | 11.5 us                                                                  | 11.3 us: 1.02x faster                                                |
| regex_v8                     | 9.35 ms                                                                  | 9.19 ms: 1.02x faster                                                |
| generators                   | 21.3 ms                                                                  | 21.0 ms: 1.01x faster                                                |
| typing_runtime_protocols     | 71.1 us                                                                  | 70.1 us: 1.01x faster                                                |
| sqlite_synth                 | 825 ns                                                                   | 814 ns: 1.01x faster                                                 |
| pidigits                     | 169 ms                                                                   | 167 ms: 1.01x faster                                                 |
| coverage                     | 40.0 ms                                                                  | 39.7 ms: 1.01x faster                                                |
| docutils                     | 1.03 sec                                                                 | 1.02 sec: 1.01x faster                                               |
| sphinx                       | 433 ms                                                                   | 431 ms: 1.01x faster                                                 |
| dulwich_log                  | 19.1 ms                                                                  | 19.0 ms: 1.00x faster                                                |
| asyncio_websockets           | 190 ms                                                                   | 189 ms: 1.00x faster                                                 |
| create_gc_cycles             | 512 us                                                                   | 514 us: 1.00x slower                                                 |
| bench_thread_pool            | 551 us                                                                   | 554 us: 1.01x slower                                                 |
| scimark_sparse_mat_mult      | 2.16 ms                                                                  | 2.18 ms: 1.01x slower                                                |
| sympy_sum                    | 63.2 ms                                                                  | 64.1 ms: 1.02x slower                                                |
| sympy_integrate              | 8.35 ms                                                                  | 8.49 ms: 1.02x slower                                                |
| sqlglot_v2_normalize         | 50.1 ms                                                                  | 51.0 ms: 1.02x slower                                                |
| sympy_expand                 | 192 ms                                                                   | 196 ms: 1.02x slower                                                 |
| xml_etree_parse              | 57.1 ms                                                                  | 58.8 ms: 1.03x slower                                                |
| coroutines                   | 10.6 ms                                                                  | 11.0 ms: 1.03x slower                                                |
| sympy_str                    | 113 ms                                                                   | 117 ms: 1.04x slower                                                 |
| async_generators             | 189 ms                                                                   | 198 ms: 1.05x slower                                                 |
| pylint                       | 122 ms                                                                   | 128 ms: 1.05x slower                                                 |
| mdp                          | 635 ms                                                                   | 673 ms: 1.06x slower                                                 |
| sqlglot_v2_optimize          | 24.7 ms                                                                  | 26.3 ms: 1.07x slower                                                |
| genshi_xml                   | 24.2 ms                                                                  | 28.3 ms: 1.17x slower                                                |
| Geometric mean               | (ref)                                                                    | 1.09x faster                                                         |

Benchmark hidden because not significant (14): async_tree_eager_io_tg, async_tree_memoization_tg, gc_traversal, async_tree_eager_memoization_tg, async_tree_cpu_io_mixed, regex_effbot, pathlib, bench_mp_pool, async_tree_eager_cpu_io_mixed, python_startup, python_startup_no_site, regex_dna, async_tree_cpu_io_mixed_tg, async_tree_eager_cpu_io_mixed_tg

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.03x