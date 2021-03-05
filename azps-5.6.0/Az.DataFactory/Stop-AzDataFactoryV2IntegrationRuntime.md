---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 405754afec3ff62eb59d385646df43f699557d18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998491"
---
# <span data-ttu-id="df5a8-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="df5a8-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="df5a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="df5a8-103">Interrompe un runtime di integrazione dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="df5a8-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="df5a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df5a8-104">SYNTAX</span></span>

### <span data-ttu-id="df5a8-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="df5a8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df5a8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df5a8-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df5a8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="df5a8-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df5a8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="df5a8-108">DESCRIPTION</span></span>
<span data-ttu-id="df5a8-109">Il cmdlet **Stop-AzDataFactoryV2IntegrationRuntime** interrompe un runtime di integrazione dedicato gestito in stato "Avviato", che è stato avviato dal cmdlet Start-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="df5a8-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="df5a8-110">Le risorse vengono rilasciate e lo stato viene trasferire in "Arrestato".</span><span class="sxs-lookup"><span data-stu-id="df5a8-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="df5a8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df5a8-111">EXAMPLES</span></span>

### <span data-ttu-id="df5a8-112">Esempio 1: Arrestare un runtime di integrazione gestita in stato "Avviato".</span><span class="sxs-lookup"><span data-stu-id="df5a8-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="df5a8-113">Il runtime di integrazione gestita 'test-reserlved-ir' è in stato "Avviato".</span><span class="sxs-lookup"><span data-stu-id="df5a8-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="df5a8-114">Dopo aver Stop-AzDataFactoryV2IntegrationRuntime cmdlet, le risorse vengono rilasciate e lo stato viene trasferimento a "Arrestato".</span><span class="sxs-lookup"><span data-stu-id="df5a8-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="df5a8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df5a8-115">PARAMETERS</span></span>

### <span data-ttu-id="df5a8-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="df5a8-116">-DataFactoryName</span></span>
<span data-ttu-id="df5a8-117">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="df5a8-117">The data factory name.</span></span>

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

### <span data-ttu-id="df5a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5a8-118">-DefaultProfile</span></span>
<span data-ttu-id="df5a8-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df5a8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df5a8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="df5a8-120">-Force</span></span>
<span data-ttu-id="df5a8-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="df5a8-121">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df5a8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df5a8-122">-InputObject</span></span>
<span data-ttu-id="df5a8-123">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="df5a8-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="df5a8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="df5a8-124">-Name</span></span>
<span data-ttu-id="df5a8-125">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="df5a8-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="df5a8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df5a8-126">-ResourceGroupName</span></span>
<span data-ttu-id="df5a8-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="df5a8-127">The resource group name.</span></span>

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

### <span data-ttu-id="df5a8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df5a8-128">-ResourceId</span></span>
<span data-ttu-id="df5a8-129">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="df5a8-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="df5a8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df5a8-130">-Confirm</span></span>
<span data-ttu-id="df5a8-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df5a8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df5a8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df5a8-132">-WhatIf</span></span>
<span data-ttu-id="df5a8-133">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="df5a8-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="df5a8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5a8-134">CommonParameters</span></span>
<span data-ttu-id="df5a8-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df5a8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5a8-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df5a8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5a8-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="df5a8-137">INPUTS</span></span>

### <span data-ttu-id="df5a8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="df5a8-138">System.String</span></span>

### <span data-ttu-id="df5a8-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="df5a8-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="df5a8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df5a8-140">OUTPUTS</span></span>

### <span data-ttu-id="df5a8-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="df5a8-141">System.Void</span></span>

## <span data-ttu-id="df5a8-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="df5a8-142">NOTES</span></span>
<span data-ttu-id="df5a8-143">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori, copia, attività, runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="df5a8-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="df5a8-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df5a8-144">RELATED LINKS</span></span>

[<span data-ttu-id="df5a8-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="df5a8-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
