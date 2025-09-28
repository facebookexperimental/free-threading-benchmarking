# Results vs. base

- fork: python
- ref: 48d0d0dd9733eae4935f
- machine: darwin-arm64
- commit hash: 48d0d0d
- commit date: 2025-09-26
- overall geometric mean: 1.007x faster
- HPT reliability: 81.23%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250926-3.15.0a0-48d0d0d/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json | results/bm-20250926-3.15.0a0-48d0d0d-JIT/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                                                                            | 116 ms: 1.03x slower                                                                                                  |
| docutils       | 1.04 sec                                                                                                          | 1.05 sec: 1.01x slower                                                                                                |
| html5lib       | 24.4 ms                                                                                                           | 24.0 ms: 1.02x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20250926-3.15.0a0-48d0d0d/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json | results/bm-20250926-3.15.0a0-48d0d0d-JIT/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_none_tg               | 106 ms                                                                                                            | 104 ms: 1.01x faster                                                                                                  |
| async_tree_io_tg                 | 253 ms                                                                                                            | 250 ms: 1.01x faster                                                                                                  |
| async_tree_io                    | 254 ms                                                                                                            | 251 ms: 1.01x faster                                                                                                  |
| async_tree_eager                 | 42.2 ms                                                                                                           | 41.9 ms: 1.01x faster                                                                                                 |
| async_tree_eager_memoization     | 110 ms                                                                                                            | 111 ms: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg       | 259 ms                                                                                                            | 261 ms: 1.01x slower                                                                                                  |
| asyncio_websockets               | 189 ms                                                                                                            | 191 ms: 1.01x slower                                                                                                  |
| coroutines                       | 10.1 ms                                                                                                           | 10.2 ms: 1.01x slower                                                                                                 |
| async_tree_eager_cpu_io_mixed_tg | 245 ms                                                                                                            | 248 ms: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed          | 261 ms                                                                                                            | 264 ms: 1.01x slower                                                                                                  |
| async_tree_eager_cpu_io_mixed    | 220 ms                                                                                                            | 223 ms: 1.01x slower                                                                                                  |
| async_generators                 | 173 ms                                                                                                            | 182 ms: 1.06x slower                                                                                                  |
| Geometric mean                   | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (9): asyncio_tcp, async_tree_eager_io_tg, async_tree_none, async_tree_eager_tg, asyncio_tcp_ssl, async_tree_memoization_tg, async_tree_memoization, async_tree_eager_memoization_tg, async_tree_eager_io

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250926-3.15.0a0-48d0d0d/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json | results/bm-20250926-3.15.0a0-48d0d0d-JIT/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                                                                           | 31.0 ms: 1.01x faster                                                                                                 |
| pidigits       | 161 ms                                                                                                            | 160 ms: 1.01x faster                                                                                                  |
| nbody          | 50.5 ms                                                                                                           | 56.4 ms: 1.12x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.03x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250926-3.15.0a0-48d0d0d/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json | results/bm-20250926-3.15.0a0-48d0d0d-JIT/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 49.2 ms                                                                                                           | 48.3 ms: 1.02x faster                                                                                                 |
| regex_v8       | 9.78 ms                                                                                                           | 9.68 ms: 1.01x faster                                                                                                 |
| regex_effbot   | 1.44 ms                                                                                                           | 1.47 ms: 1.02x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.00x faster                                                                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250926-3.15.0a0-48d0d0d/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json | results/bm-20250926-3.15.0a0-48d0d0d-JIT/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 948 ms                                                                                                            | 813 ms: 1.17x faster                                                                                                  |
| unpickle_pure_python | 102 us                                                                                                            | 92.9 us: 1.10x faster                                                                                                 |
| xml_etree_process    | 25.7 ms                                                                                                           | 23.7 ms: 1.08x faster                                                                                                 |
| pickle_pure_python   | 150 us                                                                                                            | 141 us: 1.07x faster                                                                                                  |
| xml_etree_generate   | 36.2 ms                                                                                                           | 34.3 ms: 1.06x faster                                                                                                 |
| json_dumps           | 3.87 ms                                                                                                           | 3.78 ms: 1.02x faster                                                                                                 |
| pickle_dict          | 13.1 us                                                                                                           | 12.8 us: 1.02x faster                                                                                                 |
| pickle               | 6.03 us                                                                                                           | 5.94 us: 1.01x faster                                                                                                 |
| xml_etree_parse      | 61.3 ms                                                                                                           | 60.8 ms: 1.01x faster                                                                                                 |
| unpickle             | 6.41 us                                                                                                           | 6.52 us: 1.02x slower                                                                                                 |
| json_loads           | 10.7 us                                                                                                           | 11.1 us: 1.03x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (3): xml_etree_iterparse, unpickle_list, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250926-3.15.0a0-48d0d0d/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json | results/bm-20250926-3.15.0a0-48d0d0d-JIT/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 6.20 ms                                                                                                           | 6.23 ms: 1.00x slower                                                                                                 |
| python_startup         | 8.65 ms                                                                                                           | 8.71 ms: 1.01x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250926-3.15.0a0-48d0d0d/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json | results/bm-20250926-3.15.0a0-48d0d0d-JIT/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 5.06 ms                                                                                                           | 4.38 ms: 1.16x faster                                                                                                 |
| genshi_text     | 10.1 ms                                                                                                           | 9.90 ms: 1.02x faster                                                                                                 |
| django_template | 15.5 ms                                                                                                           | 15.4 ms: 1.01x faster                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | results/bm-20250926-3.15.0a0-48d0d0d/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json | results/bm-20250926-3.15.0a0-48d0d0d-JIT/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads                      | 948 ms                                                                                                            | 813 ms: 1.17x faster                                                                                                  |
| pprint_safe_repr                 | 336 ms                                                                                                            | 288 ms: 1.17x faster                                                                                                  |
| mako                             | 5.06 ms                                                                                                           | 4.38 ms: 1.16x faster                                                                                                 |
| pprint_pformat                   | 672 ms                                                                                                            | 585 ms: 1.15x faster                                                                                                  |
| fannkuch                         | 189 ms                                                                                                            | 171 ms: 1.11x faster                                                                                                  |
| unpickle_pure_python             | 102 us                                                                                                            | 92.9 us: 1.10x faster                                                                                                 |
| xml_etree_process                | 25.7 ms                                                                                                           | 23.7 ms: 1.08x faster                                                                                                 |
| telco                            | 2.86 ms                                                                                                           | 2.68 ms: 1.07x faster                                                                                                 |
| pickle_pure_python               | 150 us                                                                                                            | 141 us: 1.07x faster                                                                                                  |
| scimark_fft                      | 129 ms                                                                                                            | 122 ms: 1.06x faster                                                                                                  |
| xml_etree_generate               | 36.2 ms                                                                                                           | 34.3 ms: 1.06x faster                                                                                                 |
| scimark_monte_carlo              | 30.7 ms                                                                                                           | 29.5 ms: 1.04x faster                                                                                                 |
| pyflate                          | 198 ms                                                                                                            | 191 ms: 1.04x faster                                                                                                  |
| sqlglot_v2_parse                 | 565 us                                                                                                            | 546 us: 1.03x faster                                                                                                  |
| scimark_sor                      | 52.1 ms                                                                                                           | 50.5 ms: 1.03x faster                                                                                                 |
| comprehensions                   | 7.57 us                                                                                                           | 7.34 us: 1.03x faster                                                                                                 |
| raytrace                         | 121 ms                                                                                                            | 118 ms: 1.03x faster                                                                                                  |
| sqlglot_v2_normalize             | 47.5 ms                                                                                                           | 46.3 ms: 1.03x faster                                                                                                 |
| sqlite_synth                     | 950 ns                                                                                                            | 927 ns: 1.02x faster                                                                                                  |
| json_dumps                       | 3.87 ms                                                                                                           | 3.78 ms: 1.02x faster                                                                                                 |
| sqlglot_v2_transpile             | 687 us                                                                                                            | 672 us: 1.02x faster                                                                                                  |
| pickle_dict                      | 13.1 us                                                                                                           | 12.8 us: 1.02x faster                                                                                                 |
| richards_super                   | 24.5 ms                                                                                                           | 24.0 ms: 1.02x faster                                                                                                 |
| regex_compile                    | 49.2 ms                                                                                                           | 48.3 ms: 1.02x faster                                                                                                 |
| genshi_text                      | 10.1 ms                                                                                                           | 9.90 ms: 1.02x faster                                                                                                 |
| html5lib                         | 24.4 ms                                                                                                           | 24.0 ms: 1.02x faster                                                                                                 |
| deepcopy_reduce                  | 1.15 us                                                                                                           | 1.13 us: 1.02x faster                                                                                                 |
| spectral_norm                    | 44.6 ms                                                                                                           | 43.9 ms: 1.02x faster                                                                                                 |
| async_tree_none_tg               | 106 ms                                                                                                            | 104 ms: 1.01x faster                                                                                                  |
| logging_simple                   | 2.35 us                                                                                                           | 2.32 us: 1.01x faster                                                                                                 |
| pickle                           | 6.03 us                                                                                                           | 5.94 us: 1.01x faster                                                                                                 |
| float                            | 31.4 ms                                                                                                           | 31.0 ms: 1.01x faster                                                                                                 |
| async_tree_io_tg                 | 253 ms                                                                                                            | 250 ms: 1.01x faster                                                                                                  |
| chaos                            | 27.0 ms                                                                                                           | 26.6 ms: 1.01x faster                                                                                                 |
| sqlglot_v2_optimize              | 23.1 ms                                                                                                           | 22.8 ms: 1.01x faster                                                                                                 |
| create_gc_cycles                 | 924 us                                                                                                            | 914 us: 1.01x faster                                                                                                  |
| regex_v8                         | 9.78 ms                                                                                                           | 9.68 ms: 1.01x faster                                                                                                 |
| async_tree_io                    | 254 ms                                                                                                            | 251 ms: 1.01x faster                                                                                                  |
| richards                         | 21.6 ms                                                                                                           | 21.4 ms: 1.01x faster                                                                                                 |
| logging_format                   | 2.57 us                                                                                                           | 2.55 us: 1.01x faster                                                                                                 |
| xml_etree_parse                  | 61.3 ms                                                                                                           | 60.8 ms: 1.01x faster                                                                                                 |
| logging_silent                   | 41.7 ns                                                                                                           | 41.4 ns: 1.01x faster                                                                                                 |
| django_template                  | 15.5 ms                                                                                                           | 15.4 ms: 1.01x faster                                                                                                 |
| async_tree_eager                 | 42.2 ms                                                                                                           | 41.9 ms: 1.01x faster                                                                                                 |
| thrift                           | 315 us                                                                                                            | 313 us: 1.01x faster                                                                                                  |
| pidigits                         | 161 ms                                                                                                            | 160 ms: 1.01x faster                                                                                                  |
| scimark_lu                       | 48.6 ms                                                                                                           | 48.4 ms: 1.00x faster                                                                                                 |
| bpe_tokeniser                    | 1.98 sec                                                                                                          | 1.98 sec: 1.00x slower                                                                                                |
| sympy_sum                        | 55.4 ms                                                                                                           | 55.5 ms: 1.00x slower                                                                                                 |
| python_startup_no_site           | 6.20 ms                                                                                                           | 6.23 ms: 1.00x slower                                                                                                 |
| meteor_contest                   | 49.2 ms                                                                                                           | 49.5 ms: 1.00x slower                                                                                                 |
| async_tree_eager_memoization     | 110 ms                                                                                                            | 111 ms: 1.01x slower                                                                                                  |
| hexiom                           | 2.86 ms                                                                                                           | 2.87 ms: 1.01x slower                                                                                                 |
| python_startup                   | 8.65 ms                                                                                                           | 8.71 ms: 1.01x slower                                                                                                 |
| gc_traversal                     | 2.03 ms                                                                                                           | 2.05 ms: 1.01x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg       | 259 ms                                                                                                            | 261 ms: 1.01x slower                                                                                                  |
| typing_runtime_protocols         | 63.1 us                                                                                                           | 63.6 us: 1.01x slower                                                                                                 |
| go                               | 57.0 ms                                                                                                           | 57.4 ms: 1.01x slower                                                                                                 |
| asyncio_websockets               | 189 ms                                                                                                            | 191 ms: 1.01x slower                                                                                                  |
| coroutines                       | 10.1 ms                                                                                                           | 10.2 ms: 1.01x slower                                                                                                 |
| json                             | 1.89 ms                                                                                                           | 1.91 ms: 1.01x slower                                                                                                 |
| async_tree_eager_cpu_io_mixed_tg | 245 ms                                                                                                            | 248 ms: 1.01x slower                                                                                                  |
| nqueens                          | 39.3 ms                                                                                                           | 39.7 ms: 1.01x slower                                                                                                 |
| async_tree_cpu_io_mixed          | 261 ms                                                                                                            | 264 ms: 1.01x slower                                                                                                  |
| crypto_pyaes                     | 37.1 ms                                                                                                           | 37.6 ms: 1.01x slower                                                                                                 |
| docutils                         | 1.04 sec                                                                                                          | 1.05 sec: 1.01x slower                                                                                                |
| async_tree_eager_cpu_io_mixed    | 220 ms                                                                                                            | 223 ms: 1.01x slower                                                                                                  |
| coverage                         | 32.7 ms                                                                                                           | 33.2 ms: 1.01x slower                                                                                                 |
| unpickle                         | 6.41 us                                                                                                           | 6.52 us: 1.02x slower                                                                                                 |
| deltablue                        | 1.50 ms                                                                                                           | 1.53 ms: 1.02x slower                                                                                                 |
| sympy_expand                     | 169 ms                                                                                                            | 172 ms: 1.02x slower                                                                                                  |
| bench_mp_pool                    | 41.5 ms                                                                                                           | 42.3 ms: 1.02x slower                                                                                                 |
| sympy_str                        | 98.8 ms                                                                                                           | 101 ms: 1.02x slower                                                                                                  |
| sympy_integrate                  | 7.36 ms                                                                                                           | 7.52 ms: 1.02x slower                                                                                                 |
| regex_effbot                     | 1.44 ms                                                                                                           | 1.47 ms: 1.02x slower                                                                                                 |
| deepcopy_memo                    | 12.5 us                                                                                                           | 12.8 us: 1.03x slower                                                                                                 |
| pycparser                        | 493 ms                                                                                                            | 507 ms: 1.03x slower                                                                                                  |
| k_core                           | 959 ms                                                                                                            | 990 ms: 1.03x slower                                                                                                  |
| generators                       | 17.5 ms                                                                                                           | 18.0 ms: 1.03x slower                                                                                                 |
| many_optionals                   | 319 us                                                                                                            | 330 us: 1.03x slower                                                                                                  |
| 2to3                             | 112 ms                                                                                                            | 116 ms: 1.03x slower                                                                                                  |
| json_loads                       | 10.7 us                                                                                                           | 11.1 us: 1.03x slower                                                                                                 |
| async_generators                 | 173 ms                                                                                                            | 182 ms: 1.06x slower                                                                                                  |
| shortest_path                    | 220 ms                                                                                                            | 235 ms: 1.07x slower                                                                                                  |
| connected_components             | 202 ms                                                                                                            | 218 ms: 1.08x slower                                                                                                  |
| unpack_sequence                  | 29.7 ns                                                                                                           | 32.9 ns: 1.11x slower                                                                                                 |
| nbody                            | 50.5 ms                                                                                                           | 56.4 ms: 1.12x slower                                                                                                 |
| scimark_sparse_mat_mult          | 1.85 ms                                                                                                           | 2.11 ms: 1.14x slower                                                                                                 |
| Geometric mean                   | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (23): asyncio_tcp, async_tree_eager_io_tg, async_tree_none, async_tree_eager_tg, asyncio_tcp_ssl, async_tree_memoization_tg, regex_dna, bench_thread_pool, pathlib, xml_etree_iterparse, sphinx, deepcopy, dulwich_log, unpickle_list, dask, pickle_list, genshi_xml, async_tree_memoization, mdp, async_tree_eager_memoization_tg, subparsers, async_tree_eager_io, pylint

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 81.23% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x