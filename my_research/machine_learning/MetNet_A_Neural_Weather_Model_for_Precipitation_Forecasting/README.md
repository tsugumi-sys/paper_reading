# MetNet: A Neural Weather Model for Precipitation Forecasting

Casper Kaae et al.

[Paper PDF](https://arxiv.org/abs/2003.12140)

## Motivation

- Weather forecasting is suitable for DNN due to vast amounts of continuously collected data and a rich spatial and temporal structure that presents long range dependencies.
- Weather prediction model should be able to reproduce probablistic outputs and represent uncertainty in the predictions like  (Krizhevsky et al., 2012; He et al., 2016; Vaswani et al.,2017).
- MetNet predict the rate of the precipitation with the 1km^2 spatial and 2 minutes temporal resolution using NN and self-annotation.

## Method

- We cast precipitation forecasting as a structured prediction problem where the output comes in the form of a three-dimensional tensor [time, location, rate of thr precipitaion.]
- Target precipitation rates are estimated by the Multi Radar Multi Sensor (MRMS) ground based radars as a function of the returned radar echoes  (Zhang et al., 2016). The spatial size of MRMS data is about 1km^2.
- MetNet use CNN for spatial downsampler, ConvLSTM for temporal encoder and self-attension blocks for spatial aggrefator.
- Evaluation is performed in the three way.
  - 8 hours prediction
  - [MetNet Ablation Experiments (Spatial and Temporal)](https://qiita.com/yu4u/items/606e6e5225ad9b603269)
  - Visualization (Case study)

## Insight

- We show that for up to 7 to 8 hours of lead time MetNet is able to outperform the High Resolution Rapid Refresh (HRRR) system which is the current best operational NWP available from NOAA, the National Oceanic and Atmospheric Administration.
- MetNet outperforms HRRR substantially on the three thresholds up to a lead time of respectively 400, 440 and the full 480 minutes. MetNet is also substantially better than the optical 8 flow method and than the persistence baseline for all lead times.
- The first ablation experiment reduces the spatial size of the input patch to 512 km. The performance of this configuration, called MetNet-ReducedSpatial, is similar to MetNet up to 150 minutes and then it starts to become progressively worse. This indicates the importance of the large spatial context used as input as well as the ability of MetNet’s architecture to capture information contained in the original receptive field of 1024 km.
- The second ablation configuration is called MetNet-ReducedTemporal and reduces the temporal context of MetNet’s input features from 90 minutes prior to Tx to 30 minutes prior to Tx. This does not affect MetNet’s performance significantly and suffices to capture the advection in the input patch.

## Contribution Summary

- They created probability output prediction model using CNN, ConvLSTM and self-attension. The prediction performance is outeperformed the other numerical weather prediction in the case of 1mm/h predicts.
- Spatial scale is more important than the temporal scale for MetNet from the Ablation experiments results.

## Keyword

- Self-Attention  (Ho et al.,2019)

## Unknown

- How about the heavier rainfalls ?

## Reflection

## Reference

- Peter Bauer, Alan Thorpe, and Gilbert Brunet. The quiet revolution of numerical weather prediction. Nature, 525(7567):47–55, 2015..
- Alex Krizhevsky, Ilya Sutskever, and Geoffrey E Hinton. Imagenet classification with deep convolutional neural networks. In Advances in neural information processing systems, pages 1097–1105, 2012.
- Kaiming He, Xiangyu Zhang, Shaoqing Ren, and Jian Sun. Deep residual learning for image recognition. In Proceedings of the IEEE conference on computer vision and pattern recognition, pages 770–778, 2016.
- Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N Gomez, Łukasz Kaiser, and Illia Polosukhin. Attention is all you need. In Advances in neural information processing systems, pages 5998–6008, 2017.
- Shreya Agrawal, Luke Barrington, Carla Bromberg, John Burge, Cenk Gazen, and Jason Hickey. Machine learning for precipitation nowcasting from radar images.
- G Ayzel, M Heistermann, A Sorokin, O Nikitin, and O Lukyanova. All convolutional neural networks for radar-based precipitation nowcasting. Procedia Computer Science, 150:186–192, 2019a.
- Vadim Lebedev, Vladimir Ivashkin, Irina Rudenko, Alexander Ganshin, Alexander Molchanov, Sergey Ovcharenko, Ruslan Grokhovetskiy, Ivan Bushmarinov, and Dmitry Solomentsev. Precipitation nowcasting with satellite imagery. arXiv preprint arXiv:1905.09932, 2019.
- Xingjian et al., 2015
- Xingjian Shi, Zhihan Gao, Leonard Lausen, Hao Wang, Dit-Yan Yeung, Wai-kin Wong, and Wangchun Woo. Deep learning for precipitation nowcasting: A benchmark and a new model. In Advances in neural information processing systems, pages 5617–5627, 2017.

---
