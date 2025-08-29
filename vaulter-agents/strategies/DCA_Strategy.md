# DCA (Dollar Cost Averaging) Strategy

## Overview

The DCA Strategy automatically purchases Bitcoin at regular intervals using a sophisticated algorithm that adjusts the purchase amount based on market conditions and price predictions.

## How It Works

### Core Algorithm

1. **Balance Monitoring**: Continuously monitors USDC balance across specified chains
2. **Trigger Detection**: Executes when USDC balance exceeds the trigger amount
3. **Intelligent Amount Calculation**: Adjusts purchase amount based on BTC price predictions
4. **Market Execution**: Swaps USDC for wBTC using optimal DEX routing
5. **Performance Tracking**: Records execution details and portfolio impact

### Intelligent DCA Logic

The strategy uses AI-powered price predictions to optimize purchase timing:

#### **Standard DCA**
- **Condition**: BTC price change < ±0.2%
- **Action**: Purchase trigger amount (e.g., 5 USDC)
- **Use Case**: Normal market conditions

#### **Aggressive DCA**
- **Condition**: BTC expected to rise > 0.2%
- **Action**: Increase purchase by 20% (e.g., 5 → 6 USDC)
- **Use Case**: Bullish market conditions

#### **Conservative DCA**
- **Condition**: BTC expected to fall > 0.2%
- **Action**: Decrease purchase by 20% (e.g., 5 → 4 USDC)
- **Use Case**: Bearish market conditions

## Configuration Parameters

### Required Settings
- **Trigger Amount**: Minimum USDC balance to trigger DCA (e.g., 5 USDC)
- **Trigger Chain**: Blockchain network for USDC balance monitoring
- **Max Amount**: Maximum purchase amount per execution (optional)

### Optional Settings
- **Allowed Chains**: Specific chains for execution
- **Custom Prompt**: Additional strategy instructions

## Execution Flow

```
1. Check USDC Balance
   ↓
2. Compare with Trigger Amount
   ↓
3. Get BTC Price Predictions
   ↓
4. Calculate Optimal Purchase Amount
   ↓
5. Execute USDC → wBTC Swap
   ↓
6. Record Transaction & Update Portfolio
```

## Example Execution

### Input
- **Trigger Amount**: 5 USDC
- **Available Balance**: 52 USDC
- **BTC Prediction**: +0.28% in 8 hours

### Execution
1. **Strategy**: Aggressive (0.28% > 0.2%)
2. **Purchase Amount**: 6 USDC (5 × 1.2)
3. **Swap**: 6 USDC → 0.0006 wBTC
4. **Result**: Portfolio optimized with increased BTC exposure

## Benefits

### **Automated Accumulation**
- No manual intervention required
- Consistent Bitcoin purchases
- Eliminates emotional trading decisions

### **Market Intelligence**
- AI-powered price predictions
- Dynamic amount adjustment
- Optimal timing based on market conditions

### **Risk Management**
- Fixed trigger amounts prevent overspending
- Conservative mode reduces exposure in bear markets
- Multi-chain support for diversification

### **Cost Efficiency**
- Optimized DEX routing for best prices
- Gas cost optimization
- Slippage protection

## Risk Considerations

### **Market Risk**
- Bitcoin price volatility affects purchase value
- Predictions may not always be accurate
- Past performance doesn't guarantee future results

### **Technical Risk**
- Smart contract risks on DEX platforms
- Network congestion affecting gas costs
- Potential slippage on large orders

### **Liquidity Risk**
- Insufficient liquidity for large purchases
- Price impact on significant orders
- Market depth considerations

## Performance Metrics

### **Tracking Metrics**
- Total BTC accumulated
- Average purchase price
- Dollar cost average vs. market price
- Transaction success rate
- Gas costs per execution

### **Optimization Opportunities**
- Adjust trigger amounts based on market conditions
- Fine-tune prediction thresholds
- Optimize for specific time periods

## Best Practices

### **Setting Trigger Amounts**
- Start with small amounts (5-10 USDC)
- Consider your monthly investment budget
- Account for gas costs in calculations

### **Chain Selection**
- Choose chains with good USDC liquidity
- Consider gas costs vs. execution speed
- Monitor chain-specific performance

### **Monitoring & Adjustment**
- Review performance monthly
- Adjust parameters based on market conditions
- Consider increasing amounts during bear markets

## Troubleshooting

### **Common Issues**

**Strategy Not Executing**
- Check USDC balance on specified chain
- Verify trigger amount configuration
- Ensure strategy is active

**High Gas Costs**
- Consider using Layer 2 networks
- Optimize execution timing
- Review gas price settings

**Slippage Issues**
- Reduce purchase amounts
- Use limit orders when available
- Monitor market liquidity

## Advanced Features

### **Multi-Chain Support**
- Execute across multiple networks
- Optimize for best prices
- Diversify execution risk

### **Portfolio Integration**
- Automatic position tracking
- Performance analytics
- Integration with other strategies

### **Customization Options**
- Adjustable prediction thresholds
- Custom trigger conditions
- Flexible execution parameters

---
