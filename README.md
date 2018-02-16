# ec2_cluster

# Instructions
1. download the clusterMPIkey.pem and put it on the desktop
2. right click on desktop and click git bash here and type in the following line of code:
     ssh -i "clusterMPIkey.pem" ec2-user@ec2-34-204-45-96.compute-1.amazonaws.com
3. After you are connected, type cd mpitest
4. Type: mpiexec -np x -hostfile ~/nodefile prime_mpi.x (Change x after -np to number of processes you want to use. 1,2,4,8,etc)
5. This program calculates the number of prime integers between 1 and N as well as the time taken to calculate each.

As more processes are added, the calculation time for N = 262144 decreases with diminishing returns. By that, I mean after enough processes are added, the gains in performance become marginal and not worth the extra cost.
