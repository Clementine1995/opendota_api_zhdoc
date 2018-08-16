1. 获取战队数据
	接口：GET /teams
	请求参数：
	查询参数：
	响应数据：array
	```
	[
		{
			"team_id": 0,
			"rating": 0,
			"wins": 0,
			"losses": 0,
			"last_match_time": 0,
			"name": "string",
			"tag": "string"
		}
	]
	```
2. 获取某一战队的更详细数据
	接口：GET /teams/{team_id}
	请求参数：
		team_id：integer,Required(Team ID)
	查询参数：
	响应数据：object
	```
	{
		"team_id": 0,
		"rating": 0,
		"wins": 0,
		"losses": 0,
		"last_match_time": 0,
		"name": "string",
		"tag": "string"
	}
	```
3. 获取一个战队的比赛数据
	接口：GET /teams/{team_id}/matches
	请求参数：
		team_id：integer,Required(Team ID)
	查询参数：
	响应数据：object
	```
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
	```
4. 获取一个战队的队员信息
	接口：GET /teams/{team_id}/players
	请求参数：
		team_id：integer,Required(Team ID)
	查询参数：
	响应数据：object
	```
	{
		"account_id": "string",
		"name": "string",
		"games_played": 0,
		"wins": 0,
		"is_current_team_member": true
	}
	```
5. 获取一个战队英雄使用情况
	接口：GET /teams/{team_id}/heroes
	请求参数：
		team_id：integer,Required(Team ID)
	查询参数：
	响应数据：object
	```
	{
		"hero_id": 0,
		"name": "string",
		"games_played": 0,
		"wins": 0
	}
	```