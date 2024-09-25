# Results vs. 3.13.0rc1+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e001027
- commit date: 2024-08-15
- overall geometric mean: 1.45x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.33x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 442 ms                                                  | 698 ms: 1.58x slower                                  |
| docutils       | 4.01 sec                                                | 5.02 sec: 1.25x slower                                |
| html5lib       | 98.1 ms                                                 | 149 ms: 1.52x slower                                  |
| tornado_http   | 248 ms                                                  | 429 ms: 1.73x slower                                  |
| Geometric mean | (ref)                                                   | 1.51x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|-------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.46 sec                                                | 1.19 sec: 1.22x faster                                |
| async_tree_none         | 576 ms                                                  | 614 ms: 1.07x slower                                  |
| async_tree_cpu_io_mixed | 899 ms                                                  | 974 ms: 1.08x slower                                  |
| asyncio_tcp             | 985 ms                                                  | 1.12 sec: 1.14x slower                                |
| asyncio_tcp_ssl         | 2.79 sec                                                | 3.41 sec: 1.22x slower                                |
| async_generators        | 592 ms                                                  | 763 ms: 1.29x slower                                  |
| coroutines              | 29.2 ms                                                 | 43.6 ms: 1.49x slower                                 |
| Geometric mean          | (ref)                                                   | 1.07x slower                                          |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 248 ms                                                  | 275 ms: 1.11x slower                                  |
| float          | 115 ms                                                  | 191 ms: 1.66x slower                                  |
| nbody          | 124 ms                                                  | 317 ms: 2.56x slower                                  |
| Geometric mean | (ref)                                                   | 1.68x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 288 ms                                                  | 297 ms: 1.03x slower                                  |
| regex_v8       | 32.4 ms                                                 | 36.7 ms: 1.13x slower                                 |
| regex_compile  | 177 ms                                                  | 303 ms: 1.71x slower                                  |
| Geometric mean | (ref)                                                   | 1.18x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle             | 21.4 us                                                 | 23.1 us: 1.08x slower                                 |
| unpickle_list        | 6.67 us                                                 | 7.97 us: 1.20x slower                                 |
| json_dumps           | 14.9 ms                                                 | 17.9 ms: 1.20x slower                                 |
| json_loads           | 36.1 us                                                 | 48.4 us: 1.34x slower                                 |
| xml_etree_generate   | 129 ms                                                  | 180 ms: 1.39x slower                                  |
| xml_etree_process    | 86.5 ms                                                 | 133 ms: 1.54x slower                                  |
| tomli_loads          | 2.80 sec                                                | 4.36 sec: 1.56x slower                                |
| unpickle_pure_python | 296 us                                                  | 574 us: 1.94x slower                                  |
| pickle_pure_python   | 417 us                                                  | 910 us: 2.18x slower                                  |
| Geometric mean       | (ref)                                                   | 1.27x slower                                          |

