# Results vs. base

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20240906-3.14.0a0-ef4b69d/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json | results/bm-20240906-3.14.0a0-ef4b69d-NOGIL/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 451 ms                                                                                                          | 719 ms: 1.59x slower                                                                                                  |
| docutils       | 4.22 sec                                                                                                        | 4.96 sec: 1.18x slower                                                                                                |
| html5lib       | 94.5 ms                                                                                                         | 139 ms: 1.47x slower                                                                                                  |
| tornado_http   | 263 ms                                                                                                          | 350 ms: 1.33x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.38x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | results/bm-20240906-3.14.0a0-ef4b69d/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json | results/bm-20240906-3.14.0a0-ef4b69d-NOGIL/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json |
|-------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg        | 1.33 sec                                                                                                        | 1.17 sec: 1.13x faster                                                                                                |
| async_tree_io           | 1.42 sec                                                                                                        | 1.34 sec: 1.06x faster                                                                                                |
| asyncio_websockets      | 781 ms                                                                                                          | 747 ms: 1.05x faster                                                                                                  |
| async_tree_none_tg      | 494 ms                                                                                                          | 514 ms: 1.04x slower                                                                                                  |
| async_tree_cpu_io_mixed | 893 ms                                                                                                          | 952 ms: 1.07x slower                                                                                                  |
| async_tree_memoization  | 647 ms                                                                                                          | 747 ms: 1.15x slower                                                                                                  |
| async_tree_none         | 523 ms                                                                                                          | 610 ms: 1.17x slower                                                                                                  |
| asyncio_tcp_ssl         | 2.90 sec                                                                                                        | 3.56 sec: 1.23x slower                                                                                                |
| async_generators        | 591 ms                                                                                                          | 734 ms: 1.24x slower                                                                                                  |
| asyncio_tcp             | 972 ms                                                                                                          | 1.22 sec: 1.25x slower                                                                                                |
| coroutines              | 29.9 ms                                                                                                         | 41.7 ms: 1.40x slower                                                                                                 |
| Geometric mean          | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20240906-3.14.0a0-ef4b69d/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json | results/bm-20240906-3.14.0a0-ef4b69d-NOGIL/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 125 ms                                                                                                          | 204 ms: 1.63x slower                                                                                                  |
| nbody          | 129 ms                                                                                                          | 300 ms: 2.33x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.55x slower                                                                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20240906-3.14.0a0-ef4b69d/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json | results/bm-20240906-3.14.0a0-ef4b69d-NOGIL/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 5.19 ms                                                                                                         | 4.86 ms: 1.07x faster                                                                                                 |
| regex_dna      | 310 ms                                                                                                          | 294 ms: 1.05x faster                                                                                                  |
| regex_compile  | 189 ms                                                                                                          | 284 ms: 1.50x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20240906-3.14.0a0-ef4b69d/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json | results/bm-20240906-3.14.0a0-ef4b69d-NOGIL/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 253 ms                                                                                                          | 215 ms: 1.18x faster                                                                                                  |
| pickle_dict          | 45.7 us                                                                                                         | 40.9 us: 1.12x faster                                                                                                 |
| pickle_list          | 7.25 us                                                                                                         | 6.59 us: 1.10x faster                                                                                                 |
| xml_etree_iterparse  | 182 ms                                                                                                          | 171 ms: 1.06x faster                                                                                                  |
| unpickle             | 20.6 us                                                                                                         | 21.8 us: 1.05x slower                                                                                                 |
| json_loads           | 37.8 us                                                                                                         | 44.0 us: 1.16x slower                                                                                                 |
| json_dumps           | 15.4 ms                                                                                                         | 18.1 ms: 1.17x slower                                                                                                 |
| xml_etree_generate   | 128 ms                                                                                                          | 163 ms: 1.27x slower                                                                                                  |
| xml_etree_process    | 86.8 ms                                                                                                         | 128 ms: 1.47x slower                                                                                                  |
| tomli_loads          | 2.72 sec                                                                                                        | 4.30 sec: 1.58x slower                                                                                                |
| unpickle_pure_python | 299 us                                                                                                          | 550 us: 1.84x slower                                                                                                  |
| pickle_pure_python   | 418 us                                                                                                          | 870 us: 2.08x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                           | 1.18x slower                                                                                                          |

