# Results vs. base

- fork: python
- ref: c08c89addfe30a3e0e70
- machine: linux-x86_64
- commit hash: c08c89a
- commit date: 2026-07-19
- overall geometric mean: 1.089x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-JIT/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| docutils       | 2.42 sec                                                                                                        | 2.50 sec: 1.03x slower                                                                                              |
| Geometric mean | (ref)                                                                                                           | 1.01x slower                                                                                                        |

Benchmark hidden because not significant (3): 2to3, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-JIT/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| async_tree_none            | 287 ms                                                                                                          | 266 ms: 1.08x faster                                                                                                |
| async_tree_memoization     | 371 ms                                                                                                          | 347 ms: 1.07x faster                                                                                                |
| async_tree_memoization_tg  | 360 ms                                                                                                          | 341 ms: 1.05x faster                                                                                                |
| async_tree_none_tg         | 295 ms                                                                                                          | 282 ms: 1.04x faster                                                                                                |
| async_tree_cpu_io_mixed    | 542 ms                                                                                                          | 520 ms: 1.04x faster                                                                                                |
| async_tree_io_tg           | 752 ms                                                                                                          | 722 ms: 1.04x faster                                                                                                |
| async_tree_io              | 707 ms                                                                                                          | 680 ms: 1.04x faster                                                                                                |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 537 ms: 1.03x faster                                                                                                |
| async_generators           | 337 ms                                                                                                          | 352 ms: 1.04x slower                                                                                                |
| coroutines                 | 23.4 ms                                                                                                         | 24.7 ms: 1.05x slower                                                                                               |
| Geometric mean             | (ref)                                                                                                           | 1.02x faster                                                                                                        |

Benchmark hidden because not significant (3): asyncio_websockets, asyncio_tcp_ssl, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-JIT/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| nbody          | 90.8 ms                                                                                                         | 63.6 ms: 1.43x faster                                                                                               |
| float          | 73.6 ms                                                                                                         | 55.8 ms: 1.32x faster                                                                                               |
| pidigits       | 195 ms                                                                                                          | 184 ms: 1.06x faster                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.26x faster                                                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-JIT/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 181 ms                                                                                                          | 166 ms: 1.09x faster                                                                                                |
| regex_compile  | 148 ms                                                                                                          | 143 ms: 1.03x faster                                                                                                |
| regex_v8       | 21.6 ms                                                                                                         | 21.5 ms: 1.01x faster                                                                                               |
| regex_effbot   | 2.57 ms                                                                                                         | 2.64 ms: 1.03x slower                                                                                               |
| Geometric mean | (ref)                                                                                                           | 1.02x faster                                                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-JIT/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python | 214 us                                                                                                          | 182 us: 1.17x faster                                                                                                |
| pickle_pure_python   | 310 us                                                                                                          | 266 us: 1.17x faster                                                                                                |
| xml_etree_process    | 60.5 ms                                                                                                         | 55.4 ms: 1.09x faster                                                                                               |
| json_dumps           | 9.80 ms                                                                                                         | 9.13 ms: 1.07x faster                                                                                               |
| xml_etree_generate   | 85.7 ms                                                                                                         | 81.3 ms: 1.05x faster                                                                                               |
| unpickle             | 15.3 us                                                                                                         | 14.7 us: 1.04x faster                                                                                               |
| xml_etree_iterparse  | 90.3 ms                                                                                                         | 86.7 ms: 1.04x faster                                                                                               |
| unpickle_list        | 5.48 us                                                                                                         | 5.29 us: 1.04x faster                                                                                               |
| json_loads           | 27.5 us                                                                                                         | 26.6 us: 1.03x faster                                                                                               |
| xml_etree_parse      | 144 ms                                                                                                          | 141 ms: 1.02x faster                                                                                                |
| tomli_loads          | 1.81 sec                                                                                                        | 1.79 sec: 1.01x faster                                                                                              |
| pickle               | 12.9 us                                                                                                         | 13.2 us: 1.02x slower                                                                                               |
| pickle_list          | 5.51 us                                                                                                         | 5.64 us: 1.02x slower                                                                                               |
| pickle_dict          | 33.7 us                                                                                                         | 34.6 us: 1.03x slower                                                                                               |
| Geometric mean       | (ref)                                                                                                           | 1.05x faster                                                                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-JIT/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                         | 12.5 ms: 1.01x slower                                                                                               |
| python_startup_no_site | 7.04 ms                                                                                                         | 7.15 ms: 1.02x slower                                                                                               |
| Geometric mean         | (ref)                                                                                                           | 1.01x slower                                                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-JIT/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| mako            | 12.0 ms                                                                                                         | 10.1 ms: 1.18x faster                                                                                               |
| django_template | 36.0 ms                                                                                                         | 38.7 ms: 1.07x slower                                                                                               |
| Geometric mean  | (ref)                                                                                                           | 1.05x faster                                                                                                        |

