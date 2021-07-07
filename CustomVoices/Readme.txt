this mod allow using external sound banks as voice packs for pilots
it creates custom resource for ModTek - VoicePackDef
{
  "name":"tex_voice", - name of voice pack. This name should be set in PilotDef.Voice field
  "vobank":"tex_voice_soundbank", - sound bank for voice pack. 
  "baseVoice":"m_vizzini01", - fallback in-game voice 
  "stop_event": "tex_stop_voice", - event name from sound bank which is fired if voice audio should be stopped. Should be exported by sound bank.
  "gender":"Male", - gender of voice pack. Used for auto-generated pilots. 
  "dark_phrases":{ - phrases vocalized by pilots have two moods "dark" and "light". By default pilot have "light" mood. 
                     On critical hit, overheat, fall, friendly death mood changed to "dark".
    "target_alpha": ["tex_hit_target"],  - map for linked game events to audio events. 
                                         Record like "ammo_gone_ac10": ["tex_missed_target"] means on ac10 depletion tex_missed_target sound event will be fired.
  },
  "light_phrases":{
   ...........................................
  }
}

used VO events 

MechMove_Move
MechMove_Sprint

--AmmoCategory.OutOfAmmoAudioVOEvent
    AmmoDepleted_AC10
    AmmoDepleted_AC2
    AmmoDepleted_AC20
    AmmoDepleted_AC5
    AmmoDepleted_Gauss
    AmmoDepleted_LRM
    AmmoDepleted_MG
    AmmoDepleted_Multiple
    AmmoDepleted_SRM
    AmmoDepleted_Flamer

TakeDamage_WeaponLost_All
TakeDamage_WeaponLost
TakeDamage_Critical    
AttackTarget_MultiTarget
AttackTarget_Structure
AttackTarget_Alpha
AttackTarget_Rear
AttackTarget_Fire
EnemySpotted_Flank

--technically there is code playing these events but on "strafe" ability implement
AirstrikeLaunched_Ally
AirstrikeLaunched_Enemy

--played on mech mortar sequence
ArtilleryLaunched_Ally
ArtilleryLaunched_Enemy

AttackTarget_Kill_Vehicle
AttackTarget_Kill_Turret
AttackTarget_Kill

Chatter_Generic
Chatter_Arid
Chatter_Frozen
Chatter_Jungle
Chatter_Martian
Chatter_Urban
Chatter_Verdant
    
Mech_Chosen
Mech_Done
Commander_Retreat
AttackTarget_Critical
AttackTarget_Miss
TakeDamage_PilotKilled
TakeDamage_AllyDestroyed
TakeDamage_Critical
TakeDamage_Internal
TakeDamage_Heavy
TakeDamage_Light
MechMove_Jump
Mech_Instability_Fall
TakeDamage_Limping
Mech_Stand_Restart
Mech_Overheat_Shutdown
Mech_Overheat_Warning
Pilot_Death
Pilot_TakeDamage
Pilot_Inspired
Chatter_PVP
Mech_Reserve
AttackTarget_DFA
AttackTarget_Melee
EnemySpotted_Flank
EnemySpotted_Blip
EnemySpotted_Blip_Additional
Mech_Power_Restart
Pilot_Ejecting
SensorLock_Ally
SensorLock_Enemy