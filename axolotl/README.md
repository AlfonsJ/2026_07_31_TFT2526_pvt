
cd $HOME

python -m venv axolotl_venv
source axolotl_venv/bin/activate

mkdir axolotl
cd axolotl

pip install torch torchvision
python -c "import torch; print(torch.cuda.is_available())"
python -c "import torch; print(torch.cuda._is_compiled())"

pip install meson-python Cython scipy
pip install --no-build-isolation axolotl[flash-attn,deepspeed]



