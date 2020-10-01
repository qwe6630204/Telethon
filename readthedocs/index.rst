========================
Telethon开发文档
========================

.. code-block:: python

   from telethon.sync import TelegramClient, events

   with TelegramClient('name', api_id, api_hash) as client:
      client.send_message('me', 'Hello, myself!')
      print(client.download_profile_photo('me'))

      @client.on(events.NewMessage(pattern='(?i).*Hello'))
      async def handler(event):
         await event.reply('Hey!')

      client.run_until_disconnected()


* 你是新手吗? 开始安装吧 :ref:`installation`!
* 还在寻找参考办法? 请查阅 :ref:`client-ref`.
* 你是否升级了依赖库? 请阅读 :ref:`changelog`.
* 曾经使用过telethon v1.0? 请看 :ref:`compatibility-and-convenience`.
* 来自Bot API 还是想要创建一个新的机器人? 请看 :ref:`botapi`.
* 是否需要完整的API参考? https://tl.telethon.dev/.


Telethon是什么?
-------------

Telegram 是一个流行的即时消息应用程序. Telethon库将使您能够轻松编写可与Telegram进行交互的Python程序. Telethon已为您扫除了大多数的障碍, 因此您可以专注于开发一个应用程序.


如何使用该开发文档?
-----------------------------------

如果您刚开始接触Telethon, 请按照每个页面的步骤,一步步地进行学习;当然如果您有一定的基础,您也可以使用左侧的菜单快速跳过,选择您想要学习的部分.


.. toctree::
    :hidden:
    :caption: First Steps

    basic/installation
    basic/signing-in
    basic/quick-start
    basic/updates
    basic/next-steps

.. toctree::
    :hidden:
    :caption: Quick References

    quick-references/faq
    quick-references/client-reference
    quick-references/events-reference
    quick-references/objects-reference

.. toctree::
    :hidden:
    :caption: Concepts

    concepts/strings
    concepts/entities
    concepts/updates
    concepts/sessions
    concepts/full-api
    concepts/errors
    concepts/botapi-vs-mtproto
    concepts/asyncio

.. toctree::
    :hidden:
    :caption: Full API Examples

    examples/word-of-warning
    examples/chats-and-channels
    examples/users
    examples/working-with-messages

.. toctree::
    :hidden:
    :caption: Developing

    developing/philosophy.rst
    developing/test-servers.rst
    developing/project-structure.rst
    developing/coding-style.rst
    developing/testing.rst
    developing/understanding-the-type-language.rst
    developing/tips-for-porting-the-project.rst
    developing/telegram-api-in-other-languages.rst

.. toctree::
    :hidden:
    :caption: Miscellaneous

    misc/changelog
    misc/wall-of-shame.rst
    misc/compatibility-and-convenience

.. toctree::
    :hidden:
    :caption: Telethon Modules

    modules/client
    modules/events
    modules/custom
    modules/utils
    modules/errors
    modules/sessions
    modules/network
    modules/helpers
