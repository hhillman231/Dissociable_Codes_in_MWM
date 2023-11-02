## Dissociable Codes in Motor Working Memory
This repo contains data has been preprocessed from its original form for clarity and usability and size. It contains trial-level information. If you would like to request raw data, please contact Hanna Hillman, at hanna.hillman@yale.edu. It also contains R Markdown scripts that reproduce the figures and statistics referenced in Dissociable Codes in Motor Working Memory (Hillman, et. al., 2023)


## Experiment 1
column_name: variable
- id: anonymized participant id

- block: block # (4 blocks, each 26 trials)
- trial: trial # for given block 
    - missing trial indicates a timeout when switching hands
- setsize: how many movements were made during encoding 
    - 1 or 4 
- start_hand: which hand started on the robot
    -  0 = left hand
    -  1 = right hand
- switch_hands: were they asked to switch hands between encoding and recall?
    - 0 = no-switch trial
    - 1 = switch trial
- recall_move: which movement pt was asked to recall (first encoded target = 1)
    - always 1 if setsize == 1
    - 1, 2, 3, or 4 if setsize == 4
- targ1, targ2, targ3, targ4: numerical end point ID for target(s) moved to during encoding 
    - if setsize == 1  targ1-4 will all be the same #
- recall_targ = numerical id for the target asked to recall (same ID as targ1-4)
- targ_x: x-coordinate for the recall_targ
    - origin is at home position centered in front of pt
- targ_y: y-coordinate for the recall_targ
- pt_x: end point x-coordinate for the participants recall of target
- pt_y: end point y-coordinate for the participants recall of target
- dist_err: euclidean distance (cm) between participant recall end point and encoded target end point
- move_time: amount of time pt moved to final recall position (ms)

## Experiment 2
column_name: variable
- id: anonymized participant id

- block: block # (3 blocks, each 32 trials)
- trial: trial # for given block 
    - missing trial indicates a timeout when switching hands
- type: delay or additional irrelevant movements
    - 0 = delay
    - 1 = irrelevant movements
- size: 1 or 3 irrelevant movements/short or long delay
    - 0 = 1 irrelevant movement or short delay
    - 1 = 3 irrelevant movements or long delay
- start_hand: which hand started on the robot
    -  0 = left hand
    -  1 = right hand
- switch_hands: were they asked to switch hands between encoding and recall?
    - 0 = no-switch trial
    - 1 = switch trial
- targ: numerical ID for target to be remembered
- targ_x: x-coordinate for the recall_targ
    - origin is at home position centered in front of pt
- targ_y: y-coordinate for the recall_targ
- xtra_targ1, xtra_targ2, xtra_targ3: numerical ID for extra targets (movements) that are to be ignored
    - if 42 there was no movement 
- xtra_targ1_x, xtra_targ2_x, xtra_targ3_x: x-coordinate for extra target (movements) that are to be ignored
- xtra_targ1_y, xtra_targ2_y, xtra_targ3_y: y-coordinate for extra target (movements) that are to be ignored
- pt_x: end point x-coordinate for the participants recall of target
- pt_y: end point y-coordinate for the participants recall of target
- dist_err: euclidean distance (cm) between participant recall end point and encoded target end point
- move_time: amount of time pt moved to final recall position (ms)

## Experiment 3
column_name: variable
- id: anonymized participant id
- block: block # (3 blocks, each 32 trials)
- trial: trial # for given block 
    - missing trial indicates a timeout when switching hands
- start_hand: which hand started on the robot
    -  0 = left hand
    -  1 = right hand
- switch_hands: were they asked to switch hands between encoding and recall?
    - 0 = no-switch trial
    - 1 = switch trial
- targ_x: x-coordinate for the recall_targ
    - origin is at home position centered in front of pt
- targ_y: y-coordinate for the recall_targ
- pt_x: end point x-coordinate for the participants recall of target
- pt_y: end point y-coordinate for the participants recall of target
- vsp_setsize: number of dots in the visuospatial stimulus
    - 0 = 1 dot
    - 1 = 3 dots
- vsp1_color, vsp2_color, vsp3_color: color of the visuospatial dots 
- vsp1_x, vsp2_x, vsp3_x: x-coordinates for the dots
- vsp1_y, vsp2_y, vsp3_y: y-coordinates for the dots

- recall_vsp: numerical id for the vsp dot asked to recall  (will match vsp1/2/or3)
- recall_vsp_x: x-coordinate for vsp dot participants are prompted to recall
- recall_vsp_y: y-coordinate for vsp dot participants are prompted to recall
- recall_vsp_color: color for the  vsp dot participants are prompted to recall

- pt_vsp_x: x-coordinate for the participants recall of the vsp dot
- pt_vsp_y: y-coordinate for the participants recall of the vsp dot
- vsp_move_time: amount of time participant took using the joystick to recall vsp stimulus 
