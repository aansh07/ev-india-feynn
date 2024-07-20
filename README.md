**Market Entry Strategy Report for Electric Vehicle Start
Team Members
- **Ansh Matto** (Responsible for identifying the most optimal market segments)
---
#### Fermi Estimation (Breakdown of Problem Statement)
1. **Market Size Estimation:**
- Estimate the total number of vehicles in the market.
- Determine the proportion of electric vehicles (EVs) relative to the total market.
2. **Target Market Size:**
- Estimate the number of potential early adopters of EVs based on demographic and psychographic factors.
3. **Price Range and Sales Estimate:**
- Determine the average selling price of EVs.
- Estimate the potential sales volume by targeting specific market segments.
4. **Profit Calculation:**
- Estimate potential profit by multiplying the potential customer base by the target price range.
---
#### Data Sources (Data Collection - All Team Members)
1. **EV Market Data:**
- Market research reports
- Government statistics on EV adoption
2. **General Vehicle Type Data:**
- Industry publications
- Automobile databases
3. **Charging Stations Data:**
- Government reports
- Data from charging infrastructure providers
4. **Vehicle Usage Statistics in Cities:**
- Surveys and studies on vehicle usage patterns
- Traffic and transportation reports
5. **Demographic Data:**
- Census data
- Market research surveys
---
#### Data Pre-processing (Steps and Libraries Used)
1. **Loading Data:**
- Libraries Used: `pandas`
- Code: `df = pd.read_csv('ev_data.csv')`
2. **Handling Missing Values:**
- Checked for missing values and handled them appropriately (imputation or removal).
3. **Encoding Categorical Variables:**
- Libraries Used: `pandas`
- Code: `df_encoded = pd.get_dummies(df, columns=['Car', 'Style', 'Transmission', 'VehicleType', 'BaseModel', 'TopModel'])`
4. **Feature Scaling:**
- Libraries Used: `scikit-learn`
- Code: `scaler = StandardScaler()`, `df_scaled = scaler.fit_transform(df_encoded[features])`
5. **Dimensionality Reduction (for Visualization):**
- Libraries Used: `scikit-learn`
- Code: `pca = PCA(n_components=2)`, `principal_components = pca.fit_transform(df_scaled)`
---
#### Segment Extraction (ML Techniques Used)
1. **K-Means Clustering:**
- Libraries Used: `scikit-learn`
- Code:
```python
kmeans = KMeans(n_clusters=3, random_state=42)
df['Cluster'] = kmeans.fit_predict(df_scaled)
```
2. **PCA for Visualization:**
- Libraries Used: `scikit-learn`
- Code:
```python
pca = PCA(n_components=2)
principal_components = pca.fit_transform(df_scaled)
```
---
#### Profiling and Describing Potential Segments
1. **Cluster 0:**
- Characteristics: Higher price range, higher capacity, premium models
- Target Group: High-income individuals, tech-savvy early adopters
2. **Cluster 1:**
- Characteristics: Mid-range price, moderate range, standard models
- Target Group: Middle-income groups, environmentally conscious consumers
3. **Cluster 2:**
- Characteristics: Lower price range, basic models, lower capacity
- Target Group: Budget-conscious buyers, first-time EV buyers
---
#### Selection of Target Segment
Based on the analysis:
- **Target Segment:** Cluster 1
- **Rationale:** This segment includes middle-income groups and environmentally conscious consumers, representing a balance between affordability and technology adoption.
---
#### Customizing the Marketing Mix
1. **Product:**
- Offer mid-range priced EVs with moderate range and features.
- Focus on environmentally friendly technology and cost-efficiency.
2. **Price:**
- Set competitive pricing within the mid-range to attract the target segment.
3. **Place:**
- Focus on urban areas with established charging infrastructure.
- Partner with local dealers and online platforms for distribution.
4. **Promotion:**
- Highlight environmental benefits and cost savings.
- Use digital marketing and influencer partnerships to reach tech-savvy consumers.
---
#### Potential Customer Base and Profit Calculation
1. **Potential Customer Base:**
- Estimated based on demographic and market data for the target segment.
2. **Target Price Range:**
- Mid-range price determined from segment analysis.
3. **Potential Profit:**
- **Formula:** Potential Customer Base * Target Price Range
- Example Calculation: If potential customer base is 50,000 and target price range is $20,000:
```plaintext
Potential Profit = 50,000 * 20,000 = $1,000,000,000
```
---
#### Most Optimal Market Segments
- **Optimal Segments Identified:** Cluster 1 (middle-income, environmentally conscious consumers)
- **Team Member Responsible:** Ansh Matto
