---
title: Unity 周期函数
date: 2019-02-12 04:11:45 Z
textarea: sdfsdafdsaf
---

unity周期函数

**Awake：官方表述**

> Awake is called when the script instance is being loaded.
>
> [Awake](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Awake.html) is used to initialize any variables or game state before the game starts. [Awake](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Awake.html) is called only once during the lifetime of the script instance. [Awake](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Awake.html) is called after all objects are initialized so you can safely speak to other objects or query them using for example [GameObject.FindWithTag](https://docs.unity3d.com/ScriptReference/GameObject.FindWithTag.html). Each GameObject's [Awake](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Awake.html) is called in a random order between objects. Because of this, you should use [Awake](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Awake.html) to set up references between scripts, and use Start to pass any information back and forth.[Awake](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Awake.html) is always called before any `Start` functions. This allows you to order initialization of scripts. [Awake](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Awake.html) can not act as a coroutine.  
>   
> **Note:** Use [Awake](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Awake.html) instead of the constructor for initialization, as the serialized state of the component is undefined at construction time. [Awake](https://docs.unity3d.com/ScriptReference/MonoBehaviour.Awake.html) is called once, just like the constructor.

直译：

Awake在脚本实例被加载的时候调用，注意如果gameObject的activeSelf为false，脚本不会被加载，如果仅是脚本的enable为false则脚本依然会被加载并且调用Awake。

Awake在游戏开始前用来初始化变量或者游戏状态。在整个脚本的生命周期中只调用一次。

Start：

OnEnable：

OnDisable：

OnDestroy