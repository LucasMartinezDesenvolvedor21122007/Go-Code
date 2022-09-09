Package main
import "fmt"
var battle = make(chan string)

func warrior(name string, done chan struct{}){
	select{
	case oponent := <-battle:
		fmt.printlf("%s beat %s/n", name, oponent)
		case battle <- name
		// eu perdi :/
	}
	done<- struct{}{}
	}

func main() {
	done:= make(chan struct{})
	langs := []string{"Go", "C", "C++", "Java", "Perl", "Python"}
for_, l:range langs{Go warrior(L, done)}
for_= range langs{ <-done}
}
