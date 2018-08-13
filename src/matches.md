获取某一场比赛的详细信息
接口：`GET /matches/{match_id}`
请求参数：match_id:integer,Required
响应信息（返回信息很多）：
```
{
  "match_id": 0,
  "barracks_status_dire": 0,
  "barracks_status_radiant": 0,
  "chat": [
    {
      "time": 0,
      "unit": "string",
      "key": "string",
      "slot": 0,
      "player_slot": 0
    }
  ],
  "cluster": 0,
  "cosmetics": {},
  "dire_score": 0,
  "draft_timings": [
    {
      "order": 0,
      "pick": true,
      "active_team": 0,
      "hero_id": 0,
      "player_slot": 0,
      "extra_time": 0,
      "total_time_taken": 0
    }
  ],
  "duration": 0,
  "engine": 0,
  "first_blood_time": 0,
  "game_mode": 0,
  "human_players": 0,
  "leagueid": 0,
  "lobby_type": 0,
  "match_seq_num": 0,
  "negative_votes": 0,
  "objectives": {},
  "picks_bans": {},
  "positive_votes": 0,
  "radiant_gold_adv": {},
  "radiant_score": 0,
  "radiant_win": true,
  "radiant_xp_adv": {},
  "start_time": 0,
  "teamfights": {},
  "tower_status_dire": 0,
  "tower_status_radiant": 0,
  "version": 0,
  "replay_salt": 0,
  "series_id": 0,
  "series_type": 0,
  "radiant_team": {},
  "dire_team": {},
  "league": {},
  "skill": 0,
  "players": [
    {
      "match_id": 0,
      "player_slot": 0,
      "ability_upgrades_arr": [
        0
      ],
      "ability_uses": {},
      "ability_targets": {},
      "damage_targets": {},
      "account_id": 0,
      "actions": {},
      "additional_units": {},
      "assists": 0,
      "backpack_0": 0,
      "backpack_1": 0,
      "backpack_2": 0,
      "buyback_log": [
        {
          "time": 0,
          "slot": 0,
          "player_slot": 0
        }
      ],
      "camps_stacked": 0,
      "creeps_stacked": 0,
      "damage": {},
      "damage_inflictor": {},
      "damage_inflictor_received": {},
      "damage_taken": {},
      "deaths": 0,
      "denies": 0,
      "dn_t": [
        0
      ],
      "gold": 0,
      "gold_per_min": 0,
      "gold_reasons": {},
      "gold_spent": 0,
      "gold_t": [
        0
      ],
      "hero_damage": 0,
      "hero_healing": 0,
      "hero_hits": {},
      "hero_id": 0,
      "item_0": 0,
      "item_1": 0,
      "item_2": 0,
      "item_3": 0,
      "item_4": 0,
      "item_5": 0,
      "item_uses": {},
      "kill_streaks": {},
      "killed": {},
      "killed_by": {},
      "kills": 0,
      "kills_log": [
        {
          "time": 0,
          "key": "string"
        }
      ],
      "lane_pos": {},
      "last_hits": 0,
      "leaver_status": 0,
      "level": 0,
      "lh_t": [
        0
      ],
      "life_state": {},
      "max_hero_hit": {},
      "multi_kills": {},
      "obs": {},
      "obs_left_log": [
        {}
      ],
      "obs_log": [
        {}
      ],
      "obs_placed": 0,
      "party_id": 0,
      "permanent_buffs": [
        {}
      ],
      "pings": 0,
      "purchase": {},
      "purchase_log": [
        {
          "time": 0,
          "key": "string"
        }
      ],
      "rune_pickups": 0,
      "runes": {
        "property1": 0,
        "property2": 0
      },
      "runes_log": [
        {
          "time": 0,
          "key": 0
        }
      ],
      "sen": {},
      "sen_left_log": [
        {}
      ],
      "sen_log": [
        {}
      ],
      "sen_placed": 0,
      "stuns": 0,
      "times": [
        0
      ],
      "tower_damage": 0,
      "xp_per_min": 0,
      "xp_reasons": {},
      "xp_t": [
        0
      ],
      "personaname": "string",
      "name": "string",
      "last_login": null,
      "radiant_win": true,
      "start_time": 0,
      "duration": 0,
      "cluster": 0,
      "lobby_type": 0,
      "game_mode": 0,
      "patch": 0,
      "region": 0,
      "isRadiant": true,
      "win": 0,
      "lose": 0,
      "total_gold": 0,
      "total_xp": 0,
      "kills_per_min": 0,
      "kda": 0,
      "abandons": 0,
      "neutral_kills": 0,
      "tower_kills": 0,
      "courier_kills": 0,
      "lane_kills": 0,
      "hero_kills": 0,
      "observer_kills": 0,
      "sentry_kills": 0,
      "roshan_kills": 0,
      "necronomicon_kills": 0,
      "ancient_kills": 0,
      "buyback_count": 0,
      "observer_uses": 0,
      "sentry_uses": 0,
      "lane_efficiency": 0,
      "lane_efficiency_pct": 0,
      "lane": 0,
      "lane_role": 0,
      "is_roaming": true,
      "purchase_time": {},
      "first_purchase_time": {},
      "item_win": {},
      "item_usage": {},
      "purchase_tpscroll": {},
      "actions_per_min": 0,
      "life_state_dead": 0,
      "rank_tier": 0,
      "cosmetics": [
        0
      ],
      "benchmarks": {}
    }
  ],
  "patch": 0,
  "region": 0,
  "all_word_counts": {},
  "my_word_counts": {},
  "throw": 0,
  "loss": 0,
  "replay_url": "string"
}
```