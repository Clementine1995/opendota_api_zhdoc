1. 获取某一玩家的数据
	接口：`GET /players/{account_id}`
	请求参数： account_id:integer,Required. (这个id指的是steam32位账号ID)
	响应数据：
	```
	{
		"tracked_until": "string",
		"solo_competitive_rank": "string",
		"competitive_rank": "string",
		"rank_tier": 0,
		"leaderboard_rank": 0,
		"mmr_estimate": {
			"estimate": 0,
			"stdDev": 0,
			"n": 0
		},
		"profile": {
			"account_id": 0,
			"personaname": "string",
			"name": "string",
			"cheese": 0,
			"steamid": "string",
			"avatar": "string",
			"avatarmedium": "string",
			"avatarfull": "string",
			"profileurl": "string",
			"last_login": "string",
			"loccountrycode": "string"
		}
	}
	```
2. 获取输赢场数
	接口：``
	请求参数：account_id:integer,Required(Steam32 account ID)
	查询参数：
		limit	
		integer
		Number of matches to limit to

		offset	
		integer
		Number of matches to offset start by

		win	
		integer
		Whether the player won

		patch	
		integer
		Patch ID

		game_mode	
		integer
		Game Mode ID

		lobby_type	
		integer
		Lobby type ID

		region	
		integer
		Region ID

		date	
		integer
		Days previous

		lane_role	
		integer
		Lane Role ID

		hero_id	
		integer
		Hero ID

		is_radiant	
		integer
		Whether the player was radiant

		included_account_id	
		integer
		Account IDs in the match (array)

		excluded_account_id	
		integer
		Account IDs not in the match (array)

		with_hero_id	
		integer
		Hero IDs on the player's team (array)

		against_hero_id	
		integer
		Hero IDs against the player's team (array)

		significant	
		integer
		Whether the match was significant for aggregation purposes

		having	
		integer
		The minimum number of games played, for filtering hero stats

		sort	
		string
		The field to return matches sorted by in descending order
	响应数据：
	```
	{
		"win": 0,
		"lose": 0
	}
	```
