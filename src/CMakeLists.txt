# The Flutter tooling requires that developers have CMake 3.10 or later
# installed. You should not increase this version, as doing so will cause
# the plugin to fail to compile for some customers of the plugin.
cmake_minimum_required(VERSION 3.10)

project(discord_gamesdk_library VERSION 0.0.1 LANGUAGES C)

add_library(discord_gamesdk SHARED
  "discord_gamesdk.c"
)

set_target_properties(discord_gamesdk PROPERTIES
  PUBLIC_HEADER discord_gamesdk.h
  OUTPUT_NAME "discord_gamesdk"
)

target_compile_definitions(discord_gamesdk PUBLIC DART_SHARED_LIB)
