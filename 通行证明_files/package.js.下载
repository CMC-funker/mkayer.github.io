            var data = "";
			var wdm_qingjia_state = "已同意请假";
			srSetDataValue(data.wdmQingJia);
			srSetDataValue(data.dzxjStudentInfo);
			tongxingstate=wdm_qingjia_state;
			if(true){
				var ktx = "<img src='./通行证明_files/dui.png' />";
				$("#tximg").html(ktx);
				var txg ="green";
				txz ="<h3  style='text-align:center; color:" + txg + "'>允许通行</h3>"
				$("#txzm").html(txz);
				
			}else if(data.wdmQingJia.wdm_qingjia_state =="已同意请假" && data.txzt=="N"){
				var ktx = "<img src='./通行证明_files/cuo.png' />";
				$("#tximg").html(ktx);
				var txg ="green";
				var txgl ="red";
				txz ="<h3  style='text-align:center; color:" + txgl + "'>不允许出校门</h3><br/><h3  style='text-align:center; color:" + txg + "'>只允许进入校门，待返校确认</h3>"
				$("#txzm").html(txz);
				
			}else if(data.wdmQingJia.wdm_qingjia_state =="返校确认完成"){
				var bktx = "<img src='./通行证明_files/cuo.png' />";
				$("#tximg").html(bktx);
				var tx ="red";
				txjz ="<h3  style='text-align:center; color:" + tx + "'>已确认返校，不可进出校门</h3>"
				$("#txzm").html(txjz);
			}
			var splstr="";
			
			if(null==data.srwfsteplist||data.srwfsteplist.length==0){
				$("#shenpidivs").hide();
			}
			mui.each(data.srwfsteplist,function(i,srWfStep){
				splstr += "<tr>";
				splstr += "<td>" + srWfStep.state + "</td>";
				//splstr += "<td>" + srWfStep.starttime + "</td>";
				//splstr += "<td>" + srWfStep.finishtime + "</td>";
				splstr += "<td>" + srWfStep.owneruser + "</td>";
				splstr += "<td>" + srWfStep.appovestatus + "</td>";
				splstr += "<td>" + srWfStep.memo + "</td>";
				splstr += "</tr>";
			});
			$("#shenpiliuchen").html(splstr);
			
			
			
			srToastHide();