3. 最近比赛数据，具体是最近几场还不清楚
	接口：`GET /players/{account_id}/recentMatches`
	请求参数：account_id：integer,Required(Steam32 account ID)
	响应数据：数组
	```
	[
		{
			"match_id": 0,
			"player_slot": 0,
			"radiant_win": true,
			"duration": 0,
			"game_mode": 0,
			"lobby_type": 0,
			"hero_id": 0,
			"start_time": 0,
			"version": 0,
			"kills": 0,
			"deaths": 0,
			"assists": 0,
			"skill": 0,
			"lane": 0,
			"lane_role": 0,
			"is_roaming": true,
			"cluster": 0,
			"leaver_status": 0,
			"party_size": 0
		}
	]
	```
	注：[game_mode](https://github.com/odota/dotaconstants/blob/master/json/game_mode.json)数字对应模式可以在此查看
	[lobby_type](https://github.com/odota/dotaconstants/blob/master/json/lobby_type.json)

4. 玩家比赛数据，应该不会是全部的吧...
	接口：`GET /players/{account_id}/matches`
	请求参数：
		account_id	
		integer Required
		Steam32 account ID
	查询参数：
		limit	
		integer
		Number of matches to limit to

		offset	
		integer
		Number of matches to offset start by

		win	
		integer
		Whether the player won

		patch	
		integer
		Patch ID

		game_mode	
		integer
		Game Mode ID

		lobby_type	
		integer
		Lobby type ID

		region	
		integer
		Region ID

		date	
		integer
		Days previous

		lane_role	
		integer
		Lane Role ID

		hero_id	
		integer
		Hero ID

		is_radiant	
		integer
		Whether the player was radiant

		included_account_id	
		integer
		Account IDs in the match (array)

		excluded_account_id	
		integer
		Account IDs not in the match (array)

		with_hero_id	
		integer
		Hero IDs on the player's team (array)

		against_hero_id	
		integer
		Hero IDs against the player's team (array)

		significant	
		integer
		Whether the match was significant for aggregation purposes

		having	
		integer
		The minimum number of games played, for filtering hero stats

		sort	
		string
		The field to return matches sorted by in descending order

		project	
		string
		Fields to project (array)
	响应数据：array
	```
	[
		{
			"match_id": 0,
			"player_slot": 0,
			"radiant_win": true,
			"duration": 0,
			"game_mode": 0,
			"lobby_type": 0,
			"hero_id": 0,
			"start_time": 0,
			"version": 0,
			"kills": 0,
			"deaths": 0,
			"assists": 0,
			"skill": 0,
			"party_size": 0,
			"heroes": {
				"player_slot": {
					"account_id": 0,
					"hero_id": 0,
					"player_slot": 0
				}
			}
		}
	]
	```
5. 玩家使用的英雄
	接口：GET /players/{account_id}/heroes
	请求参数：
		account_id	
		integer Required
		Steam32 account ID
	查询参数：
		limit	
		integer
		Number of matches to limit to

		offset	
		integer
		Number of matches to offset start by

		win	
		integer
		Whether the player won

		patch	
		integer
		Patch ID

		game_mode	
		integer
		Game Mode ID

		lobby_type	
		integer
		Lobby type ID

		region	
		integer
		Region ID

		date	
		integer
		Days previous

		lane_role	
		integer
		Lane Role ID

		hero_id	
		integer
		Hero ID

		is_radiant	
		integer
		Whether the player was radiant

		included_account_id	
		integer
		Account IDs in the match (array)

		excluded_account_id	
		integer
		Account IDs not in the match (array)

		with_hero_id	
		integer
		Hero IDs on the player's team (array)

		against_hero_id	
		integer
		Hero IDs against the player's team (array)

		significant	
		integer
		Whether the match was significant for aggregation purposes

		having	
		integer
		The minimum number of games played, for filtering hero stats

		sort	
		string
		The field to return matches sorted by in descending order
	响应数据：array
	```
	[
		{
			"hero_id": 0,
			"last_played": 0,
			"games": 0,
			"win": 0,
			"with_games": 0,
			"with_win": 0,
			"against_games": 0,
			"against_win": 0
		}
	]
	```
6. 查看一起玩的人的数据
	接口：GET /players/{account_id}/peers
	请求参数：
		account_id	
		integer Required
		Steam32 account ID
	查询参数：
		limit	
		integer
		Number of matches to limit to

		offset	
		integer
		Number of matches to offset start by

		win	
		integer
		Whether the player won

		patch	
		integer
		Patch ID

		game_mode	
		integer
		Game Mode ID

		lobby_type	
		integer
		Lobby type ID

		region	
		integer
		Region ID

		date	
		integer
		Days previous

		lane_role	
		integer
		Lane Role ID

		hero_id	
		integer
		Hero ID

		is_radiant	
		integer
		Whether the player was radiant

		included_account_id	
		integer
		Account IDs in the match (array)

		excluded_account_id	
		integer
		Account IDs not in the match (array)

		with_hero_id	
		integer
		Hero IDs on the player's team (array)

		against_hero_id	
		integer
		Hero IDs against the player's team (array)

		significant	
		integer
		Whether the match was significant for aggregation purposes

		having	
		integer
		The minimum number of games played, for filtering hero stats

		sort	
		string
		The field to return matches sorted by in descending order
	响应数据：array
	```
	[
		{
			"account_id": 0,
			"last_played": 0,
			"win": 0,
			"games": 0,
			"with_win": 0,
			"with_games": 0,
			"against_win": 0,
			"against_games": 0,
			"with_gpm_sum": 0,
			"with_xpm_sum": 0,
			"personaname": "string",
			"last_login": "string",
			"avatar": "string",
			"avatarfull": "string"
		}
	]
	```
7. 与职业选手比赛记录？
	接口：GET /players/{account_id}/pros
	请求参数：
		account_id	
		integer Required
		Steam32 account ID
	查询参数：
		limit	
		integer
		Number of matches to limit to

		offset	
		integer
		Number of matches to offset start by

		win	
		integer
		Whether the player won

		patch	
		integer
		Patch ID

		game_mode	
		integer
		Game Mode ID

		lobby_type	
		integer
		Lobby type ID

		region	
		integer
		Region ID

		date	
		integer
		Days previous

		lane_role	
		integer
		Lane Role ID

		hero_id	
		integer
		Hero ID

		is_radiant	
		integer
		Whether the player was radiant

		included_account_id	
		integer
		Account IDs in the match (array)

		excluded_account_id	
		integer
		Account IDs not in the match (array)

		with_hero_id	
		integer
		Hero IDs on the player's team (array)

		against_hero_id	
		integer
		Hero IDs against the player's team (array)

		significant	
		integer
		Whether the match was significant for aggregation purposes

		having	
		integer
		The minimum number of games played, for filtering hero stats

		sort	
		string
		The field to return matches sorted by in descending order
	响应数据：
	```
	[
		{
			"account_id": 0,
			"name": "string",
			"country_code": "string",
			"fantasy_role": 0,
			"team_id": 0,
			"team_name": "string",
			"team_tag": "string",
			"is_locked": true,
			"is_pro": true,
			"locked_until": 0,
			"steamid": "string",
			"avatar": "string",
			"avatarmedium": "string",
			"avatarfull": "string",
			"profileurl": "string",
			"last_login": null,
			"full_history_time": null,
			"cheese": 0,
			"fh_unavailable": true,
			"loccountrycode": "string",
			"last_played": 0,
			"win": 0,
			"games": 0,
			"with_win": 0,
			"with_games": 0,
			"against_win": 0,
			"against_games": 0,
			"with_gpm_sum": 0,
			"with_xpm_sum": 0
		}
	]
	```
8. 统计总数
	接口：GET /players/{account_id}/totals
	请求参数：
		account_id	
		integer Required
		Steam32 account ID
	查询参数：
		limit	
		integer
		Number of matches to limit to

		offset	
		integer
		Number of matches to offset start by

		win	
		integer
		Whether the player won

		patch	
		integer
		Patch ID

		game_mode	
		integer
		Game Mode ID

		lobby_type	
		integer
		Lobby type ID

		region	
		integer
		Region ID

		date	
		integer
		Days previous

		lane_role	
		integer
		Lane Role ID

		hero_id	
		integer
		Hero ID

		is_radiant	
		integer
		Whether the player was radiant

		included_account_id	
		integer
		Account IDs in the match (array)

		excluded_account_id	
		integer
		Account IDs not in the match (array)

		with_hero_id	
		integer
		Hero IDs on the player's team (array)

		against_hero_id	
		integer
		Hero IDs against the player's team (array)

		significant	
		integer
		Whether the match was significant for aggregation purposes

		having	
		integer
		The minimum number of games played, for filtering hero stats

		sort	
		string
		The field to return matches sorted by in descending order
	响应数据：array
	```
	[
	{
	"field": "string",
	"n": 0,
	"sum": 0
	}
	]
	```
9. n局h局vh局计数？
	接口：GET /players/{account_id}/counts
	请求参数：
		account_id	
		integer Required
		Steam32 account ID
	查询参数：
	 	limit	
		integer
		Number of matches to limit to

		offset	
		integer
		Number of matches to offset start by

		win	
		integer
		Whether the player won

		patch	
		integer
		Patch ID

		game_mode	
		integer
		Game Mode ID

		lobby_type	
		integer
		Lobby type ID

		region	
		integer
		Region ID

		date	
		integer
		Days previous

		lane_role	
		integer
		Lane Role ID

		hero_id	
		integer
		Hero ID

		is_radiant	
		integer
		Whether the player was radiant

		included_account_id	
		integer
		Account IDs in the match (array)

		excluded_account_id	
		integer
		Account IDs not in the match (array)

		with_hero_id	
		integer
		Hero IDs on the player's team (array)

		against_hero_id	
		integer
		Hero IDs against the player's team (array)

		significant	
		integer
		Whether the match was significant for aggregation purposes

		having	
		integer
		The minimum number of games played, for filtering hero stats

		sort	
		string
		The field to return matches sorted by in descending order
	响应数据：obj
	```
	{
		"leaver_status": {},
		"game_mode": {},
		"lobby_type": {},
		"lane_role": {},
		"region": {},
		"patch": {}
	}
	```
10. 单排统计？
	接口：GET /players/{account_id}/histograms
	请求参数：
		account_id	
		integer Required
		Steam32 account ID

		field	
		string Required
		Field to aggregate on
	查询参数：
		limit	
		integer
		Number of matches to limit to

		offset	
		integer
		Number of matches to offset start by

		win	
		integer
		Whether the player won

		patch	
		integer
		Patch ID

		game_mode	
		integer
		Game Mode ID

		lobby_type	
		integer
		Lobby type ID

		region	
		integer
		Region ID

		date	
		integer
		Days previous

		lane_role	
		integer
		Lane Role ID

		hero_id	
		integer
		Hero ID

		is_radiant	
		integer
		Whether the player was radiant

		included_account_id	
		integer
		Account IDs in the match (array)

		excluded_account_id	
		integer
		Account IDs not in the match (array)

		with_hero_id	
		integer
		Hero IDs on the player's team (array)

		against_hero_id	
		integer
		Hero IDs against the player's team (array)

		significant	
		integer
		Whether the match was significant for aggregation purposes

		having	
		integer
		The minimum number of games played, for filtering hero stats

		sort	
		string
		The field to return matches sorted by in descending order
	响应数据：array
	```
	[
		{}
	]
	```
11. 比赛中插眼记录
	接口：GET /players/{account_id}/wardmap
	请求参数：
		account_id	
		integer Required
		Steam32 account ID
	查询参数：
		limit	
		integer
		Number of matches to limit to

		offset	
		integer
		Number of matches to offset start by

		win	
		integer
		Whether the player won

		patch	
		integer
		Patch ID

		game_mode	
		integer
		Game Mode ID

		lobby_type	
		integer
		Lobby type ID

		region	
		integer
		Region ID

		date	
		integer
		Days previous

		lane_role	
		integer
		Lane Role ID

		hero_id	
		integer
		Hero ID

		is_radiant	
		integer
		Whether the player was radiant

		included_account_id	
		integer
		Account IDs in the match (array)

		excluded_account_id	
		integer
		Account IDs not in the match (array)

		with_hero_id	
		integer
		Hero IDs on the player's team (array)

		against_hero_id	
		integer
		Hero IDs against the player's team (array)

		significant	
		integer
		Whether the match was significant for aggregation purposes

		having	
		integer
		The minimum number of games played, for filtering hero stats

		sort	
		string
		The field to return matches sorted by in descending order
	响应数据：
	```
	{
	"obs": { },
	"sen": { }
	}
	```
12. 发言记录？
	接口：GET /players/{account_id}/wordcloud
	请求参数：
		account_id	
		integer Required
		Steam32 account ID
	查询参数：
	 	limit	
		integer
		Number of matches to limit to

		offset	
		integer
		Number of matches to offset start by

		win	
		integer
		Whether the player won

		patch	
		integer
		Patch ID

		game_mode	
		integer
		Game Mode ID

		lobby_type	
		integer
		Lobby type ID

		region	
		integer
		Region ID

		date	
		integer
		Days previous

		lane_role	
		integer
		Lane Role ID

		hero_id	
		integer
		Hero ID

		is_radiant	
		integer
		Whether the player was radiant

		included_account_id	
		integer
		Account IDs in the match (array)

		excluded_account_id	
		integer
		Account IDs not in the match (array)

		with_hero_id	
		integer
		Hero IDs on the player's team (array)

		against_hero_id	
		integer
		Hero IDs against the player's team (array)

		significant	
		integer
		Whether the match was significant for aggregation purposes

		having	
		integer
		The minimum number of games played, for filtering hero stats

		sort	
		string
		The field to return matches sorted by in descending order
	响应数据：
	```
	{
		"my_word_counts": {},
		"all_word_counts": {}
	}
	```
13. 玩家排名记录
	接口：GET /players/{account_id}/ratings
	请求参数：
		account_id	
		integer Required
		Steam32 account ID
	查询参数：
	响应数据：array
	```
	[
		{
			"account_id": 0,
			"match_id": 0,
			"solo_competitive_rank": 0,
			"competitive_rank": 0,
			"time": null
		}
	]
	```
14. 玩家英雄排名
	接口：GET /players/{account_id}/pros
	请求参数：
		account_id	
		integer Required
		Steam32 account ID
	查询参数：
	响应数据：array
	```
	[
		{}
	]
	```
15. 刷新玩家匹配历史记录
	接口：POST /players/{account_id}/refresh
	请求参数：
		account_id	
		integer Required
		Steam32 account ID
	查询参数：
	响应数据：
	```
	{}
	```