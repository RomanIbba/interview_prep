## Interview question for senior level developer
**Create a game such that:**
- Players p1 and p2 start at health = 100
- Each turn, pick a random power [10, 20, 30, 40]
- During that turn player A >> obtains power 10 >> attacks player B >> player B health reduces >> 90
- Looser dies first. Print all the actions that occur

### Here is the solution I came up with in Ruby, feel free to practice and impliment in the language familiar to you:

```ruby
class Player
  attr_accessor :name, :health, :aliveStatus

  def initialize
    @playerName = ""
    @health = 100
    @aliveStatus = true
  end

  def update_health (attack)
    @health -= attack
    @aliveStatus = false if @health <= 0
  end
end

def turn(a, b)
  attackPower = rand(1..4) * 10
  b.update_health(attackPower)
  puts "#{a.name} attacks #{b.name} with #{attackPower}AP"
  puts "#{b.name} now has #{b.health}"
end

name1 = "Player A"
name2 = "Player B"

p1 = Player.new
p1.name = name1
p2 = Player.new
p2.name = name2

while p1.aliveStatus && p2.aliveStatus do
  turn p1, p2
  if p2.aliveStatus
    turn p2, p1
    puts "#{p2.name} wins !!!" unless p1.aliveStatus
  else
    puts "#{p1.name} wins !!!"
  end
end
```

*Here is the output I received*
```sh
Player A attacks Player B with 10AP
Player B now has 90
Player B attacks Player A with 20AP
Player A now has 80
Player A attacks Player B with 10AP
Player B now has 80
Player B attacks Player A with 30AP
Player A now has 50
Player A attacks Player B with 20AP
Player B now has 60
Player B attacks Player A with 30AP
Player A now has 20
Player A attacks Player B with 10AP
Player B now has 50
Player B attacks Player A with 10AP
Player A now has 10
Player A attacks Player B with 30AP
Player B now has 20
Player B attacks Player A with 40AP
Player A now has -30
Player B wins !!!
```

>Note: The use of a random number generator means that the out put will varry every run and can't be predicted.
