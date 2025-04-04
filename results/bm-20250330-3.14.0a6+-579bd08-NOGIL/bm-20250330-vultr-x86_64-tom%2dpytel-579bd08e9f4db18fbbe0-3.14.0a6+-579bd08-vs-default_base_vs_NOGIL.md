# Results vs. default_base_vs_NOGIL

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: linux-x86_64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.113x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 297 ms: 1.16x slower                                                        |
| docutils       | 2.58 sec                                                               | 2.77 sec: 1.07x slower                                                      |
| sphinx         | 991 ms                                                                 | 1.10 sec: 1.11x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg           | 645 ms                                                                 | 551 ms: 1.17x faster                                                        |
| async_tree_none_tg         | 260 ms                                                                 | 238 ms: 1.09x faster                                                        |
| async_tree_io              | 628 ms                                                                 | 583 ms: 1.08x faster                                                        |
| async_tree_memoization_tg  | 312 ms                                                                 | 299 ms: 1.04x faster                                                        |
| async_tree_none            | 280 ms                                                                 | 277 ms: 1.01x faster                                                        |
| async_tree_cpu_io_mixed_tg | 496 ms                                                                 | 491 ms: 1.01x faster                                                        |
| coroutines                 | 23.6 ms                                                                | 23.8 ms: 1.01x slower                                                       |
| async_tree_cpu_io_mixed    | 517 ms                                                                 | 523 ms: 1.01x slower                                                        |
| async_tree_memoization     | 323 ms                                                                 | 333 ms: 1.03x slower                                                        |
| async_generators           | 335 ms                                                                 | 386 ms: 1.15x slower                                                        |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                                |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 72.8 ms                                                                | 77.7 ms: 1.07x slower                                                       |
| pidigits       | 191 ms                                                                 | 223 ms: 1.17x slower                                                        |
| nbody          | 106 ms                                                                 | 135 ms: 1.27x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 22.1 ms                                                                | 22.0 ms: 1.01x faster                                                       |
| regex_dna      | 181 ms                                                                 | 182 ms: 1.01x slower                                                        |
| regex_compile  | 127 ms                                                                 | 157 ms: 1.24x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.1 ms                                                                | 88.1 ms: 1.06x faster                                                       |
| json_loads           | 28.2 us                                                                | 28.8 us: 1.02x slower                                                       |
| pickle_pure_python   | 316 us                                                                 | 361 us: 1.14x slower                                                        |
| json_dumps           | 11.2 ms                                                                | 12.8 ms: 1.14x slower                                                       |
| xml_etree_generate   | 84.7 ms                                                                | 97.6 ms: 1.15x slower                                                       |
| unpickle_pure_python | 219 us                                                                 | 257 us: 1.18x slower                                                        |
| xml_etree_process    | 59.4 ms                                                                | 70.8 ms: 1.19x slower                                                       |
| tomli_loads          | 1.95 sec                                                               | 2.36 sec: 1.21x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                                |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                | 15.7 ms: 1.05x slower                                                       |
| python_startup_no_site | 8.62 ms                                                                | 11.1 ms: 1.28x slower                                                       |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 51.3 ms                                                                | 59.3 ms: 1.16x slower                                                       |
| django_template | 36.4 ms                                                                | 43.3 ms: 1.19x slower                                                       |
| genshi_text     | 22.7 ms                                                                | 28.2 ms: 1.24x slower                                                       |
| mako            | 12.0 ms                                                                | 16.0 ms: 1.33x slower                                                       |
| Geometric mean  | (ref)                                                                  | 1.23x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20250325-vultr-x86_64-python-96ef4c511f3ec763dbb0-3.14.0a6+-96ef4c5 | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal               | 4.25 ms                                                                | 1.79 ms: 2.38x faster                                                       |
| create_gc_cycles           | 1.86 ms                                                                | 1.35 ms: 1.38x faster                                                       |
| async_tree_io_tg           | 645 ms                                                                 | 551 ms: 1.17x faster                                                        |
| async_tree_none_tg         | 260 ms                                                                 | 238 ms: 1.09x faster                                                        |
| sqlite_synth               | 2.19 us                                                                | 2.02 us: 1.08x faster                                                       |
| async_tree_io              | 628 ms                                                                 | 583 ms: 1.08x faster                                                        |
| xml_etree_iterparse        | 93.1 ms                                                                | 88.1 ms: 1.06x faster                                                       |
| async_tree_memoization_tg  | 312 ms                                                                 | 299 ms: 1.04x faster                                                        |
| async_tree_none            | 280 ms                                                                 | 277 ms: 1.01x faster                                                        |
| async_tree_cpu_io_mixed_tg | 496 ms                                                                 | 491 ms: 1.01x faster                                                        |
| regex_v8                   | 22.1 ms                                                                | 22.0 ms: 1.01x faster                                                       |
| regex_dna                  | 181 ms                                                                 | 182 ms: 1.01x slower                                                        |
| pathlib                    | 19.6 ms                                                                | 19.8 ms: 1.01x slower                                                       |
| coroutines                 | 23.6 ms                                                                | 23.8 ms: 1.01x slower                                                       |
| async_tree_cpu_io_mixed    | 517 ms                                                                 | 523 ms: 1.01x slower                                                        |
| json                       | 4.96 ms                                                                | 5.02 ms: 1.01x slower                                                       |
| json_loads                 | 28.2 us                                                                | 28.8 us: 1.02x slower                                                       |
| async_tree_memoization     | 323 ms                                                                 | 333 ms: 1.03x slower                                                        |
| pycparser                  | 1.14 sec                                                               | 1.19 sec: 1.05x slower                                                      |
| python_startup             | 14.9 ms                                                                | 15.7 ms: 1.05x slower                                                       |
| float                      | 72.8 ms                                                                | 77.7 ms: 1.07x slower                                                       |
| docutils                   | 2.58 sec                                                               | 2.77 sec: 1.07x slower                                                      |
| bench_mp_pool              | 89.7 ms                                                                | 96.6 ms: 1.08x slower                                                       |
| generators                 | 29.6 ms                                                                | 32.0 ms: 1.08x slower                                                       |
| dulwich_log                | 66.5 ms                                                                | 72.8 ms: 1.09x slower                                                       |
| sphinx                     | 991 ms                                                                 | 1.10 sec: 1.11x slower                                                      |
| pylint                     | 283 ms                                                                 | 314 ms: 1.11x slower                                                        |
| k_core                     | 2.07 sec                                                               | 2.30 sec: 1.11x slower                                                      |
| thrift                     | 779 us                                                                 | 868 us: 1.11x slower                                                        |
| mdp                        | 2.49 sec                                                               | 2.79 sec: 1.12x slower                                                      |
| bpe_tokeniser              | 4.35 sec                                                               | 4.87 sec: 1.12x slower                                                      |
| subparsers                 | 22.4 ms                                                                | 25.2 ms: 1.12x slower                                                       |
| many_optionals             | 1.04 ms                                                                | 1.16 ms: 1.12x slower                                                       |
| pickle_pure_python         | 316 us                                                                 | 361 us: 1.14x slower                                                        |
| json_dumps                 | 11.2 ms                                                                | 12.8 ms: 1.14x slower                                                       |
| xml_etree_generate         | 84.7 ms                                                                | 97.6 ms: 1.15x slower                                                       |
| async_generators           | 335 ms                                                                 | 386 ms: 1.15x slower                                                        |
| genshi_xml                 | 51.3 ms                                                                | 59.3 ms: 1.16x slower                                                       |
| 2to3                       | 256 ms                                                                 | 297 ms: 1.16x slower                                                        |
| sqlglot_v2_normalize       | 103 ms                                                                 | 120 ms: 1.16x slower                                                        |
| deepcopy_reduce            | 2.69 us                                                                | 3.13 us: 1.16x slower                                                       |
| sqlglot_v2_optimize        | 52.3 ms                                                                | 61.0 ms: 1.17x slower                                                       |
| pidigits                   | 191 ms                                                                 | 223 ms: 1.17x slower                                                        |
| nqueens                    | 83.6 ms                                                                | 98.0 ms: 1.17x slower                                                       |
| logging_simple             | 6.15 us                                                                | 7.22 us: 1.17x slower                                                       |
| unpickle_pure_python       | 219 us                                                                 | 257 us: 1.18x slower                                                        |
| sympy_sum                  | 158 ms                                                                 | 185 ms: 1.18x slower                                                        |
| sympy_expand               | 469 ms                                                                 | 552 ms: 1.18x slower                                                        |
| pprint_safe_repr           | 721 ms                                                                 | 851 ms: 1.18x slower                                                        |
| logging_silent             | 97.8 ns                                                                | 116 ns: 1.18x slower                                                        |
| django_template            | 36.4 ms                                                                | 43.3 ms: 1.19x slower                                                       |
| deepcopy                   | 261 us                                                                 | 311 us: 1.19x slower                                                        |
| xml_etree_process          | 59.4 ms                                                                | 70.8 ms: 1.19x slower                                                       |
| logging_format             | 6.90 us                                                                | 8.22 us: 1.19x slower                                                       |
| sympy_integrate            | 19.8 ms                                                                | 23.6 ms: 1.19x slower                                                       |
| telco                      | 7.51 ms                                                                | 8.95 ms: 1.19x slower                                                       |
| chaos                      | 57.4 ms                                                                | 68.6 ms: 1.19x slower                                                       |
| pyflate                    | 419 ms                                                                 | 501 ms: 1.20x slower                                                        |
| pprint_pformat             | 1.46 sec                                                               | 1.75 sec: 1.20x slower                                                      |
| sqlalchemy_imperative      | 19.6 ms                                                                | 23.5 ms: 1.20x slower                                                       |
| sympy_str                  | 277 ms                                                                 | 334 ms: 1.21x slower                                                        |
| fannkuch                   | 406 ms                                                                 | 490 ms: 1.21x slower                                                        |
| tomli_loads                | 1.95 sec                                                               | 2.36 sec: 1.21x slower                                                      |
| sqlalchemy_declarative     | 130 ms                                                                 | 157 ms: 1.21x slower                                                        |
| scimark_sor                | 113 ms                                                                 | 137 ms: 1.22x slower                                                        |
| sqlglot_v2_transpile       | 1.58 ms                                                                | 1.94 ms: 1.22x slower                                                       |
| comprehensions             | 17.0 us                                                                | 20.8 us: 1.23x slower                                                       |
| regex_compile              | 127 ms                                                                 | 157 ms: 1.24x slower                                                        |
| scimark_fft                | 323 ms                                                                 | 399 ms: 1.24x slower                                                        |
| shortest_path              | 440 ms                                                                 | 547 ms: 1.24x slower                                                        |
| sqlglot_v2_parse           | 1.28 ms                                                                | 1.59 ms: 1.24x slower                                                       |
| genshi_text                | 22.7 ms                                                                | 28.2 ms: 1.24x slower                                                       |
| spectral_norm              | 91.4 ms                                                                | 114 ms: 1.24x slower                                                        |
| raytrace                   | 261 ms                                                                 | 326 ms: 1.25x slower                                                        |
| scimark_sparse_mat_mult    | 4.55 ms                                                                | 5.71 ms: 1.25x slower                                                       |
| scimark_lu                 | 114 ms                                                                 | 144 ms: 1.26x slower                                                        |
| deltablue                  | 3.10 ms                                                                | 3.91 ms: 1.26x slower                                                       |
| nbody                      | 106 ms                                                                 | 135 ms: 1.27x slower                                                        |
| meteor_contest             | 102 ms                                                                 | 130 ms: 1.27x slower                                                        |
| connected_components       | 396 ms                                                                 | 503 ms: 1.27x slower                                                        |
| hexiom                     | 6.05 ms                                                                | 7.75 ms: 1.28x slower                                                       |
| richards                   | 42.7 ms                                                                | 54.8 ms: 1.28x slower                                                       |
| scimark_monte_carlo        | 65.9 ms                                                                | 84.5 ms: 1.28x slower                                                       |
| crypto_pyaes               | 70.2 ms                                                                | 90.0 ms: 1.28x slower                                                       |
| python_startup_no_site     | 8.62 ms                                                                | 11.1 ms: 1.28x slower                                                       |
| typing_runtime_protocols   | 157 us                                                                 | 202 us: 1.29x slower                                                        |
| go                         | 112 ms                                                                 | 144 ms: 1.29x slower                                                        |
| deepcopy_memo              | 30.2 us                                                                | 39.1 us: 1.29x slower                                                       |
| richards_super             | 48.3 ms                                                                | 63.8 ms: 1.32x slower                                                       |
| mako                       | 12.0 ms                                                                | 16.0 ms: 1.33x slower                                                       |
| coverage                   | 79.8 ms                                                                | 109 ms: 1.36x slower                                                        |
| bench_thread_pool          | 1.05 ms                                                                | 3.16 ms: 3.00x slower                                                       |
| Geometric mean             | (ref)                                                                  | 1.14x slower                                                                |

Benchmark hidden because not significant (3): regex_effbot, xml_etree_parse, asyncio_websockets
Ignored benchmarks (1) of results/bm-20250330-3.14.0a6+-579bd08-NOGIL/bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08.json: html5lib

- Geometric mean (including insignificant results): 1.113x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.21x