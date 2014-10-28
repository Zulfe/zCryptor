//this a caeser cipher form of encryption
package APCS;

import javax.swing.JOptionPane;

public class Encryptor {
	public static void main(String [] args){
		String userInput = JOptionPane.showInputDialog("Welcome to the Encryptor! Please input a message.");
		//checks if user's input and shift is valid
		if(userInput.length() == 0){
			JOptionPane.showMessageDialog(null, "Error: User has not inputted a message.");
			return;
		}
		
		String userShift = JOptionPane.showInputDialog("We're using Caeser's Shifting Encryption. Input a shift value.");
		int userShiftVal = Integer.parseInt(userShift);
		//checks if user's shift input is valid
		if(!(userShiftVal >= 0)){
			JOptionPane.showMessageDialog(null, "Error: Shift value is not a number or number is less than 0.");
			return;
		}

		
		//converts the message using userShiftVal as the shift value
		String encInput = "";
		
		//converts the string char by char for the length of the message
		for(int i = 0; i < (userInput.length()); i++){
			//if there's a space, but a space in the new message
			if((userInput.charAt(i)) == (' ')){
				encInput = encInput + " ";
			} else {
				//new character from the string
				char stringPart = userInput.charAt(i);
				//change the character based on the user shift val
				char stringPartFinal = (char) (stringPart + userShiftVal);
				if(stringPartFinal > 122)
					stringPartFinal = (char) (stringPart + userShiftVal - 26);
				encInput = encInput + stringPartFinal;
			}
		}
		JOptionPane.showMessageDialog(null, encInput);
	}
	
}