Benchmark hidden because not significant (2): pickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20240906-3.14.0a0-ef4b69d/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json | results/bm-20240906-3.14.0a0-ef4b69d-NOGIL/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 17.7 ms                                                                                                         | 21.5 ms: 1.21x slower                                                                                                 |
| python_startup         | 26.1 ms                                                                                                         | 32.8 ms: 1.26x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.24x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20240906-3.14.0a0-ef4b69d/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json | results/bm-20240906-3.14.0a0-ef4b69d-NOGIL/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 18.5 ms                                                                                                         | 30.1 ms: 1.63x slower                                                                                                 |
| genshi_text     | 31.2 ms                                                                                                         | 55.1 ms: 1.77x slower                                                                                                 |
| genshi_xml      | 72.3 ms                                                                                                         | 129 ms: 1.79x slower                                                                                                  |
| django_template | 46.7 ms                                                                                                         | 85.9 ms: 1.84x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.75x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                | results/bm-20240906-3.14.0a0-ef4b69d/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json | results/bm-20240906-3.14.0a0-ef4b69d-NOGIL/bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d.json |
|--------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal             | 6.19 ms                                                                                                         | 4.60 ms: 1.34x faster                                                                                                 |
| create_gc_cycles         | 2.70 ms                                                                                                         | 2.12 ms: 1.27x faster                                                                                                 |
| xml_etree_parse          | 253 ms                                                                                                          | 215 ms: 1.18x faster                                                                                                  |
| async_tree_io_tg         | 1.33 sec                                                                                                        | 1.17 sec: 1.13x faster                                                                                                |
| pickle_dict              | 45.7 us                                                                                                         | 40.9 us: 1.12x faster                                                                                                 |
| pickle_list              | 7.25 us                                                                                                         | 6.59 us: 1.10x faster                                                                                                 |
| regex_effbot             | 5.19 ms                                                                                                         | 4.86 ms: 1.07x faster                                                                                                 |
| xml_etree_iterparse      | 182 ms                                                                                                          | 171 ms: 1.06x faster                                                                                                  |
| async_tree_io            | 1.42 sec                                                                                                        | 1.34 sec: 1.06x faster                                                                                                |
| regex_dna                | 310 ms                                                                                                          | 294 ms: 1.05x faster                                                                                                  |
| asyncio_websockets       | 781 ms                                                                                                          | 747 ms: 1.05x faster                                                                                                  |
| async_tree_none_tg       | 494 ms                                                                                                          | 514 ms: 1.04x slower                                                                                                  |
| unpickle                 | 20.6 us                                                                                                         | 21.8 us: 1.05x slower                                                                                                 |
| async_tree_cpu_io_mixed  | 893 ms                                                                                                          | 952 ms: 1.07x slower                                                                                                  |
| json                     | 7.18 ms                                                                                                         | 8.10 ms: 1.13x slower                                                                                                 |
| sqlite_synth             | 4.03 us                                                                                                         | 4.60 us: 1.14x slower                                                                                                 |
| async_tree_memoization   | 647 ms                                                                                                          | 747 ms: 1.15x slower                                                                                                  |
| json_loads               | 37.8 us                                                                                                         | 44.0 us: 1.16x slower                                                                                                 |
| async_tree_none          | 523 ms                                                                                                          | 610 ms: 1.17x slower                                                                                                  |
| json_dumps               | 15.4 ms                                                                                                         | 18.1 ms: 1.17x slower                                                                                                 |
| docutils                 | 4.22 sec                                                                                                        | 4.96 sec: 1.18x slower                                                                                                |
| python_startup_no_site   | 17.7 ms                                                                                                         | 21.5 ms: 1.21x slower                                                                                                 |
| pathlib                  | 30.6 ms                                                                                                         | 37.2 ms: 1.22x slower                                                                                                 |
| pycparser                | 1.79 sec                                                                                                        | 2.18 sec: 1.22x slower                                                                                                |
| asyncio_tcp_ssl          | 2.90 sec                                                                                                        | 3.56 sec: 1.23x slower                                                                                                |
| pylint                   | 508 ms                                                                                                          | 625 ms: 1.23x slower                                                                                                  |
| async_generators         | 591 ms                                                                                                          | 734 ms: 1.24x slower                                                                                                  |
| asyncio_tcp              | 972 ms                                                                                                          | 1.22 sec: 1.25x slower                                                                                                |
| python_startup           | 26.1 ms                                                                                                         | 32.8 ms: 1.26x slower                                                                                                 |
| xml_etree_generate       | 128 ms                                                                                                          | 163 ms: 1.27x slower                                                                                                  |
| telco                    | 11.5 ms                                                                                                         | 14.7 ms: 1.27x slower                                                                                                 |
| coverage                 | 121 ms                                                                                                          | 157 ms: 1.29x slower                                                                                                  |
| meteor_contest           | 153 ms                                                                                                          | 199 ms: 1.30x slower                                                                                                  |
| mdp                      | 3.93 sec                                                                                                        | 5.18 sec: 1.32x slower                                                                                                |
| generators               | 41.1 ms                                                                                                         | 54.6 ms: 1.33x slower                                                                                                 |
| tornado_http             | 263 ms                                                                                                          | 350 ms: 1.33x slower                                                                                                  |
| scimark_fft              | 470 ms                                                                                                          | 652 ms: 1.39x slower                                                                                                  |
| coroutines               | 29.9 ms                                                                                                         | 41.7 ms: 1.40x slower                                                                                                 |
| bench_thread_pool        | 3.89 ms                                                                                                         | 5.45 ms: 1.40x slower                                                                                                 |
| dulwich_log              | 108 ms                                                                                                          | 152 ms: 1.41x slower                                                                                                  |
| scimark_sparse_mat_mult  | 6.13 ms                                                                                                         | 8.80 ms: 1.43x slower                                                                                                 |
| thrift                   | 1.17 ms                                                                                                         | 1.70 ms: 1.46x slower                                                                                                 |
| deepcopy_reduce          | 4.09 us                                                                                                         | 5.97 us: 1.46x slower                                                                                                 |
| pyflate                  | 735 ms                                                                                                          | 1.08 sec: 1.46x slower                                                                                                |
| html5lib                 | 94.5 ms                                                                                                         | 139 ms: 1.47x slower                                                                                                  |
| fannkuch                 | 565 ms                                                                                                          | 831 ms: 1.47x slower                                                                                                  |
| xml_etree_process        | 86.8 ms                                                                                                         | 128 ms: 1.47x slower                                                                                                  |
| regex_compile            | 189 ms                                                                                                          | 284 ms: 1.50x slower                                                                                                  |
| typing_runtime_protocols | 231 us                                                                                                          | 353 us: 1.53x slower                                                                                                  |
| nqueens                  | 114 ms                                                                                                          | 174 ms: 1.53x slower                                                                                                  |
| spectral_norm            | 161 ms                                                                                                          | 249 ms: 1.55x slower                                                                                                  |
| deepcopy                 | 362 us                                                                                                          | 568 us: 1.57x slower                                                                                                  |
| sqlglot_normalize        | 152 ms                                                                                                          | 240 ms: 1.58x slower                                                                                                  |
| tomli_loads              | 2.72 sec                                                                                                        | 4.30 sec: 1.58x slower                                                                                                |
| 2to3                     | 451 ms                                                                                                          | 719 ms: 1.59x slower                                                                                                  |
| bpe_tokeniser            | 6.41 sec                                                                                                        | 10.2 sec: 1.60x slower                                                                                                |
| logging_format           | 9.69 us                                                                                                         | 15.5 us: 1.60x slower                                                                                                 |
| sympy_integrate          | 29.9 ms                                                                                                         | 48.3 ms: 1.62x slower                                                                                                 |
| mako                     | 18.5 ms                                                                                                         | 30.1 ms: 1.63x slower                                                                                                 |
| crypto_pyaes             | 95.7 ms                                                                                                         | 156 ms: 1.63x slower                                                                                                  |
| float                    | 125 ms                                                                                                          | 204 ms: 1.63x slower                                                                                                  |
| pprint_safe_repr         | 1.00 sec                                                                                                        | 1.68 sec: 1.68x slower                                                                                                |
| comprehensions           | 22.1 us                                                                                                         | 37.3 us: 1.69x slower                                                                                                 |
| sqlglot_optimize         | 76.7 ms                                                                                                         | 130 ms: 1.70x slower                                                                                                  |
| deepcopy_memo            | 39.5 us                                                                                                         | 67.4 us: 1.71x slower                                                                                                 |
| sympy_str                | 402 ms                                                                                                          | 696 ms: 1.73x slower                                                                                                  |
| richards                 | 66.0 ms                                                                                                         | 114 ms: 1.73x slower                                                                                                  |
| richards_super           | 71.0 ms                                                                                                         | 123 ms: 1.74x slower                                                                                                  |
| pprint_pformat           | 1.99 sec                                                                                                        | 3.48 sec: 1.75x slower                                                                                                |
| genshi_text              | 31.2 ms                                                                                                         | 55.1 ms: 1.77x slower                                                                                                 |
| hexiom                   | 9.21 ms                                                                                                         | 16.4 ms: 1.78x slower                                                                                                 |
| genshi_xml               | 72.3 ms                                                                                                         | 129 ms: 1.79x slower                                                                                                  |
| scimark_monte_carlo      | 89.4 ms                                                                                                         | 160 ms: 1.79x slower                                                                                                  |
| logging_silent           | 143 ns                                                                                                          | 260 ns: 1.81x slower                                                                                                  |
| django_template          | 46.7 ms                                                                                                         | 85.9 ms: 1.84x slower                                                                                                 |
| unpickle_pure_python     | 299 us                                                                                                          | 550 us: 1.84x slower                                                                                                  |
| sqlglot_transpile        | 2.28 ms                                                                                                         | 4.43 ms: 1.94x slower                                                                                                 |
| scimark_sor              | 172 ms                                                                                                          | 340 ms: 1.98x slower                                                                                                  |
| sqlglot_parse            | 1.87 ms                                                                                                         | 3.72 ms: 1.99x slower                                                                                                 |
| scimark_lu               | 149 ms                                                                                                          | 305 ms: 2.05x slower                                                                                                  |
| logging_simple           | 8.60 us                                                                                                         | 17.7 us: 2.06x slower                                                                                                 |
| pickle_pure_python       | 418 us                                                                                                          | 870 us: 2.08x slower                                                                                                  |
| raytrace                 | 358 ms                                                                                                          | 751 ms: 2.10x slower                                                                                                  |
| sympy_expand             | 635 ms                                                                                                          | 1.33 sec: 2.10x slower                                                                                                |
| chaos                    | 83.6 ms                                                                                                         | 176 ms: 2.11x slower                                                                                                  |
| go                       | 168 ms                                                                                                          | 361 ms: 2.15x slower                                                                                                  |
| sympy_sum                | 211 ms                                                                                                          | 492 ms: 2.33x slower                                                                                                  |
| nbody                    | 129 ms                                                                                                          | 300 ms: 2.33x slower                                                                                                  |
| deltablue                | 4.79 ms                                                                                                         | 11.3 ms: 2.37x slower                                                                                                 |
| unpack_sequence          | 72.4 ns                                                                                                         | 180 ns: 2.48x slower                                                                                                  |
| Geometric mean           | (ref)                                                                                                           | 1.40x slower                                                                                                          |

Benchmark hidden because not significant (7): bench_mp_pool, pidigits, async_tree_cpu_io_mixed_tg, pickle, unpickle_list, async_tree_memoization_tg, regex_v8

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.14x