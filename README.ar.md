بيان الانظمة التفاعلية
Reactive Manifesto
----------------------

بدأت العديد من المنظمات العاملة فى مجالات مختلفة فى إكتشاف بعض أساليب بناء الانظمة التى تشترك مع بعضها فى بعض المبادئ الهامة. هذة الانظمة تتمتع بالمزيد من الإستقرار Robust، والمتانة Resilient ، والقدرة على التكيف Flexible ، مما يؤهلها للوفاء بالمتطلبات الحديثة بشكل أعلى.

Organisations working in disparate domains are independently discovering patterns for building software that look the same. These systems are more robust, more resilient, more flexible and better positioned to meet modern demands. 

هذه التغييرات مطلوبة الآن بعد التطورالكبير والسريع فى متطلبات الانظمة الحديثة على مدار السنين الأخيرة. منذ زمن ليس بالكبير، كانت الأنظمة الكبيرة تحتاج عشرات من الخوادم، وعديد من الثوانى للرد على طلبات المستخدمين، وإغلاق الخدمة لساعات للصيانة والتعديلات، والكثير من الجيجابايت من البيانات. أما الآن يتم تنصيب ونشر البرامج على مختلف أنواع البيئات ، من الهواتف  المحمولة إلى عناقيد الخوادم السحابية Cloud-based clusters التى تحوي آلاف المعالجات ذوات الاكثر من نواة ، ويتوقع المستخدم الآن رداً خلال بعض أجزاء الثانية، وأنظمة تعمل ١٠٠٪ من الوقت، كما يتم حساب كمية البيانات الآن بالبيتابايت!
 بكل بساطة ، لا تستطيع أساليب بناء أنظمة البارحة على مجاراة متطلبات أنظمة اليوم.

These changes are happening because application requirements have changed dramatically in recent years. Only a few years ago a large application had tens of servers, seconds of response time, hours of offline maintenance and gigabytes of data. Today applications are deployed on everything from mobile devices to cloud-based clusters running thousands of multi-core processors. Users expect millisecond response times and 100% uptime. Data is measured in Petabytes. Today's demands are simply not met by yesterday’s software architectures.

نحن نعتقد أننا بحاجة إلى أساليب أكثر إحكاماً لبناء الأنظمة، ونؤمن بأن جميع الأركان المطلوبة تم التعرف عليها بالفعل: نحن نحتاج أنظمة متجاوبة Responsive ، متينة Resilient ، مرنة Elastic ، ورسائلية Message-driven. ونطلق عليها اسم الانظمة التفاعلية Reactive Systems.

We believe that a coherent approach to systems architecture is needed, and we believe that all necessary aspects are already recognised individually: we want systems that are Responsive, Resilient, Elastic and Message Driven. We call these Reactive Systems.

