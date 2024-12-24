# Makefile

# 编译参数
CC = gcc
CFLAGS = -Wall -g
# 源文件和目标文件
SRCS = $(wildcard *.c)
OBJS = $(patsubst %.c, %.o, $(SRCS))
# 可执行文件
TARGET = main
# 编译规则
$(TARGET): $(OBJS)
	$(CC) $(CFLAGS) -o $@ $^
%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@
# 清理规则
clean:
	rm -f $(OBJS) $(TARGET)
# 运行规则
run: $(TARGET)
	./$(TARGET)
