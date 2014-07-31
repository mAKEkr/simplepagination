CodeIgniter Simple Pagination Library
================

CodeIgniter의 Pagination을 개발자들이 간단하게 사용하기 위하여, 그리고 사용자에게 간단하게 제공하기 위하여 만든 라이브러리입니다. 페이지네이션 형식은 일반 그누보드 및 제로보드와 같은 공개형 보드 프로그램들에서 사용되어오던 형식과 동일하며, 기존에 사용해오던 CodeIgniter의 Pagination 라이브러리와도 어느정도 호환성이 확보되어있습니다.

##설치법 및 사용법
설치법과 사용법은 다음과 같습니다.

1. CodeIgniter의 Application/Libraries 폴더에 Simplepagination.php를 넣는다.
2. Controller의 안에 $this->load->library('simplepagination'); 로 라이브러리를 불러옵니다.
3. SimplePagination라이브러리를 불러오기 전, 설정을 생성합니다(설정은 array로 전달합니다. 아래의 설정을 참고하세요)
4. $this->SimplePagination->getPagination($options) 로 불러옵니다. 반환되는 값은 string입니다.

##설정
설정은 배열로 전송해야하며, 다음과 같은 key값을 넣어주셔야합니다.

- **url**(필수) : 페이지가 오기 전까지의 주소입니다. (예를 들어 `(url)/lists/boardid/(pageno)` 의 형식으로 되어있다면, `(url)/lists/boardid)` 까지입니다. 마지막의 `/` 는 꼭 지워주셔야 합니다.
- **current_page**(필수) : 현재 페이지의 값입니다.
- **last_page**(필수) : 마지막 페이지의 값입니다.
- **suffix**(선택) : url이 작성된 뒤에 자동으로 삽입될 값입니다.(검색이나 url writing방식이 다를경우 유용합니다)
