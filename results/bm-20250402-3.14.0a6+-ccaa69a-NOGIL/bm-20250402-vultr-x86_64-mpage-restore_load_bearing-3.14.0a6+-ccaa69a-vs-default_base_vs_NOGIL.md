# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.075x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 289 ms: 1.13x slower                                                  |
| docutils       | 2.59 sec                                                               | 2.77 sec: 1.07x slower                                                |
| sphinx         | 1.00 sec                                                               | 1.10 sec: 1.09x slower                                                |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 630 ms                                                                 | 535 ms: 1.18x faster                                                  |
| async_tree_none_tg         | 269 ms                                                                 | 232 ms: 1.16x faster                                                  |
| async_tree_memoization_tg  | 331 ms                                                                 | 292 ms: 1.14x faster                                                  |
| async_tree_io              | 629 ms                                                                 | 564 ms: 1.12x faster                                                  |
| async_tree_none            | 283 ms                                                                 | 268 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 510 ms                                                                 | 482 ms: 1.06x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| async_tree_memoization     | 324 ms                                                                 | 322 ms: 1.01x faster                                                  |
| async_generators           | 340 ms                                                                 | 365 ms: 1.07x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 71.6 ms                                                                | 70.0 ms: 1.02x faster                                                 |
| pidigits       | 198 ms                                                                 | 195 ms: 1.01x faster                                                  |
| nbody          | 94.7 ms                                                                | 113 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                                | 21.6 ms: 1.02x faster                                                 |
| regex_effbot   | 2.68 ms                                                                | 2.83 ms: 1.05x slower                                                 |
| regex_dna      | 172 ms                                                                 | 182 ms: 1.06x slower                                                  |
| regex_compile  | 132 ms                                                                 | 152 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.0 ms                                                                | 87.3 ms: 1.08x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 129 ms: 1.01x faster                                                  |
| pickle_pure_python   | 319 us                                                                 | 343 us: 1.07x slower                                                  |
| unpickle_pure_python | 223 us                                                                 | 240 us: 1.08x slower                                                  |
| tomli_loads          | 2.03 sec                                                               | 2.23 sec: 1.10x slower                                                |
| xml_etree_generate   | 85.9 ms                                                                | 95.5 ms: 1.11x slower                                                 |
| xml_etree_process    | 61.3 ms                                                                | 69.3 ms: 1.13x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 12.8 ms: 1.13x slower                                                 |
| json_loads           | 27.1 us                                                                | 30.7 us: 1.13x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                | 15.9 ms: 1.05x slower                                                 |
| python_startup_no_site | 8.71 ms                                                                | 11.2 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 36.9 ms                                                                | 40.8 ms: 1.11x slower                                                 |
| genshi_xml      | 51.3 ms                                                                | 57.6 ms: 1.12x slower                                                 |
| genshi_text     | 22.3 ms                                                                | 26.5 ms: 1.19x slower                                                 |
| mako            | 12.2 ms                                                                | 15.5 ms: 1.27x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.17x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.21 ms                                                                | 1.78 ms: 2.37x faster                                                 |
| create_gc_cycles           | 1.85 ms                                                                | 1.35 ms: 1.38x faster                                                 |
| async_tree_io_tg           | 630 ms                                                                 | 535 ms: 1.18x faster                                                  |
| async_tree_none_tg         | 269 ms                                                                 | 232 ms: 1.16x faster                                                  |
| async_tree_memoization_tg  | 331 ms                                                                 | 292 ms: 1.14x faster                                                  |
| async_tree_io              | 629 ms                                                                 | 564 ms: 1.12x faster                                                  |
| xml_etree_iterparse        | 94.0 ms                                                                | 87.3 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.18 us                                                                | 2.03 us: 1.07x faster                                                 |
| async_tree_none            | 283 ms                                                                 | 268 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 510 ms                                                                 | 482 ms: 1.06x faster                                                  |
| pathlib                    | 19.8 ms                                                                | 19.2 ms: 1.03x faster                                                 |
| float                      | 71.6 ms                                                                | 70.0 ms: 1.02x faster                                                 |
| regex_v8                   | 22.0 ms                                                                | 21.6 ms: 1.02x faster                                                 |
| pidigits                   | 198 ms                                                                 | 195 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| xml_etree_parse            | 129 ms                                                                 | 129 ms: 1.01x faster                                                  |
| async_tree_memoization     | 324 ms                                                                 | 322 ms: 1.01x faster                                                  |
| pycparser                  | 1.14 sec                                                               | 1.17 sec: 1.03x slower                                                |
| generators                 | 31.1 ms                                                                | 32.1 ms: 1.03x slower                                                 |
| python_startup             | 15.1 ms                                                                | 15.9 ms: 1.05x slower                                                 |
| regex_effbot               | 2.68 ms                                                                | 2.83 ms: 1.05x slower                                                 |
| bpe_tokeniser              | 4.34 sec                                                               | 4.58 sec: 1.06x slower                                                |
| regex_dna                  | 172 ms                                                                 | 182 ms: 1.06x slower                                                  |
| scimark_fft                | 326 ms                                                                 | 347 ms: 1.06x slower                                                  |
| dulwich_log                | 68.8 ms                                                                | 73.5 ms: 1.07x slower                                                 |
| docutils                   | 2.59 sec                                                               | 2.77 sec: 1.07x slower                                                |
| async_generators           | 340 ms                                                                 | 365 ms: 1.07x slower                                                  |
| pickle_pure_python         | 319 us                                                                 | 343 us: 1.07x slower                                                  |
| bench_mp_pool              | 89.4 ms                                                                | 96.2 ms: 1.08x slower                                                 |
| unpickle_pure_python       | 223 us                                                                 | 240 us: 1.08x slower                                                  |
| json                       | 4.85 ms                                                                | 5.25 ms: 1.08x slower                                                 |
| sqlglot_v2_normalize       | 109 ms                                                                 | 119 ms: 1.08x slower                                                  |
| spectral_norm              | 97.5 ms                                                                | 106 ms: 1.09x slower                                                  |
| pprint_safe_repr           | 738 ms                                                                 | 802 ms: 1.09x slower                                                  |
| scimark_sparse_mat_mult    | 4.61 ms                                                                | 5.01 ms: 1.09x slower                                                 |
| scimark_sor                | 116 ms                                                                 | 126 ms: 1.09x slower                                                  |
| sphinx                     | 1.00 sec                                                               | 1.10 sec: 1.09x slower                                                |
| k_core                     | 2.06 sec                                                               | 2.26 sec: 1.09x slower                                                |
| pylint                     | 288 ms                                                                 | 315 ms: 1.09x slower                                                  |
| logging_silent             | 102 ns                                                                 | 112 ns: 1.10x slower                                                  |
| tomli_loads                | 2.03 sec                                                               | 2.23 sec: 1.10x slower                                                |
| many_optionals             | 1.05 ms                                                                | 1.15 ms: 1.10x slower                                                 |
| nqueens                    | 81.7 ms                                                                | 90.4 ms: 1.11x slower                                                 |
| django_template            | 36.9 ms                                                                | 40.8 ms: 1.11x slower                                                 |
| sqlglot_v2_optimize        | 54.3 ms                                                                | 60.1 ms: 1.11x slower                                                 |
| scimark_lu                 | 119 ms                                                                 | 132 ms: 1.11x slower                                                  |
| deepcopy_reduce            | 2.73 us                                                                | 3.04 us: 1.11x slower                                                 |
| xml_etree_generate         | 85.9 ms                                                                | 95.5 ms: 1.11x slower                                                 |
| deltablue                  | 3.34 ms                                                                | 3.72 ms: 1.11x slower                                                 |
| pprint_pformat             | 1.51 sec                                                               | 1.68 sec: 1.12x slower                                                |
| pyflate                    | 421 ms                                                                 | 471 ms: 1.12x slower                                                  |
| subparsers                 | 22.9 ms                                                                | 25.7 ms: 1.12x slower                                                 |
| genshi_xml                 | 51.3 ms                                                                | 57.6 ms: 1.12x slower                                                 |
| xml_etree_process          | 61.3 ms                                                                | 69.3 ms: 1.13x slower                                                 |
| 2to3                       | 256 ms                                                                 | 289 ms: 1.13x slower                                                  |
| json_dumps                 | 11.3 ms                                                                | 12.8 ms: 1.13x slower                                                 |
| json_loads                 | 27.1 us                                                                | 30.7 us: 1.13x slower                                                 |
| mdp                        | 1.19 sec                                                               | 1.35 sec: 1.13x slower                                                |
| chaos                      | 56.3 ms                                                                | 63.9 ms: 1.14x slower                                                 |
| sympy_expand               | 477 ms                                                                 | 544 ms: 1.14x slower                                                  |
| deepcopy                   | 261 us                                                                 | 298 us: 1.14x slower                                                  |
| go                         | 116 ms                                                                 | 133 ms: 1.15x slower                                                  |
| telco                      | 7.46 ms                                                                | 8.58 ms: 1.15x slower                                                 |
| hexiom                     | 6.18 ms                                                                | 7.11 ms: 1.15x slower                                                 |
| sympy_sum                  | 161 ms                                                                 | 186 ms: 1.15x slower                                                  |
| logging_simple             | 6.23 us                                                                | 7.18 us: 1.15x slower                                                 |
| regex_compile              | 132 ms                                                                 | 152 ms: 1.15x slower                                                  |
| sqlglot_v2_transpile       | 1.59 ms                                                                | 1.84 ms: 1.15x slower                                                 |
| comprehensions             | 17.4 us                                                                | 20.2 us: 1.16x slower                                                 |
| raytrace                   | 260 ms                                                                 | 302 ms: 1.16x slower                                                  |
| sympy_integrate            | 19.8 ms                                                                | 23.1 ms: 1.17x slower                                                 |
| sympy_str                  | 282 ms                                                                 | 331 ms: 1.17x slower                                                  |
| fannkuch                   | 393 ms                                                                 | 461 ms: 1.17x slower                                                  |
| logging_format             | 6.91 us                                                                | 8.16 us: 1.18x slower                                                 |
| sqlalchemy_imperative      | 20.5 ms                                                                | 24.2 ms: 1.18x slower                                                 |
| sqlglot_v2_parse           | 1.28 ms                                                                | 1.52 ms: 1.19x slower                                                 |
| genshi_text                | 22.3 ms                                                                | 26.5 ms: 1.19x slower                                                 |
| sqlalchemy_declarative     | 133 ms                                                                 | 158 ms: 1.19x slower                                                  |
| scimark_monte_carlo        | 63.5 ms                                                                | 75.6 ms: 1.19x slower                                                 |
| nbody                      | 94.7 ms                                                                | 113 ms: 1.20x slower                                                  |
| richards                   | 44.6 ms                                                                | 53.7 ms: 1.21x slower                                                 |
| shortest_path              | 442 ms                                                                 | 536 ms: 1.21x slower                                                  |
| richards_super             | 50.7 ms                                                                | 61.5 ms: 1.21x slower                                                 |
| connected_components       | 401 ms                                                                 | 489 ms: 1.22x slower                                                  |
| deepcopy_memo              | 30.0 us                                                                | 36.6 us: 1.22x slower                                                 |
| crypto_pyaes               | 70.2 ms                                                                | 85.8 ms: 1.22x slower                                                 |
| typing_runtime_protocols   | 159 us                                                                 | 197 us: 1.24x slower                                                  |
| mako                       | 12.2 ms                                                                | 15.5 ms: 1.27x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 129 ms: 1.27x slower                                                  |
| python_startup_no_site     | 8.71 ms                                                                | 11.2 ms: 1.28x slower                                                 |
| coverage                   | 80.1 ms                                                                | 113 ms: 1.41x slower                                                  |
| bench_thread_pool          | 1.06 ms                                                                | 3.15 ms: 2.98x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, asyncio_websockets
Ignored benchmarks (1) of results/bm-20250402-3.14.0a6+-ccaa69a-NOGIL/bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a.json: html5lib

- Geometric mean (including insignificant results): 1.075x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x