@Name:AdditionalAudioEffect
@Default:undefined
@Type:String
@Description: additional sound effect on projectile impact. Value format "<type>:<name>".
							type values: "enum" - building in-game enum value
							"id" - unsigned integer (if you know value)
							"name" - audio event name 
							"none" - none additional sound for this type name doesn't matter
							may be set per ammo, mode and weapon. Mode have priority than ammo than weapon

@Name:AdditionalImpactVFX
@Default:undefined
@Type:String
@Description:additional VFX played on impact. Mode have priority, than ammo, than weapon. Long played effects not supposed. 
             Effect game object will be cleaned and returned to pool on next fire sequence of this weapon
						 
@Name:AdditionalImpactVFXScaleX
@Default:0
@Type:float
@Description:scale of additional VFX, used only when AdditionalImpactVFX is not empty. Note, not all VFXs supports scaling.

@Name:AdditionalImpactVFXScaleY
@Default:0
@Type:float
@Description:scale of additional VFX, used only when AdditionalImpactVFX is not empty. Note, not all VFXs supports scaling.

@Name:AdditionalImpactVFXScaleZ
@Default:0
@Type:float
@Description:scale of additional VFX, used only when AdditionalImpactVFX is not empty. Note, not all VFXs supports scaling.

@Name:AirMechDamageModifier
@Default:1
@Type:float
@Description: weapon damage modifier if target is in air mech mode. 
							workd only with CustomUnits mod

@Name:AlternateAPDamageCalc
@Default:false
@Type:boolean
@Description:not used

