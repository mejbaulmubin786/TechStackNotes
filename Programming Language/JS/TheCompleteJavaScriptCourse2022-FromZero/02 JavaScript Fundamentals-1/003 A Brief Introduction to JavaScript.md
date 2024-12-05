1
00:00:00,930 --> 00:00:04,230
<v ->So you've already written a line or two of JavaScript,</v>

2
00:00:04,230 --> 00:00:08,890
but what exactly is JavaScript and what can we do with it?

3
00:00:08,890 --> 00:00:10,660
Well, that's exactly what

4
00:00:10,660 --> 00:00:12,750
we're gonna find out in this video.

5
00:00:12,750 --> 00:00:14,280
And so in this lecture,

6
00:00:14,280 --> 00:00:17,230
we will set the stage for the rest of the course.

7
00:00:17,230 --> 00:00:19,150
And so it's really important that you

8
00:00:19,150 --> 00:00:20,883
follow this one until the end.

9
00:00:22,160 --> 00:00:25,680
So we can define JavaScript in many different ways.

10
00:00:25,680 --> 00:00:27,440
But, my definition is that

11
00:00:27,440 --> 00:00:30,050
it's a high level object-oriented,

12
00:00:30,050 --> 00:00:32,950
multi-paradigm programming language.

13
00:00:32,950 --> 00:00:34,290
And with that being said,

14
00:00:34,290 --> 00:00:36,810
can we move on to the next lecture now?

15
00:00:36,810 --> 00:00:39,210
Well, probably not because

16
00:00:39,210 --> 00:00:41,980
what does any of that actually mean?

17
00:00:41,980 --> 00:00:44,740
So let's deconstruct this just a little bit

18
00:00:44,740 --> 00:00:47,830
to at least make some sense out of this.

19
00:00:47,830 --> 00:00:50,660
And starting with programming language itself,

20
00:00:50,660 --> 00:00:53,580
a programming language is basically just a tool

21
00:00:53,580 --> 00:00:55,270
that allows us to write code

22
00:00:55,270 --> 00:00:58,910
that will instruct a computer to do something.

23
00:00:58,910 --> 00:01:00,800
And of course, that's our main goal

24
00:01:00,800 --> 00:01:03,550
of using JavaScript, right?

25
00:01:03,550 --> 00:01:05,100
Then I go on and say that

26
00:01:05,100 --> 00:01:07,460
JavaScript is a high-level language,

27
00:01:07,460 --> 00:01:09,780
which means that we don't have to think

28
00:01:09,780 --> 00:01:12,930
about a lot of complex stuff such as managing

29
00:01:12,930 --> 00:01:16,360
the computer's memory while it runs or program.

30
00:01:16,360 --> 00:01:17,460
So in JavaScript,

31
00:01:17,460 --> 00:01:20,090
there are a lot of so-called abstractions

32
00:01:20,090 --> 00:01:21,870
over all these small details

33
00:01:21,870 --> 00:01:23,920
that we don't want to worry about.

34
00:01:23,920 --> 00:01:25,040
And this makes the language

35
00:01:25,040 --> 00:01:28,260
a lot easier to write and to learn.

36
00:01:28,260 --> 00:01:31,760
Next, I say that JavaScript is object oriented.

37
00:01:31,760 --> 00:01:33,910
And all that means is that the language

38
00:01:33,910 --> 00:01:37,100
is mostly based on the concept of objects

39
00:01:37,100 --> 00:01:39,600
for storing most kinds of data.

40
00:01:39,600 --> 00:01:41,280
And of course, we will learn all about

41
00:01:41,280 --> 00:01:44,690
object-oriented programming throughout this course.

42
00:01:44,690 --> 00:01:48,490
Finally, JavaScript is also a multi-paradigm language,

43
00:01:48,490 --> 00:01:51,680
meaning that it's so flexible and versatile,

44
00:01:51,680 --> 00:01:54,940
that we can use all kinds of different programming styles,

45
00:01:54,940 --> 00:01:58,250
such as imperative and declarative programming.

46
00:01:58,250 --> 00:01:59,990
And these different styles are just

