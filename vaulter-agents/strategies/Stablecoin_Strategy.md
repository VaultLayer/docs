# Stablecoin Strategy

## Overview

The Stablecoin Strategy automatically optimizes your stablecoin holdings by finding the highest-yielding opportunities across multiple DeFi protocols. This strategy ensures your USDC and other stablecoins are always earning the best possible yield through intelligent protocol selection and position management.

## How It Works

### Core Algorithm

1. **Balance Assessment**: Analyzes current stablecoin holdings across chains
2. **Protocol Scanning**: Scans multiple DeFi protocols for yield opportunities
3. **Yield Comparison**: Compares APY across Aave, Morpho, and other protocols
4. **Position Optimization**: Moves funds to highest-yielding protocols
5. **Performance Tracking**: Monitors yield performance and rebalances as needed

### Dual-Mode Execution

The strategy operates in two distinct modes based on available USDC balance:

#### **New Position Mode** (Sufficient Balance)
- **Trigger**: USDC balance above trigger amount
- **Actions**: Creates new positions and rebalances existing ones
- **Focus**: Maximizing total yield through new deployments and optimizations

#### **Rebalancing Mode** (Limited Balance)
- **Trigger**: USDC balance below trigger amount
- **Actions**: Rebalances existing positions to better protocols
- **Focus**: Optimizing current positions without requiring new capital

This dual-mode approach ensures continuous portfolio optimization regardless of available balance.

### Yield Optimization Logic

#### **Protocol Selection**
- **Aave**: Traditional lending protocol with stable yields
- **Morpho**: Optimized lending with higher APY through peer-to-peer matching
- **Other Protocols**: Additional yield opportunities as available

#### **Position Management**
- **Supply Positions**: Earn yield by supplying stablecoins
- **Borrow Positions**: Leverage opportunities when beneficial
- **Rebalancing**: Automatic position adjustment for optimal yield
- **Existing Position Optimization**: Move current positions to better protocols even with limited new capital

## Configuration Parameters

### Required Settings
- **Trigger Amount**: Minimum stablecoin balance to trigger new position creation (e.g., 100 USDC)
  - *Note: Rebalancing of existing positions works even below this threshold*
- **Trigger Chain**: Blockchain network for stablecoin operations
- **Max Amount**: Maximum allocation per protocol (optional)

### Optional Settings
- **Allowed Chains**: Specific chains for execution
- **Protocol Preferences**: Preferred DeFi protocols
- **Custom Prompt**: Additional strategy instructions

## Supported Chains

The strategy supports the following blockchain networks:

| Chain | Chain ID | Aliases | Default RPC |
|-------|----------|---------|-------------|
| **CoreDAO** | 1116 | core, coredao, glyph | `https://rpc.coredao.org` |
| **Ethereum** | 1 | eth, mainnet | `https://ethereum-rpc.publicnode.com` |
| **Arbitrum** | 42161 | arb | `https://arb1.arbitrum.io/rpc` |
| **Base** | 8453 | coinbase | `https://mainnet.base.org` |
| **Polygon** | 137 | matic | `https://polygon-rpc.com` |
| **BSC** | 56 | binance, bnb | `https://bsc-dataseed.binance.org` |
| **Avalanche** | 43114 | avax | `https://api.avax.network/ext/bc/C/rpc` |
| **Optimism** | 10 | op | `https://mainnet.optimism.io` |

*Note: CoreDAO is the default chain if no trigger chain is specified.*

## Execution Flow

```
1. Check Stablecoin Balance
   ↓
2. Determine Execution Mode
   ├─ Sufficient Balance → New Position Mode
   └─ Limited Balance → Rebalancing Mode
   ↓
3. Scan Available Protocols
   ↓
4. Compare Yield Rates
   ↓
5. Execute Position Optimization
   ├─ New Position Mode: Create positions + rebalance existing
   └─ Rebalancing Mode: Optimize existing positions only
   ↓
6. Record Transactions & Update Portfolio
```

## Technical Implementation

### Providers Used

The strategy utilizes several data providers to gather real-time information:

#### **Balance Providers**
- **ETH Balance Provider**: Fetches current USDC balance across chains
- **Portfolio Analysis**: Analyzes total portfolio value and asset distribution

