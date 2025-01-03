cmake_minimum_required(VERSION 3.5)

# Project Name
project(psp_postal)

# Include directories
include_directories(
    source
    source/RSPiX
    source/RSPiX/Inc
    source/RSPiX/Src
    source/RSPiX/Src/BLUE
    source/RSPiX/Src/BLUE/unix
    source/RSPiX/Src/CYAN
    source/RSPiX/Src/CYAN/Unix
    source/RSPiX/Src/ORANGE
    source/RSPiX/Src/ORANGE/CDT
    source/RSPiX/Src/ORANGE/GameLib
    source/RSPiX/Src/ORANGE/File
    source/RSPiX/Src/ORANGE/Multigrid
    source/RSPiX/Src/GREEN/Image
    source/WishPiX
    source/WishPiX/Spry
    ${PSPSDK}/include
    ${PSPSDK}/include/SDL
)

# Source files
set(SOURCE_FILES
    source/AnimThing.cpp
    source/ball.cpp
    source/barrel.cpp
    source/bouy.cpp
    source/character.cpp
    source/chunk.cpp
    source/deathWad.cpp
    source/demon.cpp
    source/dispenser.cpp
    source/doofus.cpp
    source/dude.cpp
    source/explode.cpp
    source/fire.cpp
    source/fireball.cpp
    source/firebomb.cpp
    source/flag.cpp
    source/flagbase.cpp
    source/grenade.cpp
    source/heatseeker.cpp
    source/hood.cpp
    source/item3d.cpp
    source/mine.cpp
    source/napalm.cpp
    source/navnet.cpp
    source/ostrich.cpp
    source/person.cpp
    source/PowerUp.cpp
    source/pylon.cpp
    source/rocket.cpp
    source/sentry.cpp
    source/SndRelay.cpp
    source/SoundThing.cpp
    source/thing.cpp
    source/Thing3d.cpp
    source/trigger.cpp
    source/warp.cpp
    source/weapon.cpp
    source/alphablitforpostal.cpp
    source/Anim3D.cpp
    source/BufQ.cpp
    source/bulletFest.cpp
    source/camera.cpp
    source/crawler.cpp
    source/cutscene.cpp
    source/encrypt.cpp
    source/gameedit.cpp
    source/GameSettings.cpp
    source/grip.cpp
    source/IdBank.cpp
    source/InputSettings.cpp
    source/InputSettingsDlg.cpp
    source/keys.cpp
    source/Log.cpp
    source/logtab.cpp
    source/MemFileFest.cpp
    source/MenuSettings.cpp
    source/MenuTrans.cpp
    source/net.cpp
    source/NetBrowse.cpp
    source/NetClient.cpp
    source/NetDlg.cpp
    source/netmsgr.cpp
    source/NetServer.cpp
    source/organ.cpp
    source/Personatorium.cpp
    source/ProtoBSDIP.cpp
    source/realm.cpp
    source/scene.cpp
    source/score.cpp
    source/settings.cpp
    source/smash.cpp
    source/socket.cpp
    source/StockPile.cpp
    source/TexEdit.cpp
    source/toolbar.cpp
    source/TriggerRegions.cpp
    source/update.cpp
    source/yatime.cpp
    source/aivars.cpp
    source/band.cpp
    source/credits.cpp
    source/game.cpp
    source/input.cpp
    source/localize.cpp
    source/main.cpp
    source/menus.cpp
    source/play.cpp
    source/SampleMaster.cpp
    source/title.cpp
    source/RSPiX/Src/BLUE/unix/Bdebug.cpp
    source/RSPiX/Src/BLUE/unix/Bjoy.cpp
    source/RSPiX/Src/BLUE/unix/Bkey.cpp
    source/RSPiX/Src/BLUE/unix/Bmain.cpp
    source/RSPiX/Src/BLUE/unix/Bmouse.cpp
    source/RSPiX/Src/BLUE/unix/Btime.cpp
    source/RSPiX/Src/BLUE/unix/Bdisp.cpp
    source/RSPiX/Src/BLUE/unix/Bsound.cpp
    source/RSPiX/Src/GREEN/Hot/hot.cpp
    source/RSPiX/Src/GREEN/Image/Image.cpp
    source/RSPiX/Src/GREEN/Image/Imagecon.cpp
    source/RSPiX/Src/GREEN/Image/ImageFile.cpp
    source/RSPiX/Src/GREEN/InputEvent/InputEvent.cpp
    source/RSPiX/Src/GREEN/Mix/mix.cpp
    source/RSPiX/Src/GREEN/Mix/MixBuf.cpp
    source/RSPiX/Src/GREEN/Image/pal.cpp
    source/RSPiX/Src/GREEN/Image/PalFile.cpp
    source/RSPiX/Src/GREEN/Sample/sample.cpp
    source/RSPiX/Src/GREEN/Snd/snd.cpp
    source/RSPiX/Src/GREEN/SndFx/SndFx.cpp
    source/RSPiX/Src/GREEN/Task/task.cpp
    source/RSPiX/Src/GREEN/3D/pipeline.cpp
    source/RSPiX/Src/GREEN/3D/render.cpp
    source/RSPiX/Src/GREEN/3D/types3d.cpp
    source/RSPiX/Src/GREEN/3D/zbuffer.cpp
    source/RSPiX/Src/GREEN/BLiT/alphablit.cpp
    source/RSPiX/Src/GREEN/BLiT/BLIT.cpp
    source/RSPiX/Src/GREEN/BLiT/BLITINIT.cpp
    source/RSPiX/Src/GREEN/BLiT/BLiTT.cpp
    source/RSPiX/Src/GREEN/BLiT/CFNT.cpp
    source/RSPiX/Src/GREEN/BLiT/Fspr1.cpp
    source/RSPiX/Src/GREEN/BLiT/FSPR8.cpp
    source/RSPiX/Src/GREEN/BLiT/line.cpp
    source/RSPiX/Src/GREEN/BLiT/mono.cpp
    source/RSPiX/Src/GREEN/BLiT/Rotate96.cpp
    source/RSPiX/Src/GREEN/BLiT/RPrint.cpp
    source/RSPiX/Src/GREEN/BLiT/ScaleFlat.cpp
    source/RSPiX/Src/ORANGE/GameLib/ANIMSPRT.cpp
    source/RSPiX/Src/ORANGE/Attribute/attribute.cpp
    source/RSPiX/Src/ORANGE/GUI/btn.cpp
    source/RSPiX/Src/ORANGE/Channel/channel.cpp
    source/RSPiX/Src/ORANGE/color/colormatch.cpp
    source/RSPiX/Src/ORANGE/DirtRect/DirtRect.cpp
    source/RSPiX/Src/ORANGE/color/dithermatch.cpp
    source/RSPiX/Src/ORANGE/GUI/dlg.cpp
    source/RSPiX/Src/ORANGE/GUI/edit.cpp
    source/RSPiX/Src/ORANGE/File/file.cpp
    source/RSPiX/Src/ORANGE/QuickMath/FixedPoint.cpp
    source/RSPiX/Src/ORANGE/GUI/guiItem.cpp
    source/RSPiX/Src/ORANGE/IFF/iff.cpp
    source/RSPiX/Src/ORANGE/ImageTools/lasso.cpp
    source/RSPiX/Src/ORANGE/Laymage/laymage.cpp
    source/RSPiX/Src/ORANGE/GUI/ListBox.cpp
    source/RSPiX/Src/ORANGE/GUI/ListContents.cpp
    source/RSPiX/Src/ORANGE/Meter/meter.cpp
    source/RSPiX/Src/ORANGE/MsgBox/MsgBox.cpp
    source/RSPiX/Src/ORANGE/GUI/MultiBtn.cpp
    source/RSPiX/Src/ORANGE/MultiGrid/MultiGrid.cpp
    source/RSPiX/Src/ORANGE/MultiGrid/MultiGridIndirect.cpp
    source/RSPiX/Src/ORANGE/GUI/ProcessGui.cpp
    source/RSPiX/Src/ORANGE/Debug/profile.cpp
    source/RSPiX/Src/ORANGE/GUI/PushBtn.cpp
    source/RSPiX/Src/ORANGE/QuickMath/QuickMath.cpp
    source/RSPiX/Src/ORANGE/GameLib/Region.cpp
    source/RSPiX/Src/ORANGE/RString/rstring.cpp
    source/RSPiX/Src/ORANGE/GUI/scrollbar.cpp
    source/RSPiX/Src/ORANGE/GameLib/SHAPES.cpp
    source/RSPiX/Src/ORANGE/Parse/SimpleBatch.cpp
    source/RSPiX/Src/ORANGE/GameLib/SPRITE.cpp
    source/RSPiX/Src/ORANGE/str/str.cpp
    source/RSPiX/Src/ORANGE/GUI/txt.cpp
    source/RSPiX/Src/CYAN/Unix/uDialog.cpp
    source/RSPiX/Src/CYAN/Unix/uColors.cpp
    source/RSPiX/Src/CYAN/Unix/uPath.cpp
    source/WishPiX/Menu/menu.cpp
    source/WishPiX/Prefs/prefline.cpp
    source/WishPiX/Prefs/prefs.cpp
    source/WishPiX/ResourceManager/resmgr.cpp
    source/WishPiX/Spry/spry.cpp
)