47
00:01:59,990 --> 00:02:03,760
different ways of structuring our code, basically.

48
00:02:03,760 --> 00:02:07,540
Again, you will learn all about this throughout the course.

49
00:02:07,540 --> 00:02:10,670
This just a first, very high level overview,

50
00:02:10,670 --> 00:02:13,113
but I hope it's been making sense so far.

51
00:02:14,640 --> 00:02:18,100
Anyway, now that we know what JavaScript actually is,

52
00:02:18,100 --> 00:02:20,620
at least kind of, what is the role

53
00:02:20,620 --> 00:02:22,720
that it plays in web development,

54
00:02:22,720 --> 00:02:26,340
or in other words, what do we actually use it for?

55
00:02:26,340 --> 00:02:27,830
And to answer that question,

56
00:02:27,830 --> 00:02:31,940
let's actually look at a three core technologies of the web,

57
00:02:31,940 --> 00:02:36,240
HTML, CSS and of course, JavaScript.

58
00:02:36,240 --> 00:02:39,140
So these three technologies all work together

59
00:02:39,140 --> 00:02:41,520
to create beautiful, interactive

60
00:02:41,520 --> 00:02:44,860
and dynamic websites or web applications.

61
00:02:44,860 --> 00:02:49,130
Now the HTML is responsible for the content of the page.

62
00:02:49,130 --> 00:02:51,880
So the text, the images, the buttons,

63
00:02:51,880 --> 00:02:54,480
and all the contents that you see on the webpage

64
00:02:54,480 --> 00:02:57,150
is always written in HTML.

65
00:02:57,150 --> 00:03:00,040
Then the CSS is responsible for the

66
00:03:00,040 --> 00:03:02,160
presentation of that content.

67
00:03:02,160 --> 00:03:05,000
So basically for styling and for laying out

68
00:03:05,000 --> 00:03:07,330
the elements on a webpage.

69
00:03:07,330 --> 00:03:10,300
And then, finally, JavaScript is the real

70
00:03:10,300 --> 00:03:12,920
programming language of the internet.

71
00:03:12,920 --> 00:03:15,540
And it allows developers to add dynamic

72
00:03:15,540 --> 00:03:19,470
and interactive effects to any webpage.

73
00:03:19,470 --> 00:03:23,110
We also use it to manipulate the content or the CSS,

74
00:03:23,110 --> 00:03:25,420
load data from remote servers

75
00:03:25,420 --> 00:03:29,310
and really build entire applications in the browser,

76
00:03:29,310 --> 00:03:32,530
which we then call web applications.

77
00:03:32,530 --> 00:03:35,340
Now, we can also use the analogy of nouns,

78
00:03:35,340 --> 00:03:38,300
adjectives, and verbs to make this separation

79
00:03:38,300 --> 00:03:40,783
of roles a bit easier to understand.

80
00:03:41,670 --> 00:03:45,290
So in this analogy, HTML represents the nouns.

81
00:03:45,290 --> 00:03:49,870
For example, saying that the P element is a paragraph.

82
00:03:49,870 --> 00:03:53,070
And so paragraph is the noun here.

83
00:03:53,070 --> 00:03:55,390
The CSS then, is the adjective,

84
00:03:55,390 --> 00:03:57,660
because it describes the noun.

85
00:03:57,660 --> 00:04:02,510
Like this piece of CSS saying the paragraph text is red.

86
00:04:02,510 --> 00:04:06,470
And so here, red is the adjective describing the noun.

87
00:04:06,470 --> 00:04:10,110
And finally JavaScript is, of course, the verb,

88
00:04:10,110 --> 00:04:12,910
like saying hide the paragraph.

89
00:04:12,910 --> 00:04:16,960
And so here we are doing something and so we have a verb.

90
00:04:16,960 --> 00:04:17,800
Okay?

91
00:04:17,800 --> 00:04:19,390
Does that make sense?

92
00:04:19,390 --> 00:04:21,140
Now, since we've been talking a lot

93
00:04:21,140 --> 00:04:24,580
about dynamic effects and web applications here,

