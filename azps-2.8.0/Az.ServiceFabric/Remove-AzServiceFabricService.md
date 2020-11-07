---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 1314eb4d6bf4cfa802e0c6f40cc5ae7646209572
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854542"
---
# <span data-ttu-id="a1b1d-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="a1b1d-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="a1b1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b1d-103">Rimuovere un servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-103">Remove a service from the cluster.</span></span>

## <span data-ttu-id="a1b1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1b1d-104">SYNTAX</span></span>

### <span data-ttu-id="a1b1d-105">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1b1d-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1b1d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b1d-106">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b1d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a1b1d-107">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1b1d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1b1d-108">DESCRIPTION</span></span>
<span data-ttu-id="a1b1d-109">Questo cmdlet consente di rimuovere un modulo del servizio nel cluster.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-109">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="a1b1d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1b1d-110">EXAMPLES</span></span>

### <span data-ttu-id="a1b1d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1b1d-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="a1b1d-112">In questo esempio viene rimosso il servizio "testApp ~ testService1".</span><span class="sxs-lookup"><span data-stu-id="a1b1d-112">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="a1b1d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1b1d-113">PARAMETERS</span></span>

### <span data-ttu-id="a1b1d-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="a1b1d-114">-ApplicationName</span></span>
<span data-ttu-id="a1b1d-115">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-115">Specify the name of the application.</span></span>

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

### <span data-ttu-id="a1b1d-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="a1b1d-116">-ClusterName</span></span>
<span data-ttu-id="a1b1d-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a1b1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b1d-118">-DefaultProfile</span></span>
<span data-ttu-id="a1b1d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b1d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a1b1d-120">-Force</span></span>
<span data-ttu-id="a1b1d-121">Rimuovi senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="a1b1d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1b1d-122">-InputObject</span></span>
<span data-ttu-id="a1b1d-123">Risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-123">The service resource.</span></span>

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

### <span data-ttu-id="a1b1d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1b1d-124">-Name</span></span>
<span data-ttu-id="a1b1d-125">Specificare il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-125">Specify the name of the service.</span></span>

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

### <span data-ttu-id="a1b1d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1b1d-126">-PassThru</span></span>
<span data-ttu-id="a1b1d-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a1b1d-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a1b1d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b1d-128">-ResourceGroupName</span></span>
<span data-ttu-id="a1b1d-129">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a1b1d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b1d-130">-ResourceId</span></span>
<span data-ttu-id="a1b1d-131">ARM ResourceId del servizio.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-131">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="a1b1d-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1b1d-132">-Confirm</span></span>
<span data-ttu-id="a1b1d-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b1d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b1d-134">-WhatIf</span></span>
<span data-ttu-id="a1b1d-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1b1d-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b1d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b1d-137">CommonParameters</span></span>
<span data-ttu-id="a1b1d-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b1d-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b1d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b1d-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1b1d-140">INPUTS</span></span>

### <span data-ttu-id="a1b1d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a1b1d-141">System.String</span></span>

### <span data-ttu-id="a1b1d-142">Microsoft. Azure. Commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="a1b1d-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="a1b1d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1b1d-143">OUTPUTS</span></span>

### <span data-ttu-id="a1b1d-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1b1d-144">System.Boolean</span></span>

## <span data-ttu-id="a1b1d-145">Note</span><span class="sxs-lookup"><span data-stu-id="a1b1d-145">NOTES</span></span>

## <span data-ttu-id="a1b1d-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1b1d-146">RELATED LINKS</span></span>
