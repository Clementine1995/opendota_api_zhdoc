1. 获取英雄数据
	接口：GET /heroes
	请求参数：
	查询参数：
	响应数据：array
	```
	[
		{
			"id": 0,
			"name": "string",
			"localized_name": "string",
			"primary_attr": "string",
			"attack_type": "string",
			"roles": [
				"string"
			]
		}
	]
	```
2. 获取最近某一英雄比赛数据
	接口：GET /heroes/{hero_id}/matches
	请求参数：
	hero_id:integer,Required(Hero ID)
	查询参数：
	响应数据：array
	```
	[
		{
			"match_id": 0,
			"duration": 0,
			"start_time": 0,
			"radiant_team_id": 0,
			"radiant_name": "string",
			"dire_team_id": 0,
			"dire_name": "string",
			"leagueid": 0,
			"league_name": "string",
			"series_id": 0,
			"series_type": 0,
			"radiant_score": 0,
			"dire_score": 0,
			"radiant_win": true,
			"radiant": true
		}
	]
	```
3. 获取某一个英雄对阵其他英雄的数据
	接口：GET /heroes/{hero_id}/matchups
	请求参数：
	  hero_id:integer, Required(Hero ID)
	查询参数：
	响应数据：array
	```
	[
		{
			"id": 0,
			"name": "string",
			"localized_name": "string",
			"primary_attr": "string",
			"attack_type": "string",
			"roles": [
				"string"
			]
		}
	]
	```
4. 获取某一个英雄在不同比赛持续时间的表现情况
	接口：GET /heroes/{hero_id}/durations
	请求参数：
		hero_id:integer, Required(Hero ID)
	查询参数：
	响应数据：array
	```
	[
		{
			"duration_bin": "string",
			"games_played": 0,
			"wins": 0
		}
	]
	```
5. 获取玩过某英雄的玩家
	接口：GET /heroes/{hero_id}/players
	请求参数：
		hero_id:integer, Required(Hero ID)
	查询参数：
	响应数据：array
	```
	[
		[
			{
				"account_id": 0,
				"steamid": "string",
				"avatar": "string",
				"avatarmedium": "string",
				"avatarfull": "string",
				"profileurl": "string",
				"personaname": "string",
				"last_login": null,
				"full_history_time": null,
				"cheese": 0,
				"fh_unavailable": true,
				"loccountrycode": "string",
				"name": "string",
				"country_code": "string",
				"fantasy_role": 0,
				"team_id": 0,
				"team_name": "string",
				"team_tag": "string",
				"is_locked": true,
				"is_pro": true,
				"locked_until": 0
			}
		]
	]
	```