
# UI Libraries

1. [ace](https://ace.c9.io) - Code editor for 110+ languages and matches the features/performance of Sublime, Vim and TextMate etc.

2. [prettify](https://github.com/google/code-prettify) - Pretty-printer for code (not an editor). Easy to use.

3. [w2ui](http://w2ui.com/web/demo) - Most common UI widgets: Layout, resizable-grid, sidebar, tabs, toolbar, popup etc.

4. [jsonform](https://github.com/joshfire/jsonform) - Creates forms by writing just a JSON schema - Handles code-editors, WYSIWYG editors etc.

5. [underscore.js](http://underscorejs.org/) - Great collection of utilities. Html-escaping/unescaping, templates, `isNull`, `isUndefined` etc.

6. [spectrum](http://bgrins.github.io/spectrum/) - Color picker.

7. [tablesorter](https://mottie.github.io/tablesorter/docs/) - Table that can be sorted by clicking on column-headers. Lots of plugins.

8. [notify.js](https://notifyjs.com/) - Eases notification creation.

9. [json-formatter.js](http://azimi.me/json-formatter-js/) - Cool JSON formatter with expandable json-trees.

10. [json-query](https://www.npmjs.com/package/json-query) - Ability to query JSON data objects.

11. [Font Awesome](http://fontawesome.io/) - Free library with 675 free icons, very easy to use.

12. [moment js](http://momentjs.com/docs/#/parsing/) - Free library for working with dates in JavaScript

13. [multiple dropdown selector](http://wenzhixin.net.cn/p/multiple-select/docs/)


# Time-series Databases

1. [List of all timeseries databases](http://www.erol.si/2015/01/the-complete-list-of-all-timeseries-databases-for-your-iot-project/)

2. [OpenTS-DB to Kairos-DB](http://www.erol.si/2015/01/why-i-switched-from-opentsdb-to-kairosdb/)





# Graphs for metrics

1. [Grafana](http://docs.grafana.org/installation/)

2. [Feed Grafana from Graphite](http://docs.grafana.org/datasources/graphite/)




# Monitoring

1. [Several ways to monitor your linux machine](http://www.netinstructions.com/how-to-monitor-your-linux-machine/)




# Java

1. [Java Decompiler](https://github.com/java-decompiler/jd-gui) - JD-GUI is a standalone graphical utility that displays Java source codes of ".class" files

2. [DoubleBraceInitialization](http://wiki.c2.com/?DoubleBraceInitialization) - Initialise collections during declaration. Example:
```java
Map<String, List<String>> TWEETERS_DB = new HashMap<String, List<String>>() {{
    put("foo.com/blog/1", Arrays.asList("sally", "bob", "tim", "george", "nathan"));
    put("engineering.twitter.com/blog/5", Arrays.asList("adam", "david", "sally", "nathan"));
    put("tech.backtype.com/blog/123", Arrays.asList("tim", "mike", "john"));
  }};
```
The first brace creates a new AnonymousInnerClass, the second declares an **instance initializer block** that is run when the anonymous inner class is instantiated.
Disadvantages:
- If you serialise the collection you will also serialise everything in the outer class.
- Can fail comparison by equals() method if class-equality is checked in the equals() method.


# Linux

1. [Linux ate my ram.com](http://www.linuxatemyram.com/play.html) - Magic of disk caching. Counted under used but still available to the applications for their own use.

2. [tc - Traffic Control](https://linux.die.net/man/8/tc) - Controls traffic on a port by limiting bandwidth, filtering by policies or re-scheduling-to-avoid-bursts.

3. [tcpdump](http://www.tcpdump.org/tcpdump_man.html) - Used to analyze network traffic in conjunction with [wireshark](https://en.wikipedia.org/wiki/Wireshark)

4. [seq](https://linux.die.net/man/1/seq) - Generate sequence numbers

5. [dd](http://ss64.com/bash/dd.html) - Create files with random data, wipe hard disk, convert and copy files

6. [stress-ng](https://websetnet.com/how-to-stress-test-cpu-and-memory-vm-on-a-linux-and-unix-with-stress-ng/) - Stress test cpu, memory, drive, I/O, sockets and many more resources on Linux

7. [sar -q \<interval\> \<count\>](https://linux.die.net/man/1/sar) - Report queue length and load averages for the CPU every given interval and for a given number of counts. One of the output parameters - `runq-sz`  is the number of kernel threads in memory that are waiting for a CPU to run. **Typically, this value should be less than 2. Consistently higher values mean that the system might be CPU-bound.**

8. [Tilda Dot: (~.)](https://www.cyberciti.biz/faq/openssh-linux-unix-osx-kill-hung-ssh-session/) - Disconnects an SSH session. Useful to kill a hung SSH session and get back to terminal.

9. [dmesg -T](http://man7.org/linux/man-pages/man1/dmesg.1.html) - **D**river **mes**sa**g**es - View errors reported by device drivers to see if there are any hardware failures.


# Tools and software

1. [Chrome Sense Plugin](https://chrome.google.com/webstore/detail/sense-beta/lhjgkmllcaadmopgmanpapmpjgmfcfig?hl=en) - A JSON aware developer console to ElasticSearch

2. [Elastic Search Toolbox](https://chrome.google.com/webstore/detail/elasticsearch-toolbox/focdbmjgdonlpdknobfghplhmafpgfbp?hl=en-US) - Query Builder for ElasticSearch


# Vim plugins and scripts

1. [nerdtree](https://github.com/scrooloose/nerdtree) - File explorer alongside vim

2. [vim-nerdtree-tabs](https://github.com/jistr/vim-nerdtree-tabs) - Helps to get a single nerdtree for all tabs

3. `nmap gc :NERDTreeFind<CR>` - locate current file in the NERDTree using gc

4. `nmap gg <C-w><C-w>` - Map gg to Ctrl-w + Ctrl-w - Helps to cycle between NERDTree window and the editor using gg

5. `gt` - cycle between the tabs


# Client-Server

1. [Does ServerSocket.accept() return socket on arbitrary port?](http://stackoverflow.com/questions/17731247/does-serversocket-accept-return-socket-on-arbitrary-port) - No. The `Socket` returned by ServerSocket.accept() is bound to the same port as the `ServerSocket` but it also contains information about the client's port number and that information is enough to disambiguate the target-socket of messages coming to the server.


# Load testing

1. CPU
```bash
sysbench --test=cpu --cpu-max-prime=100000 run
sysbench --test=cpu --cpu-max-prime=100000 --num-threads=16 run
```

2. Memory
```bash
sysbench --test=memory --num-threads=16 --memory-block-size=4K --memory-total-size=100G --memory-oper=write run
sysbench --test=memory --num-threads=16 --memory-block-size=4K --memory-total-size=100G --memory-oper=read run
```

3. Network

See [this tutorial](https://www.davidklee.net/2015/10/13/network-throughput-testing-with-iperf3/) or [this tutorial](http://www.e2college.com/blogs/linux/linux_networking/iperf3_tutorial.html).
Can be installed through yum
```bash
yum install iperf3
```

4. Disk IO

```bash
sysbench --test=fileio --file-total-size=300G --file-num=16 prepare
for each in 16 32 64; do sysbench --test=fileio --file-total-size=300G --file-test-mode=rndrd --max-time=240 --max-requests=0 --file-block-size=4K --file-num=16 --num-threads=$each run; sleep 10; done
```


# iTerm2
[iTerm2](https://www.iterm2.com/index.html) is a versatile terminal with lots of features.  
Some of its most useful Mac shortcuts are:

1. `cmd-d`: Split pane veritcally.
2. `cmd-shift-d`: Split pane horizontally.
3. `cmd-alt-<arrow-keys>`: Navigate among split panes.
4. `cmd-shift-enter`: Maximize current pane and hide all the others.
5. `cmd-alt-i`: Send input to all panes in current tab.
6. `cmd-alt-shift-i`: Send input to only the current pane.
7. `cmd-;`: Autocomplete by matching words in current scrollback.
8. `cmd-shift-h`: Show history of copied text.
9. `cmd-alt-e`: Search in all tabs at once.
10. `cmd-alt-b`: Shows state of screen at various points in the past. Navigate time by right/left arrow keys.
11. Click once and then `shift-click` at other place to select and copy without dragging.
12. `cmd-t`: Opens a new Tab which you can split in its own panes.
13. `cmd-<number>`: Takes you directly to the tab with that number.
14. `Preferences -> Profiles -> Window -> Transparency`: Increase some transparency to see background windows. Very useful.
