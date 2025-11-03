# CSS385-OnePager-Performance-Considerations

## Sources of Performance Concerns
Games that are similar to A Cat’s Quest in terms of performance for a 2D top-down game are Stardew Valley, The Legend of Zelda: Four Swords, and Celeste, and I may face similar concerns that these games have faced when it comes to building my own.
1. **Memory handling** when it comes to loading, accessing, and unloading assets can put strain on the RAM in some devices when trying to run data for all the different files. 
2. **Low FPS** can result in frame drops and on-screen motion that looks laggy and not smooth or fluid, stemming from **overdraw**. When a system’s GPU has trouble calculating every layer and has to redraw the same pixel multiple times in a frame, this leads to drained battery and glitches. 
3. **Multiple draw calls** can overwork the CPU of the system, also causing **frame rate drops**. Since a game like A Cat’s Quest requires many sprites to make an immersive world experience, having a draw call for each one can strain the CPU and cause low FPS. 


## One Common Strategy for each Performance Concern
1. Removing things that are no longer needed and cleaning up are crucial when it comes to memory handling by dynamically allocating assets, and can significantly improve performance.
2. Splitting draw calls into two for layers, an opaque one and a transparent one. This allows for limited GPU processing to only what is necessary instead of constantly redrawing the same pixels.
3. Sprite Atlases are large textures that contain multiple sprites built into Unity’s library, allowing for the GPU to process them in batches rather than separately. This can prove very useful when it comes to implementation instead of using multiple draw calls for each sprite. 


## Summary of Strategy Usages
I would use Sprite Atlases as a solution for both memory handling and multiple draw calls since they can not only be used to handle the issue of multiple draw calls, but also perform more optimal runtimes and improve memory performance. I would also remove things that aren’t necessary and clean up as I continue to add more sprites, scenes, etc. This way ensures a smoother runtime with memory performance staying low. 

## References
https://learn.unity.com/tutorial/optimization-approaches-for-project-assets
https://www.reddit.com/r/Unity2D/comments/1m2l8m7/2d_game_performance_and_why_your_pretty_game_runs/
https://developer.arm.com/Additional%20Resources/Video%20Tutorials/Avoiding%20overdraw%20in%202D%20games

