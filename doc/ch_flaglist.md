# ch的全部flag

List of Phases:
|||||
|--|--|--|--|
|  All                                      |BGJit                                    |Module                                   |LibInit|                                  
|  JsLibInit                                |Parse                                    |RegexCompile                             |DeferParse|                               
|  Redeferral                               |DeferEventHandlers                       |FunctionSourceInfoParse                  |StringTemplateParse|                      
|  CreateParserState                        |SkipNestedDeferred                       |CacheScopeInfoNames                      |ScanAhead|                                
|  ParallelParse                            |EarlyReferenceErrors                     |EarlyErrorOnAssignToCall                 |BgParse|                                  
|  ByteCode                                 |CachedScope                              |StackFunc                                |StackClosure|                             
|  DisableStackFuncOnDeferredEscape         |DelayCapture                             |DebuggerScope                            |ByteCodeSerialization|                    
|  VariableIntEncoding                      |NativeCodeSerialization                  |OptimizeBlockScope                       |Delay|                                    
|  Speculation                              |GatherCodeGenData                        |Wasm                                     |WasmBytecode|                             
|  WasmReader                               |WasmSection                              |WasmOpCodeDistribution                   |WasmDeferred|                             
|  WasmValidatePrejit                       |WasmInOut                                |WasmMemWrites                            |Asmjs|                                    
|  AsmjsTmpRegisterAllocation               |AsmjsEncoder                             |AsmjsInterpreter                         |AsmJsJITTemplate|                         
|  AsmjsFunctionEntry                       |AsmjsInterpreterStack                    |AsmjsEntryPointInfo                      |AsmjsCallDebugBreak|                      
|  BackEnd                                  |IRBuilder                                |SwitchOpt                                |BailOnNoProfile|                          
|  BackendConcatExprOpt                     |ClosureRangeCheck                        |ClosureRegCheck                          |Inline|                                   
|  InlineRecursive                          |InlineAtEveryCaller                      |InlineTree                               |TryAggressiveInlining|                    
|  InlineConstructors                       |InlineBuiltIn                            |InlineInJitLoopBody                      |InlineAccessors|                          
|  InlineGetters                            |InlineSetters                            |InlineApply                              |InlineApplyTarget|                        
|  InlineApplyWithoutArrayArg               |BailOutOnNotStackArgs                    |InlineCall                               |InlineCallTarget|                         
|  PartialPolymorphicInline                 |PolymorphicInline                        |PolymorphicInlineFixedMethods            |InlineOutsideLoops|                       
|  InlineFunctionsWithLoops                 |EliminateArgoutForInlinee                |InlineBuiltInCaller                      |InlineArgsOpt|                            
|  RemoveInlineFrame                        |InlinerConstFold                         |InlineCallbacks                          |ExecBOIFastPath|                          
|  FGBuild                                  |OptimizeTryFinally                       |RemoveBreakBlock                         |TailDup|                                  
|  FGPeeps                                  |GlobOpt                                  |PathDepBranchFolding                     |OptimizeTryCatch|                         
|  CaptureByteCodeRegUse                    |Backward                                 |TrackIntUsage                            |TrackNegativeZero|                        
|  TypedArrayVirtual                        |TrackIntOverflow                         |TrackCompoundedIntOverflow               |Forward|                                  
|  ValueTable                               |ValueNumbering                           |AVTInPrePass                             |PathDependentValues|                      
|  TrackRelativeIntBounds                   |BoundCheckElimination                    |BoundCheckHoist                          |LoopCountBasedBoundCheckHoist|            
|  CopyProp                                 |ObjPtrCopyProp                           |ConstProp                                |Int64ConstProp|                           
|  ConstFold                                |CSE                                      |HoistConstInt                            |TypeSpec|                                 
|  AggressiveIntTypeSpec                    |AggressiveMulIntTypeSpec                 |LossyIntTypeSpec                         |FloatTypeSpec|                            
|  StringTypeSpec                           |InductionVars                            |Invariants                               |FieldCopyProp|                            
|  FieldPRE                                 |MakeObjSymLiveInLandingPad               |HostOpt                                  |ObjTypeSpec|                              
|  ObjTypeSpecNewObj                        |ObjTypeSpecIsolatedFldOps                |ObjTypeSpecIsolatedFldOpsWithBailOut     |ObjTypeSpecStore|                         
|  EquivObjTypeSpec                         |EquivObjTypeSpecByDefault                |TraceObjTypeSpecTypeGuards               |TraceObjTypeSpecWriteGuards|              
|  LiveOutFields                            |DisabledObjTypeSpec                      |DepolymorphizeInlinees                   |ReuseAuxSlotPtr|                          
|  PolyEquivTypeGuard                       |SimulatePolyCacheWithOneTypeForFunction  |CheckThis                                |StackArgOpt|                              
|  StackArgFormalsOpt                       |IndirCopyProp                            |ArrayCheckHoist                          |ArrayMissingValueCheckHoist|              
|  ArraySegmentHoist                        |JsArraySegmentHoist                      |ArrayLengthHoist                         |EliminateArrayAccessHelperCall|           
|  NativeArray                              |NativeNewScArray                         |NativeArrayConversion                    |CopyOnAccessArray|                        
|  NativeArrayLeafSegment                   |TypedArrayTypeSpec                       |LdLenIntSpec                             |FixDataProps|                             
|  FixMethodProps                           |FixAccessorProps                         |FixDataVarProps                          |UseFixedDataProps|                        
|  UseFixedDataPropsInInliner               |LazyBailout                              |LazyFixedDataBailout                     |LazyFixedTypeBailout|                     
|  FixedMethods                             |FEFixedMethods                           |FixedFieldGuardCheck                     |FixedNewObj|                              
|  JitAllocNewObj                           |FixedCtorInlining                        |FixedCtorCalls                           |FixedScriptMethodInlining|                
|  FixedScriptMethodCalls                   |FixedBuiltInMethodInlining               |FixedBuiltInMethodCalls                  |SplitNewScObject|                         
|  OptTagChecks                             |MemOp                                    |MemSet                                   |MemCopy|                                  
|  IncrementalBailout                       |DeadStore                                |ReverseCopyProp                          |MarkTemp|                                 
|  MarkTempNumber                           |MarkTempObject                           |MarkTempNumberOnTempObject               |SpeculationPropagationAnalysis|           
|  DumpGlobOptInstr                         |Lowerer                                  |FastPath                                 |LoopFastPath|                             
|  MathFastPath                             |Atom                                     |MulStrengthReduction                     |AgenPeeps|                                
|  BranchFastPath                           |CallFastPath                             |BitopsFastPath                           |OtherFastPath|                            
|  ObjectFastPath                           |ProfileBasedFldFastPath                  |AddFldFastPath                           |RootObjectFldFastPath|                    
|  ArrayLiteralFastPath                     |ArrayCtorFastPath                        |NewScopeSlotFastPath                     |FrameDisplayFastPath|                     
|  HoistMarkTempInit                        |HoistConstAddr                           |JitWriteBarrier                          |PreLowererPeeps|                          
|  CFGInJit                                 |TypedArray                               |TracePinnedTypes                         |InterruptProbe|                           
|  EncodeConstants                          |RegAlloc                                 |Liveness                                 |RegParams|                                
|  LinearScan                               |OpHelperRegOpt                           |StackPack                                |SecondChance|                             
|  RegionUseCount                           |RegHoistLoads                            |ClearRegLoopExit                         |Peeps|                                    
|  Layout                                   |EHBailoutPatchUp                         |FinalLower                               |PrologEpilog|                             
|  InsertNOPs                               |Encoder                                  |Emitter                                  |DebugBreak|                               
|  BrShorten                                |LoopAlign                                |SWB                                      |Run|                                      
|  Interpreter                              |EvalCompile                              |FastIndirectEval                         |IdleDecommit|                             
|  IdleCollect                              |Marshal                                  |MemoryAllocation                         |PageHeap|                                 
|  LargeMemoryAllocation                    |PageAllocatorAlloc                       |Recycler                                 |ThreadCollect|                            
|  ExplicitFree                             |ExpirableCollect                         |GarbageCollect                           |ConcurrentCollect|                        
|  BackgroundResetMarks                     |BackgroundFindRoots                      |BackgroundRescan                         |BackgroundRepeatMark|                     
|  BackgroundFinishMark                     |ConcurrentPartialCollect                 |ParallelMark                             |PartialCollect|                           
|  ResetMarks                               |ResetWriteWatch                          |FindRoot                                 |FindRootArena|                            
|  FindImplicitRoot                         |FindRootExt                              |ScanStack                                |ConcurrentMark|                           
|  ConcurrentWait                           |Rescan                                   |Mark                                     |Sweep|                                    
|  SweepWeak                                |SweepSmall                               |SweepLarge                               |SweepPartialReuse|                        
|  ConcurrentSweep                          |Finalize                                 |Dispose                                  |FinishPartial|                            
|  Host                                     |BailOut                                  |RegexQc                                  |RegexOptBT|                               
|  InlineCache                              |PolymorphicInlineCache                   |MissingPropertyCache                     |PropertyCache|                            
|  CloneCacheInCollision                    |ConstructorCache                         |InlineCandidate                          |InlineHostCandidate|                      
|  ScriptFunctionWithInlineCache            |IsConcatSpreadableCache                  |Arena                                    |ApplyUsage|                               
|  ObjectHeaderInlining                     |ObjectHeaderInliningForConstructors      |ObjectHeaderInliningForObjectLiterals    |ObjectHeaderInliningForEmptyObjects|      
|  OptUnknownElementName                    |TypePropertyCache                        |InlineSlots                              |DynamicProfile|                           
|  DynamicProfileStorage                    |JITLoopBody                              |JITLoopBodyInTryCatch                    |JITLoopBodyInTryFinally|                  
|  ReJIT                                    |ExecutionMode                            |SimpleJitDynamicProfile                  |SimpleJit|                                
|  FullJit                                  |FailNativeCodeInstall                    |PixelArray                               |Etw|                                      
|  Profiler                                 |CustomHeap                               |XDataAllocator                           |PageAllocator|                            
|  StringConcat                             |PRNG                                     |PreReservedHeapAlloc                     |CFG|                                      
|  ExceptionStackTrace                      |ExtendedExceptionInfoStackTrace          |ProjectionMetadata                       |TypeHandlerTransition|                    
|  Debugger                                 |ENC                                      |ConsoleScope                             |ScriptProfiler|                           
|  JSON                                     |Intl                                     |RegexResultNotUsed                       |Error|                                    
|  PropertyRecord                           |TypePathDynamicSize                      |ObjectCopy                               |ShareTypesWithAttributes|                 
|  ShareAccessorTypes                       |ShareFuncTypes                           |ConditionalCompilation                   |InterpreterProfile|                       
|  InterpreterAutoProfile                   |ByteCodeConcatExprOpt                    |TraceInlineCacheInvalidation             |TracePropertyGuards|                      
|  StackFramesEvent                         |PerfHint                                 |TypeShareForChangePrototype              |DeferSourceLoad|                          
|  DataCache                                |ObjectMutationBreakpoint                 |NativeCodeData                           |XData|                                    

