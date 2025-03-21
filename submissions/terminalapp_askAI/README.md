
# **ai_terminal**

A magical and interactive terminal app where you can ask questions to an AI, set alarms on your device, open software, and get answers in the cutest way possible! It features text-to-speech and a delightful loading animation. Whether you need a quick answer or want to set reminders for your tasks, this app has it all!

## **Features**
- **AI Chat**: Ask the AI any question and receive an answer in the terminal.
- **Text-to-Speech (TTS)**: Listen to the AI's response through a text-to-speech engine.
- **Magical Loading Animation**: Watch a cute animation while the AI is processing your question.
- **Set Alarms**: Set alarms on macOS using Apple's Reminders app.
- **Open Software**: Open any software directly from the terminal.

## **Requirements**
- Python 3.x
- Dependencies:
  - `requests`: For making API calls to the AI service.
  - `json`: For handling JSON data.
  - `argparse`: For handling command-line arguments.
  - `subprocess`: For running system commands to open software or set alarms.
  - `pyttsx3`: For text-to-speech (TTS) functionality.
  - `termcolor`: For colorful terminal output.
  - `rich`: For enhanced console output and spinner.
  - `concurrent.futures`: For threading and concurrency.
  - `os`, `sys`: For platform-specific functionalities (macOS, Linux, Windows).

## **Installation**

You can easily install the **ai_terminal** app via PyPI. To install, run the following command:

```bash
pip install hc-ai-terminal
```

This will install the app and its required dependencies.

## **Usage**

### **AI Chat**
To ask a question to the AI, simply run the app:
```bash
ai "What is the meaning of life?"
```

The app will show a cute loading animation and provide an answer after processing. It also uses text-to-speech (TTS) to read out the answer.

### **Set an Alarm**
To set an alarm on macOS, use the `--alarm` flag followed by the time in `HH:MM` format (24-hour):
```bash
ai --alarm 08:00
```

This will create an alarm using the Reminders app on macOS. The app will speak the time when the alarm is set.

### **Open a Software Application**
To open an application (e.g., "Safari" on macOS), use the `--open` flag:
```bash
ai --open "Safari"
```

This will attempt to open the specified application, depending on your operating system.

### **Combined Command**
You can combine multiple commands in one run:
```bash
ai "What is the weather today?" --alarm 08:00 --open "Safari"
```

This will ask a question, set an alarm, and open Safari all at once.

### **Interactive Mode**
If no arguments are provided, the app will enter interactive mode, where you can ask questions and get answers directly.

## **Platforms Supported**
- macOS: Alarm setting is supported through the AppleScript integration with the Reminders app.
- Linux/Windows: Alarm setting is not supported, but other features work.
- Software opening is supported on macOS, Linux, and Windows.

## **Known Issues**
- TTS may not work properly on all platforms. If text-to-speech fails, the app falls back to a simple printed message.
- Alarm setting only works on macOS.

## **Contributing**
Feel free to fork this project and submit pull requests. If you encounter any issues, open an issue on GitHub.

## **License**
This project is open source and available under the MIT License.
