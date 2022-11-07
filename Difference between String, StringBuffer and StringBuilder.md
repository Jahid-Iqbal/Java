# Differences between String, StringBuffer and StringBuilder

Subject | String | StringBuffer | StringBuilder |
--------|--------|--------------|---------------|
**Storage**| Heap, SCP| Heap Area| Heap Area|
**Objects**| Immutable|Mutable|Mutable|
**Memory**|Each time allocates memory for changing the content. So, consuming more memory.|All changes happens over original object. So. consuming less memory.| All changes happens over original object. So. consuming less memory.|
**Thread Safe**| No. As the methods are non-synchronized|Yes. As the methods are synchronized.|No. As the methods are non-synchronized.|
**Performance**| Slow| Faster, compared to String.| Faster, compared to StringBuffer as methods are non-synchronized.|
**Use:**|If content is changing rarely.| If content is changing frequently.|If content is changing frequently.