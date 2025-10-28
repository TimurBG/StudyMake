# Makefile для проекта Kazino-Royal

.PHONY: all debug release clean

# Переменные для флагов компиляции
RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall

# Переменные для имён исполняемых файлов
RELEASE_EXEC  = Kazino-Royal
DEBUG_EXEC    = Kazino-Royal-dbg

# Переменная для исходного файла
SOURCE = Kazino-Royal.cpp

# Целевая сборка по умолчанию (выполняет debug и release)
all: debug release

# Правило для сборки отладочной версии
debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): $(SOURCE)
	g++ $(DEBUG_FLAGS) $(SOURCE) -o $(DEBUG_EXEC)

# Правило для сборки релизной версии
release: $(RELEASE_EXEC)

$(RELEASE_EXEC): $(SOURCE)
	g++ $(RELEASE_FLAGS) $(SOURCE) -o $(RELEASE_EXEC)

# Правило для очистки (удаляет исполняемые файлы)
clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)
