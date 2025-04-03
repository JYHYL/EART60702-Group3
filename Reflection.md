### Wanglu Yu
This project allowed me to contribute more to the group, particularly in programming. Compared to project 1, I took on more responsibility and gained greater confidence in my abilities. One of the most noticeable improvements was my increased ability to work with .nc files. Although I’m not yet proficient, I have mastered the basic methods for reading and processing them. This skill will also be valuable for my upcoming ERP project, which involves similar data formats.

That said, we did face some challenges during the project. Although we completed the EDA early, we had to redo a large portion of it because we initially failed to include an additional dataset. This experience taught me the importance of thoroughly confirming all project requirements before getting started. In future projects, I plan to list all requirements in advance to avoid heading in the wrong direction and wasting time.

As for the presentation, I was still nervous, but I felt a bit more relaxed than last time — which, for me, is already an improvement.

Another major issue was that I initially misjudged the project deadline, which caused us to start late and work under time pressure. Although we managed to complete everything in the end, this taught me that confirming the deadline early is crucial to avoiding unnecessary stress and last-minute rushes.

### Silang Nimai

This project experience has deepened my understanding of the complexity involved in handling meteorological data. It requires familiarity with mainstream meteorological products, the ability to retrieve and consult relevant datasets, the skill to match meteorological variables with different naming conventions through domain knowledge, and the capability to extract data with specific temporal and spatial resolutions using code. I have realized the importance of establishing a complete workflow, including early-stage knowledge preparation and supporting scripts.

Previously, some of my research group peers worked on national-scale climate change studies, others coupled reanalysis data with hydrological models for runoff simulation, and some applied algorithms to merge and evaluate satellite product data. During the initial design phase of this project, I reflected on these research directions based on the available data and developed a deeper understanding of them.

Although we ultimately selected a relatively simple prediction task, I applied the stacking method I had learned for the first time. While this was merely an initial attempt and did not improve the model’s performance, it may serve as a viable option for future applications. In terms of image selection, I also realized that it is sometimes more appropriate to choose images based on the properties we aim to highlight, rather than those that best display differences.

Throughout the course of this project, I gained practical experience in project management, including writing a README file, configuring environments, understanding the concepts of branches and the main branch, and handling pull requests. I also learned to manage the project using both Git and the GitHub web interface.

### Madeleine Carnell

In this project, I played a central role in the technical development and coordination of our group’s overall workflow. Early on, I helped define the project structure, proposed the initial modelling plan, and ensured that our work remained aligned. I took responsibility for organising group meetings, setting internal deadlines, and keeping momentum consistent across tasks. Our original plan focused solely on applying machine learning models to the provided MME simulations to forecast maximum urban temperatures in Manchester.

However, less than a week before our presentation, we realised that an external dataset needed to be incorporated. This significantly changed the project scope, requiring us to restructure our data pipeline and model comparisons. I took the lead in responding to this shift by selecting the CHESS-SCAPE RCP8.5 dataset as a suitable academic benchmark. Given practical limitations — such as the CHESS data being split into hundreds of files for daily resolution — I opted for the monthly version. I handled the preprocessing, including spatial extraction for Manchester, time alignment, unit conversion, and feature matching. Not all variables aligned perfectly, but I made pragmatic decisions based on availability, methodological fit, and time constraints.

I designed and implemented the Random Forest modelling framework in parallel, training individual models on each MME simulation and CHESS separately. I created a consistent pipeline for sequencing, training, evaluation, and saving results, and documented performance using RMSE and prediction visualisations. While one group member led on GitHub documentation, I focused on environment reproducibility and README drafting. That said, one thing I would do differently next time is begin the repository structure earlier. Our original GitHub organisation was not fully aligned with best practices, and we had to restructure and clean it after the presentation. It’s something I’d prioritise from the start in future projects.

This project strengthened my technical skills in handling real-world climate data, particularly in netCDF format using `xarray`, and improved my understanding of supervised learning models like Random Forest. It also gave me valuable experience in aligning data across incompatible sources, managing collaborative workflows, and navigating last-minute changes under pressure. Throughout, I worked closely with my teammates to ensure our contributions remained integrated and aligned.

Looking back, I would also consider narrowing the scope of our research question to something with a more tangible societal or environmental application — for example, modelling wheat yields, PM2.5 air quality, or drought conditions using similar supervised learning approaches. These questions often allow for a stronger narrative and more precise interpretation of model performance. Nonetheless, I’m proud of how we adapted our work under pressure, produced a robust model comparison framework, and positioned our results in relation to an academic climate projection dataset, all of which made for a meaningful and well-rounded final project.


