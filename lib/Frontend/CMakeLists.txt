add_swift_host_library(swiftFrontend STATIC
  ArgsToFrontendInputsConverter.cpp
  ArgsToFrontendOptionsConverter.cpp
  ArgsToFrontendOutputsConverter.cpp
  CompilerInvocation.cpp
  DiagnosticVerifier.cpp
  Frontend.cpp
  FrontendInputsAndOutputs.cpp
  FrontendOptions.cpp
  ParseableInterfaceModuleLoader.cpp
  ParseableInterfaceSupport.cpp
  PrintingDiagnosticConsumer.cpp
  SerializedDiagnosticConsumer.cpp
  DEPENDS
    SwiftOptions)
target_link_libraries(swiftFrontend PRIVATE
  swiftSIL
  swiftMigrator
  swiftOption
  swiftParseSIL
  swiftSILGen
  swiftSILOptimizer
  swiftSema
  swiftSerialization)

