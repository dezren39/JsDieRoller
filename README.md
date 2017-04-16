# JsDieRoller
Class Assignment, no arrays allowed.

    var fName;
    var numDice;
    var result = 0;

    fName = prompt("Please enter you first name: ");

    while(fName == "") {
      fName = prompt("Reminder: Please enter you first name: ", fName);
    }

    numDice = prompt("How many dice would you like to roll?");

    while(isNaN(numDice) || parseFloat(numDice) != parseInt(numDice)) { 
      numDice = prompt("How many dice would you like to roll?");
    }

    document.write("<p>Rolling " + numDice + 
      " die...<br \>	Hey " + fName + ", you rolled a");

    for (i = 0; i < numDice; i++) {
      var randomNumber = Math.floor(1 + (Math.random() * 6));
      alert("Dice #" + (i + 1) + " " + randomNumber);
      document.write(" " + randomNumber);

      if (i + 2 == numDice) {
        document.write(i == 0 ? " and " : ", and");
      }
      else if (i + 1 != numDice) {
        document.write(",")
      }
      result = result + randomNumber;
    }

    document.write(" for a grand total of " + result + "</p>");
