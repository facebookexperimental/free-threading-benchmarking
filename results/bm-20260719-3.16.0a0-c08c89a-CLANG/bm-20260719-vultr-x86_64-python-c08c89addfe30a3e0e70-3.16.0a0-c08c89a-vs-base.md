# Results vs. base

- fork: python
- ref: c08c89addfe30a3e0e70
- machine: linux-x86_64
- commit hash: c08c89a
- commit date: 2026-07-19
- overall geometric mean: 1.029x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-CLANG/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                                                          | 254 ms: 1.01x faster                                                                                                  |
| docutils       | 2.42 sec                                                                                                        | 2.36 sec: 1.02x faster                                                                                                |
| html5lib       | 59.9 ms                                                                                                         | 57.5 ms: 1.04x faster                                                                                                 |
| sphinx         | 990 ms                                                                                                          | 971 ms: 1.02x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-CLANG/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_generators           | 337 ms                                                                                                          | 323 ms: 1.05x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 542 ms                                                                                                          | 521 ms: 1.04x faster                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 22.8 ms: 1.03x faster                                                                                                 |
| async_tree_none            | 287 ms                                                                                                          | 280 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 545 ms: 1.02x faster                                                                                                  |
| asyncio_tcp                | 447 ms                                                                                                          | 440 ms: 1.02x faster                                                                                                  |
| asyncio_tcp_ssl            | 1.45 sec                                                                                                        | 1.48 sec: 1.02x slower                                                                                                |
| Geometric mean             | (ref)                                                                                                           | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, async_tree_io, asyncio_websockets, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-CLANG/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| nbody          | 90.8 ms                                                                                                         | 82.3 ms: 1.10x faster                                                                                                 |
| float          | 73.6 ms                                                                                                         | 71.6 ms: 1.03x faster                                                                                                 |
| pidigits       | 195 ms                                                                                                          | 191 ms: 1.02x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.05x faster                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-CLANG/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                                                                          | 143 ms: 1.03x faster                                                                                                  |
| regex_v8       | 21.6 ms                                                                                                         | 22.9 ms: 1.06x slower                                                                                                 |
| regex_dna      | 181 ms                                                                                                          | 196 ms: 1.08x slower                                                                                                  |
| regex_effbot   | 2.57 ms                                                                                                         | 3.25 ms: 1.27x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-CLANG/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| unpickle_list        | 5.48 us                                                                                                         | 4.25 us: 1.29x faster                                                                                                 |
| pickle_dict          | 33.7 us                                                                                                         | 31.2 us: 1.08x faster                                                                                                 |
| unpickle             | 15.3 us                                                                                                         | 14.3 us: 1.07x faster                                                                                                 |
| xml_etree_process    | 60.5 ms                                                                                                         | 56.6 ms: 1.07x faster                                                                                                 |
| json_dumps           | 9.80 ms                                                                                                         | 9.29 ms: 1.06x faster                                                                                                 |
| pickle_list          | 5.51 us                                                                                                         | 5.29 us: 1.04x faster                                                                                                 |
| pickle_pure_python   | 310 us                                                                                                          | 299 us: 1.03x faster                                                                                                  |
| xml_etree_generate   | 85.7 ms                                                                                                         | 82.9 ms: 1.03x faster                                                                                                 |
| unpickle_pure_python | 214 us                                                                                                          | 208 us: 1.03x faster                                                                                                  |
| json_loads           | 27.5 us                                                                                                         | 26.8 us: 1.02x faster                                                                                                 |
| xml_etree_iterparse  | 90.3 ms                                                                                                         | 92.8 ms: 1.03x slower                                                                                                 |
| pickle               | 12.9 us                                                                                                         | 13.7 us: 1.06x slower                                                                                                 |
| xml_etree_parse      | 144 ms                                                                                                          | 159 ms: 1.11x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-CLANG/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                         | 12.5 ms: 1.01x slower                                                                                                 |
| python_startup_no_site | 7.04 ms                                                                                                         | 7.18 ms: 1.02x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.02x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-CLANG/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.0 ms                                                                                                         | 32.7 ms: 1.10x faster                                                                                                 |
| mako            | 12.0 ms                                                                                                         | 12.0 ms: 1.00x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.05x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-CLANG/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| unpickle_list              | 5.48 us                                                                                                         | 4.25 us: 1.29x faster                                                                                                 |
| logging_silent             | 96.1 ns                                                                                                         | 79.5 ns: 1.21x faster                                                                                                 |
| scimark_sparse_mat_mult    | 4.79 ms                                                                                                         | 4.17 ms: 1.15x faster                                                                                                 |
| deltablue                  | 3.28 ms                                                                                                         | 2.86 ms: 1.15x faster                                                                                                 |
| scimark_fft                | 319 ms                                                                                                          | 278 ms: 1.15x faster                                                                                                  |
| comprehensions             | 15.9 us                                                                                                         | 14.3 us: 1.11x faster                                                                                                 |
| nbody                      | 90.8 ms                                                                                                         | 82.3 ms: 1.10x faster                                                                                                 |
| scimark_monte_carlo        | 64.0 ms                                                                                                         | 58.0 ms: 1.10x faster                                                                                                 |
| django_template            | 36.0 ms                                                                                                         | 32.7 ms: 1.10x faster                                                                                                 |
| sqlglot_v2_transpile       | 1.48 ms                                                                                                         | 1.35 ms: 1.10x faster                                                                                                 |
| scimark_lu                 | 114 ms                                                                                                          | 105 ms: 1.09x faster                                                                                                  |
| thrift                     | 796 us                                                                                                          | 728 us: 1.09x faster                                                                                                  |
| spectral_norm              | 92.4 ms                                                                                                         | 84.8 ms: 1.09x faster                                                                                                 |
| logging_simple             | 6.04 us                                                                                                         | 5.56 us: 1.09x faster                                                                                                 |
| richards                   | 42.0 ms                                                                                                         | 38.7 ms: 1.09x faster                                                                                                 |
| deepcopy_reduce            | 2.59 us                                                                                                         | 2.39 us: 1.08x faster                                                                                                 |
| deepcopy                   | 235 us                                                                                                          | 217 us: 1.08x faster                                                                                                  |
| richards_super             | 48.1 ms                                                                                                         | 44.5 ms: 1.08x faster                                                                                                 |
| pickle_dict                | 33.7 us                                                                                                         | 31.2 us: 1.08x faster                                                                                                 |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.07 ms: 1.08x faster                                                                                                 |
| scimark_sor                | 109 ms                                                                                                          | 102 ms: 1.08x faster                                                                                                  |
| deepcopy_memo              | 26.7 us                                                                                                         | 24.9 us: 1.07x faster                                                                                                 |
| unpickle                   | 15.3 us                                                                                                         | 14.3 us: 1.07x faster                                                                                                 |
| xml_etree_process          | 60.5 ms                                                                                                         | 56.6 ms: 1.07x faster                                                                                                 |
| raytrace                   | 253 ms                                                                                                          | 238 ms: 1.07x faster                                                                                                  |
| logging_format             | 6.68 us                                                                                                         | 6.28 us: 1.06x faster                                                                                                 |
| typing_runtime_protocols   | 119 us                                                                                                          | 112 us: 1.06x faster                                                                                                  |
| sqlglot_v2_optimize        | 51.0 ms                                                                                                         | 48.0 ms: 1.06x faster                                                                                                 |
| nqueens                    | 74.4 ms                                                                                                         | 70.1 ms: 1.06x faster                                                                                                 |
| mdp                        | 1.13 sec                                                                                                        | 1.07 sec: 1.06x faster                                                                                                |
| json_dumps                 | 9.80 ms                                                                                                         | 9.29 ms: 1.06x faster                                                                                                 |
| chaos                      | 54.5 ms                                                                                                         | 51.6 ms: 1.05x faster                                                                                                 |
| hexiom                     | 5.71 ms                                                                                                         | 5.42 ms: 1.05x faster                                                                                                 |
| sympy_sum                  | 157 ms                                                                                                          | 150 ms: 1.05x faster                                                                                                  |
| sympy_integrate            | 19.1 ms                                                                                                         | 18.2 ms: 1.05x faster                                                                                                 |
| async_generators           | 337 ms                                                                                                          | 323 ms: 1.05x faster                                                                                                  |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.28 ms: 1.04x faster                                                                                                 |
| sqlglot_v2_normalize       | 100 ms                                                                                                          | 96.2 ms: 1.04x faster                                                                                                 |
| sympy_str                  | 274 ms                                                                                                          | 263 ms: 1.04x faster                                                                                                  |
| pathlib                    | 17.9 ms                                                                                                         | 17.2 ms: 1.04x faster                                                                                                 |
| html5lib                   | 59.9 ms                                                                                                         | 57.5 ms: 1.04x faster                                                                                                 |
| pickle_list                | 5.51 us                                                                                                         | 5.29 us: 1.04x faster                                                                                                 |
| async_tree_cpu_io_mixed    | 542 ms                                                                                                          | 521 ms: 1.04x faster                                                                                                  |
| go                         | 105 ms                                                                                                          | 101 ms: 1.04x faster                                                                                                  |
| sympy_expand               | 461 ms                                                                                                          | 444 ms: 1.04x faster                                                                                                  |
| coverage                   | 83.5 ms                                                                                                         | 80.6 ms: 1.04x faster                                                                                                 |
| pickle_pure_python         | 310 us                                                                                                          | 299 us: 1.03x faster                                                                                                  |
| xml_etree_generate         | 85.7 ms                                                                                                         | 82.9 ms: 1.03x faster                                                                                                 |
| telco                      | 159 ms                                                                                                          | 154 ms: 1.03x faster                                                                                                  |
| regex_compile              | 148 ms                                                                                                          | 143 ms: 1.03x faster                                                                                                  |
| subparsers                 | 9.41 ms                                                                                                         | 9.12 ms: 1.03x faster                                                                                                 |
| unpickle_pure_python       | 214 us                                                                                                          | 208 us: 1.03x faster                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 22.8 ms: 1.03x faster                                                                                                 |
| pyflate                    | 402 ms                                                                                                          | 391 ms: 1.03x faster                                                                                                  |
| float                      | 73.6 ms                                                                                                         | 71.6 ms: 1.03x faster                                                                                                 |
| shortest_path              | 443 ms                                                                                                          | 431 ms: 1.03x faster                                                                                                  |
| json_loads                 | 27.5 us                                                                                                         | 26.8 us: 1.02x faster                                                                                                 |
| async_tree_none            | 287 ms                                                                                                          | 280 ms: 1.02x faster                                                                                                  |
| docutils                   | 2.42 sec                                                                                                        | 2.36 sec: 1.02x faster                                                                                                |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 4.09 sec: 1.02x faster                                                                                                |
| pylint                     | 113 ms                                                                                                          | 111 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 545 ms: 1.02x faster                                                                                                  |
| generators                 | 29.0 ms                                                                                                         | 28.4 ms: 1.02x faster                                                                                                 |
| sphinx                     | 990 ms                                                                                                          | 971 ms: 1.02x faster                                                                                                  |
| pprint_safe_repr           | 724 ms                                                                                                          | 711 ms: 1.02x faster                                                                                                  |
| fannkuch                   | 374 ms                                                                                                          | 368 ms: 1.02x faster                                                                                                  |
| pidigits                   | 195 ms                                                                                                          | 191 ms: 1.02x faster                                                                                                  |
| pprint_pformat             | 1.46 sec                                                                                                        | 1.44 sec: 1.02x faster                                                                                                |
| asyncio_tcp                | 447 ms                                                                                                          | 440 ms: 1.02x faster                                                                                                  |
| dulwich_log                | 68.6 ms                                                                                                         | 67.6 ms: 1.01x faster                                                                                                 |
| sqlite_synth               | 2.22 us                                                                                                         | 2.19 us: 1.01x faster                                                                                                 |
| 2to3                       | 256 ms                                                                                                          | 254 ms: 1.01x faster                                                                                                  |
| connected_components       | 397 ms                                                                                                          | 393 ms: 1.01x faster                                                                                                  |
| many_optionals             | 910 us                                                                                                          | 901 us: 1.01x faster                                                                                                  |
| crypto_pyaes               | 69.4 ms                                                                                                         | 69.6 ms: 1.00x slower                                                                                                 |
| mako                       | 12.0 ms                                                                                                         | 12.0 ms: 1.00x slower                                                                                                 |
| python_startup             | 12.4 ms                                                                                                         | 12.5 ms: 1.01x slower                                                                                                 |
| asyncio_tcp_ssl            | 1.45 sec                                                                                                        | 1.48 sec: 1.02x slower                                                                                                |
| python_startup_no_site     | 7.04 ms                                                                                                         | 7.18 ms: 1.02x slower                                                                                                 |
| unpack_sequence            | 40.3 ns                                                                                                         | 41.4 ns: 1.03x slower                                                                                                 |
| xml_etree_iterparse        | 90.3 ms                                                                                                         | 92.8 ms: 1.03x slower                                                                                                 |
| pycparser                  | 1.10 sec                                                                                                        | 1.14 sec: 1.04x slower                                                                                                |
| json                       | 4.95 ms                                                                                                         | 5.15 ms: 1.04x slower                                                                                                 |
| meteor_contest             | 99.8 ms                                                                                                         | 104 ms: 1.04x slower                                                                                                  |
| pickle                     | 12.9 us                                                                                                         | 13.7 us: 1.06x slower                                                                                                 |
| regex_v8                   | 21.6 ms                                                                                                         | 22.9 ms: 1.06x slower                                                                                                 |
| regex_dna                  | 181 ms                                                                                                          | 196 ms: 1.08x slower                                                                                                  |
| create_gc_cycles           | 1.67 ms                                                                                                         | 1.81 ms: 1.08x slower                                                                                                 |
| xml_etree_parse            | 144 ms                                                                                                          | 159 ms: 1.11x slower                                                                                                  |
| gc_traversal               | 4.04 ms                                                                                                         | 4.51 ms: 1.12x slower                                                                                                 |
| regex_effbot               | 2.57 ms                                                                                                         | 3.25 ms: 1.27x slower                                                                                                 |
| bench_mp_pool              | 274 ms                                                                                                          | 354 ms: 1.29x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, k_core, async_tree_io, asyncio_websockets, tomli_loads, async_tree_io_tg

- Geometric mean (including insignificant results): 1.029x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.03x