@Name:AlternateDamageCalc
@Default:false
@Type:boolean
@Description:if true alternate damage calc formula will be implemented 
             DamagePerShot = (damage from weaponDef + (damage from ammo) + (damage from mode)*(damage multiplayer from ammo)*(damage multiplayer from mode)*(damage with effects)/(damage from weaponDef)

@Name:AlternateHeatDamageCalc
@Default:false
@Type:boolean
@Description: same as  AlternateDamageCalc but for heat

@Name:AlternateInstabilityCalc
@Default:false
@Type:boolean
@Description:same as  AlternateDamageCalc but for instability 

@Name:AlwaysIndirectVisuals
@Default:NotSet
@Type:boolean
@Description:if true missiles will always plays indirect visuals, even if direct line of sight exists

@Name:AmmoCategory
@Default:NotSet
@Type:string
@Description:AmmoCategory can now be overridden by weapon mode. If setted as "NotSet" weapon wouldn't use any ammo. 
		         If weapon has mode with "NotSet" ammo category you will not see warnings in mechlab for this weapon, 
						 even if you are not supply this weapon with ammo.
						 
@Name:AMSDamage
@Default:0
@Type:float
@Description:damage AMS inflicting to missiles subtracting from missile health on success hit. Used while AMS working. If missile health become 0 missile counted as intercepted. Additive for ammo, mode, weapon.
Can be accessed via statistic value CAC_AMSDamage and modifier CAC_AMSDamage_Mod

@Name:AMSHitChance
@Default:0
@Type:float
@Description:if this weapon is AMS, this value is AMS efficiency, 
						 if this weapon is missile launcher this value shows how difficult to intercept missile with AMS. Negative value - is harder, 
						 positive is easer. 
						 See aditional notes in Main CustomAmmoCategories readme (AMS mechanic notes)

@Name:AMSImmune
@Default:NotSet
@Type:boolean
@Description:if true, weapon missiles is immune to AMS and none AMS will try to intercept them. Can be set for mode ammo and weapon

@Name:AMSShootsEveryAttack
@Default:NotSet
@Type:boolean
@Description:if true AMS will not share AMS.ShootsWhenFired between all missile attacks this round. 
             Every missile attack will cause AMS.ShootsWhenFired shoots. 
						 if not true AMS will shoot AMS.ShootsWhenFired per round

@Name:AOECapable
@Default:NotSet
@Type:boolean
@Description:if true weapon will included in AOE damage calculations. If true set in weapon definition 
              all shoots will have AoE effect (even for energy weapon). If true, it can't be overridden by ammo.

@Name:AOEDamage
@Default:0
@Type:float
@Description:Area of effect range. If AOECapable in weapon is set to true this value will be used. If AOECapable is true in weapon definition, AOEDamage can't be overridden in ammo.

@Name:AoEDmgFalloffType
@Default:NotSet
@Type:enum. Possible values: NotSet, Quadratic, Cubic, SquareRoot, Log10, LogE, Exp, Linear
@Description: function to distance ratio to damage in AoE damage processing. Effective NotSet counted as Linear

@Name:AOEEffectsFalloff
@Default:NotSet
@Type:boolean
@Description:if true and weapon inflicts AoE damage, random roll will be permitted before onHit effect apply. 
             Example: aoe range = 100m, projectile hits ground in 30m from combatant - onHits effects will be applied with 0.7 chance ((100 - 30) / 100)

@Name:AOEHeatDamage
@Default:0
@Type:float
@Description:AoE heat. Same rules as for AOERange. If AOECapable is true in weapon definition, AOEHeatDamage can't be overridden in ammo.

@Name:AOEInstability
@Default:0
@Type:float
@Description:not documented yet

@Name:AOERange
@Default:0
@Type:float
@Description:not documented yet

@Name:APArmorShardsMod
@Default:0
@Type:float
@Description:not documented yet

@Name:APCriticalChanceMultiplier
@Default:не число
@Type:float
@Description:not documented yet

@Name:APMaxArmorThickness
@Default:0
@Type:float
@Description:not documented yet

@Name:ArmorDamageModifier
@Default:0
@Type:float
@Description:not documented yet

@Name:BallisticDamagePerPallet
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:baseModeId
@Default:undefined
@Type:String
@Description:not documented yet

@Name:blockWeaponsInInstalledLocation
@Default:false
@Type:boolean
@Description:not documented yet

@Name:blockWeaponsInMechLocations
@Default:undefined
@Type:List`1
@Description:not documented yet

@Name:BuildingsDamageModifier
@Default:1
@Type:float
@Description:not documented yet

@Name:CanBeBlocked
@Default:true
@Type:boolean
@Description:not documented yet

@Name:CantHitUnaffecedByPathing
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:ClearMineFieldRadius
@Default:0
@Type:integer
@Description:not documented yet

@Name:ColorChangeRule
@Default:None
@Type:enum. Possible values: None, Linear, Random, RandomOnce, t0, t1, t2, t3, t4, t5, t6, t7, t8, t9, t10, t11, t12, t13, t14, t15, t16, t17, t18, t19, t20, t21, t22, t23, t24, t25, t26, t27, t28, t29, t30, t31
@Description:not documented yet

@Name:ColorSpeedChange
@Default:0
@Type:float
@Description:not documented yet

@Name:ColorsTable
@Default:undefined
@Type:List`1
@Description:not documented yet

@Name:Cooldown
@Default:0
@Type:integer
@Description:not documented yet

@Name:DamageFalloffEndDistance
@Default:0
@Type:float
@Description:not documented yet

@Name:DamageFalloffStartDistance
@Default:0
@Type:float
@Description:not documented yet

@Name:DamageNotDivided
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:DamageOnJamming
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:deferredEffect
@Default:undefined
@Type:DeferredEffectDef
@Description:not documented yet

@Name:DestroyOnJamming
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:DirectFireModifier
@Default:0
@Type:float
@Description:not documented yet
Can be accessed via statistic value CAC_DirectFireModifier and modifier CAC_DirectFireModifier_Mod

@Name:DisableClustering
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:DistantVariance
@Default:0
@Type:float
@Description:not documented yet

@Name:DistantVarianceReversed
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:EjectWeapon
@Default:false
@Type:boolean
@Description:not documented yet

@Name:evasivePipsMods
@Default:undefined
@Type:EvasivePipsMods
@Description:not documented yet

@Name:FireAnimationSpeedMod
@Default:1
@Type:float
@Description:not documented yet

@Name:FireDelayMultiplier
@Default:10
@Type:float
@Description:not documented yet

@Name:FireDurationWithoutForest
@Default:0
@Type:integer
@Description:not documented yet

@Name:FireOnSuccessHit
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:FireTerrainCellRadius
@Default:0
@Type:integer
@Description:not documented yet

@Name:FireTerrainChance
@Default:0
@Type:float
@Description:not documented yet

@Name:FireTerrainStrength
@Default:0
@Type:integer
@Description:not documented yet

@Name:FlatJammingChance
@Default:0
@Type:float
@Description:not documented yet

@Name:ForbiddenRange
@Default:0
@Type:float
@Description:not documented yet

@Name:GunneryJammingBase
@Default:0
@Type:float
@Description:not documented yet

@Name:GunneryJammingMult
@Default:0
@Type:float
@Description:not documented yet

@Name:HasShells
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:HitGenerator
@Default:NotSet
@Type:enum. Possible values: NotSet, Individual, Cluster, AOE, Streak
@Description:not documented yet

@Name:Id
@Default:undefined
@Type:String
@Description:not documented yet

@Name:IFFDef
@Default:undefined
@Type:String
@Description:not documented yet

@Name:ImprovedBallistic
@Default:true
@Type:boolean
@Description:not documented yet

@Name:InternalAmmo
@Default:undefined
@Type:Dictionary`2
@Description:not documented yet

@Name:IsAAMS
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:IsAMS
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:ISDamageModifier
@Default:0
@Type:float
@Description:not documented yet

@Name:isDamageVariation
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:isHaveInternalAmmo
@Default:false
@Type:boolean
@Description:not documented yet

@Name:isHeatVariation
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:isStabilityVariation
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:MaxMissRadius
@Default:0
@Type:float
@Description:not documented yet
Can be accessed via statistic value CAC_MaxMissRadius and modifier CAC_MaxMissRadius_Mod

@Name:MaxShellsDistance
@Default:0
@Type:float
@Description:not documented yet

@Name:MechDamageModifier
@Default:1
@Type:float
@Description:not documented yet

@Name:MinMissRadius
@Default:0
@Type:float
@Description:not documented yet
Can be accessed via statistic value CAC_MinMissRadius and modifier CAC_MinMissRadius_Mod

@Name:MinShellsDistance
@Default:0
@Type:float
@Description:not documented yet

@Name:MissileFiringIntervalMultiplier
@Default:1
@Type:float
@Description:not documented yet

@Name:MissileHealth
@Default:1
@Type:float
@Description:not documented yet
Can be accessed via statistic value CAC_MissileHealth and modifier CAC_MissileHealth_Mod

@Name:MissileVolleyIntervalMultiplier
@Default:1
@Type:float
@Description:not documented yet

@Name:MissileVolleySize
@Default:0
@Type:integer
@Description:not documented yet

@Name:Modes
@Default:undefined
@Type:Dictionary`2
@Description:not documented yet

@Name:NotUseInMelee
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:PrefireAnimationSpeedMod
@Default:1
@Type:float
@Description:not documented yet

@Name:preFireSFX
@Default:undefined
@Type:String
@Description:not documented yet

@Name:ProjectileScale
@Default:undefined
@Type:CustomVector
@Description:not documented yet

@Name:ProjectileSpeedMultiplier
@Default:1
@Type:float
@Description:not documented yet

@Name:QuadDamageModifier
@Default:1
@Type:float
@Description:not documented yet

@Name:RangedDmgFalloffType
@Default:NotSet
@Type:enum. Possible values: NotSet, Quadratic, Cubic, SquareRoot, Log10, LogE, Exp, Linear
@Description:not documented yet

@Name:SelfDocumentationName
@Default:undefined
@Type:String
@Description:not documented yet

@Name:ShellsRadius
@Default:0
@Type:float
@Description:not documented yet

@Name:ShotsPerAmmo
@Default:1
@Type:float
@Description:not documented yet

@Name:SpreadRange
@Default:0
@Type:float
@Description:not documented yet
Can be accessed via statistic value CAC_SpreadRange and modifier CAC_SpreadRange_Mod

@Name:StatusEffectsPerHit
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:Streak
@Default:false
@Type:boolean
@Description:not documented yet

@Name:TagsAccuracyModifiers
@Default:undefined
@Type:Dictionary`2
@Description:not documented yet

@Name:TargetMechLegsOnly
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:TrooperSquadDamageModifier
@Default:1
@Type:float
@Description:not documented yet

@Name:TurretDamageModifier
@Default:1
@Type:float
@Description:not documented yet

@Name:Unguided
@Default:NotSet
@Type:boolean
@Description:not documented yet

@Name:VehicleDamageModifier
@Default:1
@Type:float
@Description:not documented yet

@Name:VTOLDamageModifier
@Default:1
@Type:float
@Description:not documented yet

