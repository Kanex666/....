# ....
...  
const  { execShellCommand , greenLog , redLog }  =  yêu cầu ( ' ../helper.js' ) ;

mô-đun . xuất khẩu  =  {
	từ khóa : [ 'clone' ,  'c' ] ,
	thông số : [ ] ,
	description : 'Clone kb2abot phien ban moi nhat ve duong dan ~ / kb2abot' ,
	fn : async  ( )  =>  {
		thử  {
			bàn điều khiển . log ( 'Dang tai phien ban moi nhat cua kb2abot ve may...' ) ;
			await  executeShellCommand ( 'git clone https://github.com/kb2ateam/kb2abot' ) ;
		}  bắt  ( e )  {
			redLog ( 'Da gap loi trong luc tai kb2abot' ) ;
			ném  e . tin nhắn ;
		}
		greenLog ( 'Da tai kb2abot ve thanh cong!' ) ;
	}
} ;