#### **Protocol Providers**
- **Aave APY Provider**: Real-time APY rates for supply and borrow positions
- **Aave Positions Provider**: Current positions and balances on Aave
- **Morpho Curated Vaults Provider**: Top USDC vaults with APY and TVL data
- **Morpho Positions Provider**: Current positions in Morpho ERC4626 vaults

#### **Market Data Providers**
- **Price Provider**: Real-time token prices for value calculations
- **Market Info Provider**: Protocol-specific market information

### Action Execution

The strategy can execute the following actions:

#### **Aave Actions**
- **AAVE_SUPPLY**: Supply USDC to Aave for yield
- **AAVE_WITHDRAW**: Withdraw USDC from Aave positions
- **AAVE_BORROW**: Borrow against supplied collateral
- **AAVE_REPAY**: Repay borrowed amounts

#### **Morpho Actions**
- **MORPHO_SUPPLY**: Supply USDC to Morpho ERC4626 vaults
- **MORPHO_WITHDRAW**: Withdraw from Morpho vault positions

### Chain Configuration

The strategy automatically detects and configures the appropriate chain based on the Agent's minting chain.

## Example Execution

### Example 1: New Position Mode (Sufficient Balance)

#### Input
- **USDC Balance**: 500 USDC
- **Trigger Amount**: 100 USDC
- **Current Position**: 300 USDC in Aave (3.2% APY)
- **Available Opportunities**: Morpho (4.8% APY)

#### Execution
1. **Mode Detection**: Balance (500) > Trigger (100) → New Position Mode
2. **Yield Analysis**: Morpho offers 1.6% higher APY
3. **Position Optimization**: Transfer 300 USDC from Aave to Morpho
4. **New Position**: Deploy remaining 200 USDC to Morpho
5. **Result**: Annual yield increased from $9.60 to $33.60

### Example 2: Rebalancing Mode (Limited Balance)

#### Input
- **USDC Balance**: 50 USDC
- **Trigger Amount**: 100 USDC
- **Current Position**: 300 USDC in Aave (3.2% APY)
- **Available Opportunities**: Morpho (4.8% APY)

#### Execution
1. **Mode Detection**: Balance (50) < Trigger (100) → Rebalancing Mode
2. **Yield Analysis**: Morpho offers 1.6% higher APY
3. **Position Rebalancing**: Transfer 300 USDC from Aave to Morpho
4. **Result**: Annual yield increased from $9.60 to $14.40 (no new capital required)

## Benefits

### **Yield Maximization**
- Automatically finds highest-yielding protocols
- Cross-protocol yield optimization
- Continuous yield monitoring and rebalancing
- **Dual-mode optimization**: Works with both new capital and existing positions

### **Risk Diversification**
- Spreads funds across multiple protocols
- Reduces single-protocol risk
- Maintains stablecoin stability

### **Automated Management**
- No manual protocol hunting required
- Automatic position rebalancing
- Continuous yield optimization
- **Always-on optimization**: Works regardless of available balance

### **Gas Optimization**
- Batches operations to minimize costs
- Optimizes transaction timing
- Efficient position management

## Risk Considerations

### **Smart Contract Risk**
- DeFi protocol security vulnerabilities
- Flash loan attacks and exploits
- Protocol upgrade risks

### **Market Risk**
- Stablecoin depegging events
- Interest rate fluctuations
- Protocol parameter changes

### **Technical Risk**
- Network congestion affecting gas costs
- Transaction failures during rebalancing
- Smart contract interaction errors

### **Liquidity Risk**
- Protocol liquidity constraints
- Withdrawal delays
- Emergency exit limitations

## Performance Metrics

### **Tracking Metrics**
- Total yield earned across protocols
- Yield improvement achieved
- Gas costs per rebalancing
- Portfolio value impact
- Protocol performance comparison

### **Optimization Opportunities**
- Adjust rebalancing frequency based on yield differentials
- Optimize for gas costs vs. yield improvement
- Monitor protocol health and performance

## Best Practices

### **Setting Trigger Amounts**
- Consider gas costs vs. yield improvement
- Account for minimum deposit requirements
- Balance frequency with efficiency
- **Rebalancing threshold**: Set lower for more aggressive existing position optimization

### **Protocol Selection**
- Diversify across multiple protocols
- Monitor protocol health and security
- Consider historical performance

### **Risk Management**
- Maintain emergency withdrawal capability
- Monitor protocol updates and changes
- Set appropriate position limits

