bash
```
│   .gitignore
│   LICENSE
│   pytest.ini
│   README.md
│   SimuQuant workspace.code-workspace
│   __init__.py
│
├───asim
│   ├───layer2_advanced_simulation
│   │       buy_on_crash_analyzer.py
│   │       buy_on_dip_analyzer.py
│   │       collect_mc_metrics.py
│   │       compute_horizon_var_top10.py
│   │       dedup_final_top10.py
│   │       fix_missing_mc_variants.py
│   │       flag_final_candidates.py
│   │       generate_final_artifacts.py
│   │       macro_overlay_evaluator.py
│   │       mc_simulator.py
│   │       produce_final_top10.py
│   │       produce_summary_tables.py
│   │       rank_candidates_buy_on_crash.py
│   │       rank_candidates_to_buy.py
│   │       rank_seasonality_candidates.py
│   │       rank_seasonality_with_mc.py
│   │       rank_timing_candidates.py
│   │       README.md
│   │       run_full_mc_top_candidates.py
│   │       run_mode_a.py
│   │       run_mode_b.py
│   │       run_targeted_full_mc.py
│   │       score_synthesizer.py
│   │       setup_result_folders.py
│   │       signal_classifier.py
│   │       top_candidate_selector.py
│   │       validate_var_scale.py
│   │       __init__.py
│   │
│   ├───layer3_insight_engine
│   │       buy_on_crash_mc_analyzer.py
│   │       buy_on_dip_mc_analyzer.py
│   │       mode_comparator.py
│   │       mode_comparator_timing.py
│   │       README_report_builder.md
│   │       report_builder.py
│   │       seasonal_buy_week_selector.py
│   │       __init__.py
│   │
│   ├───money_manager
│   │   │   __init__.py
│   │   │
│   │   ├───common
│   │   │       config_loader.py
│   │   │       info.py
│   │   │       __init__.py
│   │   │
│   │   ├───dynamic_model
│   │   │   │   .gitignore
│   │   │   │   dynamicsizer.py
│   │   │   │
│   │   │   └───src
│   │   │           output_handler.py
│   │   │           trading_models.py
│   │   │
│   │   ├───post_analysis
│   │   │       postsizeranalysis.py
│   │   │       __init__.py
│   │   │
│   │   └───static_model
│   │           staticsizer.py
│   │           __init__.py
│   │
│   ├───reporting_center
│   │   │   active_signals_dashboard.py
│   │   │   dispatcher.py
│   │   │   export_center.py
│   │   │   IMPLEMENTATION_SUMMARY.md
│   │   │   INTEGRATION_GUIDE.md
│   │   │   macro_market_assessment.py
│   │   │   portfolio_groups.py
│   │   │   portfolio_group_overview.py
│   │   │   symbol_deep_dive.py
│   │   │   symbol_deep_dive_old.py
│   │   │   symbol_name_mapper.py
│   │   │   weekly_entry_calendar.py
│   │   │   __init__.py
│   │   │
│   │   └───export
│   │           reporting_exporter.py
│   │           __init__.py
│   │
│   ├───seasonality
│   │   │   asim_seasonality_finder.py
│   │   │   config_loader.py
│   │   │   README.md
│   │   │   __init__.py
│   │   │
│   │   ├───backtester
│   │   │       seasonality_backtester.py
│   │   │       __init__.py
│   │   │
│   │   ├───cycle_scout
│   │   │       cycle_scout.py
│   │   │       __init__.py
│   │   │
│   │   ├───docs
│   │   │       readme_docker_usage.md
│   │   │       readme_kubernetes_usage.md
│   │   │
│   │   ├───entry_finder
│   │   │       seasonality_entry_finder.py
│   │   │       __init__.py
│   │   │
│   │   └───weekday_finder
│   │           weekday_finder.py
│   │
│   └───timing
│           bond_market_stress.py
│           buy_on_crash.py
│           buy_on_dip.py
│           daily_signal_checker.py
│           macro_overlay.py
│           macro_overlay_carry_trade_stress.py
│           macro_overlay_sovereign_stress.py
│           macro_overlay_yield_collapse_stress.py
│           macro_overlay_yield_spike_stress.py
│           yield_collapse_stress_legend.md
│           yield_spike_stress_legend.md
│           __init__.py
│
├───config
│   ├───advanced_analytics
│   │   └───insights
│   │           run_modes.yaml
│   │
│   ├───config_runtime
│   └───symbols_config
│           approved_symbols.yaml
│
├───data
│   │   macro_downloader.py
│   │   vendor_config.py
│   │
│   ├───clean
│   │   └───diagnostics
│   ├───macro
│   │       bund10y_germany_fred.csv
│   │       cpi_germany.csv
│   │       cpi_us.csv
│   │       djia.csv
│   │       dj_utilities.csv
│   │       ecb_deposit_rate.csv
│   │       eurusd.csv
│   │       fed_funds_rate.csv
│   │       france_10y.csv
│   │       gdp_germany.csv
│   │       germany_10y.csv
│   │       gold.csv
│   │       interest_rate_germany_combined.csv
│   │       lqd.csv
│   │       move_index.csv
│   │       nasdaq.csv
│   │       oil_brent.csv
│   │       oil_us_crude.csv
│   │       sd3e.csv
│   │       sx5e.csv
│   │       sx6p.csv
│   │       treasury_13w.csv
│   │       treasury_5y.csv
│   │       unemployment_germany.csv
│   │       unemployment_us.csv
│   │       usdjpy.csv
│   │       us_10y_tnote.csv
│   │       vix.csv
│   │
│   ├───macro_archive
│   ├───preparation
│   │       cleaner.py
│   │       downloader.py
│   │       run_clean_pipeline.py
│   │       save_clean_data.py
│   │       save_raw_data.py
│   │       simulate_data.py
│   │       structure.py
│   │       __init__.py
│   │
│   ├───quality
│   │       deep_gap_scan.py
│   │       diagnostics.py
│   │       expected_non_trading_days.py
│   │       fallback_handler.py
│   │       filter_symbols.py
│   │       interpolation.py
│   │       preprocessor.py
│   │       quality_dashboard.py
│   │       quality_labels.py
│   │       run_diagnostics_cli.py
│   │       __init__.py
│   │
│   ├───raw
│   └───symbols_config
│           approved_symbols.yaml
│
├───products
│   ├───alpha_1
│   │   │   dispatcher.py
│   │   │   __init__.py
│   │   │   __main__.py
│   │   │
│   │   └───configs
│   │           backtester_config.yaml
│   │           cycle_scout_config.yaml
│   │           mm_config.yaml
│   │           mm_config_live.yaml
│   │
│   └───alpha_2
│           backtester.py
│           config.yaml
│           dispatcher.py
│           scanner.py
│           __init__.py
│           __main__.py
│
├───results
│   └───alpha_1
├───test
│   │   conftest.py
│   │   README.md
│   │   __init__.py
│   │
│   ├───integration
│   │   │   dummy_utils.py
│   │   │   test_end_to_end_signal_checker.py
│   │   │   test_seasonality_pipeline.py
│   │   │   __init__.py
│   │   │
│   │   ├───advanced_analytics
│   │   │   └───insight_engine
│   │   │           test_score_synthesizer_integration.py
│   │   │
│   │   ├───data_preparation
│   │   │       test_downloader_integration.py
│   │   │       test_pipeline_chaining.py
│   │   │       test_save_raw_data_integration.py
│   │   │       __init__.py
│   │   │
│   │   ├───data_quality
│   │   │       test_cli_quality_report.py
│   │   │       test_deep_gap_scan_integration.py
│   │   │       __init__.py
│   │   │
│   │   ├───money_manager
│   │   │       test_dynamic_runner_integration.py
│   │   │       __init__.py
│   │   │
│   │   ├───risk_advisor
│   │   │       __init__.py
│   │   │
│   │   └───seasonality
│   │           test_seasonality_backtester_integration.py
│   │           test_seasonality_core_integration.py
│   │           test_seasonality_cycle_integration.py
│   │           test_seasonality_entry_integration.py
│   │           __init__.py
│   │
│   └───unit
│       │   test_action_planner.py
│       │   test_action_planner_additional.py
│       │   test_export_functions.py
│       │   test_mc_variants.py
│       │   test_mc_variants_detectors.py
│       │   test_mc_variants_extra.py
│       │   test_plot_cluster_return_overview.py
│       │   test_plot_functions.py
│       │   test_portfolio_groups.py
│       │   test_repro_run_seed.py
│       │   test_score_calculations.py
│       │   __init__.py
│       │
│       ├───advanced_analytics
│       │   │   test_buy_on_dip_mc_plot_legends.py
│       │   │   test_rank_candidates_scatter_plot.py
│       │   │
│       │   └───insight_engine
│       │           test_mc_confidence.py
│       │           test_mc_run_mode_b.py
│       │           test_mc_simulator.py
│       │           test_mc_variants.py
│       │           test_mode_comparator.py
│       │           test_score_synthesizer.py
│       │           test_score_synthesizer_extra.py
│       │           test_score_synthesizer_yaml.py
│       │           test_seasonal_buy_week_selector.py
│       │           test_signal_classifier.py
│       │           test_signal_classifier_edge_cases.py
│       │           test_signal_classifier_extra_unit.py
│       │           test_week_label_edge_cases.py
│       │
│       ├───data
│       │       test_macro_downloader.py
│       │
│       ├───data_preparation
│       │       test_cleaner.py
│       │       test_csv_export_format.py
│       │       test_data_structure.py
│       │       test_downloader.py
│       │       test_downloader_validation.py
│       │       test_save_clean_data.py
│       │       __init__.py
│       │
│       ├───data_quality
│       │       test_deep_gap_scan.py
│       │       test_dispatcher.py
│       │       test_edge_cases.py
│       │       test_expected_non_trading_days.py
│       │       test_export_approved_symbols_yaml.py
│       │       test_fallback_handler.py
│       │       test_filter_missing_days.py
│       │       test_filter_symbols.py
│       │       test_get_missing_days_returns_correct_dates.py
│       │       test_interpolation.py
│       │       test_quality_label_generator.py
│       │       test_quality_report_snapshot.py
│       │       test_run_diagnostics_cli.py
│       │       __init__.py
│       │
│       ├───layer2_advanced_simulation
│       │       test_buy_on_crash_analyzer.py
│       │       test_buy_on_dip_analyzer.py
│       │       test_rank_candidates_buy_on_crash.py
│       │       test_rank_candidates_to_buy.py
│       │       test_rank_timing_candidates.py
│       │
│       ├───layer3_insight_engine
│       │       test_buy_on_crash_mc_analyzer.py
│       │       test_buy_on_dip_mc_analyzer.py
│       │       test_mode_comparator_timing.py
│       │       test_report_builder.py
│       │       __init__.py
│       │
│       ├───macro
│       │       test_macro_archive.py
│       │
│       ├───money_manager
│       │       test_dynamic_sizer.py
│       │       test_mc_risk_metrics.py
│       │       test_mc_summary_csv.py
│       │       test_mc_summary_csv_a.py
│       │       test_mc_summary_csv_b.py
│       │       test_mm_metadata.py
│       │       test_static_sizer.py
│       │       __init__.py
│       │
│       ├───reporting_center
│       │       test_reporting_center.py
│       │       test_reporting_exporter.py
│       │       test_symbol_name_mapper.py
│       │
│       ├───seasonality
│       │       test_backtester_scoring.py
│       │       test_cycle_scout.py
│       │       test_entry_config_validation.py
│       │       test_entry_config_writer.py
│       │       test_entry_finder_utils.py
│       │       test_seasonality_finder.py
│       │       test_seasonality_utils.py
│       │       test_weekday_finder.py
│       │       __init__.py
│       │
│       ├───timing
│       │       NEW_TESTS_README.md
│       │       test_all_run_mode_integration.py
│       │       test_buy_on_crash.py
│       │       test_buy_on_crash_allsymbols_tradelog.py
│       │       test_buy_on_crash_ampel_column.py
│       │       test_buy_on_crash_check_consistency.py
│       │       test_buy_on_crash_check_consistency_of_backtesting_and_daily_signal_checker.py
│       │       test_buy_on_crash_performance_summary.py
│       │       test_buy_on_crash_portfolio_plots.py
│       │       test_buy_on_crash_robustness_classification.py
│       │       test_buy_on_crash_signal_logic.py
│       │       test_buy_on_crash_symbol_equity_curve.py
│       │       test_buy_on_dip.py
│       │       test_buy_on_dip_check_consistency_of_backtesting_and_daily_signal_checker.py
│       │       test_buy_on_dip_symbol_equity_curve.py
│       │       test_buy_on_dip_winrate_robustness.py
│       │       test_daily_signal_checker.py
│       │       test_daily_signal_checker_3day_logic.py
│       │       test_daily_signal_checker_buy_on_crash.py
│       │       test_daily_signal_checker_buy_on_dip.py
│       │       test_daily_signal_checker_crash_output.py
│       │       test_daily_signal_checker_html_output.py
│       │       test_daily_signal_checker_readable_names.py
│       │       test_macro_overlay.py
│       │       test_macro_overlay_carry_trade_stress.py
│       │       test_macro_overlay_plot.py
│       │       test_macro_overlay_resultdir.py
│       │       test_macro_overlay_sovereign_stress.py
│       │       test_macro_overlay_yield_collapse_stress.py
│       │       test_macro_overlay_yield_spike_stress.py
│       │       test_macro_stress_json_export.py
│       │       TEST_SAFETY.md
│       │       test_sentiment_indices_overlay.py
│       │       test_unified_html_reports.py
│       │
│       └───utils
│               path_utils.py
│               test_clean_artifacts_macro_protection.py
│               test_clean_artifacts_modes.py
│               test_data_loader.py
│               test_def_name_collision.py
│               test_empty_reporting_folder.py
│               test_insights.py
│               test_insights_utils.py
│               test_output_handler.py
│               test_utils_portability.py
│               test_weeknum_consistency.py
│               test_week_mapping.py
│               test_week_utils.py
│               __init__.py
│
├───tools
│       backup_macro_initial.py
│       force_high_fidelity_mc.py
│       import_smoke.py
│       run_collect_print.py
│       run_fix_missing_mc.py
│       run_high_fidelity_mc.py
│       run_show_rank_and_collect.py
│       validate_carry_trade_system.py
│
├───utils
│   │   action_planner.py
│   │   clean_artifacts.py
│   │   data_loader.py
│   │   html_report_template.py
│   │   output_handler.py
│   │   path_utils.py
│   │   seasonality.py
│   │   timestamps.py
│   │   timing.py
│   │   week_mapping.py
│   │   week_utils.py
│   │   __init__.py
│   │
│   ├───insights
│   │       cluster_utils.py
│   │       grid_search.py
│   │       insights.py
│   │       mc_variants.py
│   │       outlier_utils.py
│   │       timing_mc_forward.py
│   │       timing_mc_plots.py
│   │       timing_report_generator.py
│   │       timing_risk_classifier.py
│   │       __init__.py
│   │
│   └───macro
│           overlay_utils.py
│
└───work
        ActionPlanner.xlsx
        potential_stress_scenarios_for_next_12_months.txt
        stress_scenario_reminder_de.txt
        stress_scenario_reminder_en.txt
```
