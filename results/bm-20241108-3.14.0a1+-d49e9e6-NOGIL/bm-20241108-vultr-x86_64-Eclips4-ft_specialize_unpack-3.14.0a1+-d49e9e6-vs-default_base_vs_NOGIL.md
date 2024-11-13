# Results vs. default_base_vs_NOGIL

- fork: Eclips4
- ref: ft_specialize_unpack
- machine: linux-x86_64
- commit hash: d49e9e6
- commit date: 2024-11-08
- overall geometric mean: 1.51x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.39x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 395 ms: 1.55x slower                                                    |
| docutils       | 2.60 sec                                                               | 3.36 sec: 1.29x slower                                                  |
| html5lib       | 65.1 ms                                                                | 106 ms: 1.63x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.49x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| asyncio_tcp      | 506 ms                                                                 | 583 ms: 1.15x slower                                                    |
| asyncio_tcp_ssl  | 1.52 sec                                                               | 1.84 sec: 1.21x slower                                                  |
| async_generators | 369 ms                                                                 | 494 ms: 1.34x slower                                                    |
| coroutines       | 23.2 ms                                                                | 31.7 ms: 1.37x slower                                                   |
| Geometric mean   | (ref)                                                                  | 1.21x slower                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 224 ms                                                                 | 185 ms: 1.21x faster                                                    |
| nbody          | 93.8 ms                                                                | 171 ms: 1.82x slower                                                    |
| float          | 79.9 ms                                                                | 152 ms: 1.90x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.42x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.07 ms                                                                | 3.03 ms: 1.01x faster                                                   |
| regex_dna      | 186 ms                                                                 | 185 ms: 1.01x faster                                                    |
| regex_v8       | 23.5 ms                                                                | 25.0 ms: 1.06x slower                                                   |
| regex_compile  | 131 ms                                                                 | 227 ms: 1.74x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle               | 12.3 us                                                                | 12.0 us: 1.03x faster                                                   |
| pickle_dict          | 32.4 us                                                                | 31.6 us: 1.02x faster                                                   |
| xml_etree_parse      | 135 ms                                                                 | 133 ms: 1.02x faster                                                    |
| pickle_list          | 5.09 us                                                                | 5.16 us: 1.01x slower                                                   |
| unpickle_list        | 4.85 us                                                                | 5.13 us: 1.06x slower                                                   |
| xml_etree_iterparse  | 95.8 ms                                                                | 103 ms: 1.08x slower                                                    |
| unpickle             | 13.8 us                                                                | 15.0 us: 1.09x slower                                                   |
| json_loads           | 26.5 us                                                                | 29.8 us: 1.12x slower                                                   |
| json_dumps           | 11.5 ms                                                                | 15.3 ms: 1.33x slower                                                   |
| xml_etree_generate   | 84.3 ms                                                                | 114 ms: 1.36x slower                                                    |
| tomli_loads          | 2.09 sec                                                               | 3.18 sec: 1.52x slower                                                  |
| xml_etree_process    | 59.1 ms                                                                | 93.0 ms: 1.57x slower                                                   |
| pickle_pure_python   | 319 us                                                                 | 618 us: 1.94x slower                                                    |
| unpickle_pure_python | 216 us                                                                 | 429 us: 1.98x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.25x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.49 ms                                                                | 10.2 ms: 1.36x slower                                                   |
| python_startup         | 11.1 ms                                                                | 15.7 ms: 1.41x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.39x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 50.4 ms                                                                | 79.3 ms: 1.57x slower                                                   |
| genshi_text     | 22.6 ms                                                                | 40.0 ms: 1.77x slower                                                   |
| mako            | 11.7 ms                                                                | 20.7 ms: 1.77x slower                                                   |
| django_template | 35.4 ms                                                                | 65.0 ms: 1.84x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.74x slower                                                            |

All benchmarks:
===============