List of flags:

                                               ArrayValidate                  Validate each array for valid elements (default: false)
                                   MemOpMissingValueValidate                  Validate Missing Value Tracking on memset/memcopy
                                         OOPJITFixupValidate                  Validate that all entries in fixup list are allocated as NativeCodeData and that all NativeCodeData gets fixed up
                                             ArenaNoFreeList                  Do not free list in arena
                                            ArenaNoPageReuse                  Do not reuse page in arena
                                           ArenaUseHeapAlloc                  Arena use heap to allocate memory instead of page allocator
                                         ValidateInlineStack                  Does a stack walk on helper calls to validate inline stack is correctly restored
                                                     AsmDiff                  Dump the IR without memory locations and varying parameters.
                                                 AsmDumpMode [:String]        Dump the final assembly to a file without memory locations and varying parameters
					The 'filename' is the file where the assembly will be dumped. Dump to console if no file is specified
                                                       AsmJs                  Enable Asmjs
                                            AsmJsStopOnError                  Stop execution on any AsmJs validation errors
                                                   AsmJsEdge                  Enable asm.js features which may have backward incompatible changes or not validate on old demos
                                                        Wasm                  Enable WebAssembly
                                                     WasmI64                  Enable Int64 testing for WebAssembly. ArgIns can be [number,string,{low:number,high:number}]. Return values will be {low:number,high:number}
                                               WasmFastArray                  Enable fast array implementation for WebAssembly
                                WasmSharedArrayVirtualBuffer                  Use Virtual allocation for WebAssemblySharedArrayBuffer (Windows only)
                                            WasmMathExFilter                  Enable Math exception filter for WebAssembly
                                            WasmCheckVersion                  Check the binary version for WebAssembly
                                          WasmAssignModuleID                  Assign an individual ID for WebAssembly module
                                            WasmIgnoreLimits                  Ignore the WebAssembly binary limits 
                                                    WasmFold                  Enable i32/i64 const folding
                                          WasmIgnoreResponse                  Ignore the type of the Response object
                                            WasmMaxTableSize [:Number]        Maximum size allowed to the WebAssembly.Table
                                                 WasmThreads                  Enable WebAssembly threads feature
                                              WasmMultiValue                  Use new WebAssembly multi-value
                                             WasmSignExtends                  Use new WebAssembly sign extension operators
                                             WasmNontrapping                  Enable non-trapping float-to-int conversions in WebAssembly
                                            WasmExperimental                  Enable WebAssembly experimental features
                                                    WasmSimd                  Enable SIMD in WebAssembly
                                                 AssertBreak                  Debug break on assert
                                                 AssertPopUp                  Pop up asserts (default: false)
                                                AssertIgnore                  Ignores asserts if set
                                              AsyncDebugging                  Enable async debugging feature (default: false)
                                        BailOnNoProfileLimit [:Number]        The limit of bailout on no profile info before triggering a rejit
                                   BailOnNoProfileRejitLimit [:Number]        The limit of bailout on no profile info before we disable the bailouts
                                                BaselineMode                  Dump only stable content that can be used for baseline comparison
                                                 DumpOnCrash [:String]        generate heap dump on asserts or unhandled exception if set
                                              FullMemoryDump [:String]        Will perform a full memory dump when -DumpOnCrash is supplied.
                                                     BailOut [:NumberPairSet] Source location to insert BailOut
                                          BailOutAtEveryLine                  Inserts BailOut at every line of source (default: false)
                                      BailOutAtEveryByteCode                  Inserts BailOut at every Byte code (default: false)
                                  BailOutAtEveryImplicitCall                  Force generating implicit call bailout even when we don't need it
                                             BailOutByteCode [:NumberSet]     Byte code location to insert BailOut. Use with -prejit only
                                                   Benchmark                  Disable security code which introduce variability in benchmarks
                                                       BgJit                  Background JIT. Disable to force heuristic-based foreground JITting. (default: true)
                                                     BgParse                  Background Parse. Disable to force all parsing to occur on UI thread. (default: true)
                                                  BgJitDelay [:Number]        Delay to wait for speculative jitting before starting script execution
                                          BgJitDelayFgBuffer [:Number]        When speculatively jitting in the foreground thread, do so for (BgJitDelay - BgJitDelayBuffer) milliseconds
                                         BgJitPendingFuncCap [:Number]        Disable delay if pending function count larger then cap
                                         CreateFunctionProxy                  Create function proxies instead of full function bodies
                                                 HybridFgJit                  When background JIT is enabled, enable jitting in the foreground based on heuristics. This flag is only effective when OptimizeForManyInstances is disabled (UI threads).
                           HybridFgJitBgQueueLengthThreshold [:Number]        The background job queue length must exceed this threshold to consider jitting in the foreground
                                                BytecodeHist                  Provide a histogram of the bytecodes run by the script. (NoNative required).
                                           CurrentSourceInfo                  Enable IASD get current script source info
                                                      CFGLog                  Log CFG checks
                                              CheckAlignment                  Insert checks in the native code to verify 8-byte alignment of stack
                                  CheckEmitBufferPermissions                  Check JIT code buffers at commit and decommit time to ensure no PAGE_EXECUTE_READWRITE pages.
                                             CheckMemoryLeak                  Check for heap memory leak
                                                  DumpOnLeak [:String]        Create a dump on failed memory leak check
                                              CheckOpHelpers                  Verify opHelper labels in the JIT are set properly
                               CloneInlinedPolymorphicCaches                  Clones polymorphic inline caches in inlined functions
                                           ConcurrentRuntime                  Enable Concurrent GC and background JIT when creating runtime
                                                     Console                  Create console window in GUI app
                                            ConsoleExitPause                  Pause on exit when a console window is created in GUI app
                                  ConstructorInlineThreshold [:Number]        Maximum size in bytecodes of a constructor inline candidate with monomorphic field access
                ConstructorCallsRequiredToFinalizeCachedType [:Number]        Number of calls to a constructor required before the type cached in the constructor cache is finalized
                                    PropertyCacheMissPenalty [:Number]        Number of string or symbol cache hits per miss needed to be worth using cache
                                  PropertyCacheMissThreshold [:Number]        Point at which we disable string or symbol property cache
                                      PropertyCacheMissReset [:Number]        Point at which we try to start using string or symbol cache after giving up
                                            CrashOnException                  Removes the top-level exception handler, allowing jc.exe to crash on an unhandled exception.  No effect on IE. (default: false)
                                                       Debug                  Disable phases (layout, security code, etc) which makes JIT output harder to debug
                                                  DebugBreak [:NumberSet]     Index of the function where you want to break
                                         StatementDebugBreak [:NumberTrioSet] Index of the statement where you want to break
                                      DebugBreakOnPhaseBegin [:Phase]         Break into debugger at the beginning of given phase for listed function
                                                 DebugWindow                  Send console output to debugger window
                                            ParserStateCache                  Enable creation of parser state cache
                                  DeferTopLevelTillFirstCall                  Enable tracking of deferred top level functions in a script file, until the first function of the script context is parsed.
                                                  DeferParse [:Number]        Minimum size of defer-parsed script (non-zero only: use /nodeferparse do disable
                                    DirectCallTelemetryStats                  Enables logging stats for direct call telemetry
                                           DisableArrayBTree                  Disable creation of BTree for Arrays
                                      DisableRentalThreading                  Disable rental threading when creating runtime
                                  DisableVTuneSourceLineInfo                  Disable VTune Source line info for Dynamic JITted code
                                             DisplayMemStats                  Display memory usage statistics
                                                        Dump [:Phase]         What All to dump
                                             DumpIRAddresses                  Print addresses in IR dumps
                                           DumpLineNoInColor                  Print the source code in high intensity color for better readability
                                       DumpObjectGraphOnExit                  Dump object graph on recycler destructor
                                    DumpObjectGraphOnCollect                  Dump object graph on recycler destructor
                                     DumpEvalStringOnRemoval                  Dumps an eval string when its being removed from the eval map
                                       DumpObjectGraphOnEnum                  Dump object graph on recycler heap enumeration
                                         DynamicProfileCache [:String]        File to cache dynamic profile information
                                                         Dpc [:String]        File to cache dynamic profile information
                                      DynamicProfileCacheDir [:String]        Directory to cache dynamic profile information
                                         DynamicProfileInput [:String]        Read only file containing dynamic profile information
                                                         Dpi [:String]        Read only file containing dynamic profile information
                                         WininetProfileCache                  Use the WININET cache to save the profile information
                               NoDynamicProfileInMemoryCache                  Enable in-memory cache for dynamic sources
                                  ProfileBasedSpeculativeJit                  Enable dynamic profile based speculative JIT
                                  ProfileBasedSpeculationCap [:Number]        In the presence of dynamic profile speculative JIT is capped to this many bytecode instructions
                                    DynamicProfileMutatorDll [:String]        Path of the mutator DLL
                                       DynamicProfileMutator [:String]        Type of local, temp, return, param, loop implicit flag and implicit flag. 
					i.e local=LikelyArray_NoMissingValues_NonInts_NonFloats;temp=Int8Array;param=LikelyNumber;return=LikelyString;loopimplicitflag=ImplicitCall_ToPrimitive;implicitflag=ImplicitCall_None
					or pass DynamicProfileMutator:random
					See DynamicProfileInfo.h for enum values
                 ExecuteByteCodeBufferReturnsInvalidByteCode                  Serialized byte code execution always returns SCRIPT_E_INVALID_BYTECODE
                                  ExpirableCollectionGCCount [:Number]        Number of GCs during which Expirable object profiling occurs
                         ExpirableCollectionTriggerThreshold [:Number]        Threshold at which Expirable Object Collection is triggered (In Percentage)
                                         SkipSplitOnNoResult                  If the result of Regex split isn't used, skip executing the regex. (Perf optimization)
                                                  TestEtwDll [:String]        Path of the TestEtwEventSink DLL
                                              CollectGarbage                  Enable CollectGarbage API
                                                        Intl                  Intl object support
                                                IntlBuiltIns                  Intl built-in function support
                                                IntlPlatform                  Make the internal Intl native helper object visible to user code
                                                   JsBuiltIn                  JS Built-in function support
                                                    JitRepro                  Add Function.invokeJit to execute codegen on an encoded rpc buffer
                                       EntryPointInfoRpcData                  Keep encoded rpc buffer for jitted function on EntryPointInfo until cleanup
                                                 LdChakraLib                  Access to the Chakra internal library with the __chakraLibrary keyword
                                                         ES6                  Enable ES6 stable features
                                                      ES6All                  Enable all ES6 features, both stable and unstable
                                             ES6Experimental                  Enable all experimental features
                                                  ES6Species                  Enable ES6 '@@species' properties and built-in behaviors
                                               ES7AsyncAwait                  Enable ES7 'async' and 'await' keywords
                                                  ES6Classes                  Enable ES6 'class' and 'extends' keywords
                                             ES6DateParseFix                  Enable ES6 Date.parse fixes
                                              ES6DefaultArgs                  Enable ES6 Default Arguments
                                            ES6Destructuring                  Enable ES6 Destructuring
                                         ES6ForLoopSemantics                  Enable ES6 for loop per iteration bindings
                                         ES6FunctionNameFull                  Enable ES6 Full function.name
                                               ES6Generators                  Enable ES6 generators
                                   ES7ExponentiationOperator                  Enable ES7 exponentiation operator (**)
                                            ES7ValuesEntries                  Enable ES7 Object.values and Object.entries
                                            ES7TrailingComma                  Enable ES7 trailing comma in function
                                       ES6IsConcatSpreadable                  Enable ES6 isConcatSpreadable Symbol
                                                     ES6Math                  Enable ES6 Math extensions
                                             ESDynamicImport                  Enable dynamic import
                                                   ES6Module                  Enable ES6 Modules
                                                   ES6Object                  Enable ES6 Object extensions
                                                   ES6Number                  Enable ES6 Number extensions
                                           ES6ObjectLiterals                  Enable ES6 Object literal extensions
                                                  ES6Promise                  Enable ES6 Promise feature
                                                    ES6Proxy                  Enable ES6 Proxy feature
                                                     ES6Rest                  Enable ES6 Rest parameters
                                                   ES6Spread                  Enable ES6 Spread support
                                                   ES6String                  Enable ES6 String extensions
                                     ES6StringPrototypeFixes                  Enable ES6 String.prototype fixes
                                           ES6PrototypeChain                  Enable ES6 prototypes (Example: Date prototype is object)
                                              ES6ToPrimitive                  Enable ES6 ToPrimitive symbol
                                                 ES6ToLength                  Enable ES6 ToLength fixes
                                              ES6ToStringTag                  Enable ES6 ToStringTag symbol
                                                  ES6Unicode                  Enable ES6 Unicode 6.0 extensions
                                           ES6UnicodeVerbose                  Enable ES6 Unicode 6.0 verbose failure output
                                              ES6Unscopables                  Enable ES6 With Statement Unscopables
                                              ES6RegExSticky                  Enable ES6 RegEx sticky flag
                                 ES6RegExPrototypeProperties                  Enable ES6 properties on the RegEx prototype
                                             ES6RegExSymbols                  Enable ES6 RegExp symbols
                                              ES6HasInstance                  Enable ES6 @@hasInstance symbol
                                                  ES6Verbose                  Enable ES6 verbose trace
                           ESObjectGetOwnPropertyDescriptors                  Enable Object.getOwnPropertyDescriptors
                                         ESSharedArrayBuffer                  Enable SharedArrayBuffer
                                            JitES6Generators                  Enable JITing of ES6 generators
                                   FastLineColumnCalculation                  Enable fast calculation of line/column numbers from the source.
                                                    Filename [:String]        Jscript source file
                                            FreeRejittedCode                  Free rejitted code
                                             ForceGuardPages                  Force the addition of guard pages
                                        PrintGuardPageBounds                  Prints the bounds of a guard page
                                           ForceLegacyEngine                  Force a jscrip9 dll load
                                                       Force [:Phase]         Force certain phase to run ignoring heuristics
                                                      Stress [:Phase]         Stress certain phases by making them kick in even if they normally would not.
                                             ForceArrayBTree                  Force enable creation of BTree for Arrays
                                             StrongArraySort                  Add secondary comparisons to the default array sort comparator to disambiguate sorts of equal-toString'd objects.
                                 ForceCleanPropertyOnCollect                  Force cleaning of property on collection
                                    ForceCleanCacheOnCollect                  Force cleaning of dynamic caches on collection
                                       ForceGCAfterJSONParse                  Force GC to happen after JSON parsing
                                      ForceDecommitOnCollect                  Force decommit collect
                                             ForceDeferParse                  Defer parsing of all function bodies
                                        ForceDiagnosticsMode                  Enable diagnostics mode and debug interpreter loop
                                       ForceGetWriteWatchOOM                  Force GetWriteWatch to go into OOM codepath in HeapBlockMap rescan
                            ForcePostLowerGlobOptInstrString                  Force tracking of globopt instr string post lower
                                             ForceSplitScope                  All functions will have unmerged body and param scopes
                        EnumerateSpecialPropertiesInDebugger                  Enable enumeration of special debug properties
                                         EnableJitInDiagMode                  Enable Fast F12 (only applicable with ForceDiagnosticsMode or while under debugger)
              EnableContinueAfterExceptionWrappersForHelpers                  Enable wrapper over helper methods in debugger, Fast F12 only
             EnableContinueAfterExceptionWrappersForBuiltIns                  Enable wrapper over library calls in debugger, Fast F12 only
                       EnableFunctionSourceReportForHeapEnum                  During HeapEnum, whether to report function source info (url/row/col)
                                   ForceFragmentAddressSpace [:Number]        Fragment the address space
                                          ForceOOMOnEBCommit [:Number]        Force CommitBuffer to return OOM
                                         ForceDynamicProfile                  Force to always generate profiling byte code
                                               ForceES5Array                  Force using ES5Array
                                          ForceAsmJsLinkFail                  Force asm.js link time validation to fail
                                ForceExpireOnNonCacheCollect                  Allow expiration collect outside of cache collection cleanups
                                               ForceFastPath                  Force fast-paths in native codegen
                                              ForceFloatPref                  Force float preferencing (JIT only)
                                            ForceJITLoopBody                  Force jit loop body only
                                 ForceStaticInterpreterThunk                  Force using static interpreter thunk
                             DumpCommentsFromReferencedFiles                  Allow printing comments of comment-table of the referenced file as well (use with -trace:CommentTable)
                                       DelayFullJITSmallFunc [:Number]        Scale Full JIT threshold for small functions which are going to be inlined soon. To provide fraction scale, the final scale is scale following this option divided by 10
                                       EnableFatalErrorOnOOM                  Enabling failfast fatal error on OOM
                                 DeferLoadingAvailableSource                  Treat available source code as a dummy defer-mappable object to go through that code path.
                                                 ForceNative                  Force JIT everything that is called before running it, ignoring limits
                                             ForceSerialized                  Always serialize and deserialize byte codes before execution
                         ForceSerializedBytecodeMajorVersion [:Number]        Force the byte code serializer to write this major version number
                        ForceSerializedBytecodeVersionSchema [:Number]        Force the byte code serializer to write this kind of version. Decimal 10 is engineering, 20 is release mode, and 0 means use the default setting.
                                             ForceStrictMode                  Force strict mode checks on all functions
                                              ForceUndoDefer                  Defer parsing of all function bodies, but undo deferral
                              ForceBlockingConcurrentCollect                  Force doing in-thread GC on concurrent thread- this will skip doing concurrent collect
                                             FreTestDiagMode                  Enabled collection of diagnostic information on fretest builds
                                         ByteCodeBranchLimit [:Number]        Short branch limit before we use the branch island
                                        MediumByteCodeLayout                  Always use medium layout for bytecodes
                                         LargeByteCodeLayout                  Always use large layout for bytecodes
                                              FaultInjection [:Number]        FaultInjectMode - 0 (count only), 1 (count equal), 2 (count at or above), 3 (stackhashing)
                                         FaultInjectionCount [:Number]        Injects an out of memory at the specified allocation
                                          FaultInjectionType [:String]        FaultType (flag values) -  1 (Throw), 2 (NoThrow), 4 (MarkThrow), 8 (MarkNoThrow), FFFFFFFF (All)
                                        FaultInjectionFilter [:String]        A string to restrict the fault injection, the string can be like ArenaAllocator name
                                     FaultInjectionAllocSize [:Number]        Do fault injection only this size
                                     FaultInjectionStackFile [:String]        Stacks to match, default: stack.txt in current directory
                                FaultInjectionStackLineCount [:Number]        Count of lines in the stack file used for matching
                                     FaultInjectionStackHash [:String]        Match stacks hash on Chakra frames to inject the fault, hex string
                 FaultInjectionScriptContextToTerminateCount [:Number]        Script context# COUNT % (Number of script contexts) to terminate
                                        InduceCodeGenFailure [:Number]        Probability of a codegen job failing.
                                    InduceCodeGenFailureSeed [:Number]        Seed used while calculating codegen failure probability
             InjectPartiallyInitializedInterpreterFrameError [:Number]        The number of interpreter stack frame (with 1 being bottom-most) to inject error before the frame is initialized.
         InjectPartiallyInitializedInterpreterFrameErrorType [:Number]        Type of error to inject: 0 - debug break, 1 - exception.
                   GenerateByteCodeBufferReturnsCantGenerate                  Serialized byte code generation always returns SCRIPT_E_CANT_GENERATE
                                        GoptCleanupThreshold [:Number]        Number of instructions seen before we cleanup the value table
                                     AsmGoptCleanupThreshold [:Number]        Number of instructions seen before we cleanup the value table
                                           HighPrecisionDate                  Enable sub-millisecond resolution in Javascript Date for benchmark timing
                                              InlineCountMax [:Number]        Maximum count in bytecodes to inline in a given function
                                  InlineCountMaxInLoopBodies [:Number]        Maximum count in bytecodes to inline in a given function
                                                     icminlb [:Number]        Maximum count in bytecodes to inline in a given function
                             InlineInLoopBodyScaleDownFactor [:Number]        Maximum depth of a recursive inline call
                                                     iilbsdf [:Number]        Maximum depth of a recursive inline call
                                             InlineThreshold [:Number]        Maximum size in bytecodes of an inline candidate
                                    AggressiveInlineCountMax [:Number]        Maximum count in bytecodes to inline in a given function
                                   AggressiveInlineThreshold [:Number]        Maximum size in bytecodes of an inline candidate for aggressive inlining
                   InlineThresholdAdjustCountInLargeFunction [:Number]        Adjustment in the maximum size in bytecodes of an inline candidate in a large function
             InlineThresholdAdjustCountInMediumSizedFunction [:Number]        Adjustment in the maximum size in bytecodes of an inline candidate in a medium sized function
                   InlineThresholdAdjustCountInSmallFunction [:Number]        Adjustment in the maximum size in bytecodes of an inline candidate in a small function
                                           AsmJsInlineAdjust [:Number]        Adjustment in the maximum size in bytecodes of an inline candidate for wasm function
                                                   Interpret [:String]        List of functions to interpret
                                                  Instrument [:Phase]         Instrument the generated code from the given phase
                                           JitQueueThreshold [:Number]        Max number of work items/script context in the jit queue
                                                  LeakReport [:String]        File name for the leak report
                                         LoopInlineThreshold [:Number]        Maximum size in bytecodes of an inline candidate with loops or not enough profile data
                                         LeafInlineThreshold [:Number]        Maximum size in bytecodes of an inline candidate with loops or not enough profile data
                             ConstantArgumentInlineThreshold [:Number]        Maximum size in bytecodes of an inline candidate with constant argument and the argument being used for a branch
                                    RecursiveInlineThreshold [:Number]        Maximum size in bytecodes of an inline candidate to inline recursively
                                     RecursiveInlineDepthMax [:Number]        Maximum depth of a recursive inline call
                                     RecursiveInlineDepthMin [:Number]        Maximum depth of a recursive inline call
                                               RedeferralCap [:Number]        Number of compilations beyond which we stop redeferring a function
                                                        Loop [:Number]        Number of times to execute the script (useful for profiling short benchmarks and finding leaks)
                                          LoopInterpretCount [:Number]        Number of times loop has to be interpreted before JIT Loop body
                                                         lic [:Number]        Number of times loop has to be interpreted before JIT Loop body
                                       LoopProfileIterations [:Number]        Number of iterations of a loop that must be profiled before jitting the loop body
                                  OutsideLoopInlineThreshold [:Number]        Maximum size in bytecodes of an inline candidate outside a loop in inliner
                                          MaxFuncInlineDepth [:Number]        Number of times to allow inlining a function recursively, plus one (min: 1, max: 255)
                                 MaxNumberOfInlineesWithLoop [:Number]        Number of times to allow inlinees with a loop in a top function
                                                    Memspect [:Phase]         Enables memspect tracking to perform memory investigations.
                                  PolymorphicInlineThreshold [:Number]        Maximum size in bytecodes of a polymorphic inline candidate
                                               PrimeRecycler                  Prime the recycler first
                                                 PrivateHeap                  Use HeapAlloc with a private heap
                                         TraceEngineRefcount                  Output traces for ScriptEngine AddRef/Release to debug lifetime management
                                              LeakStackTrace                  Include stack trace on leaked pinned object and heap objects
                                             ForceMemoryLeak                  Fake leak some memory to test leak report and check memory leak
                                            DumpAfterFinalGC                  Collect a process dump after calling finalgc
                                             ForceOldDateAPI                  Force Chakra to use old dates API regardless of availability of a new one
                                 JitLoopBodyHotLoopThreshold [:Number]        Number of times loop has to be iterated in jitloopbody before it is determined as hot
                          LoopBodySizeThresholdToDisableOpts [:Number]        Minimum bytecode size of a loop body, above which we might consider switching off optimizations in jit loop body to avoid rejits
                                           MaxJitThreadCount [:Number]        Number of maximum allowed parallel jit threads (actual number is factor of number of processors and other heuristics)
                                      ForceMaxJitThreadCount                  Force the number of parallel jit threads as specified by MaxJitThreadCount flag (creation guaranteed)
                                             MitigateSpectre                  Use mitigations for Spectre
                                          PoisonVarArrayLoad                  Poison loads from Var arrays
                                          PoisonIntArrayLoad                  Poison loads from Int arrays
                                        PoisonFloatArrayLoad                  Poison loads from Float arrays
                                        PoisonTypedArrayLoad                  Poison loads from TypedArrays
                                            PoisonStringLoad                  Poison indexed loads from strings
                                       PoisonObjectsForLoads                  Poison objects after type checks for loads
                                         PoisonVarArrayStore                  Poison stores to Var arrays
                                         PoisonIntArrayStore                  Poison stores to Int arrays
                                       PoisonFloatArrayStore                  Poison stores to Float arrays
                                       PoisonTypedArrayStore                  Poison stores to TypedArrays
                                           PoisonStringStore                  Poison indexed stores to strings
                                      PoisonObjectsForStores                  Poison objects after type checks for stores
                                           MinInterpretCount [:Number]        Minimum number of times a function must be interpreted
                                        MinSimpleJitRunCount [:Number]        Minimum number of times a function must be run in simple jit
                                           MaxInterpretCount [:Number]        Maximum number of times a function can be interpreted
                                                         Mic [:Number]        Maximum number of times a function can be interpreted
                                        MaxSimpleJitRunCount [:Number]        Maximum number of times a function will be run in SimpleJitted code
                                                       Msjrc [:Number]        Maximum number of times a function will be run in SimpleJitted code
                                               MinMemOpCount [:Number]        Minimum count of a loop to activate MemOp
                                                        Mmoc [:Number]        Minimum count of a loop to activate MemOp
                                  MaxCopyOnAccessArrayLength [:Number]        Maximum length of copy-on-access array
                                  MinCopyOnAccessArrayLength [:Number]        Minimum length of copy-on-access array
                           CopyOnAccessArraySegmentCacheSize [:Number]        Size of copy-on-access array segment cache (1-32)
                                   MinTemplatizedJitRunCount [:Number]        Minimum number of times a function must be Templatized Jitted
                                 MinAsmJsInterpreterRunCount [:Number]        Minimum number of times a function must be Asm Interpreted
                               MinTemplatizedJitLoopRunCount [:Number]        Minimum LoopCount run of the Templatized Jit function to run FullJited
                                   MaxTemplatizedJitRunCount [:Number]        Maximum number of times a function must be templatized jit
                                                       Mtjrc [:Number]        Maximum number of times a function must be templatized jit
                                 MaxAsmJsInterpreterRunCount [:Number]        Maximum number of times a function must be interpreted in asmjs
                                                        Maic [:Number]        Maximum number of times a function must be interpreted in asmjs
                              AutoProfilingInterpreter0Limit [:Number]        Limit after which to transition to the next execution mode
                                  ProfilingInterpreter0Limit [:Number]        Limit after which to transition to the next execution mode
                              AutoProfilingInterpreter1Limit [:Number]        Limit after which to transition to the next execution mode
                                              SimpleJitLimit [:Number]        Limit after which to transition to the next execution mode
                                  ProfilingInterpreter1Limit [:Number]        Limit after which to transition to the next execution mode
                                         ExecutionModeLimits [:String]        Execution mode limits in th form: AutoProfilingInterpreter0.ProfilingInterpreter0.AutoProfilingInterpreter1.SimpleJit.ProfilingInterpreter1 - Example: -ExecutionModeLimits:12.4.0.132.12
                                                         Eml [:String]        Execution mode limits in th form: AutoProfilingInterpreter0.ProfilingInterpreter0.AutoProfilingInterpreter1.SimpleJit.ProfilingInterpreter1 - Example: -ExecutionModeLimits:12.4.0.132.12
                                  EnforceExecutionModeLimits                  Enforces the execution mode limits such that they are never exceeded.
                                                        Eeml                  Enforces the execution mode limits such that they are never exceeded.
                                              SimpleJitAfter [:Number]        Number of calls to a function after which to simple-JIT the function
                                                         Sja [:Number]        Number of calls to a function after which to simple-JIT the function
                                                FullJitAfter [:Number]        Number of calls to a function after which to full-JIT the function. The function will be profiled for every iteration.
                                                         Fja [:Number]        Number of calls to a function after which to full-JIT the function. The function will be profiled for every iteration.
                                                NewSimpleJit                  Uses the new simple JIT
                                       MaxLinearIntCaseCount [:Number]        Maximum number of cases(in switch statement) for which instructions can be generated linearly
                               MaxSingleCharStrJumpTableSize [:Number]        Maximum single char string jump table size
                              MaxSingleCharStrJumpTableRatio [:Number]        Maximum single char string jump table size as multiples of the actual case arm
                                      MinSwitchJumpTableSize [:Number]        Minimum size of the jump table, that is created for consecutive integer case arms in a Switch Statement
                                    MaxLinearStringCaseCount [:Number]        Maximum number of string cases(in switch statement) for which instructions can be generated linearly
                                   MinDeferredFuncTokenCount [:Number]        Minimum length in tokens of defer-parsed function
                             SkipFuncCountForBailOnNoProfile [:Number]        Initial Number of functions in a func body to be skipped from forcibly inserting BailOnNoProfile.
                            MaxJITFunctionBytecodeByteLength [:Number]        The biggest function we'll JIT (bytecode bytelength)
                                 MaxJITFunctionBytecodeCount [:Number]        The biggest function we'll JIT (bytecode count)
                                         MaxLoopsPerFunction [:Number]        Maximum number of loops in any function in the script
                              FuncObjectInlineCacheThreshold [:Number]        Maximum number of inline caches a function body may have to allow for inline caches to be allocated on the function object
                                                NoDeferParse                  Disable deferred parsing
                                                      NoLogo                  No logo, which we don't display anyways
                                           OOPJITMissingOpts                  Use optimizations that are missing from OOP JIT
                                        CrashOnOOPJITFailure                  Crash runtime process if JIT process crashes
                                          OOPCFGRegistration                  Do CFG registration OOP (under OOP JIT)
                                            ForceJITCFGCheck                  Have JIT code always do CFG check even if range check succeeded
                                            UseJITTrampoline                  Use trampoline for JIT entry points and emit range checks for it
                                                    NoNative                  Disable native codegen
                                                NopFrequency [:Number]        Frequency of NOPs inserted by NOP insertion phase.  A NOP is guaranteed to be inserted within a range of (1<<n) instrs (default=8)
                                                NoStrictMode                  Disable strict mode checks on all functions
                                              NormalizeStats                  When dumping stats, do some normalization (used with -instrument:linearscan)
                                                         Off [:Phase]         Turn off specific phases or feature.(Might not work for all phases)
                                         OffProfiledByteCode [:Phase]         Turn off specific byte code for phases or feature.(Might not work for all phases)
                                                          On [:Phase]         Turn on specific phases or feature.(Might not work for all phases)
                                                  OutputFile [:String]        Log the output to a specified file. Default: output.log in the working directory.
                                          OutputFileOpenMode [:String]        File open mode for OutputFile. Default: wt, specify 'at' for append
                                               InMemoryTrace                  Enable in-memory trace (investigate crash using trace in dump file). Use !jd.dumptrace to print it.
                                     InMemoryTraceBufferSize [:Number]        The size of circular buffer for in-memory trace (the units used is: number of trace calls). 
                                             RichTraceFormat                  Whether to use extra data in Output/Trace header.
                                              TraceWithStack                  Whether the trace need to include stack trace (for each trace entry).
                             PrintRunTimeDataCollectionTrace                  Print traces needed for runtime data collection
                                                      Prejit                  Prejit everything, including things that are not called, ignoring limits (default: false)
                                              PrintSrcInDump                  Print the lineno and the source code in the intermediate dumps
                                           ProfileDictionary [:Number]        Profile dictionary usage. Only dictionaries with max depth of <number> or above are displayed (0=no filter).
                                                     Profile [:Phase]         Profile the given phase
                                            ProfileThreshold [:Number]        A phase is displayed in the profiler report only if its contribution is more than this threshold
                                        ProfileObjectLiteral                  Profile Object literal usage
                                               ProfileMemory [:String]        Profile memory usage
                                              ProfileStrings                  Profile string statistics
                                                ProfileTypes                  Profile type statistics
                                              ProfileEvalMap                  Profile eval map statistics
                                  ProfileBailOutRecordMemory                  Profile bailout record memory statistics
                                           ValidateIntRanges                  Validate at runtime int ranges/bounds determined by the globopt
                                        RejitMaxBailOutCount [:Number]        Maximum number of bailouts for a bailout record after which rejit is forced
                                CallsToBailoutsRatioForRejit [:Number]        Ratio of function calls to bailouts above which a rejit is considered
                       LoopIterationsToBailoutsRatioForRejit [:Number]        Ratio of loop iteration count to bailouts above which a rejit of the loop body is considered
                                      MinBailOutsBeforeRejit [:Number]        Minimum number of bailouts for a single bailout record after which a rejit is considered
                              MinBailOutsBeforeRejitForLoops [:Number]        Minimum number of bailouts for a single bailout record after which a rejit is considered
                                           LibraryStackFrame                  Display library stack frame
                                   LibraryStackFrameDebugger                  Assume debugger support for library stack frame
                                              RecyclerStress                  Stress the recycler by collect on every allocation call
                                    RecyclerBackgroundStress                  Stress the recycler by collect in the background thread on every allocation call
                                    RecyclerConcurrentStress                  Stress the concurrent recycler by concurrent collect on every allocation call
                              RecyclerConcurrentRepeatStress                  Stress the concurrent recycler by concurrent collect on every allocation call and repeat mark and rescan in the background thread
                                       RecyclerPartialStress                  Stress the partial recycler by partial collect on every allocation call
                                         RecyclerTrackStress                  Stress tracked object handling by simulating tracked objects for regular allocations
                                RecyclerInduceFalsePositives                  Stress recycler by forcing false positive object marks
                                   RecyclerForceMarkInterior                  Force all the mark as interior
                                RecyclerPriorityBoostTimeout [:Number]        Adjust priority boost timeout
                                RecyclerThreadCollectTimeout [:Number]        Adjust thread collect timeout
                                  EnableConcurrentSweepAlloc                  Turns off the feature to allow allocations during concurrent sweep.
                                                        ecsa                  Turns off the feature to allow allocations during concurrent sweep.
                                                    PageHeap [:Number]        Use full page for heap allocations
                                          PageHeapAllocStack                  Capture alloc stack under page heap mode
                                           PageHeapFreeStack                  Capture free stack under page heap mode
                                        PageHeapBucketNumber [:NumberRange]   Bucket numbers to be used for page heap allocations
                                           PageHeapBlockType [:Number]        Type of blocks to use page heap for
                                   PageHeapDecommitGuardPage                  Decommit page heap guard page
                                         RecyclerNoPageReuse                  Do not reuse page in recycler
                                              RecyclerVerify [:Phase]         Verify recycler memory
                                       RecyclerVerifyPadSize [:Number]        Padding size to verify recycler memory
                                                RecyclerTest                  Run recycler tests instead of executing script
                                RecyclerProtectPagesOnRescan                  Temporarily switch all pages to read only during rescan
                                          RecyclerVerifyMark                  verify concurrent gc
                                                LowMemoryCap [:Number]        Memory cap indicating a low-memory process
                                 NewPagesCapDuringBGSweeping [:Number]        New pages count allowed to be allocated during background sweeping
                                            AllocPolicyLimit [:Number]        Memory allocation policy limit in MB (default: -1, which means no allocation policy limit).
                                       RuntimeDataOutputFile [:String]        Filename to write the dynamic profile info
                                                ReportErrors                  Enable reporting of syntax errors
                                              SpeculationCap [:Number]        How much bytecode we'll speculatively JIT
                                                       Stats [:Phase]         Stats the given phase
                                           SwallowExceptions                  Force a try/catch around every statement
                                        PrintSystemException                  Always print a message when there's OOM or OOS
                                     SwitchOptHolesThreshold [:Number]        Maximum percentage of holes (missing case values in a switch statement) with which a jump table can be created
                                                     TempMin [:Number]        Temp number switch which code can temporarily use for debugging
                                                     TempMax [:Number]        Temp number switch which code can temporarily use for debugging
                                                       Trace [:Phase]         Trace the given phase
                                           LoopAlignNopLimit [:Number]        Max number of nops for loop alignment
                                                 TraceMemory [:Phase]         Trace memory usage
                                        TraceMetaDataParsing [:Number]        Trace metadata parsing for generating JS projections. [Levels 1-5, with 5 corresponding to most detailed]
                                        TraceWin8Allocations                  Trace the win8 memory allocations
                             TraceWin8DeallocationsImmediate                  Trace the win8 memory deallocations immediately
                                      PrintWin8StatsDetailed                  Print the detailed memory trace report
                                           TraceProtectPages                  Trace calls to protecting pages of custom heap allocated pages
                                             TraceProjection [:Number]        Trace projection related activities, [Levels 1-3, with 3 corresponding to most detailed]
                                        TraceAsyncDebugCalls                  Trace calls to async debugging API (default: false)
                                               TrackDispatch                  Save stack traces of where JavascriptDispatch/HostVariant are created
                                                     Verbose                  Dump details
                                                 UseFullName                  Enable fully qualified name
                                       UseFunctionIdForTrace                  Use function id instead of function number for trace output
                                                        Utf8                  Use UTF8 for file output
                                                     Version [:Number]        Version in which to run the jscript engine. [one of 1,2,3,4,5,6]. Default is latest for jc/jshost, 1 for IE
                                         WERExceptionSupport                  WER feature for extended exception support. Enabled when WinRT is enabled
                               ExtendedErrorStackForTestHost                  Enable passing extended error stack string to test host.
                                             errorStackTrace                  error.StackTrace feature. Remove when feature complete
                                  DoHeapEnumOnEngineShutdown                  Perform a heap enumeration whenever shut a script engine down
                                                RegexTracing                  Trace all Regex invocations to the output.
                                                RegexProfile                  Collect usage statistics on all Regex invocations.
                                                  RegexDebug                  Trace compilation of UnifiedRegex expressions.
                                          RegexBytecodeDebug                  Display layout of UnifiedRegex bytecode (requires -RegexDebug to view).
                                               RegexOptimize                  Optimize regular expressions in the unified Regex system (default: true)
                                     DynamicRegexMruListSize [:Number]        Size of the MRU list for dynamic regexes
                                    OptimizeForManyInstances                  Optimize script engine for many instances (low memory footprint per engine, assume low spare CPU cycles) (default: false)
                                     EnableArrayTypeMutation                  Enable force array type mutation on re-entrant region
                                       ArrayMutationTestSeed [:Number]        Seed used for the array mutation
                                                   TestTrace [:Phase]         Test trace for the given phase
                                        EnableEvalMapCleanup                  Enable cleaning up the eval map
                                       TraceObjectAllocation                  Enable cleaning up the eval map
                                                         Sse [:Number]        Virtually disables SSE-based optimizations above the specified SSE level in the Chakra JIT (does not affect CRT SSE usage)
                               DeletedPropertyReuseThreshold [:Number]        Start reusing deleted property indexes after this many properties are deleted. Zero to disable reuse.
                 ForceStringKeyedSimpleDictionaryTypeHandler                  Force switch to string keyed version of SimpleDictionaryTypeHandler on first new property added to a SimpleDictionaryTypeHandler
                           BigDictionaryTypeHandlerThreshold [:Number]        Min Slot Capacity required to convert DictionaryTypeHandler to BigDictionaryTypeHandler.(Advisable to give more than 15 - to avoid false positive cases)
                                     TypeSnapshotEnumeration                  Create a true snapshot of the type of an object before enumeration and enumerate only those properties.
                                           EnumerationCompat                  When set in IE10 mode, restores enumeration behavior to RC behavior
                                           IsolatePrototypes                  Should prototypes get unique types not shared with other objects (default: true)?
                                           ChangeTypeOnProto                  When becoming a prototype should the object switch to a new type (default: true)?
                                           ShareInlineCaches                  Determines whether inline caches are shared between all loads (or all stores) of the same property ID
                                          DisableDebugObject                  Disable test only Debug object properties
                                                    DumpHeap                  enable Debug.dumpHeap even when DisableDebugObject is set
                                                   autoProxy [:String]        enable creating proxy for each object creation
                                               PerfHintLevel [:Number]        Specifies the perf-hint level (1,2) 1 == critical, 2 == only noisy
                                        MemProtectHeapStress                  Stress the recycler by collect on every allocation call
                              MemProtectHeapBackgroundStress                  Stress the recycler by collect in the background thread on every allocation call
                              MemProtectHeapConcurrentStress                  Stress the concurrent recycler by concurrent collect on every allocation call
                        MemProtectHeapConcurrentRepeatStress                  Stress the concurrent recycler by concurrent collect on every allocation call and repeat mark and rescan in the background thread
                                 MemProtectHeapPartialStress                  Stress the partial recycler by partial collect on every allocation call
                                         FixPropsOnPathTypes                  Mark properties as fixed on path types (default: false).
                                          BailoutTraceFilter [:NumberSet]     Filter the bailout trace messages to specific bailout kinds.
                                            RejitTraceFilter [:NumberSet]     Filter the rejit trace messages to specific bailout kinds.
                                MaxBackgroundFinishMarkCount [:Number]        Maximum number of background finish mark
                                BackgroundFinishMarkWaitTime [:Number]        Millisecond to wait for background finish mark
                          MinBackgroundRepeatMarkRescanBytes [:Number]        Minimum number of bytes rescan to trigger background finish mark
                              ZeroMemoryWithNonTemporalStore                  Zero free memory with non-temporal stores to avoid evicting other content from processor cache
                                       MaxMarkStackPageCount [:Number]        Restrict recycler mark stack size (in pages)
                                   MaxTrackedObjectListCount [:Number]        Restrict recycler tracked object count during GC
                                         NumberAllocPlusSize [:Number]        Additional bytes to allocate with JavascriptNumber from number allocator (0~496)
               InitializeInterpreterSlotsWithInvalidStackVar                  Enable the initialization of the interpreter local slots with invalid stack vars
                                                   PRNGSeed0 [:Number]        Override seed0 for Math.Random()
                                                   PRNGSeed1 [:Number]        Override seed1 for Math.Random()
                                  ClearInlineCachesOnCollect                  Clear all inline caches on every garbage collection
              InlineCacheInvalidationListCompactionThreshold [:Number]        Compact inline cache invalidation lists if their utilization falls below this threshold
                       ConstructorCacheInvalidationThreshold [:Number]        Clear uniquePropertyGuard entries from recyclableData if number of invalidations of constructor caches happened are more than the threshold.
                   InvalidateSolutionContextsForGetStructure                  To reduce memory consumption, in the end of GetStructure call, invalidate script contexts used only for GetStructure -- this would invalidate ones associated with solution files (not top-most references such as helpers.js)
                                                  ES5LangTel                  Print ES5 language telemetry output.
                                                  ES6LangTel                  Print ES6 language telemetry output.
                                                  ESBLangTel                  Print ES built-ins telemetry output.
                                                DateParseTel                  Print Date.parse telemetry output.
                                           GCMemoryThreshold [:Number]        Threshold for allocation-based GC initiation (in MB)
                                        PreReservedHeapAlloc                  Enable Pre-reserved Heap Page Allocator
                                                    CFGInJit                  Enable CFG check in JIT
                                                         CFG                  Force enable CFG on jshost. version in the jshost's manifest file disables CFG
             SimulatePolyCacheWithOneTypeForInlineCacheIndex [:Number]        Use with SimulatePolyCacheWithOneTypeForFunction to simulate creating a polymorphic inline cache containing only one type due to a collision, for testing ObjTypeSpec
                                        JITServerIdleTimeout [:Number]        Idle timeout in milliseconds to do the cleanup in JIT server
                      JITServerMaxInactivePageAllocatorCount [:Number]        Max inactive page allocators to keep before schedule a cleanup
                                     StrictWriteBarrierCheck                  Check write barrier setting on none write barrier pages
                                            WriteBarrierTest                  Always return true while checking barrier to test recycler regardless of annotation
                                   ForceSoftwareWriteBarrier                  Use to turn off write watch to test software write barrier on windows
                                            VerifyBarrierBit                  Verify software write barrier bit is set while marking
                                            EnableBGFreeZero                  Use to turn off background freeing and zeroing to simulate linux
                                       KeepRecyclerTrackData                  Keep recycler track data after sweep until reuse
                                      MaxSingleAllocSizeInMB [:Number]        Max size(in MB) in single allocation

Usage: ch.exe [-v|-version] [-h|-help] [-?] [flaglist] <source file>
	-v|-version		Displays version info
	-h|-help		Displays this help message
	-?			Displays this help message with complete [flaglist] info

Host Config Flags: 

         dbgbaseline          	"Baseline file to compare debugger output"
         DebugLaunch          	"Create the test debugger and execute test in the debug mode"
GenerateLibraryByteCodeHeader          	"Generate bytecode header file from library code"
GenerateParserStateCache          	"Parse source file to create parser state cache and write it to file or console"
 UseParserStateCache          	"Create parser state cache while parsing and use it during script execution"
InspectMaxStringLength          	"Max string length to dump in locals inspection"
          Serialized          	"If source is UTF8, deserializes from bytecode file"
              OOPJIT          	"Run JIT in a separate process"
EnsureCloseJITServer          	"JIT process will be force closed when ch is terminated"
IgnoreScriptErrorCode          	"Don't return error code on script error"
    MuteHostErrorMsg          	"Mute host error output, e.g. module load failures"
   TraceHostCallback          	"Output traces for host callbacks"
             Test262          	"load Test262 harness"
TrackRejectedPromises          	"Enable tracking of unhandled promise rejections"
    CustomConfigFile          	"Custom config file to be used to pass in additional flags to Chakra"
  ExecuteWithBgParse          	"[No-op] Load script with bgparse (note: requires bgparse to be on as well)"