## Troubleshooting

### **Common Issues**

**Strategy Not Executing**
- Check stablecoin balance on specified chain
- Verify trigger amount configuration
- Ensure strategy is active
- **Note**: Strategy will still rebalance existing positions even with low balance

**High Gas Costs**
- Increase minimum rebalancing amounts
- Optimize execution timing
- Consider Layer 2 solutions

**Position Failures**
- Check protocol permissions
- Verify sufficient gas limits
- Monitor network conditions

**Yield Issues**
- Verify protocol APY rates
- Check position status
- Monitor protocol updates

## Advanced Features

### **Dual-Mode Optimization**
- **New Position Mode**: Creates new positions when sufficient balance available
- **Rebalancing Mode**: Optimizes existing positions even with limited balance
- **Seamless Transition**: Automatically switches between modes based on balance

### **Multi-Chain Support**
- Execute across multiple networks
- Optimize for best yield rates
- Diversify protocol risk

### **Portfolio Integration**
- Automatic position tracking
- Performance analytics
- Integration with other strategies
- **Continuous optimization**: Works with existing positions regardless of new capital availability

### **Customization Options**
- Adjustable rebalancing thresholds
- Custom protocol preferences
- Flexible execution timing

## Protocol Integration

### **Supported Protocols**

#### **Aave**
- **Type**: Traditional lending protocol
- **Features**: Stable yields, high liquidity
- **Risk Level**: Low to medium
- **APY Range**: 2-5%
- **Supported Chains**: All supported chains (Ethereum, Arbitrum, Base, etc.)

#### **Morpho**
- **Type**: Optimized peer-to-peer lending
- **Features**: Higher yields through P2P matching
- **Risk Level**: Medium
- **APY Range**: 3-7%
- **Supported Chains**: All supported chains via ERC4626 vaults

#### **Additional Protocols**
- **Compound**: Traditional lending
- **Yearn Finance**: Yield aggregation
- **Convex Finance**: Curve yield optimization

### **Security Features**
- Multi-signature requirements
- Time-lock mechanisms
- Emergency pause functionality

## Performance Optimization

### **Yield Maximization**
- **Protocol Selection**: Choose highest-yielding protocols
- **Timing Optimization**: Rebalance during optimal conditions
- **Compounding Strategy**: Reinvest yields for compound growth

### **Gas Optimization**
- **Batch Operations**: Combine multiple transactions
- **Optimal Timing**: Execute during low gas periods
- **Efficient Routing**: Use optimal transaction paths

### **Risk Mitigation**
- **Diversification**: Spread across multiple protocols
- **Monitoring**: Continuous protocol health monitoring
- **Emergency Procedures**: Quick response to protocol issues

## Strategy Comparison

### **vs. Manual Management**
- **Automation**: No manual intervention required
- **Efficiency**: Continuous optimization
- **Consistency**: Eliminates human error
- **Always-on**: Works even when no new capital is available

### **vs. Single Protocol**
- **Yield**: Higher yields through optimization
- **Risk**: Reduced single-protocol risk
- **Flexibility**: Adapts to changing conditions

### **vs. Traditional Banking**
- **Yield**: Significantly higher returns
- **Accessibility**: No minimum balance requirements
- **Transparency**: On-chain verification
- **Continuous Optimization**: Always working to improve yields, even with existing positions

## Market Conditions

### **Bull Market**
- **Strategy**: Maximize yield through aggressive optimization
- **Focus**: Higher-yielding protocols
- **Frequency**: More frequent rebalancing

### **Bear Market**
- **Strategy**: Conservative yield optimization
- **Focus**: Stable, proven protocols
- **Frequency**: Less frequent rebalancing

### **Sideways Market**
- **Strategy**: Balanced yield optimization
- **Focus**: Consistent yield generation
- **Frequency**: Regular rebalancing

## Future Enhancements

### **Planned Features**
- **Cross-chain Optimization**: Optimize across multiple chains
- **Advanced Analytics**: Detailed performance tracking
- **Custom Strategies**: User-defined optimization rules
- **Enhanced Rebalancing**: More sophisticated position optimization algorithms

### **Protocol Expansion**
- **New Protocols**: Additional DeFi protocol integration
- **Yield Farming**: Liquidity mining opportunities
- **Derivatives**: Options and futures strategies

---