| Benchmark                | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                                | 2.55 ms: 1.35x faster                                                   |
| create_gc_cycles         | 1.37 ms                                                                | 1.11 ms: 1.24x faster                                                   |
| pidigits                 | 224 ms                                                                 | 185 ms: 1.21x faster                                                    |
| pickle                   | 12.3 us                                                                | 12.0 us: 1.03x faster                                                   |
| pickle_dict              | 32.4 us                                                                | 31.6 us: 1.02x faster                                                   |
| xml_etree_parse          | 135 ms                                                                 | 133 ms: 1.02x faster                                                    |
| regex_effbot             | 3.07 ms                                                                | 3.03 ms: 1.01x faster                                                   |
| regex_dna                | 186 ms                                                                 | 185 ms: 1.01x faster                                                    |
| pickle_list              | 5.09 us                                                                | 5.16 us: 1.01x slower                                                   |
| unpickle_list            | 4.85 us                                                                | 5.13 us: 1.06x slower                                                   |
| regex_v8                 | 23.5 ms                                                                | 25.0 ms: 1.06x slower                                                   |
| xml_etree_iterparse      | 95.8 ms                                                                | 103 ms: 1.08x slower                                                    |
| unpickle                 | 13.8 us                                                                | 15.0 us: 1.09x slower                                                   |
| json                     | 4.90 ms                                                                | 5.43 ms: 1.11x slower                                                   |
| json_loads               | 26.5 us                                                                | 29.8 us: 1.12x slower                                                   |
| bench_mp_pool            | 64.4 ms                                                                | 72.4 ms: 1.12x slower                                                   |
| sqlite_synth             | 2.19 us                                                                | 2.47 us: 1.13x slower                                                   |
| asyncio_tcp              | 506 ms                                                                 | 583 ms: 1.15x slower                                                    |
| asyncio_tcp_ssl          | 1.52 sec                                                               | 1.84 sec: 1.21x slower                                                  |
| pathlib                  | 18.2 ms                                                                | 22.0 ms: 1.21x slower                                                   |
| telco                    | 7.52 ms                                                                | 9.22 ms: 1.22x slower                                                   |
| scimark_fft              | 338 ms                                                                 | 416 ms: 1.23x slower                                                    |
| mdp                      | 2.37 sec                                                               | 2.97 sec: 1.25x slower                                                  |
| coverage                 | 81.1 ms                                                                | 103 ms: 1.27x slower                                                    |
| unpack_sequence          | 51.1 ns                                                                | 65.8 ns: 1.29x slower                                                   |
| docutils                 | 2.60 sec                                                               | 3.36 sec: 1.29x slower                                                  |
| scimark_sparse_mat_mult  | 4.50 ms                                                                | 5.92 ms: 1.32x slower                                                   |
| pylint                   | 318 ms                                                                 | 421 ms: 1.33x slower                                                    |
| json_dumps               | 11.5 ms                                                                | 15.3 ms: 1.33x slower                                                   |
| async_generators         | 369 ms                                                                 | 494 ms: 1.34x slower                                                    |
| spectral_norm            | 109 ms                                                                 | 147 ms: 1.35x slower                                                    |
| xml_etree_generate       | 84.3 ms                                                                | 114 ms: 1.36x slower                                                    |
| python_startup_no_site   | 7.49 ms                                                                | 10.2 ms: 1.36x slower                                                   |
| coroutines               | 23.2 ms                                                                | 31.7 ms: 1.37x slower                                                   |
| dulwich_log              | 75.5 ms                                                                | 104 ms: 1.37x slower                                                    |
| meteor_contest           | 101 ms                                                                 | 141 ms: 1.40x slower                                                    |
| bpe_tokeniser            | 4.35 sec                                                               | 6.12 sec: 1.41x slower                                                  |
| python_startup           | 11.1 ms                                                                | 15.7 ms: 1.41x slower                                                   |
| generators               | 28.8 ms                                                                | 41.2 ms: 1.43x slower                                                   |
| nqueens                  | 78.6 ms                                                                | 117 ms: 1.49x slower                                                    |
| pycparser                | 1.13 sec                                                               | 1.72 sec: 1.52x slower                                                  |
| fannkuch                 | 369 ms                                                                 | 562 ms: 1.52x slower                                                    |
| tomli_loads              | 2.09 sec                                                               | 3.18 sec: 1.52x slower                                                  |
| 2to3                     | 254 ms                                                                 | 395 ms: 1.55x slower                                                    |
| xml_etree_process        | 59.1 ms                                                                | 93.0 ms: 1.57x slower                                                   |
| genshi_xml               | 50.4 ms                                                                | 79.3 ms: 1.57x slower                                                   |
| deepcopy                 | 264 us                                                                 | 424 us: 1.61x slower                                                    |
| typing_runtime_protocols | 158 us                                                                 | 254 us: 1.61x slower                                                    |
| crypto_pyaes             | 66.7 ms                                                                | 108 ms: 1.63x slower                                                    |
| html5lib                 | 65.1 ms                                                                | 106 ms: 1.63x slower                                                    |
| sqlglot_optimize         | 53.9 ms                                                                | 89.1 ms: 1.65x slower                                                   |
| sqlglot_normalize        | 107 ms                                                                 | 176 ms: 1.65x slower                                                    |
| sympy_integrate          | 19.7 ms                                                                | 32.9 ms: 1.67x slower                                                   |
| deepcopy_reduce          | 2.64 us                                                                | 4.53 us: 1.72x slower                                                   |
| pyflate                  | 449 ms                                                                 | 773 ms: 1.72x slower                                                    |
| regex_compile            | 131 ms                                                                 | 227 ms: 1.74x slower                                                    |
| thrift                   | 746 us                                                                 | 1.30 ms: 1.75x slower                                                   |
| deepcopy_memo            | 30.6 us                                                                | 53.5 us: 1.75x slower                                                   |
| genshi_text              | 22.6 ms                                                                | 40.0 ms: 1.77x slower                                                   |
| mako                     | 11.7 ms                                                                | 20.7 ms: 1.77x slower                                                   |
| comprehensions           | 17.1 us                                                                | 30.9 us: 1.80x slower                                                   |
| nbody                    | 93.8 ms                                                                | 171 ms: 1.82x slower                                                    |
| pprint_safe_repr         | 707 ms                                                                 | 1.29 sec: 1.83x slower                                                  |
| pprint_pformat           | 1.46 sec                                                               | 2.68 sec: 1.83x slower                                                  |
| django_template          | 35.4 ms                                                                | 65.0 ms: 1.84x slower                                                   |
| scimark_sor              | 135 ms                                                                 | 254 ms: 1.89x slower                                                    |
| float                    | 79.9 ms                                                                | 152 ms: 1.90x slower                                                    |
| sympy_str                | 272 ms                                                                 | 528 ms: 1.94x slower                                                    |
| pickle_pure_python       | 319 us                                                                 | 618 us: 1.94x slower                                                    |
| scimark_monte_carlo      | 65.1 ms                                                                | 127 ms: 1.95x slower                                                    |
| unpickle_pure_python     | 216 us                                                                 | 429 us: 1.98x slower                                                    |
| richards                 | 45.9 ms                                                                | 91.4 ms: 1.99x slower                                                   |
| sqlglot_transpile        | 1.59 ms                                                                | 3.30 ms: 2.07x slower                                                   |
| logging_simple           | 6.03 us                                                                | 12.5 us: 2.07x slower                                                   |
| logging_format           | 6.67 us                                                                | 13.9 us: 2.08x slower                                                   |
| logging_silent           | 106 ns                                                                 | 222 ns: 2.08x slower                                                    |
| chaos                    | 58.4 ms                                                                | 122 ms: 2.09x slower                                                    |
| hexiom                   | 5.92 ms                                                                | 12.5 ms: 2.11x slower                                                   |
| richards_super           | 51.8 ms                                                                | 110 ms: 2.12x slower                                                    |
| scimark_lu               | 115 ms                                                                 | 244 ms: 2.13x slower                                                    |
| sqlglot_parse            | 1.30 ms                                                                | 2.83 ms: 2.19x slower                                                   |
| sympy_expand             | 458 ms                                                                 | 1.05 sec: 2.28x slower                                                  |
| raytrace                 | 263 ms                                                                 | 628 ms: 2.39x slower                                                    |
| sympy_sum                | 152 ms                                                                 | 374 ms: 2.46x slower                                                    |
| go                       | 122 ms                                                                 | 312 ms: 2.56x slower                                                    |
| deltablue                | 3.25 ms                                                                | 9.30 ms: 2.86x slower                                                   |
| bench_thread_pool        | 1.01 ms                                                                | 3.47 ms: 3.42x slower                                                   |
| Geometric mean           | (ref)                                                                  | 1.51x slower                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.46x
- 95% likely to have a slowdown of 1.43x
- 99% likely to have a slowdown of 1.39x

# Memory
- memory change: 1.21x