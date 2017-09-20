# Leak report
The leak that was present was "cleaned" in the strip method. The method makes the string "cleaned" to compare against but doesn't not free this memory after the comparison occurs and there is no reason to store this information. An if statement is needed however because attempting to free an empty string will give an error so we need to check if "cleaned" is empty or not before freeing it.

