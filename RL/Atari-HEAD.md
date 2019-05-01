Atari-HEAD: Atari Human Eye-Tracking and Demonstration Dataset
CMU, Google 등에서 Atari Game에 대한 휴먼 데이터 셋을 만듬. 

이전 데이터 셋들과 비교했을 때 차이점은 단순하게 사람이 게임을 플레이한 데이터 셋만 있는 것이 아니라 화면에서 어떤 부분을 보았는지 실시간으로 eye tracker를 이용하여 모았음.
16개의 아타리 게임의 데이터 셋을 모았음.

데이터 셋 주소 : https://zenodo.org/record/2587121
데이터 셋에 저장된 내용 : (frame, human keystroke acion, human decision time to take that action, gaze position, reward from environment)

아이트래커 장비 -> EyeLink 1000 (1000Hz)

데이터를 쌓은 플레이어의 수준은 아마추어 수준

사용한 방법 -> Attention-Guided Imitation Learning


데이터 수집: Semi-frame-by-frame game mode  

In the default ALE setting, the game runs continuously at 60Hz, a speed that is very challenging even for expert human players. The most unique feature of our experimental setup is that the game pauses at every frame until an action is taken by the human player.

 However, human can hold down an action key and the game will run continuously at 20Hz. The reasons for such setup are as follows: Maximizing human performance to obtain near-optimal policies Frame-by-frame gameplay enable the players to play the games at their comfortable speeds, allowing very precise control in difficult states that require longer time to make decisions. It makes the games more relaxing and minimizes fatigue which could results in blinking or poor decisions. Resolving state-action mismatch Closed-loop human visuomotor reaction time ∆t is around 250-300 milliseconds.

 Therefore in the continuous gameplay setting, st and at that are simultaneously recorded at time step t could be mismatched. Action at is intended for a state st−∆t that was 250-300ms ago. 

For fast-pace games this could be problematic. Frame-by-frame gameplay ensures that st and at are matched at every timestep. Highlighting critical states Human decision time was recorded for every frame. Hypothetically, the states that could lead to a large reward or penalty, and/or the states that require sophisticated decisions, will take longer for the player to make a decision. Fig. 2 shows an example. 




데이터 셋에 저장된 게임 목록


성능 평가 → 모든 게임에서 기존의 성능 대비 높다.
