# Question_Bot
# chatBot
# CS1004 example chatbot using loop and variable prompts
 
write 'Dalliana: Hi! My name is Dalliana.'
await read 'Dalliana: What\'s your name?', defer name
write 'Dalliana: Hello ' + name
done = false
while not done
  prompt = (name + ' can you guess who I am?') + ':'
  await read prompt, defer q
  if (q.match /quit|exit|give up/)
    #this is related to the boolean values
   write 'Dalliana: OK, nice talking to you!'
   done = true
  else if (q.match /robot|human|chatbot/)
    #this is /also/ related to the boolean values
    write 'Dalliana: Close.. But I am a human, of course.'
  else (write 'Dalliana: Good guesswork!')

