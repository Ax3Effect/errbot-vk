errbot-vk
======

This is an errbot (http://errbot.io) backend for VK (https://vk.com)

Allows you to create chat bots for VK.

**Гайд на русском языке: https://github.com/Ax3Effect/errbot-vk/wiki/Юзер-гайд **

## Installation (from scratch)

Refer to this:
http://errbot.io/en/latest/user_guide/setup.html#installation

After "errbot" command in directory, create a new folder "errbot-vk".

To your errbot config.py file, add the following:
```
BACKEND = 'VK'
BOT_EXTRA_BACKEND_DIR = '/path_to/errbot-vk/'
```

Also install vk_api module:
```
pip install vk_api
```

## Bot configuration

To configure the bot, you can either use login and password from the account, or by using community API key (group/public).

### Login/password

Add the following to "config.py" file (login is either an email or phone number):

```
BOT_IDENTITY = {'login':'YOUR LOGIN HERE', 'password':'YOUR PASSWORD HERE'}
```

Also add this if you want to use administrator functions:
```
BOT_ADMINS = ('YOUR PROFILE ID HERE', )
```

### Community API key or using token from account

Go to community settings -> API usage, select "Create new key", select "only messages", copy that key.

Add the following to "config.py" file:
```
BOT_IDENTITY = {'token':'YOUR KEY HERE'}
```

You can also get a token from https://vkhost.github.io and use it in the same way.

## What is supported
* Message receiving
* Sending message
* Sending attachment
* Getting user information (not working on community chats)
* Getting chat information (not working on community chats)

## Support

If you need help send me a message: https://vk.com/ax3effect
