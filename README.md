# WeatherUpdate
# Weather update project

website: https://openweathermap.org/

-> signup in the above given url.

-> Generate your api-key = API Key

-> API call : api.openweathermap.org/data/2.5/weather?q={city name}&appid={API key}

-> call the API(HTTP request) using requests.get()

-> convert the data to json format

-> from json, get the necessary data



You can schedule a notification message using slack and Twilio API's
    # For slack: 

you need an slack account + webhook url

webhook_url = "https://hooks.slack.com/services/<enter ur webhook slack url>"
    
payload = { 'text': msg }

return requests.post(webhook_url, headers={'Content-Type': 'application/json'}, data=json.dumps(payload))

    # For Twilio:

you need the sid and token

modules required:

from twilio.twiml.voice_response import VoiceResponse

from twilio.rest import Client

from twilio.base.exceptions import TwilioRestException

Paste the code:

account_sid = '<>'

auth_token = '<>'

resp = VoiceResponse()

client = Client(account_sid, auth_token)

call = client.calls.create(url = 'url', to='+to_num',from_='from_num' )

    # Read a message aloud to the caller 
    
resp.say("Thanks for calling! We just sent you a text with a clue.", voice='alice')

#client.messages.create(body="Hello world", from_='', to='')

