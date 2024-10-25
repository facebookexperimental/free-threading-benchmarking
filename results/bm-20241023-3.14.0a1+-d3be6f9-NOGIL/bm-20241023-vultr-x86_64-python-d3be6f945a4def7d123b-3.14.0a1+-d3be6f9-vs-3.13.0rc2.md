# Results vs. 3.13.0rc2

- fork: python
- ref: d3be6f945a4def7d123b
- machine: linux-x86_64
- commit hash: d3be6f9
- commit date: 2024-10-23
- overall geometric mean: 1.57x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.41x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 414 ms: 1.60x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.34 sec: 1.28x slower                                                 |
| html5lib       | 67.0 ms                                                      | 103 ms: 1.54x slower                                                   |
| tornado_http   | 114 ms                                                       | 162 ms: 1.42x slower                                                   |
| Geometric mean | (ref)                                                        | 1.45x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp      | 505 ms                                                       | 582 ms: 1.15x slower                                                   |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.78 sec: 1.18x slower                                                 |
| async_generators | 377 ms                                                       | 495 ms: 1.31x slower                                                   |
| coroutines       | 23.6 ms                                                      | 32.0 ms: 1.36x slower                                                  |
| Geometric mean   | (ref)                                                        | 1.19x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.16x faster                                                   |
| float          | 77.5 ms                                                      | 153 ms: 1.97x slower                                                   |
| nbody          | 85.1 ms                                                      | 219 ms: 2.58x slower                                                   |
| Geometric mean | (ref)                                                        | 1.63x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.07 ms: 1.01x faster                                                  |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 26.2 ms: 1.15x slower                                                  |
| regex_compile  | 132 ms                                                       | 228 ms: 1.72x slower                                                   |
| Geometric mean | (ref)                                                        | 1.19x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_list          | 4.93 us                                                      | 4.74 us: 1.04x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.02x faster                                                   |
| pickle_dict          | 32.5 us                                                      | 33.4 us: 1.03x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 5.10 us: 1.08x slower                                                  |
| json_loads           | 27.0 us                                                      | 30.0 us: 1.11x slower                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 109 ms: 1.15x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 113 ms: 1.32x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 15.3 ms: 1.45x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 93.0 ms: 1.57x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 3.26 sec: 1.63x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 419 us: 2.00x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 608 us: 2.07x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.27x slower                                                           |

