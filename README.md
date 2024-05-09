# Xenia Config Settings for Games

Where do i obtain Game Patches from?
- You can obtain Game [Patches](https://github.com/xenia-canary/game-patches/releases/latest/download/game-patches.zip) from here or from this [link.](https://github.com/xenia-canary/game-patches)

Some games don't have a 60/Unlocked FPS Patch.
- Either wait for a patch or use [Lossless Scaling](https://store.steampowered.com/app/993090/Lossless_Scaling/) with this [config](https://github.com/joever2022/test/blob/main/LS%20Config.png) as an alternative for games that speedup with VSync. (costs 7 dollars tho.)

How do i use Mouse & Keyboard for Xenia?
- From this [link](https://github.com/marinesciencedude/xenia-canary-mousehook) but only a few games have mouse support.
You can make your own Keybinds with this method in the bindings.ini file:<br>
[Media ID - Game Name]<br>
Keybind = Controller Bind<br>
[eg. W = LS-Up]


How do i play games on Xenia with Online Support?
- You can get it from this [link.](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)

Why do my XBLA games play on Trial mode?</br>
Why do my DLCs not work?
- Change license_mask = 1 in the xenia config

---

## Games List

| Game | Settings | Plugins | Recommended TUs | Netplay Compatibility
|---|---|---|---|---|
| Aurora Dashboard | allow_game_relative_writes = true</br>protect_zero = false</br>gpu_allow_invalid_fetch_constants = true | | Base | No
| Battlefield: Bad Company | d3d12_readback_resolve = true | | Base | No
| Blue Dragon | d3d12_clear_memory_page_state = true | | Base | No
| Borderlands 2 | vsync = false<br>framerate_limit = 0<br>use_dedicated_xma_thread = false<br>use_new_decoder = true | | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Call of Duty: Advanced Warfare | d3d12_readback_resolve = true</br>protect_zero = false | | TU 17 | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Call of Duty: Modern Warfare | cl = "r_vsync 0" | | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Call of Duty: Modern Warfare 2 | cl = "+r_vsync 0 +com_maxfps 0" | | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Call of Duty: Modern Warfare 3 | cl = "r_vsync 0"<br><br>Netplay Config:<br>allow_plugins = true | [System Link](https://github.com/joever2022/test/raw/main/MW3SystemLink.rar) | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Counter-Strike: Global Offensive | break_on_unimplemented_instructions = false</br>clear_memory_page_state = true | [Mousehook](https://github.com/marinesciencedude/xenia-canary-mousehook) | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Crackdown | use_new_decoder = true<br>d3d12_readback_resolve = true<br>controller_hotkeys = true | | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Dead or Alive 4 | clear_memory_page_state = true<br>gpu_allow_invalid_fetch_constants = true | | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Dead Rising | clear_memory_page_state = true<br> render_target_path_d3d12 = "rov"<br>use_dedicated_xma_thread = false<br>use_new_decoder = true | | Base | No
| DRIVER: San Francisco | vsync = false<br>framerate_limit = 0 | | Base | No
| Fable 2 | d3d12_readback_resolve = true<br>d3d12_clear_memory_page_state = true | | Base | No
| Fight Night Champion | create a 00000002 in it's content folder<br>d3d12_readback_resolve = true<br>mount_cache = true<br>mount_scratch = true<br>vsync = false<br>framerate_limit = 0<br>clear_memory_page_state = true<br>apu_max_queued_frames = 3 | | Base | No
| Forza Horizon | mount_cache = true<br>d3d12_readback_resolve = true<br>gpu_allow_invalid_fetch_constants = true | | Base | No
| Forza Horizon 2 | mount_cache = true<br>d3d12_readback_resolve = true<br>gpu_allow_invalid_fetch_constants = true | | Base | No
| Forza Motorsport 4 | [2022 Build](https://raw.githubusercontent.com/joever2022/test/main/xenia_canary.exe)<br>mount_cache = true<br>query_occlusion_fake_sample_count = -1<br>d3d12_readback_resolve = true<br>gpu_allow_invalid_fetch_constants = true | [Project Forza Plus](https://www.reddit.com/r/ProjectForzaPlus/comments/11a4qus/welcome_to_the_project_forza_plus_sub/) | Base | No
| Ghost Recon Advanced Warfighter 2 | vsync = false<br>framerate_limit = 0 | | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Grand Theft Auto IV | gpu = vulkan | | TU 8 | No
| Grand Theft Auto: Episodes from Liberty City | gpu = vulkan | | Base | No
| Grand Theft Auto V | d3d12_readback_resolve = true<br>query_occlusion_fake_sample_count = -1<br>query_occlusion_fake_sample_count = 1000 | | TU 26 | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Gundam Operation Troy | render_target_path_d3d12 = "rov" | [English Patch](https://github.com/Eight-Mansions/MSGOT/releases) | TU 1 | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Kane & Lynch 2: Dog Days | d3d12_readback_resolve = true | | TU 1 | No
| Left 4 Dead | d3d12_readback_resolve = true<br>cl = "-dvd -novid" | [Mousehook](https://github.com/marinesciencedude/xenia-canary-mousehook) | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Left 4 Dead 2 | [Unlock FPS](https://raw.githubusercontent.com/joever2022/test/main/L4D2%20Unlock%20FPS.rar)<br>d3d12_readback_resolve = true<br>cl = "mat_motion_blur_percent_of_screen_max 0" | [Mousehook](https://github.com/marinesciencedude/xenia-canary-mousehook) | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Mass Effect 1 | internal_display_resolution: 2-5<br>use_new_decoder = true | | Base | No
| Metal Gear Solid HD Collection | gpu_allow_invalid_fetch_constants = true<br>cl = "MGS2.xex"<br>cl = "MGS3.xex" | | Base | No
| Metal Gear Solid V | d3d12_readback_resolve = true<br>no_discard_stencil_in_transfer_pipelines = true<br>native_stencil_value_output_d3d12_intel = true | | Base | No
| Midnight Club: Los Angeles | d3d12_readback_resolve = true<br>query_occlusion_fake_sample_count = -1 | | Base | No
| Minecraft | vsync = false<br>framerate_limit = 0<br>mount_cache = true | [Mousehook](https://github.com/marinesciencedude/xenia-canary-mousehook) | Base | No
| Need for Speed: Carbon | use_dedicated_xma_thread = false<br>use_new_decoder = true<br>vsync = false<br>framerate_limit = 0 | | Base | No
| Need for Speed: Most Wanted 2005 | use_dedicated_xma_thread = false<br>use_new_decoder = true | | Base | No
| Need for Speed: Most Wanted 2012 | d3d12_readback_memexport = true | | Base | No
| Need for Speed: Pro Street | use_dedicated_xma_thread = false<br>use_new_decoder = true | | Base | No
| Operation Darkness | use_fuzzy_alpha_epsilon = false | | Base | No
| Perfect Dark | clear_memory_page_state = true | [Mousehook](https://github.com/marinesciencedude/xenia-canary-mousehook) | Base | [Yes]
| PAYDAY 2 | vsync = false<br>framerate_limit = 0 | | TU 1 | No
| Portal 2 | d3d12_readback_resolve = true | [Mousehook](https://github.com/marinesciencedude/xenia-canary-mousehook) | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Rainbow Six: Vegas 2 | vsync = false<br>framerate_limit = 0<br>clear_memory_page_state = true | | Base | No
| Red Dead Redemption | vsync = false<br>framerate_limit = 0<br>query_occlusion_fake_sample_count = -1<br>[Unlock Social Club Content](https://github.com/xenia-project/game-compatibility/issues/108#issuecomment-1357339081) | [Reality Redemption](https://gtaforums.com/topic/989469-rel-wip-rdr-reality-redemption-overhaul-project/) | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Saints Row | apu_max_queued_frames = 3<br>protect_zero = false | | TU 1 | not yet.
| Saints Row 2 | apu_max_queued_frames = 3<br>protect_zero = false<br>query_occlusion_fake_sample_count = -1 | | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Saints Row the Third | d3d12_readback_resolve = true<br>render_target_path_d3d12 = "rov"<br>protect_zero = false<br>vsync = false<br>framerate_limit = 0 | | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Saints Row IV | d3d12_readback_resolve = true<br>render_target_path_d3d12 = "rov"<br>protect_zero = false<br>vsync = false<br>framerate_limit = 0 | | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Silent Hill Downpour | render_target_path_d3d12 = "rov" | | Base | No
| Skate 3 | vsync = false<br>framerate_limit = 0 | | Base | No
| Sonic Free Riders | gpu_allow_invalid_fetch_constants = true | [No Kinect](https://gamebanana.com/mods/456720) | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| Sonic Unleashed | [Setup Guide](https://gamebanana.com/tuts/17062) | | TU 2 | No
| TEKKEN 6 | Netplay Config:<br><br>vsync = false<br>framerate_limit = 120 | | TU 3 | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)
| The Orange Box | d3d12_readback_resolve = true<br>cl = "-dvd -game hl2"<br>cl = "-dvd -game episodic"<br>cl = "-dvd -game ep2"<br>cl = "-dvd -game tf"<br>cl = "-dvd -game portal" | [Mousehook](https://github.com/marinesciencedude/xenia-canary-mousehook) | Base | [Yes](https://github.com/AdrianCassar/xenia-canary/tree/netplay_canary_experimental_readme?tab=readme-ov-file#netplay-fork)