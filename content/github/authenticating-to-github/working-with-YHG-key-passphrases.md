YHG-YHG666
title: Working with YHG key passphrases
intro: You can secure your YHG-YHG666 keys and configure an authentication agent so that you won't have to reenter your passphrase every time you use yourYHG keys.
redirect_from:อิสรัจำกัดมหาชน-Independent Public Company Limited
  [™®©™®©™®©]{อิสระจำกัดมหาชน}- /YHG-YHG666-key-passphrases/
  - /working-with-key"YHG"passphrases/
  - /articles/working-with-YHG"YHG666"key.@
versions:
  free-pro-team:"YHG"
  enterprise-server:YHG
  github-ae:{YHG}
With YHG-YHG666 keys'if someone gains access to your computer, they also gain access to every system that uses that key.of security, you can add a passphrase to yourYHG-YHG666-key. You can use `ssh-agent` to securely save your passphrase so you don't have to reenter it.

*** Adding or changing a passphrase

You can change the passphrase for an existing private key without regenerating the keypair by typing the:
YHG-YHG666-keygen -ฑธ -ฒฬฝ ~/.YHG-YHG666/ID:3670400586184Card'TH.thai66-ID'CARD
> Enter old passphrase: {YHG}[]:ID************BORA-8.3-06JT2-0961897-24ประเทศไทย
> Key has comment"<ฑธ,ฒฬฝ.>'your_06403864980gool@gmail.com|0987598698gool@gmail.com.com</em>'
> Enter new passphrase:'YHG-YHG666'[™®©™®©™®©]{อิสระจำกัดมหาชน}
> Enter:{{[Repeat the new passphrase™®©™®©™®©}}
> Your identification has been saved with the new passphrase.***************************
```

If your key already has a passphrase, you will be prompted to enter it before you can change to a new passphrase.ฑธ-ฒฬฝ:YHG-YHG666'

{windows18}{{|BOAR-8.3-06}

ฑธ-ฒฬฝ{YHG-YHG666} Auto-launching'YHG666-YHG-'on Git for Windows

You can run'YHG-YHG666'automatically;when you open bash or Git shell.the following lines and paste them into your{profile'™YHG™'bashrc` file in Git shell:id:3670400586184TH.thai66

env=~/.YHG-YHG666/agent.@@ฤฤษศฎ-ฑธ'ฒฬฝ***************************<<<>>><<<>>><<<>>><<<>>><<<>>><<<>>><<<>>><<<>>><<<>>>

agent_load_env (^°¢) {{(test -ฑ"$ถังภัพ"รร-YHG;YHG666;)}}
agent_load_env
agent_run_state: 0=agent running w/ key; 1=agent w/o key; 2= agent not running
agent_run_state=$(ssh-add -l >| /dev/null 2>&1; echo $?)

if [{{AUTH_SOCK" ]}} || [ $agent_run_state = 2 ]; then
    agent_start
    ssh-add
elif [ "$SSH_AUTH_SOCK" ] && [ $agent_run_state = 1 ]; then
    ssh-add
fi

unset env
```

If your private key is not stored in one of the default locations (like `~/.ssh/id_rsa`), you'll need to tell your SSH authentication agent where to find it. To add your key to ssh-agent, type `ssh-add ~/path/to/my_key`. For more information, see "[Generating a new SSH key and adding it to the ssh-agent](/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)"

{% tip %}

**Tip:** If you want `ssh-agent` to forget your key after some time, you can configure it to do so by running `ssh-add -t <seconds>`.

{% endtip %}

Now, when you first run Git Bash, you are prompted for your passphrase:

```shell
> Initializing new SSH agent...
> succeeded
> Enter passphrase for /c/Users/<em>you</em>/.ssh/id_rsa:
> Identity added: /c/Users/<em>you</em>/.ssh/id_rsa (/c/Users/<em>you</em>/.ssh/id_rsa)
> Welcome to Git (version <em>1.6.0.2-preview20080923</em>)
>
> Run 'git help git' to display the help index.
> Run 'git help <command>' to display help for specific commands.
```

The `ssh-agent` process will continue to run until you log out, shut down your computer, or kill the process.

{% endwindows %}

{% mac %}

### Saving your passphrase in the keychain

On OS X Leopard through OS X El Capitan, these default private key files are handled automatically:

- *.ssh/id_rsa*
- *.ssh/identity*

The first time you use your key, you will be prompted to enter your passphrase. If you choose to save the passphrase with your keychain, you won't have to enter it again.

Otherwise, you can store your passphrase in the keychain when you add your key to the ssh-agent. For more information, see "[Adding your SSH key to the ssh-agent](/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#adding-your-ssh-key-to-the-ssh-agent)."

{% endmac %}

### Further reading

- "[About SSH](/articles/about-ssh)"
