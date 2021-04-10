#
# Start stopped instances specified by tag
#
    - local_action:
          module: ec2
          region: us-east-2
          instance_tags:
            Name: Windows1
          state: running
#
# Restart instances specified by tag
#
    - local_action:
          module: ec2
          region: us-east-2
          instance_tags:
            Name: Windows1
          state: restarted
#
#Terminate instances specified by tag
#

- name: Terminate instances that were previously launched
  ec2:
        region: us-east-2
        state: absent
        instance_ids: i-064afdb355cfbe354

 - name: Terminate instances that were previously launched
   ec2:
        region: us-east-2
        state: absent
        instance_ids: '{{ i-03d1fd738516c4b73} {i-014fdfd8ea54176bc}}' (Syntax Error)