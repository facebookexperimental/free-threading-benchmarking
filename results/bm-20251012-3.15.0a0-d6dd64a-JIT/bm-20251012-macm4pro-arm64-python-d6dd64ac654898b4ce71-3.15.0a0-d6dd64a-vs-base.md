# Results vs. base

- fork: python
- ref: d6dd64ac654898b4ce71
- machine: darwin-arm64
- commit hash: d6dd64a
- commit date: 2025-10-12
- overall geometric mean: 1.019x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json | results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 113 ms                                                                                                            | 117 ms: 1.04x slower                                                                                                  |
| docutils       | 1.03 sec                                                                                                          | 1.05 sec: 1.02x slower                                                                                                |
| html5lib       | 23.6 ms                                                                                                           | 24.2 ms: 1.02x slower                                                                                                 |
| sphinx         | 403 ms                                                                                                            | 410 ms: 1.02x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json | results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json |
|-------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed | 222 ms                                                                                                            | 224 ms: 1.01x slower                                                                                                  |
| async_tree_memoization        | 148 ms                                                                                                            | 149 ms: 1.01x slower                                                                                                  |
| coroutines                    | 9.90 ms                                                                                                           | 10.1 ms: 1.02x slower                                                                                                 |
| async_tree_eager_memoization  | 109 ms                                                                                                            | 111 ms: 1.03x slower                                                                                                  |
| async_tree_eager_io           | 244 ms                                                                                                            | 251 ms: 1.03x slower                                                                                                  |
| async_tree_eager              | 40.3 ms                                                                                                           | 42.2 ms: 1.05x slower                                                                                                 |
| async_generators              | 173 ms                                                                                                            | 183 ms: 1.06x slower                                                                                                  |
| Geometric mean                | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (14): asyncio_tcp_ssl, async_tree_eager_cpu_io_mixed_tg, asyncio_websockets, async_tree_none_tg, async_tree_eager_io_tg, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_eager_memoization_tg, asyncio_tcp, async_tree_io, async_tree_eager_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json | results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 28.7 ms                                                                                                           | 31.4 ms: 1.09x slower                                                                                                 |
| nbody          | 47.6 ms                                                                                                           | 56.7 ms: 1.19x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json | results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 9.78 ms                                                                                                           | 9.69 ms: 1.01x faster                                                                                                 |
| regex_compile  | 46.4 ms                                                                                                           | 48.3 ms: 1.04x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json | results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 871 ms                                                                                                            | 825 ms: 1.06x faster                                                                                                  |
| xml_etree_process    | 25.2 ms                                                                                                           | 24.0 ms: 1.05x faster                                                                                                 |
| unpickle_pure_python | 97.3 us                                                                                                           | 93.6 us: 1.04x faster                                                                                                 |
| xml_etree_generate   | 35.0 ms                                                                                                           | 34.2 ms: 1.02x faster                                                                                                 |
| json_dumps           | 3.85 ms                                                                                                           | 3.81 ms: 1.01x faster                                                                                                 |
| unpickle_list        | 2.03 us                                                                                                           | 2.01 us: 1.01x faster                                                                                                 |
| pickle_dict          | 13.0 us                                                                                                           | 12.9 us: 1.00x faster                                                                                                 |
| json_loads           | 11.0 us                                                                                                           | 11.1 us: 1.01x slower                                                                                                 |
| xml_etree_parse      | 63.2 ms                                                                                                           | 63.9 ms: 1.01x slower                                                                                                 |
| xml_etree_iterparse  | 44.3 ms                                                                                                           | 44.7 ms: 1.01x slower                                                                                                 |
| unpickle             | 6.30 us                                                                                                           | 6.37 us: 1.01x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (3): pickle_pure_python, pickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json | results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 6.35 ms                                                                                                           | 6.40 ms: 1.01x slower                                                                                                 |
| python_startup         | 8.87 ms                                                                                                           | 8.95 ms: 1.01x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json | results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 4.71 ms                                                                                                           | 4.41 ms: 1.07x faster                                                                                                 |
| genshi_text     | 9.73 ms                                                                                                           | 10.0 ms: 1.03x slower                                                                                                 |
| django_template | 15.0 ms                                                                                                           | 15.7 ms: 1.04x slower                                                                                                 |
| genshi_xml      | 21.0 ms                                                                                                           | 22.1 ms: 1.05x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.01x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                     | results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json | results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-macm4pro-arm64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a.json |
|-------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pprint_safe_repr              | 316 ms                                                                                                            | 291 ms: 1.08x faster                                                                                                  |
| pprint_pformat                | 636 ms                                                                                                            | 592 ms: 1.07x faster                                                                                                  |
| mako                          | 4.71 ms                                                                                                           | 4.41 ms: 1.07x faster                                                                                                 |
| tomli_loads                   | 871 ms                                                                                                            | 825 ms: 1.06x faster                                                                                                  |
| telco                         | 2.84 ms                                                                                                           | 2.69 ms: 1.05x faster                                                                                                 |
| xml_etree_process             | 25.2 ms                                                                                                           | 24.0 ms: 1.05x faster                                                                                                 |
| unpickle_pure_python          | 97.3 us                                                                                                           | 93.6 us: 1.04x faster                                                                                                 |
| sqlite_synth                  | 962 ns                                                                                                            | 937 ns: 1.03x faster                                                                                                  |
| xml_etree_generate            | 35.0 ms                                                                                                           | 34.2 ms: 1.02x faster                                                                                                 |
| scimark_sor                   | 51.1 ms                                                                                                           | 50.2 ms: 1.02x faster                                                                                                 |
| fannkuch                      | 176 ms                                                                                                            | 173 ms: 1.02x faster                                                                                                  |
| generators                    | 18.2 ms                                                                                                           | 18.0 ms: 1.01x faster                                                                                                 |
| json_dumps                    | 3.85 ms                                                                                                           | 3.81 ms: 1.01x faster                                                                                                 |
| regex_v8                      | 9.78 ms                                                                                                           | 9.69 ms: 1.01x faster                                                                                                 |
| unpickle_list                 | 2.03 us                                                                                                           | 2.01 us: 1.01x faster                                                                                                 |
| pickle_dict                   | 13.0 us                                                                                                           | 12.9 us: 1.00x faster                                                                                                 |
| mdp                           | 543 ms                                                                                                            | 542 ms: 1.00x faster                                                                                                  |
| bench_mp_pool                 | 42.6 ms                                                                                                           | 42.9 ms: 1.01x slower                                                                                                 |
| json                          | 1.94 ms                                                                                                           | 1.95 ms: 1.01x slower                                                                                                 |
| async_tree_eager_cpu_io_mixed | 222 ms                                                                                                            | 224 ms: 1.01x slower                                                                                                  |
| async_tree_memoization        | 148 ms                                                                                                            | 149 ms: 1.01x slower                                                                                                  |
| python_startup_no_site        | 6.35 ms                                                                                                           | 6.40 ms: 1.01x slower                                                                                                 |
| python_startup                | 8.87 ms                                                                                                           | 8.95 ms: 1.01x slower                                                                                                 |
| subparsers                    | 17.8 ms                                                                                                           | 18.0 ms: 1.01x slower                                                                                                 |
| scimark_fft                   | 121 ms                                                                                                            | 122 ms: 1.01x slower                                                                                                  |
| json_loads                    | 11.0 us                                                                                                           | 11.1 us: 1.01x slower                                                                                                 |
| xml_etree_parse               | 63.2 ms                                                                                                           | 63.9 ms: 1.01x slower                                                                                                 |
| xml_etree_iterparse           | 44.3 ms                                                                                                           | 44.7 ms: 1.01x slower                                                                                                 |
| unpickle                      | 6.30 us                                                                                                           | 6.37 us: 1.01x slower                                                                                                 |
| bench_thread_pool             | 408 us                                                                                                            | 413 us: 1.01x slower                                                                                                  |
| coverage                      | 32.6 ms                                                                                                           | 33.0 ms: 1.01x slower                                                                                                 |
| sphinx                        | 403 ms                                                                                                            | 410 ms: 1.02x slower                                                                                                  |
| dulwich_log                   | 18.8 ms                                                                                                           | 19.2 ms: 1.02x slower                                                                                                 |
| meteor_contest                | 49.1 ms                                                                                                           | 49.9 ms: 1.02x slower                                                                                                 |
| docutils                      | 1.03 sec                                                                                                          | 1.05 sec: 1.02x slower                                                                                                |
| comprehensions                | 7.22 us                                                                                                           | 7.35 us: 1.02x slower                                                                                                 |
| create_gc_cycles              | 920 us                                                                                                            | 936 us: 1.02x slower                                                                                                  |
| logging_format                | 2.49 us                                                                                                           | 2.53 us: 1.02x slower                                                                                                 |
| coroutines                    | 9.90 ms                                                                                                           | 10.1 ms: 1.02x slower                                                                                                 |
| sympy_sum                     | 55.0 ms                                                                                                           | 56.1 ms: 1.02x slower                                                                                                 |
| logging_simple                | 2.27 us                                                                                                           | 2.32 us: 1.02x slower                                                                                                 |
| crypto_pyaes                  | 37.2 ms                                                                                                           | 38.0 ms: 1.02x slower                                                                                                 |
| thrift                        | 307 us                                                                                                            | 314 us: 1.02x slower                                                                                                  |
| html5lib                      | 23.6 ms                                                                                                           | 24.2 ms: 1.02x slower                                                                                                 |
| deepcopy_reduce               | 1.11 us                                                                                                           | 1.13 us: 1.02x slower                                                                                                 |
| async_tree_eager_memoization  | 109 ms                                                                                                            | 111 ms: 1.03x slower                                                                                                  |
| many_optionals                | 370 us                                                                                                            | 379 us: 1.03x slower                                                                                                  |
| bpe_tokeniser                 | 1.94 sec                                                                                                          | 1.99 sec: 1.03x slower                                                                                                |
| nqueens                       | 37.9 ms                                                                                                           | 38.9 ms: 1.03x slower                                                                                                 |
| genshi_text                   | 9.73 ms                                                                                                           | 10.0 ms: 1.03x slower                                                                                                 |
| async_tree_eager_io           | 244 ms                                                                                                            | 251 ms: 1.03x slower                                                                                                  |
| pyflate                       | 183 ms                                                                                                            | 188 ms: 1.03x slower                                                                                                  |
| raytrace                      | 115 ms                                                                                                            | 119 ms: 1.03x slower                                                                                                  |
| sqlglot_v2_normalize          | 45.4 ms                                                                                                           | 46.8 ms: 1.03x slower                                                                                                 |
| k_core                        | 989 ms                                                                                                            | 1.02 sec: 1.03x slower                                                                                                |
| sqlglot_v2_optimize           | 22.3 ms                                                                                                           | 23.1 ms: 1.03x slower                                                                                                 |
| sympy_integrate               | 7.35 ms                                                                                                           | 7.59 ms: 1.03x slower                                                                                                 |
| 2to3                          | 113 ms                                                                                                            | 117 ms: 1.04x slower                                                                                                  |
| typing_runtime_protocols      | 62.3 us                                                                                                           | 64.6 us: 1.04x slower                                                                                                 |
| pycparser                     | 476 ms                                                                                                            | 494 ms: 1.04x slower                                                                                                  |
| sympy_str                     | 97.4 ms                                                                                                           | 101 ms: 1.04x slower                                                                                                  |
| scimark_monte_carlo           | 28.8 ms                                                                                                           | 30.0 ms: 1.04x slower                                                                                                 |
| sympy_expand                  | 165 ms                                                                                                            | 172 ms: 1.04x slower                                                                                                  |
| scimark_lu                    | 47.8 ms                                                                                                           | 49.7 ms: 1.04x slower                                                                                                 |
| regex_compile                 | 46.4 ms                                                                                                           | 48.3 ms: 1.04x slower                                                                                                 |
| sqlglot_v2_transpile          | 649 us                                                                                                            | 676 us: 1.04x slower                                                                                                  |
| django_template               | 15.0 ms                                                                                                           | 15.7 ms: 1.04x slower                                                                                                 |
| sqlglot_v2_parse              | 529 us                                                                                                            | 552 us: 1.04x slower                                                                                                  |
| async_tree_eager              | 40.3 ms                                                                                                           | 42.2 ms: 1.05x slower                                                                                                 |
| genshi_xml                    | 21.0 ms                                                                                                           | 22.1 ms: 1.05x slower                                                                                                 |
| async_generators              | 173 ms                                                                                                            | 183 ms: 1.06x slower                                                                                                  |
| richards                      | 20.4 ms                                                                                                           | 21.6 ms: 1.06x slower                                                                                                 |
| deltablue                     | 1.47 ms                                                                                                           | 1.55 ms: 1.06x slower                                                                                                 |
| richards_super                | 22.9 ms                                                                                                           | 24.4 ms: 1.06x slower                                                                                                 |
| hexiom                        | 2.71 ms                                                                                                           | 2.88 ms: 1.06x slower                                                                                                 |
| chaos                         | 25.1 ms                                                                                                           | 26.7 ms: 1.07x slower                                                                                                 |
| logging_silent                | 39.0 ns                                                                                                           | 41.8 ns: 1.07x slower                                                                                                 |
| deepcopy                      | 103 us                                                                                                            | 111 us: 1.07x slower                                                                                                  |
| go                            | 53.1 ms                                                                                                           | 57.3 ms: 1.08x slower                                                                                                 |
| shortest_path                 | 222 ms                                                                                                            | 241 ms: 1.08x slower                                                                                                  |
| spectral_norm                 | 44.8 ms                                                                                                           | 48.9 ms: 1.09x slower                                                                                                 |
| connected_components          | 205 ms                                                                                                            | 224 ms: 1.09x slower                                                                                                  |
| float                         | 28.7 ms                                                                                                           | 31.4 ms: 1.09x slower                                                                                                 |
| deepcopy_memo                 | 11.5 us                                                                                                           | 12.6 us: 1.10x slower                                                                                                 |
| scimark_sparse_mat_mult       | 1.83 ms                                                                                                           | 2.09 ms: 1.15x slower                                                                                                 |
| unpack_sequence               | 27.9 ns                                                                                                           | 32.6 ns: 1.17x slower                                                                                                 |
| nbody                         | 47.6 ms                                                                                                           | 56.7 ms: 1.19x slower                                                                                                 |
| Geometric mean                | (ref)                                                                                                             | 1.02x slower                                                                                                          |

Benchmark hidden because not significant (24): regex_dna, asyncio_tcp_ssl, pickle_pure_python, pathlib, dask, async_tree_eager_cpu_io_mixed_tg, asyncio_websockets, async_tree_none_tg, pidigits, async_tree_eager_io_tg, async_tree_io_tg, async_tree_cpu_io_mixed_tg, gc_traversal, async_tree_memoization_tg, async_tree_cpu_io_mixed, pickle, pickle_list, regex_effbot, async_tree_eager_memoization_tg, asyncio_tcp, async_tree_io, async_tree_eager_tg, async_tree_none, pylint

- Geometric mean (including insignificant results): 1.019x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x