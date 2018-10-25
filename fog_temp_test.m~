

clear all;
clc;

% Input data

L_k = 1900;     % Processing density [unit cycles/byte]

D_k = 10*10^6; % input data size [unit byte] 

f_k = 600*10^6; % CPU rate at end-user [unit cycles/second]

f_i_k = 5*10^9; % CPU rate at fog node [unit cycles/second]


C_ul = 20*10^6; % uplink bandwidth [unit Hz]

eta = 3.5; % Spectral efficiency [unit b/s/Hz];

% End of input data 

% if the entire data is processed at end-user side
t_k_local = L_k*D_k/f_k; % Time for locally processing at end-user [unit second]
disp('====Single user/task case====')

disp(['Case 1: if the entire data is processed at end-user side  ', sprintf('%7.4f',t_k_local) ' second'])


% if the total data is offloaded to the fog node 
r_k = C_ul*eta; %Transmission rate [unit b/s]

t_k_i_trans = D_k*8/r_k %Transmission time to fog [unit s], (byte->bit conversion) 

t_k_i_local = L_k*D_k/f_i_k; % Time for locally processing at primary fog node [unit second]


t_k_i_local+t_k_i_trans;
disp('Case 2: if the entire data is offloaded to the primary fog node')
disp(['and entire data is processed at fog node side  ', sprintf('%7.4f',t_k_i_local+t_k_i_trans) ' second'])


disp('====Two users (or tasks) case====')
t_k_i_trans = D_k*8*2/r_k %Transmission time to fog [unit s], (byte->bit conversion) 

t_k_i_local = L_k*D_k/f_i_k; % Time for locally processing at primary fog node [unit second]


t_k_i_local+t_k_i_trans;
disp('Case 2: if the entire data is offloaded to the primary fog node')
disp(['and entire data is processed at fog node side  ', sprintf('%7.4f',t_k_i_local+t_k_i_trans) ' second'])








