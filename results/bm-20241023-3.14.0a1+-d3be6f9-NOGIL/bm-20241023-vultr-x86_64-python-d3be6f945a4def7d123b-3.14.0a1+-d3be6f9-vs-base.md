# Results vs. base

- fork: python
- ref: d3be6f945a4def7d123b
- machine: linux-x86_64
- commit hash: d3be6f9
- commit date: 2024-10-23
- overall geometric mean: 1.54x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.43x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241023-3.14.0a1+-d3be6f9/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json | results/bm-20241023-3.14.0a1+-d3be6f9-NOGIL/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                                                            | 414 ms: 1.64x slower                                                                                                    |
| docutils       | 2.60 sec                                                                                                          | 3.34 sec: 1.28x slower                                                                                                  |
| html5lib       | 63.2 ms                                                                                                           | 103 ms: 1.63x slower                                                                                                    |
| tornado_http   | 113 ms                                                                                                            | 162 ms: 1.44x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.49x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | results/bm-20241023-3.14.0a1+-d3be6f9/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json | results/bm-20241023-3.14.0a1+-d3be6f9-NOGIL/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json |
|------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_tcp      | 503 ms                                                                                                            | 582 ms: 1.16x slower                                                                                                    |
| asyncio_tcp_ssl  | 1.52 sec                                                                                                          | 1.78 sec: 1.17x slower                                                                                                  |
| async_generators | 373 ms                                                                                                            | 495 ms: 1.33x slower                                                                                                    |
| coroutines       | 22.3 ms                                                                                                           | 32.0 ms: 1.44x slower                                                                                                   |
| Geometric mean   | (ref)                                                                                                             | 1.21x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241023-3.14.0a1+-d3be6f9/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json | results/bm-20241023-3.14.0a1+-d3be6f9-NOGIL/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                                                            | 186 ms: 1.00x slower                                                                                                    |
| float          | 78.4 ms                                                                                                           | 153 ms: 1.95x slower                                                                                                    |
| nbody          | 99.4 ms                                                                                                           | 219 ms: 2.21x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.63x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241023-3.14.0a1+-d3be6f9/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json | results/bm-20241023-3.14.0a1+-d3be6f9-NOGIL/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 3.13 ms                                                                                                           | 3.07 ms: 1.02x faster                                                                                                   |
| regex_dna      | 181 ms                                                                                                            | 183 ms: 1.01x slower                                                                                                    |
| regex_v8       | 24.8 ms                                                                                                           | 26.2 ms: 1.05x slower                                                                                                   |
| regex_compile  | 131 ms                                                                                                            | 228 ms: 1.74x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241023-3.14.0a1+-d3be6f9/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json | results/bm-20241023-3.14.0a1+-d3be6f9-NOGIL/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pickle_list          | 4.88 us                                                                                                           | 4.74 us: 1.03x faster                                                                                                   |
| xml_etree_parse      | 136 ms                                                                                                            | 133 ms: 1.02x faster                                                                                                    |
| unpickle             | 14.1 us                                                                                                           | 14.6 us: 1.04x slower                                                                                                   |
| pickle_dict          | 32.0 us                                                                                                           | 33.4 us: 1.04x slower                                                                                                   |
| unpickle_list        | 4.64 us                                                                                                           | 5.10 us: 1.10x slower                                                                                                   |
| xml_etree_iterparse  | 96.0 ms                                                                                                           | 109 ms: 1.14x slower                                                                                                    |
| json_loads           | 26.3 us                                                                                                           | 30.0 us: 1.14x slower                                                                                                   |
| xml_etree_generate   | 86.2 ms                                                                                                           | 113 ms: 1.31x slower                                                                                                    |
| json_dumps           | 11.6 ms                                                                                                           | 15.3 ms: 1.31x slower                                                                                                   |
| tomli_loads          | 2.10 sec                                                                                                          | 3.26 sec: 1.55x slower                                                                                                  |
| xml_etree_process    | 59.6 ms                                                                                                           | 93.0 ms: 1.56x slower                                                                                                   |
| pickle_pure_python   | 311 us                                                                                                            | 608 us: 1.95x slower                                                                                                    |
| unpickle_pure_python | 214 us                                                                                                            | 419 us: 1.96x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.25x slower                                                                                                            |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241023-3.14.0a1+-d3be6f9/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json | results/bm-20241023-3.14.0a1+-d3be6f9-NOGIL/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                                                           | 10.1 ms: 1.36x slower                                                                                                   |
| python_startup         | 11.0 ms                                                                                                           | 15.4 ms: 1.41x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.38x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241023-3.14.0a1+-d3be6f9/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json | results/bm-20241023-3.14.0a1+-d3be6f9-NOGIL/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 49.8 ms                                                                                                           | 82.5 ms: 1.66x slower                                                                                                   |
| mako            | 11.8 ms                                                                                                           | 20.7 ms: 1.75x slower                                                                                                   |
| genshi_text     | 22.1 ms                                                                                                           | 40.8 ms: 1.85x slower                                                                                                   |
| django_template | 35.2 ms                                                                                                           | 65.6 ms: 1.86x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.78x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20241023-3.14.0a1+-d3be6f9/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json | results/bm-20241023-3.14.0a1+-d3be6f9-NOGIL/bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal             | 3.30 ms                                                                                                           | 2.48 ms: 1.33x faster                                                                                                   |
| create_gc_cycles         | 1.38 ms                                                                                                           | 1.13 ms: 1.22x faster                                                                                                   |
| pickle_list              | 4.88 us                                                                                                           | 4.74 us: 1.03x faster                                                                                                   |
| regex_effbot             | 3.13 ms                                                                                                           | 3.07 ms: 1.02x faster                                                                                                   |
| xml_etree_parse          | 136 ms                                                                                                            | 133 ms: 1.02x faster                                                                                                    |
| pidigits                 | 185 ms                                                                                                            | 186 ms: 1.00x slower                                                                                                    |
| regex_dna                | 181 ms                                                                                                            | 183 ms: 1.01x slower                                                                                                    |
| unpickle                 | 14.1 us                                                                                                           | 14.6 us: 1.04x slower                                                                                                   |
| pickle_dict              | 32.0 us                                                                                                           | 33.4 us: 1.04x slower                                                                                                   |
| regex_v8                 | 24.8 ms                                                                                                           | 26.2 ms: 1.05x slower                                                                                                   |
| unpickle_list            | 4.64 us                                                                                                           | 5.10 us: 1.10x slower                                                                                                   |
| json                     | 4.88 ms                                                                                                           | 5.46 ms: 1.12x slower                                                                                                   |
| bench_mp_pool            | 62.9 ms                                                                                                           | 70.8 ms: 1.13x slower                                                                                                   |
| sqlite_synth             | 2.21 us                                                                                                           | 2.49 us: 1.13x slower                                                                                                   |
| xml_etree_iterparse      | 96.0 ms                                                                                                           | 109 ms: 1.14x slower                                                                                                    |
| json_loads               | 26.3 us                                                                                                           | 30.0 us: 1.14x slower                                                                                                   |
| asyncio_tcp              | 503 ms                                                                                                            | 582 ms: 1.16x slower                                                                                                    |
| asyncio_tcp_ssl          | 1.52 sec                                                                                                          | 1.78 sec: 1.17x slower                                                                                                  |
| pathlib                  | 18.4 ms                                                                                                           | 22.0 ms: 1.19x slower                                                                                                   |
| telco                    | 7.42 ms                                                                                                           | 9.33 ms: 1.26x slower                                                                                                   |
| docutils                 | 2.60 sec                                                                                                          | 3.34 sec: 1.28x slower                                                                                                  |
| coverage                 | 80.4 ms                                                                                                           | 103 ms: 1.29x slower                                                                                                    |
| mdp                      | 2.35 sec                                                                                                          | 3.06 sec: 1.30x slower                                                                                                  |
| xml_etree_generate       | 86.2 ms                                                                                                           | 113 ms: 1.31x slower                                                                                                    |
| pylint                   | 319 ms                                                                                                            | 418 ms: 1.31x slower                                                                                                    |
| json_dumps               | 11.6 ms                                                                                                           | 15.3 ms: 1.31x slower                                                                                                   |
| meteor_contest           | 103 ms                                                                                                            | 136 ms: 1.32x slower                                                                                                    |
| async_generators         | 373 ms                                                                                                            | 495 ms: 1.33x slower                                                                                                    |
| scimark_fft              | 337 ms                                                                                                            | 453 ms: 1.34x slower                                                                                                    |
| python_startup_no_site   | 7.41 ms                                                                                                           | 10.1 ms: 1.36x slower                                                                                                   |
| dulwich_log              | 74.3 ms                                                                                                           | 103 ms: 1.39x slower                                                                                                    |
| scimark_sparse_mat_mult  | 4.44 ms                                                                                                           | 6.23 ms: 1.40x slower                                                                                                   |
| python_startup           | 11.0 ms                                                                                                           | 15.4 ms: 1.41x slower                                                                                                   |
| tornado_http             | 113 ms                                                                                                            | 162 ms: 1.44x slower                                                                                                    |
| coroutines               | 22.3 ms                                                                                                           | 32.0 ms: 1.44x slower                                                                                                   |
| bpe_tokeniser            | 4.34 sec                                                                                                          | 6.24 sec: 1.44x slower                                                                                                  |
| generators               | 29.7 ms                                                                                                           | 43.7 ms: 1.47x slower                                                                                                   |
| pycparser                | 1.14 sec                                                                                                          | 1.70 sec: 1.49x slower                                                                                                  |
| nqueens                  | 79.7 ms                                                                                                           | 119 ms: 1.50x slower                                                                                                    |
| fannkuch                 | 381 ms                                                                                                            | 572 ms: 1.50x slower                                                                                                    |
| tomli_loads              | 2.10 sec                                                                                                          | 3.26 sec: 1.55x slower                                                                                                  |
| xml_etree_process        | 59.6 ms                                                                                                           | 93.0 ms: 1.56x slower                                                                                                   |
| typing_runtime_protocols | 156 us                                                                                                            | 248 us: 1.60x slower                                                                                                    |
| spectral_norm            | 109 ms                                                                                                            | 175 ms: 1.61x slower                                                                                                    |
| html5lib                 | 63.2 ms                                                                                                           | 103 ms: 1.63x slower                                                                                                    |
| sympy_integrate          | 20.1 ms                                                                                                           | 32.8 ms: 1.63x slower                                                                                                   |
| crypto_pyaes             | 66.9 ms                                                                                                           | 110 ms: 1.64x slower                                                                                                    |
| 2to3                     | 252 ms                                                                                                            | 414 ms: 1.64x slower                                                                                                    |
| genshi_xml               | 49.8 ms                                                                                                           | 82.5 ms: 1.66x slower                                                                                                   |
| deepcopy                 | 261 us                                                                                                            | 434 us: 1.66x slower                                                                                                    |
| thrift                   | 755 us                                                                                                            | 1.27 ms: 1.68x slower                                                                                                   |
| sqlglot_optimize         | 53.8 ms                                                                                                           | 91.3 ms: 1.70x slower                                                                                                   |
| sqlglot_normalize        | 106 ms                                                                                                            | 182 ms: 1.72x slower                                                                                                    |
| deepcopy_reduce          | 2.61 us                                                                                                           | 4.54 us: 1.74x slower                                                                                                   |
| pyflate                  | 457 ms                                                                                                            | 794 ms: 1.74x slower                                                                                                    |
| regex_compile            | 131 ms                                                                                                            | 228 ms: 1.74x slower                                                                                                    |
| mako                     | 11.8 ms                                                                                                           | 20.7 ms: 1.75x slower                                                                                                   |
| deepcopy_memo            | 30.2 us                                                                                                           | 53.8 us: 1.78x slower                                                                                                   |
| comprehensions           | 17.1 us                                                                                                           | 30.9 us: 1.80x slower                                                                                                   |
| genshi_text              | 22.1 ms                                                                                                           | 40.8 ms: 1.85x slower                                                                                                   |
| django_template          | 35.2 ms                                                                                                           | 65.6 ms: 1.86x slower                                                                                                   |
| pprint_pformat           | 1.47 sec                                                                                                          | 2.78 sec: 1.89x slower                                                                                                  |
| pprint_safe_repr         | 711 ms                                                                                                            | 1.34 sec: 1.89x slower                                                                                                  |
| float                    | 78.4 ms                                                                                                           | 153 ms: 1.95x slower                                                                                                    |
| pickle_pure_python       | 311 us                                                                                                            | 608 us: 1.95x slower                                                                                                    |
| unpickle_pure_python     | 214 us                                                                                                            | 419 us: 1.96x slower                                                                                                    |
| sympy_str                | 273 ms                                                                                                            | 538 ms: 1.97x slower                                                                                                    |
| logging_format           | 6.86 us                                                                                                           | 13.7 us: 2.00x slower                                                                                                   |
| richards                 | 45.6 ms                                                                                                           | 91.3 ms: 2.00x slower                                                                                                   |
| logging_silent           | 107 ns                                                                                                            | 216 ns: 2.01x slower                                                                                                    |
| scimark_monte_carlo      | 65.1 ms                                                                                                           | 133 ms: 2.04x slower                                                                                                    |
| logging_simple           | 6.08 us                                                                                                           | 12.5 us: 2.05x slower                                                                                                   |
| sqlglot_transpile        | 1.62 ms                                                                                                           | 3.33 ms: 2.06x slower                                                                                                   |
| scimark_sor              | 135 ms                                                                                                            | 281 ms: 2.08x slower                                                                                                    |
| hexiom                   | 6.02 ms                                                                                                           | 12.5 ms: 2.08x slower                                                                                                   |
| richards_super           | 51.8 ms                                                                                                           | 110 ms: 2.12x slower                                                                                                    |
| chaos                    | 59.6 ms                                                                                                           | 130 ms: 2.19x slower                                                                                                    |
| sqlglot_parse            | 1.32 ms                                                                                                           | 2.89 ms: 2.20x slower                                                                                                   |
| nbody                    | 99.4 ms                                                                                                           | 219 ms: 2.21x slower                                                                                                    |
| scimark_lu               | 112 ms                                                                                                            | 248 ms: 2.21x slower                                                                                                    |
| sympy_expand             | 462 ms                                                                                                            | 1.05 sec: 2.27x slower                                                                                                  |
| raytrace                 | 264 ms                                                                                                            | 650 ms: 2.46x slower                                                                                                    |
| sympy_sum                | 154 ms                                                                                                            | 382 ms: 2.48x slower                                                                                                    |
| unpack_sequence          | 54.5 ns                                                                                                           | 136 ns: 2.49x slower                                                                                                    |
| go                       | 121 ms                                                                                                            | 305 ms: 2.52x slower                                                                                                    |
| deltablue                | 3.26 ms                                                                                                           | 9.30 ms: 2.86x slower                                                                                                   |
| bench_thread_pool        | 1.01 ms                                                                                                           | 3.18 ms: 3.15x slower                                                                                                   |
| Geometric mean           | (ref)                                                                                                             | 1.54x slower                                                                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, pickle

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.47x
- 95% likely to have a slowdown of 1.46x
- 99% likely to have a slowdown of 1.43x

# Memory
- memory change: 1.18x