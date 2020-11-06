---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a66ed7e910b5b9fbd1057d50e2fa3e5058400855
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514415"
---
# <span data-ttu-id="36299-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="36299-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="36299-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36299-102">SYNOPSIS</span></span>
<span data-ttu-id="36299-103">Aggiorna un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="36299-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36299-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36299-104">SYNTAX</span></span>

### <span data-ttu-id="36299-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36299-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36299-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="36299-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36299-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="36299-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36299-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36299-108">DESCRIPTION</span></span>
<span data-ttu-id="36299-109">Il cmdlet **Update-AzureRmDataFactoryV2IntegrationRuntime** aggiorna le proprietà di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="36299-109">The **Update-AzureRmDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="36299-110">Attualmente il cmdlet supporta solo l'aggiornamento di "AutoUpdate" e "AutoUpdateDelayOffset" per l'integrazione autonoma di Runtime.</span><span class="sxs-lookup"><span data-stu-id="36299-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="36299-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36299-111">EXAMPLES</span></span>

### <span data-ttu-id="36299-112">Esempio 1: aggiorna un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="36299-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntime `
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

<span data-ttu-id="36299-113">Il cmdlet aggiorna l'integrazione di runtime indipendente denominata "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="36299-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="36299-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36299-114">PARAMETERS</span></span>

### <span data-ttu-id="36299-115">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="36299-115">-AutoUpdate</span></span>
<span data-ttu-id="36299-116">Abilitare o disabilitare l'aggiornamento automatico di runtime self-hosted Integration.</span><span class="sxs-lookup"><span data-stu-id="36299-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36299-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="36299-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="36299-118">L'ora in ore del giorno per l'aggiornamento automatico di runtime self-hosted Integration.</span><span class="sxs-lookup"><span data-stu-id="36299-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36299-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="36299-119">-DataFactoryName</span></span>
<span data-ttu-id="36299-120">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="36299-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36299-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36299-121">-DefaultProfile</span></span>
<span data-ttu-id="36299-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36299-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36299-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36299-123">-InputObject</span></span>
<span data-ttu-id="36299-124">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="36299-124">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36299-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="36299-125">-Name</span></span>
<span data-ttu-id="36299-126">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="36299-126">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36299-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36299-127">-ResourceGroupName</span></span>
<span data-ttu-id="36299-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36299-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36299-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36299-129">-ResourceId</span></span>
<span data-ttu-id="36299-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="36299-130">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36299-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36299-131">-Confirm</span></span>
<span data-ttu-id="36299-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36299-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36299-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36299-133">-WhatIf</span></span>
<span data-ttu-id="36299-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36299-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36299-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36299-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36299-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36299-136">CommonParameters</span></span>
<span data-ttu-id="36299-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36299-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36299-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36299-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36299-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36299-139">INPUTS</span></span>

### <span data-ttu-id="36299-140">System. String</span><span class="sxs-lookup"><span data-stu-id="36299-140">System.String</span></span>
<span data-ttu-id="36299-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="36299-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="36299-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36299-142">OUTPUTS</span></span>

### <span data-ttu-id="36299-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="36299-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="36299-144">Note</span><span class="sxs-lookup"><span data-stu-id="36299-144">NOTES</span></span>
<span data-ttu-id="36299-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="36299-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="36299-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36299-146">RELATED LINKS</span></span>

<span data-ttu-id="36299-147">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="36299-147">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

