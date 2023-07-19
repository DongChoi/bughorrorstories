# BUG HORROR STORIES

## Jul 12, 2023

### Time consumed couple of hours.

- Wow I have not had any horror stories in a while. I do have a recent one, not too bad though. I have been practicing and learning the new changes made by NextJS v12 -> v13 as well as TailWind CSS. For Next13, I had a lot of trouble with the file structure changes introduced in 13. For example, nextauth file and folder systems are different as well as routes being able to handle many different calls. ROUTES ARE AMAZING but the folder structure threw me into a rabbit hole because there is not much documentation on the new version so I had to make sure I was not reading outdate advice. It was also my first time setting up AuthO so that was really fun.

- As for Tailwind CSS I didn't really have that much trouble for the most part. I think this is because I like to think that I have strong fundamental knowledge with vanilla css which is what I've used the whole time. This was my first time also making my application mobile responsive with mobile first design. I had a lot of fun with it but when it got to animations which I never done before as well really messed me up. As far as I know, most people (on youtube at least) render

## May 5, 2023

### Time consumed one hour.

- I must be going crazy with prisma and vercel lately. I kept getting type errors even after npx prisma generate and migrating to dev to update the sql files and types for typescript. I had two files, one was called createChildComment and the other one was createComment. I eventually fixed the createComment but didn't realize that the vercel had shown me that the createChildComment was the one with the type errors. So I kept working on the createComment THE WHOLE TIME. Because the code was almost identical but with different end points (as create child comment was in api/comments/:parentCommentId and create comment was in api/projects/:studio/:name). One great skill I learned and honed today was to understand how to navigate index.d.ts. Wow what a life saver that is. It is so much easier to correct types now. I am very proud of myself for learning how to be more efficient at digging down the files to see what my types are supposed to look like.

## May 1, 2023

### Time consumed BASICALLY THE WHOLE DAY.

- ...nextauth typing disaster. Oh my goodness, what a day. I thought everything was good for production after manipulating the session and token output. BUT then when I pushed it to the dev branch, vercel failed to deploy. But guess what, vercel actually showed a informal error log. It was a typing issue and I created the interfaces to reflect what the session and tokens were supposed to be. But guess what, Vercel still logged that there was still a type error. I TRIED TO CHANGE THE TYPES SO MANY TIMES. After struggling with it for like two hours, I worked out, went home and decompressed. I couldn't fall asleep though... because this was one of those things I couldn't let go until I had fixed the problem. I actually solved it pretty fast after going through the next-auth docs (I guess I just needed some time away from it... but coffee kind of hinders me from walking away sometimes lol). I found out that I had to make a next-auth.d.ts and create a session, jwt, and account type that combines existing ones for the call back. AND VOILA! The session type was correct! I was not able to fix the session(session, token, account) typing. I saw that many tutorials used both session and token callback args as any so I took it as a victory for at least doing the session typing correct.

## April 25, 2023

### Time consumed ~1.5Hrs

- what a day, after working at thecoreloop for a while and making pull requests, improving and fixing bugs, the co-founder finally added me to their vercel account. I was wary as whenever I made a push to their git, their vercel was failing to deploy but it worked just as fine on my local machine and vercel. After they allowed my credentials, I finally got the chance to see the logs to see why it was failing to deploy. The logs pointed at something that I never worked on before so I was confused. Errors started to change as I commented out the areas the log was pointing to. Then, the cofounder tried to redeploy deleting one file after another, of the the files I worked on, crushing my manhood at the same time lol. Then I was like f\*\*k it, I can reapply the code once the bug was found. After deleting most of my work, Vercel was able to deploy again. When we found out the problem file, I realized that in the schema.prisma, there was an environmental variable that was not registered with vercel. At this point **I WAS FURIOUS, NO OTHER CLOUD PLATFORM THAT I'VE WORKED WITH GAVE ME SUCH A MISLEADING FAILED DEPLOYMENT LOG. WHAT ARE YOU DOING OVER THERE VERCEL?! CREATE A MORE ACCURATE BUG MESSAGE STATING THAT THE ENVIRONMENTAL VARIABLES WERE UNDEFINED OR NOT FOUND.** I was at least relieved because all of my work so far wasn't wasted... BUT MY 1.5 HRS WAS!! The co-founder then told me that this is his every day for him and I felt such a sense of comradre and felt for him because he has to deal with this everyday haha. I can't wait until when we migrate our servers to AWS kubernetes as we will have a tougher time together. <small>at least they will have better deployment logs... even if its thousands of lines, I'd prefer that lol.</small>
