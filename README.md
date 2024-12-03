# Python_Day9
#Project: Build a Program to Check for Duplicate Signal Readings in a Dataset
def check_duplicates(signal_readings):
    """
    Check for duplicate signal readings in a dataset.

    Parameters:
    signal_readings (list): A list of signal readings.

    Returns:
    tuple: A boolean indicating if duplicates were found, and a set of duplicate readings.
    """
    unique_readings = set(signal_readings)
    duplicates = set([x for x in signal_readings if signal_readings.count(x) > 1])
    has_duplicates = len(signal_readings) != len(unique_readings)
    
    return has_duplicates, duplicates

# Example usage:
signal_readings = [10, 12, 15, 14, 11, 13, 12, 14]
has_duplicates, duplicates = check_duplicates(signal_readings)
if has_duplicates:
    print(f"Duplicates found: {duplicates}")
else:
    print("No duplicates found")
