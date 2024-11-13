# Results vs. base

- fork: Eclips4
- ref: ft_specialize_unpack
- machine: linux-x86_64
- commit hash: d49e9e6
- commit date: 2024-11-08
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 417 ms                                                                 | 395 ms: 1.06x faster                                                    |
| docutils       | 3.41 sec                                                               | 3.36 sec: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|--------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| asyncio_websockets | 518 ms                                                                 | 521 ms: 1.00x slower                                                    |
| coroutines         | 31.1 ms                                                                | 31.7 ms: 1.02x slower                                                   |
| Geometric mean     | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (3): async_generators, asyncio_tcp_ssl, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 205 ms                                                                 | 171 ms: 1.20x faster                                                    |
| pidigits       | 183 ms                                                                 | 185 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 231 ms                                                                 | 227 ms: 1.02x faster                                                    |
| regex_effbot   | 3.00 ms                                                                | 3.03 ms: 1.01x slower                                                   |
| regex_dna      | 182 ms                                                                 | 185 ms: 1.02x slower                                                    |
| regex_v8       | 24.6 ms                                                                | 25.0 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 111 ms                                                                 | 103 ms: 1.07x faster                                                    |
| tomli_loads          | 3.24 sec                                                               | 3.18 sec: 1.02x faster                                                  |
| pickle_pure_python   | 630 us                                                                 | 618 us: 1.02x faster                                                    |
| xml_etree_process    | 93.9 ms                                                                | 93.0 ms: 1.01x faster                                                   |
| xml_etree_parse      | 134 ms                                                                 | 133 ms: 1.01x faster                                                    |
| pickle_list          | 5.18 us                                                                | 5.16 us: 1.00x faster                                                   |
| json_loads           | 29.9 us                                                                | 29.8 us: 1.00x faster                                                   |
| pickle_dict          | 31.6 us                                                                | 31.6 us: 1.00x slower                                                   |
| json_dumps           | 15.2 ms                                                                | 15.3 ms: 1.01x slower                                                   |
| unpickle_pure_python | 423 us                                                                 | 429 us: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (4): unpickle, xml_etree_generate, unpickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 10.2 ms                                                                | 10.2 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml     | 82.8 ms                                                                | 79.3 ms: 1.04x faster                                                   |
| mako           | 21.2 ms                                                                | 20.7 ms: 1.02x faster                                                   |
| genshi_text    | 40.5 ms                                                                | 40.0 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpack_sequence          | 146 ns                                                                 | 65.8 ns: 2.22x faster                                                   |
| nbody                    | 205 ms                                                                 | 171 ms: 1.20x faster                                                    |
| spectral_norm            | 162 ms                                                                 | 147 ms: 1.10x faster                                                    |
| scimark_sor              | 278 ms                                                                 | 254 ms: 1.09x faster                                                    |
| xml_etree_iterparse      | 111 ms                                                                 | 103 ms: 1.07x faster                                                    |
| 2to3                     | 417 ms                                                                 | 395 ms: 1.06x faster                                                    |
| mdp                      | 3.14 sec                                                               | 2.97 sec: 1.06x faster                                                  |
| sqlglot_normalize        | 184 ms                                                                 | 176 ms: 1.05x faster                                                    |
| scimark_sparse_mat_mult  | 6.19 ms                                                                | 5.92 ms: 1.05x faster                                                   |
| genshi_xml               | 82.8 ms                                                                | 79.3 ms: 1.04x faster                                                   |
| pprint_safe_repr         | 1.35 sec                                                               | 1.29 sec: 1.04x faster                                                  |
| pprint_pformat           | 2.78 sec                                                               | 2.68 sec: 1.04x faster                                                  |
| telco                    | 9.56 ms                                                                | 9.22 ms: 1.04x faster                                                   |
| sqlglot_optimize         | 92.2 ms                                                                | 89.1 ms: 1.03x faster                                                   |
| deepcopy_reduce          | 4.68 us                                                                | 4.53 us: 1.03x faster                                                   |
| deepcopy                 | 437 us                                                                 | 424 us: 1.03x faster                                                    |
| sympy_str                | 543 ms                                                                 | 528 ms: 1.03x faster                                                    |
| scimark_fft              | 427 ms                                                                 | 416 ms: 1.03x faster                                                    |
| json                     | 5.55 ms                                                                | 5.43 ms: 1.02x faster                                                   |
| mako                     | 21.2 ms                                                                | 20.7 ms: 1.02x faster                                                   |
| tomli_loads              | 3.24 sec                                                               | 3.18 sec: 1.02x faster                                                  |
| pycparser                | 1.75 sec                                                               | 1.72 sec: 1.02x faster                                                  |
| sympy_sum                | 382 ms                                                                 | 374 ms: 1.02x faster                                                    |
| pickle_pure_python       | 630 us                                                                 | 618 us: 1.02x faster                                                    |
| scimark_monte_carlo      | 130 ms                                                                 | 127 ms: 1.02x faster                                                    |
| generators               | 41.9 ms                                                                | 41.2 ms: 1.02x faster                                                   |
| fannkuch                 | 571 ms                                                                 | 562 ms: 1.02x faster                                                    |
| sympy_expand             | 1.06 sec                                                               | 1.05 sec: 1.02x faster                                                  |
| regex_compile            | 231 ms                                                                 | 227 ms: 1.02x faster                                                    |
| docutils                 | 3.41 sec                                                               | 3.36 sec: 1.02x faster                                                  |
| scimark_lu               | 247 ms                                                                 | 244 ms: 1.01x faster                                                    |
| chaos                    | 124 ms                                                                 | 122 ms: 1.01x faster                                                    |
| deepcopy_memo            | 54.2 us                                                                | 53.5 us: 1.01x faster                                                   |
| genshi_text              | 40.5 ms                                                                | 40.0 ms: 1.01x faster                                                   |
| bench_thread_pool        | 3.51 ms                                                                | 3.47 ms: 1.01x faster                                                   |
| bpe_tokeniser            | 6.19 sec                                                               | 6.12 sec: 1.01x faster                                                  |
| dulwich_log              | 105 ms                                                                 | 104 ms: 1.01x faster                                                    |
| raytrace                 | 634 ms                                                                 | 628 ms: 1.01x faster                                                    |
| sqlglot_parse            | 2.86 ms                                                                | 2.83 ms: 1.01x faster                                                   |
| pyflate                  | 780 ms                                                                 | 773 ms: 1.01x faster                                                    |
| xml_etree_process        | 93.9 ms                                                                | 93.0 ms: 1.01x faster                                                   |
| xml_etree_parse          | 134 ms                                                                 | 133 ms: 1.01x faster                                                    |
| sympy_integrate          | 33.2 ms                                                                | 32.9 ms: 1.01x faster                                                   |
| create_gc_cycles         | 1.11 ms                                                                | 1.11 ms: 1.01x faster                                                   |
| pathlib                  | 22.1 ms                                                                | 22.0 ms: 1.01x faster                                                   |
| pickle_list              | 5.18 us                                                                | 5.16 us: 1.00x faster                                                   |
| json_loads               | 29.9 us                                                                | 29.8 us: 1.00x faster                                                   |
| crypto_pyaes             | 109 ms                                                                 | 108 ms: 1.00x faster                                                    |
| python_startup_no_site   | 10.2 ms                                                                | 10.2 ms: 1.00x faster                                                   |
| pickle_dict              | 31.6 us                                                                | 31.6 us: 1.00x slower                                                   |
| asyncio_websockets       | 518 ms                                                                 | 521 ms: 1.00x slower                                                    |
| richards_super           | 109 ms                                                                 | 110 ms: 1.01x slower                                                    |
| json_dumps               | 15.2 ms                                                                | 15.3 ms: 1.01x slower                                                   |
| coverage                 | 102 ms                                                                 | 103 ms: 1.01x slower                                                    |
| logging_simple           | 12.4 us                                                                | 12.5 us: 1.01x slower                                                   |
| regex_effbot             | 3.00 ms                                                                | 3.03 ms: 1.01x slower                                                   |
| deltablue                | 9.19 ms                                                                | 9.30 ms: 1.01x slower                                                   |
| unpickle_pure_python     | 423 us                                                                 | 429 us: 1.01x slower                                                    |
| nqueens                  | 115 ms                                                                 | 117 ms: 1.01x slower                                                    |
| pidigits                 | 183 ms                                                                 | 185 ms: 1.01x slower                                                    |
| typing_runtime_protocols | 250 us                                                                 | 254 us: 1.01x slower                                                    |
| meteor_contest           | 139 ms                                                                 | 141 ms: 1.01x slower                                                    |
| regex_dna                | 182 ms                                                                 | 185 ms: 1.02x slower                                                    |
| regex_v8                 | 24.6 ms                                                                | 25.0 ms: 1.02x slower                                                   |
| coroutines               | 31.1 ms                                                                | 31.7 ms: 1.02x slower                                                   |
| thrift                   | 1.28 ms                                                                | 1.30 ms: 1.02x slower                                                   |
| go                       | 305 ms                                                                 | 312 ms: 1.02x slower                                                    |
| logging_silent           | 216 ns                                                                 | 222 ns: 1.02x slower                                                    |
| Geometric mean           | (ref)                                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (20): sqlglot_transpile, pylint, hexiom, unpickle, gc_traversal, xml_etree_generate, async_generators, richards, bench_mp_pool, python_startup, asyncio_tcp_ssl, comprehensions, html5lib, unpickle_list, asyncio_tcp, float, django_template, pickle, logging_format, sqlite_synth

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x