# Databases

<h3>Courier service</h3>
<p><strong>Task</strong>:<br />There is a company delivering orders - a Courier Service.</p>
<ol>
<li>The order table contains information about the order that the courier will deliver.<br />FIO &ndash; Recipient's full name;<br />address &ndash; delivery address;<br />kurier &ndash;the code of the employee who delivered the shipment, null by default;<br />price &ndash; shipping cost;</li>
<li>The order tracking trace table contains the history of various order statuses.<br />state &ndash; order status code: 1 &ndash; New; 2 &ndash; accepted to the warehouse; 3 &ndash; delivered; 4 &ndash; not delivered<br />datetime &ndash; date and time of the status setting;</li>
<li>The courier table contains information about employees (couriers and managers).<br />FIO &ndash; Courier's full name<br />manager &ndash; the courier has a manager code, null by default</li>
<p>Display all delivered orders that were not accepted to the warehouse.<br />Bring out the couriers who delivered more orders than their managers.<br />Output managers and the cost of all orders delivered by their couriers, for the last month.<br />Output managers who have no more than three couriers.<br />Display the orders and the last status set for it. Leave only statuses in the report: new and accepted to the warehouse.</p>
<p><strong>Manual</strong>:<br />I started the database in the Ubuntu 20.04 terminal.</p>
<ol>
<li>To work in the system, you need to install postresql in the terminal in this way:
<br />u@uv:~$ sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" &gt; /etc/apt/sources.list.d/pgdg.list'<br />u@uv:~$ wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -<br />u@uv:~$ sudo apt-get update<br />u@uv:~$ apt list | grep postgresql<br />u@uv:~$ sudo apt-get -y install postgresql<br />u@uv:~$ systemctl status postgresql
<li>To start the program, you need to enter the following commands in the terminal:
<br />:~$ sudo mysql -u root<br />mysql&gt; CREATE DATABASE testbdserver;<br />mysql&gt; \q<br />:~$ mysql -u root -p testbdserver &lt; data-dump0.sql
<br />:~$ sudo su - postgres<br />postgres@uv:~$ psql
</li>
</ol>
<p><strong>Tools</strong>:</p>
<ol>
<li>Ubuntu 20.04</li>
<li>mysql</li>
</ol>