- // ================ CORE QUALITY ================
- "gpu_level" "1"                     // Minimum Shader Details Level 0= high
- "cpu_level" "1"                     // Minimum Effect Details Level
- "mat_set_shader_quality" "0"

// ================ FOV ================
- //"r_aspectratio" "2.15"              // [ADJUST] FOV control: 1.33=70fov | 1.56=75fov | 1.75=80fov | 2.0=85fov | 2.15=90fov | 2.49=100fov | 3.0=110fov | 3.5=120fov

// ================ LIGHTING & SHADOWS ================
- "r_directlighting" "false"              //*
- "r_ssao" "false"                        //* Disable ambient occlusion
- "r_shadows" "0"                     //* [FPS IMPACT] 0=Off (max FPS) | 1=On (shadows enabled)
- "r_rendersun" "0"                   //*
- "lb_enable_shadow_casting" "0"      // [FPS IMPACT] 0=Off (shadows disabled, +FPS) | 1=On (shadow casting enabled)
- "lb_csm_draw_alpha_tested" "0"
- "lb_csm_draw_translucent" "0"
- "lb_barnlight_shadowmap_scale" "0.01" //default 0.5
"lb_csm_cascade_size_override" "0.25" //was 1
"lb_dynamic_shadow_resolution_quantization" "32" //64
"lb_csm_override_staticgeo_cascades_value" "0"
"lb_csm_receiver_plane_depth_bias" "0.00002"
"lb_csm_receiver_plane_depth_bias_transmissive_backface" "0.0002"
"lb_sun_csm_size_cull_threshold_texels" "30"
"lb_dynamic_shadow_resolution_base" "32"
"lb_enable_fog_mixed_shadows" "0"
"r_citadel_sun_shadow_slope_scale_depth_bias" "1.0" //was 1
"r_lightmap_size_directional_irradiance" "0" //was 4
"r_size_cull_threshold_shadow" "200" //Default: 100<br>Threshold of shadow map size percentage below which objects get culled
"csm_max_shadow_dist_override" "0"
"sc_cache_envmap_lpv_lookup" "false" //was true
- "cl_retire_low_priority_lights" "1"
- "sc_disable_spotlight_shadows" "1"
- "cl_globallight_shadow_mode" "0"
- "lb_enable_dynamic_lights" "0"
"lb_enable_lights" "0" //was 1
- "lb_enable_stationary_lights" "0"         // Disable stationary lights
"lb_max_visible_barn_lights_override" "1"
"lb_max_visible_envmaps_override" "4" //default 4 DO NOT CHANGE OR IT BREAKS GAME
- "lb_ssss_samples" "0"
//"r_multiscattering" "0"                   // Disable multiscattering (only works with shadows disable)

// ================ SPARSE SHADOW TREE ================
- "sparseshadowtree_enable_rendering" "0"
- "sparseshadowtree_disable_for_viewmodel" "1"

// ================ DISTANCE FIELD ================
- "r_citadel_distancefield_farfield_enable" "false"
- "r_citadel_npr_outlines_max_dist" "600"

// ================ FOG & ATMOSPHERE ================
- "r_enable_volume_fog" "0"
- "r_enable_gradient_fog" "0"
- "r_enable_cubemap_fog" "0"
- "volume_fog_intermediate_textures_hdr" "0"

// ================ SKY & ENVIRONMENT ================
- "r_draw3dskybox" "0"
- "r_drawskybox" "1"                  // Set to 0 to disable skybox
"r_monitor_3dskybox" "0"
"r_world_wind_strength" "0"
"sv_waterdist" "0"

// ================ SSAO ================
"r_citadel_ssao_bent_normals" "false"
"r_citadel_ssao_denoise_passes" "0"
"r_citadel_ssao_quality" "0"
"r_citadel_ssao_radius" "0"
"r_citadel_ssao_thin_occluder_compensation" "0"

// ================ PARTICLE SYSTEM ================
"r_particle_max_detail_level" "0"
"r_particle_cables_cast_shadows" "0"
"r_RainParticleDensity" "0"
- "r_physics_particle_op_spawn_scale" "0"
"r_particle_max_size_cull" "1600" //was 800 Particle systems larger than this in every dimension skip culling to save CPU.  They will be drawn anyway
"particle_cluster_nodraw" "1"
"r_particle_mixed_resolution_viewstart" "800"
"r_particle_max_draw_distance" "300000" // Lower = less particle range, more FPS, dont go below this value it doesnt draw trooper hp bar,
"r_particle_model_new8" "0"
"cl_show_splashes" "0"
"r_particle_skip_postsim" "1"
"r_limit_particle_job_duration" "1"
"cl_particle_sim_fallback_threshold_ms" "0" // [ADJUST] Lower = more aggressive fallback to simple particles (higher FPS, less detail)
"cl_particle_fallback_base" "10"
"cl_particle_fallback_multiplier" "10" //was 10
"cl_particle_sim_fallback_base_multiplier" "100" //default 10
"r_particle_min_timestep" "0.001"

