replace
N = int(os.environ.get('BOARD_SIZE', 9))
in go.py

python3 rl_loop/local_integration_test1.py

BLACK="gnugo --mode gtp"
WHITE="python3 gtp1.py --load_file=./aminigo/000000-bootstrap/models/000000-bootstrap --num_readouts=10 --flagfile=rl_loop/local_flags1"
TWOGTP="gogui-twogtp -black \"$BLACK\" -white \"$WHITE\" -games 10 \
  -size 9 -alternate -sgffile gnugo"
gogui -size 9 -program "$TWOGTP" -computer-both -auto
for random play

and
WHITE="python3 gtp1.py --load_file=./aminigo/0000xx-xxxxxxxxx/models/0000xx-xxxxxxxxx --num_readouts=10 --flagfile=rl_loop/local_flags1"
for trained play
