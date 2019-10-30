# Hm7

class Task:

    def __init__(self, name, deadline, level):
        self.name = name
        self.deadline = deadline
        self.level = level
        
class TaskManager:   

    def addTask(self, task):
        self.tasks.append(task)
    def __init__(self):
        self.tasks = []
    def printAllTasks(self):
        for task in self.tasks:
            print(task.name, task.deadline)

    def printTheMostImportantTasks(self):
        max = 0
        for task in self.tasks:
            if task.level > max:
                max = task.level
                name = task.name
                deadline = task.deadline
        print(name, deadline)


def main():
    auaTasks = TaskManager()
    personalTasks = TaskManager()
    t = Task("Calculus HW", "30/10/19", 10)
    auaTasks.addTask(t)
    t = Task("Get Ready for Midterms", "01/10/19", 5)
    auaTasks.addTask(t)
    t = Task("Pay Cellphone Bill", "31/10/19", 2)
    personalTasks.addTask(t)
    t = Task("Mothers gift for birthday", "21/05/19")
    personalTasks.addTask(t)
    personalTasks.printTheMostImportantTasks()


main()