// ================ PHYSICS & CLOTH ================
"cloth_update" "1"                   // [FPS IMPACT] 0=Off (cosmetic only, +FPS) | 1=On (cloth physics enabled)
"cloth_sim_on_tick" "0"
"presettle_cloth_iterations" "0" //default 3
"pred_cloth_pos_max" "0"           // Reduce cloth prediction was 1
"pred_cloth_pos_multiplier" "0" //was 0.3
"pred_cloth_pos_strength" "0" //was 0.1
"pred_cloth_rot_high" "0" //was 0.05
"pred_cloth_rot_low" "0" //was 0.005
"pred_cloth_rot_multiplier" "0" //was 0.2 changing these values does fucking nothing
"cl_phys_timescale" "1"              // [FPS IMPACT] 0=Disable physics (max FPS) | 1=Normal physics | Lower = slower physics, less CPU
"cl_fasttempentcollision" "100000" //test Temp Entities" are things like shell casings hitting the floor. Increasing this number usually tells the engine to skip collision checks for them entirely or expire them instantly to avoid physics costs.

"phys_threaded_cloth_bone_update" "1"
"phys_threaded_kinematic_bone_update" "1"
"phys_threaded_transform_update" "1"

// ================ RAGDOLL ================
"cl_ragdoll_limit" "0"              // Set it on console if ragdoll still lingers longer
"ragdoll_parallel_pose_control" "1"

// ================ MODEL & DECAL OPTIMIZATIONS ================
"r_drawmodeldecals" "0" //does not exist in master convar
"r_character_decal_resolution" "0.01" //default 1
"r_decals" "1"                  // im p sure valve killed this command [ADJUST] Max decals visible: 1= only 1 bullet hole(max FPS) | 16=default
"r_propsmaxdist" "700"
"props_break_max_pieces_perframe" "0" 
"r_citadel_screenspace_particles_full_res" "0"
"r_citadel_gpu_culling_shadows" "1"
"skeleton_instance_lod_optimization" "1"
"r_size_cull_threshold" "2.5" //was 1.2, 5 is too aggressive
"r_hair_ao" "0"
"r_render_hair" "0"                   // doesnt work [FPS IMPACT] 0=Off (max FPS boost, bald heroes) | 1=On (hair rendered)
"r_haircull_percent" "100"
"ik_final_fixup_enable" "0"
"ik_fabrik_align_chain" "0"
"cl_impacteffects" "0"
"enable_boneflex" "false"            // cloth flexing
"cl_eye_yaw_multiplier" "0"

// ================ LOD & CULLING ================
- "sc_instanced_mesh_lod_bias" "15"     // [FPS IMPACT] Higher = lower quality models, more FPS | 0=High quality | 10=Low quality
- "sc_instanced_mesh_lod_bias_shadow" "10" // Bias for LOD selection of instanced meshes in shadowmaps
"sc_instanced_mesh_motion_vectors" "0" // Set 1 if you use motion blur
"sc_instanced_mesh_size_cull_bias" "10" // Bias for size culling of instanced meshes
"sc_instanced_mesh_size_cull_bias_shadow" "10" // Bias for size culling instanced meshes in shadowmaps
"sc_fade_distance_scale_override" "180"
"sc_clutter_enable" "0"                   // [FPS IMPACT] 0=No debris/props (max FPS) | 1=Props visible (immersive)
"sc_aggregate_bvh_threshold" "16"         // Lower BVH threshold (default: 128)
"sc_layer_batch_threshold" "16"           // Lower batch threshold (default: 128)
"sc_layer_batch_threshold_fullsort" "20" //default 80

// ================ ROPE PHYSICS ================
"rope_collide" "0"
"rope_subdiv" "0"
"rope_wind_dist" "0"
"rope_smooth_enlarge" "0"
"rope_smooth_maxalpha" "0"
"rope_smooth_maxalphawidth" "0"
"rope_smooth_minalpha" "0"
"rope_smooth_minwidth" "0"
"r_ropetranslucent" "0"
"r_drawropes" "0"

// ================ TERRAIN & FOLIAGE ================
"r_grass_quality" "0"
"r_grass_start_fade" "0"
"r_grass_end_fade" "0"

