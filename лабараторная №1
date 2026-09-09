import turtle

def perform_switch_case(state, t, step, up_count):
    if state == "UP":
        up_count += 1
        t.setheading(90)
        t.forward(50)

        if up_count == 3:
            return "STOP", step, up_count

        return "RIGHT", step, up_count

    if state == "RIGHT":
        t.setheading(0)
        t.forward(50)

        if step == 1:
            state = "DOWN"
        elif step == 2:
            state = "UP"
        elif step == 3:
            state = "DOWN"
        elif step == 4:
            state = "UP"
        else:
            state = "STOP"

        step += 1
        return state, step, up_count

    if state == "DOWN":
        t.setheading(270)
        t.forward(50)
        return "RIGHT", step, up_count

    return state, step, up_count


def draw():
    t = turtle.Turtle()
    t.speed(3)
    t.width(3)

    curr_state = "UP"
    step = 1
    up_count = 0

    while curr_state != "STOP":
        curr_state, step, up_count = perform_switch_case(curr_state, t, step, up_count)

    turtle.done()


if __name__ == "__main__":
    draw()