الأنظمة المبنية لتكون أنظمة تفاعلية تتميز بالمزيد من المرونة، والفصل بين المسئوليات loosly-coupled ، وقدرة إستيعاب أكثر مرونة Scalable. مما يجعلها أسهل فى البناء والتطوير والتعديل، وأكثر إستيعاباً [للأخطاء](/glossary#Failure) ، حيث تتعامل مع الخطأ بحكمة دون كوارث. كما تتمتع بسرعة الاستجابة ، تاركة مستخدميها ردوداً تفاعلية أكثر فائدة.

Systems built as Reactive Systems are more flexible, loosely-coupled and [scalable](/glossary#Scalability). This makes them easier to develop and amenable to change. They are significantly more tolerant of [failure](/glossary#Failure) and when failure does occur they meet it with elegance rather than disaster. Reactive Systems are highly responsive, giving [users](/glossary#User) effective interactive feedback. 

*الانظمة التفاعلية هي:*

*Reactive Systems are:*

* <a name="التجاوب"></a>**التجاوب Responsivity**: [النظام](/glossary#نظام) يستجيب فى وقت مناسب. سرعة الاستجابة هي حجر الزاوية فى معادلة قابلية استخدام النظام Usability، وليس ذلك فحسب، بل تضمن اكتشاف المشاكل سريعاً والتعامل معها بفاعلية أعلى. الأنظمة المتجاوبة تركز على توفير ردود متسقة وفائقة السرعة، مما يضمن إيصال الخدمة بجودة مناسبة ومضمونة ، والذى بدوره يسهل التعامل مع الأخطاء ، ويبنى ثقة المستخدم ، مشجعاً المزيد من التفاعل مع النظام.

* <a name="Responsive"></a>**Responsive**: The [system](/glossary#System) responds in a timely manner if at all possible. Responsiveness is the cornerstone of usability and utility, but more than that, responsiveness means that problems may be detected quickly and dealt with effectively. Responsive systems focus on providing rapid and consistent response times, establishing reliable upper bounds so they deliver a consistent quality of service. This consistent behaviour in turn simplifies error handling, builds end user confidence, and encourages further interaction. 

* <a name="الصمود"></a>**الصمود Resilience**: النظام يبقى متجاوباً حتى فى حالة وقوع الاخطاء. وذلك ليس حصراً على الانظمة عالية الإتاحة وخطيرة المهام، فكل الأنظمة غير الصامدة تصبح غير متجاوبة بعد حدوث أي خطأ. ويضمن صمود النظام كلا من: التناسخ Replication والاحتواء Containment والفصل Isolation والتفويض Delegation. حيث يتم *احتواء* الخطأ داخل كل عنصر، مع *فصل* عناصر النظام، يضمن قابلية العنصر على احتواء الخطأ واستعادة العمل دون التأثير فى بقية النظام ككل. ويتم *تفويض* إستعادة كل من العناصر إلى عنصر خارجى، كما يضمن *التناسخ* عند الحاجة بقاء النظام متاحاً طوال الوقت. ولا يعنى مستخدم عنصر بمسئولية التعامل مع أخطائه.

* <a name="Resilient"></a>**Resilient**: The system stays responsive in the face of [failure](/glossary#Failure). This applies not only to highly-available, mission critical systems — any system that is not resilient will be unresponsive after a failure. Resilience is achieved by [replication](/glossary#Replication), containment, [isolation](/glossary#Isolation) and [delegation](/glossary#Delegation). Failures are contained within each [component](/glossary#Component), isolating components from each other and thereby ensuring that parts of the system can fail and recover without compromising the system as a whole. Recovery of each component is delegated to another (external) component and high-availability is ensured by replication where necessary. The client of a component is not burdened with handling its failures.

* <a name="المرونة"></a>**المرونة**: النظام يبقى متجاوباً تحت مختلف ضغوط العمل. النظم التفاعلية يمكنها التعامل مع التغير فى معدل الإستخدام بزيادة أو تقليل الموارد المتاحة لخدمة ذلك الإستخدام. وذلك يعني تصميم نظام دون نقط تزاحم Contention points أو نقط اختناق مركزية Central bottleneck، مما يضمن القدرة على تقسيم Shard او تناسخ Replicate عناصره وتقسيم ضغط العمل عليها.
تدعم نظم العمل التفاعلية طرق التوسع او التحجيم Scaling عن طريق التنبؤ بالإستخدام Predictive ، أو الأستجابة للتغييرات Reactive بناء على معلومات مستمرة عن معدلات الأداء Performance measures. وتقوم بذلك بطريقة فعالة من حيث تكلفة الموارد المادية Hardware والبرمجية Software.

* <a name="Elastic"></a>**Elastic**: The system stays responsive under varying workload. Reactive Systems can react to changes in the input rate by increasing or decreasing the [resources](/glossary#Resource) allocated to service these inputs. This implies designs that have no contention points or central bottlenecks, resulting in the ability to shard or replicate components and distribute inputs among them. Reactive Systems support predictive, as well as Reactive, scaling algorithms by providing relevant live performance measures. They achieve [elasticity](/glossary#Elasticity) in a cost-effective way on commodity hardware and software platforms.

* <a name="رسائلية"></a>**رسائلية**: تعتمد الأنظمة التفاعلية على أساليب نقل غير متزامنة Asynchronous للمعلومات، مما يضمن الفصل بين عناصر النظام وتقليل التبعية loose-coupling ، وتجاهل مكان الموارد المستخدمة Location transparency. كما يوفر هذا الفاصل وسيلة لتحويل الأخطاء إلى رسائل.
ويضمن الإلتزام بهذا المبدأ إمكانية التحكم بمعدلات إستخدام الموارد ، ومرونة النظام ، وإنسيابية المعلومات عن طريق تصميم ومراقبة مسارات الرسائل فى النظام وتطبيق مبدأ الضغط العكسى Back pressure عند الحاجة.
ويضمن التراسل مع تجاهل مكان المعالجة Location Transparency إمكانية إدارة الأخطاء بنفس الطريقة سواء فى حالة إستخدام خادم واحد أو مجموعة خوادم.
كما يضمن التراسل غير المتزامن Non-blocking للمستقبلين إستهلاكاً أقل للموارد حيث يتم الإستهلاك فقط فى وقت تفعيل العنصر المرتبط بالعملية.

* <a name="Message-Driven"></a>**Message Driven**: Reactive Systems rely on [asynchronous](/glossary#Asynchronous) [message-passing](/glossary#Message-Driven) to establish a boundary between components that ensures loose coupling, isolation, and [location transparency](/glossary#Location-Transparency). This boundary also provides the means to delegate [failures](/glossary#Failure) as messages. Employing explicit message-passing enables load management, elasticity, and flow control by shaping and monitoring the message queues in the system and applying [back-pressure](/glossary#Back-Pressure) when necessary. Location transparent messaging as a means of communication makes it possible for the management of failure to work with the same constructs and semantics across a cluster or within a single host. [Non-blocking](/glossary#Non-Blocking) communication allows recipients to only consume [resources](/glossary#Resource) while active, leading to less system overhead.

تتكون الأنظمة الكبيرة من أنظمة أصغر، وبالتالى تعتمد على المزايا التفاعلية لمقوماتها. وذلك يعنى أن الأنظمة التفاعلية تطبق هذه المبادئ على جميع المستويات ، لتسهل عملية إندماج عناصر النظام. وتعتمد أكبر أنظمة العالم على خطط بنيت على هذه المبادئ ، لتخدم مليارات المستخدمين يومياً. ولذلك حان الوقت للتوعية بتلك المبادئ لتطبيقها منذ البداية بدلاً من إكتشافها من جديد مع كل مرة. 

Large systems are composed of smaller ones and therefore depend on the Reactive properties of their constituents. This means that Reactive Systems apply design principles so these properties apply at all levels of scale, making them composable. The largest systems in the world rely upon architectures based on these properties and serve the needs of billions of people daily. It is time to apply these design principles consciously from the start instead of rediscovering them each time.

[وقع البيان](http://www.reactivemanifesto.org/#sign-button)

[Sign the manifesto](http://www.reactivemanifesto.org/#sign-button)