All benchmarks:
===============

| Benchmark                  | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-JIT/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| richards_super             | 48.1 ms                                                                                                         | 20.3 ms: 2.38x faster                                                                                               |
| richards                   | 42.0 ms                                                                                                         | 18.2 ms: 2.31x faster                                                                                               |
| nbody                      | 90.8 ms                                                                                                         | 63.6 ms: 1.43x faster                                                                                               |
| scimark_sor                | 109 ms                                                                                                          | 77.8 ms: 1.41x faster                                                                                               |
| scimark_lu                 | 114 ms                                                                                                          | 81.7 ms: 1.40x faster                                                                                               |
| bench_mp_pool              | 274 ms                                                                                                          | 197 ms: 1.39x faster                                                                                                |
| spectral_norm              | 92.4 ms                                                                                                         | 68.6 ms: 1.35x faster                                                                                               |
| float                      | 73.6 ms                                                                                                         | 55.8 ms: 1.32x faster                                                                                               |
| scimark_monte_carlo        | 64.0 ms                                                                                                         | 51.4 ms: 1.24x faster                                                                                               |
| deltablue                  | 3.28 ms                                                                                                         | 2.65 ms: 1.24x faster                                                                                               |
| deepcopy_memo              | 26.7 us                                                                                                         | 21.7 us: 1.23x faster                                                                                               |
| scimark_fft                | 319 ms                                                                                                          | 259 ms: 1.23x faster                                                                                                |
| mako                       | 12.0 ms                                                                                                         | 10.1 ms: 1.18x faster                                                                                               |
| pprint_safe_repr           | 724 ms                                                                                                          | 615 ms: 1.18x faster                                                                                                |
| unpickle_pure_python       | 214 us                                                                                                          | 182 us: 1.17x faster                                                                                                |
| telco                      | 159 ms                                                                                                          | 136 ms: 1.17x faster                                                                                                |
| pyflate                    | 402 ms                                                                                                          | 345 ms: 1.17x faster                                                                                                |
| pickle_pure_python         | 310 us                                                                                                          | 266 us: 1.17x faster                                                                                                |
| pprint_pformat             | 1.46 sec                                                                                                        | 1.26 sec: 1.16x faster                                                                                              |
| logging_simple             | 6.04 us                                                                                                         | 5.24 us: 1.15x faster                                                                                               |
| nqueens                    | 74.4 ms                                                                                                         | 64.9 ms: 1.15x faster                                                                                               |
| gc_traversal               | 4.04 ms                                                                                                         | 3.53 ms: 1.14x faster                                                                                               |
| fannkuch                   | 374 ms                                                                                                          | 331 ms: 1.13x faster                                                                                                |
| typing_runtime_protocols   | 119 us                                                                                                          | 106 us: 1.13x faster                                                                                                |
| chaos                      | 54.5 ms                                                                                                         | 48.4 ms: 1.12x faster                                                                                               |
| scimark_sparse_mat_mult    | 4.79 ms                                                                                                         | 4.29 ms: 1.12x faster                                                                                               |
| comprehensions             | 15.9 us                                                                                                         | 14.3 us: 1.11x faster                                                                                               |
| logging_format             | 6.68 us                                                                                                         | 6.04 us: 1.11x faster                                                                                               |
| xml_etree_process          | 60.5 ms                                                                                                         | 55.4 ms: 1.09x faster                                                                                               |
| regex_dna                  | 181 ms                                                                                                          | 166 ms: 1.09x faster                                                                                                |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.07 ms: 1.08x faster                                                                                               |
| async_tree_none            | 287 ms                                                                                                          | 266 ms: 1.08x faster                                                                                                |
| sqlglot_v2_transpile       | 1.48 ms                                                                                                         | 1.38 ms: 1.07x faster                                                                                               |
| json_dumps                 | 9.80 ms                                                                                                         | 9.13 ms: 1.07x faster                                                                                               |
| crypto_pyaes               | 69.4 ms                                                                                                         | 64.7 ms: 1.07x faster                                                                                               |
| connected_components       | 397 ms                                                                                                          | 371 ms: 1.07x faster                                                                                                |
| async_tree_memoization     | 371 ms                                                                                                          | 347 ms: 1.07x faster                                                                                                |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 3.93 sec: 1.07x faster                                                                                              |
| subparsers                 | 9.41 ms                                                                                                         | 8.84 ms: 1.06x faster                                                                                               |
| pathlib                    | 17.9 ms                                                                                                         | 16.9 ms: 1.06x faster                                                                                               |
| pidigits                   | 195 ms                                                                                                          | 184 ms: 1.06x faster                                                                                                |
| go                         | 105 ms                                                                                                          | 99.0 ms: 1.06x faster                                                                                               |
| xml_etree_generate         | 85.7 ms                                                                                                         | 81.3 ms: 1.05x faster                                                                                               |
| async_tree_memoization_tg  | 360 ms                                                                                                          | 341 ms: 1.05x faster                                                                                                |
| sqlite_synth               | 2.22 us                                                                                                         | 2.11 us: 1.05x faster                                                                                               |
| shortest_path              | 443 ms                                                                                                          | 422 ms: 1.05x faster                                                                                                |
| sqlglot_v2_normalize       | 100 ms                                                                                                          | 95.7 ms: 1.05x faster                                                                                               |
| unpickle                   | 15.3 us                                                                                                         | 14.7 us: 1.04x faster                                                                                               |
| async_tree_none_tg         | 295 ms                                                                                                          | 282 ms: 1.04x faster                                                                                                |
| async_tree_cpu_io_mixed    | 542 ms                                                                                                          | 520 ms: 1.04x faster                                                                                                |
| sqlglot_v2_optimize        | 51.0 ms                                                                                                         | 48.9 ms: 1.04x faster                                                                                               |
| meteor_contest             | 99.8 ms                                                                                                         | 95.9 ms: 1.04x faster                                                                                               |
| xml_etree_iterparse        | 90.3 ms                                                                                                         | 86.7 ms: 1.04x faster                                                                                               |
| async_tree_io_tg           | 752 ms                                                                                                          | 722 ms: 1.04x faster                                                                                                |
| async_tree_io              | 707 ms                                                                                                          | 680 ms: 1.04x faster                                                                                                |
| unpickle_list              | 5.48 us                                                                                                         | 5.29 us: 1.04x faster                                                                                               |
| regex_compile              | 148 ms                                                                                                          | 143 ms: 1.03x faster                                                                                                |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 537 ms: 1.03x faster                                                                                                |
| json_loads                 | 27.5 us                                                                                                         | 26.6 us: 1.03x faster                                                                                               |
| create_gc_cycles           | 1.67 ms                                                                                                         | 1.63 ms: 1.03x faster                                                                                               |
| raytrace                   | 253 ms                                                                                                          | 247 ms: 1.03x faster                                                                                                |
| json                       | 4.95 ms                                                                                                         | 4.85 ms: 1.02x faster                                                                                               |
| xml_etree_parse            | 144 ms                                                                                                          | 141 ms: 1.02x faster                                                                                                |
| deepcopy                   | 235 us                                                                                                          | 231 us: 1.02x faster                                                                                                |
| deepcopy_reduce            | 2.59 us                                                                                                         | 2.54 us: 1.02x faster                                                                                               |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.32 ms: 1.02x faster                                                                                               |
| thrift                     | 796 us                                                                                                          | 784 us: 1.02x faster                                                                                                |
| tomli_loads                | 1.81 sec                                                                                                        | 1.79 sec: 1.01x faster                                                                                              |
| sympy_expand               | 461 ms                                                                                                          | 458 ms: 1.01x faster                                                                                                |
| regex_v8                   | 21.6 ms                                                                                                         | 21.5 ms: 1.01x faster                                                                                               |
| hexiom                     | 5.71 ms                                                                                                         | 5.68 ms: 1.00x faster                                                                                               |
| pylint                     | 113 ms                                                                                                          | 112 ms: 1.00x faster                                                                                                |
| python_startup             | 12.4 ms                                                                                                         | 12.5 ms: 1.01x slower                                                                                               |
| python_startup_no_site     | 7.04 ms                                                                                                         | 7.15 ms: 1.02x slower                                                                                               |
| pickle                     | 12.9 us                                                                                                         | 13.2 us: 1.02x slower                                                                                               |
| pycparser                  | 1.10 sec                                                                                                        | 1.13 sec: 1.02x slower                                                                                              |
| pickle_list                | 5.51 us                                                                                                         | 5.64 us: 1.02x slower                                                                                               |
| pickle_dict                | 33.7 us                                                                                                         | 34.6 us: 1.03x slower                                                                                               |
| regex_effbot               | 2.57 ms                                                                                                         | 2.64 ms: 1.03x slower                                                                                               |
| docutils                   | 2.42 sec                                                                                                        | 2.50 sec: 1.03x slower                                                                                              |
| many_optionals             | 910 us                                                                                                          | 942 us: 1.03x slower                                                                                                |
| dulwich_log                | 68.6 ms                                                                                                         | 71.1 ms: 1.04x slower                                                                                               |
| sympy_integrate            | 19.1 ms                                                                                                         | 19.8 ms: 1.04x slower                                                                                               |
| async_generators           | 337 ms                                                                                                          | 352 ms: 1.04x slower                                                                                                |
| sympy_str                  | 274 ms                                                                                                          | 286 ms: 1.04x slower                                                                                                |
| generators                 | 29.0 ms                                                                                                         | 30.5 ms: 1.05x slower                                                                                               |
| coroutines                 | 23.4 ms                                                                                                         | 24.7 ms: 1.05x slower                                                                                               |
| sympy_sum                  | 157 ms                                                                                                          | 167 ms: 1.06x slower                                                                                                |
| django_template            | 36.0 ms                                                                                                         | 38.7 ms: 1.07x slower                                                                                               |
| mdp                        | 1.13 sec                                                                                                        | 1.23 sec: 1.09x slower                                                                                              |
| k_core                     | 2.07 sec                                                                                                        | 2.30 sec: 1.11x slower                                                                                              |
| unpack_sequence            | 40.3 ns                                                                                                         | 65.8 ns: 1.63x slower                                                                                               |
| Geometric mean             | (ref)                                                                                                           | 1.08x faster                                                                                                        |

Benchmark hidden because not significant (8): coverage, sphinx, asyncio_websockets, asyncio_tcp_ssl, html5lib, 2to3, logging_silent, asyncio_tcp

- Geometric mean (including insignificant results): 1.089x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.05x