94
00:04:24,580 --> 00:04:27,640
let's now actually take a look at a real example

95
00:04:27,640 --> 00:04:31,463
to make it even more clear what JavaScript is capable of.

96
00:04:33,060 --> 00:04:36,760
And so this is the Twitter web application on twitter.com

97
00:04:36,760 --> 00:04:38,440
and there is a lot happening

98
00:04:38,440 --> 00:04:41,480
as we open a profile page like this one.

99
00:04:41,480 --> 00:04:45,290
And so I thought that this was a very cool example.

100
00:04:45,290 --> 00:04:46,850
So right off the bat,

101
00:04:46,850 --> 00:04:48,080
you see that there are these

102
00:04:48,080 --> 00:04:50,450
two rotating spinners on the page,

103
00:04:50,450 --> 00:04:53,770
meaning that JavaScript is probably loading some data

104
00:04:53,770 --> 00:04:56,880
from the Twitter service in the background.

105
00:04:56,880 --> 00:04:59,150
Then, as the data arrives,

106
00:04:59,150 --> 00:05:01,370
JavaScript hides these spinners,

107
00:05:01,370 --> 00:05:03,703
and instead show us the loaded content.

108
00:05:04,570 --> 00:05:06,350
So this is a very cool example

109
00:05:06,350 --> 00:05:10,370
of manipulating styles and content, right?

110
00:05:10,370 --> 00:05:14,100
But there's also some simpler dynamic effect on this page,

111
00:05:14,100 --> 00:05:16,560
like JavaScript showing the tweet box

112
00:05:16,560 --> 00:05:18,530
whenever we hit the tweet button

113
00:05:18,530 --> 00:05:22,630
and then hides it as we click outside of that box.

114
00:05:22,630 --> 00:05:24,900
And finally, JavaScript also displays

115
00:05:24,900 --> 00:05:27,180
this really nice user information

116
00:05:27,180 --> 00:05:30,610
as we hover our mouse over any user on Twitter.

117
00:05:30,610 --> 00:05:34,440
And it probably also loads this data on the fly.

118
00:05:34,440 --> 00:05:37,040
So a lot of cool stuff going on here,

119
00:05:37,040 --> 00:05:39,640
and it's all powered by JavaScript.

120
00:05:39,640 --> 00:05:41,450
How cool is that?

121
00:05:41,450 --> 00:05:43,830
And in fact, by the end of the course,

122
00:05:43,830 --> 00:05:45,550
you will actually know how to use

123
00:05:45,550 --> 00:05:48,340
all of these techniques that we just saw here.

124
00:05:48,340 --> 00:05:50,040
And so I hope that this makes you

125
00:05:50,040 --> 00:05:53,143
even more excited about all the content ahead.

126
00:05:54,770 --> 00:05:56,670
Alright, now that we saw what

127
00:05:56,670 --> 00:06:00,730
JavaScript is really capable of, let's quickly recap,

128
00:06:00,730 --> 00:06:03,090
and also look at other cool stuff

129
00:06:03,090 --> 00:06:06,720
that we can build with the power of JavaScript.

130
00:06:06,720 --> 00:06:08,460
So as you already know,

131
00:06:08,460 --> 00:06:12,230
Java script allows us to add dynamic effects to pages.

132
00:06:12,230 --> 00:06:14,600
And in fact, to build entire

133
00:06:14,600 --> 00:06:17,220
web applications in the browser,

134
00:06:17,220 --> 00:06:19,920
and these applications feel almost like the apps

135
00:06:19,920 --> 00:06:23,960
that we use on our computers and phones every single day.

136
00:06:23,960 --> 00:06:25,550
So we can say that JavaScript

137
00:06:25,550 --> 00:06:28,160
is what made modern web development,

138
00:06:28,160 --> 00:06:30,380
and really the whole modern web itself

139
00:06:30,380 --> 00:06:32,750
possible in the first place.

140
00:06:32,750 --> 00:06:34,690
Now, if you're already somewhat familiar

141
00:06:34,690 --> 00:06:37,170
with the web development industry,

