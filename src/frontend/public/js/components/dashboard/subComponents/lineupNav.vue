<template>
    <div class="lineup-nav">
        <ul>
            <li><a href="/dashboard/lineup"><span class="fa fa-eye"></span> Line-up</a></li>
            <li><a href="/dashboard/questions"><span class="fa fa-comment"></span> Questions</a></li>
            <li><a href="/dashboard/feedback"><span class="fa fa-question-circle"></span> Feedback</a></li>
        </ul>
    </div>
</template>
<style scoped>
.lineup-nav{
  padding: 1px 0 10px 0;
  float: right;
}
.lineup-nav ul{
  list-style: none;
  padding: 0;
  text-align: center;
}
.lineup-nav ul li{
  display: inline-block;
  padding: 5px;
}
.lineup-nav ul li a{
  color: var(--upnext-input-addon);
  font-size: 1em;
  text-decoration: none;
  transition: .3s;
}
.lineup-nav ul li a:hover{
  color: var(--upnext-blue)
}

.lineup-nav ul li .active{
  color: var(--upnext-blue)
}
</style>


