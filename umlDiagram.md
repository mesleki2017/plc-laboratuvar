@startuml
package "PLC Hardware" {
 [S7-1500] --> [Remote IO] 
  [Delta HMI] --> [S7-1500]
 [Remote IO] --> [IO Cards]
 [S7-1200]
 
 
}

node "Hydraulic" {
frame "Driver"{
  [SINAMICS S120/G120]
}
frame "mechanical"{
[hydraulic pump motor]
[hydraulic pump]
[hydraulic valves]
[Hydraulic cylinder]
}

}

node "Sensors"{
[Limit Switches]
[pressure sensor]
[vibration sensor]
[temperature sensor]
}


database "MySql" {
  folder "This is my folder" {
    [Folder 3]
  }
  frame "Foo" {
    [Frame 4]
  }
}


[S7-1500] --> [S7-1200]
@enduml