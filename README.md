# solana--finder
sudo apt-get update \
&& sudo apt-get install python3-venv git -y \
&& git clone https://github.com/c29r3/solana-snapshot-finder.git \
&& cd solana-snapshot-finder \
&& python3 -m venv venv \
&& source ./venv/bin/activate \
&& pip3 install -r requirements.txt
# в следующей строке ниже не забыть прописать свой путь с папке ledger/  Данная команда для скачивания в сети Тестнет
sudo python3 snapshot-finder.py --snapshot_path /root/solana/ledger/ -r https://api.testnet.solana.com --min_download_speed 95   
# если не работает то возможно надо доустановить библиотеку командой
sudo apt install python3-tqdm

pip install "git+https://github.com/tqdm/tqdm.git@devel#egg=tqdm"
