FROM fr3akyphantom/vapoursynth-av1an-rt

# refresh mirror lists
RUN paru -Sy --repo
ARG PARU_OPTS="--skipreview --noprovides --removemake --cleanafter --useask --combinedupgrade --batchinstall --nokeepsrc"
# reinstall x265 to release version
RUN paru -Rdd --noconfirm x265-git && paru -S --noconfirm --needed ${PARU_OPTS} x265
RUN paru -S --noconfirm --needed ${PARU_OPTS} vapoursynth-plugin-fft3dfilter-git
