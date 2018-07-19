# TimerTask
A JavaScript TimerTask lib.

## About
This is a js timer for auto run tasks.
## API
	<script>
		// 1. Create a new Instance;
		var task = new TimerTask();
		// 2. Start run timer;
		task.start();
		// 3. Add task
		var id = task.setTask(time, doFunction,param)
		// 4. Remove task
		task.removeTask(id)
		//5. Get task(s)
		task.getTask([time])
		//6. Stop run timer
		task.stop();		
	</script>
	
## Usage

	<script src="TimerTask.js"></script>
	<script>
		$(function() {
			var task = new TimerTask();
			task.start();
			console.log((new Date()).getTime())
			task.setTask(1,function(){
				console.log((new Date()).getTime())
			});
			task.setTask(2,function(){
				console.log((new Date()).getTime())
			});
			task.setTask(3.5,function(a,b){
				console.log(a,b)
			},"ar1","ar2");

		});
	</script>

