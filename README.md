## getCategories?.(catrgoires)

Опциональная функция

## Типизирум опциональный пропсы

type CategoriesProps = {
value: number;
onChangeCategory?: (idx: number) => void;
};

Знак вопроса если надо пропсы сделать опциональными

## // @ts-ignore
Если надо игнорировать код
dispatch(
      fetchPizzas({
        sortBy,
        order,
        category,
        search,
        currentPage,
      })
    );

## Если не работает event listener

  React.useEffect(() => {
    const handleClickOutside = (event: MouseEvent) => {
      const _event = event as MouseEvent & {
        path: Node[];
      };
      if (sortRef.current && !_event.path.includes(sortRef.current)) {
        setOpen(false);
      }
    };

    document.body.addEventListener("click", handleClickOutside);

    return () => document.body.removeEventListener("click", handleClickOutside);
  }, []);