// ================ UI & HUD ================
"panorama_disable_box_shadow" "0"
"r_dashboard_render_quality" "0"
"closecaption" "false"
"citadel_hud_objective_health_enabled" "2"  // [ADJUST] Objective health display: 0=Off | 1=Shrines only | 2=T1/T2 Towers | 3=Barracks
"citadel_boss_glow_disabled" "1"
"citadel_damage_offscreen_indicator_disabled" "1" // Set 1 to disable
"citadel_portrait_world_renderer_off" "true" // Set true to disable hero hud
"panorama_use_new_occlusion_invalidation" "1"
"panorama_temp_comp_layer_min_dimension" "128"
"panorama_max_overlay_fps" "15"
"panorama_max_fps" "15"               // [ADJUST] UI FPS cap - 0=Unlimited (smooth UI) | 30/60=Standard | Higher = smoother HUD but more CPU
"panorama_async_compute_mipgen" "1"
"citadel_show_new_damage_feedback_numbers" "0" // Set 1 to enable
"hud_free_cursor" "0"                // Reduces UI input delay in minimap/spectator modes (not sure if this is true)
"citadel_camera_soft_collision" "0"
"citadel_camera_wobble_disable" "1"
"citadel_unit_status_use_new" "0"
"mm_idle_show_warning_at_s" "999"   // How many seconds to wait before showing the idle warning dialog
"citadel_hideout_ball_show_juggle_count" "1"
"citadel_hideout_ball_show_juggle_fx" "1"

// ================ NETWORK & PREDICTION ================
"cl_prediction_savedata_postentitypacketreceived" "1"
"r_frame_sync_enable" "0" //was 0
"cl_clock_buffer_ticks" "0"          // Testing set 1 to smooth over packet loss
"cl_async_usercmd_send" "true"
"cl_smooth" "0"                      // [ADJUST] 0=No smoothing (lower input lag) | 1=Smoothing enabled (may add delay)
"cl_smoothtime" "0.01"
"cl_smooth_draw_debug" "0"
"cl_interp_parallel" "1"
"cl_parallel_readpacketentities" "1"
"cl_parallel_readpacketentities_threshold" "2"
"net_async_clientconnect" "1"
"engine_max_ticks_to_simulate" "33"

// ================ AI OPTIMIZATIONS ================
"ai_strong_optimizations_no_checkstand" "1"
"ai_expression_optimization" "1"

// ================ AUDIO ================
- "audio_enable_vmix_mastering" "0"     // [FPS IMPACT] 0=Off (saves CPU, +FPS) | 1=On (audio mastering enabled)"
"dsp_volume" "0"                    // idk
- "snd_occlusion_bounces" "0"
- "snd_steamaudio_num_threads" "4"     // [ADJUST] Audio thread count - 1=Low CPU usage | Higher = better audio quality, more CPU By default, it might only use 1 thread. Increasing this allows the heavy sound math to spread out, preventing it from stalling the main game loop during loud teamfights
- "snd_mix_async" "1"
- "soundsystem_update_async" "1"

// ================ TEXTURE STREAMING ================
"r_texture_pool_size" "256"           // [ADJUST] VRAM usage in MB - Lower = less VRAM used, may cause texture pop-in | 512-1024 range
- "r_texture_stream_mip_bias" "4"         // [FPS IMPACT] Higher = blurrier textures, more FPS | 0=High quality | 2=Balanced | 4=Low quality
"r_texture_lod_scale" "4"               // [FPS IMPACT] 0=High quality (sharp) | 2=Medium | 4=Low quality (blurry, max FPS)
"r_fallback_texture_lod_scale" "4"
"r_texture_budget_update_period" "0.5" // Faster texture streaming adjustment 0.05
"r_texture_pool_reduce_rate" "512"

// ================ MEMORY BUDGET ================
- "r_texture_budget_dynamic" "1"          // Dynamic texture budget adjustment
- "r_texture_budget_threshold" "0.8"

// ================ SHADER & RENDERING ================
- "mat_async_shader_load" "1"
- "r_renderdoc_auto_shader_pdbs" "0"
"sc_hdr_enabled_override" "0"
- "r_texturefilteringquality" "0"
- "r_max_portal_render_targets" "2"   // Set how many amount to render portals
"mat_colcorrection_disableentities" "0" // Disable map color-correction entities
"r_gbuffer_disable_npr_lighting" "true"
"r_citadel_npr_outlines" "false"

