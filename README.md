# maxprofit

class Solution {
public:
    int maxProfit(vector<int>& prices) {
        
          int i;
          int curr_min=INT_MAX;
          int curr_profit=0;
          for(int i=0;i<prices.size();i++){
              curr_min=min(curr_min,prices[i]);
              curr_profit=max(curr_profit,prices[i]-curr_min);
          }
          return curr_profit;
    }
};
