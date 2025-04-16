# WinCCUnified-APIGPT-Integration
Integrating WinCC Unified with ChatGPT API

To send data to the GPT API, use the following script in a button:  
let tag1 = Tags("prompt");  
let prompt1 = tag1.Read();  
try   
{  
  let response = await Screen.Items("API Integration_1").getOpenAIResponse(prompt1);  
  let txt = Screen.FindItem("Text_1").Text ;  
  Screen.FindItem("Text_1").Text = txt + "\r\n" + response;  
}   
catch (error)  
{  
  let txt = Screen.FindItem("Text_1").Text ;  
  Screen.FindItem("Text_1").Text = txt + "\r\n" + error;  
}  
![image](https://github.com/user-attachments/assets/9886d350-4c5c-4c3e-99ef-fdd05eb99cef)
