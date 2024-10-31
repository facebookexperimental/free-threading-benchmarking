# Results vs. 3.13.0rc2

- fork: python
- ref: ac3a2c8abceeec448486
- machine: linux-x86_64
- commit hash: ac3a2c8
- commit date: 2024-10-31
- overall geometric mean: 1.57x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.42x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 413 ms: 1.59x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.37 sec: 1.29x slower                                                 |
| html5lib       | 67.0 ms                                                      | 106 ms: 1.58x slower                                                   |
| tornado_http   | 114 ms                                                       | 162 ms: 1.42x slower                                                   |
| Geometric mean | (ref)                                                        | 1.46x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|--------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 520 ms                                                       | 518 ms: 1.01x faster                                                   |
| asyncio_tcp        | 505 ms                                                       | 580 ms: 1.15x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                                     | 1.80 sec: 1.19x slower                                                 |
| async_generators   | 377 ms                                                       | 500 ms: 1.33x slower                                                   |
| coroutines         | 23.6 ms                                                      | 32.3 ms: 1.37x slower                                                  |
| Geometric mean     | (ref)                                                        | 1.20x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.17x faster                                                   |
| float          | 77.5 ms                                                      | 154 ms: 1.98x slower                                                   |
| nbody          | 85.1 ms                                                      | 219 ms: 2.58x slower                                                   |
| Geometric mean | (ref)                                                        | 1.64x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.17 ms: 1.03x slower                                                  |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 25.3 ms: 1.12x slower                                                  |
| regex_compile  | 132 ms                                                       | 228 ms: 1.72x slower                                                   |
| Geometric mean | (ref)                                                        | 1.19x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle               | 11.3 us                                                      | 10.8 us: 1.05x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 31.2 us: 1.04x faster                                                  |
| pickle_list          | 4.93 us                                                      | 4.76 us: 1.04x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.03x faster                                                   |
| unpickle             | 14.3 us                                                      | 14.8 us: 1.03x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 5.04 us: 1.07x slower                                                  |
| json_loads           | 27.0 us                                                      | 29.8 us: 1.10x slower                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 111 ms: 1.17x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 113 ms: 1.32x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 15.1 ms: 1.43x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 93.5 ms: 1.58x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 3.30 sec: 1.64x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 427 us: 2.03x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 620 us: 2.10x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.26x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.1 ms: 1.36x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 82.4 ms: 1.69x slower                                                  |
| mako            | 11.3 ms                                                      | 21.1 ms: 1.86x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 40.4 ms: 1.87x slower                                                  |
| django_template | 34.1 ms                                                      | 64.9 ms: 1.90x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.83x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.44 ms: 1.29x faster                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.11 ms: 1.21x faster                                                  |
| pidigits                 | 217 ms                                                       | 186 ms: 1.17x faster                                                   |
| pickle                   | 11.3 us                                                      | 10.8 us: 1.05x faster                                                  |
| pickle_dict              | 32.5 us                                                      | 31.2 us: 1.04x faster                                                  |
| pickle_list              | 4.93 us                                                      | 4.76 us: 1.04x faster                                                  |
| xml_etree_parse          | 136 ms                                                       | 133 ms: 1.03x faster                                                   |
| asyncio_websockets       | 520 ms                                                       | 518 ms: 1.01x faster                                                   |
| regex_effbot             | 3.08 ms                                                      | 3.17 ms: 1.03x slower                                                  |
| regex_dna                | 180 ms                                                       | 186 ms: 1.03x slower                                                   |
| unpickle                 | 14.3 us                                                      | 14.8 us: 1.03x slower                                                  |
| unpickle_list            | 4.71 us                                                      | 5.04 us: 1.07x slower                                                  |
| json_loads               | 27.0 us                                                      | 29.8 us: 1.10x slower                                                  |
| regex_v8                 | 22.7 ms                                                      | 25.3 ms: 1.12x slower                                                  |
| json                     | 4.93 ms                                                      | 5.51 ms: 1.12x slower                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.47 us: 1.12x slower                                                  |
| pathlib                  | 19.2 ms                                                      | 22.0 ms: 1.14x slower                                                  |
| asyncio_tcp              | 505 ms                                                       | 580 ms: 1.15x slower                                                   |
| xml_etree_iterparse      | 94.9 ms                                                      | 111 ms: 1.17x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.80 sec: 1.19x slower                                                 |
| telco                    | 7.82 ms                                                      | 9.50 ms: 1.21x slower                                                  |
| deepcopy                 | 355 us                                                       | 438 us: 1.23x slower                                                   |
| coverage                 | 83.0 ms                                                      | 102 ms: 1.23x slower                                                   |
| docutils                 | 2.62 sec                                                     | 3.37 sec: 1.29x slower                                                 |
| scimark_fft              | 349 ms                                                       | 452 ms: 1.29x slower                                                   |
| mdp                      | 2.36 sec                                                     | 3.08 sec: 1.31x slower                                                 |
| pylint                   | 317 ms                                                       | 419 ms: 1.32x slower                                                   |
| xml_etree_generate       | 85.4 ms                                                      | 113 ms: 1.32x slower                                                   |
| async_generators         | 377 ms                                                       | 500 ms: 1.33x slower                                                   |
| meteor_contest           | 102 ms                                                       | 138 ms: 1.36x slower                                                   |
| python_startup_no_site   | 7.39 ms                                                      | 10.1 ms: 1.36x slower                                                  |
| coroutines               | 23.6 ms                                                      | 32.3 ms: 1.37x slower                                                  |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 6.45 ms: 1.37x slower                                                  |
| dulwich_log              | 74.8 ms                                                      | 104 ms: 1.39x slower                                                   |
| deepcopy_memo            | 39.1 us                                                      | 54.3 us: 1.39x slower                                                  |
| python_startup           | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                                  |
| bpe_tokeniser            | 4.45 sec                                                     | 6.32 sec: 1.42x slower                                                 |
| tornado_http             | 114 ms                                                       | 162 ms: 1.42x slower                                                   |
| json_dumps               | 10.5 ms                                                      | 15.1 ms: 1.43x slower                                                  |
| deepcopy_reduce          | 3.11 us                                                      | 4.59 us: 1.47x slower                                                  |
| generators               | 28.8 ms                                                      | 42.8 ms: 1.48x slower                                                  |
| nqueens                  | 78.6 ms                                                      | 120 ms: 1.52x slower                                                   |
| pycparser                | 1.12 sec                                                     | 1.70 sec: 1.52x slower                                                 |
| fannkuch                 | 370 ms                                                       | 576 ms: 1.56x slower                                                   |
| xml_etree_process        | 59.3 ms                                                      | 93.5 ms: 1.58x slower                                                  |
| html5lib                 | 67.0 ms                                                      | 106 ms: 1.58x slower                                                   |
| spectral_norm            | 111 ms                                                       | 176 ms: 1.58x slower                                                   |
| 2to3                     | 260 ms                                                       | 413 ms: 1.59x slower                                                   |
| crypto_pyaes             | 67.9 ms                                                      | 109 ms: 1.61x slower                                                   |
| thrift                   | 778 us                                                       | 1.26 ms: 1.62x slower                                                  |
| tomli_loads              | 2.01 sec                                                     | 3.30 sec: 1.64x slower                                                 |
| typing_runtime_protocols | 155 us                                                       | 254 us: 1.64x slower                                                   |
| sympy_integrate          | 19.8 ms                                                      | 33.0 ms: 1.66x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 82.4 ms: 1.69x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 181 ms: 1.71x slower                                                   |
| regex_compile            | 132 ms                                                       | 228 ms: 1.72x slower                                                   |
| sqlglot_optimize         | 52.7 ms                                                      | 91.6 ms: 1.74x slower                                                  |
| pyflate                  | 449 ms                                                       | 790 ms: 1.76x slower                                                   |
| pprint_safe_repr         | 738 ms                                                       | 1.35 sec: 1.83x slower                                                 |
| mako                     | 11.3 ms                                                      | 21.1 ms: 1.86x slower                                                  |
| genshi_text              | 21.5 ms                                                      | 40.4 ms: 1.87x slower                                                  |
| pprint_pformat           | 1.50 sec                                                     | 2.81 sec: 1.87x slower                                                 |
| comprehensions           | 16.5 us                                                      | 31.0 us: 1.88x slower                                                  |
| django_template          | 34.1 ms                                                      | 64.9 ms: 1.90x slower                                                  |
| sympy_str                | 275 ms                                                       | 540 ms: 1.97x slower                                                   |
| richards                 | 45.2 ms                                                      | 89.7 ms: 1.98x slower                                                  |
| float                    | 77.5 ms                                                      | 154 ms: 1.98x slower                                                   |
| logging_format           | 6.84 us                                                      | 13.7 us: 2.00x slower                                                  |
| scimark_monte_carlo      | 65.4 ms                                                      | 131 ms: 2.01x slower                                                   |
| logging_simple           | 6.16 us                                                      | 12.4 us: 2.01x slower                                                  |
| unpickle_pure_python     | 210 us                                                       | 427 us: 2.03x slower                                                   |
| hexiom                   | 5.99 ms                                                      | 12.6 ms: 2.10x slower                                                  |
| scimark_sor              | 134 ms                                                       | 283 ms: 2.10x slower                                                   |
| pickle_pure_python       | 294 us                                                       | 620 us: 2.10x slower                                                   |
| logging_silent           | 103 ns                                                       | 217 ns: 2.11x slower                                                   |
| go                       | 141 ms                                                       | 299 ms: 2.12x slower                                                   |
| sqlglot_transpile        | 1.56 ms                                                      | 3.31 ms: 2.12x slower                                                  |
| richards_super           | 51.6 ms                                                      | 110 ms: 2.13x slower                                                   |
| scimark_lu               | 113 ms                                                       | 252 ms: 2.24x slower                                                   |
| chaos                    | 57.3 ms                                                      | 129 ms: 2.24x slower                                                   |
| sympy_expand             | 457 ms                                                       | 1.06 sec: 2.31x slower                                                 |
| sqlglot_parse            | 1.25 ms                                                      | 2.90 ms: 2.32x slower                                                  |
| sympy_sum                | 156 ms                                                       | 382 ms: 2.46x slower                                                   |
| raytrace                 | 253 ms                                                       | 650 ms: 2.57x slower                                                   |
| nbody                    | 85.1 ms                                                      | 219 ms: 2.58x slower                                                   |
| deltablue                | 3.12 ms                                                      | 9.25 ms: 2.96x slower                                                  |
| unpack_sequence          | 44.8 ns                                                      | 144 ns: 3.22x slower                                                   |
| bench_thread_pool        | 919 us                                                       | 3.19 ms: 3.47x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 70.8 ms: 6.44x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.57x slower                                                           |
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.49x
- 95% likely to have a slowdown of 1.47x
- 99% likely to have a slowdown of 1.42x

# Memory
- memory change: 1.20x