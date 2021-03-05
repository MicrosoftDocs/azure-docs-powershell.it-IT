---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: ca0f14bf6940c9d81933c4a42703d828efdc5e51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998421"
---
# <span data-ttu-id="310dd-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="310dd-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="310dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="310dd-102">SYNOPSIS</span></span>
<span data-ttu-id="310dd-103">Aggiorna il nodo di runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="310dd-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="310dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="310dd-104">SYNTAX</span></span>

### <span data-ttu-id="310dd-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="310dd-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="310dd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="310dd-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="310dd-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="310dd-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="310dd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="310dd-108">DESCRIPTION</span></span>
<span data-ttu-id="310dd-109">Il cmdlet **Update-AzDataFactoryV2IntegrationRuntimeNode** aggiorna le proprietà del nodo di runtime di integrazione self-hosted in un data factory.</span><span class="sxs-lookup"><span data-stu-id="310dd-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="310dd-110">Attualmente supporta solo l'aggiornamento di 'ConcurrentJobsLimit'.</span><span class="sxs-lookup"><span data-stu-id="310dd-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="310dd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="310dd-111">EXAMPLES</span></span>

### <span data-ttu-id="310dd-112">Esempio 1: Aggiornare il nodo di runtime di integrazione self-hosted</span><span class="sxs-lookup"><span data-stu-id="310dd-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="310dd-113">Il cmdlet aggiorna 'ConcurrentJobsLimit' a 3 per il nodo "Node_1" nel runtime di integrazione self-hosted 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="310dd-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="310dd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="310dd-114">PARAMETERS</span></span>

### <span data-ttu-id="310dd-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="310dd-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="310dd-116">Numero di processi simultanei consentiti nel nodo di runtime dell'integrazione.</span><span class="sxs-lookup"><span data-stu-id="310dd-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="310dd-117">Sono consentiti valori compresi tra 1 e maxConcurrentJobs.</span><span class="sxs-lookup"><span data-stu-id="310dd-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310dd-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="310dd-118">-DataFactoryName</span></span>
<span data-ttu-id="310dd-119">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="310dd-119">The data factory name.</span></span>

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

### <span data-ttu-id="310dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310dd-120">-DefaultProfile</span></span>
<span data-ttu-id="310dd-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="310dd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="310dd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="310dd-122">-InputObject</span></span>
<span data-ttu-id="310dd-123">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="310dd-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="310dd-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="310dd-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="310dd-125">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="310dd-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="310dd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="310dd-126">-Name</span></span>
<span data-ttu-id="310dd-127">Nome del nodo di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="310dd-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="310dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="310dd-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="310dd-129">The resource group name.</span></span>

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

### <span data-ttu-id="310dd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="310dd-130">-ResourceId</span></span>
<span data-ttu-id="310dd-131">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="310dd-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="310dd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="310dd-132">-Confirm</span></span>
<span data-ttu-id="310dd-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="310dd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="310dd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="310dd-134">-WhatIf</span></span>
<span data-ttu-id="310dd-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="310dd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="310dd-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="310dd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="310dd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310dd-137">CommonParameters</span></span>
<span data-ttu-id="310dd-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="310dd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310dd-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="310dd-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310dd-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="310dd-140">INPUTS</span></span>

### <span data-ttu-id="310dd-141">System.String</span><span class="sxs-lookup"><span data-stu-id="310dd-141">System.String</span></span>

### <span data-ttu-id="310dd-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="310dd-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="310dd-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="310dd-143">OUTPUTS</span></span>

### <span data-ttu-id="310dd-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="310dd-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="310dd-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="310dd-145">NOTES</span></span>
<span data-ttu-id="310dd-146">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori, copia, attività, runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="310dd-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="310dd-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="310dd-147">RELATED LINKS</span></span>

<span data-ttu-id="310dd-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="310dd-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

