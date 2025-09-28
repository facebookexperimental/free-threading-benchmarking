# Results vs. default_base_vs_NOGIL

- fork: python
- ref: 48d0d0dd9733eae4935f
- machine: darwin-arm64
- commit hash: 48d0d0d
- commit date: 2025-09-26
- overall geometric mean: 1.001x slower
- HPT reliability: 88.84%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                                  | 122 ms: 1.07x slower                                                    |
| docutils       | 1.04 sec                                                                | 981 ms: 1.06x faster                                                    |
| html5lib       | 24.3 ms                                                                 | 23.3 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                                   | 1.01x faster                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 257 ms                                                                  | 194 ms: 1.33x faster                                                    |
| async_tree_io_tg                 | 255 ms                                                                  | 198 ms: 1.29x faster                                                    |
| async_tree_eager_io              | 252 ms                                                                  | 203 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 107 ms                                                                  | 86.5 ms: 1.24x faster                                                   |
| async_tree_io                    | 256 ms                                                                  | 210 ms: 1.22x faster                                                    |
| async_tree_memoization_tg        | 149 ms                                                                  | 124 ms: 1.21x faster                                                    |
| async_tree_eager_memoization_tg  | 131 ms                                                                  | 112 ms: 1.18x faster                                                    |
| async_tree_memoization           | 150 ms                                                                  | 130 ms: 1.16x faster                                                    |
| async_tree_none                  | 115 ms                                                                  | 100 ms: 1.15x faster                                                    |
| async_tree_eager_tg              | 88.9 ms                                                                 | 78.0 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 263 ms                                                                  | 234 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 249 ms                                                                  | 226 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 266 ms                                                                  | 242 ms: 1.10x faster                                                    |
| asyncio_websockets               | 190 ms                                                                  | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization     | 111 ms                                                                  | 109 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 223 ms                                                                  | 222 ms: 1.00x faster                                                    |
| async_generators                 | 178 ms                                                                  | 182 ms: 1.03x slower                                                    |
| coroutines                       | 10.3 ms                                                                 | 10.7 ms: 1.04x slower                                                   |
| async_tree_eager                 | 42.6 ms                                                                 | 48.9 ms: 1.15x slower                                                   |
| Geometric mean                   | (ref)                                                                   | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                                 | 29.6 ms: 1.06x faster                                                   |
| pidigits       | 163 ms                                                                  | 160 ms: 1.02x faster                                                    |
| nbody          | 50.7 ms                                                                 | 56.2 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                                   | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 9.99 ms                                                                 | 9.37 ms: 1.07x faster                                                   |
| regex_dna      | 96.6 ms                                                                 | 95.1 ms: 1.02x faster                                                   |
| regex_effbot   | 1.46 ms                                                                 | 1.44 ms: 1.01x faster                                                   |
| regex_compile  | 49.5 ms                                                                 | 52.8 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                                   | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 43.3 ms                                                                 | 37.3 ms: 1.16x faster                                                   |
| xml_etree_parse      | 61.3 ms                                                                 | 58.5 ms: 1.05x faster                                                   |
| tomli_loads          | 943 ms                                                                  | 955 ms: 1.01x slower                                                    |
| json_dumps           | 3.84 ms                                                                 | 3.91 ms: 1.02x slower                                                   |
| pickle_pure_python   | 147 us                                                                  | 151 us: 1.02x slower                                                    |
| xml_etree_generate   | 35.9 ms                                                                 | 36.9 ms: 1.03x slower                                                   |
| xml_etree_process    | 25.4 ms                                                                 | 26.8 ms: 1.06x slower                                                   |
| json_loads           | 10.8 us                                                                 | 11.5 us: 1.07x slower                                                   |
| unpickle_pure_python | 102 us                                                                  | 111 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                                   | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|------------------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.67 ms                                                                 | 9.50 ms: 1.10x slower                                                   |
| python_startup_no_site | 6.20 ms                                                                 | 6.90 ms: 1.11x slower                                                   |
| Geometric mean         | (ref)                                                                   | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|-----------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 15.5 ms                                                                 | 16.4 ms: 1.05x slower                                                   |
| genshi_xml      | 22.3 ms                                                                 | 23.9 ms: 1.07x slower                                                   |
| genshi_text     | 10.2 ms                                                                 | 11.6 ms: 1.13x slower                                                   |
| mako            | 5.01 ms                                                                 | 5.70 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                                   | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20250926-macm4pro-arm64-python-93ac3525b92f5f891821-3.15.0a0-93ac352 | bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d |
|----------------------------------|:-----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.03 ms                                                                 | 749 us: 2.72x faster                                                    |
| create_gc_cycles                 | 920 us                                                                  | 472 us: 1.95x faster                                                    |
| async_tree_eager_io_tg           | 257 ms                                                                  | 194 ms: 1.33x faster                                                    |
| async_tree_io_tg                 | 255 ms                                                                  | 198 ms: 1.29x faster                                                    |
| async_tree_eager_io              | 252 ms                                                                  | 203 ms: 1.24x faster                                                    |
| async_tree_none_tg               | 107 ms                                                                  | 86.5 ms: 1.24x faster                                                   |
| async_tree_io                    | 256 ms                                                                  | 210 ms: 1.22x faster                                                    |
| async_tree_memoization_tg        | 149 ms                                                                  | 124 ms: 1.21x faster                                                    |
| async_tree_eager_memoization_tg  | 131 ms                                                                  | 112 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 43.3 ms                                                                 | 37.3 ms: 1.16x faster                                                   |
| async_tree_memoization           | 150 ms                                                                  | 130 ms: 1.16x faster                                                    |
| async_tree_none                  | 115 ms                                                                  | 100 ms: 1.15x faster                                                    |
| async_tree_eager_tg              | 88.9 ms                                                                 | 78.0 ms: 1.14x faster                                                   |
| sqlite_synth                     | 952 ns                                                                  | 836 ns: 1.14x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 263 ms                                                                  | 234 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 249 ms                                                                  | 226 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 266 ms                                                                  | 242 ms: 1.10x faster                                                    |
| pycparser                        | 493 ms                                                                  | 462 ms: 1.07x faster                                                    |
| regex_v8                         | 9.99 ms                                                                 | 9.37 ms: 1.07x faster                                                   |
| docutils                         | 1.04 sec                                                                | 981 ms: 1.06x faster                                                    |
| float                            | 31.4 ms                                                                 | 29.6 ms: 1.06x faster                                                   |
| xml_etree_parse                  | 61.3 ms                                                                 | 58.5 ms: 1.05x faster                                                   |
| html5lib                         | 24.3 ms                                                                 | 23.3 ms: 1.05x faster                                                   |
| asyncio_websockets               | 190 ms                                                                  | 185 ms: 1.03x faster                                                    |
| pyflate                          | 201 ms                                                                  | 197 ms: 1.02x faster                                                    |
| pidigits                         | 163 ms                                                                  | 160 ms: 1.02x faster                                                    |
| regex_dna                        | 96.6 ms                                                                 | 95.1 ms: 1.02x faster                                                   |
| regex_effbot                     | 1.46 ms                                                                 | 1.44 ms: 1.01x faster                                                   |
| async_tree_eager_memoization     | 111 ms                                                                  | 109 ms: 1.01x faster                                                    |
| bpe_tokeniser                    | 2.01 sec                                                                | 2.00 sec: 1.01x faster                                                  |
| pathlib                          | 10.4 ms                                                                 | 10.4 ms: 1.00x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 223 ms                                                                  | 222 ms: 1.00x faster                                                    |
| tomli_loads                      | 943 ms                                                                  | 955 ms: 1.01x slower                                                    |
| dask                             | 522 ms                                                                  | 530 ms: 1.02x slower                                                    |
| json_dumps                       | 3.84 ms                                                                 | 3.91 ms: 1.02x slower                                                   |
| many_optionals                   | 330 us                                                                  | 337 us: 1.02x slower                                                    |
| dulwich_log                      | 18.1 ms                                                                 | 18.6 ms: 1.02x slower                                                   |
| pickle_pure_python               | 147 us                                                                  | 151 us: 1.02x slower                                                    |
| async_generators                 | 178 ms                                                                  | 182 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.9 ms                                                                 | 36.9 ms: 1.03x slower                                                   |
| sqlglot_v2_normalize             | 47.6 ms                                                                 | 48.9 ms: 1.03x slower                                                   |
| coroutines                       | 10.3 ms                                                                 | 10.7 ms: 1.04x slower                                                   |
| k_core                           | 957 ms                                                                  | 993 ms: 1.04x slower                                                    |
| json                             | 1.90 ms                                                                 | 1.97 ms: 1.04x slower                                                   |
| sqlglot_v2_optimize              | 23.2 ms                                                                 | 24.2 ms: 1.04x slower                                                   |
| subparsers                       | 18.2 ms                                                                 | 19.0 ms: 1.04x slower                                                   |
| deepcopy                         | 110 us                                                                  | 115 us: 1.05x slower                                                    |
| pprint_safe_repr                 | 333 ms                                                                  | 350 ms: 1.05x slower                                                    |
| sqlglot_v2_transpile             | 685 us                                                                  | 720 us: 1.05x slower                                                    |
| scimark_fft                      | 127 ms                                                                  | 134 ms: 1.05x slower                                                    |
| telco                            | 2.90 ms                                                                 | 3.05 ms: 1.05x slower                                                   |
| logging_simple                   | 2.37 us                                                                 | 2.49 us: 1.05x slower                                                   |
| django_template                  | 15.5 ms                                                                 | 16.4 ms: 1.05x slower                                                   |
| deepcopy_memo                    | 12.5 us                                                                 | 13.2 us: 1.06x slower                                                   |
| xml_etree_process                | 25.4 ms                                                                 | 26.8 ms: 1.06x slower                                                   |
| scimark_sor                      | 52.2 ms                                                                 | 55.1 ms: 1.06x slower                                                   |
| pprint_pformat                   | 670 ms                                                                  | 710 ms: 1.06x slower                                                    |
| sqlglot_v2_parse                 | 566 us                                                                  | 599 us: 1.06x slower                                                    |
| regex_compile                    | 49.5 ms                                                                 | 52.8 ms: 1.07x slower                                                   |
| json_loads                       | 10.8 us                                                                 | 11.5 us: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                                  | 122 ms: 1.07x slower                                                    |
| thrift                           | 312 us                                                                  | 334 us: 1.07x slower                                                    |
| deltablue                        | 1.52 ms                                                                 | 1.63 ms: 1.07x slower                                                   |
| shortest_path                    | 218 ms                                                                  | 233 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.44 ms                                                                 | 7.98 ms: 1.07x slower                                                   |
| generators                       | 17.4 ms                                                                 | 18.7 ms: 1.07x slower                                                   |
| genshi_xml                       | 22.3 ms                                                                 | 23.9 ms: 1.07x slower                                                   |
| sympy_sum                        | 55.9 ms                                                                 | 60.3 ms: 1.08x slower                                                   |
| logging_format                   | 2.59 us                                                                 | 2.79 us: 1.08x slower                                                   |
| comprehensions                   | 7.79 us                                                                 | 8.42 us: 1.08x slower                                                   |
| deepcopy_reduce                  | 1.15 us                                                                 | 1.25 us: 1.08x slower                                                   |
| go                               | 57.6 ms                                                                 | 62.5 ms: 1.08x slower                                                   |
| logging_silent                   | 41.2 ns                                                                 | 44.7 ns: 1.09x slower                                                   |
| unpickle_pure_python             | 102 us                                                                  | 111 us: 1.09x slower                                                    |
| hexiom                           | 2.90 ms                                                                 | 3.16 ms: 1.09x slower                                                   |
| mdp                              | 546 ms                                                                  | 597 ms: 1.09x slower                                                    |
| nqueens                          | 39.8 ms                                                                 | 43.6 ms: 1.09x slower                                                   |
| python_startup                   | 8.67 ms                                                                 | 9.50 ms: 1.10x slower                                                   |
| connected_components             | 202 ms                                                                  | 222 ms: 1.10x slower                                                    |
| richards                         | 21.5 ms                                                                 | 23.6 ms: 1.10x slower                                                   |
| sympy_str                        | 99.9 ms                                                                 | 110 ms: 1.10x slower                                                    |
| richards_super                   | 24.4 ms                                                                 | 27.0 ms: 1.11x slower                                                   |
| raytrace                         | 119 ms                                                                  | 132 ms: 1.11x slower                                                    |
| nbody                            | 50.7 ms                                                                 | 56.2 ms: 1.11x slower                                                   |
| sympy_expand                     | 170 ms                                                                  | 188 ms: 1.11x slower                                                    |
| chaos                            | 26.5 ms                                                                 | 29.4 ms: 1.11x slower                                                   |
| python_startup_no_site           | 6.20 ms                                                                 | 6.90 ms: 1.11x slower                                                   |
| scimark_lu                       | 49.2 ms                                                                 | 54.9 ms: 1.12x slower                                                   |
| scimark_monte_carlo              | 30.3 ms                                                                 | 33.8 ms: 1.12x slower                                                   |
| scimark_sparse_mat_mult          | 1.90 ms                                                                 | 2.13 ms: 1.12x slower                                                   |
| meteor_contest                   | 49.7 ms                                                                 | 55.9 ms: 1.13x slower                                                   |
| genshi_text                      | 10.2 ms                                                                 | 11.6 ms: 1.13x slower                                                   |
| mako                             | 5.01 ms                                                                 | 5.70 ms: 1.14x slower                                                   |
| typing_runtime_protocols         | 64.8 us                                                                 | 73.7 us: 1.14x slower                                                   |
| crypto_pyaes                     | 37.4 ms                                                                 | 42.8 ms: 1.14x slower                                                   |
| async_tree_eager                 | 42.6 ms                                                                 | 48.9 ms: 1.15x slower                                                   |
| spectral_norm                    | 43.8 ms                                                                 | 50.8 ms: 1.16x slower                                                   |
| coverage                         | 32.9 ms                                                                 | 40.6 ms: 1.23x slower                                                   |
| bench_thread_pool                | 426 us                                                                  | 557 us: 1.31x slower                                                    |
| Geometric mean                   | (ref)                                                                   | 1.01x slower                                                            |

Benchmark hidden because not significant (4): pylint, fannkuch, bench_mp_pool, sphinx
Ignored benchmarks (8) of results/bm-20250926-3.15.0a0-48d0d0d-NOGIL/bm-20250926-macm4pro-arm64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 88.84% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.12x