# Add executable
add_executable(${PROJECT_NAME} ${SOURCE_FILES})

# SDL2 Integration
include(FindPkgConfig)
pkg_search_module(SDL2 REQUIRED sdl2)
target_include_directories(${PROJECT_NAME} PRIVATE ${SDL2_INCLUDE_DIRS})
target_link_libraries(${PROJECT_NAME} PRIVATE
    ${SDL2_LIBRARIES}
    pspgu
    pspdisplay
    pspdebug
    pspge
    pspaudio
    pspvfpu
    pspnet
    pspnet_apctl
    pspnet_inet
    pspnet_resolver
)

# Compiler options
set(COMMON_COMPILE_FLAGS
    -G0
    -Wall
    -Wno-narrowing
    -O2
    -fno-exceptions
    -fno-rtti
    -std=c++11
    -DPSP
    -DPLATFORM_UNIX
    -DDEBUG
    -DLOCALE=US
    -DTARGET=POSTAL_2015
    -w
)

target_compile_options(${PROJECT_NAME} PRIVATE ${COMMON_COMPILE_FLAGS})

# Post-build steps to create an EBOOT.PBP file (for PSP only)
if(PSP)
    create_pbp_file(
        TARGET ${PROJECT_NAME}
        ICON_PATH "../source/ICON0.PNG"
        BACKGROUND_PATH "../source/PIC1.PNG"
        PREVIEW_PATH NULL
        TITLE POSTAL PSP
        VERSION 01.00
    )
endif()

# Custom clean target
add_custom_target(clean-all
    COMMAND ${CMAKE_COMMAND} -E remove_directory ${CMAKE_BINARY_DIR}
)
