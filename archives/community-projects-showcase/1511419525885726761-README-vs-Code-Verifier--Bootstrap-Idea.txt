# Thread 'README-vs-Code Verifier (Bootstrap Idea)' in forum #community-projects-showcase
# thread_id=1511419525885726761 forum_id=1316137596535177246
# Started 2026-06-02T20:46:20.283548+00:00

[2026-06-02T17:21:35.788000+00:00] xriddick (id=1511419525885726761)
    README-vs-Code Verifier (Bootstrap Idea)
    
    Goal: Build a small model that checks whether code actually matches what the README or documentation claims.
    
    Version 1:
    
    1. Use a tiny CPU-friendly model (nanoGPT or similar).
    
    2. Dataset:
    
    claim,code,label
    
    Example:
    
    "deletes files","open(path,'w').write('')","LIE"
    "deletes files","os.remove(path)","MATCH"
    
    3. Train:
    
    Claim + Code -> MATCH or LIE
    
    4. Start with 50-100 hand-labeled examples to validate the pipeline.
    
    5. Test on unseen examples.
    
    6. Scale by adding more repositories, claims, and contributors.
    
    7. If context becomes a problem, swap the model architecture while keeping the same dataset format.
    
    Long-term goal:
    
    Claim + Code
        ↓
    MATCH / LIE / UNCERTAIN
        ↓
    Evidence
    
    Example:
    
    "LIE: code empties the file but never deletes it."
    
    The purpose of V1 is not to solve code understanding. The purpose is to create the smallest reproducible framework for README-vs-code verification and improve it over time.

