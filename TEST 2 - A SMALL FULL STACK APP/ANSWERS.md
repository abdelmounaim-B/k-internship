for the sorting, after trying to implement the feature here is what i did so far :   


const handleSort = async () => {
    const loadNotebooks = async () => {
      const loadedNotebooks = await api.getNotebooks();
      console.log(loadedNotebooks)
      // const SortedList = loadedNotebooks.sort((a, b) => a.title - b.title);
      const SortedList = loadedNotebooks.sort((a, b) => a.updatedAt - b.updatedAt);
      console.log(SortedList)
      // const SortedList = loadedNotebooks.sort();
      setNotebooks(SortedList);
    };
  };

  i tryed to sort using title and last updated and it didnt work somhow, even the cosole.log i couldnt see it on the console, so i tryed and thats what i came up with.