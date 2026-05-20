# Results vs. 3.12.6

- fork: python
- ref: de9c32fc34fe2e000de1
- machine: darwin-arm64
- commit hash: de9c32f
- commit date: 2026-05-20
- overall geometric mean: 1.123x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 971 ms: 1.05x faster                                                    |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                   |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 308 ms: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 119 ms: 1.49x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 310 ms: 1.48x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 329 ms: 1.46x faster                                                    |
| async_generators                 | 206 ms                                                   | 146 ms: 1.42x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.38x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 336 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 275 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 286 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.7 ms: 1.12x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 257 ms: 1.21x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 151 ms: 1.34x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 102 ms: 3.18x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.4 ms: 1.25x faster                                                   |
| nbody          | 54.2 ms                                                  | 45.4 ms: 1.19x faster                                                   |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                    | 1.14x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 47.1 ms: 1.16x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.8 ms: 1.06x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.71 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.3 ms: 1.19x faster                                                   |
| tomli_loads          | 957 ms                                                   | 831 ms: 1.15x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 66.5 ms: 1.02x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 102 us: 1.00x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.06x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.11 ms: 5.05x faster                                                   |
| pylint                           | 128 ms                                                   | 57.0 ms: 2.25x faster                                                   |
| mdp                              | 1.09 sec                                                 | 516 ms: 2.11x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 308 ms: 1.61x faster                                                    |
| deepcopy                         | 161 us                                                   | 101 us: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 119 ms: 1.49x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 310 ms: 1.48x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 329 ms: 1.46x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.45x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 49.9 us: 1.42x faster                                                   |
| async_generators                 | 206 ms                                                   | 146 ms: 1.42x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.38x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.30 us: 1.35x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 336 ms: 1.33x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.31x faster                                                   |
| go                               | 70.0 ms                                                  | 53.9 ms: 1.30x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.27x faster                                                    |
| float                            | 37.9 ms                                                  | 30.4 ms: 1.25x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.4 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.22x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.22x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.1 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 275 ms: 1.21x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.3 ns: 1.20x faster                                                   |
| nbody                            | 54.2 ms                                                  | 45.4 ms: 1.19x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.3 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 286 ms: 1.19x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.1 ms: 1.16x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.0 ms: 1.16x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 831 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.50 us: 1.12x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 40.7 ms: 1.12x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.31 us: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.2 ms: 1.10x faster                                                   |
| generators                       | 21.9 ms                                                  | 20.0 ms: 1.10x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.10x faster                                                  |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.89 ms: 1.10x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.80 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.54 ms: 1.06x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 93.8 ms: 1.06x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.3 ms: 1.05x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.1 ms: 1.05x faster                                                   |
| docutils                         | 1.02 sec                                                 | 971 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 313 ms: 1.05x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 638 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.94 ms: 1.03x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 936 ns: 1.03x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.3 ms: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 487 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 66.5 ms: 1.02x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| thrift                           | 322 us                                                   | 319 us: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 102 us: 1.00x faster                                                    |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.71 ms: 1.01x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 52.5 ms: 1.02x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.2 ms: 1.03x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.03x slower                                                    |
| shortest_path                    | 219 ms                                                   | 227 ms: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                    |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 40.6 ms: 1.05x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 869 us: 1.05x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.86 ms: 1.10x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 46.4 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 257 ms: 1.21x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 242 us: 1.24x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 57.9 ms: 1.33x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 151 ms: 1.34x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 102 ms: 3.18x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260520-3.16.0a0-de9c32f/bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.123x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.20x