142
00:06:37,170 --> 00:06:39,830
you probably heard of modern JavaScript libraries

143
00:06:39,830 --> 00:06:44,830
and frameworks such as React, Angular or Vue, right?

144
00:06:45,180 --> 00:06:48,500
And if you didn't, that's absolutely no problem.

145
00:06:48,500 --> 00:06:51,650
All you need to know is that these are basically tools

146
00:06:51,650 --> 00:06:54,970
that make writing modern, large scale web applications,

147
00:06:54,970 --> 00:06:57,350
a lot easier and faster.

148
00:06:57,350 --> 00:07:00,270
Now what matters here, is that all these frameworks

149
00:07:00,270 --> 00:07:05,260
and libraries are still 100% based on JavaScript.

150
00:07:05,260 --> 00:07:07,980
And what this means is that you should become really,

151
00:07:07,980 --> 00:07:09,802
really good at JavaScript before learning

152
00:07:09,802 --> 00:07:13,100
and using any of these frameworks,

153
00:07:13,100 --> 00:07:16,000
and not just jump into your first framework

154
00:07:16,000 --> 00:07:19,880
after you know how to write, like, 10 lines of JavaScript.

155
00:07:19,880 --> 00:07:21,200
Okay?

156
00:07:21,200 --> 00:07:23,340
Also your library of choice

157
00:07:23,340 --> 00:07:26,670
might not always be as popular as it is today.

158
00:07:26,670 --> 00:07:30,450
And the best way to be prepared is, you guessed it,

159
00:07:30,450 --> 00:07:33,400
becoming really good at JavaScript,

160
00:07:33,400 --> 00:07:37,520
because then you can easily learn whatever is popular next.

161
00:07:37,520 --> 00:07:39,740
So no matter what anyone tells you,

162
00:07:39,740 --> 00:07:41,610
learning JavaScript properly

163
00:07:41,610 --> 00:07:44,650
is the single best investment that you can make

164
00:07:44,650 --> 00:07:47,980
in your web development career right now.

165
00:07:47,980 --> 00:07:50,950
Now the JavaScript language and the web browser

166
00:07:50,950 --> 00:07:53,260
are actually two separate things.

167
00:07:53,260 --> 00:07:55,500
And what that means is that JavaScript

168
00:07:55,500 --> 00:07:58,740
can also run outside of web browsers.

169
00:07:58,740 --> 00:08:02,970
For example, it's possible to use JavaScript on a web server

170
00:08:02,970 --> 00:08:06,770
using a very popular technology called Node.js,

171
00:08:06,770 --> 00:08:09,430
which doesn't need any browser at all.

172
00:08:09,430 --> 00:08:13,330
And this allows us to create so-called backend applications,

173
00:08:13,330 --> 00:08:16,390
which are simply applications that run on a web server

174
00:08:16,390 --> 00:08:20,150
and interact with databases and stuff like that.

175
00:08:20,150 --> 00:08:23,450
On the other hand, when we use JavaScript in the browser,

176
00:08:23,450 --> 00:08:27,000
we create so-called front end applications.

177
00:08:27,000 --> 00:08:30,040
So in this course, we will learn the ins and outs

178
00:08:30,040 --> 00:08:32,410
of the JavaScript language itself,

179
00:08:32,410 --> 00:08:35,710
and of course also how to use it in the browser

180
00:08:35,710 --> 00:08:38,400
in order to create all these amazing effects

181
00:08:38,400 --> 00:08:40,260
that we've been talking about.

182
00:08:40,260 --> 00:08:41,530
So basically we're going to be

183
00:08:41,530 --> 00:08:44,720
building front-end web applications.

184
00:08:44,720 --> 00:08:45,730
And in the future,

185
00:08:45,730 --> 00:08:48,860
I might also add a section about Node.js

186
00:08:48,860 --> 00:08:50,380
at the end of this course,

187
00:08:50,380 --> 00:08:53,410
so that you can get a sense of how we can use JavaScript

188
00:08:53,410 --> 00:08:56,573
outside of the browser environment as well.