// test
"cl_physics_highlight_active" "0" //Turns on the absbox for all active physics objects.<br>  0 : un-highlight.<br>
"phys_highlight_expensive_objects_strength" "0" //Default: 0.02<br>Highlight expensive physics objects strength, no need since expensive obj is disabled by default
"r_citadel_shadowdb" "256" //Default: 2048<br>
"r_citadel_shadow_quality" "0" //Default: 1<br>Shadow Quality
"r_effects_bloom" "false" //Default: true<br>
"r_citadel_glow_health_bars" "false" //default true
"r_citadel_enable_pano_world_blur" "false" //Default: true<br>Enable world-blur style
"r_depth_of_field" "false" //default true
"r_directional_lightmaps" "false" //default true
"r_citadel_distancefield_blur" "false" //Default: true<br>Enable/Disable distance field blur
"r_citadel_distancefield_shadows" "false" //Default: true<br>
"mat_max_lighting_complexity" "1" //default 8
"r_muzzleflashbrightness" "0.01" //default 0.4 idk if this does anything
"r_particle_cables_render" "true" //default true break lash ult do not disable
"r_postprocess_enable" "false" //default true
"lb_dynamic_shadow_resolution" "false" //default true
"cl_glow_brightness" "0" //default 1
"r_distancefield_enable" "false" //default true Graphics/Enable Distance Field rendering
"lb_enable_sunlight" "false" //Default: true<br>SceneSystem/LightBinner/Enable Sunlight
"citadel_trooper_friendly_glow_disabled" "true" //was false doesnt work btw
"cl_input_enable_raw_keyboard" "true" //Default: false<br>Enable raw keyboard input
"r_environment_map_roughness_range" "0.01" //Default: 0.2 0.3<br>Fade region for sampling environment maps on lightmapped nonmetals. Smoother values than the first param sample envmaps. Rougher values than the second sample only lightmap SH. r_environment_map_roughness_range 1 1 to always sample envmaps for comparison. BASICALLY TURN OFF REFLECTIONS ON MAP I THINK
"lb_cubemap_normalization_max" "1" //Default: 32<br>
"lb_cubemap_normalization_roughness_begin" "0.01" //Default: 0.1<br>
"thumper_use_plane_reflection" "false" //Default: true<br>
"cl_ragdoll_default_scale" "0" //default 1 doesnt matter since ragdoll disabled
"sc_instanced_mesh_mesh_shader" "false" //default true Toggles mesh shader rendering for instanced meshes

"r_citadel_disable_npr_lighting" "false" //True to make lighting ass, save you just a bit more fps

"r_fullscreen_gamma" "1.4" //recommended ppl to use this to make the game brighter, bigge number = darker (use again in console if game not bright, only work in fullscreen exclusive, try 2.1 then 1.4 to make it work i have 2 keys binded for this)

"mat_colorcorrection" "0"
"panorama_allow_transitions" "false" //default true turns off UI anim (shop,etc)
"panorama_disable_blur" "true" //disable ui blur
//"r_citadel_upscaling" "0" //Default: 4<br> doesnt do anything
"citadel_trooper_glow_disabled" "true"

"lb_mixed_shadows" "false"
"r_arealights" "false" //was true
"r_citadel_antialiasing" "0" //default 1
"r_character_decal_monitor_render_res" "64" //Default: 512<br>
"r_citadel_depthoffield_enable" "false"
"mat_viewportscale" "0.01" //was 1 this controls LOD on everything except trees and bushes (good) for some reason
"fx_drawmetalspark" "false" //Default: true<br>Draw metal spark effects.
"r_mapextents" "4500" //Default: 16384<br>Set the max dimension for the map.  This determines the far clipping plane, set to higher number if no like popping building
"r_citadel_npr_force_solid_outline" "true" //default false
"r_dopixelvisibility" "true" //default true enables or disables pixel visibility calculations, which can affect performance and visibility checks within the game.
"citadel_player_outline_enemies" "false" //turn off enemy outline DOES NOT BREAK BACKSTABBER OR PING THRU WALL
"sc_screen_size_lod_scale_override" "0.01" //was -1
"mat_colorcorrection" "0"
"r_farz" "6000" //default -1 far clipping plane, same as r_mapextents but this affect another thing that i dont understand yet, it gives fps though
"cl_disable_ragdolls" "true"
//"citadel_player_glow_disabled" "true" //default false, breaks backstabber
"citadel_trooper_outline_enabled" "false" //turn off trooper outline

"citadel_hideout_enable_testing_tools" "true" //default false doesnt work

"r_light_sensitivity_mode" "true"
"sv_pvs_max_distance" "2800" //default 4000, unrender things(boxes, creeps, objs,etc) behind walls or out of viewing distance, does not affect player model.
"sv_remove_ent_from_pvs" "1" //default 0 remove entities from potential view something, basically culling objs outside of view

