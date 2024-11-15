# Results vs. base

- fork: python
- ref: 3fecbe9255391be1ac3c
- machine: linux-x86_64
- commit hash: 3fecbe9
- commit date: 2024-11-15
- overall geometric mean: 1.54x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.39x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                                                            | 415 ms: 1.63x slower                                                                                                    |
| docutils       | 2.61 sec                                                                                                          | 3.39 sec: 1.30x slower                                                                                                  |
| html5lib       | 66.4 ms                                                                                                           | 107 ms: 1.61x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.50x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_tcp      | 505 ms                                                                                                            | 583 ms: 1.15x slower                                                                                                    |
| asyncio_tcp_ssl  | 1.52 sec                                                                                                          | 1.82 sec: 1.20x slower                                                                                                  |
| async_generators | 368 ms                                                                                                            | 497 ms: 1.35x slower                                                                                                    |
| coroutines       | 22.9 ms                                                                                                           | 31.7 ms: 1.38x slower                                                                                                   |
| Geometric mean   | (ref)                                                                                                             | 1.21x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 224 ms                                                                                                            | 183 ms: 1.22x faster                                                                                                    |
| float          | 78.7 ms                                                                                                           | 152 ms: 1.93x slower                                                                                                    |
| nbody          | 95.4 ms                                                                                                           | 198 ms: 2.07x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.48x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 3.13 ms                                                                                                           | 2.98 ms: 1.05x faster                                                                                                   |
| regex_dna      | 183 ms                                                                                                            | 180 ms: 1.01x faster                                                                                                    |
| regex_v8       | 24.1 ms                                                                                                           | 24.6 ms: 1.02x slower                                                                                                   |
| regex_compile  | 131 ms                                                                                                            | 227 ms: 1.73x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                                                            | 133 ms: 1.03x faster                                                                                                    |
| pickle               | 12.4 us                                                                                                           | 12.7 us: 1.02x slower                                                                                                   |
| pickle_dict          | 31.6 us                                                                                                           | 32.5 us: 1.03x slower                                                                                                   |
| unpickle_list        | 4.71 us                                                                                                           | 4.94 us: 1.05x slower                                                                                                   |
| unpickle             | 13.4 us                                                                                                           | 14.5 us: 1.08x slower                                                                                                   |
| xml_etree_iterparse  | 95.6 ms                                                                                                           | 109 ms: 1.14x slower                                                                                                    |
| json_loads           | 24.8 us                                                                                                           | 28.8 us: 1.16x slower                                                                                                   |
| xml_etree_generate   | 85.6 ms                                                                                                           | 114 ms: 1.34x slower                                                                                                    |
| json_dumps           | 11.5 ms                                                                                                           | 15.3 ms: 1.34x slower                                                                                                   |
| tomli_loads          | 2.11 sec                                                                                                          | 3.25 sec: 1.54x slower                                                                                                  |
| xml_etree_process    | 59.6 ms                                                                                                           | 93.6 ms: 1.57x slower                                                                                                   |
| unpickle_pure_python | 220 us                                                                                                            | 420 us: 1.91x slower                                                                                                    |
| pickle_pure_python   | 321 us                                                                                                            | 618 us: 1.93x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.26x slower                                                                                                            |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 7.43 ms                                                                                                           | 10.3 ms: 1.38x slower                                                                                                   |
| python_startup         | 11.1 ms                                                                                                           | 15.7 ms: 1.42x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.40x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 49.9 ms                                                                                                           | 82.4 ms: 1.65x slower                                                                                                   |
| mako            | 11.7 ms                                                                                                           | 20.8 ms: 1.78x slower                                                                                                   |
| genshi_text     | 22.3 ms                                                                                                           | 40.7 ms: 1.82x slower                                                                                                   |
| django_template | 35.3 ms                                                                                                           | 65.4 ms: 1.85x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.77x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal             | 3.23 ms                                                                                                           | 2.47 ms: 1.31x faster                                                                                                   |
| pidigits                 | 224 ms                                                                                                            | 183 ms: 1.22x faster                                                                                                    |
| create_gc_cycles         | 1.36 ms                                                                                                           | 1.13 ms: 1.20x faster                                                                                                   |
| regex_effbot             | 3.13 ms                                                                                                           | 2.98 ms: 1.05x faster                                                                                                   |
| xml_etree_parse          | 136 ms                                                                                                            | 133 ms: 1.03x faster                                                                                                    |
| regex_dna                | 183 ms                                                                                                            | 180 ms: 1.01x faster                                                                                                    |
| pickle                   | 12.4 us                                                                                                           | 12.7 us: 1.02x slower                                                                                                   |
| regex_v8                 | 24.1 ms                                                                                                           | 24.6 ms: 1.02x slower                                                                                                   |
| pickle_dict              | 31.6 us                                                                                                           | 32.5 us: 1.03x slower                                                                                                   |
| unpickle_list            | 4.71 us                                                                                                           | 4.94 us: 1.05x slower                                                                                                   |
| unpickle                 | 13.4 us                                                                                                           | 14.5 us: 1.08x slower                                                                                                   |
| json                     | 4.74 ms                                                                                                           | 5.30 ms: 1.12x slower                                                                                                   |
| sqlite_synth             | 2.18 us                                                                                                           | 2.47 us: 1.13x slower                                                                                                   |
| bench_mp_pool            | 63.7 ms                                                                                                           | 72.5 ms: 1.14x slower                                                                                                   |
| xml_etree_iterparse      | 95.6 ms                                                                                                           | 109 ms: 1.14x slower                                                                                                    |
| asyncio_tcp              | 505 ms                                                                                                            | 583 ms: 1.15x slower                                                                                                    |
| json_loads               | 24.8 us                                                                                                           | 28.8 us: 1.16x slower                                                                                                   |
| asyncio_tcp_ssl          | 1.52 sec                                                                                                          | 1.82 sec: 1.20x slower                                                                                                  |
| pathlib                  | 18.5 ms                                                                                                           | 22.1 ms: 1.20x slower                                                                                                   |
| scimark_fft              | 342 ms                                                                                                            | 416 ms: 1.22x slower                                                                                                    |
| telco                    | 7.39 ms                                                                                                           | 9.23 ms: 1.25x slower                                                                                                   |
| coverage                 | 81.7 ms                                                                                                           | 104 ms: 1.27x slower                                                                                                    |
| scimark_sparse_mat_mult  | 4.62 ms                                                                                                           | 5.94 ms: 1.29x slower                                                                                                   |
| docutils                 | 2.61 sec                                                                                                          | 3.39 sec: 1.30x slower                                                                                                  |
| pylint                   | 318 ms                                                                                                            | 420 ms: 1.32x slower                                                                                                    |
| xml_etree_generate       | 85.6 ms                                                                                                           | 114 ms: 1.34x slower                                                                                                    |
| json_dumps               | 11.5 ms                                                                                                           | 15.3 ms: 1.34x slower                                                                                                   |
| async_generators         | 368 ms                                                                                                            | 497 ms: 1.35x slower                                                                                                    |
| meteor_contest           | 101 ms                                                                                                            | 138 ms: 1.37x slower                                                                                                    |
| mdp                      | 2.36 sec                                                                                                          | 3.24 sec: 1.37x slower                                                                                                  |
| python_startup_no_site   | 7.43 ms                                                                                                           | 10.3 ms: 1.38x slower                                                                                                   |
| coroutines               | 22.9 ms                                                                                                           | 31.7 ms: 1.38x slower                                                                                                   |
| dulwich_log              | 75.6 ms                                                                                                           | 105 ms: 1.39x slower                                                                                                    |
| spectral_norm            | 116 ms                                                                                                            | 162 ms: 1.40x slower                                                                                                    |
| bpe_tokeniser            | 4.34 sec                                                                                                          | 6.12 sec: 1.41x slower                                                                                                  |
| python_startup           | 11.1 ms                                                                                                           | 15.7 ms: 1.42x slower                                                                                                   |
| generators               | 28.4 ms                                                                                                           | 41.1 ms: 1.45x slower                                                                                                   |
| nqueens                  | 79.9 ms                                                                                                           | 116 ms: 1.45x slower                                                                                                    |
| fannkuch                 | 379 ms                                                                                                            | 564 ms: 1.49x slower                                                                                                    |
| pycparser                | 1.15 sec                                                                                                          | 1.75 sec: 1.53x slower                                                                                                  |
| tomli_loads              | 2.11 sec                                                                                                          | 3.25 sec: 1.54x slower                                                                                                  |
| xml_etree_process        | 59.6 ms                                                                                                           | 93.6 ms: 1.57x slower                                                                                                   |
| crypto_pyaes             | 67.7 ms                                                                                                           | 108 ms: 1.59x slower                                                                                                    |
| html5lib                 | 66.4 ms                                                                                                           | 107 ms: 1.61x slower                                                                                                    |
| typing_runtime_protocols | 156 us                                                                                                            | 253 us: 1.62x slower                                                                                                    |
| 2to3                     | 254 ms                                                                                                            | 415 ms: 1.63x slower                                                                                                    |
| deepcopy                 | 265 us                                                                                                            | 435 us: 1.64x slower                                                                                                    |
| genshi_xml               | 49.9 ms                                                                                                           | 82.4 ms: 1.65x slower                                                                                                   |
| sympy_integrate          | 19.8 ms                                                                                                           | 33.2 ms: 1.68x slower                                                                                                   |
| sqlglot_optimize         | 54.2 ms                                                                                                           | 91.4 ms: 1.69x slower                                                                                                   |
| thrift                   | 749 us                                                                                                            | 1.26 ms: 1.69x slower                                                                                                   |
| sqlglot_normalize        | 108 ms                                                                                                            | 184 ms: 1.70x slower                                                                                                    |
| pyflate                  | 452 ms                                                                                                            | 772 ms: 1.71x slower                                                                                                    |
| deepcopy_reduce          | 2.67 us                                                                                                           | 4.57 us: 1.71x slower                                                                                                   |
| regex_compile            | 131 ms                                                                                                            | 227 ms: 1.73x slower                                                                                                    |
| deepcopy_memo            | 30.5 us                                                                                                           | 53.6 us: 1.76x slower                                                                                                   |
| mako                     | 11.7 ms                                                                                                           | 20.8 ms: 1.78x slower                                                                                                   |
| comprehensions           | 17.3 us                                                                                                           | 30.8 us: 1.78x slower                                                                                                   |
| genshi_text              | 22.3 ms                                                                                                           | 40.7 ms: 1.82x slower                                                                                                   |
| django_template          | 35.3 ms                                                                                                           | 65.4 ms: 1.85x slower                                                                                                   |
| pprint_pformat           | 1.48 sec                                                                                                          | 2.75 sec: 1.85x slower                                                                                                  |
| pprint_safe_repr         | 713 ms                                                                                                            | 1.34 sec: 1.87x slower                                                                                                  |
| unpickle_pure_python     | 220 us                                                                                                            | 420 us: 1.91x slower                                                                                                    |
| scimark_monte_carlo      | 65.9 ms                                                                                                           | 126 ms: 1.91x slower                                                                                                    |
| float                    | 78.7 ms                                                                                                           | 152 ms: 1.93x slower                                                                                                    |
| pickle_pure_python       | 321 us                                                                                                            | 618 us: 1.93x slower                                                                                                    |
| logging_format           | 6.95 us                                                                                                           | 13.7 us: 1.97x slower                                                                                                   |
| logging_simple           | 6.23 us                                                                                                           | 12.3 us: 1.97x slower                                                                                                   |
| sympy_str                | 272 ms                                                                                                            | 541 ms: 1.99x slower                                                                                                    |
| scimark_sor              | 135 ms                                                                                                            | 270 ms: 1.99x slower                                                                                                    |
| logging_silent           | 105 ns                                                                                                            | 213 ns: 2.02x slower                                                                                                    |
| richards                 | 46.1 ms                                                                                                           | 93.2 ms: 2.02x slower                                                                                                   |
| chaos                    | 59.7 ms                                                                                                           | 122 ms: 2.04x slower                                                                                                    |
| nbody                    | 95.4 ms                                                                                                           | 198 ms: 2.07x slower                                                                                                    |
| hexiom                   | 6.03 ms                                                                                                           | 12.5 ms: 2.07x slower                                                                                                   |
| richards_super           | 51.9 ms                                                                                                           | 109 ms: 2.09x slower                                                                                                    |
| sqlglot_transpile        | 1.60 ms                                                                                                           | 3.35 ms: 2.10x slower                                                                                                   |
| scimark_lu               | 115 ms                                                                                                            | 247 ms: 2.16x slower                                                                                                    |
| sqlglot_parse            | 1.29 ms                                                                                                           | 2.90 ms: 2.24x slower                                                                                                   |
| sympy_expand             | 459 ms                                                                                                            | 1.06 sec: 2.31x slower                                                                                                  |
| raytrace                 | 263 ms                                                                                                            | 621 ms: 2.36x slower                                                                                                    |
| go                       | 122 ms                                                                                                            | 295 ms: 2.41x slower                                                                                                    |
| sympy_sum                | 153 ms                                                                                                            | 381 ms: 2.49x slower                                                                                                    |
| deltablue                | 3.27 ms                                                                                                           | 9.08 ms: 2.78x slower                                                                                                   |
| bench_thread_pool        | 1.02 ms                                                                                                           | 3.49 ms: 3.43x slower                                                                                                   |
| unpack_sequence          | 40.8 ns                                                                                                           | 144 ns: 3.54x slower                                                                                                    |
| Geometric mean           | (ref)                                                                                                             | 1.54x slower                                                                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, pickle_list

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.45x
- 95% likely to have a slowdown of 1.43x
- 99% likely to have a slowdown of 1.39x

# Memory
- memory change: 1.20x