189
00:08:57,550 --> 00:08:58,383
All right.

190
00:08:58,383 --> 00:09:00,233
And now, just to finish, I want to mention

191
00:09:00,233 --> 00:09:03,110
that we can actually also use JavaScript

192
00:09:03,110 --> 00:09:06,070
to build kind of native mobile applications,

193
00:09:06,070 --> 00:09:08,820
as well as native desktop applications

194
00:09:08,820 --> 00:09:12,500
for any phone and computer operating system out there.

195
00:09:12,500 --> 00:09:15,600
That's because of modern tools like React Native,

196
00:09:15,600 --> 00:09:19,350
the Ionic framework and tools like Electron.

197
00:09:19,350 --> 00:09:22,500
These have completely changed the whole development industry

198
00:09:22,500 --> 00:09:24,070
over the last couple of years,

199
00:09:24,070 --> 00:09:27,960
making things possible that were never possible before.

200
00:09:27,960 --> 00:09:30,900
So as you can see, there's almost nothing

201
00:09:30,900 --> 00:09:33,070
that you can't build after becoming

202
00:09:33,070 --> 00:09:35,020
really good at JavaScript,

203
00:09:35,020 --> 00:09:39,260
which if you think about it, is really kind of mind-blowing.

204
00:09:39,260 --> 00:09:43,233
It's just amazing, because the possibilities are so endless.

205
00:09:44,200 --> 00:09:45,033
Okay.

206
00:09:45,033 --> 00:09:46,540
And now to finish this lecture,

207
00:09:46,540 --> 00:09:49,840
I want to briefly talk about JavaScript releases

208
00:09:49,840 --> 00:09:52,400
or versions, as you might call them.

209
00:09:52,400 --> 00:09:55,120
We will come back to this topic by the end of the section

210
00:09:55,120 --> 00:09:57,240
because it's super important,

211
00:09:57,240 --> 00:10:00,360
but it's also a good idea to get a first overview

212
00:10:00,360 --> 00:10:03,470
of JavaScript releases at this point.

213
00:10:03,470 --> 00:10:06,140
Anyway, to make a long story short,

214
00:10:06,140 --> 00:10:10,280
there has been a huge update to the language in 2015,

215
00:10:10,280 --> 00:10:13,020
which is officially called ES2015,

216
00:10:13,020 --> 00:10:15,440
but most people just call it ES6,

217
00:10:15,440 --> 00:10:19,100
simply because it was released after ES5.

218
00:10:19,100 --> 00:10:23,090
And by the way, E. S stands for ECMAScript.

219
00:10:23,090 --> 00:10:25,180
Now after ES2015,

220
00:10:25,180 --> 00:10:27,410
there is now a yearly new release

221
00:10:27,410 --> 00:10:29,940
with a couple of new JavaScript features.

222
00:10:29,940 --> 00:10:32,870
In all of these new releases or versions,

223
00:10:32,870 --> 00:10:37,870
starting from ES2015, is what we call modern JavaScript.

224
00:10:38,100 --> 00:10:40,530
But, why am I telling you all this?

225
00:10:40,530 --> 00:10:42,870
Well, it's simply because in this course,

226
00:10:42,870 --> 00:10:44,890
I'm gonna teach you a modern JavaScript,

227
00:10:44,890 --> 00:10:46,400
right from the beginning.

228
00:10:46,400 --> 00:10:49,860
And I wanted to make that very clear right from the start.

229
00:10:49,860 --> 00:10:51,840
However, I'm also convinced that

230
00:10:51,840 --> 00:10:56,840
you need to understand what came before ES2015, so ES5.

231
00:10:57,360 --> 00:11:01,750
And so I will also show you what's important of ES5.

232
00:11:01,750 --> 00:11:03,880
The reason for that is in a complete video

233
00:11:03,880 --> 00:11:07,690
about JavaScript releases at the end of this section,

234
00:11:07,690 --> 00:11:11,830
because now I no longer want to bore you with theory.

235
00:11:11,830 --> 00:11:15,383
So instead, let's now finally get started.

