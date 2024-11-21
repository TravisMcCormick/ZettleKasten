
``` dataviewjs
const allTasks = dv.current().file.tasks;

dv.paragraph(`Number of tasks found: ${allTasks.length}`);

allTasks.forEach(task => {
  dv.paragraph(`Task: "${task.text}", Subpath: "${task.section?.subpath}"`);
});

const quadrants = {
  "Urgent Important": [],
  "Not Urgent Important": [],
  "Urgent Not Important": [],
  "Not Urgent Not Important": []
};

for (const task of allTasks) {
  const subpath = task.section?.subpath;
  if (subpath && quadrants.hasOwnProperty(subpath)) {
    quadrants[subpath].push(task);
  } else {
    dv.paragraph(`No quadrant match found for task "${task.text}" with subpath "${subpath}"`);
  }
}

function renderTasks(tasks) {
  if (!tasks || tasks.length === 0) {
    return "<li>No tasks</li>";
  }
  return tasks.map(task => `<li>${task.text}</li>`).join("");
}

dv.container.innerHTML = `
<style>
  .matrix-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    text-align: center;
  }
  .matrix-cell {
    border: 1px solid #444;
    padding: 10px;
    border-radius: 5px;
    background: #222;
    color: #ddd;
  }
  .matrix-cell h3 {
    margin: 5px 0;
    font-size: 1.2em;
    color: #42a5f5;
  }
  .matrix-cell ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }
</style>
<div class="matrix-container">
  <div class="matrix-cell">
    <h3>Do</h3>
    <ul>${renderTasks(quadrants["Urgent Important"])}</ul>
  </div>
  <div class="matrix-cell">
    <h3>Plan</h3>
    <ul>${renderTasks(quadrants["Not Urgent Important"])}</ul>
  </div>
  <div class="matrix-cell">
    <h3>Delegate</h3>
    <ul>${renderTasks(quadrants["Urgent Not Important"])}</ul>
  </div>
  <div class="matrix-cell">
    <h3>Schedule</h3>
    <ul>${renderTasks(quadrants["Not Urgent Not Important"])}</ul>
  </div>
</div>
`;
```

# Tasks:

## Urgent Important
- [ ] Task 1
## Not Urgent Important
- [ ] Task 2
## Urgent Not Important
- [ ] Task 3
## Not Urgent Not Important
- [ ] Task 4

*Give the table a second to load on startup or after adding a new task*
*If you change the name of the file, open the dataviewjs code and then close it to fix*