Benchmark hidden because not significant (2): pickle, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.1 ms: 1.36x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.4 ms: 1.41x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 82.5 ms: 1.69x slower                                                  |
| mako            | 11.3 ms                                                      | 20.7 ms: 1.82x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 40.8 ms: 1.89x slower                                                  |
| django_template | 34.1 ms                                                      | 65.6 ms: 1.92x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.83x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1+-d3be6f9 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.48 ms: 1.27x faster                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.13 ms: 1.18x faster                                                  |
| pidigits                 | 217 ms                                                       | 186 ms: 1.16x faster                                                   |
| pickle_list              | 4.93 us                                                      | 4.74 us: 1.04x faster                                                  |
| xml_etree_parse          | 136 ms                                                       | 133 ms: 1.02x faster                                                   |
| regex_effbot             | 3.08 ms                                                      | 3.07 ms: 1.01x faster                                                  |
| regex_dna                | 180 ms                                                       | 183 ms: 1.02x slower                                                   |
| pickle_dict              | 32.5 us                                                      | 33.4 us: 1.03x slower                                                  |
| unpickle_list            | 4.71 us                                                      | 5.10 us: 1.08x slower                                                  |
| json                     | 4.93 ms                                                      | 5.46 ms: 1.11x slower                                                  |
| json_loads               | 27.0 us                                                      | 30.0 us: 1.11x slower                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.49 us: 1.13x slower                                                  |
| pathlib                  | 19.2 ms                                                      | 22.0 ms: 1.14x slower                                                  |
| asyncio_tcp              | 505 ms                                                       | 582 ms: 1.15x slower                                                   |
| regex_v8                 | 22.7 ms                                                      | 26.2 ms: 1.15x slower                                                  |
| xml_etree_iterparse      | 94.9 ms                                                      | 109 ms: 1.15x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.78 sec: 1.18x slower                                                 |
| telco                    | 7.82 ms                                                      | 9.33 ms: 1.19x slower                                                  |
| deepcopy                 | 355 us                                                       | 434 us: 1.22x slower                                                   |
| coverage                 | 83.0 ms                                                      | 103 ms: 1.25x slower                                                   |
| docutils                 | 2.62 sec                                                     | 3.34 sec: 1.28x slower                                                 |
| scimark_fft              | 349 ms                                                       | 453 ms: 1.30x slower                                                   |
| mdp                      | 2.36 sec                                                     | 3.06 sec: 1.30x slower                                                 |
| async_generators         | 377 ms                                                       | 495 ms: 1.31x slower                                                   |
| pylint                   | 317 ms                                                       | 418 ms: 1.32x slower                                                   |
| xml_etree_generate       | 85.4 ms                                                      | 113 ms: 1.32x slower                                                   |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 6.23 ms: 1.32x slower                                                  |
| meteor_contest           | 102 ms                                                       | 136 ms: 1.34x slower                                                   |
| coroutines               | 23.6 ms                                                      | 32.0 ms: 1.36x slower                                                  |
| python_startup_no_site   | 7.39 ms                                                      | 10.1 ms: 1.36x slower                                                  |
| deepcopy_memo            | 39.1 us                                                      | 53.8 us: 1.38x slower                                                  |
| dulwich_log              | 74.8 ms                                                      | 103 ms: 1.38x slower                                                   |
| bpe_tokeniser            | 4.45 sec                                                     | 6.24 sec: 1.40x slower                                                 |
| python_startup           | 11.0 ms                                                      | 15.4 ms: 1.41x slower                                                  |
| tornado_http             | 114 ms                                                       | 162 ms: 1.42x slower                                                   |
| json_dumps               | 10.5 ms                                                      | 15.3 ms: 1.45x slower                                                  |
| deepcopy_reduce          | 3.11 us                                                      | 4.54 us: 1.46x slower                                                  |
| generators               | 28.8 ms                                                      | 43.7 ms: 1.52x slower                                                  |
| nqueens                  | 78.6 ms                                                      | 119 ms: 1.52x slower                                                   |
| pycparser                | 1.12 sec                                                     | 1.70 sec: 1.52x slower                                                 |
| html5lib                 | 67.0 ms                                                      | 103 ms: 1.54x slower                                                   |
| fannkuch                 | 370 ms                                                       | 572 ms: 1.55x slower                                                   |
| xml_etree_process        | 59.3 ms                                                      | 93.0 ms: 1.57x slower                                                  |
| spectral_norm            | 111 ms                                                       | 175 ms: 1.57x slower                                                   |
| 2to3                     | 260 ms                                                       | 414 ms: 1.60x slower                                                   |
| typing_runtime_protocols | 155 us                                                       | 248 us: 1.60x slower                                                   |
| crypto_pyaes             | 67.9 ms                                                      | 110 ms: 1.62x slower                                                   |
| tomli_loads              | 2.01 sec                                                     | 3.26 sec: 1.63x slower                                                 |
| thrift                   | 778 us                                                       | 1.27 ms: 1.63x slower                                                  |
| sympy_integrate          | 19.8 ms                                                      | 32.8 ms: 1.66x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 82.5 ms: 1.69x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 182 ms: 1.72x slower                                                   |
| regex_compile            | 132 ms                                                       | 228 ms: 1.72x slower                                                   |
| sqlglot_optimize         | 52.7 ms                                                      | 91.3 ms: 1.73x slower                                                  |
| pyflate                  | 449 ms                                                       | 794 ms: 1.77x slower                                                   |
| pprint_safe_repr         | 738 ms                                                       | 1.34 sec: 1.82x slower                                                 |
| mako                     | 11.3 ms                                                      | 20.7 ms: 1.82x slower                                                  |
| pprint_pformat           | 1.50 sec                                                     | 2.78 sec: 1.85x slower                                                 |
| comprehensions           | 16.5 us                                                      | 30.9 us: 1.88x slower                                                  |
| genshi_text              | 21.5 ms                                                      | 40.8 ms: 1.89x slower                                                  |
| django_template          | 34.1 ms                                                      | 65.6 ms: 1.92x slower                                                  |
| sympy_str                | 275 ms                                                       | 538 ms: 1.96x slower                                                   |
| float                    | 77.5 ms                                                      | 153 ms: 1.97x slower                                                   |
| unpickle_pure_python     | 210 us                                                       | 419 us: 2.00x slower                                                   |
| logging_format           | 6.84 us                                                      | 13.7 us: 2.01x slower                                                  |
| richards                 | 45.2 ms                                                      | 91.3 ms: 2.02x slower                                                  |
| logging_simple           | 6.16 us                                                      | 12.5 us: 2.03x slower                                                  |
| scimark_monte_carlo      | 65.4 ms                                                      | 133 ms: 2.03x slower                                                   |
| pickle_pure_python       | 294 us                                                       | 608 us: 2.07x slower                                                   |
| scimark_sor              | 134 ms                                                       | 281 ms: 2.09x slower                                                   |
| hexiom                   | 5.99 ms                                                      | 12.5 ms: 2.09x slower                                                  |
| logging_silent           | 103 ns                                                       | 216 ns: 2.10x slower                                                   |
| richards_super           | 51.6 ms                                                      | 110 ms: 2.13x slower                                                   |
| sqlglot_transpile        | 1.56 ms                                                      | 3.33 ms: 2.14x slower                                                  |
| go                       | 141 ms                                                       | 305 ms: 2.17x slower                                                   |
| scimark_lu               | 113 ms                                                       | 248 ms: 2.20x slower                                                   |
| chaos                    | 57.3 ms                                                      | 130 ms: 2.28x slower                                                   |
| sympy_expand             | 457 ms                                                       | 1.05 sec: 2.30x slower                                                 |
| sqlglot_parse            | 1.25 ms                                                      | 2.89 ms: 2.31x slower                                                  |
| sympy_sum                | 156 ms                                                       | 382 ms: 2.46x slower                                                   |
| raytrace                 | 253 ms                                                       | 650 ms: 2.57x slower                                                   |
| nbody                    | 85.1 ms                                                      | 219 ms: 2.58x slower                                                   |
| deltablue                | 3.12 ms                                                      | 9.30 ms: 2.98x slower                                                  |
| unpack_sequence          | 44.8 ns                                                      | 136 ns: 3.03x slower                                                   |
| bench_thread_pool        | 919 us                                                       | 3.18 ms: 3.46x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 70.8 ms: 6.44x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.57x slower                                                           |

Benchmark hidden because not significant (3): asyncio_websockets, pickle, unpickle
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.50x
- 95% likely to have a slowdown of 1.46x
- 99% likely to have a slowdown of 1.41x

# Memory
- memory change: 1.19x