# Challenge
# Terapkan Load Balancing untuk wayshub-frontend menggunakan 2 server, Menggunakan Methon Round Robin dan Least Connections

## Topologi Load Balancing
<img width="563" height="293" alt="LoadBalancing" src="https://github.com/user-attachments/assets/6957bb0e-49f6-4636-beb3-6dddf3f9d4bc" />


Keterangan: 
- Server1(dumbwaysfauzi) berperan sebagai server Nginx dan server backend1
  - IP Address server backend1(dumbwaysfauzi): 192.168.1.208/24
- Server2(BackendServers) berperan sebagai server backend2
  - IP address server backend2(BackendServers): 192.168.1.21/24

## Membuat Server Baru
- Membuat server dengan nama 'BackendServer'
<img width="624" height="363" alt="Membuatserver" src="https://github.com/user-attachments/assets/5468a59a-cb06-4fa0-be94-9f81f3e010c5" />

- BackendServers dengan IP: 192.168.1.21 
<img width="624" height="211" alt="ipbackendserver" src="https://github.com/user-attachments/assets/512b0c96-5807-4961-91bd-b7da09392352" />

- Tes ping kedua server apakah terhubung satu sama lain, serta tes ke google juga untuk BackendServers
<img width="601" height="246" alt="tesping1" src="https://github.com/user-attachments/assets/6f4c540c-4e56-4f44-adfc-bf222d263c5f" />

<img width="610" height="405" alt="tesping2" src="https://github.com/user-attachments/assets/6378de8a-3b7c-49fd-b6d7-b2be3a9b33d4" />

- 

