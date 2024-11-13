# Results vs. 3.13.0rc2

- fork: Eclips4
- ref: ft_specialize_unpack
- machine: linux-x86_64
- commit hash: d49e9e6
- commit date: 2024-11-08
- overall geometric mean: 1.54x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.38x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 395 ms: 1.52x slower                                                    |
| docutils       | 2.62 sec                                                     | 3.36 sec: 1.28x slower                                                  |
| html5lib       | 67.0 ms                                                      | 106 ms: 1.59x slower                                                    |
| Geometric mean | (ref)                                                        | 1.46x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| asyncio_tcp      | 505 ms                                                       | 583 ms: 1.15x slower                                                    |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.84 sec: 1.22x slower                                                  |
| async_generators | 377 ms                                                       | 494 ms: 1.31x slower                                                    |
| coroutines       | 23.6 ms                                                      | 31.7 ms: 1.35x slower                                                   |
| Geometric mean   | (ref)                                                        | 1.20x slower                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                    |
| float          | 77.5 ms                                                      | 152 ms: 1.96x slower                                                    |
| nbody          | 85.1 ms                                                      | 171 ms: 2.01x slower                                                    |
| Geometric mean | (ref)                                                        | 1.50x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.03 ms: 1.02x faster                                                   |
| regex_dna      | 180 ms                                                       | 185 ms: 1.02x slower                                                    |
| regex_v8       | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                   |
| regex_compile  | 132 ms                                                       | 227 ms: 1.72x slower                                                    |
| Geometric mean | (ref)                                                        | 1.18x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 31.6 us: 1.03x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.02x faster                                                    |
| unpickle             | 14.3 us                                                      | 15.0 us: 1.05x slower                                                   |
| pickle_list          | 4.93 us                                                      | 5.16 us: 1.05x slower                                                   |
| pickle               | 11.3 us                                                      | 12.0 us: 1.06x slower                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 103 ms: 1.09x slower                                                    |
| unpickle_list        | 4.71 us                                                      | 5.13 us: 1.09x slower                                                   |
| json_loads           | 27.0 us                                                      | 29.8 us: 1.10x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 114 ms: 1.34x slower                                                    |
| json_dumps           | 10.5 ms                                                      | 15.3 ms: 1.45x slower                                                   |
| xml_etree_process    | 59.3 ms                                                      | 93.0 ms: 1.57x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 3.18 sec: 1.58x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 429 us: 2.04x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 618 us: 2.10x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.27x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                   |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 79.3 ms: 1.63x slower                                                   |
| mako            | 11.3 ms                                                      | 20.7 ms: 1.83x slower                                                   |
| genshi_text     | 21.5 ms                                                      | 40.0 ms: 1.86x slower                                                   |
| django_template | 34.1 ms                                                      | 65.0 ms: 1.90x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.80x slower                                                            |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|--------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.55 ms: 1.23x faster                                                   |
| create_gc_cycles         | 1.34 ms                                                      | 1.11 ms: 1.21x faster                                                   |
| pidigits                 | 217 ms                                                       | 185 ms: 1.17x faster                                                    |
| pickle_dict              | 32.5 us                                                      | 31.6 us: 1.03x faster                                                   |
| xml_etree_parse          | 136 ms                                                       | 133 ms: 1.02x faster                                                    |
| regex_effbot             | 3.08 ms                                                      | 3.03 ms: 1.02x faster                                                   |
| regex_dna                | 180 ms                                                       | 185 ms: 1.02x slower                                                    |
| unpickle                 | 14.3 us                                                      | 15.0 us: 1.05x slower                                                   |
| pickle_list              | 4.93 us                                                      | 5.16 us: 1.05x slower                                                   |
| pickle                   | 11.3 us                                                      | 12.0 us: 1.06x slower                                                   |
| xml_etree_iterparse      | 94.9 ms                                                      | 103 ms: 1.09x slower                                                    |
| unpickle_list            | 4.71 us                                                      | 5.13 us: 1.09x slower                                                   |
| json                     | 4.93 ms                                                      | 5.43 ms: 1.10x slower                                                   |
| regex_v8                 | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                   |
| json_loads               | 27.0 us                                                      | 29.8 us: 1.10x slower                                                   |
| sqlite_synth             | 2.21 us                                                      | 2.47 us: 1.12x slower                                                   |
| pathlib                  | 19.2 ms                                                      | 22.0 ms: 1.15x slower                                                   |
| asyncio_tcp              | 505 ms                                                       | 583 ms: 1.15x slower                                                    |
| telco                    | 7.82 ms                                                      | 9.22 ms: 1.18x slower                                                   |
| scimark_fft              | 349 ms                                                       | 416 ms: 1.19x slower                                                    |
| deepcopy                 | 355 us                                                       | 424 us: 1.19x slower                                                    |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.84 sec: 1.22x slower                                                  |
| coverage                 | 83.0 ms                                                      | 103 ms: 1.25x slower                                                    |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.92 ms: 1.26x slower                                                   |
| mdp                      | 2.36 sec                                                     | 2.97 sec: 1.26x slower                                                  |
| docutils                 | 2.62 sec                                                     | 3.36 sec: 1.28x slower                                                  |
| async_generators         | 377 ms                                                       | 494 ms: 1.31x slower                                                    |
| spectral_norm            | 111 ms                                                       | 147 ms: 1.32x slower                                                    |
| pylint                   | 317 ms                                                       | 421 ms: 1.33x slower                                                    |
| xml_etree_generate       | 85.4 ms                                                      | 114 ms: 1.34x slower                                                    |
| coroutines               | 23.6 ms                                                      | 31.7 ms: 1.35x slower                                                   |
| deepcopy_memo            | 39.1 us                                                      | 53.5 us: 1.37x slower                                                   |
| bpe_tokeniser            | 4.45 sec                                                     | 6.12 sec: 1.38x slower                                                  |
| python_startup_no_site   | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                   |
| dulwich_log              | 74.8 ms                                                      | 104 ms: 1.38x slower                                                    |
| meteor_contest           | 102 ms                                                       | 141 ms: 1.39x slower                                                    |
| python_startup           | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                   |
| generators               | 28.8 ms                                                      | 41.2 ms: 1.43x slower                                                   |
| json_dumps               | 10.5 ms                                                      | 15.3 ms: 1.45x slower                                                   |
| deepcopy_reduce          | 3.11 us                                                      | 4.53 us: 1.46x slower                                                   |
| unpack_sequence          | 44.8 ns                                                      | 65.8 ns: 1.47x slower                                                   |
| nqueens                  | 78.6 ms                                                      | 117 ms: 1.49x slower                                                    |
| fannkuch                 | 370 ms                                                       | 562 ms: 1.52x slower                                                    |
| 2to3                     | 260 ms                                                       | 395 ms: 1.52x slower                                                    |
| pycparser                | 1.12 sec                                                     | 1.72 sec: 1.54x slower                                                  |
| xml_etree_process        | 59.3 ms                                                      | 93.0 ms: 1.57x slower                                                   |
| tomli_loads              | 2.01 sec                                                     | 3.18 sec: 1.58x slower                                                  |
| html5lib                 | 67.0 ms                                                      | 106 ms: 1.59x slower                                                    |
| crypto_pyaes             | 67.9 ms                                                      | 108 ms: 1.60x slower                                                    |
| genshi_xml               | 48.8 ms                                                      | 79.3 ms: 1.63x slower                                                   |
| typing_runtime_protocols | 155 us                                                       | 254 us: 1.64x slower                                                    |
| sympy_integrate          | 19.8 ms                                                      | 32.9 ms: 1.66x slower                                                   |
| sqlglot_normalize        | 106 ms                                                       | 176 ms: 1.67x slower                                                    |
| thrift                   | 778 us                                                       | 1.30 ms: 1.68x slower                                                   |
| sqlglot_optimize         | 52.7 ms                                                      | 89.1 ms: 1.69x slower                                                   |
| regex_compile            | 132 ms                                                       | 227 ms: 1.72x slower                                                    |
| pyflate                  | 449 ms                                                       | 773 ms: 1.72x slower                                                    |
| pprint_safe_repr         | 738 ms                                                       | 1.29 sec: 1.75x slower                                                  |
| pprint_pformat           | 1.50 sec                                                     | 2.68 sec: 1.79x slower                                                  |
| mako                     | 11.3 ms                                                      | 20.7 ms: 1.83x slower                                                   |
| genshi_text              | 21.5 ms                                                      | 40.0 ms: 1.86x slower                                                   |
| comprehensions           | 16.5 us                                                      | 30.9 us: 1.88x slower                                                   |
| scimark_sor              | 134 ms                                                       | 254 ms: 1.89x slower                                                    |
| django_template          | 34.1 ms                                                      | 65.0 ms: 1.90x slower                                                   |
| sympy_str                | 275 ms                                                       | 528 ms: 1.92x slower                                                    |
| scimark_monte_carlo      | 65.4 ms                                                      | 127 ms: 1.95x slower                                                    |
| float                    | 77.5 ms                                                      | 152 ms: 1.96x slower                                                    |
| nbody                    | 85.1 ms                                                      | 171 ms: 2.01x slower                                                    |
| richards                 | 45.2 ms                                                      | 91.4 ms: 2.02x slower                                                   |
| logging_format           | 6.84 us                                                      | 13.9 us: 2.03x slower                                                   |
| logging_simple           | 6.16 us                                                      | 12.5 us: 2.03x slower                                                   |
| unpickle_pure_python     | 210 us                                                       | 429 us: 2.04x slower                                                    |
| hexiom                   | 5.99 ms                                                      | 12.5 ms: 2.09x slower                                                   |
| pickle_pure_python       | 294 us                                                       | 618 us: 2.10x slower                                                    |
| sqlglot_transpile        | 1.56 ms                                                      | 3.30 ms: 2.11x slower                                                   |
| chaos                    | 57.3 ms                                                      | 122 ms: 2.13x slower                                                    |
| richards_super           | 51.6 ms                                                      | 110 ms: 2.13x slower                                                    |
| logging_silent           | 103 ns                                                       | 222 ns: 2.16x slower                                                    |
| scimark_lu               | 113 ms                                                       | 244 ms: 2.17x slower                                                    |
| go                       | 141 ms                                                       | 312 ms: 2.22x slower                                                    |
| sqlglot_parse            | 1.25 ms                                                      | 2.83 ms: 2.27x slower                                                   |
| sympy_expand             | 457 ms                                                       | 1.05 sec: 2.29x slower                                                  |
| sympy_sum                | 156 ms                                                       | 374 ms: 2.41x slower                                                    |
| raytrace                 | 253 ms                                                       | 628 ms: 2.48x slower                                                    |
| deltablue                | 3.12 ms                                                      | 9.30 ms: 2.98x slower                                                   |
| bench_thread_pool        | 919 us                                                       | 3.47 ms: 3.77x slower                                                   |
| bench_mp_pool            | 11.0 ms                                                      | 72.4 ms: 6.58x slower                                                   |
| Geometric mean           | (ref)                                                        | 1.54x slower                                                            |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.47x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.38x

# Memory
- memory change: 1.22x