Benchmark hidden because not significant (5): pickle_list, pickle_dict, xml_etree_parse, xml_etree_iterparse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 31.2 ms: 1.41x slower                                 |
| python_startup_no_site | 14.6 ms                                                 | 22.7 ms: 1.55x slower                                 |
| Geometric mean         | (ref)                                                   | 1.48x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|-----------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 46.9 ms                                                 | 80.8 ms: 1.72x slower                                 |
| genshi_xml      | 68.3 ms                                                 | 118 ms: 1.73x slower                                  |
| genshi_text     | 31.7 ms                                                 | 59.2 ms: 1.87x slower                                 |
| mako            | 16.1 ms                                                 | 30.6 ms: 1.90x slower                                 |
| Geometric mean  | (ref)                                                   | 1.80x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|--------------------------|:-------------------------------------------------------:|:-----------------------------------------------------:|
| create_gc_cycles         | 2.46 ms                                                 | 1.95 ms: 1.26x faster                                 |
| async_tree_io_tg         | 1.46 sec                                                | 1.19 sec: 1.22x faster                                |
| gc_traversal             | 5.91 ms                                                 | 5.18 ms: 1.14x faster                                 |
| bench_mp_pool            | 19.4 ms                                                 | 17.0 ms: 1.14x faster                                 |
| regex_dna                | 288 ms                                                  | 297 ms: 1.03x slower                                  |
| async_tree_none          | 576 ms                                                  | 614 ms: 1.07x slower                                  |
| sqlite_synth             | 4.07 us                                                 | 4.35 us: 1.07x slower                                 |
| async_tree_cpu_io_mixed  | 899 ms                                                  | 974 ms: 1.08x slower                                  |
| unpickle                 | 21.4 us                                                 | 23.1 us: 1.08x slower                                 |
| pidigits                 | 248 ms                                                  | 275 ms: 1.11x slower                                  |
| regex_v8                 | 32.4 ms                                                 | 36.7 ms: 1.13x slower                                 |
| asyncio_tcp              | 985 ms                                                  | 1.12 sec: 1.14x slower                                |
| unpickle_list            | 6.67 us                                                 | 7.97 us: 1.20x slower                                 |
| json_dumps               | 14.9 ms                                                 | 17.9 ms: 1.20x slower                                 |
| asyncio_tcp_ssl          | 2.79 sec                                                | 3.41 sec: 1.22x slower                                |
| deepcopy                 | 484 us                                                  | 596 us: 1.23x slower                                  |
| telco                    | 11.4 ms                                                 | 14.1 ms: 1.24x slower                                 |
| pylint                   | 472 ms                                                  | 586 ms: 1.24x slower                                  |
| docutils                 | 4.01 sec                                                | 5.02 sec: 1.25x slower                                |
| pathlib                  | 29.3 ms                                                 | 37.5 ms: 1.28x slower                                 |
| async_generators         | 592 ms                                                  | 763 ms: 1.29x slower                                  |
| meteor_contest           | 157 ms                                                  | 203 ms: 1.29x slower                                  |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 9.11 ms: 1.30x slower                                 |
| deepcopy_reduce          | 4.27 us                                                 | 5.58 us: 1.31x slower                                 |
| json                     | 6.55 ms                                                 | 8.77 ms: 1.34x slower                                 |
| json_loads               | 36.1 us                                                 | 48.4 us: 1.34x slower                                 |
| scimark_fft              | 477 ms                                                  | 642 ms: 1.35x slower                                  |
| generators               | 39.2 ms                                                 | 53.0 ms: 1.35x slower                                 |
| deepcopy_memo            | 51.7 us                                                 | 70.9 us: 1.37x slower                                 |
| coverage                 | 110 ms                                                  | 152 ms: 1.38x slower                                  |
| xml_etree_generate       | 129 ms                                                  | 180 ms: 1.39x slower                                  |
| mdp                      | 3.80 sec                                                | 5.29 sec: 1.39x slower                                |
| pycparser                | 1.57 sec                                                | 2.21 sec: 1.41x slower                                |
| python_startup           | 22.0 ms                                                 | 31.2 ms: 1.41x slower                                 |
| fannkuch                 | 543 ms                                                  | 786 ms: 1.45x slower                                  |
| coroutines               | 29.2 ms                                                 | 43.6 ms: 1.49x slower                                 |
| crypto_pyaes             | 99.8 ms                                                 | 150 ms: 1.50x slower                                  |
| html5lib                 | 98.1 ms                                                 | 149 ms: 1.52x slower                                  |
| thrift                   | 1.11 ms                                                 | 1.70 ms: 1.52x slower                                 |
| bench_thread_pool        | 3.06 ms                                                 | 4.67 ms: 1.53x slower                                 |
| xml_etree_process        | 86.5 ms                                                 | 133 ms: 1.54x slower                                  |
| spectral_norm            | 159 ms                                                  | 245 ms: 1.54x slower                                  |
| python_startup_no_site   | 14.6 ms                                                 | 22.7 ms: 1.55x slower                                 |
| tomli_loads              | 2.80 sec                                                | 4.36 sec: 1.56x slower                                |
| 2to3                     | 442 ms                                                  | 698 ms: 1.58x slower                                  |
| nqueens                  | 108 ms                                                  | 175 ms: 1.62x slower                                  |
| richards                 | 65.8 ms                                                 | 107 ms: 1.63x slower                                  |
| sympy_integrate          | 29.7 ms                                                 | 48.4 ms: 1.63x slower                                 |
| typing_runtime_protocols | 216 us                                                  | 355 us: 1.64x slower                                  |
| sqlglot_normalize        | 146 ms                                                  | 240 ms: 1.65x slower                                  |
| bpe_tokeniser            | 6.25 sec                                                | 10.3 sec: 1.65x slower                                |
| float                    | 115 ms                                                  | 191 ms: 1.66x slower                                  |
| logging_simple           | 8.98 us                                                 | 14.9 us: 1.66x slower                                 |
| sqlglot_optimize         | 76.2 ms                                                 | 128 ms: 1.68x slower                                  |
| regex_compile            | 177 ms                                                  | 303 ms: 1.71x slower                                  |
| pyflate                  | 661 ms                                                  | 1.13 sec: 1.71x slower                                |
| django_template          | 46.9 ms                                                 | 80.8 ms: 1.72x slower                                 |
| genshi_xml               | 68.3 ms                                                 | 118 ms: 1.73x slower                                  |
| tornado_http             | 248 ms                                                  | 429 ms: 1.73x slower                                  |
| pprint_pformat           | 2.00 sec                                                | 3.57 sec: 1.79x slower                                |
| richards_super           | 76.3 ms                                                 | 137 ms: 1.79x slower                                  |
| pprint_safe_repr         | 959 ms                                                  | 1.77 sec: 1.85x slower                                |
| genshi_text              | 31.7 ms                                                 | 59.2 ms: 1.87x slower                                 |
| logging_format           | 9.48 us                                                 | 17.9 us: 1.88x slower                                 |
| comprehensions           | 20.9 us                                                 | 39.5 us: 1.89x slower                                 |
| scimark_monte_carlo      | 89.9 ms                                                 | 170 ms: 1.89x slower                                  |
| mako                     | 16.1 ms                                                 | 30.6 ms: 1.90x slower                                 |
| unpickle_pure_python     | 296 us                                                  | 574 us: 1.94x slower                                  |
| hexiom                   | 8.35 ms                                                 | 16.3 ms: 1.95x slower                                 |
| sqlglot_transpile        | 2.30 ms                                                 | 4.53 ms: 1.97x slower                                 |
| sympy_str                | 367 ms                                                  | 730 ms: 1.99x slower                                  |
| logging_silent           | 130 ns                                                  | 267 ns: 2.05x slower                                  |
| scimark_sor              | 172 ms                                                  | 354 ms: 2.06x slower                                  |
| chaos                    | 84.7 ms                                                 | 175 ms: 2.07x slower                                  |
| sympy_expand             | 631 ms                                                  | 1.31 sec: 2.08x slower                                |
| sqlglot_parse            | 1.80 ms                                                 | 3.81 ms: 2.12x slower                                 |
| scimark_lu               | 154 ms                                                  | 330 ms: 2.14x slower                                  |
| pickle_pure_python       | 417 us                                                  | 910 us: 2.18x slower                                  |
| go                       | 195 ms                                                  | 452 ms: 2.31x slower                                  |
| raytrace                 | 350 ms                                                  | 816 ms: 2.33x slower                                  |
| sympy_sum                | 213 ms                                                  | 509 ms: 2.39x slower                                  |
| deltablue                | 4.56 ms                                                 | 11.3 ms: 2.48x slower                                 |
| nbody                    | 124 ms                                                  | 317 ms: 2.56x slower                                  |
| unpack_sequence          | 73.9 ns                                                 | 191 ns: 2.58x slower                                  |
| Geometric mean           | (ref)                                                   | 1.45x slower                                          |

Benchmark hidden because not significant (12): async_tree_memoization_tg, async_tree_io, async_tree_none_tg, pickle_list, regex_effbot, pickle_dict, async_tree_cpu_io_mixed_tg, xml_etree_parse, xml_etree_iterparse, async_tree_memoization, asyncio_websockets, pickle
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.40x
- 95% likely to have a slowdown of 1.38x
- 99% likely to have a slowdown of 1.33x

# Memory
- memory change: 1.15x