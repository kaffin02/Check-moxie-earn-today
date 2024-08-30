query GetMoxieEarningsToday($timeframe: FarcasterMoxieEarningStatsTimeframe!, $blockchain: EveryBlockchain!, $_eq: FarcasterMoxieEarningStatsEntityType, $_eq1: String) {
  FarcasterMoxieEarningStats(
    input: {timeframe: $timeframe, blockchain: $blockchain, filter: {entityType: {_eq: $_eq}, entityId: {_eq: $_eq1}}}
  ) {
    FarcasterMoxieEarningStat {
      allEarningsAmount
      castEarningsAmount
      entityId
      entityType
      frameDevEarningsAmount
      otherEarningsAmount
      timeframe
    }
  }
}
