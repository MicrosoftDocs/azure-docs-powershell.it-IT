---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 2a41a61b67ea77e2927acf5eef7b7d520464978a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198646"
---
# <span data-ttu-id="6f4b8-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6f4b8-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="6f4b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="6f4b8-103">Rimuovere un servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-103">Remove a service from the cluster.</span></span> <span data-ttu-id="6f4b8-104">Supporta solo i ARM distribuiti.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="6f4b8-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f4b8-105">SYNTAX</span></span>

### <span data-ttu-id="6f4b8-106">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6f4b8-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f4b8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f4b8-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f4b8-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6f4b8-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f4b8-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6f4b8-109">DESCRIPTION</span></span>
<span data-ttu-id="6f4b8-110">Questo cmdlet rimuove un servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="6f4b8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f4b8-111">EXAMPLES</span></span>

### <span data-ttu-id="6f4b8-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6f4b8-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="6f4b8-113">Questo esempio rimuove il servizio "testApp~testService1".</span><span class="sxs-lookup"><span data-stu-id="6f4b8-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="6f4b8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f4b8-114">PARAMETERS</span></span>

### <span data-ttu-id="6f4b8-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="6f4b8-115">-ApplicationName</span></span>
<span data-ttu-id="6f4b8-116">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-116">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f4b8-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6f4b8-117">-ClusterName</span></span>
<span data-ttu-id="6f4b8-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f4b8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f4b8-119">-DefaultProfile</span></span>
<span data-ttu-id="6f4b8-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f4b8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6f4b8-121">-Force</span></span>
<span data-ttu-id="6f4b8-122">Rimuovere senza richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="6f4b8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f4b8-123">-InputObject</span></span>
<span data-ttu-id="6f4b8-124">Risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-124">The service resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f4b8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6f4b8-125">-Name</span></span>
<span data-ttu-id="6f4b8-126">Specificare il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-126">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f4b8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f4b8-127">-PassThru</span></span>
<span data-ttu-id="6f4b8-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6f4b8-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6f4b8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f4b8-129">-ResourceGroupName</span></span>
<span data-ttu-id="6f4b8-130">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f4b8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f4b8-131">-ResourceId</span></span>
<span data-ttu-id="6f4b8-132">Arm ResourceId del servizio.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-132">Arm ResourceId of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f4b8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f4b8-133">-Confirm</span></span>
<span data-ttu-id="6f4b8-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f4b8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f4b8-135">-WhatIf</span></span>
<span data-ttu-id="6f4b8-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f4b8-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f4b8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f4b8-138">CommonParameters</span></span>
<span data-ttu-id="6f4b8-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f4b8-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f4b8-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="6f4b8-141">INPUTS</span></span>

### <span data-ttu-id="6f4b8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6f4b8-142">System.String</span></span>

### <span data-ttu-id="6f4b8-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="6f4b8-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="6f4b8-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f4b8-144">OUTPUTS</span></span>

### <span data-ttu-id="6f4b8-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f4b8-145">System.Boolean</span></span>

## <span data-ttu-id="6f4b8-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="6f4b8-146">NOTES</span></span>

## <span data-ttu-id="6f4b8-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f4b8-147">RELATED LINKS</span></span>
