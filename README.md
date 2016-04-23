# TeensyBooth
Enter, Left, and Right buttons for photobooth

int ledbutton = 1;  // Set a button to any pin
int leftbutton = 2;
int rightbutton = 3;

void setup()
{
  pinMode(ledbutton, INPUT_PULLUP);
  pinMode(leftbutton, INPUT_PULLUP);
  pinMode(rightbutton, INPUT_PULLUP);// Set the button as an input
  digitalWrite(ledbutton, HIGH);
  digitalWrite(leftbutton, HIGH);
  digitalWrite(rightbutton, HIGH);// Pull the button high
}

void loop()
{
  if (digitalRead(ledbutton) == 0)  // if the button goes low
  {
    Keyboard.press(KEY_ENTER);  // send a 'z' to the computer via Keyboard HID
    delay(100);  // delay so there aren't a kajillion z's
    Keyboard.release(KEY_ENTER);
  }

  if (digitalRead(leftbutton) == 0)  // if the button goes low

  {
    Keyboard.press(KEY_LEFT);  // send a 'z' to the computer via Keyboard HID
    delay(300);  // delay so there aren't a kajillion z's
    Keyboard.release(KEY_LEFT);
  }

  if (digitalRead(rightbutton) == 0)  // if the button goes low

  {
    Keyboard.press(KEY_RIGHT);  // send a 'z' to the computer via Keyboard HID
    delay(300);  // delay so there aren't a kajillion z's
    Keyboard.release(KEY_RIGHT);
  }
}


