# Results vs. base

- fork: python
- ref: 7a918411a300ddeef06d
- machine: darwin-arm64
- commit hash: 7a91841
- commit date: 2026-09-05
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-JIT/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| docutils       | 939 ms                                                                                                            | 923 ms: 1.02x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.00x faster                                                                                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                    | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-JIT/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_none_tg           | 126 ms                                                                                                            | 115 ms: 1.09x faster                                                                                                  |
| async_tree_none              | 120 ms                                                                                                            | 110 ms: 1.09x faster                                                                                                  |
| async_tree_io_tg             | 328 ms                                                                                                            | 302 ms: 1.09x faster                                                                                                  |
| async_tree_io                | 312 ms                                                                                                            | 290 ms: 1.08x faster                                                                                                  |
| async_tree_eager_io          | 310 ms                                                                                                            | 290 ms: 1.07x faster                                                                                                  |
| async_tree_eager             | 40.0 ms                                                                                                           | 37.5 ms: 1.07x faster                                                                                                 |
| async_tree_eager_io_tg       | 336 ms                                                                                                            | 317 ms: 1.06x faster                                                                                                  |
| async_tree_memoization       | 176 ms                                                                                                            | 166 ms: 1.06x faster                                                                                                  |
| async_tree_memoization_tg    | 173 ms                                                                                                            | 165 ms: 1.05x faster                                                                                                  |
| async_tree_eager_tg          | 103 ms                                                                                                            | 98.8 ms: 1.04x faster                                                                                                 |
| async_tree_cpu_io_mixed      | 281 ms                                                                                                            | 274 ms: 1.02x faster                                                                                                  |
| async_tree_eager_memoization | 115 ms                                                                                                            | 112 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg   | 290 ms                                                                                                            | 285 ms: 1.02x faster                                                                                                  |
| asyncio_websockets           | 189 ms                                                                                                            | 190 ms: 1.00x slower                                                                                                  |
| coroutines                   | 9.41 ms                                                                                                           | 9.81 ms: 1.04x slower                                                                                                 |
| async_generators             | 144 ms                                                                                                            | 152 ms: 1.06x slower                                                                                                  |
| Geometric mean               | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (5): async_tree_eager_memoization_tg, async_tree_eager_cpu_io_mixed, asyncio_tcp, asyncio_tcp_ssl, async_tree_eager_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-JIT/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| nbody          | 42.6 ms                                                                                                           | 32.0 ms: 1.33x faster                                                                                                 |
| float          | 28.7 ms                                                                                                           | 23.1 ms: 1.25x faster                                                                                                 |
| pidigits       | 165 ms                                                                                                            | 163 ms: 1.01x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.19x faster                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-JIT/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 54.2 ms                                                                                                           | 46.6 ms: 1.16x faster                                                                                                 |
| regex_v8       | 9.25 ms                                                                                                           | 9.14 ms: 1.01x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-JIT/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pickle_pure_python   | 141 us                                                                                                            | 110 us: 1.28x faster                                                                                                  |
| unpickle_pure_python | 101 us                                                                                                            | 83.9 us: 1.20x faster                                                                                                 |
| xml_etree_process    | 25.2 ms                                                                                                           | 22.6 ms: 1.11x faster                                                                                                 |
| xml_etree_iterparse  | 44.1 ms                                                                                                           | 40.4 ms: 1.09x faster                                                                                                 |
| xml_etree_generate   | 36.0 ms                                                                                                           | 33.4 ms: 1.08x faster                                                                                                 |
| tomli_loads          | 821 ms                                                                                                            | 767 ms: 1.07x faster                                                                                                  |
| json_dumps           | 3.59 ms                                                                                                           | 3.36 ms: 1.07x faster                                                                                                 |
| unpickle             | 6.35 us                                                                                                           | 6.09 us: 1.04x faster                                                                                                 |
| pickle               | 6.21 us                                                                                                           | 6.03 us: 1.03x faster                                                                                                 |
| json_loads           | 10.7 us                                                                                                           | 10.4 us: 1.03x faster                                                                                                 |
| pickle_dict          | 13.0 us                                                                                                           | 12.7 us: 1.02x faster                                                                                                 |
| pickle_list          | 2.36 us                                                                                                           | 2.35 us: 1.00x faster                                                                                                 |
| unpickle_list        | 2.02 us                                                                                                           | 2.06 us: 1.02x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.07x faster                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-JIT/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 9.52 ms                                                                                                           | 9.09 ms: 1.05x faster                                                                                                 |
| python_startup_no_site | 6.72 ms                                                                                                           | 6.61 ms: 1.02x faster                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-JIT/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 4.56 ms                                                                                                           | 3.88 ms: 1.18x faster                                                                                                 |
| django_template | 14.9 ms                                                                                                           | 15.2 ms: 1.02x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.07x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                    | results/bm-20260905-3.16.0a0-7a91841/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json | results/bm-20260905-3.16.0a0-7a91841-JIT/bm-20260905-macm4pro-arm64-python-7a918411a300ddeef06d-3.16.0a0-7a91841.json |
|------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| richards_super               | 23.2 ms                                                                                                           | 10.8 ms: 2.15x faster                                                                                                 |
| richards                     | 20.4 ms                                                                                                           | 9.62 ms: 2.12x faster                                                                                                 |
| scimark_lu                   | 49.8 ms                                                                                                           | 30.8 ms: 1.62x faster                                                                                                 |
| scimark_sor                  | 48.9 ms                                                                                                           | 32.3 ms: 1.51x faster                                                                                                 |
| nbody                        | 42.6 ms                                                                                                           | 32.0 ms: 1.33x faster                                                                                                 |
| spectral_norm                | 42.3 ms                                                                                                           | 32.0 ms: 1.32x faster                                                                                                 |
| pyflate                      | 190 ms                                                                                                            | 147 ms: 1.29x faster                                                                                                  |
| pickle_pure_python           | 141 us                                                                                                            | 110 us: 1.28x faster                                                                                                  |
| scimark_fft                  | 123 ms                                                                                                            | 97.3 ms: 1.26x faster                                                                                                 |
| chaos                        | 25.5 ms                                                                                                           | 20.2 ms: 1.26x faster                                                                                                 |
| float                        | 28.7 ms                                                                                                           | 23.1 ms: 1.25x faster                                                                                                 |
| deltablue                    | 1.47 ms                                                                                                           | 1.18 ms: 1.24x faster                                                                                                 |
| logging_simple               | 2.17 us                                                                                                           | 1.74 us: 1.24x faster                                                                                                 |
| logging_format               | 2.39 us                                                                                                           | 1.93 us: 1.24x faster                                                                                                 |
| sqlglot_v2_parse             | 505 us                                                                                                            | 416 us: 1.21x faster                                                                                                  |
| raytrace                     | 121 ms                                                                                                            | 99.7 ms: 1.21x faster                                                                                                 |
| crypto_pyaes                 | 38.0 ms                                                                                                           | 31.5 ms: 1.21x faster                                                                                                 |
| unpickle_pure_python         | 101 us                                                                                                            | 83.9 us: 1.20x faster                                                                                                 |
| pprint_pformat               | 622 ms                                                                                                            | 520 ms: 1.20x faster                                                                                                  |
| mako                         | 4.56 ms                                                                                                           | 3.88 ms: 1.18x faster                                                                                                 |
| pprint_safe_repr             | 302 ms                                                                                                            | 257 ms: 1.17x faster                                                                                                  |
| sqlglot_v2_transpile         | 620 us                                                                                                            | 528 us: 1.17x faster                                                                                                  |
| scimark_monte_carlo          | 28.0 ms                                                                                                           | 24.0 ms: 1.17x faster                                                                                                 |
| deepcopy_memo                | 11.8 us                                                                                                           | 10.1 us: 1.17x faster                                                                                                 |
| regex_compile                | 54.2 ms                                                                                                           | 46.6 ms: 1.16x faster                                                                                                 |
| nqueens                      | 34.9 ms                                                                                                           | 30.8 ms: 1.13x faster                                                                                                 |
| comprehensions               | 6.60 us                                                                                                           | 5.92 us: 1.11x faster                                                                                                 |
| xml_etree_process            | 25.2 ms                                                                                                           | 22.6 ms: 1.11x faster                                                                                                 |
| sqlglot_v2_normalize         | 45.5 ms                                                                                                           | 40.9 ms: 1.11x faster                                                                                                 |
| typing_runtime_protocols     | 48.4 us                                                                                                           | 43.9 us: 1.10x faster                                                                                                 |
| hexiom                       | 2.66 ms                                                                                                           | 2.41 ms: 1.10x faster                                                                                                 |
| go                           | 52.6 ms                                                                                                           | 48.0 ms: 1.09x faster                                                                                                 |
| xml_etree_iterparse          | 44.1 ms                                                                                                           | 40.4 ms: 1.09x faster                                                                                                 |
| async_tree_none_tg           | 126 ms                                                                                                            | 115 ms: 1.09x faster                                                                                                  |
| telco                        | 2.90 ms                                                                                                           | 2.66 ms: 1.09x faster                                                                                                 |
| async_tree_none              | 120 ms                                                                                                            | 110 ms: 1.09x faster                                                                                                  |
| async_tree_io_tg             | 328 ms                                                                                                            | 302 ms: 1.09x faster                                                                                                  |
| subparsers                   | 4.05 ms                                                                                                           | 3.73 ms: 1.09x faster                                                                                                 |
| deepcopy_reduce              | 1.08 us                                                                                                           | 1.00 us: 1.08x faster                                                                                                 |
| xml_etree_generate           | 36.0 ms                                                                                                           | 33.4 ms: 1.08x faster                                                                                                 |
| async_tree_io                | 312 ms                                                                                                            | 290 ms: 1.08x faster                                                                                                  |
| fannkuch                     | 162 ms                                                                                                            | 150 ms: 1.07x faster                                                                                                  |
| meteor_contest               | 48.3 ms                                                                                                           | 44.9 ms: 1.07x faster                                                                                                 |
| sqlglot_v2_optimize          | 22.2 ms                                                                                                           | 20.8 ms: 1.07x faster                                                                                                 |
| tomli_loads                  | 821 ms                                                                                                            | 767 ms: 1.07x faster                                                                                                  |
| json_dumps                   | 3.59 ms                                                                                                           | 3.36 ms: 1.07x faster                                                                                                 |
| async_tree_eager_io          | 310 ms                                                                                                            | 290 ms: 1.07x faster                                                                                                  |
| dulwich_log                  | 18.2 ms                                                                                                           | 17.0 ms: 1.07x faster                                                                                                 |
| async_tree_eager             | 40.0 ms                                                                                                           | 37.5 ms: 1.07x faster                                                                                                 |
| sympy_expand                 | 169 ms                                                                                                            | 159 ms: 1.06x faster                                                                                                  |
| async_tree_eager_io_tg       | 336 ms                                                                                                            | 317 ms: 1.06x faster                                                                                                  |
| async_tree_memoization       | 176 ms                                                                                                            | 166 ms: 1.06x faster                                                                                                  |
| bpe_tokeniser                | 1.96 sec                                                                                                          | 1.85 sec: 1.06x faster                                                                                                |
| scimark_sparse_mat_mult      | 1.82 ms                                                                                                           | 1.72 ms: 1.06x faster                                                                                                 |
| async_tree_memoization_tg    | 173 ms                                                                                                            | 165 ms: 1.05x faster                                                                                                  |
| python_startup               | 9.52 ms                                                                                                           | 9.09 ms: 1.05x faster                                                                                                 |
| unpickle                     | 6.35 us                                                                                                           | 6.09 us: 1.04x faster                                                                                                 |
| many_optionals               | 237 us                                                                                                            | 228 us: 1.04x faster                                                                                                  |
| async_tree_eager_tg          | 103 ms                                                                                                            | 98.8 ms: 1.04x faster                                                                                                 |
| sympy_sum                    | 55.2 ms                                                                                                           | 53.1 ms: 1.04x faster                                                                                                 |
| json                         | 1.88 ms                                                                                                           | 1.81 ms: 1.03x faster                                                                                                 |
| sympy_str                    | 99.4 ms                                                                                                           | 96.1 ms: 1.03x faster                                                                                                 |
| pickle                       | 6.21 us                                                                                                           | 6.03 us: 1.03x faster                                                                                                 |
| json_loads                   | 10.7 us                                                                                                           | 10.4 us: 1.03x faster                                                                                                 |
| pickle_dict                  | 13.0 us                                                                                                           | 12.7 us: 1.02x faster                                                                                                 |
| async_tree_cpu_io_mixed      | 281 ms                                                                                                            | 274 ms: 1.02x faster                                                                                                  |
| pathlib                      | 10.7 ms                                                                                                           | 10.4 ms: 1.02x faster                                                                                                 |
| async_tree_eager_memoization | 115 ms                                                                                                            | 112 ms: 1.02x faster                                                                                                  |
| thrift                       | 311 us                                                                                                            | 305 us: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg   | 290 ms                                                                                                            | 285 ms: 1.02x faster                                                                                                  |
| sqlite_synth                 | 932 ns                                                                                                            | 917 ns: 1.02x faster                                                                                                  |
| docutils                     | 939 ms                                                                                                            | 923 ms: 1.02x faster                                                                                                  |
| python_startup_no_site       | 6.72 ms                                                                                                           | 6.61 ms: 1.02x faster                                                                                                 |
| connected_components         | 206 ms                                                                                                            | 203 ms: 1.01x faster                                                                                                  |
| regex_v8                     | 9.25 ms                                                                                                           | 9.14 ms: 1.01x faster                                                                                                 |
| pidigits                     | 165 ms                                                                                                            | 163 ms: 1.01x faster                                                                                                  |
| shortest_path                | 223 ms                                                                                                            | 222 ms: 1.01x faster                                                                                                  |
| sympy_integrate              | 7.45 ms                                                                                                           | 7.42 ms: 1.00x faster                                                                                                 |
| pickle_list                  | 2.36 us                                                                                                           | 2.35 us: 1.00x faster                                                                                                 |
| asyncio_websockets           | 189 ms                                                                                                            | 190 ms: 1.00x slower                                                                                                  |
| gc_traversal                 | 1.92 ms                                                                                                           | 1.92 ms: 1.00x slower                                                                                                 |
| bench_mp_pool                | 44.7 ms                                                                                                           | 44.9 ms: 1.00x slower                                                                                                 |
| deepcopy                     | 97.5 us                                                                                                           | 98.0 us: 1.01x slower                                                                                                 |
| generators                   | 17.2 ms                                                                                                           | 17.3 ms: 1.01x slower                                                                                                 |
| create_gc_cycles             | 813 us                                                                                                            | 820 us: 1.01x slower                                                                                                  |
| bench_thread_pool            | 421 us                                                                                                            | 427 us: 1.01x slower                                                                                                  |
| unpickle_list                | 2.02 us                                                                                                           | 2.06 us: 1.02x slower                                                                                                 |
| django_template              | 14.9 ms                                                                                                           | 15.2 ms: 1.02x slower                                                                                                 |
| logging_silent               | 41.5 ns                                                                                                           | 42.9 ns: 1.03x slower                                                                                                 |
| coroutines                   | 9.41 ms                                                                                                           | 9.81 ms: 1.04x slower                                                                                                 |
| async_generators             | 144 ms                                                                                                            | 152 ms: 1.06x slower                                                                                                  |
| mdp                          | 514 ms                                                                                                            | 586 ms: 1.14x slower                                                                                                  |
| k_core                       | 975 ms                                                                                                            | 1.14 sec: 1.16x slower                                                                                                |
| unpack_sequence              | 23.5 ns                                                                                                           | 30.8 ns: 1.31x slower                                                                                                 |
| Geometric mean               | (ref)                                                                                                             | 1.09x faster                                                                                                          |

Benchmark hidden because not significant (13): pylint, async_tree_eager_memoization_tg, sphinx, xml_etree_parse, pycparser, async_tree_eager_cpu_io_mixed, asyncio_tcp, regex_dna, regex_effbot, 2to3, asyncio_tcp_ssl, async_tree_eager_cpu_io_mixed_tg, html5lib

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.04x