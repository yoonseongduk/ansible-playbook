- name: this is a play at the top level of a file
  hosts: all
  tasks:
    - name: cmd 01
      tags: echo
      shell: echo "hi...$(hostname) ${USER}" > /tmp/ansible_${USER}.out
    - name: cmd 02
      tags: cat
      shell: cat /tmp/ansible_${USER}.out
    - name: cmd 03
      tags: root-auth
      shell: cat /etc/shadow
      become: yes
      become_user: root
