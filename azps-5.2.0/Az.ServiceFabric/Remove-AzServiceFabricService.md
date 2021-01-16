---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 2a41a61b67ea77e2927acf5eef7b7d520464978a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357881"
---
# <span data-ttu-id="60e61-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="60e61-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="60e61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60e61-102">SYNOPSIS</span></span>
<span data-ttu-id="60e61-103">Rimuovere un servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="60e61-103">Remove a service from the cluster.</span></span> <span data-ttu-id="60e61-104">Supporta solo i servizi distribuiti con ARM.</span><span class="sxs-lookup"><span data-stu-id="60e61-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="60e61-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60e61-105">SYNTAX</span></span>

### <span data-ttu-id="60e61-106">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60e61-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60e61-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="60e61-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60e61-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="60e61-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60e61-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60e61-109">DESCRIPTION</span></span>
<span data-ttu-id="60e61-110">Questo cmdlet consente di rimuovere un modulo del servizio nel cluster.</span><span class="sxs-lookup"><span data-stu-id="60e61-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="60e61-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60e61-111">EXAMPLES</span></span>

### <span data-ttu-id="60e61-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60e61-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="60e61-113">In questo esempio viene rimosso il servizio "testApp ~ testService1".</span><span class="sxs-lookup"><span data-stu-id="60e61-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="60e61-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60e61-114">PARAMETERS</span></span>

### <span data-ttu-id="60e61-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="60e61-115">-ApplicationName</span></span>
<span data-ttu-id="60e61-116">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="60e61-116">Specify the name of the application.</span></span>

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

### <span data-ttu-id="60e61-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="60e61-117">-ClusterName</span></span>
<span data-ttu-id="60e61-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="60e61-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="60e61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e61-119">-DefaultProfile</span></span>
<span data-ttu-id="60e61-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60e61-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60e61-121">-Force</span><span class="sxs-lookup"><span data-stu-id="60e61-121">-Force</span></span>
<span data-ttu-id="60e61-122">Rimuovi senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="60e61-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="60e61-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60e61-123">-InputObject</span></span>
<span data-ttu-id="60e61-124">Risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="60e61-124">The service resource.</span></span>

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

### <span data-ttu-id="60e61-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="60e61-125">-Name</span></span>
<span data-ttu-id="60e61-126">Specificare il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="60e61-126">Specify the name of the service.</span></span>

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

### <span data-ttu-id="60e61-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60e61-127">-PassThru</span></span>
<span data-ttu-id="60e61-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="60e61-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="60e61-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60e61-129">-ResourceGroupName</span></span>
<span data-ttu-id="60e61-130">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60e61-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="60e61-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60e61-131">-ResourceId</span></span>
<span data-ttu-id="60e61-132">ARM ResourceId del servizio.</span><span class="sxs-lookup"><span data-stu-id="60e61-132">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="60e61-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60e61-133">-Confirm</span></span>
<span data-ttu-id="60e61-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60e61-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60e61-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e61-135">-WhatIf</span></span>
<span data-ttu-id="60e61-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60e61-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60e61-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60e61-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60e61-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e61-138">CommonParameters</span></span>
<span data-ttu-id="60e61-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60e61-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e61-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60e61-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e61-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60e61-141">INPUTS</span></span>

### <span data-ttu-id="60e61-142">System. String</span><span class="sxs-lookup"><span data-stu-id="60e61-142">System.String</span></span>

### <span data-ttu-id="60e61-143">Microsoft. Azure. Commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="60e61-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="60e61-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60e61-144">OUTPUTS</span></span>

### <span data-ttu-id="60e61-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60e61-145">System.Boolean</span></span>

## <span data-ttu-id="60e61-146">Note</span><span class="sxs-lookup"><span data-stu-id="60e61-146">NOTES</span></span>

## <span data-ttu-id="60e61-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60e61-147">RELATED LINKS</span></span>
