Bootstrap: docker
From: centos

%runscript
exec echo "Centos7 image for use with GridFTP"

%files
# src dest

%environment
# export XYZ=/blah/

%labels
AUTHOR alvin@nscc.sg

%post
#echo "The post section is where you can install, and configure your container."
#
rpm -hUv http://www.globus.org/ftppub/gt6/installers/repo/globus-toolkit-repo-latest.noarch.rpm
yum -y update && yum -y install epel-release
yum -y install yum-plugin-priorities # globus installer needs this
yum -y install globus-data-management-client globus-data-management-server
/etc/init.d/globus-gridftp-sshftp reconfigure
