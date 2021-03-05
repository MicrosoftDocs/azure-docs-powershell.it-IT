---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: fa9e9e0b2de02a320cb5140aac21e30f7c2b5bbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006909"
---
# <span data-ttu-id="93543-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="93543-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="93543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93543-102">SYNOPSIS</span></span>
<span data-ttu-id="93543-103">Aggiorna un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="93543-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="93543-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93543-104">SYNTAX</span></span>

### <span data-ttu-id="93543-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93543-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93543-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="93543-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93543-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="93543-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93543-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="93543-108">DESCRIPTION</span></span>
<span data-ttu-id="93543-109">Il cmdlet **Update-AzDataFactoryV2IntegrationRuntime aggiorna** le proprietà di runtime dell'integrazione.</span><span class="sxs-lookup"><span data-stu-id="93543-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="93543-110">Attualmente il cmdlet supporta solo l'aggiornamento di "AutoUpdate" e "AutoUpdateDelayGraf" per il runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="93543-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="93543-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93543-111">EXAMPLES</span></span>

### <span data-ttu-id="93543-112">Esempio 1: Aggiorna un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="93543-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzDataFactoryV2IntegrationRuntime `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -Name 'test-selfhost-ir' `
    -AutoUpdate Off `
    -AutoUpdateDelayOffset $ts

Nodes                     : {Node_1}
CreateTime                : 11/18/2017 2:45:38 PM
InternalChannelEncryption : 
Version                   : 3.2.6519.3
Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
ScheduledUpdateDate       : 
UpdateDelayOffset         : 
LocalTimeZoneOffset       : 
AutoUpdate                : Off
ServiceUrls               : {wu.frontend.int.clouddatahub-int.net, *.servicebus.windows.net}
State                     : Online
Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
Type                      : SelfHosted
ResourceGroupName         : rg-test-dfv2
DataFactoryName           : test-df-eu2
Name                      : test-selfhost-ir
Description               : New 2 description
```

<span data-ttu-id="93543-113">Il cmdlet aggiorna il runtime di integrazione self-hosted denominato "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="93543-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="93543-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93543-114">PARAMETERS</span></span>

### <span data-ttu-id="93543-115">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="93543-115">-AutoUpdate</span></span>
<span data-ttu-id="93543-116">Abilitare o disabilitare l'aggiornamento automatico del runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="93543-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93543-117">-AutoUpdateDelayGrafo</span><span class="sxs-lookup"><span data-stu-id="93543-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="93543-118">Ora del giorno per l'aggiornamento automatico del runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="93543-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93543-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="93543-119">-DataFactoryName</span></span>
<span data-ttu-id="93543-120">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="93543-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93543-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93543-121">-DefaultProfile</span></span>
<span data-ttu-id="93543-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93543-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93543-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93543-123">-InputObject</span></span>
<span data-ttu-id="93543-124">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="93543-124">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93543-125">-Name</span><span class="sxs-lookup"><span data-stu-id="93543-125">-Name</span></span>
<span data-ttu-id="93543-126">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="93543-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93543-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93543-127">-ResourceGroupName</span></span>
<span data-ttu-id="93543-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="93543-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93543-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93543-129">-ResourceId</span></span>
<span data-ttu-id="93543-130">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="93543-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93543-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93543-131">-Confirm</span></span>
<span data-ttu-id="93543-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93543-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93543-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93543-133">-WhatIf</span></span>
<span data-ttu-id="93543-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93543-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93543-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93543-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93543-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93543-136">CommonParameters</span></span>
<span data-ttu-id="93543-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93543-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93543-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93543-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93543-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="93543-139">INPUTS</span></span>

### <span data-ttu-id="93543-140">System.String</span><span class="sxs-lookup"><span data-stu-id="93543-140">System.String</span></span>

### <span data-ttu-id="93543-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="93543-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="93543-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93543-142">OUTPUTS</span></span>

### <span data-ttu-id="93543-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="93543-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="93543-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="93543-144">NOTES</span></span>
<span data-ttu-id="93543-145">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori, copia, attività, runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="93543-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="93543-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93543-146">RELATED LINKS</span></span>

<span data-ttu-id="93543-147">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="93543-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

