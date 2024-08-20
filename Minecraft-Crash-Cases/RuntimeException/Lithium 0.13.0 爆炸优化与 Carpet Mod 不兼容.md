# 错误报告

## 基本信息

**错误标题**: **RuntimeException**

**时间**: 2024-08-20 10:53

### 错误描述

Fabric1.21加载carpet无法初始化并抛出异常

### 错误日志

```log
java.lang.RuntimeException: Could not execute entrypoint stage 'client' due to errors, provided by 'carpet' at 'carpet.CarpetServer::onGameStarted'!
	at net.fabricmc.loader.impl.FabricLoaderImpl.lambda$invokeEntrypoints$2(FabricLoaderImpl.java:403)
	at net.fabricmc.loader.impl.util.ExceptionUtil.gatherExceptions(ExceptionUtil.java:33)
	at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:401)
	at net.fabricmc.loader.impl.game.minecraft.Hooks.startClient(Hooks.java:53)
	at net.minecraft.class_310.<init>(class_310.java:477)
	at net.minecraft.client.main.Main.main(Main.java:239)
	at net.fabricmc.loader.impl.game.minecraft.MinecraftGameProvider.launch(MinecraftGameProvider.java:480)
	at net.fabricmc.loader.impl.launch.knot.Knot.launch(Knot.java:74)
	at net.fabricmc.loader.impl.launch.knot.KnotClient.main(KnotClient.java:23)
	at java.base/jdk.internal.reflect.DirectMethodHandleAccessor.invoke(DirectMethodHandleAccessor.java:103)
	at java.base/java.lang.reflect.Method.invoke(Method.java:580)
	at oolloo.jlw.Wrapper.invokeMain(Wrapper.java:110)
	at oolloo.jlw.Wrapper.main(Wrapper.java:103)
Caused by: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_1927 failed
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.getPostMixinClassByteArray(KnotClassDelegate.java:427)
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.tryLoadClass(KnotClassDelegate.java:323)
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.loadClass(KnotClassDelegate.java:218)
	at net.fabricmc.loader.impl.launch.knot.KnotClassLoader.loadClass(KnotClassLoader.java:119)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:526)
	at java.base/java.lang.Class.getDeclaredMethods0(Native Method)
	at java.base/java.lang.Class.privateGetDeclaredMethods(Class.java:3578)
	at java.base/java.lang.Class.getDeclaredMethods(Class.java:2676)
	at carpet.script.annotation.AnnotationParser.parseFunctionClass(AnnotationParser.java:127)
	at carpet.script.CarpetScriptServer.parseFunctionClasses(CarpetScriptServer.java:507)
	at carpet.CarpetServer.onGameStarted(CarpetServer.java:78)
	at java.base/java.lang.invoke.MethodHandleProxies$1.invoke(MethodHandleProxies.java:199)
	at jdk.proxy3/com.sun.proxy.jdk.proxy3.$Proxy61.onInitializeClient(Unknown Source)
	at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:399)
	... 10 more
Caused by: org.spongepowered.asm.mixin.transformer.throwables.MixinTransformerError: An unexpected critical error was encountered
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.applyMixins(MixinProcessor.java:392)
	at org.spongepowered.asm.mixin.transformer.MixinTransformer.transformClass(MixinTransformer.java:234)
	at org.spongepowered.asm.mixin.transformer.MixinTransformer.transformClassBytes(MixinTransformer.java:202)
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.getPostMixinClassByteArray(KnotClassDelegate.java:422)
	... 23 more
Caused by: org.spongepowered.asm.mixin.injection.throwables.InjectionError: Critical injection failure: Redirector onExplosion(Lnet/minecraft/class_243;Lnet/minecraft/class_1297;)F in carpet.mixins.json:Explosion_scarpetEventMixin from mod carpet failed injection check, (0/1) succeeded. Scanned 0 target(s). Using refmap fabric-carpet-refmap.json
	at org.spongepowered.asm.mixin.injection.struct.InjectionInfo.postInject(InjectionInfo.java:531)
	at org.spongepowered.asm.mixin.transformer.MixinTargetContext.applyInjections(MixinTargetContext.java:1490)
	at org.spongepowered.asm.mixin.transformer.MixinApplicatorStandard.applyInjections(MixinApplicatorStandard.java:752)
	at org.spongepowered.asm.mixin.transformer.MixinApplicatorStandard.applyMixin(MixinApplicatorStandard.java:330)
	at org.spongepowered.asm.mixin.transformer.MixinApplicatorStandard.apply(MixinApplicatorStandard.java:246)
	at org.spongepowered.asm.mixin.transformer.TargetClassContext.apply(TargetClassContext.java:437)
	at org.spongepowered.asm.mixin.transformer.TargetClassContext.applyMixins(TargetClassContext.java:418)
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.applyMixins(MixinProcessor.java:363)
	... 26 more
```
## 环境信息

**操作系统**: [请填写操作系统的名称及版本号]
**Minecraft版本/Java版本**: [Minecraft fabric 1.21/Java 21.0.1]
**网络环境**: [无需联网]

## 详细分析

### 用户操作
1. 自行添加mod
2. 更新模组后API不兼容
3. 更新API后出现报错

### 原因分析
高版本模组有不兼容，日志没有指出不兼容mod需要二分法排查

### 操作结果
Lithium 0.13.0 爆炸优化与 Carpet Mod 不兼容

### 影响范围
此错误导致 Minecraft 无法加载 加载 Carpet Mod 模组，影响了游戏的启动


## 解决方案

1. 通过在 config 文件夹的 lithium.properties 文件中添加以下行，手动禁用 lithium 的优化：```mixin.world.explosions.cache_exposure=false```

## 联系信息

**紧急程度**: [低]

---

## 附加说明

- **报告模板版本**: 1.0
- **模板最后更新时间**: `2024-08-20`
- **备注**: []
