// ============================================
// Polymarket API Types
// ============================================

export interface PolymarketMarket {
  id: string;
  question: string;
  slug: string;
  description?: string;
  outcomes: string[];
  outcomePrices?: string;
  volume: number;
  volumeNum?: number;
  liquidity: number;
  liquidityNum?: number;
  startDate?: string;
  endDate?: string;
  endDateIso?: string;
  active: boolean;
  closed: boolean;
  archived: boolean;
  new: boolean;
  featured: boolean;
  restricted: boolean;
  groupItemTitle?: string;
  groupItemThreshold?: number;
  enableOrderBook: boolean;
  conditionId?: string;
  questionId?: string;
  clobTokenIds?: string[];
  yesPrice?: number;
  noPrice?: number;
  eventSlug?: string;
  eventTitle?: string;
  impliedProbability?: number;
  potentialRoi?: number;
  roiIfYes?: number;
  roiIfNo?: number;
}

export interface PolymarketEvent {
  id: string;
  slug: string;
  title: string;
  description?: string;
  startDate?: string;
  endDate?: string;
  active: boolean;
  closed: boolean;
  archived: boolean;
  new: boolean;
  featured: boolean;
  restricted: boolean;
  markets: PolymarketMarket[];
  tags?: string[];
  volume?: number;
  liquidity?: number;
  commentCount?: number;
}

export interface OrderBookEntry {
  price: string;
  size: string;
}

export interface OrderBook {
  market: string;
  asset_id: string;
  bids: OrderBookEntry[];
  asks: OrderBookEntry[];
  hash: string;
  timestamp: string;
}

export interface PriceInfo {
  tokenId: string;
  price: number;
  side: "BUY" | "SELL";
  timestamp: string;
}

export interface TrumpBetOpportunity {
  market: PolymarketMarket;
  category: TrumpBetCategory;
  keywords: string[];
  yesPrice: number;
  noPrice: number;
  roiIfYes: number;
  roiIfNo: number;
  isContrarian: boolean;
  contrarianSide: "YES" | "NO" | null;
  contrarianRoi: number;
  liquidityScore: "high" | "medium" | "low";
  daysUntilClose?: number;
  isExpiringSoon: boolean;
  riskLevel: "low" | "medium" | "high";
  riskFactors: string[];
}

export type TrumpBetCategory =
  | "speech"
  | "policy"
  | "election"
  | "legal"
  | "media"
  | "personnel"
  | "foreign"
  | "economic"
  | "other";

export interface MarketSearchOptions {
  searchTerms?: string[];
  tags?: string[];
  active?: boolean;
  closed?: boolean;
  minVolume?: number;
  maxOdds?: number;
  minRoi?: number;
  limit?: number;
  offset?: number;
}

export interface TrumpBetFilters {
  categories?: TrumpBetCategory[];
  minRoi?: number;
  maxYesPrice?: number;
  minLiquidity?: number;
  onlyContrarian?: boolean;
  expiringWithinDays?: number;
  riskLevels?: ("low" | "medium" | "high")[];
}

export interface GammaMarketsResponse {
  markets: PolymarketMarket[];
  count?: number;
  limit?: number;
  offset?: number;
}

export interface GammaEventsResponse {
  events: PolymarketEvent[];
  count?: number;
  limit?: number;
  offset?: number;
}

export interface ClobPriceResponse {
  price: string;
  side: string;
}

export interface MarketPriceUpdate {
  marketId: string;
  tokenId: string;
  price: number;
  timestamp: string;
}