"phys_cull_internal_mesh_contacts" "true" //default false
"citadel_use_pvs_for_players" "true" //default false, culls players when out of view
//"r_particle_max_texture_layers" "3" //was -1

"r_citadel_distancefield_down_sample" "6" //default 1

"ai_gather_conditions_async" "true" //default false
"enable_priority_boost" "1" 

"update_voices_low_priority" "true" //default false
"animgraph_enable_parallel_preupdate" "true" //default false Enables parallel processing for the pre-update phase of animation graphs, helping spread the load across more CPU cores
"anim_decode_forcewritealltransforms" "true" //Default: false<br>Force BatchAnimationDecode to write transformations for all bones
//"net_skip_redundant_change_callbacks" "true" //default false im p sure this keep pulling up report screen for some reason
"animgraph_footlock_enabled" "false"
"r_morphing_enabled" "false" 
"r_smooth_morph_normals" "0"

"animgraph_slowdownonslopes_enabled" "false"
"cl_simulate_dormant_entities" "false"
//"engine_allow_multiple_simulates_per_frame" "false" //default false not sure about this one so dont change it

"animgraph_enable_parallel_op_evaluation" "true" //default false
"animgraph_enable_parallel_preupdate" "true" //false
//"ai_lod_auto_enabled" "1" //default 0, idk about this
"ai_use_async_ragdoll_fixup" "true" //doesnt really need tbh since ragdoll is disabled
"cl_phys_networked_start_sleep" "true" //try on and off, this is probably what causing result screen to pop up when idling
"func_break_max_pieces" "1" //default 15

"r_light_flickering_enabled" "false"
"sc_clutter_density_none_size" "0.1" //Default 0.0035
//"r_draw_overlays" "false" //removes the walker line on the ground too, do not recommend
"snd_mixahead" "0.05" //set to 0.001 if have good CPU, 0.05 adds 50ms to audio mixing thus save CPU perf, should not be perceiveable by any human. 
//"cl_interp" "0.033" //i would not play with interps
"r_draw_particle_children_with_parents" "0"
 
"r_ssao_blur" "0"
"r_decals_max_on_deformables" "0"
"r_particle_cables_render_meshlets" "false" //default true
"lb_csm_cross_fade_override" "0"
"lb_csm_distance_fade_override" "0"
"sc_enable_discard" "true" //default true
"sc_clutter_density_full_size" "0.5"
"sc_clutter_density_none_size" "0.1"
"r_decals_overlap_threshold" "5"
"r_flashlightbrightness" "0"
"r_flashlightfar" "0"
"r_flashlightshadowatten" "0"
"sc_allow_dithered_lod" "0"
"sc_dithered_lod_transition_amt" "0"

"lb_dynamic_shadow_penumbra" "false" //default true
"phys_multithreading_enabled" "1" //default true, alr enabled no need to include ngl
//"engine_allow_multiple_ticks_per_frame" "0" //remove
"nav_pathfind_multithread" "1" //default false test 1 and 0, moves npc pathing to separate thread

"cl_predict_after_every_createmove" "0" // test 1 0 
"cl_predictioncopy_runs" "0" //put to 1 if character vibrates
"r_particle_batch_collections" "1"

"r_texture_stream_mip_bias" "3"
"r_texture_stream_resolution_bias" "0.01"
//"lb_enable_envmaps" "0" //REMOVE THIS DO NOT CHANGE THIS VALUE CUZ EVERYTHING IS GONNA BE BLACK
"lb_enable_baked_shadows" "0"
"r_world_wind_frequency_grass" "0"
"r_world_wind_frequency_trees" "0"
"mat_tonemap_bloom_scale" "0"
"mat_disable_dynamic_shader_compile" "1"
"lb_barnlight_shadow_use_precomputed_vis" "0"
"r_low_latency" "1" //Force enabling this for kaiz only, Default: 1<br>NVIDIA Low Latency/AMD Anti-Lag 2 (0 = off, 1 = on, 2 = NV-only, on + boost)
"mesh_calculate_curvature_smooth_pass_count" "0"
"panorama_transition_time_factor" "2" //faster transition for the stuff that doesnt use animation
"phys_dynamic_scaling" "false" //default true
"phys_expensive_shape_threshold" "100" //was 6
"sc_max_framebuffer_copies_per_layer" "0" //no idea what this does ngl
"r_strip_invisible_during_sceneobject_update" "1" //Default: false<br>
citadel_npc_force_animate_every_tick        "false"
