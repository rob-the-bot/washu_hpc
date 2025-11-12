FROM fr3akyphantom/vapoursynth-av1an-runtime:amd64-v3

# refresh mirror lists
RUN paru -Sy --repo
ARG PARU_OPTS="--skipreview --noprovides --removemake --cleanafter --useask --combinedupgrade --batchinstall --nokeepsrc"
# reinstall x265 to release version
RUN paru -Rdd --noconfirm x265-git && paru -S --noconfirm --needed ${PARU_OPTS} x265 python-setuptools
RUN paru -S --noconfirm --needed ${PARU_OPTS} vapoursynth-plugin-havsfunc

# apply fix on the keyword arguments
# https://github.com/HomeOfVapourSynthEvolution/havsfunc/issues/96#issuecomment-3271109915
RUN sudo sed -i '1212s/_lambda/lambda_/;1213s/_global/global_/' '/usr/lib/python3.13/site-packages/havsfunc.py'

# NOTE: eventually we need to move to the `QTGMC` in `vs-jetpack`
# since the `QTGMC` in `havsfunc` is deprecated
# https://github.com/HomeOfVapourSynthEvolution/havsfunc/issues/99
