<!DOCTYPE html>
<html lang="en">

<body>

<div id="main">

/**
 * Iterates over a list with a function asynchronously
 * @param {Array} list - the list of Items to be iterated over
 * @param {Function} iterateFunction - the function to be performed on each element of the list
 * @param {callbackFunction} callback - call back after finished.
 */
 <code>
function iterate(list, iterateFunction,callback){
    
    var completed = 0;

    function done(){
        completed++;
        if(completed == list.length){
            callback();
        }
    }

    for(var i = 0;i&lt; list.length;i++){
        iterateFunction(list[i],done);
    }
}

module.exports = iterate;</code>
        </article>
    </section>




</div>


<footer>
    Documentation generated by <a href="https://github.com/jsdoc3/jsdoc">JSDoc 3.5.5</a> on Sat Sep 16 2017 11:14:23 GMT-0500 (Central Daylight Time)
</footer>

</body>
</html>
