# Results vs. 3.13.0rc2

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: linux-x86_64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.023x faster
- HPT reliability: 87.26%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 257 ms: 1.01x faster                                                        |
| docutils       | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 320 ms: 1.43x faster                                                        |
| async_tree_io              | 881 ms                                                                 | 632 ms: 1.39x faster                                                        |
| async_tree_io_tg           | 901 ms                                                                 | 646 ms: 1.39x faster                                                        |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 511 ms: 1.30x faster                                                        |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 492 ms: 1.29x faster                                                        |
| async_tree_none_tg         | 333 ms                                                                 | 259 ms: 1.28x faster                                                        |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.27x faster                                                        |
| async_generators           | 375 ms                                                                 | 337 ms: 1.11x faster                                                        |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                       |
| Geometric mean             | (ref)                                                                  | 1.24x faster                                                                |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 75.0 ms: 1.02x faster                                                       |
| pidigits       | 216 ms                                                                 | 227 ms: 1.05x slower                                                        |
| nbody          | 85.3 ms                                                                | 102 ms: 1.20x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.80 ms: 1.15x faster                                                       |
| regex_dna      | 189 ms                                                                 | 181 ms: 1.04x faster                                                        |
| regex_v8       | 23.2 ms                                                                | 22.4 ms: 1.04x faster                                                       |
| regex_compile  | 131 ms                                                                 | 129 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.04x faster                                                        |
| json_loads           | 27.3 us                                                                | 27.0 us: 1.01x faster                                                       |
| xml_etree_iterparse  | 94.4 ms                                                                | 93.4 ms: 1.01x faster                                                       |
| xml_etree_generate   | 85.4 ms                                                                | 84.7 ms: 1.01x faster                                                       |
| xml_etree_process    | 59.2 ms                                                                | 60.1 ms: 1.01x slower                                                       |
| json_dumps           | 10.6 ms                                                                | 11.2 ms: 1.06x slower                                                       |
| unpickle_pure_python | 208 us                                                                 | 224 us: 1.07x slower                                                        |
| pickle_pure_python   | 292 us                                                                 | 321 us: 1.10x slower                                                        |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                                |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.62 ms: 1.16x slower                                                       |
| python_startup         | 11.0 ms                                                                | 14.9 ms: 1.35x slower                                                       |
| Geometric mean         | (ref)                                                                  | 1.25x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 50.5 ms: 1.03x slower                                                       |
| genshi_text     | 21.7 ms                                                                | 22.5 ms: 1.04x slower                                                       |
| django_template | 34.2 ms                                                                | 35.8 ms: 1.05x slower                                                       |
| mako            | 11.2 ms                                                                | 12.3 ms: 1.10x slower                                                       |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 320 ms: 1.43x faster                                                        |
| async_tree_io              | 881 ms                                                                 | 632 ms: 1.39x faster                                                        |
| async_tree_io_tg           | 901 ms                                                                 | 646 ms: 1.39x faster                                                        |
| deepcopy                   | 357 us                                                                 | 263 us: 1.36x faster                                                        |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                                        |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 511 ms: 1.30x faster                                                        |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 492 ms: 1.29x faster                                                        |
| async_tree_none_tg         | 333 ms                                                                 | 259 ms: 1.28x faster                                                        |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.27x faster                                                        |
| deepcopy_memo              | 38.1 us                                                                | 30.6 us: 1.24x faster                                                       |
| go                         | 141 ms                                                                 | 116 ms: 1.21x faster                                                        |
| deepcopy_reduce            | 3.12 us                                                                | 2.70 us: 1.16x faster                                                       |
| scimark_sor                | 134 ms                                                                 | 116 ms: 1.15x faster                                                        |
| regex_effbot               | 3.21 ms                                                                | 2.80 ms: 1.15x faster                                                       |
| pylint                     | 317 ms                                                                 | 282 ms: 1.12x faster                                                        |
| async_generators           | 375 ms                                                                 | 337 ms: 1.11x faster                                                        |
| dulwich_log                | 74.5 ms                                                                | 67.1 ms: 1.11x faster                                                       |
| spectral_norm              | 108 ms                                                                 | 97.2 ms: 1.11x faster                                                       |
| pyflate                    | 449 ms                                                                 | 424 ms: 1.06x faster                                                        |
| telco                      | 7.77 ms                                                                | 7.42 ms: 1.05x faster                                                       |
| logging_format             | 6.92 us                                                                | 6.63 us: 1.04x faster                                                       |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.04x faster                                                        |
| regex_dna                  | 189 ms                                                                 | 181 ms: 1.04x faster                                                        |
| richards                   | 44.4 ms                                                                | 42.7 ms: 1.04x faster                                                       |
| regex_v8                   | 23.2 ms                                                                | 22.4 ms: 1.04x faster                                                       |
| richards_super             | 50.4 ms                                                                | 49.1 ms: 1.03x faster                                                       |
| coverage                   | 82.5 ms                                                                | 80.5 ms: 1.02x faster                                                       |
| json                       | 4.98 ms                                                                | 4.86 ms: 1.02x faster                                                       |
| float                      | 76.7 ms                                                                | 75.0 ms: 1.02x faster                                                       |
| scimark_fft                | 348 ms                                                                 | 340 ms: 1.02x faster                                                        |
| regex_compile              | 131 ms                                                                 | 129 ms: 1.02x faster                                                        |
| docutils                   | 2.63 sec                                                               | 2.58 sec: 1.02x faster                                                      |
| json_loads                 | 27.3 us                                                                | 27.0 us: 1.01x faster                                                       |
| logging_simple             | 6.14 us                                                                | 6.07 us: 1.01x faster                                                       |
| xml_etree_iterparse        | 94.4 ms                                                                | 93.4 ms: 1.01x faster                                                       |
| 2to3                       | 259 ms                                                                 | 257 ms: 1.01x faster                                                        |
| xml_etree_generate         | 85.4 ms                                                                | 84.7 ms: 1.01x faster                                                       |
| mdp                        | 2.34 sec                                                               | 2.32 sec: 1.01x faster                                                      |
| bpe_tokeniser              | 4.46 sec                                                               | 4.44 sec: 1.00x faster                                                      |
| sympy_integrate            | 19.7 ms                                                                | 19.6 ms: 1.00x faster                                                       |
| sympy_sum                  | 154 ms                                                                 | 156 ms: 1.01x slower                                                        |
| meteor_contest             | 101 ms                                                                 | 102 ms: 1.01x slower                                                        |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                       |
| sympy_str                  | 274 ms                                                                 | 277 ms: 1.01x slower                                                        |
| scimark_monte_carlo        | 65.8 ms                                                                | 66.5 ms: 1.01x slower                                                       |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                       |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.01x slower                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 158 us: 1.01x slower                                                        |
| xml_etree_process          | 59.2 ms                                                                | 60.1 ms: 1.01x slower                                                       |
| logging_silent             | 98.2 ns                                                                | 99.9 ns: 1.02x slower                                                       |
| deltablue                  | 3.10 ms                                                                | 3.17 ms: 1.02x slower                                                       |
| sympy_expand               | 454 ms                                                                 | 465 ms: 1.02x slower                                                        |
| pprint_safe_repr           | 719 ms                                                                 | 736 ms: 1.02x slower                                                        |
| hexiom                     | 5.95 ms                                                                | 6.10 ms: 1.02x slower                                                       |
| pprint_pformat             | 1.46 sec                                                               | 1.50 sec: 1.03x slower                                                      |
| comprehensions             | 16.6 us                                                                | 17.1 us: 1.03x slower                                                       |
| genshi_xml                 | 49.1 ms                                                                | 50.5 ms: 1.03x slower                                                       |
| genshi_text                | 21.7 ms                                                                | 22.5 ms: 1.04x slower                                                       |
| generators                 | 28.5 ms                                                                | 29.7 ms: 1.04x slower                                                       |
| chaos                      | 56.3 ms                                                                | 58.6 ms: 1.04x slower                                                       |
| scimark_lu                 | 112 ms                                                                 | 117 ms: 1.04x slower                                                        |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.97 ms: 1.05x slower                                                       |
| pidigits                   | 216 ms                                                                 | 227 ms: 1.05x slower                                                        |
| django_template            | 34.2 ms                                                                | 35.8 ms: 1.05x slower                                                       |
| nqueens                    | 77.7 ms                                                                | 81.9 ms: 1.05x slower                                                       |
| json_dumps                 | 10.6 ms                                                                | 11.2 ms: 1.06x slower                                                       |
| crypto_pyaes               | 68.2 ms                                                                | 72.4 ms: 1.06x slower                                                       |
| unpickle_pure_python       | 208 us                                                                 | 224 us: 1.07x slower                                                        |
| raytrace                   | 250 ms                                                                 | 269 ms: 1.08x slower                                                        |
| fannkuch                   | 376 ms                                                                 | 408 ms: 1.09x slower                                                        |
| mako                       | 11.2 ms                                                                | 12.3 ms: 1.10x slower                                                       |
| pickle_pure_python         | 292 us                                                                 | 321 us: 1.10x slower                                                        |
| bench_thread_pool          | 924 us                                                                 | 1.05 ms: 1.14x slower                                                       |
| python_startup_no_site     | 7.41 ms                                                                | 8.62 ms: 1.16x slower                                                       |
| nbody                      | 85.3 ms                                                                | 102 ms: 1.20x slower                                                        |
| python_startup             | 11.0 ms                                                                | 14.9 ms: 1.35x slower                                                       |
| gc_traversal               | 3.32 ms                                                                | 4.64 ms: 1.40x slower                                                       |
| create_gc_cycles           | 1.33 ms                                                                | 1.87 ms: 1.40x slower                                                       |
| bench_mp_pool              | 11.0 ms                                                                | 89.6 ms: 8.15x slower                                                       |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                                |

Benchmark hidden because not significant (4): sqlite_synth, asyncio_websockets, tomli_loads, thrift
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250330-3.14.0a6+-579bd08/bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.023x faster

# HPT report

- Reliability score: 87.26% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x