import random

# Define the number of races
num_simulations = 43
#how many races won of these races
driver_wins = 4

# Driver's statistics 
driver_win_percentage = 0.1
# Win chance
driver_avg_finish = 13.6
#avg of finishing placement
driver_laps_led_mean = 237
#number of Laps that were led 
driver_laps_led_stddev = .017
#chance of laps to be lead total

for _ in range(num_simulations):
    # Simulate race outcomes
    finish_position = random.randint(1, 40)
    laps_led = max(0, int(random.normalvariate(driver_laps_led_mean, driver_laps_led_stddev)))

    # Check if the driver won the simulated race
    if finish_position == 1 or (finish_position == 2 and laps_led > 0):
        driver_wins += 1

# Calculate the estimated probability of the driver winning
probability_of_winning = driver_wins / num_simulations
print(f"Estimated probability of winning: {probability_of_winning:.2%}")
