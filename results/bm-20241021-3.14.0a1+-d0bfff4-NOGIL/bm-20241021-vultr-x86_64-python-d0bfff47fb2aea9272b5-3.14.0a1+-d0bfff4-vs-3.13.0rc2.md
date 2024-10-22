# Results vs. 3.13.0rc2

- fork: python
- ref: d0bfff47fb2aea9272b5
- machine: linux-x86_64
- commit hash: d0bfff4
- commit date: 2024-10-21
- overall geometric mean: 1.57x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.41x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 414 ms: 1.59x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.33 sec: 1.27x slower                                                 |
| html5lib       | 67.0 ms                                                      | 103 ms: 1.54x slower                                                   |
| tornado_http   | 114 ms                                                       | 163 ms: 1.43x slower                                                   |
| Geometric mean | (ref)                                                        | 1.45x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.72 sec: 1.14x slower                                                 |
| asyncio_tcp      | 505 ms                                                       | 580 ms: 1.15x slower                                                   |
| async_generators | 377 ms                                                       | 496 ms: 1.31x slower                                                   |
| coroutines       | 23.6 ms                                                      | 31.9 ms: 1.35x slower                                                  |
| Geometric mean   | (ref)                                                        | 1.18x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                   |
| float          | 77.5 ms                                                      | 155 ms: 2.00x slower                                                   |
| nbody          | 85.1 ms                                                      | 226 ms: 2.65x slower                                                   |
| Geometric mean | (ref)                                                        | 1.66x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| regex_effbot   | 3.08 ms                                                      | 3.13 ms: 1.01x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 25.9 ms: 1.14x slower                                                  |
| regex_compile  | 132 ms                                                       | 228 ms: 1.73x slower                                                   |
| Geometric mean | (ref)                                                        | 1.19x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle               | 11.3 us                                                      | 10.9 us: 1.04x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 31.2 us: 1.04x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| pickle_list          | 4.93 us                                                      | 4.83 us: 1.02x faster                                                  |
| unpickle_list        | 4.71 us                                                      | 5.12 us: 1.09x slower                                                  |
| json_loads           | 27.0 us                                                      | 29.4 us: 1.09x slower                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 109 ms: 1.15x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 113 ms: 1.32x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 15.5 ms: 1.47x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 92.6 ms: 1.56x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 3.30 sec: 1.64x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 425 us: 2.02x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 618 us: 2.10x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.26x slower                                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.0 ms: 1.36x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 81.3 ms: 1.67x slower                                                  |
| mako            | 11.3 ms                                                      | 20.9 ms: 1.84x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 40.5 ms: 1.88x slower                                                  |
| django_template | 34.1 ms                                                      | 64.8 ms: 1.90x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.82x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.56 ms: 1.23x faster                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.10 ms: 1.22x faster                                                  |
| pidigits                 | 217 ms                                                       | 187 ms: 1.16x faster                                                   |
| pickle                   | 11.3 us                                                      | 10.9 us: 1.04x faster                                                  |
| pickle_dict              | 32.5 us                                                      | 31.2 us: 1.04x faster                                                  |
| xml_etree_parse          | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| pickle_list              | 4.93 us                                                      | 4.83 us: 1.02x faster                                                  |
| regex_dna                | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| regex_effbot             | 3.08 ms                                                      | 3.13 ms: 1.01x slower                                                  |
| unpickle_list            | 4.71 us                                                      | 5.12 us: 1.09x slower                                                  |
| json_loads               | 27.0 us                                                      | 29.4 us: 1.09x slower                                                  |
| json                     | 4.93 ms                                                      | 5.42 ms: 1.10x slower                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.46 us: 1.12x slower                                                  |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.72 sec: 1.14x slower                                                 |
| regex_v8                 | 22.7 ms                                                      | 25.9 ms: 1.14x slower                                                  |
| pathlib                  | 19.2 ms                                                      | 21.9 ms: 1.14x slower                                                  |
| xml_etree_iterparse      | 94.9 ms                                                      | 109 ms: 1.15x slower                                                   |
| asyncio_tcp              | 505 ms                                                       | 580 ms: 1.15x slower                                                   |
| telco                    | 7.82 ms                                                      | 9.41 ms: 1.20x slower                                                  |
| deepcopy                 | 355 us                                                       | 436 us: 1.23x slower                                                   |
| coverage                 | 83.0 ms                                                      | 103 ms: 1.24x slower                                                   |
| docutils                 | 2.62 sec                                                     | 3.33 sec: 1.27x slower                                                 |
| scimark_fft              | 349 ms                                                       | 459 ms: 1.31x slower                                                   |
| pylint                   | 317 ms                                                       | 417 ms: 1.31x slower                                                   |
| async_generators         | 377 ms                                                       | 496 ms: 1.31x slower                                                   |
| xml_etree_generate       | 85.4 ms                                                      | 113 ms: 1.32x slower                                                   |
| mdp                      | 2.36 sec                                                     | 3.16 sec: 1.34x slower                                                 |
| coroutines               | 23.6 ms                                                      | 31.9 ms: 1.35x slower                                                  |
| python_startup_no_site   | 7.39 ms                                                      | 10.0 ms: 1.36x slower                                                  |
| dulwich_log              | 74.8 ms                                                      | 102 ms: 1.37x slower                                                   |
| meteor_contest           | 102 ms                                                       | 140 ms: 1.38x slower                                                   |
| deepcopy_memo            | 39.1 us                                                      | 54.3 us: 1.39x slower                                                  |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 6.54 ms: 1.39x slower                                                  |
| python_startup           | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                                  |
| bpe_tokeniser            | 4.45 sec                                                     | 6.32 sec: 1.42x slower                                                 |
| tornado_http             | 114 ms                                                       | 163 ms: 1.43x slower                                                   |
| deepcopy_reduce          | 3.11 us                                                      | 4.55 us: 1.46x slower                                                  |
| json_dumps               | 10.5 ms                                                      | 15.5 ms: 1.47x slower                                                  |
| generators               | 28.8 ms                                                      | 42.7 ms: 1.48x slower                                                  |
| nqueens                  | 78.6 ms                                                      | 119 ms: 1.51x slower                                                   |
| pycparser                | 1.12 sec                                                     | 1.70 sec: 1.52x slower                                                 |
| html5lib                 | 67.0 ms                                                      | 103 ms: 1.54x slower                                                   |
| xml_etree_process        | 59.3 ms                                                      | 92.6 ms: 1.56x slower                                                  |
| fannkuch                 | 370 ms                                                       | 582 ms: 1.57x slower                                                   |
| 2to3                     | 260 ms                                                       | 414 ms: 1.59x slower                                                   |
| typing_runtime_protocols | 155 us                                                       | 247 us: 1.59x slower                                                   |
| crypto_pyaes             | 67.9 ms                                                      | 111 ms: 1.63x slower                                                   |
| spectral_norm            | 111 ms                                                       | 181 ms: 1.63x slower                                                   |
| thrift                   | 778 us                                                       | 1.27 ms: 1.63x slower                                                  |
| tomli_loads              | 2.01 sec                                                     | 3.30 sec: 1.64x slower                                                 |
| sympy_integrate          | 19.8 ms                                                      | 33.0 ms: 1.66x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 81.3 ms: 1.67x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 180 ms: 1.71x slower                                                   |
| sqlglot_optimize         | 52.7 ms                                                      | 90.4 ms: 1.71x slower                                                  |
| regex_compile            | 132 ms                                                       | 228 ms: 1.73x slower                                                   |
| pyflate                  | 449 ms                                                       | 798 ms: 1.78x slower                                                   |
| pprint_safe_repr         | 738 ms                                                       | 1.34 sec: 1.82x slower                                                 |
| mako                     | 11.3 ms                                                      | 20.9 ms: 1.84x slower                                                  |
| comprehensions           | 16.5 us                                                      | 30.4 us: 1.85x slower                                                  |
| pprint_pformat           | 1.50 sec                                                     | 2.77 sec: 1.85x slower                                                 |
| genshi_text              | 21.5 ms                                                      | 40.5 ms: 1.88x slower                                                  |
| django_template          | 34.1 ms                                                      | 64.8 ms: 1.90x slower                                                  |
| sympy_str                | 275 ms                                                       | 540 ms: 1.97x slower                                                   |
| logging_format           | 6.84 us                                                      | 13.6 us: 1.99x slower                                                  |
| float                    | 77.5 ms                                                      | 155 ms: 2.00x slower                                                   |
| logging_simple           | 6.16 us                                                      | 12.4 us: 2.01x slower                                                  |
| richards                 | 45.2 ms                                                      | 90.7 ms: 2.01x slower                                                  |
| unpickle_pure_python     | 210 us                                                       | 425 us: 2.02x slower                                                   |
| scimark_monte_carlo      | 65.4 ms                                                      | 135 ms: 2.06x slower                                                   |
| richards_super           | 51.6 ms                                                      | 108 ms: 2.10x slower                                                   |
| hexiom                   | 5.99 ms                                                      | 12.6 ms: 2.10x slower                                                  |
| pickle_pure_python       | 294 us                                                       | 618 us: 2.10x slower                                                   |
| scimark_sor              | 134 ms                                                       | 283 ms: 2.10x slower                                                   |
| logging_silent           | 103 ns                                                       | 217 ns: 2.12x slower                                                   |
| sqlglot_transpile        | 1.56 ms                                                      | 3.33 ms: 2.13x slower                                                  |
| go                       | 141 ms                                                       | 305 ms: 2.16x slower                                                   |
| scimark_lu               | 113 ms                                                       | 248 ms: 2.20x slower                                                   |
| chaos                    | 57.3 ms                                                      | 130 ms: 2.26x slower                                                   |
| sympy_expand             | 457 ms                                                       | 1.05 sec: 2.31x slower                                                 |
| sqlglot_parse            | 1.25 ms                                                      | 2.89 ms: 2.31x slower                                                  |
| sympy_sum                | 156 ms                                                       | 381 ms: 2.45x slower                                                   |
| raytrace                 | 253 ms                                                       | 650 ms: 2.57x slower                                                   |
| nbody                    | 85.1 ms                                                      | 226 ms: 2.65x slower                                                   |
| deltablue                | 3.12 ms                                                      | 9.23 ms: 2.95x slower                                                  |
| unpack_sequence          | 44.8 ns                                                      | 145 ns: 3.23x slower                                                   |
| bench_thread_pool        | 919 us                                                       | 3.18 ms: 3.47x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 70.6 ms: 6.42x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.57x slower                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, unpickle
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.49x
- 95% likely to have a slowdown of 1.47x
- 99% likely to have a slowdown of 1.41x

# Memory
- memory change: 1.19x