# bonds
class LowRiskBond:
    def __init__(self, principal, interest_rate, term):
        self.principal = principal
        self.interest_rate = interest_rate
        self.term = term
        self.current_value = principal

    def calculate_interest(self):
        interest_earned = self.current_value * (self.interest_rate / 100)
        self.current_value += interest_earned
        return interest_earned

    def display_info(self):
        print(f"Principal: ${self.principal}")
        print(f"Interest Rate: {self.interest_rate}%")
        print(f"Term: {self.term} years")
        print(f"Current Value: ${self.current_value}")

# Example usage
if __name__ == "__main__":
    # Creating an instance of the LowRiskBond class
    low_risk_bond = LowRiskBond(principal=10000, interest_rate=2, term=5)

    # Displaying information about the bond
    low_risk_bond.display_info()

    # Simulating interest calculation for 3 years
    for _ in range(3):
        interest_earned = low_risk_bond.calculate_interest()
        print(f"Interest Earned: ${interest_earned}")

    # Displaying updated information about the bond
    low_risk_bond.display_info()
