메인화면에 페이징 목록 만들고 GetMapping하기

페이징처리는 사용자가 어떤페이지번호를 클릭하냐에 따라 데이터가 변하기 때문에


@GetMapping("/paging")
    public String paging(Model model){

    }
page라는 파라미터를 넘겨와야하기 때문에 @RequestParam 활용
  @GetMapping("/paging")
    public String paging(Model model
    ,@RequestParam(value="page",required = false,defaultValue ="1") int page){
      
    }

value는 파라미터이름 표현 , required=false는 필수가 아니다 (그러므로 에러가발생하지않음) ->없으면 기본값으로 1페이지로 하기위해 defaultValue ="1"을 사용함

고로 만약 page값이 없다면  1로 값이있다면 뒤에 int page를 써서 page를 불러오게끔 설정


 
