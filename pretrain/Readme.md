#### 在pretrain下生成预训练模型 
1.通过datapro.py对数据进行处理，每段话从中间断开分成两句话，每段话之间用空白行隔开，针对ccl2019幽默度比赛task1和task2，生成cclhumortask12_bert.txt，以及加上去年ccl幽默度得比赛数据和我们自行对task1数据翻译生成得到得数据，生成了cclhumortaskalldata_bert.txt 

2.通过运行prepocess.py对cclhumortask12_bert.txt和cclhumortaskalldata_bert.txt这两份数据分别在chinese_L-12_H-768_A-12、bert_wwm、bert_wwm_ex 、roberta四个中文预训练模型处理得到了8个文件夹 
  pytorchmodeltask12_bert_1005  
  pytorchmodeltask12_roerta_1005  
  pytorchmodeltask12_wwm_1005  
  pytorchmodeltask12_wwm_ex_1005  
  pytorchmodeltaskalldata_bert_1005  
  pytorchmodeltaskalldata_roerta_1006  
  pytorchmodeltaskalldata_wwm_1005  
  pytorchmodeltaskalldata_wwm_ex_1005  

3.运行finetune_on_pretrain.py针对上述生成得8个文件夹分别进行预训练，为了文件结构清晰，最终生成的pytorch预训练模型也放在了上面8个文件夹中 
